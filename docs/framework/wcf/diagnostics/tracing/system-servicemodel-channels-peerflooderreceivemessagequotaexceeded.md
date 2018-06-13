---
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: 5c1e6c51ffd5aeafe65a67c8989f554ebf0824d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33478923"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a><span data-ttu-id="5b720-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span><span class="sxs-lookup"><span data-stu-id="5b720-102">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span></span>
<span data-ttu-id="5b720-103">İletilerin gelen alma hızı çok yüksektir.</span><span class="sxs-lookup"><span data-stu-id="5b720-103">The inbound receive rate of messages is too high.</span></span>  
  
## <a name="description"></a><span data-ttu-id="5b720-104">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5b720-104">Description</span></span>  
 <span data-ttu-id="5b720-105">Bu izleme, gelen iletileri işlemek çalışılırken zaman oluşur.</span><span class="sxs-lookup"><span data-stu-id="5b720-105">This trace occurs when attempting to process inbound messages.</span></span> <span data-ttu-id="5b720-106">Bu komşusu için belirlediğiniz kotayı aştığı için bir ileti için belirli bir komşu iletilemedi.</span><span class="sxs-lookup"><span data-stu-id="5b720-106">A message could not be forwarded to a specific neighbor because the quota set for that neighbor has been exceeded.</span></span> <span data-ttu-id="5b720-107">Bu durum, bu komşusu için biriktirme listesi iletileri temizlemek bir yanıt vermeyen komşu başarısız oluşur.</span><span class="sxs-lookup"><span data-stu-id="5b720-107">This occurs when an unresponsive neighbor fails to clear a backlog of messages pending for that neighbor.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="5b720-108">Sorun giderme</span><span class="sxs-lookup"><span data-stu-id="5b720-108">Troubleshooting</span></span>  
 <span data-ttu-id="5b720-109">Mesh içinde gönderilen iletileri hızını azaltın.</span><span class="sxs-lookup"><span data-stu-id="5b720-109">Reduce the rate at which messages are sent within the mesh.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b720-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5b720-110">See Also</span></span>  
 [<span data-ttu-id="5b720-111">İzleme</span><span class="sxs-lookup"><span data-stu-id="5b720-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="5b720-112">Uygulamanızda Sorun Giderme için İzleme Kullanma</span><span class="sxs-lookup"><span data-stu-id="5b720-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="5b720-113">Yönetim ve Tanılama</span><span class="sxs-lookup"><span data-stu-id="5b720-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
