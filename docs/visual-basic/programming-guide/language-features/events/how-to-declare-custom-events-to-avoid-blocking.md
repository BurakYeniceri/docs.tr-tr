---
title: "Nasıl yapılır: Engellemekten Kaçınacak Şekilde Özel Olayları Bildirme (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- declaring events [Visual Basic], custom
- events [Visual Basic], custom
- custom events [Visual Basic]
ms.assetid: 998b6a90-67c5-4d2c-8b11-366d3e355505
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 4a36c855efb67752674615a61f2fa701974ce5f1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-declare-custom-events-to-avoid-blocking-visual-basic"></a><span data-ttu-id="3f867-102">Nasıl yapılır: Engellemekten Kaçınacak Şekilde Özel Olayları Bildirme (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3f867-102">How to: Declare Custom Events To Avoid Blocking (Visual Basic)</span></span>
<span data-ttu-id="3f867-103">Bu bir olay işleyicisi değil sonraki olay işleyicileri engelle önemli olduğu durumlarda bazı durumlar vardır.</span><span class="sxs-lookup"><span data-stu-id="3f867-103">There are several circumstances when it is important that one event handler not block subsequent event handlers.</span></span> <span data-ttu-id="3f867-104">Özel olaylar, olay işleyicileri zaman uyumsuz olarak çağırmak olay izin verin.</span><span class="sxs-lookup"><span data-stu-id="3f867-104">Custom events allow the event to call its event handlers asynchronously.</span></span>  
  
 <span data-ttu-id="3f867-105">Varsayılan olarak, yedekleme deposu için bir olay bildirimi seri olarak tüm olay işleyicileri birleştiren bir çok noktaya yayın temsilci alandır.</span><span class="sxs-lookup"><span data-stu-id="3f867-105">By default, the backing-store field for an event declaration is a multicast delegate that serially combines all the event handlers.</span></span> <span data-ttu-id="3f867-106">Bu, bir işleyici tamamlanması uzun sürüyorsa, işlem tamamlanana kadar diğer işleyicilerin engellediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3f867-106">This means that if one handler takes a long time to complete, it blocks the other handlers until it completes.</span></span> <span data-ttu-id="3f867-107">(Uyum gösteren olay işleyicileri hiçbir zaman uzun veya olası engelleme işlemleri gerçekleştirmeniz gerekir.)</span><span class="sxs-lookup"><span data-stu-id="3f867-107">(Well-behaved event handlers should never perform lengthy or potentially blocking operations.)</span></span>  
  
 <span data-ttu-id="3f867-108">Visual Basic sağlar olayları varsayılan uygulaması kullanmak yerine özel bir olay olay işleyicileri yürütülecek zaman uyumsuz olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f867-108">Instead of using the default implementation of events that Visual Basic provides, you can use a custom event to execute the event handlers asynchronously.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f867-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="3f867-109">Example</span></span>  
 <span data-ttu-id="3f867-110">Bu örnekte, `AddHandler` erişimci ekler her işleyicisi için temsilci `Click` olaya bir <xref:System.Collections.ArrayList> depolanan `EventHandlerList` alan.</span><span class="sxs-lookup"><span data-stu-id="3f867-110">In this example, the `AddHandler` accessor adds the delegate for each handler of the `Click` event to an <xref:System.Collections.ArrayList> stored in the `EventHandlerList` field.</span></span>  
  
 <span data-ttu-id="3f867-111">Ne zaman, başlatır kod `Click` olayı `RaiseEvent` erişimci tüm olay işleyici temsilcileri kullanarak zaman uyumsuz olarak çağırır <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="3f867-111">When code raises the `Click` event, the `RaiseEvent` accessor invokes all the event handler delegates asynchronously using the <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A> method.</span></span> <span data-ttu-id="3f867-112">Bu yöntem, bir çalışan iş parçacığı üzerinde her işleyiciyi çağırır ve işleyicileri birbirine engellemek için hemen döndürür.</span><span class="sxs-lookup"><span data-stu-id="3f867-112">That method invokes each handler on a worker thread and returns immediately, so handlers cannot block one another.</span></span>  
  
 [!code-vb[VbVbalrEvents#27](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-declare-custom-events-to-avoid-blocking_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="3f867-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="3f867-113">See Also</span></span>  
 <xref:System.Collections.ArrayList>  
 <xref:System.Web.Services.Protocols.LogicalMethodInfo.BeginInvoke%2A>  
 [<span data-ttu-id="3f867-114">Olayları</span><span class="sxs-lookup"><span data-stu-id="3f867-114">Events</span></span>](../../../../visual-basic/programming-guide/language-features/events/index.md)  
 [<span data-ttu-id="3f867-115">Nasıl yapılır: bellekten kazanacak şekilde özel olayları bildirme</span><span class="sxs-lookup"><span data-stu-id="3f867-115">How to: Declare Custom Events To Conserve Memory</span></span>](../../../../visual-basic/programming-guide/language-features/events/how-to-declare-custom-events-to-conserve-memory.md)
