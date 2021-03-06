---
title: Veri isteme
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sending data
- WebRequest class, sending and receiving data
- requesting data from Internet, about requesting data
- WebClient class, sending and receiving data
- network, requesting data
- receiving data
- sending data, about sending data
- response to Internet request, about responding to Internet requests
- data requests
- receiving data, about receiving data
- Internet, requesting data
ms.assetid: df6f1e1d-6f2a-45dd-8141-4a85c3dafe1d
ms.openlocfilehash: 026912a2dc8a09fb52e0427fc7bf2dbb1d55413a
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50182820"
---
# <a name="requesting-data"></a>Veri isteme
Günümüzün Internet dağıtılmış işletim ortamında çalışan uygulamalar geliştirme, her türden kaynaklardan veri almak için verimli, kullanımı kolay bir yöntem gerektirir. Takılabilir protokoller birden çok Internet protokollerinden veri almak için tek bir arabirim kullanan uygulamalar geliştirmenize olanak tanır.  
  
## <a name="uploading-and-downloading-data-from-an-internet-server"></a>Karşıya yükleme ve bir Internet sunucusundan veri indirme  
 Basit isteği ve yanıt işlemleri <xref:System.Net.WebClient> sınıf verileri karşıya yükleme veya bir Internet sunucusundan verileri indirmek için kolay bir yöntem sağlar. **WebClient** dosyaları karşıya yükleme ve indirme, gönderme ve alma akışları ve bir veri arabelleği sunucuya göndermek ve bir yanıt almak için yöntemler sağlar. **WebClient** kullanan <xref:System.Net.WebRequest> ve <xref:System.Net.WebResponse> sınıfları, takılabilir Protokolü herhangi kayıtlı Internet kaynağına gerçek bağlantı olmak için kullanılabilir.  
  
 Daha karmaşık işlem istek verileri kullanarak sunuculardan yapmanız istemci uygulamaları **WebRequest** sınıfı ve alt öğeleri. **WebRequest** sunucuya bağlanırken, isteği gönderme ve yanıt alma ayrıntıları. **WebRequest** özellikleri ve takılabilir protokoller kullanan tüm uygulamalar için kullanılabilen yöntemleri kümesini tanımlayan bir soyut sınıftır. Alt öğeleri **WebRequest**, gibi <xref:System.Net.HttpWebRequest>, özellikleri ve yöntemleri tarafından tanımlanan uygulamak **WebRequest** temel alınan protokolü ile tutarlı bir şekilde.  
  
 **WebRequest** sınıfı protokole özgü örneklerini oluşturur **WebRequest** URI değerini kullanarak alt öğeleri, geçirilen kendi <xref:System.Net.WebRequest.Create%2A> belirli türetilmiş sınıf belirlemek için yöntemi oluşturmak için örneği. Uygulamaları belirtin, **WebRequest** alt öğesi alt öğesi'nın oluşturucuyla kaydederek bir isteği işlemek için kullanılması gerekir <xref:System.Net.WebRequest.RegisterPrefix%2A?displayProperty=nameWithType> yöntemi.  
  
 İstek çağırarak Internet kaynağına yapılan <xref:System.Net.WebRequest.GetResponse%2A> metodunda **WebRequest**. **GetResponse yanıtına** yöntemi oluşturur özelliklerini protokole özgü istekten **WebRequest**sunucusuna TCP veya UDP Yuva bağlantısı kurar ve isteği gönderir. HTTP gibi sunucusuna veri gönderme istekleri **Post** veya FTP **Put** istekleri <xref:System.Net.WebRequest.GetRequestStream%2A?displayProperty=nameWithType> yöntemi, veri göndermek bir ağ akışı sağlar.  
  
 **GetResponse yanıtına** yöntemi döndürür protokole özgü **WebResponse** eşleşen **WebRequest.**  
  
 **WebResponse** sınıfı, ayrıca bir soyut sınıf özellikleri ve takılabilir protokoller kullanan tüm uygulamalar için kullanılabilen yöntemleri tanımlar. **Webresponse'tan** alt öğeleri, bu özellikleri ve yöntemleri için temel alınan protokoldeki uygulayın. <xref:System.Net.HttpWebResponse> Gibi uygulayan sınıf **WebResponse** HTTP için sınıf.  
  
 Sunucu tarafından döndürülen verilerin uygulama tarafından döndürülen akış içinde sunulan <xref:System.Net.WebResponse.GetResponseStream%2A?displayProperty=nameWithType> yöntemi. Aşağıdaki örnekte gösterildiği gibi diğer, bu akış kullanabilirsiniz.  
  
```csharp  
StreamReader sr =  
   new StreamReader(resp.GetResponseStream(), Encoding.ASCII);  
```  
  
```vb  
Dim sr As StreamReader  
sr = New StreamReader(resp.GetResponseStream(), Encoding.ASCII)  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [.NET Framework'te Ağ Programlaması](../../../docs/framework/network-programming/index.md)  
 [Nasıl yapılır: Web Sayfası İsteme ve Sonuçları Akış Olarak Alma](../../../docs/framework/network-programming/how-to-request-a-web-page-and-retrieve-the-results-as-a-stream.md)  
 [Nasıl yapılır: WebRequest ile Eşleşen Protokole Özgü WebResponse Alma](../../../docs/framework/network-programming/how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest.md)
