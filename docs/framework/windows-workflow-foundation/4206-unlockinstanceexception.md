---
title: 4206 - UnlockInstanceException
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5a46dc5f-d517-4135-8905-25a42f01206b
caps.latest.revision: "2"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 349844edb44e547a666f10c8d210d120ebf5a39f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="4206---unlockinstanceexception"></a><span data-ttu-id="379b5-102">4206 - UnlockInstanceException</span><span class="sxs-lookup"><span data-stu-id="379b5-102">4206 - UnlockInstanceException</span></span>
## <a name="properties"></a><span data-ttu-id="379b5-103">Özellikler</span><span class="sxs-lookup"><span data-stu-id="379b5-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="379b5-104">Kimlik</span><span class="sxs-lookup"><span data-stu-id="379b5-104">ID</span></span>|<span data-ttu-id="379b5-105">4206</span><span class="sxs-lookup"><span data-stu-id="379b5-105">4206</span></span>|  
|<span data-ttu-id="379b5-106">Anahtar Sözcükler</span><span class="sxs-lookup"><span data-stu-id="379b5-106">Keywords</span></span>|<span data-ttu-id="379b5-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="379b5-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="379b5-108">Düzey</span><span class="sxs-lookup"><span data-stu-id="379b5-108">Level</span></span>|<span data-ttu-id="379b5-109">Hata</span><span class="sxs-lookup"><span data-stu-id="379b5-109">Error</span></span>|  
|<span data-ttu-id="379b5-110">Kanal</span><span class="sxs-lookup"><span data-stu-id="379b5-110">Channel</span></span>|<span data-ttu-id="379b5-111">Microsoft Windows uygulaması sunucu-uygulamalar/hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="379b5-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="379b5-112">Açıklama</span><span class="sxs-lookup"><span data-stu-id="379b5-112">Description</span></span>  
 <span data-ttu-id="379b5-113">Bir örneği kilidini çalışılırken bir özel durumla karşılaşıldı gösterir.</span><span class="sxs-lookup"><span data-stu-id="379b5-113">Indicates an exception was encountered while trying to unlock an instance.</span></span>  
  
## <a name="message"></a><span data-ttu-id="379b5-114">İleti</span><span class="sxs-lookup"><span data-stu-id="379b5-114">Message</span></span>  
 <span data-ttu-id="379b5-115">Örnek kilidini açmak çalışırken karşılaşılan %1 özel durumu.</span><span class="sxs-lookup"><span data-stu-id="379b5-115">Encountered exception %1 while attempting to unlock instance.</span></span>  
  
## <a name="details"></a><span data-ttu-id="379b5-116">Ayrıntılar</span><span class="sxs-lookup"><span data-stu-id="379b5-116">Details</span></span>  
  
|<span data-ttu-id="379b5-117">Veri öğesi adı</span><span class="sxs-lookup"><span data-stu-id="379b5-117">Data Item Name</span></span>|<span data-ttu-id="379b5-118">Veri öğesi türü</span><span class="sxs-lookup"><span data-stu-id="379b5-118">Data Item Type</span></span>|<span data-ttu-id="379b5-119">Açıklama</span><span class="sxs-lookup"><span data-stu-id="379b5-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="379b5-120">ExceptionMessage</span><span class="sxs-lookup"><span data-stu-id="379b5-120">ExceptionMessage</span></span>|<span data-ttu-id="379b5-121">xs: String</span><span class="sxs-lookup"><span data-stu-id="379b5-121">xs:string</span></span>|<span data-ttu-id="379b5-122">SQL özel durum iletisi.</span><span class="sxs-lookup"><span data-stu-id="379b5-122">The message from the SQL exception.</span></span>|  
|<span data-ttu-id="379b5-123">AppDomain</span><span class="sxs-lookup"><span data-stu-id="379b5-123">AppDomain</span></span>|<span data-ttu-id="379b5-124">xs: String</span><span class="sxs-lookup"><span data-stu-id="379b5-124">xs:string</span></span>|<span data-ttu-id="379b5-125">AppDomain.CurrentDomain.FriendlyName tarafından döndürülen dize.</span><span class="sxs-lookup"><span data-stu-id="379b5-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
