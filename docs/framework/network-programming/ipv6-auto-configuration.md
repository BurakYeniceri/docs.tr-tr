---
title: IPv6 otomatik yapılandırma
ms.date: 03/30/2017
ms.assetid: 581c1d21-1013-43a3-bf3e-2d9ead62b79c
ms.openlocfilehash: 31aaebaefa0d2682ee20ae93496aff42ae1633d8
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50199142"
---
# <a name="ipv6-auto-configuration"></a>IPv6 otomatik yapılandırma
IPv6 için önemli bir hedef düğüm Tak ve Kullan desteklemektir. Diğer bir deyişle, bir IPv6 ağa bir düğüm eklenir ve herhangi bir insan müdahalesi olmadan otomatik olarak yapılandırılmış olması mümkündür.  
  
## <a name="type-of-auto-configuration"></a>Otomatik yapılandırma türü  
 IPv6 otomatik yapılandırma aşağıdaki türlerini destekler:  
  
-   **Durum bilgisi olan otomatik yapılandırma**. Bir Dinamik Ana Bilgisayar Yapılandırma Protokolü için IPv6 gerektiğinden bu tür bir yapılandırma, belirli bir düzeyde kullanıcı müdahalesi gerektirir. (DHCPv6) sunucusu yükleme ve yönetim düğümleri. DHCPv6 sunucusu için yapılandırma bilgileri sağlayan düğümlerin listesini tutar. Sunucu ne kadar her adresi kullanımda olduğu ve ne zaman, yeniden atama için kullanılabilir olduğunu bilmesi için ayrıca durum bilgisini tutar.  
  
-   **Durum bilgisiz otomatik yapılandırma**. Bu tür bir yapılandırma küçük kuruluşlar ve kişiler için uygundur. Bu durumda, her konağın, adresinden alınan yönlendirici reklam içeriğini belirler. Adresin ağ kimliği bölümünü tanımlamak için IEEE EUI-64 standart'ı kullanarak, ana bilgisayar adresi bağlantısına benzersizliğini varsaymak şüphelenilebilir.  
  
 Adres nasıl belirlendiğinden bağımsız olarak düğüm olası adresini yerel bağlantısını benzersiz olduğunu doğrulamanız gerekir. Bu, bir komşu isteği göndererek yapılır olası adresine bir ileti. Düğüm herhangi bir yanıt alırsa, adresi zaten kullanımda olduğunu ve başka bir adres belirlemeniz gerekir bilir.  
  
## <a name="ipv6-mobility"></a>IPv6 Mobility  
 Mobil cihazları çoğalan yeni gereksinimi kullanıma sundu: bir cihazın rasgele IPv6 Internet üzerindeki konumlara değiştirip hala var olan bağlantıları korumak mümkün olması gerekir. Bu işlevselliği sağlayacak şekilde, bir mobil düğüme, bu her zaman erişilebilir bir ev adresi atanır. Mobil düğüm evde olduğunda Giriş bağlantısını bağlanır ve başlangıç adresini kullanır. Mobil düğüm evde olduğunda, genellikle bir yönlendirici olan bir giriş aracı düğümleri ile kurduğu ve mobil düğüm arasında iletileri geçirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İnternet Protokolü Sürüm 6](../../../docs/framework/network-programming/internet-protocol-version-6.md)  
 [Yuvalar](../../../docs/framework/network-programming/sockets.md)
