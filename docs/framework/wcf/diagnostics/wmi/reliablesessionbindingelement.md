---
title: ReliableSessionBindingElement
ms.date: 03/30/2017
ms.assetid: effda125-b8d3-4de6-8c0e-f59f5ea8f6eb
ms.openlocfilehash: 2e2e36486c3788cd714ffd0ed545fbb14f831476
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50197047"
---
# <a name="reliablesessionbindingelement"></a>ReliableSessionBindingElement
ReliableSessionBindingElement  
  
## <a name="syntax"></a>Sözdizimi  
  
```csharp
class ReliableSessionBindingElement : BindingElement  
{  
  datetime AcknowledgementInterval;  
  boolean FlowControlEnabled;  
  datetime InactivityTimeout;  
  sint32 MaxPendingChannels;  
  sint32 MaxRetryCount;  
  sint32 MaxTransferWindowSize;  
  boolean Ordered;  
  integer ReliableMessagingVersion;  
};  
```  
  
## <a name="methods"></a>Yöntemler  
 ReliableSessionBindingElement sınıf herhangi bir yöntemi tanımlamaz.  
  
## <a name="properties"></a>Özellikler  
 ReliableSessionBindingElement sınıfı aşağıdaki özelliklere sahiptir:  
  
### <a name="acknowledgementinterval"></a>AcknowledgementInterval  
 Veri türü: tarih/saat  
  
 Erişim türü: salt okunur  
  
 Bir hedef fabrikası tarafından oluşturulan güvenilir kanalda ileti kaynağı için bir onay göndermeden önce bekleyeceği zaman aralığı.  
  
### <a name="flowcontrolenabled"></a>FlowControlEnabled  
 Veri türü: Boole  
  
 Erişim türü: salt okunur  
  
 Akış denetimi etkin olup olmadığını belirten bir Boole değeri.  
  
### <a name="inactivitytimeout"></a>InactivityTimeout  
 Veri türü: tarih/saat  
  
 Erişim türü: salt okunur  
  
 Herhangi bir ileti kanalı hatalı önce göndermemeyi diğer tarafın kanalı göndermemesini sağladığı sürenin üst sınırını belirtir.  
  
### <a name="maxpendingchannels"></a>MaxPendingChannels  
 Veri türü: SINT32  
  
 Erişim türü: salt okunur  
  
 Bekleyebilen kabul edilecek bekleyebileceği kanalları maksimum sayısı.  
  
### <a name="maxretrycount"></a>MaxRetryCount  
 Veri türü: SINT32  
  
 Erişim türü: salt okunur  
  
 En fazla kaç kez güvenilir bir kanalın çalışır değil aldığı için bir bildirim çağırarak bir ileti göndermesi `Send` , arka plandaki kanal.  
  
### <a name="maxtransferwindowsize"></a>MaxTransferWindowSize  
 Veri türü: SINT32  
  
 Erişim türü: salt okunur  
  
 Güvenilir oturum için maksimum aktarım pencere boyutu.  
  
### <a name="ordered"></a>Sıralı  
 Veri türü: Boole  
  
 Erişim türü: salt okunur  
  
 İletilerin gönderildiği sırada ulşamasını garanti edilip edilmediğini belirten bir Boole değeri.  
  
### <a name="reliablemessagingversion"></a>ReliableMessagingVersion  
 Veri türü: tamsayı  
  
 Erişim türü: salt okunur  
  
 Güvenilir bir oturumda kullanılan WS-ReliableMessaging protokol sürümünü belirten bir tamsayı.  
  
## <a name="requirements"></a>Gereksinimler  
  
|MOF|Bildirilmiş Servicemodel.mof.|  
|---------|-----------------------------------|  
|Ad Alanı|İçinde tanımlı root\ServiceModel|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.ServiceModel.Channels.ReliableSessionBindingElement>
