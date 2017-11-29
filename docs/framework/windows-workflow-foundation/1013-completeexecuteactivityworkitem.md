---
title: 1013 - CompleteExecuteActivityWorkItem
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 31fc57b3-ef2f-48f0-a5de-b4e2c5c9ded7
caps.latest.revision: "3"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 8f430e7b58d5aba277b0a35a20f1f5fdb707bce9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="1013---completeexecuteactivityworkitem"></a><span data-ttu-id="98d24-102">1013 - CompleteExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="98d24-102">1013 - CompleteExecuteActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="98d24-103">Özellikler</span><span class="sxs-lookup"><span data-stu-id="98d24-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="98d24-104">Kimlik</span><span class="sxs-lookup"><span data-stu-id="98d24-104">ID</span></span>|<span data-ttu-id="98d24-105">1013</span><span class="sxs-lookup"><span data-stu-id="98d24-105">1013</span></span>|  
|<span data-ttu-id="98d24-106">Anahtar Sözcükler</span><span class="sxs-lookup"><span data-stu-id="98d24-106">Keywords</span></span>|<span data-ttu-id="98d24-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="98d24-107">WFRuntime</span></span>|  
|<span data-ttu-id="98d24-108">Düzey</span><span class="sxs-lookup"><span data-stu-id="98d24-108">Level</span></span>|<span data-ttu-id="98d24-109">Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="98d24-109">Verbose</span></span>|  
|<span data-ttu-id="98d24-110">Kanal</span><span class="sxs-lookup"><span data-stu-id="98d24-110">Channel</span></span>|<span data-ttu-id="98d24-111">Microsoft Windows uygulaması sunucu-uygulamalar/hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="98d24-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="98d24-112">Açıklama</span><span class="sxs-lookup"><span data-stu-id="98d24-112">Description</span></span>  
 <span data-ttu-id="98d24-113">Bir ExecuteActivityWorkItem tamamlandığını gösterir</span><span class="sxs-lookup"><span data-stu-id="98d24-113">Indicates an ExecuteActivityWorkItem has completed</span></span>  
  
## <a name="message"></a><span data-ttu-id="98d24-114">İleti</span><span class="sxs-lookup"><span data-stu-id="98d24-114">Message</span></span>  
 <span data-ttu-id="98d24-115">'%1', DisplayName etkinliği için bir ExecuteActivityWorkItem tamamlandı: '%2', örnek kimliği: '%3'.</span><span class="sxs-lookup"><span data-stu-id="98d24-115">An ExecuteActivityWorkItem has completed for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="98d24-116">Ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="98d24-116">Details</span></span>  
  
|<span data-ttu-id="98d24-117">Veri öğesi adı</span><span class="sxs-lookup"><span data-stu-id="98d24-117">Data Item Name</span></span>|<span data-ttu-id="98d24-118">Veri öğesi türü</span><span class="sxs-lookup"><span data-stu-id="98d24-118">Data Item Type</span></span>|<span data-ttu-id="98d24-119">Açıklama</span><span class="sxs-lookup"><span data-stu-id="98d24-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="98d24-120">Etkinlik</span><span class="sxs-lookup"><span data-stu-id="98d24-120">Activity</span></span>|<span data-ttu-id="98d24-121">xs: String</span><span class="sxs-lookup"><span data-stu-id="98d24-121">xs:string</span></span>|<span data-ttu-id="98d24-122">Etkinlik türü adı.</span><span class="sxs-lookup"><span data-stu-id="98d24-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="98d24-123">Görünen adı</span><span class="sxs-lookup"><span data-stu-id="98d24-123">DisplayName</span></span>|<span data-ttu-id="98d24-124">xs: String</span><span class="sxs-lookup"><span data-stu-id="98d24-124">xs:string</span></span>|<span data-ttu-id="98d24-125">Etkinliğin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="98d24-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="98d24-126">örnek kimliği</span><span class="sxs-lookup"><span data-stu-id="98d24-126">InstanceId</span></span>|<span data-ttu-id="98d24-127">xs: String</span><span class="sxs-lookup"><span data-stu-id="98d24-127">xs:string</span></span>|<span data-ttu-id="98d24-128">Etkinlik örnek kimliği.</span><span class="sxs-lookup"><span data-stu-id="98d24-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="98d24-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="98d24-129">AppDomain</span></span>|<span data-ttu-id="98d24-130">xs: String</span><span class="sxs-lookup"><span data-stu-id="98d24-130">xs:string</span></span>|<span data-ttu-id="98d24-131">AppDomain.CurrentDomain.FriendlyName tarafından döndürülen dize.</span><span class="sxs-lookup"><span data-stu-id="98d24-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
