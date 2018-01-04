---
title: "Ağ izleme yorumlama"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- TraceMode attribute
- hexidecimal data, network tracing output
- network tracing, analyzing
- protocolonly
- text, network tracing output
- includehex
ms.assetid: ad22b4b8-00af-4778-9cca-cb609ce1f8ff
caps.latest.revision: "9"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: 91357d3400cccc6c61fa25bc72d7e8e6c5027811
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="interpreting-network-tracing"></a>Ağ izleme yorumlama
Ağ izleme etkinleştirildiğinde izleme uygulamanızı yapar çeşitli çağrıları yakalamak için kullanabileceğiniz <xref:System.Net> sınıfı üyeleri. Bu çağrılar çıkışı aşağıdaki örneklere benzer olabilir.  
  
```  
[588]   (4357)   Entering Socket#33574638::Send()  
[588]   (4387)   Exiting Socket#33574638::Send()-> 61#61  
```  
  
 [588] önceki örnekte geçerli iş parçacığının benzersiz tanımlayıcısıdır. (4357) ve (4387) olan zaman damgaları belirten uygulama başlatıldığından bu yana geçen milisaniye sayısı. Zaman damgası aşağıdaki veri girme ve yönteminden çıkılıyor uygulama gösterir **Socket.Send**. Nesne yürütme **Gönder** yöntemi kendi benzersiz tanımlayıcı olarak 33574638 sahiptir. Yöntemi çıkış izleme dönüş değeri (önceki örnekte 61) içerir.  
  
 Ağ izlerini gönderilen veya uygulama düzeyi protokolleri Köprü Metni Aktarım Protokolü (HTTP) gibi kullanarak, uygulama tarafından alınan ağ trafiği yakalayabilirsiniz. Bu veriler metin olarak yakalanabilir ve isteğe bağlı olarak, onaltılık veri. Onaltılık veri, belirttiğiniz zaman kullanılabilir **includehex** değeri olarak **İzlemeModu** özniteliği. (Bu öznitelik hakkında ayrıntılı bilgi için bkz: [nasıl yapılır: yapılandırma ağ izleme](../../../docs/framework/network-programming/how-to-configure-network-tracing.md).) Aşağıdaki örnek izleme kullanılarak oluşturulan **includehex**.  
  
 `[1692]   (1142)   00000000 : 47 45 54 20 2F 77 70 61-64 2E 64 61 74 20 48 54 : GET /wpad.dat HT`  
  
 `[1692]   (1142)   00000010 : 54 50 2F 31 2E 31 0D 0A-48 6F 73 74 3A 20 69 74 : TP/1.1..Host: it`  
  
 `[1692]   (1142)   00000020 : 67 70 72 6F 78 79 0D 0A-43 6F 6E 6E 65 63 74 69 : gproxy..Connecti`  
  
 `[1692]   (1142)   00000030 : 6F 6E 3A 20 43 6C 6F 73-65 0D 0A 0D 0A     : on: Close....`  
  
 Onaltılık verileri atlamak için belirtmeniz **protocolonly** değeri olarak **İzlemeModu** özniteliği. İzleme aşağıdaki örnekte, **protocolonly** belirtilir.  
  
 `[2444]   (594)   Data from ConnectStream#33574638::WriteHeaders<<GET /wpad.dat HTTP/1.1`  
  
 `Host: itgproxy`  
  
 `Connection: Close`  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Ağ İzlemeyi Etkinleştirme](../../../docs/framework/network-programming/enabling-network-tracing.md)  
 [Nasıl yapılır: Ağ İzlemeyi Yapılandırma](../../../docs/framework/network-programming/how-to-configure-network-tracing.md)  
 [.NET Framework'te Ağ İzleme](../../../docs/framework/network-programming/network-tracing.md)
