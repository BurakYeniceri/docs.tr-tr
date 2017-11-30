---
title: "Paylaşılan WithEvents değişkenlerinin olayları paylaşılmayan yöntemler tarafından işlenemez"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30594
- vbc30594
helpviewer_keywords: BC30594
ms.assetid: 5b9fceb4-ab11-41bb-ad3b-6f1a9da8ae7e
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 53372927b88df3946583564492df42170f302739
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="events-of-shared-withevents-variables-cannot-be-handled-by-non-shared-methods"></a><span data-ttu-id="30029-102">Paylaşılan WithEvents değişkenlerinin olayları paylaşılmayan yöntemler tarafından işlenemez</span><span class="sxs-lookup"><span data-stu-id="30029-102">Events of shared WithEvents variables cannot be handled by non-shared methods</span></span>
<span data-ttu-id="30029-103">İle bildirilen bir değişken `Shared` değiştiricisi paylaşılan bir değişkendir.</span><span class="sxs-lookup"><span data-stu-id="30029-103">A variable declared with the `Shared` modifier is a shared variable.</span></span> <span data-ttu-id="30029-104">Paylaşılan değişken tam olarak bir depolama konumu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="30029-104">A shared variable identifies exactly one storage location.</span></span> <span data-ttu-id="30029-105">İle bildirilen bir değişken `WithEvents` değiştiricisi onaylar değişkeni ait olduğu türü değişkeni başlatır olay kümesini işler.</span><span class="sxs-lookup"><span data-stu-id="30029-105">A variable declared with the `WithEvents` modifier asserts that the type to which the variable belongs handles the set of events the variable raises.</span></span> <span data-ttu-id="30029-106">Değişkene bir değer atandığında, özellik tarafından oluşturulan `WithEvents` bildirim varolan herhangi bir olay işleyicisini unhooks ve yeni olay işleyicisi kancalarını `Add` yöntemi.</span><span class="sxs-lookup"><span data-stu-id="30029-106">When a value is assigned to the variable, the property created by the `WithEvents` declaration unhooks any existing event handler and hooks up the new event handler via the `Add` method.</span></span>  
  
 <span data-ttu-id="30029-107">**Hata Kimliği:** BC30594</span><span class="sxs-lookup"><span data-stu-id="30029-107">**Error ID:** BC30594</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="30029-108">Bu hatayı düzeltmek için</span><span class="sxs-lookup"><span data-stu-id="30029-108">To correct this error</span></span>  
  
-   <span data-ttu-id="30029-109">Olay işleyici bildirmek `Shared`.</span><span class="sxs-lookup"><span data-stu-id="30029-109">Declare your event handler `Shared`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="30029-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="30029-110">See Also</span></span>  
 [<span data-ttu-id="30029-111">Paylaşılan</span><span class="sxs-lookup"><span data-stu-id="30029-111">Shared</span></span>](../../../visual-basic/language-reference/modifiers/shared.md)  
 [<span data-ttu-id="30029-112">WithEvents</span><span class="sxs-lookup"><span data-stu-id="30029-112">WithEvents</span></span>](../../../visual-basic/language-reference/modifiers/withevents.md)
