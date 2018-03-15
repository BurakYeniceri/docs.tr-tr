---
title: "parametresi değiştiricisi (C# Başvurusu)"
ms.date: 03/06/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- parameters [C#], in
- in parameters [C#]
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 035aac3e6b902f607e533b709713eb1d07c9774a
ms.sourcegitcommit: 83dd5ec003e788ccb3e33f3412a7af39ae347646
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2018
---
# <a name="in-parameter-modifier-c-reference"></a><span data-ttu-id="5ac23-102">parametresi değiştiricisi (C# Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="5ac23-102">in parameter modifier (C# Reference)</span></span>

<span data-ttu-id="5ac23-103">`in` Anahtar sözcüğü başvuruya göre geçirilecek bağımsız değişkenler neden olur.</span><span class="sxs-lookup"><span data-stu-id="5ac23-103">The `in` keyword causes arguments to be passed by reference.</span></span> <span data-ttu-id="5ac23-104">Benzer; [ref](ref.md) veya [çıkışı](out-parameter-modifier.md) anahtar sözcüklerini dışındaki `in` bağımsız değişkenleri ancak çağrılan yöntemi tarafından değiştirilemez `ref` bağımsız değişkenleri değiştirilmiş, `out` bağımsız değişkenleri çağıran tarafından değiştirilmesi gerekir ve bu değişiklik observable arama bağlamında.</span><span class="sxs-lookup"><span data-stu-id="5ac23-104">It is like the [ref](ref.md) or [out](out-parameter-modifier.md) keywords, except that `in` arguments cannot be modified by the called method, whereas `ref` arguments may be modified,  `out` arguments must be modified by the caller, and those modifications are observable in the calling context.</span></span>

[!code-csharp-interactive[cs-in-keyword](../../../../samples/snippets/csharp/language-reference/keywords/in-ref-out-modifier/InParameterModifier.cs#1)]  

<span data-ttu-id="5ac23-105">Önceki örnekte gösteren `in` değiştiricisi gereksiz çağrı sitede.</span><span class="sxs-lookup"><span data-stu-id="5ac23-105">The preceding example demonstrates that the `in` modifier is unnecessary at the call site.</span></span> <span data-ttu-id="5ac23-106">Yalnızca yöntemi bildiriminde de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5ac23-106">It is only required in the method declaration.</span></span>

> [!NOTE] 
> <span data-ttu-id="5ac23-107">`in` Anahtar sözcüğü de kullanılabilir bir genel tür parametresi tür parametresi, bir parçası olarak karşıtıdır olduğunu belirtmek için bir `foreach` deyimi, veya bir parçası olarak bir `join` yan tümcesinde bir LINQ Sorgu.</span><span class="sxs-lookup"><span data-stu-id="5ac23-107">The `in` keyword can also be used with a generic type parameter to specify that the type parameter is contravariant, as part of a `foreach` statement, or as part of a `join` clause in a LINQ query.</span></span> <span data-ttu-id="5ac23-108">Kullanımı hakkında daha fazla bilgi için `in` anahtar sözcüğü bu bağlamlarında bkz [içinde](in.md) Bu kullanımlar için bağlantılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ac23-108">For more information on the use of the `in` keyword in these contexts, see [in](in.md) which provides links to all those uses.</span></span>
  
 <span data-ttu-id="5ac23-109">Değişkenler geçildi olarak `in` bağımsız değişkenleri, bir yöntem çağrısı iletilmeden önce başlatılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5ac23-109">Variables passed as `in` arguments must be initialized before being passed in a method call.</span></span> <span data-ttu-id="5ac23-110">Ancak, çağrılan yöntemin düzgün bir değer atamak veya bağımsız değişkeni değiştirin.</span><span class="sxs-lookup"><span data-stu-id="5ac23-110">However, the called method may not assign a value or modify the argument.</span></span>  
  
 <span data-ttu-id="5ac23-111">Ancak `in`, `ref`, ve `out` anahtar sözcükleri neden farklı bir çalışma zamanı davranışı, derleme zamanında yöntem imzası parçası değerlendirilmez.</span><span class="sxs-lookup"><span data-stu-id="5ac23-111">Although the `in`, `ref`, and `out` keywords cause different run-time behavior, they are not considered part of the method signature at compile time.</span></span> <span data-ttu-id="5ac23-112">Bir yöntem aldığını tek fark ise, bu nedenle, yöntem aşırı yüklenemez bir `ref` veya `in` bağımsız değişkeni ve diğer alır bir `out` bağımsız değişkeni.</span><span class="sxs-lookup"><span data-stu-id="5ac23-112">Therefore, methods cannot be overloaded if the only difference is that one method takes a `ref` or `in` argument and the other takes an `out` argument.</span></span> <span data-ttu-id="5ac23-113">Aşağıdaki kod, örneğin, derlenmez:</span><span class="sxs-lookup"><span data-stu-id="5ac23-113">The following code, for example, will not compile:</span></span>  
  
```csharp
class CS0663_Example
{
    // Compiler error CS0663: "Cannot define overloaded 
    // methods that differ only on in, ref and out".
    public void SampleMethod(in int i) { }
    public void SampleMethod(ref int i) { }
}
```
  
<span data-ttu-id="5ac23-114">Aşırı yükleme varlığını temel `in` izin verilir, ancak derleyici uyarısı oluşturur:</span><span class="sxs-lookup"><span data-stu-id="5ac23-114">Overloading based on the presence of `in` is allowed, but generates a compiler warning:</span></span>  
  
```csharp
class InOverloads
{
    // Discouraged. Calling SampleMethod(value) is ambiguous.
    public void SampleMethod(in int i) { }
    public void SampleMethod(int i) { }
}
```

<span data-ttu-id="5ac23-115">Özellikleri veya sabitleri bayraklarıdır olarak `in` parametreleri, çünkü arama yöntemi değerlerine değişiklik yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="5ac23-115">Properties or constants may be passed as `in` parameters, because the calling method may not modify their values.</span></span>
  
<span data-ttu-id="5ac23-116">Kullanamazsınız `in`, `ref`, ve `out` yöntemleri şu tür için anahtar sözcükleri:</span><span class="sxs-lookup"><span data-stu-id="5ac23-116">You can't use the `in`, `ref`, and `out` keywords for the following kinds of methods:</span></span>  
  
- <span data-ttu-id="5ac23-117">Kullanarak tanımladığınız zaman uyumsuz yöntemleri [zaman uyumsuz](../../../csharp/language-reference/keywords/async.md) değiştiricisi.</span><span class="sxs-lookup"><span data-stu-id="5ac23-117">Async methods, which you define by using the [async](../../../csharp/language-reference/keywords/async.md) modifier.</span></span>  
  
- <span data-ttu-id="5ac23-118">Dahil yineleyici metotları bir [verim return](../../../csharp/language-reference/keywords/yield.md) veya `yield break` deyimi.</span><span class="sxs-lookup"><span data-stu-id="5ac23-118">Iterator methods, which include a [yield return](../../../csharp/language-reference/keywords/yield.md) or `yield break` statement.</span></span>  

<span data-ttu-id="5ac23-119">Genellikle bildirmelidir `in` bağımsız değişkenleri değere göre geçirme gerekli kopyalama işlemleri önlemek için bağımsız değişkenler.</span><span class="sxs-lookup"><span data-stu-id="5ac23-119">You typically declare `in` arguments to avoid the copy operations necessary for passing arguments by value.</span></span> <span data-ttu-id="5ac23-120">Bağımsız değişkenler yapıları veya yapıları dizileri olduğunda bu kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="5ac23-120">This is most useful when arguments are structures or arrays of structures.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="5ac23-121">C# Dil Belirtimi</span><span class="sxs-lookup"><span data-stu-id="5ac23-121">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="5ac23-122">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5ac23-122">See Also</span></span>  
 [<span data-ttu-id="5ac23-123">C# başvurusu</span><span class="sxs-lookup"><span data-stu-id="5ac23-123">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="5ac23-124">C# Programlama Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="5ac23-124">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="5ac23-125">C# Anahtar Sözcükleri</span><span class="sxs-lookup"><span data-stu-id="5ac23-125">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="5ac23-126">Yöntem Parametreleri</span><span class="sxs-lookup"><span data-stu-id="5ac23-126">Method Parameters</span></span>](../../../csharp/language-reference/keywords/method-parameters.md)
