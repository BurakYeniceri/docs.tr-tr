---
title: .NET core uygulama dağıtımı
description: Bir .NET Core uygulamasını dağıtma.
author: rpetrusha
ms.author: ronpet
ms.date: 09/03/2018
ms.openlocfilehash: 390af06e81788c3f64f255e5c85efdaa167274f4
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48836634"
---
# <a name="net-core-application-deployment"></a>.NET core uygulama dağıtımı

İki .NET Core uygulamaları için dağıtım türleri oluşturabilirsiniz:

- Framework bağımlı dağıtım. Adından da anlaşılacağı gibi .NET Core hedef sistemdeki bir paylaşılan sistem genelinde sürüm varlığını framework bağımlı dağıtım (FDD) kullanır. .NET Core zaten mevcut olduğundan, uygulamanızı de .NET Core yüklemeleri arasında taşınabilir. Uygulamanızı, yalnızca kendi kodunu ve .NET Core kitaplıklar dışında herhangi bir üçüncü taraf bağımlılıkları içerir. FDDs içeren *.dll* kullanılarak başlatılabilen dosyaları [dotnet yardımcı programı](../tools/dotnet.md) komut satırından. Örneğin, `dotnet app.dll` adlı bir uygulamayı çalıştıran `app`.

- Kendi başına dağıtım. FDD, hedef sistemde paylaşılan Bileşenler'in kendi içinde bir dağıtım (SCD) içermez. .NET Core kitaplıkları ve .NET Core çalışma zamanı hem de dahil olmak üzere tüm bileşenlerin uygulama ile birlikte ve diğer .NET Core uygulamalardan yalıtılır. SCDs içeren bir yürütülebilir dosya (gibi *app.exe* adlı bir uygulama için Windows platformlarında `app`), platforma özgü .NET Core konak adı bir sürümü olduğu ve bir *.dll* (örneğin, dosya *app.dll*), gerçek uygulama olduğu.

## <a name="framework-dependent-deployments-fdd"></a>Framework bağımlı dağıtımlar (FDD)

Bir FDD için yalnızca uygulama ve üçüncü taraf bağımlılıklarının dağıtın. .NET Core uygulamanızı hedef sistemde mevcut .NET Core sürümünü kullanır bu yana dağıtmanız gerekmez. .NET Core hedefleyen .NET Core ve ASP.NET Core uygulamaları için varsayılan dağıtım modeli budur.

### <a name="why-create-a-framework-dependent-deployment"></a>Framework bağımlı dağıtım neden oluşturulsun mu?

Bir FDD dağıtma, çok sayıda avantaj vardır:

- .NET Core uygulamanızı önceden çalışır hedef işletim sistemlerini tanımlamak zorunda değilsiniz. .NET Core yürütülebilir dosyaları ve kitaplıkları işletim sisteminden bağımsız olarak için ortak bir PE dosyası biçimini kullandığından, .NET Core uygulamanızı alttaki işletim sisteminden bağımsız olarak çalıştırabilirsiniz. PE dosyası biçimi hakkında daha fazla bilgi için bkz. [.NET bütünleştirilmiş kodu dosya biçimi](../../standard/assembly-format.md).

- Dağıtım paketinin boyutu küçüktür. Yalnızca uygulamanız ve onun bağımlılıklarını, .NET Core kendisini dağıtırsınız.

- Birden fazla uygulama konak sistemlerinde iki disk alanı ve bellek kullanımını azaltır aynı .NET Core yüklemesini kullanın.

Bazı dezavantajları vardır:

- Yalnızca .NET Core, hedef sürümünü veya sonraki bir sürümü zaten konak sisteminde yüklü değilse, uygulamayı çalıştırabilirsiniz.

- .NET Core çalışma zamanı ve kitaplıklarda bilgi birikiminizi gelecek sürümleri olmadan değiştirmek mümkündür. Nadiren de olsa Bu, uygulamanın davranış şekli değişebilir.

## <a name="self-contained-deployments-scd"></a>Bağımsız dağıtımlar (SCD)

