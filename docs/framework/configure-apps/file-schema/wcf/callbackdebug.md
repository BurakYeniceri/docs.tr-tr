---
title: '&lt;callbackDebug&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 4073feda-1857-4be4-9947-227afb847ced
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: ccb48efcdd1924ade27220a685e146a7f5eeef76
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="ltcallbackdebuggt"></a><span data-ttu-id="d21a4-102">&lt;callbackDebug&gt;</span><span class="sxs-lookup"><span data-stu-id="d21a4-102">&lt;callbackDebug&gt;</span></span>
<span data-ttu-id="d21a4-103">Hizmeti için hata ayıklama belirten bir [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] geri çağırma nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d21a4-103">Specifies service debugging for a [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] callback object.</span></span>  
  
 <span data-ttu-id="d21a4-104">\<Sistem. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="d21a4-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="d21a4-105">\<davranışları ></span><span class="sxs-lookup"><span data-stu-id="d21a4-105">\<behaviors></span></span>  
<span data-ttu-id="d21a4-106">\<endpointBehaviors ></span><span class="sxs-lookup"><span data-stu-id="d21a4-106">\<endpointBehaviors></span></span>  
<span data-ttu-id="d21a4-107">\<davranışı ></span><span class="sxs-lookup"><span data-stu-id="d21a4-107">\<behavior></span></span>  
<span data-ttu-id="d21a4-108">\<callbackDebug ></span><span class="sxs-lookup"><span data-stu-id="d21a4-108">\<callbackDebug></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d21a4-109">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d21a4-109">Syntax</span></span>  
  
```xml  
<callbackDebug  includeExceptionDetailInFaults="Boolean" />  
```  
  
## <a name="type"></a><span data-ttu-id="d21a4-110">Tür</span><span class="sxs-lookup"><span data-stu-id="d21a4-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d21a4-111">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="d21a4-111">Attributes and Elements</span></span>  
 <span data-ttu-id="d21a4-112">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d21a4-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d21a4-113">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="d21a4-113">Attributes</span></span>  
  
|<span data-ttu-id="d21a4-114">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="d21a4-114">Attribute</span></span>|<span data-ttu-id="d21a4-115">Açıklama</span><span class="sxs-lookup"><span data-stu-id="d21a4-115">Description</span></span>|  
|---------------|-----------------|  
|`includeExceptionDetailInFaults`|<span data-ttu-id="d21a4-116">İstemci geri araması nesneleri yönetilen özel durum bilgilerini SOAP hataları hizmete geri döndürme olup olmadığını belirten bir değer.</span><span class="sxs-lookup"><span data-stu-id="d21a4-116">A value that specifies whether client callback objects return managed exception information in SOAP faults back to the service.</span></span><br /><br /> <span data-ttu-id="d21a4-117">Bu öznitelik ayarlanırsa, `true` tekrar hata ayıklama amacıyla hizmet için bir istemci geri çağırma nesnesindeki yönetilen özel durum bilgi akışını programlı olarak etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d21a4-117">If you set this attribute to `true` programmatically, you can enable the flow of managed exception information in a client callback object back to the service for debugging purposes.</span></span> <span data-ttu-id="d21a4-118">**Dikkat:** döndürme istemcilere yönetilen özel durum bilgileri, bir güvenlik riski olabilir.</span><span class="sxs-lookup"><span data-stu-id="d21a4-118">**Caution:**  Returning managed exception information to clients can be a security risk.</span></span> <span data-ttu-id="d21a4-119">Özel durum ayrıntıları yetkisiz istemcileri tarafından kullanılan iç hizmet uygulaması hakkında bilgi kullanıma olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="d21a4-119">This is because exception details expose information about the internal service implementation that could be used by unauthorized clients.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d21a4-120">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="d21a4-120">Child Elements</span></span>  
 <span data-ttu-id="d21a4-121">Yok.</span><span class="sxs-lookup"><span data-stu-id="d21a4-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d21a4-122">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="d21a4-122">Parent Elements</span></span>  
  
|<span data-ttu-id="d21a4-123">Öğe</span><span class="sxs-lookup"><span data-stu-id="d21a4-123">Element</span></span>|<span data-ttu-id="d21a4-124">Açıklama</span><span class="sxs-lookup"><span data-stu-id="d21a4-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d21a4-125">\<davranışı ></span><span class="sxs-lookup"><span data-stu-id="d21a4-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="d21a4-126">Bir uç nokta davranışını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d21a4-126">Specifies an endpoint behavior.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d21a4-127">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d21a4-127">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.CallbackDebugElement>  
 <xref:System.ServiceModel.Description.CallbackDebugBehavior>
