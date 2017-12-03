---
title: '&lt;persistableType&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 56443902885e191d93897096e55742f7665ba00a
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2017
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="30c7c-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="30c7c-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="30c7c-103">Tüm kalıcı türlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30c7c-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="30c7c-104">\<Sistem. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="30c7c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="30c7c-105">\<comContracts ></span><span class="sxs-lookup"><span data-stu-id="30c7c-105">\<comContracts></span></span>  
<span data-ttu-id="30c7c-106">\<comContract ></span><span class="sxs-lookup"><span data-stu-id="30c7c-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="30c7c-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="30c7c-107">Syntax</span></span>  
  
```xml  
<comContracts>  
  <comContract>  
      <persistableTypes>  
         <persistableType id="string"  
            name="string">  
         </persistableType>  
      </persistableTypes>  
  </comContract>  
</comContracts>  
```  
  
## <a name="type"></a><span data-ttu-id="30c7c-108">Tür</span><span class="sxs-lookup"><span data-stu-id="30c7c-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="30c7c-109">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="30c7c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="30c7c-110">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="30c7c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="30c7c-111">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="30c7c-111">Attributes</span></span>  
  
|<span data-ttu-id="30c7c-112">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="30c7c-112">Attribute</span></span>|<span data-ttu-id="30c7c-113">Açıklama</span><span class="sxs-lookup"><span data-stu-id="30c7c-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="30c7c-114">kimlik</span><span class="sxs-lookup"><span data-stu-id="30c7c-114">id</span></span>|<span data-ttu-id="30c7c-115">Kalıcı bir türü için benzersiz bir tanımlayıcı belirten bir dize içeriyor gerekli bir öznitelik.</span><span class="sxs-lookup"><span data-stu-id="30c7c-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="30c7c-116">name</span><span class="sxs-lookup"><span data-stu-id="30c7c-116">name</span></span>|<span data-ttu-id="30c7c-117">Kalıcı türünün adını belirten dize içeren bir isteğe bağlı öznitelik.</span><span class="sxs-lookup"><span data-stu-id="30c7c-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="30c7c-118">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="30c7c-118">Child Elements</span></span>  
 <span data-ttu-id="30c7c-119">Yok.</span><span class="sxs-lookup"><span data-stu-id="30c7c-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="30c7c-120">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="30c7c-120">Parent Elements</span></span>  
  
|<span data-ttu-id="30c7c-121">Öğe</span><span class="sxs-lookup"><span data-stu-id="30c7c-121">Element</span></span>|<span data-ttu-id="30c7c-122">Açıklama</span><span class="sxs-lookup"><span data-stu-id="30c7c-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="30c7c-123">\<persistableTypes ></span><span class="sxs-lookup"><span data-stu-id="30c7c-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="30c7c-124">Bir koleksiyonu `persistableType` öğeleri.</span><span class="sxs-lookup"><span data-stu-id="30c7c-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="30c7c-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="30c7c-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>  
 [<span data-ttu-id="30c7c-126">\<comContracts ></span><span class="sxs-lookup"><span data-stu-id="30c7c-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="30c7c-127">COM + uygulamaları ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="30c7c-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="30c7c-128">Nasıl yapılır: COM + hizmet ayarlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30c7c-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
