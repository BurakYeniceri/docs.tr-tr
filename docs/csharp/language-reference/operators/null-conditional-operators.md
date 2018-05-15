---
title: Null-conditional İşleçleri (C# ve Visual Basic)
ms.date: 04/03/2015
dev_langs:
- csharp
- vb
helpviewer_keywords:
- null-conditional operators [C#]
- null-conditional operators [Visual Basic]
- ?. operator [C#]
- ?. operator [Visual Basic]
- ?[] operator [C#]
- ?[] operator [Visual Basic]
ms.assetid: 9c7b2c8f-a785-44ca-836c-407bfb6d27f5
ms.openlocfilehash: da771fa4a2a89dca308508ea81ef8e0060efa7f0
ms.sourcegitcommit: e5bb395ec86f536e114314184288f40a8c745e2e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2018
---
# <a name="-and--null-conditional-operators-c-and-visual-basic"></a><span data-ttu-id="56366-102">?.</span><span class="sxs-lookup"><span data-stu-id="56366-102">?.</span></span> <span data-ttu-id="56366-103">ve? [] null-conditional işleçleri (C# ve Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="56366-103">and ?[] null-conditional Operators (C# and Visual Basic)</span></span>
<span data-ttu-id="56366-104">Üye erişimi gerçekleştirmeden önce sol işleneni null değerini sınar (`?.`) veya dizin (`?[]`) döndürür; işlem `null` sol işleneni değerlendirilirse `null`.</span><span class="sxs-lookup"><span data-stu-id="56366-104">Tests the value of the left-hand operand for null before performing a member access (`?.`) or index (`?[]`) operation; returns `null` if the left-hand operand evaluates to `null`.</span></span> 

<span data-ttu-id="56366-105">Bu işleçleri özellikle veri yapılara azalan düzen için null işlemek için daha az kod denetler yazmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="56366-105">These operators help you write less code to handle null checks, especially for descending into data structures.</span></span>  
  
```csharp  
int? length = customers?.Length; // null if customers is null   
Customer first = customers?[0];  // null if customers is null  
int? count = customers?[0]?.Orders?.Count();  // null if customers, the first customer, or Orders is null  
```  
  
```vb  
Dim length = customers?.Length  ' null if customers is null  
Dim first as Customer = customers?(0)  ' null if customers is null  
Dim count as Integer? = customers?(0)?.Orders?.Count()  ' null if customers, the first customer, or Orders is null  
```  
  
 <span data-ttu-id="56366-106">Null-conditional işleçleri short-circuiting.</span><span class="sxs-lookup"><span data-stu-id="56366-106">The null-conditional operators are short-circuiting.</span></span>  <span data-ttu-id="56366-107">Koşullu üye erişimi ve dizin işlemi zinciri tek bir işlemde null değeri döndürülürse, rest zincirinin yürütme durdurur.</span><span class="sxs-lookup"><span data-stu-id="56366-107">If one operation in a chain of conditional member access and index operation returns null, then the rest of the chain’s execution stops.</span></span>  <span data-ttu-id="56366-108">Aşağıdaki örnekte, `E` varsa yürütmez `A`, `B`, veya `C` null olarak değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="56366-108">In the following example, `E` doesn't execute if `A`, `B`, or `C` evaluates to null.</span></span>
  
```csharp
A?.B?.C?.Do(E);
A?.B?.C?[E];
```

```vb
A?.B?.C?.Do(E);
A?.B?.C?(E);
```  
  
 <span data-ttu-id="56366-109">Başka bir kullanım null-conditional üye erişimi için çok az kod ile iş parçacığı açısından güvenli şekilde temsilciler çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="56366-109">Another use for the null-conditional member access is invoking delegates in a thread-safe way with much less code.</span></span>  <span data-ttu-id="56366-110">Eski şekilde aşağıdaki gibi bir kod gerektirir:</span><span class="sxs-lookup"><span data-stu-id="56366-110">The old way requires code like the following:</span></span>  
  
```csharp  
var handler = this.PropertyChanged;  
if (handler != null)  
    handler(…);
```  
  
```vb  
Dim handler = AddressOf(Me.PropertyChanged)  
If handler IsNot Nothing  
    Call handler(…)  
```  
  
 <span data-ttu-id="56366-111">Yeni yol çok daha kolaydır:</span><span class="sxs-lookup"><span data-stu-id="56366-111">The new way is much simpler:</span></span>  
  
```csharp
PropertyChanged?.Invoke(…)  
```  

```vb
PropertyChanged?.Invoke(…)
```  
  
 <span data-ttu-id="56366-112">Derleyici değerlendirmek için kod oluşturur çünkü iş parçacığı yeni yoludur `PropertyChanged` sonucu geçici bir değişkende tutma yalnızca bir kez.</span><span class="sxs-lookup"><span data-stu-id="56366-112">The new way is thread-safe because the compiler generates code to evaluate `PropertyChanged` one time only, keeping the result in a temporary variable.</span></span> <span data-ttu-id="56366-113">Açıkça çağırmanız gerekir `Invoke` yöntemi hiçbir null-conditional temsilci çağırma sözdizimi olduğundan `PropertyChanged?(e)`.</span><span class="sxs-lookup"><span data-stu-id="56366-113">You need to explicitly call the `Invoke` method because there is no null-conditional delegate invocation syntax `PropertyChanged?(e)`.</span></span>  
  
## <a name="language-specifications"></a><span data-ttu-id="56366-114">Dil belirtimleri</span><span class="sxs-lookup"><span data-stu-id="56366-114">Language Specifications</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
 <span data-ttu-id="56366-115">Daha fazla bilgi için bkz: [Visual Basic dil başvurusu](../../../visual-basic/language-reference/index.md).</span><span class="sxs-lookup"><span data-stu-id="56366-115">For more information, see the [Visual Basic Language Reference](../../../visual-basic/language-reference/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56366-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="56366-116">See Also</span></span>  
 [<span data-ttu-id="56366-117">?? (null birleşim işleci)</span><span class="sxs-lookup"><span data-stu-id="56366-117">?? (null-coalescing operator)</span></span>](null-conditional-operator.md)  
 [<span data-ttu-id="56366-118">C# başvurusu</span><span class="sxs-lookup"><span data-stu-id="56366-118">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="56366-119">C# Programlama Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="56366-119">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="56366-120">Visual Basic programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="56366-120">Visual Basic Programming Guide</span></span>](../../../visual-basic/programming-guide/index.md)
