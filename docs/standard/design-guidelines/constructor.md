---
title: Oluşturucu tasarımı
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- member design guidelines, constructors
- constructors, design guidelines
- instance constructors
- type constructors
- virtual members
- constructors, types
- default constructors
- static constructors
ms.assetid: b4496afe-5fa7-4bb0-85ca-70b0ef21e6fc
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6ad920c8028b102a13fdfe928d21768538e25b0f
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44180455"
---
# <a name="constructor-design"></a>Oluşturucu tasarımı
Oluşturucular iki tür vardır: oluşturucular ve örnek oluşturucuları yazın.  
  
 Türü oluşturucuları, statik ve türü kullanılmadan önce CLR tarafından çalıştırılır. Örnek oluşturucuları, bir türün bir örneği oluşturulduğunda çalıştırın.  
  
 Herhangi bir parametre türü oluşturucuları alamıyor. Örnek oluşturucuları olabilir. Herhangi bir parametre yakalayana örnek oluşturucuları genellikle varsayılan oluşturucu çağrılır.  
  
 Oluşturucular, bir türün örneğini oluşturmak için en iyi yoludur. Çoğu geliştirici, arayın ve bunlar örnekleri (örneğin, Fabrika yöntemleri) oluşturmanın farklı yolları düşünmeden önce bir oluşturucu kullanmayı deneyin.  
  
 **✓ CONSIDER** sağlayan basit, ideal olarak varsayılan, Oluşturucular.  
  
 Basit bir oluşturucu çok küçük bir dizi parametre vardır ve tüm parametreleri ilkel veya sabit listeleri. Basit tür oluşturucular framework'ün kullanılabilirlik artırın.  
  
 **✓ CONSIDER** statik Üreteç yöntemi yerine bir oluşturucu istenen işlemin semantiği doğrudan yapımı yeni bir örneğini eşleşmiyorsa ya da Oluşturucusu tasarım yönergeleri izleyerek doğal olmayan hissi kullanarak.  
  
 **✓ DO** ana özelliklerini ayarlamak için kısayol olarak Oluşturucusu parametrelerini kullanın.  
  
 Semantik fark olmalıdır bazı özellik kümeleri tarafından izlenen boş oluşturucu ve birden çok bağımsız değişkenlerle bir kurucu kullanarak.  
  
 **✓ DO** Oluşturucu parametreleri yalnızca özelliğini ayarlamak için kullanılan Oluşturucu parametreleri ve bir özellik için aynı adı kullanın.  
  
 Bu tür parametreleri ve özellikleri arasındaki tek fark büyük/küçük harfleri.  
  
 **✓ DO** Oluşturucusu en az iş.  
  
 Oluşturucuları, oluşturucu parametresi kadar iş yakalama dışında yapmanız gerekir. Başka bir işlem maliyetini gerekli kadar Gecikmeli.  
  
 **✓ DO** uygunsa örnek Oluşturucular, özel durumlar oluşturma.  
  
 **✓ DO** böyle bir oluşturucu gerekliyse, sınıflar, bir ortak varsayılan oluşturucu açıkça bildirin.  
  
 Türe göre açıkça tüm oluşturucular bildirmeyin, birçok dili (C# gibi) genel bir varsayılan oluşturucu otomatik olarak ekler. (Soyut sınıflar korumalı Oluşturucu Al)  
  
 Parametreli bir kurucu ekleme, derleyici varsayılan oluşturucuyu eklemesini önler. Bu genellikle yanlışlıkla bozucu değişiklikleri neden olur.  
  
 **X AVOID** açıkça varsayılan oluşturucular üzerinde yapıları tanımlama.  
  
 Varsayılan Oluşturucu tanımlanmamışsa, dizideki her yuva çalıştırılacak sahip olmadığından bu dizi oluşturma daha hızlı sağlar. C# ' de dahil olmak üzere birçok derleyiciler yapılar, bu nedenle parametresiz oluşturucular izin verme unutmayın.  
  
 **X AVOID** kurucusu içinde bir nesne üzerinde sanal üyeler çağırma.  
  
 En çok türetilen türü oluşturucusuna tamamen henüz çalıştırılmadı bile sanal bir üye çağırmak çağrılacak, en çok türetilen geçersiz kılma neden olur.  
  
### <a name="type-constructor-guidelines"></a>Tür oluşturucu yönergeleri  
 **✓ DO** statik oluşturucular özel yap.  
  
 Bir sınıf oluşturucu olarak da adlandırılan bir statik Oluşturucu, bir tür başlatmak için kullanılır. CLR türünün ilk örneği oluşturulduğunda veya herhangi bir statik üyeye türdeki adlı önce statik oluşturucuyu çağırır. Kullanıcının statik Oluşturucu ne zaman çağrıldığını üzerinde denetimi yoktur. Statik oluşturucu özel değilse, CLR dışındaki kod tarafından çağrılabilir. Oluşturucu içinde gerçekleştirilen işlemlere bağlı olarak bu, beklenmeyen davranışlara neden olabilir. C# derleyicisi statik oluşturucular özel olmasını zorlar.  
  
 **X DO NOT** statik oluşturucular özel durumlar oluşturma.  
  
 Bir tür oluşturucusunda bir özel durum, geçerli uygulama etki alanında türü kullanılamaz.  
  
 **✓ CONSIDER** çalışma zamanı açıkça tanımlanmış bir statik oluşturucusu yok türleri performansını optimize etmek mümkün olduğundan statik oluşturucular açıkça kullanmak yerine statik alanları satır içi başlatılıyor.  
  
 *Kısımları © 2005, 2009 Microsoft Corporation. Tüm hakları saklıdır.*  
  
 *İzni Pearson eğitim, Inc. tarafından yeniden yazdırılmaları [çerçeve tasarım yönergeleri: kuralları, deyimlerini ve yeniden kullanılabilir .NET kitaplıkları, sürüm 2 için desenler](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina ve Brad Abrams, 22 Eki 2008 tarafından yayımlanan Microsoft Windows geliştirme serisi bir parçası olarak Addison Wesley Professional.*  
  
## <a name="see-also"></a>Ayrıca bkz.

- [Üye Tasarımı Yönergeleri](../../../docs/standard/design-guidelines/member.md)  
- [Çerçeve Tasarım Yönergeleri](../../../docs/standard/design-guidelines/index.md)
