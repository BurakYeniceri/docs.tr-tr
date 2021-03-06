---
title: Taşınabilir Alt Küme Projesine Hizmet Başvurusu Ekle
ms.date: 03/30/2017
ms.assetid: 61ccfe0f-a34b-40ca-8f5e-725fa1b8095e
ms.openlocfilehash: efe95a326e7c13237c7d2d74888c85bf919ed287
ms.sourcegitcommit: 15d99019aea4a5c3c91ddc9ba23692284a7f61f3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49121148"
---
# <a name="add-service-reference-in-a-portable-subset-project"></a>Taşınabilir Alt Küme Projesine Hizmet Başvurusu Ekle
Taşınabilir alt küme projeleri bir tek kaynak ağacının Bakımı ve birden çok .NET uygulamalarını (masaüstünde, Silverlight, Windows Phone ve XBOX) hala desteklerken yapı sistemi .NET derleme programcılar etkinleştirin. Taşınabilir alt küme projeleri yalnızca herhangi bir .NET uygulaması üzerinde kullanılabilen bir .NET framework derlemesi olan bir .NET taşınabilir kitaplıklar başvuru.  
  
## <a name="add-service-reference-details"></a>Hizmet başvuru ayrıntıları ekleyin  
 Bir taşınabilir alt küme projesine hizmet başvurusu ekleme, aşağıdaki kısıtlamalar uygulanır:  
  
1.  İçin <xref:System.Xml.Serialization.XmlSerializer>, yalnızca sabit Kodlamalar izin verilir. SOAP Kodlamalar, içeri aktarma sırasında bir hata oluşturur.  
  
2.  Hizmetleri kullanan <xref:System.Runtime.Serialization.DataContractSerializer> senaryoları, veri sözleşme vekil yeniden kullanılan türleri yalnızca taşınabilir alt kümesinden geldiğini emin olmak için sağlanır.  
  
3.  Taşınabilir kitaplıklarda desteklenmeyen bağlamalar kullanan uç noktaları (dışındaki tüm bağlamaları <xref:System.ServiceModel.BasicHttpBinding>, <xref:System.ServiceModel.WSHttpBinding> işlem akışı, güvenilir oturumlar veya MTOM kodlama ve eşdeğer özel bağlamalar olmadan) göz ardı edilir.  
  
4.  İleti üstbilgileri içeri aktarmadan önce tüm işlemlerdeki tüm ileti açıklamalarını silinir.  
  
5.  Taşınabilir olmayan öznitelikler <xref:System.ComponentModel.DesignerCategoryAttribute>, <xref:System.SerializableAttribute>, ve <xref:System.ServiceModel.TransactionFlowAttribute> oluşturulan istemci proxy koddan kaldırıldı.  
  
6.  ProtectionLevel, Sessionmode'u, IsInitiating ve IsTerminating kaldırılma taşınabilir olmayan özellikler <xref:System.ServiceModel.ServiceContractAttribute>, <xref:System.ServiceModel.OperationContractAttribute>, ve <xref:System.ServiceModel.FaultContractAttribute>.  
  
7.  Tüm hizmet işlemlerini zaman uyumsuz işlemler istemci proxy'de'olarak oluşturulur.  
  
8.  Taşınabilir olmayan türler kullanan oluşturulan istemci oluşturucular kaldırılır.  
  
9. A <xref:System.Net.CookieContainer> örneği oluşturulan istemcide gösterilir.  
  
10. Bir yorum derlemeyi ve kod oluşturucunun sürümünü tanımlayan dosyasının en üstüne eklenir:`// This code was auto-generated by Microsoft.VisualStudio.Portable.AddServiceReference, version 1.0.0.0`  
  
11. <xref:System.Runtime.Serialization.ISerializable> Arabirimi desteklenmiyor.  
  
12. Net.Tcp ve PollingDuplex bağlamaları desteklenmez.  
  
13. <xref:System.Runtime.Serialization.DataContractSerializer> Hataları için her zaman kullanılır.  
  
14. <xref:System.ServiceModel.MessageContractAttribute.IsWrapped%2A> Taşınabilir alt küme projelerinde desteklenmez.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WCF İstemcisi Kullanarak Hizmetlere Erişme](../../../docs/framework/wcf/accessing-services-using-a-wcf-client.md)  
 [Taşınabilir Sınıf Kitaplığı](../../standard/cross-platform/cross-platform-development-with-the-portable-class-library.md)
