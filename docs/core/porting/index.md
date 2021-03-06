---
title: .NET Core ile .NET Framework'ten taşıma
description: Taşıma işlemlerini anlamanıza ve .NET Core için bir .NET Framework projesi taşırken faydalı bulabileceğiniz araçları keşfedin.
author: cartermp
ms.author: mairaw
ms.date: 10/23/2018
ms.openlocfilehash: 0c0ec3d8ab09e34e8dae24623903ca571f2cca6c
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50192778"
---
# <a name="porting-to-net-core-from-net-framework"></a>.NET Core ile .NET Framework'ten taşıma

.NET Framework üzerinde çalışan kod kendinizi, kodunuzu .NET Core üzerinde çalışan ilginizi çekebilir.  Bu makalede, taşıma işlemine genel bakış ve bir listesi için .NET Core taşırken faydalı bulabileceğiniz anlatılmaktadır.

## <a name="overview-of-the-porting-process"></a>Taşıma işlemine genel bakış

Taşıma için önerilen işlemi aşağıdaki adımları dizisini izler.  İşlemin bu parçaların her biri daha ayrıntılı olarak daha fazla makale bölümünde değinilmiştir.

1. Tanımlamak ve üçüncü taraf bağımlılıklarınızı hesap.

   Bu, üçüncü taraf bağımlılıkları olan, bağımlı nasıl anlama içerecektir bunları sağlanmıyorsa de .NET Core ve adımlar üzerinde çalıştırmak için uygulayabileceğiniz nasıl.
   
2. .NET Framework'ün en son sürümünü hedefleyecek şekilde bağlantı noktası istediğiniz tüm projeleri yeniden hedefle

   Bu, belirli bir API'yi burada .NET Core desteği durumlarda .NET Framework özel hedefler için API alternatifler kullanabilirsiniz sağlar.
   
3. Kullanım [.NET Portability Analyzer](../../standard/analyzers/portability-analyzer.md) bütünleştirilmiş kodlarınızı analiz edin ve kendi sonuçlarına göre bağlantı noktası için bir plan geliştirin.

   API taşınabilirlik Çözümleyicisi aracını derlenmiş bütünleştirilmiş kodlarınızı analiz edin ve üst düzey taşınabilirlik Özet gösteren bir rapor ve .NET Core üzerinde kullanılamayan, kullanmakta olduğunuz her API bir dökümünü oluşturur.  Bu raporu analizini yanı sıra kullanabilirsiniz, nasıl, kodunuzu üzerinden bağlantı noktası bir plan geliştirmek için kod tabanı.
   
4. Testleri kod bağlantı noktası.

   .NET Core'a taşıma temelinizde böyle büyük bir değişiklik olduğundan, yüksek oranda üzerinden kod bağlantı noktası olarak testleri çalıştırabilmeniz için unity'nin testlerinizi almak için önerilir.  .NET Core, bugün MSTest, xUnit ve Nunit'i destekler.
   
6. Taşıma için planınızı yürütün!

## <a name="tools-to-help"></a>Yardımcı olacak araçlar

Yararlı bulabilirsiniz araçları kısa bir listesi aşağıda verilmiştir:

* NuGet - [Nuget istemci](https://dist.nuget.org/index.html) veya [NuGet paket Gezgini](https://github.com/NuGetPackageExplorer/NuGetPackageExplorer), Microsoft'un .NET uygulamaları için Paket Yöneticisi.
* API Portability Analyzer - [komut satırı aracını](https://github.com/Microsoft/dotnet-apiport/releases) veya [Visual Studio Uzantısı](https://visualstudiogallery.msdn.microsoft.com/1177943e-cfb7-4822-a8a6-e56c7905292b), nasıl taşınabilir kod arasında .NET Framework ve .NET Core ile olan bir rapor oluşturabilen bir araç zinciri bir derleme tarafından bütünleştirilmiş kod çözümleme sorunları.  Bkz: [işlemi yardımcı olacak araçlar](https://github.com/Microsoft/dotnet-apiport/blob/master/docs/HowTo/) daha fazla bilgi için.
* Ters paket arama - A [yararlı web hizmeti](https://packagesearch.azurewebsites.net) türü için arama yapın ve bu türü içeren paketleri olanak tanır.

## <a name="next-steps"></a>Sonraki adımlar

[Üçüncü taraf bağımlılıklarını çözümleme.](third-party-deps.md)
   
