---
title: System.ServiceModel.MessageProcessingPaused
ms.date: 03/30/2017
ms.assetid: 36b5302a-93cc-478a-9bb2-8a1601fba1df
ms.openlocfilehash: 6fb1463b811d985f54b9a99e59d1280eaa040256
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33482820"
---
# <a name="systemservicemodelmessageprocessingpaused"></a><span data-ttu-id="c69ed-102">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="c69ed-102">System.ServiceModel.MessageProcessingPaused</span></span>
<span data-ttu-id="c69ed-103">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="c69ed-103">System.ServiceModel.MessageProcessingPaused</span></span>  
  
## <a name="description"></a><span data-ttu-id="c69ed-104">Açıklama</span><span class="sxs-lookup"><span data-stu-id="c69ed-104">Description</span></span>  
 <span data-ttu-id="c69ed-105">İş parçacığı bir ileti işlenirken anahtarlı.</span><span class="sxs-lookup"><span data-stu-id="c69ed-105">The threads were switched while processing a message.</span></span>  
  
 <span data-ttu-id="c69ed-106">İleti işleme tarafından aşağıdaki nedenlerden duraklatılabilir:</span><span class="sxs-lookup"><span data-stu-id="c69ed-106">Message processing can be paused by the following reasons:</span></span>  
  
-   <span data-ttu-id="c69ed-107">ConcurrencyMode tek ya da desteklemeyeceğini ve başka bir ileti işleme hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="c69ed-107">ConcurrencyMode is single or reentrant, and the service is processing another message.</span></span>  
  
-   <span data-ttu-id="c69ed-108">İşlem etkindir ve başka bir işlem işleme hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="c69ed-108">Transaction is enabled and the service is processing another transaction.</span></span>  
  
-   <span data-ttu-id="c69ed-109">Eşitleme bağlamı geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="c69ed-109">Synchronization context is not current.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c69ed-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c69ed-110">See Also</span></span>  
 [<span data-ttu-id="c69ed-111">İzleme</span><span class="sxs-lookup"><span data-stu-id="c69ed-111">Tracing</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [<span data-ttu-id="c69ed-112">Uygulamanızda Sorun Giderme için İzleme Kullanma</span><span class="sxs-lookup"><span data-stu-id="c69ed-112">Using Tracing to Troubleshoot Your Application</span></span>](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [<span data-ttu-id="c69ed-113">Yönetim ve Tanılama</span><span class="sxs-lookup"><span data-stu-id="c69ed-113">Administration and Diagnostics</span></span>](../../../../../docs/framework/wcf/diagnostics/index.md)
