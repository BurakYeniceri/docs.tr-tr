---
title: "&lt;davranışları&gt;"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0e5da4e6-1aa5-466c-924e-f10efee57f0b
caps.latest.revision: "13"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 2b38b27a7b196026e2ff873c7748ed46b96ba9b2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ltbehaviorsgt"></a><span data-ttu-id="c38d6-102">&lt;davranışları&gt;</span><span class="sxs-lookup"><span data-stu-id="c38d6-102">&lt;behaviors&gt;</span></span>
<span data-ttu-id="c38d6-103">Bu öğe adlı iki alt koleksiyonlar tanımlar `endpointBehaviors` ve `serviceBehaviors`.</span><span class="sxs-lookup"><span data-stu-id="c38d6-103">This element defines two child collections named `endpointBehaviors` and `serviceBehaviors`.</span></span>  <span data-ttu-id="c38d6-104">Her koleksiyon sırasıyla uç noktaları ve hizmetler tarafından tüketilen davranışı öğeleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="c38d6-104">Each collection defines behavior elements consumed by endpoints and services respectively.</span></span> <span data-ttu-id="c38d6-105">Her davranış öğesi kendi benzersiz tanımlanır `name` özniteliği.</span><span class="sxs-lookup"><span data-stu-id="c38d6-105">Each behavior element is identified by its unique `name` attribute.</span></span> <span data-ttu-id="c38d6-106">İle başlayarak [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bağlamalar ve davranışları olmayan bir adı olması için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c38d6-106">Starting with [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], bindings and behaviors are not required to have a name.</span></span> <span data-ttu-id="c38d6-107">Varsayılan yapılandırma ve adsız bağlamalar ve davranışları hakkında daha fazla bilgi için bkz: [Basitleştirilmiş yapılandırma](../../../../../docs/framework/wcf/simplified-configuration.md) ve [WCF hizmetleri için Basitleştirilmiş yapılandırma](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span><span class="sxs-lookup"><span data-stu-id="c38d6-107">For more information about default configuration and nameless bindings and behaviors, see [Simplified Configuration](../../../../../docs/framework/wcf/simplified-configuration.md) and [Simplified Configuration for WCF Services](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).</span></span>  
  
 <span data-ttu-id="c38d6-108">\<Sistem. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="c38d6-108">\<system.ServiceModel></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c38d6-109">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="c38d6-109">Syntax</span></span>  
  
```xml  
<behaviors>  
   <serviceBehaviors>  
   </serviceBehaviors>  
   <endpointBehaviors>  
   </endpointBehaviors>  
</behaviors>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="c38d6-110">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="c38d6-110">Attributes and Elements</span></span>  
 <span data-ttu-id="c38d6-111">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c38d6-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="c38d6-112">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="c38d6-112">Attributes</span></span>  
 <span data-ttu-id="c38d6-113">Yok.</span><span class="sxs-lookup"><span data-stu-id="c38d6-113">None</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="c38d6-114">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="c38d6-114">Child Elements</span></span>  
  
|<span data-ttu-id="c38d6-115">Öğe</span><span class="sxs-lookup"><span data-stu-id="c38d6-115">Element</span></span>|<span data-ttu-id="c38d6-116">Açıklama</span><span class="sxs-lookup"><span data-stu-id="c38d6-116">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c38d6-117">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="c38d6-117">\<endpointBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/endpointbehaviors.md)|<span data-ttu-id="c38d6-118">Bu yapılandırma bölümü belirli bir uç noktası için tanımlanmış tüm davranışları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c38d6-118">This configuration section represents all the behaviors defined for a specific endpoint.</span></span>|  
|[<span data-ttu-id="c38d6-119">\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="c38d6-119">\<serviceBehaviors></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicebehaviors.md)|<span data-ttu-id="c38d6-120">Bu yapılandırma bölümü için belirli bir hizmet tanımlanan tüm davranışları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c38d6-120">This configuration section represents all the behaviors defined for a specific service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="c38d6-121">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="c38d6-121">Parent Elements</span></span>  
  
|<span data-ttu-id="c38d6-122">Öğe</span><span class="sxs-lookup"><span data-stu-id="c38d6-122">Element</span></span>|<span data-ttu-id="c38d6-123">Açıklama</span><span class="sxs-lookup"><span data-stu-id="c38d6-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="c38d6-124">\<system.serviceModel ></span><span class="sxs-lookup"><span data-stu-id="c38d6-124">\<system.serviceModel></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/system-servicemodel.md)|<span data-ttu-id="c38d6-125">Tüm Windows Communication Foundation (WCF) yapılandırma öğelerinin kök öğesi.</span><span class="sxs-lookup"><span data-stu-id="c38d6-125">The root element of all Windows Communication Foundation (WCF) configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c38d6-126">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="c38d6-126">Remarks</span></span>  
 <span data-ttu-id="c38d6-127">Kullanabileceğiniz `<remove>` belirli bir davranışı Koleksiyondan kaldırılacak öğe.</span><span class="sxs-lookup"><span data-stu-id="c38d6-127">You can use the `<remove>` element to remove a particular behavior from the collection.</span></span> <span data-ttu-id="c38d6-128">Bunu yapmak için yalnızca kaldırmak için davranış adını sağlayın `name` özniteliği `<remove>` öğesi.</span><span class="sxs-lookup"><span data-stu-id="c38d6-128">To do so, simply supply the name of the behavior to remove in the `name` attribute of the `<remove>` element.</span></span>  <span data-ttu-id="c38d6-129">Aynı zamanda `<clear>` öğe koleksiyonunun tüm içeriği temizleyerek bir davranış koleksiyonu boş başladığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="c38d6-129">You can also use the `<clear>` element to insure that a behavior collection starts empty by clearing out all the content of the collection.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c38d6-130">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c38d6-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BehaviorsSection>  
 <xref:System.ServiceModel.Configuration.EndpointBehaviorElementCollection>  
 <xref:System.ServiceModel.Configuration.EndpointBehaviorElement>  
 <xref:System.ServiceModel.Configuration.ServiceBehaviorElementCollection>  
 <xref:System.ServiceModel.Configuration.ServiceBehaviorElement>  
 [<span data-ttu-id="c38d6-131">Yapılandırma ve çalışma zamanını davranışlarla genişletme</span><span class="sxs-lookup"><span data-stu-id="c38d6-131">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)  
 [<span data-ttu-id="c38d6-132">İstemci davranışlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c38d6-132">Configuring Client Behaviors</span></span>](../../../../../docs/framework/wcf/configuring-client-behaviors.md)  
 [<span data-ttu-id="c38d6-133">İstemci çalışma zamanı davranışını belirtme</span><span class="sxs-lookup"><span data-stu-id="c38d6-133">Specifying Client Run-Time Behavior</span></span>](../../../../../docs/framework/wcf/specifying-client-run-time-behavior.md)  
 [<span data-ttu-id="c38d6-134">Hizmet çalışma zamanı davranışını belirtme</span><span class="sxs-lookup"><span data-stu-id="c38d6-134">Specifying Service Run-Time Behavior</span></span>](../../../../../docs/framework/wcf/specifying-service-run-time-behavior.md)  
 [<span data-ttu-id="c38d6-135">Güvenlik davranışları</span><span class="sxs-lookup"><span data-stu-id="c38d6-135">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)