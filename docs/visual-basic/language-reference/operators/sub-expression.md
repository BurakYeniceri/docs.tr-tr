---
title: "Alt İfade (Visual Basic)"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- lambda expressions [Visual Basic], sub expression
- Sub Expression [Visual Basic]
- subroutines [Visual Basic], sub expressions
ms.assetid: 36b6bfd1-6539-4d8f-a5eb-6541a745ffde
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 43e35bd0386bc56478603ec36437981785cc8ffb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="sub-expression-visual-basic"></a><span data-ttu-id="cb130-102">Alt İfade (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cb130-102">Sub Expression (Visual Basic)</span></span>
<span data-ttu-id="cb130-103">Parametreler ve alt yordama lambda ifadesi tanımlamak kod bildirir.</span><span class="sxs-lookup"><span data-stu-id="cb130-103">Declares the parameters and code that define a subroutine lambda expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cb130-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="cb130-104">Syntax</span></span>  
  
```  
Sub ( [ parameterlist ] ) statement  
- or -  
Sub ( [ parameterlist ] )  
  [ statements ]  
End Sub  
```  
  
## <a name="parts"></a><span data-ttu-id="cb130-105">Bölümler</span><span class="sxs-lookup"><span data-stu-id="cb130-105">Parts</span></span>  
  
|<span data-ttu-id="cb130-106">Terim</span><span class="sxs-lookup"><span data-stu-id="cb130-106">Term</span></span>|<span data-ttu-id="cb130-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb130-107">Definition</span></span>|  
|---|---|  
|`parameterlist`|<span data-ttu-id="cb130-108">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="cb130-108">Optional.</span></span> <span data-ttu-id="cb130-109">Yordam parametreleri temsil eden yerel değişken adları listesi.</span><span class="sxs-lookup"><span data-stu-id="cb130-109">A list of local variable names that represent the parameters of the procedure.</span></span> <span data-ttu-id="cb130-110">Parantez listesi boş olsa bile mevcut olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb130-110">The parentheses must be present even when the list is empty.</span></span> <span data-ttu-id="cb130-111">Daha fazla bilgi için bkz: [parametre listesi](../../../visual-basic/language-reference/statements/parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="cb130-111">For more information, see [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span></span>|  
|`statement`|<span data-ttu-id="cb130-112">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="cb130-112">Required.</span></span> <span data-ttu-id="cb130-113">Tek bir deyimde.</span><span class="sxs-lookup"><span data-stu-id="cb130-113">A single statement.</span></span>|  
|`statements`|<span data-ttu-id="cb130-114">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="cb130-114">Required.</span></span> <span data-ttu-id="cb130-115">Deyimleri listesi.</span><span class="sxs-lookup"><span data-stu-id="cb130-115">A list of statements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cb130-116">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="cb130-116">Remarks</span></span>  
 <span data-ttu-id="cb130-117">A *lambda ifadesi* bir ada sahip olmayan bir alt yordama olduğunu ve bir veya daha fazla deyimleri yürütür.</span><span class="sxs-lookup"><span data-stu-id="cb130-117">A *lambda expression* is a subroutine that does not have a name and that executes one or more statements.</span></span> <span data-ttu-id="cb130-118">Lambda ifadesi yerde kullanabilir, bir temsilci türü dışında bağımsız değişken olarak kullanabileceğiniz `RemoveHandler`.</span><span class="sxs-lookup"><span data-stu-id="cb130-118">You can use a lambda expression anywhere that you can use a delegate type, except as an argument to `RemoveHandler`.</span></span> <span data-ttu-id="cb130-119">Temsilciler ve temsilciler ile lambda ifadeleri kullanma hakkında daha fazla bilgi için bkz: [temsilci deyimi](../../../visual-basic/language-reference/statements/delegate-statement.md) ve [gevşek temsilci dönüşümü](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span><span class="sxs-lookup"><span data-stu-id="cb130-119">For more information about delegates, and the use of lambda expressions with delegates, see [Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) and [Relaxed Delegate Conversion](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span></span>  
  
## <a name="lambda-expression-syntax"></a><span data-ttu-id="cb130-120">Lambda İfadesi Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="cb130-120">Lambda Expression Syntax</span></span>  
 <span data-ttu-id="cb130-121">Lambda ifadesi sözdizimi, standart bir alt yordama benzer.</span><span class="sxs-lookup"><span data-stu-id="cb130-121">The syntax of a lambda expression resembles that of a standard subroutine.</span></span> <span data-ttu-id="cb130-122">Farkları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="cb130-122">The differences are as follows:</span></span>  
  
-   <span data-ttu-id="cb130-123">Lambda ifadesi bir adı yok.</span><span class="sxs-lookup"><span data-stu-id="cb130-123">A lambda expression does not have a name.</span></span>  
  
-   <span data-ttu-id="cb130-124">Lambda ifadesi bir değiştiricisi gibi olamaz `Overloads` veya `Overrides`.</span><span class="sxs-lookup"><span data-stu-id="cb130-124">A lambda expression cannot have a modifier, such as `Overloads` or `Overrides`.</span></span>  
  
-   <span data-ttu-id="cb130-125">Tek satırlı lambda ifadesi gövdesi bir deyim, bir ifade olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cb130-125">The body of a single-line lambda expression must be a statement, not an expression.</span></span> <span data-ttu-id="cb130-126">Gövde alt yordam çağrısı, ancak olmayan bir işlev yordamı çağrısı oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="cb130-126">The body can consist of a call to a sub procedure, but not a call to a function procedure.</span></span>  
  
-   <span data-ttu-id="cb130-127">Lambda ifadesinde, veri türleri veya tüm parametreleri olayla gerekir ya da tüm parametreleri belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="cb130-127">In a lambda expression, either all parameters must have specified data types or all parameters must be inferred.</span></span>  
  
-   <span data-ttu-id="cb130-128">İsteğe bağlı ve `ParamArray` parametreleri lambda ifadelerde izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="cb130-128">Optional and `ParamArray` parameters are not permitted in lambda expressions.</span></span>  
  
-   <span data-ttu-id="cb130-129">Genel Parametreler lambda ifadelerde izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="cb130-129">Generic parameters are not permitted in lambda expressions.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb130-130">Örnek</span><span class="sxs-lookup"><span data-stu-id="cb130-130">Example</span></span>  
 <span data-ttu-id="cb130-131">Aşağıdaki değer konsola yazar bir lambda ifadesi bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="cb130-131">Following is an example of a lambda expression that writes a value to the console.</span></span> <span data-ttu-id="cb130-132">Aşağıdaki örnekte, hem tek satırlı ve çok satırlı lambda ifadesi sözdizimi alt yordam için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cb130-132">The example shows both the single-line and multiline lambda expression syntax for a subroutine.</span></span> <span data-ttu-id="cb130-133">Daha fazla örnek için bkz: [Lambda ifadeleri](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="cb130-133">For more examples, see [Lambda Expressions](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span></span>  
  
 [!code-vb[VbVbalrLambdas#15](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/sub-expression_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="cb130-134">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="cb130-134">See Also</span></span>  
 [<span data-ttu-id="cb130-135">Sub deyimi</span><span class="sxs-lookup"><span data-stu-id="cb130-135">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
 [<span data-ttu-id="cb130-136">Lambda ifadeleri</span><span class="sxs-lookup"><span data-stu-id="cb130-136">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)  
 [<span data-ttu-id="cb130-137">İşleçler ve ifadeler</span><span class="sxs-lookup"><span data-stu-id="cb130-137">Operators and Expressions</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)  
 [<span data-ttu-id="cb130-138">Deyimleri</span><span class="sxs-lookup"><span data-stu-id="cb130-138">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)  
 [<span data-ttu-id="cb130-139">Gevşek temsilci dönüşümü</span><span class="sxs-lookup"><span data-stu-id="cb130-139">Relaxed Delegate Conversion</span></span>](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
