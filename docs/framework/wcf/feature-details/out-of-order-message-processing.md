---
title: Düzen Dışı İleti İşleme
ms.date: 03/30/2017
ms.assetid: 33fc62a5-5d59-461c-a37a-0e1b51ac763d
ms.openlocfilehash: a7839b60dbad7919a644c196a1c63f6bc46fb5d3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33492951"
---
# <a name="out-of-order-message-processing"></a><span data-ttu-id="a293f-102">Düzen Dışı İleti İşleme</span><span class="sxs-lookup"><span data-stu-id="a293f-102">Out-of-Order Message Processing</span></span>
<span data-ttu-id="a293f-103">İş akışı hizmetleri belirli bir sırada gönderilen iletiler bağlı.</span><span class="sxs-lookup"><span data-stu-id="a293f-103">Workflow services may depend on messages being sent in a specific order.</span></span> <span data-ttu-id="a293f-104">Bir veya daha fazla iş akışı hizmeti içeren <xref:System.ServiceModel.Activities.Receive> etkinlikleri ve her <xref:System.ServiceModel.Activities.Receive> etkinlik belirli bir ileti bekleniyor.</span><span class="sxs-lookup"><span data-stu-id="a293f-104">A workflow service contains one or more <xref:System.ServiceModel.Activities.Receive> activities and each <xref:System.ServiceModel.Activities.Receive> activity is expecting a specific message.</span></span> <span data-ttu-id="a293f-105">Belirli aktarım teslim, istemciler tarafından gönderilen iletileri Gecikmeli ve bu nedenle iş akışı hizmeti beklenmedik bir sırayla teslim.</span><span class="sxs-lookup"><span data-stu-id="a293f-105">Without particular transport delivery guarantees, messages sent by clients may be delayed and therefore delivered in an order the workflow service may not expect.</span></span> <span data-ttu-id="a293f-106">İletileri gerektirmeyen bir iş akışı hizmeti uygulama özel gönderilmesini sipariş normal olarak yapılan bir paralel etkinlik kullanarak.</span><span class="sxs-lookup"><span data-stu-id="a293f-106">Implementing a workflow service that does not require messages be sent in a specific order is normally done using a Parallel activity.</span></span> <span data-ttu-id="a293f-107">Daha karmaşık bir uygulama protokolü için iş akışı çok hızlı bir şekilde çok karmaşık hale.</span><span class="sxs-lookup"><span data-stu-id="a293f-107">For a more complicated application protocol, the workflow would become very complex very quickly.</span></span>  <span data-ttu-id="a293f-108">Düzen dışı ileti işleme özelliği Windows Communication Foundation (WCF) gibi bir iş akışı tüm iç içe geçmiş paralel etkinliklerin karmaşıklık olmadan oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a293f-108">The out-of-order message processing feature in Windows Communication Foundation (WCF) allows you to create such a workflow without all of the complexity of nested Parallel activities.</span></span> <span data-ttu-id="a293f-109">Düzen dışı ileti işleme destekleyen kanalları yalnızca desteklenen <xref:System.ServiceModel.Channels.ReceiveContext> WCF MSMQ bağlamaları gibi.</span><span class="sxs-lookup"><span data-stu-id="a293f-109">Out-of-order message processing is only supported on channels that support <xref:System.ServiceModel.Channels.ReceiveContext> such as the WCF MSMQ bindings.</span></span>  
  
## <a name="enabling-out-of-order-message-processing"></a><span data-ttu-id="a293f-110">Düzen dışı ileti işleme etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a293f-110">Enabling Out-Of-Order Message Processing</span></span>  
 <span data-ttu-id="a293f-111">Düzen dışı ileti işleme ayarlayarak etkin <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> özelliğine `true` WorkflowService üzerinde.</span><span class="sxs-lookup"><span data-stu-id="a293f-111">Out-of-order message processing is enabled by setting the <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> property to `true` on the WorkflowService.</span></span> <span data-ttu-id="a293f-112">Aşağıdaki örnekte nasıl ayarlanacağını gösterir <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> kodda özelliği.</span><span class="sxs-lookup"><span data-stu-id="a293f-112">The following example shows how to set the <xref:System.ServiceModel.Activities.WorkflowService.AllowBufferedReceive%2A> property in code.</span></span>  
  
```csharp  
// Code: Opt-in to Buffered Receive processing...  
WorkflowService service = new WorkflowService  
{  
    Name="MyService",  
    Body = workflow,  
    AllowBufferedReceive = true  
};  
```  
  
 <span data-ttu-id="a293f-113">Ayrıca uygulayabilirsiniz `AllowBufferedReceive` özniteliğini XAML iş akışı hizmetinde aşağıdaki örnekte gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="a293f-113">You can also apply the `AllowBufferedReceive` attribute to a workflow service in XAML as shown in the following example.</span></span>  
  
```xaml  
// Xaml: Opt-in to Buffered Receive processing...  
<WorkflowService AllowBufferedReceive="True">  
   <!—the actual children activities -->  
</Sequence>  
```  
  
## <a name="see-also"></a><span data-ttu-id="a293f-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a293f-114">See Also</span></span>  
 <xref:System.ServiceModel.Channels.ReceiveContext>  
 [<span data-ttu-id="a293f-115">İş Akışı Hizmetleri</span><span class="sxs-lookup"><span data-stu-id="a293f-115">Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/workflow-services.md)  
 [<span data-ttu-id="a293f-116">Kuyruklar ve Güvenilir Oturumlar</span><span class="sxs-lookup"><span data-stu-id="a293f-116">Queues and Reliable Sessions</span></span>](../../../../docs/framework/wcf/feature-details/queues-and-reliable-sessions.md)
