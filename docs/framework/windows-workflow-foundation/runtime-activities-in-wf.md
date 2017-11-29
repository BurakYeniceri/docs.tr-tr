---
title: "WF etkinlikleri çalışma zamanı"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e5ae8c31-19bc-4655-88b3-6b75cd6a1bd5
caps.latest.revision: "11"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: f3aca3fcdd4fa8d73bf3412d7c20697847d0a699
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="runtime-activities-in-wf"></a><span data-ttu-id="b7ede-102">WF etkinlikleri çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="b7ede-102">Runtime Activities in WF</span></span>
[!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)]<span data-ttu-id="b7ede-103">kalıcılığı ve sonlandırma gibi iş akışı çalışma zamanı özelliklerine erişmek için birkaç sistem tarafından sağlanan etkinlikler sağlar.</span><span class="sxs-lookup"><span data-stu-id="b7ede-103"> provides several system-provided activities for accessing the features of the workflow runtime, such as persistence and termination.</span></span>  
  
|<span data-ttu-id="b7ede-104">Etkinlik</span><span class="sxs-lookup"><span data-stu-id="b7ede-104">Activity</span></span>|<span data-ttu-id="b7ede-105">Açıklama</span><span class="sxs-lookup"><span data-stu-id="b7ede-105">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.Activities.Statements.Persist>|<span data-ttu-id="b7ede-106">İş akışı durumu kalıcı açıkça istek sayısı.</span><span class="sxs-lookup"><span data-stu-id="b7ede-106">Explicitly requests that the workflow persist its state.</span></span>|  
|<xref:System.Activities.Statements.TerminateWorkflow>|<span data-ttu-id="b7ede-107">Çalışan iş akışı örneği sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="b7ede-107">Terminates the running workflow instance.</span></span>|  
|<xref:System.Activities.Statements.NoPersistScope>|<span data-ttu-id="b7ede-108">Kalıcı gelen alt etkinlikler engeller kapsayıcı etkinliği.</span><span class="sxs-lookup"><span data-stu-id="b7ede-108">A container activity that prevents child activities from persisting.</span></span>|
