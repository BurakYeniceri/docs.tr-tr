---
title: Alt İfade (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- lambda expressions [Visual Basic], sub expression
- Sub Expression [Visual Basic]
- subroutines [Visual Basic], sub expressions
ms.assetid: 36b6bfd1-6539-4d8f-a5eb-6541a745ffde
ms.openlocfilehash: 602212e664fa3362742fb1ba0dc033610272d3af
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33603541"
---
# <a name="sub-expression-visual-basic"></a><span data-ttu-id="a3a85-102">Alt İfade (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a3a85-102">Sub Expression (Visual Basic)</span></span>
<span data-ttu-id="a3a85-103">Parametreler ve alt yordama lambda ifadesi tanımlamak kod bildirir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-103">Declares the parameters and code that define a subroutine lambda expression.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3a85-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a3a85-104">Syntax</span></span>  
  
```  
Sub ( [ parameterlist ] ) statement  
- or -  
Sub ( [ parameterlist ] )  
  [ statements ]  
End Sub  
```  
  
## <a name="parts"></a><span data-ttu-id="a3a85-105">Bölümler</span><span class="sxs-lookup"><span data-stu-id="a3a85-105">Parts</span></span>  
  
|<span data-ttu-id="a3a85-106">Terim</span><span class="sxs-lookup"><span data-stu-id="a3a85-106">Term</span></span>|<span data-ttu-id="a3a85-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3a85-107">Definition</span></span>|  
|---|---|  
|`parameterlist`|<span data-ttu-id="a3a85-108">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="a3a85-108">Optional.</span></span> <span data-ttu-id="a3a85-109">Yordam parametreleri temsil eden yerel değişken adları listesi.</span><span class="sxs-lookup"><span data-stu-id="a3a85-109">A list of local variable names that represent the parameters of the procedure.</span></span> <span data-ttu-id="a3a85-110">Parantez listesi boş olsa bile mevcut olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-110">The parentheses must be present even when the list is empty.</span></span> <span data-ttu-id="a3a85-111">Daha fazla bilgi için bkz: [parametre listesi](../../../visual-basic/language-reference/statements/parameter-list.md).</span><span class="sxs-lookup"><span data-stu-id="a3a85-111">For more information, see [Parameter List](../../../visual-basic/language-reference/statements/parameter-list.md).</span></span>|  
|`statement`|<span data-ttu-id="a3a85-112">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="a3a85-112">Required.</span></span> <span data-ttu-id="a3a85-113">Tek bir deyimde.</span><span class="sxs-lookup"><span data-stu-id="a3a85-113">A single statement.</span></span>|  
|`statements`|<span data-ttu-id="a3a85-114">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="a3a85-114">Required.</span></span> <span data-ttu-id="a3a85-115">Deyimleri listesi.</span><span class="sxs-lookup"><span data-stu-id="a3a85-115">A list of statements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a3a85-116">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="a3a85-116">Remarks</span></span>  
 <span data-ttu-id="a3a85-117">A *lambda ifadesi* bir ada sahip olmayan bir alt yordama olduğunu ve bir veya daha fazla deyimleri yürütür.</span><span class="sxs-lookup"><span data-stu-id="a3a85-117">A *lambda expression* is a subroutine that does not have a name and that executes one or more statements.</span></span> <span data-ttu-id="a3a85-118">Lambda ifadesi yerde kullanabilir, bir temsilci türü dışında bağımsız değişken olarak kullanabileceğiniz `RemoveHandler`.</span><span class="sxs-lookup"><span data-stu-id="a3a85-118">You can use a lambda expression anywhere that you can use a delegate type, except as an argument to `RemoveHandler`.</span></span> <span data-ttu-id="a3a85-119">Temsilciler ve temsilciler ile lambda ifadeleri kullanma hakkında daha fazla bilgi için bkz: [temsilci deyimi](../../../visual-basic/language-reference/statements/delegate-statement.md) ve [gevşek temsilci dönüşümü](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span><span class="sxs-lookup"><span data-stu-id="a3a85-119">For more information about delegates, and the use of lambda expressions with delegates, see [Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) and [Relaxed Delegate Conversion](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md).</span></span>  
  
## <a name="lambda-expression-syntax"></a><span data-ttu-id="a3a85-120">Lambda İfadesi Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a3a85-120">Lambda Expression Syntax</span></span>  
 <span data-ttu-id="a3a85-121">Lambda ifadesi sözdizimi, standart bir alt yordama benzer.</span><span class="sxs-lookup"><span data-stu-id="a3a85-121">The syntax of a lambda expression resembles that of a standard subroutine.</span></span> <span data-ttu-id="a3a85-122">Farkları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="a3a85-122">The differences are as follows:</span></span>  
  
-   <span data-ttu-id="a3a85-123">Lambda ifadesi bir adı yok.</span><span class="sxs-lookup"><span data-stu-id="a3a85-123">A lambda expression does not have a name.</span></span>  
  
-   <span data-ttu-id="a3a85-124">Lambda ifadesi bir değiştiricisi gibi olamaz `Overloads` veya `Overrides`.</span><span class="sxs-lookup"><span data-stu-id="a3a85-124">A lambda expression cannot have a modifier, such as `Overloads` or `Overrides`.</span></span>  
  
-   <span data-ttu-id="a3a85-125">Tek satırlı lambda ifadesi gövdesi bir deyim, bir ifade olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a3a85-125">The body of a single-line lambda expression must be a statement, not an expression.</span></span> <span data-ttu-id="a3a85-126">Gövde alt yordam çağrısı, ancak olmayan bir işlev yordamı çağrısı oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-126">The body can consist of a call to a sub procedure, but not a call to a function procedure.</span></span>  
  
-   <span data-ttu-id="a3a85-127">Lambda ifadesinde, veri türleri veya tüm parametreleri olayla gerekir ya da tüm parametreleri belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-127">In a lambda expression, either all parameters must have specified data types or all parameters must be inferred.</span></span>  
  
-   <span data-ttu-id="a3a85-128">İsteğe bağlı ve `ParamArray` parametreleri lambda ifadelerde izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="a3a85-128">Optional and `ParamArray` parameters are not permitted in lambda expressions.</span></span>  
  
-   <span data-ttu-id="a3a85-129">Genel Parametreler lambda ifadelerde izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="a3a85-129">Generic parameters are not permitted in lambda expressions.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a3a85-130">Örnek</span><span class="sxs-lookup"><span data-stu-id="a3a85-130">Example</span></span>  
 <span data-ttu-id="a3a85-131">Aşağıdaki değer konsola yazar bir lambda ifadesi bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-131">Following is an example of a lambda expression that writes a value to the console.</span></span> <span data-ttu-id="a3a85-132">Aşağıdaki örnekte, hem tek satırlı ve çok satırlı lambda ifadesi sözdizimi alt yordam için gösterilir.</span><span class="sxs-lookup"><span data-stu-id="a3a85-132">The example shows both the single-line and multiline lambda expression syntax for a subroutine.</span></span> <span data-ttu-id="a3a85-133">Daha fazla örnek için bkz: [Lambda ifadeleri](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="a3a85-133">For more examples, see [Lambda Expressions](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md).</span></span>  
  
 [!code-vb[VbVbalrLambdas#15](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/sub-expression_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="a3a85-134">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a3a85-134">See Also</span></span>  
 [<span data-ttu-id="a3a85-135">Sub Deyimi</span><span class="sxs-lookup"><span data-stu-id="a3a85-135">Sub Statement</span></span>](../../../visual-basic/language-reference/statements/sub-statement.md)  
 [<span data-ttu-id="a3a85-136">Lambda İfadeleri</span><span class="sxs-lookup"><span data-stu-id="a3a85-136">Lambda Expressions</span></span>](../../../visual-basic/programming-guide/language-features/procedures/lambda-expressions.md)  
 [<span data-ttu-id="a3a85-137">İşleçler ve İfadeler</span><span class="sxs-lookup"><span data-stu-id="a3a85-137">Operators and Expressions</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)  
 [<span data-ttu-id="a3a85-138">Deyimler</span><span class="sxs-lookup"><span data-stu-id="a3a85-138">Statements</span></span>](../../../visual-basic/programming-guide/language-features/statements.md)  
 [<span data-ttu-id="a3a85-139">Gevşek Temsilci Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="a3a85-139">Relaxed Delegate Conversion</span></span>](../../../visual-basic/programming-guide/language-features/delegates/relaxed-delegate-conversion.md)
