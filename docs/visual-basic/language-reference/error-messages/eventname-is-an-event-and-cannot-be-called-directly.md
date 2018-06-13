---
title: '&#39;&lt;eventname&gt; &#39; bir olaydır ve doğrudan çağrılamaz'
ms.date: 07/20/2015
f1_keywords:
- bc32022
- vbc32022
helpviewer_keywords:
- BC32022
ms.assetid: 4dcfcb8d-a9fa-46a7-a034-29d9ff3a59b3
ms.openlocfilehash: 4d8a7d716d2b7c52d1d027a1e7959d981bb0857e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33587338"
---
# <a name="39lteventnamegt39-is-an-event-and-cannot-be-called-directly"></a><span data-ttu-id="b2978-102">&#39;&lt;eventname&gt; &#39; bir olaydır ve doğrudan çağrılamaz</span><span class="sxs-lookup"><span data-stu-id="b2978-102">&#39;&lt;eventname&gt;&#39; is an event, and cannot be called directly</span></span>
<span data-ttu-id="b2978-103">' <`eventname`>' bir olaydır ve bu nedenle doğrudan çağrılamaz.</span><span class="sxs-lookup"><span data-stu-id="b2978-103">'<`eventname`>' is an event, and so cannot be called directly.</span></span> <span data-ttu-id="b2978-104">Kullanım bir `RaiseEvent` deyimi bir olayı.</span><span class="sxs-lookup"><span data-stu-id="b2978-104">Use a `RaiseEvent` statement to raise an event.</span></span>  
  
 <span data-ttu-id="b2978-105">Bir yordam çağrısı yordam adı için bir olay belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2978-105">A procedure call specifies an event for the procedure name.</span></span> <span data-ttu-id="b2978-106">Olay işleyicisi bir yordamdır, ancak olay gerçekleşti ve işlenmiş gerekir bir sinyal, aygıttır.</span><span class="sxs-lookup"><span data-stu-id="b2978-106">An event handler is a procedure, but the event itself is a signaling device, which must be raised and handled.</span></span>  
  
 <span data-ttu-id="b2978-107">**Hata Kimliği:** BC32022</span><span class="sxs-lookup"><span data-stu-id="b2978-107">**Error ID:** BC32022</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b2978-108">Bu hatayı düzeltmek için</span><span class="sxs-lookup"><span data-stu-id="b2978-108">To correct this error</span></span>  
  
1.  <span data-ttu-id="b2978-109">Kullanım bir `RaiseEvent` bir olay sinyal ve yordam ya da bu yordamlar çağırma bildirimini.</span><span class="sxs-lookup"><span data-stu-id="b2978-109">Use a `RaiseEvent` statement to signal an event and invoke the procedure or procedures that handle it.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2978-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="b2978-110">See Also</span></span>  
 [<span data-ttu-id="b2978-111">RaiseEvent Deyimi</span><span class="sxs-lookup"><span data-stu-id="b2978-111">RaiseEvent Statement</span></span>](../../../visual-basic/language-reference/statements/raiseevent-statement.md)
