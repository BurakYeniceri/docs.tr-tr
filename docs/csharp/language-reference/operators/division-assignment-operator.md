---
title: "/= İşleci (C# Başvurusu)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- /=_CSharpKeyword
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 26096d9b5dfc565c9933f1ed8ffb241dc900d9ed
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="-operator-c-reference"></a><span data-ttu-id="7235e-102">/= İşleci (C# Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="7235e-102">/= Operator (C# Reference)</span></span>
<span data-ttu-id="7235e-103">Bölme atama işleci.</span><span class="sxs-lookup"><span data-stu-id="7235e-103">The division assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7235e-104">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="7235e-104">Remarks</span></span>  
 <span data-ttu-id="7235e-105">Bir ifade kullanılarak `/=` atama işleci gibi</span><span class="sxs-lookup"><span data-stu-id="7235e-105">An expression using the `/=` assignment operator, such as</span></span>  
  
```  
x /= y  
```  
  
 <span data-ttu-id="7235e-106">eşdeğerdir</span><span class="sxs-lookup"><span data-stu-id="7235e-106">is equivalent to</span></span>  
  
```  
x = x / y  
```  
  
 <span data-ttu-id="7235e-107">dışında `x` yalnızca bir kez değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="7235e-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="7235e-108">[/ İşleci](../../../csharp/language-reference/operators/division-operator.md) bölme gerçekleştirmek sayısal türler için önceden tanımlanmış.</span><span class="sxs-lookup"><span data-stu-id="7235e-108">The [/ operator](../../../csharp/language-reference/operators/division-operator.md) is predefined for numeric types to perform division.</span></span>  
  
 <span data-ttu-id="7235e-109">`/=` İşleci olamaz aşırı yüklenebilir doğrudan, ancak kullanıcı tanımlı türler aşırı yükleme [/ işleci](../../../csharp/language-reference/operators/division-operator.md) (bkz [işleci](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="7235e-109">The `/=` operator cannot be overloaded directly, but user-defined types can overload the [/ operator](../../../csharp/language-reference/operators/division-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="7235e-110">Tüm bileşik atama işleçleri üzerinde örtük olarak ikili İşleç aşırı yüklemesi eşdeğer bileşik atama overloads.</span><span class="sxs-lookup"><span data-stu-id="7235e-110">On all compound assignment operators, overloading the binary operator implicitly overloads the equivalent compound assignment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7235e-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="7235e-111">Example</span></span>  
 [!code-csharp[csRefOperators#5](codesnippet/CSharp/division-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="7235e-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="7235e-112">See Also</span></span>  
 [<span data-ttu-id="7235e-113">C# başvurusu</span><span class="sxs-lookup"><span data-stu-id="7235e-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="7235e-114">C# programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="7235e-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="7235e-115">C# işleçleri</span><span class="sxs-lookup"><span data-stu-id="7235e-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