Kendi içinde bir dağıtım için uygulamanızı ve tüm gerekli üçüncü taraf bağımlılıkları sürümü, uygulama oluşturmak için kullanılan bir .NET Core ile birlikte dağıtın. Bir SCD oluşturma içermez [yerel .NET Core bağımlılıklarını](https://github.com/dotnet/core/blob/master/Documentation/prereqs.md) çeşitli platformlarda, bu nedenle bu uygulama çalışmadan önce mevcut olmalıdır. Çalışma zamanında sürüm bağlama hakkında daha fazla bilgi için makaleye bakın [sürüm bağlama .NET core'da](../versions/selection.md).

NET Core 2.1 SDK (sürüm 2.1.300) ile başlayarak, .NET Core destekler *düzeltme eki sürümü ileri sarma*. .NET Core araçları kendi içinde bir dağıtım oluşturduğunuzda, otomatik olarak en son hizmet verilen çalışma zamanı .NET Core sürümünün içerir. Bu uygulama hedeflerinizi. (En son hizmet verilen çalışma zamanı için güvenlik yamaları ve diğer hata düzeltmeleri içerir.) Hizmet verilen çalışma zamanı yapı sisteminizde mevcut olması gerekmez; NuGet.org adresinden otomatik olarak yüklenir. İletme, düzeltme eki sürümü piyasaya çıkışını geri çevirmek yönergeler de dahil olmak üzere daha fazla bilgi için bkz. [müstakil dağıtım çalışma zamanı, ileri sarma](runtime-patch-selection.md).

FDD ve SCD dağıtımları ayrı konak yürütülebilir dosyaları, kullandığından, yürütülebilir bir konak için bir SCD yayımcı imza ile oturum açabilirsiniz.

### <a name="why-deploy-a-self-contained-deployment"></a>Neden kendi içinde bir dağıtım dağıtılsın mı?

Müstakil dağıtımının sağladığı iki önemli avantaj vardır:

- Uygulamanızla birlikte dağıtılan bir .NET Core sürümünün tek denetim var. .NET core yalnızca sizin tarafınızdan hizmet verebilir.

- Hedef sistem üzerinde çalışacağı bir .NET Core sürümünü sunuyorsunuz bu yana .NET Core uygulamanızı çalıştırabilirsiniz olabilirsiniz.

Ayrıca, bir dizi dezavantajları vardır:

- .NET Core, dağıtım paketinde bulunduğundan, dağıtım paketleri önceden oluşturduğunuz hedef platformlar seçmeniz gerekir.

- .NET Core yanı sıra, uygulamanızı ve üçüncü taraf bağımlılıkları içerecek şekilde sahip olduğundan, dağıtım paketi görece büyük boyutudur.

  .NET Core 2.0 ile başlayarak, yaklaşık 28 MB Linux sistemlerinde dağıtımınızın boyutunu .NET Core kullanarak azaltabilir [ *Genelleştirme sabit modu*](https://github.com/dotnet/corefx/blob/master/Documentation/architecture/globalization-invariant-mode.md). Linux üzerinde .NET Core dayanan normalde, [ICU kitaplıkları](https://github.com/dotnet/docs/issues/http%22//icu-project.org) Genelleştirme desteği. Sabit modunda kitaplıkları dağıtımınıza dahil edilmez ve tüm kültürler gibi davranırlar [sabit kültür](xref:System.Globalization.CultureInfo.InvariantCulture?displayProperty=nameWithType).

- Bir sistem için çok sayıda bağımsız bir .NET Core uygulamaları dağıtma, önemli miktarda disk alanı, her uygulama çoğaltmaları bu yana .NET Core dosyaları kullanabilir.

## <a name="step-by-step-examples"></a>Adım adım örnek

CLI araçları ile .NET Core uygulamaları dağıtma hakkında adım adım örnekler için bkz [CLI araçları ile .NET Core uygulamaları dağıtma](deploy-with-cli.md). Visual Studio ile .NET Core uygulamaları dağıtma hakkında adım adım örnekler için bkz [Visual Studio ile .NET Core uygulamaları dağıtma](deploy-with-vs.md). Her konu, aşağıdaki dağıtımlar örnekleri içerir:

- Framework bağımlı dağıtım
- Framework bağımlı dağıtım üçüncü taraf bağımlılıkları
- Kendi içinde dağıtım
- Üçüncü taraf bağımlılıkları kendi içinde dağıtım

## <a name="see-also"></a>Ayrıca bkz.

* [CLI araçları ile .NET Core uygulamaları dağıtma](deploy-with-cli.md)
* [Visual Studio ile .NET Core uygulamaları dağıtma](deploy-with-vs.md)
* [Paketler, Meta Paketler ve Çerçeveler](../packages.md)
* [.NET core çalışma zamanı tanımlayıcı (RID) Kataloğu](../rid-catalog.md)
