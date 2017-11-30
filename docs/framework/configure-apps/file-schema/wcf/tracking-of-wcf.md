---
title: WCF &lt;izleme&gt;
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 70cfaf24-a91c-4e56-ac47-d2ed87a963b3
caps.latest.revision: "3"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 7f0b3ad28c5d19ce812b714ef8e2ae92c14ab2a1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="lttrackinggt-of-wcf"></a><span data-ttu-id="0b477-102">WCF &lt;izleme&gt;</span><span class="sxs-lookup"><span data-stu-id="0b477-102">&lt;tracking&gt; of WCF</span></span>
<span data-ttu-id="0b477-103">Bir iş akışı hizmeti izleme ayarlarını tanımlamak için yapılandırma bölümünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="0b477-103">Represents a configuration section for defining tracking settings for a workflow service.</span></span>  
  
 <span data-ttu-id="0b477-104">İş akışı izleme ve yapılandırmasını daha fazla bilgi için bkz: [izleme ve izleme iş akışı](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) ve [yapılandırma izleme iş akışı için](../../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="0b477-104">For more information in workflow tracking and its configuration, see [Workflow Tracking and Tracing](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md) and [Configuring Tracking for a Workflow](../../../../../docs/framework/windows-workflow-foundation/configuring-tracking-for-a-workflow.md).</span></span>  
  
 <span data-ttu-id="0b477-105">\<system.serviceModel ></span><span class="sxs-lookup"><span data-stu-id="0b477-105">\<system.serviceModel></span></span>  
<span data-ttu-id="0b477-106">\<İzleme ></span><span class="sxs-lookup"><span data-stu-id="0b477-106">\<tracking></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0b477-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0b477-107">Syntax</span></span>  
  
```xml
   <system.serviceModel>  <tracking>       <participants>       <add name="String"            profileName="String"           type="String" />      </participants>     <trackingProfile name="String">      <workflow activityDefinitionId="String">          <activityScheduledQueries>             <activityScheduledQuery activityName="String"                 childActivityName="String"/>          </activityScheduledQueries>             <activityStateQuery activityName="String" />                <arguments>                   <argument name="String"/>                </arguments>                <states>                   <state name="String"/>                </states>                <variables>                   <variable name="String"/>                </variables>          </activityStateQueries>          <bookmarkResumptionQueries>             <bookmarkResumptionQuery name="String" />          </bookmarkResumptionQueries>          <cancelRequestQueries>             <cancelRequestQuery activityName="String"                 childActivityName="String"/>          </cancelRequestQueries>          <customTrackingQueries>             <customTrackingQuery activityName="String"                 name="String"/>          </customTrackingQueries>          <faultPropagationQueries>             <faultPropagationQuery activityName="String"                 faultHandlerActivityName="String"/>          </faultPropagationQueries>         <workflowInstanceQueries>            <workflowInstanceQuery>              <states>                 <state name="String"/>              </states>          </workflowInstanceQuery>        </workflowInstanceQueries>      </workflow>    </trackingProfile>           </profiles>  </tracking></system.serviceModel>  
```
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0b477-108">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="0b477-108">Attributes and Elements</span></span>  
 <span data-ttu-id="0b477-109">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0b477-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0b477-110">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="0b477-110">Attributes</span></span>  
 <span data-ttu-id="0b477-111">Yok.</span><span class="sxs-lookup"><span data-stu-id="0b477-111">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="0b477-112">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="0b477-112">Child Elements</span></span>  
  
|<span data-ttu-id="0b477-113">Öğe</span><span class="sxs-lookup"><span data-stu-id="0b477-113">Element</span></span>|<span data-ttu-id="0b477-114">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b477-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0b477-115">\<Katılımcıları ></span><span class="sxs-lookup"><span data-stu-id="0b477-115">\<participants></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/participants.md)|<span data-ttu-id="0b477-116">Kayıtları İzleme için abone katılımcılara tanımlama yapılandırma öğeleri koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="0b477-116">A collection of configuration elements defining participants that subscribe to tracking records.</span></span> <span data-ttu-id="0b477-117">İzleme katılımcıları izleme kayıtları yükü işlemek için mantığı içerir (örneğin, bir dosyaya yazmak tercih ettikleri).</span><span class="sxs-lookup"><span data-stu-id="0b477-117">The tracking participants contain the logic to process the payload from the tracking records (for example, they could choose to write to a file).</span></span>|  
|[<span data-ttu-id="0b477-118">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="0b477-118">\<trackingProfile></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/trackingprofile.md)|<span data-ttu-id="0b477-119">Bir iş akışı örneğinden yayılan filtre izleme kayıtları için bir izleme profili.</span><span class="sxs-lookup"><span data-stu-id="0b477-119">A tracking profile to filter tracking records emitted from a workflow instance.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0b477-120">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="0b477-120">Parent Elements</span></span>  
  
|<span data-ttu-id="0b477-121">Öğe</span><span class="sxs-lookup"><span data-stu-id="0b477-121">Element</span></span>|<span data-ttu-id="0b477-122">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0b477-122">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0b477-123">Sistem.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="0b477-123">system.ServiceModel</span></span>|<span data-ttu-id="0b477-124">Tüm iş akışı yapılandırma öğelerinin kök öğe.</span><span class="sxs-lookup"><span data-stu-id="0b477-124">The root element of all workflow configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0b477-125">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="0b477-125">Remarks</span></span>  
 <span data-ttu-id="0b477-126">İzleme, bir iş akışının yürütülmesini inceleyin olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b477-126">Tracking provides you with the ability to examine the execution of a workflow.</span></span> <span data-ttu-id="0b477-127">İş akışı izleme altyapısı, bir iş akışı yürütme sırasında anahtar olayları yansıtma kayıtları yayma Instruments.</span><span class="sxs-lookup"><span data-stu-id="0b477-127">The workflow tracking infrastructure instruments a workflow to emit records reflecting key events during the execution.</span></span> <span data-ttu-id="0b477-128">Örneğin, bir iş akışı örneği başlatıldığında veya tamamlandıktan izleme kayıtları gösterilen.</span><span class="sxs-lookup"><span data-stu-id="0b477-128">For example, when a workflow instance starts or completes tracking records are emitted.</span></span> <span data-ttu-id="0b477-129">İzleme, iş akışı değişkenleri ile ilişkili iş ilgili veriler ayrıca ayıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b477-129">Tracking can also extract business relevant data associated with the workflow variables.</span></span> <span data-ttu-id="0b477-130">Örneğin, iş akışı işleme sistemi sipariş temsil ediyorsa düzeni kimliği ile birlikte izleme kaydı ayıklanabilir.</span><span class="sxs-lookup"><span data-stu-id="0b477-130">For example, if the workflow represents an order processing system the order id can be extracted along with the tracking record.</span></span> <span data-ttu-id="0b477-131">Genel olarak, izleme WF etkinleştirme Tanılama veya İş analizi bir iş akışının yürütülmesini kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="0b477-131">In general, enabling WF tracking facilitates diagnostics or business analytics over a workflow execution.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b477-132">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="0b477-132">See Also</span></span>  
 <span data-ttu-id="0b477-133"><xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="0b477-133"><xref:System.ServiceModel.Activities.Tracking.Configuration.TrackingSection?displayProperty=nameWithType></span></span>       
 [<span data-ttu-id="0b477-134">İzleme ve izleme iş akışı</span><span class="sxs-lookup"><span data-stu-id="0b477-134">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)