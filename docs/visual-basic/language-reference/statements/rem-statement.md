---
title: REM Deyimi (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vb.'
- vb.Rem
- Rem
- "'"
helpviewer_keywords:
- REM statement [Visual Basic]
- comments, Visual Basic code
- code comments, Visual Basic
- Visual Basic code, comments
- "' comment marker character [Visual Basic]"
ms.assetid: 34126d7f-e0f9-476d-91e6-b31b398615dc
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d64ce970e3e74437f5e8c63c8a4d578900902192
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="rem-statement-visual-basic"></a><span data-ttu-id="35ef4-102">REM Deyimi (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="35ef4-102">REM Statement (Visual Basic)</span></span>
<span data-ttu-id="35ef4-103">Bir program kaynak kodunda açıklayıcı açıklamalar eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="35ef4-103">Used to include explanatory remarks in the source code of a program.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35ef4-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="35ef4-104">Syntax</span></span>  
  
```  
REM comment  
' comment  
```  
  
## <a name="parts"></a><span data-ttu-id="35ef4-105">Bölümler</span><span class="sxs-lookup"><span data-stu-id="35ef4-105">Parts</span></span>  
 `comment`  
 <span data-ttu-id="35ef4-106">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="35ef4-106">Optional.</span></span> <span data-ttu-id="35ef4-107">Eklemek istediğiniz her türlü açıklamanın metin.</span><span class="sxs-lookup"><span data-stu-id="35ef4-107">The text of any comment you want to include.</span></span> <span data-ttu-id="35ef4-108">Bir arasında gerekli bir alandır `REM` anahtar sözcüğü ve `comment`.</span><span class="sxs-lookup"><span data-stu-id="35ef4-108">A space is required between the `REM` keyword and `comment`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="35ef4-109">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="35ef4-109">Remarks</span></span>  
 <span data-ttu-id="35ef4-110">Koyabilirsiniz bir `REM` deyimi bir satır veya, tek başına, başka bir deyiminden bir satıra koyabilir.</span><span class="sxs-lookup"><span data-stu-id="35ef4-110">You can put a `REM` statement alone on a line, or you can put it on a line following another statement.</span></span> <span data-ttu-id="35ef4-111">`REM` Deyimi satırındaki son deyim olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35ef4-111">The `REM` statement must be the last statement on the line.</span></span> <span data-ttu-id="35ef4-112">Başka bir ifade izliyorsa `REM` bu deyim bir boşlukla ayrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35ef4-112">If it follows another statement, the `REM` must be separated from that statement by a space.</span></span>  
  
 <span data-ttu-id="35ef4-113">Tek tırnak işareti kullanın (`'`) yerine `REM`.</span><span class="sxs-lookup"><span data-stu-id="35ef4-113">You can use a single quotation mark (`'`) instead of `REM`.</span></span> <span data-ttu-id="35ef4-114">Bu, açıklamanızı aynı satırda başka bir ifade izleyen veya tek başına bir satıra bulunur geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="35ef4-114">This is true whether your comment follows another statement on the same line or sits alone on a line.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="35ef4-115">Devam edilemiyor bir `REM` satır devamlılığı sırası kullanarak deyimi (`_`).</span><span class="sxs-lookup"><span data-stu-id="35ef4-115">You cannot continue a `REM` statement by using a line-continuation sequence (`_`).</span></span> <span data-ttu-id="35ef4-116">Bir yorum başladıktan sonra derleyici özel bir anlamı karakter inceleyin değil.</span><span class="sxs-lookup"><span data-stu-id="35ef4-116">Once a comment begins, the compiler does not examine the characters for special meaning.</span></span> <span data-ttu-id="35ef4-117">Birden çok satırlı açıklaması için başka kullanma `REM` deyimi veya açıklama simgesini (`'`) her satırda.</span><span class="sxs-lookup"><span data-stu-id="35ef4-117">For a multiple-line comment, use another `REM` statement or a comment symbol (`'`) on each line.</span></span>  
  
## <a name="example"></a><span data-ttu-id="35ef4-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="35ef4-118">Example</span></span>  
 <span data-ttu-id="35ef4-119">Aşağıdaki örnek gösterilmektedir `REM` bir programda açıklayıcı açıklamalar dahil etmek için kullanılan ifade.</span><span class="sxs-lookup"><span data-stu-id="35ef4-119">The following example illustrates the `REM` statement, which is used to include explanatory remarks in a program.</span></span> <span data-ttu-id="35ef4-120">Ayrıca tek tırnak işareti karakteri kullanmanın alternatif gösterir (`'`) yerine `REM`.</span><span class="sxs-lookup"><span data-stu-id="35ef4-120">It also shows the alternative of using the single quotation-mark character (`'`) instead of `REM`.</span></span>  
  
 [!code-vb[VbVbalrStatements#6](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/rem-statement_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="35ef4-121">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="35ef4-121">See Also</span></span>  
 [<span data-ttu-id="35ef4-122">Kod açıklamaları</span><span class="sxs-lookup"><span data-stu-id="35ef4-122">Comments in Code</span></span>](../../../visual-basic/programming-guide/program-structure/comments-in-code.md)  
 [<span data-ttu-id="35ef4-123">Nasıl yapılır: kodda deyimleri bölme ve birleştirme</span><span class="sxs-lookup"><span data-stu-id="35ef4-123">How to: Break and Combine Statements in Code</span></span>](../../../visual-basic/programming-guide/program-structure/how-to-break-and-combine-statements-in-code.md)