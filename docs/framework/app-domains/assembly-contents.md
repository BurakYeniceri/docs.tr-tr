---
title: Derleme İçerikleri
ms.date: 03/30/2017
helpviewer_keywords:
- assemblies [.NET Framework], multifile
- assemblies [.NET Framework], single-file
- single-file assemblies
- multifile assemblies
ms.assetid: 28116714-da77-45f7-826d-fa035d121948
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1aed7e1e9e85f746c4b55b10c59dd82e85565b00
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194845"
---
# <a name="assembly-contents"></a>Derleme İçerikleri
Genel olarak, statik bir derleme dört öğeden oluşabilir:  
  
-   [Derleme bildirimi](../../../docs/framework/app-domains/assembly-manifest.md), derleme meta verileri içerir.  
  
-   Tür metaverileri.  
  
-   Türleri uygulayan Microsoft ara dili (MSIL) kodu.  
  
-   Bir kaynak kümesi.  
  
 Yalnızca derleme bildirimi gereklidir, ancak derlemeye herhangi bir anlamlı işlevsellik sağlamak için türler veya kaynaklar gereklidir.  
  
 Bu öğeleri bir derleme içinde gruplandırmanın çeşitli yolları vardır. Tüm öğeleri, aşağıda gösterildiği şekilde tek bir fiziksel dosya halinde gruplandırabilirsiniz.  
  
 ![MyAssembly.dll](../../../docs/framework/app-domains/media/assemblyover1.gif "assemblyover1")  
Tek dosyalı derleme  
  
 Alternatif olarak, bir derlemenin öğeleri birkaç dosya içinde bulunabilir. Bu dosyalar derlenmiş kod modülleri (.netmodule), kaynaklar (örneğin .bmp veya .jpg dosyaları) veya uygulama tarafından gereken diğer dosyalar olabilir. Farklı dillerde yazılan modülleri birleştirmek ve az kullanılan türleri yalnızca gerektiğinde indirilen bir modülün içine yerleştirerek bir uygulamanın indirilmesini optimize etmek istediğinizde bir çoklu dosya derlemesi oluşturun.  
  
 Aşağıdaki görselde, kuramsal bir uygulamanın geliştiricisi bazı işlevsellik kodlarını farklı modüllere ayırmayı ve büyük bir kaynak dosyasını (bu durumda bir .bmp görüntüsü) orijinal dosyasında tutmayı seçmiştir. .NET Framework, yalnızca kendine atıfta bulunulduğunda bir dosya indirdiğinden, seyrek atıfta bulunulan bir kodu uygulamadan farklı bir dosyada tutmak kod indirmeyi optimize eder.  
  
 ![MyAssembly.dll](../../../docs/framework/app-domains/media/assemblyover2.gif "assemblyover2")  
Çoklu dosya derlemesi  
  
> [!NOTE]
>  Bir çoklu dosya derlemesini oluşturan dosyalar dosya sistemi tarafından fiziksel olarak bağlı değildir. Bunun yerine, derleme bildirimi aracılığıyla bağlanırlar ve ortak dil çalışma zamanı, bunları birer birim olarak yönetir.  
  
 Bu görselde, üç dosya da MyAssembly.dll içindeki derleme bildiriminde açıklandığı şekilde bir derlemede bulunmaktadır. Dosya sistemi açısından üç ayrı dosyadırlar. Util.netmodule dosyası hiçbir derleme bilgisi içermediğinden, bu dosyanın bir modül olarak derlendiğini unutmayın. Derleme oluşturulduğunda derleme bildirimi MyAssembly.dll içine eklenerek Util.netmodule ve Graphic.bmp ile olan ilişkisini belirtir.  
  
 Kaynak kodunuzu tasarlarken, uygulamanızın işlevselliğini bir veya daha fazla dosyaya nasıl ayıracağınız hakkında açık kararlar verirsiniz. .NET Framework kodu tasarlarken, işlevselliği bir veya daha fazla derlemeye nasıl ayıracağınız hakkında da benzer kararlar verirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
- [Ortak Dil Çalışma Zamanı Modülündeki Bütünleştirilmiş Kodlar](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)  
- [Bütünleştirilmiş Kod Bildirimi](../../../docs/framework/app-domains/assembly-manifest.md)  
- [Bütünleştirilmiş Kod Güvenliği Konuları](../../../docs/framework/app-domains/assembly-security-considerations.md)
