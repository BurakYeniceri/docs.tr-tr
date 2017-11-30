---
title: "Fazla Yüklenebilir İşleçler (C# Programlama Kılavuzu)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- C# language, operator overloading
- operator overloading [C#]
ms.assetid: 390d9d01-79fc-40ab-9ed3-0bf448da1b6a
caps.latest.revision: "18"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 92dde781aa258267b7140228bc87621d26713f6d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="overloadable-operators-c-programming-guide"></a><span data-ttu-id="67ec2-102">Fazla Yüklenebilir İşleçler (C# Programlama Kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="67ec2-102">Overloadable Operators (C# Programming Guide)</span></span>

<span data-ttu-id="67ec2-103">C# işleçleri kullanarak statik üye işlevleri tanımlayarak aşırı yüklemeyi kullanıcı tanımlı türler verir [işleci](../../../csharp/language-reference/keywords/operator.md) anahtar sözcüğü.</span><span class="sxs-lookup"><span data-stu-id="67ec2-103">C# allows user-defined types to overload operators by defining static member functions using the [operator](../../../csharp/language-reference/keywords/operator.md) keyword.</span></span> <span data-ttu-id="67ec2-104">Tüm işleçleri, ancak aşırı yüklenebilir ve diğerlerinin bu tabloda listelendiği gibi kısıtlamaları olan:</span><span class="sxs-lookup"><span data-stu-id="67ec2-104">Not all operators can be overloaded, however, and others have restrictions, as listed in this table:</span></span>

| <span data-ttu-id="67ec2-105">İşleçler</span><span class="sxs-lookup"><span data-stu-id="67ec2-105">Operators</span></span> | <span data-ttu-id="67ec2-106">Overloadability</span><span class="sxs-lookup"><span data-stu-id="67ec2-106">Overloadability</span></span> |
| --------- | --------------- |
|<span data-ttu-id="67ec2-107">[+](../../../csharp/language-reference/operators/addition-operator.md), [-](../../../csharp/language-reference/operators/subtraction-operator.md), [!](../../../csharp/language-reference/operators/logical-negation-operator.md), [~](../../../csharp/language-reference/operators/bitwise-complement-operator.md), [++](../../../csharp/language-reference/operators/increment-operator.md), [--](../../../csharp/language-reference/operators/decrement-operator.md), [true](../../../csharp/language-reference/keywords/true.md), [false](../../../csharp/language-reference/keywords/false.md)</span><span class="sxs-lookup"><span data-stu-id="67ec2-107">[+](../../../csharp/language-reference/operators/addition-operator.md), [-](../../../csharp/language-reference/operators/subtraction-operator.md), [!](../../../csharp/language-reference/operators/logical-negation-operator.md), [~](../../../csharp/language-reference/operators/bitwise-complement-operator.md), [++](../../../csharp/language-reference/operators/increment-operator.md), [--](../../../csharp/language-reference/operators/decrement-operator.md), [true](../../../csharp/language-reference/keywords/true.md), [false](../../../csharp/language-reference/keywords/false.md)</span></span>|<span data-ttu-id="67ec2-108">Bu birli işleçleri aşırı yüklenmiş.</span><span class="sxs-lookup"><span data-stu-id="67ec2-108">These unary operators can be overloaded.</span></span>|
|<span data-ttu-id="67ec2-109">[+](../../../csharp/language-reference/operators/addition-operator.md), [-](../../../csharp/language-reference/operators/subtraction-operator.md), [\*](../../../csharp/language-reference/operators/multiplication-operator.md), [/](../../../csharp/language-reference/operators/division-operator.md), [%](../../../csharp/language-reference/operators/modulus-operator.md), [&](../../../csharp/language-reference/operators/and-operator.md), [&#124;](../../../csharp/language-reference/operators/or-operator.md), [^](../../../csharp/language-reference/operators/xor-operator.md), [\<\<](../../../csharp/language-reference/operators/left-shift-operator.md), [>>](../../../csharp/language-reference/operators/right-shift-operator.md)</span><span class="sxs-lookup"><span data-stu-id="67ec2-109">[+](../../../csharp/language-reference/operators/addition-operator.md), [-](../../../csharp/language-reference/operators/subtraction-operator.md), [\*](../../../csharp/language-reference/operators/multiplication-operator.md), [/](../../../csharp/language-reference/operators/division-operator.md), [%](../../../csharp/language-reference/operators/modulus-operator.md), [&](../../../csharp/language-reference/operators/and-operator.md), [&#124;](../../../csharp/language-reference/operators/or-operator.md), [^](../../../csharp/language-reference/operators/xor-operator.md), [\<\<](../../../csharp/language-reference/operators/left-shift-operator.md), [>>](../../../csharp/language-reference/operators/right-shift-operator.md)</span></span>|<span data-ttu-id="67ec2-110">Bu ikili işleçler aşırı yüklenmiş.</span><span class="sxs-lookup"><span data-stu-id="67ec2-110">These binary operators can be overloaded.</span></span>|
|<span data-ttu-id="67ec2-111">[==](../../../csharp/language-reference/operators/equality-comparison-operator.md), [!=](../../../csharp/language-reference/operators/not-equal-operator.md), [\<](../../../csharp/language-reference/operators/less-than-operator.md), [>](../../../csharp/language-reference/operators/greater-than-operator.md), [\<=](../../../csharp/language-reference/operators/less-than-equal-operator.md), [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md)</span><span class="sxs-lookup"><span data-stu-id="67ec2-111">[==](../../../csharp/language-reference/operators/equality-comparison-operator.md), [!=](../../../csharp/language-reference/operators/not-equal-operator.md), [\<](../../../csharp/language-reference/operators/less-than-operator.md), [>](../../../csharp/language-reference/operators/greater-than-operator.md), [\<=](../../../csharp/language-reference/operators/less-than-equal-operator.md), [>=](../../../csharp/language-reference/operators/greater-than-equal-operator.md)</span></span>|<span data-ttu-id="67ec2-112">Karşılaştırma işleçleri aşırı yüklenebilir (ancak bu tablonun altındaki nota bakın).</span><span class="sxs-lookup"><span data-stu-id="67ec2-112">The comparison operators can be overloaded (but see the note that follows this table).</span></span>|
|<span data-ttu-id="67ec2-113">[&&](../../../csharp/language-reference/operators/conditional-and-operator.md), [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md)</span><span class="sxs-lookup"><span data-stu-id="67ec2-113">[&&](../../../csharp/language-reference/operators/conditional-and-operator.md), [&#124;&#124;](../../../csharp/language-reference/operators/conditional-or-operator.md)</span></span>|<span data-ttu-id="67ec2-114">Koşullu mantıksal işleçleri aşırı yüklenemez, ancak kullanılarak değerlendirilir `&` ve <code>&#124;</code>, hangi aşırı yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="67ec2-114">The conditional logical operators cannot be overloaded, but they are evaluated using `&` and <code>&#124;</code>, which can be overloaded.</span></span>|
|[<span data-ttu-id="67ec2-115">&#91;&#93;</span><span class="sxs-lookup"><span data-stu-id="67ec2-115">&#91;&#93;</span></span>](../../../csharp/language-reference/operators/index-operator.md)|<span data-ttu-id="67ec2-116">Dizinin dizin oluşturma işleci aşırı yüklenemez, ancak dizin oluşturucular tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67ec2-116">The array indexing operator cannot be overloaded, but you can define indexers.</span></span>|
|[<span data-ttu-id="67ec2-117">(T) x</span><span class="sxs-lookup"><span data-stu-id="67ec2-117">(T)x</span></span>](../../../csharp/language-reference/operators/invocation-operator.md)|<span data-ttu-id="67ec2-118">Atama işleci aşırı yüklenemez, ancak yeni dönüşüm işleçleri tanımlayabilirsiniz (bkz [açık](../../../csharp/language-reference/keywords/explicit.md) ve [örtük](../../../csharp/language-reference/keywords/implicit.md)).</span><span class="sxs-lookup"><span data-stu-id="67ec2-118">The cast operator cannot be overloaded, but you can define new conversion operators (see [explicit](../../../csharp/language-reference/keywords/explicit.md) and [implicit](../../../csharp/language-reference/keywords/implicit.md)).</span></span>|
|<span data-ttu-id="67ec2-119">[+=](../../../csharp/language-reference/operators/addition-assignment-operator.md), [-=](../../../csharp/language-reference/operators/subtraction-assignment-operator.md), [\*=](../../../csharp/language-reference/operators/multiplication-assignment-operator.md), [/=](../../../csharp/language-reference/operators/division-assignment-operator.md), [%=](../../../csharp/language-reference/operators/modulus-assignment-operator.md), [&=](../../../csharp/language-reference/operators/and-assignment-operator.md), [&#124;=](../../../csharp/language-reference/operators/or-assignment-operator.md), [^=](../../../csharp/language-reference/operators/xor-assignment-operator.md), [\<\<=](../../../csharp/language-reference/operators/left-shift-assignment-operator.md), [>>=](../../../csharp/language-reference/operators/right-shift-assignment-operator.md)</span><span class="sxs-lookup"><span data-stu-id="67ec2-119">[+=](../../../csharp/language-reference/operators/addition-assignment-operator.md), [-=](../../../csharp/language-reference/operators/subtraction-assignment-operator.md), [\*=](../../../csharp/language-reference/operators/multiplication-assignment-operator.md), [/=](../../../csharp/language-reference/operators/division-assignment-operator.md), [%=](../../../csharp/language-reference/operators/modulus-assignment-operator.md), [&=](../../../csharp/language-reference/operators/and-assignment-operator.md), [&#124;=](../../../csharp/language-reference/operators/or-assignment-operator.md), [^=](../../../csharp/language-reference/operators/xor-assignment-operator.md), [\<\<=](../../../csharp/language-reference/operators/left-shift-assignment-operator.md), [>>=](../../../csharp/language-reference/operators/right-shift-assignment-operator.md)</span></span>|<span data-ttu-id="67ec2-120">Atama İşleçleri aşırı olamaz, ancak `+=`, örneğin, kullanılarak hesaplandı `+`, hangi aşırı yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="67ec2-120">Assignment operators cannot be overloaded, but `+=`, for example, is evaluated using `+`, which can be overloaded.</span></span>|
|<span data-ttu-id="67ec2-121">[=](../../../csharp/language-reference/operators/assignment-operator.md), [. ](../../../csharp/language-reference/operators/member-access-operator.md), [?:](../../../csharp/language-reference/operators/conditional-operator.md), [?? ](../../../csharp/language-reference/operators/null-conditional-operator.md), [ -> ](../../../csharp/language-reference/operators/dereference-operator.md), [ => ](../../../csharp/language-reference/operators/lambda-operator.md), [f(x)](../../../csharp/language-reference/operators/invocation-operator.md), [olarak](../../../csharp/language-reference/keywords/as.md), [işaretli ](../../../csharp/language-reference/keywords/checked.md), [denetlenmeyen](../../../csharp/language-reference/keywords/unchecked.md), [varsayılan](../../../csharp/programming-guide/statements-expressions-operators/default-value-expressions.md), [temsilci](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md), [olan](../../../csharp/language-reference/keywords/is.md), [yeni](../../../csharp/language-reference/keywords/new.md), [sizeof](../../../csharp/language-reference/keywords/sizeof.md), [typeof](../../../csharp/language-reference/keywords/typeof.md)</span><span class="sxs-lookup"><span data-stu-id="67ec2-121">[=](../../../csharp/language-reference/operators/assignment-operator.md), [.](../../../csharp/language-reference/operators/member-access-operator.md), [?:](../../../csharp/language-reference/operators/conditional-operator.md), [??](../../../csharp/language-reference/operators/null-conditional-operator.md), [->](../../../csharp/language-reference/operators/dereference-operator.md), [=>](../../../csharp/language-reference/operators/lambda-operator.md), [f(x)](../../../csharp/language-reference/operators/invocation-operator.md), [as](../../../csharp/language-reference/keywords/as.md), [checked](../../../csharp/language-reference/keywords/checked.md), [unchecked](../../../csharp/language-reference/keywords/unchecked.md), [default](../../../csharp/programming-guide/statements-expressions-operators/default-value-expressions.md), [delegate](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md), [is](../../../csharp/language-reference/keywords/is.md), [new](../../../csharp/language-reference/keywords/new.md), [sizeof](../../../csharp/language-reference/keywords/sizeof.md), [typeof](../../../csharp/language-reference/keywords/typeof.md)</span></span>|<span data-ttu-id="67ec2-122">Bu işleçleri aşırı yüklenemez.</span><span class="sxs-lookup"><span data-stu-id="67ec2-122">These operators cannot be overloaded.</span></span>|

> [!NOTE]
> <span data-ttu-id="67ec2-123">Karşılaştırma işleçleri aşırı yüklü olmadığını çiftler halinde aşırı yüklenmiş gerekir; diğer bir deyişle, `==` aşırı yüklendi `!=` da aşırı yüklenmiş gerekir.</span><span class="sxs-lookup"><span data-stu-id="67ec2-123">The comparison operators, if overloaded, must be overloaded in pairs; that is, if `==` is overloaded, `!=` must also be overloaded.</span></span> <span data-ttu-id="67ec2-124">Tersi de aşırı burada doğrudur `!=` için bir aşırı gerektirir `==`.</span><span class="sxs-lookup"><span data-stu-id="67ec2-124">The reverse is also true, where overloading `!=` requires an overload for `==`.</span></span> <span data-ttu-id="67ec2-125">Karşılaştırma işleçleri için aynı geçerlidir `<` ve `>` ve `<=` ve `>=`.</span><span class="sxs-lookup"><span data-stu-id="67ec2-125">The same is true for comparison operators `<` and `>` and for `<=` and `>=`.</span></span>

<span data-ttu-id="67ec2-126">Özel bir sınıf üzerinde bir işleç aşırı yüklemesi için doğru imzalı sınıfında bir yöntem oluşturma gerektirir.</span><span class="sxs-lookup"><span data-stu-id="67ec2-126">To overload an operator on a custom class requires creating a method on the class with the correct signature.</span></span> <span data-ttu-id="67ec2-127">Yöntem "işleci X adı veya sembol aşırı yüklenmesini işlecinin burada X" olarak adlandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="67ec2-127">The method must be named "operator X" where X is the name or symbol of the operator being overloaded.</span></span> <span data-ttu-id="67ec2-128">Birli işleçleri bir parametre içermeli ve ikili işleçler iki parametreye sahiptir.</span><span class="sxs-lookup"><span data-stu-id="67ec2-128">Unary operators have one parameter, and binary operators have two parameters.</span></span> <span data-ttu-id="67ec2-129">Her durumda, bir parametre sınıf ya da işleç bildirir yapı aynı türde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="67ec2-129">In each case, one parameter must be the same type as the class or struct that declares the operator.</span></span>

```csharp
public static Complex operator +(Complex c1, Complex c2)
{
    return new Complex(c1.real + c2.real, c1.imaginary + c2.imaginary);
}
```

<span data-ttu-id="67ec2-130">Yalnızca bir ifade sonuçla hemen geri tanımları yaygındır.</span><span class="sxs-lookup"><span data-stu-id="67ec2-130">It is common to have definitions that simply return immediately with the result of an expression.</span></span>  <span data-ttu-id="67ec2-131">Kısayoludur bir sözdizimi kullanılarak `=>` bu durumlar için.</span><span class="sxs-lookup"><span data-stu-id="67ec2-131">There is a syntax shortcut using `=>` for these situations.</span></span>

```csharp
public static Complex operator +(Complex c1, Complex c2) =>
        new Complex(c1.real + c2.real, c1.imaginary + c2.imaginary);
  
// Override ToString() to display a complex number in the traditional format:
public override string ToString() => $"{this.real} + {this.imaginary}";
```

<span data-ttu-id="67ec2-132">Daha fazla bilgi için bkz: [nasıl yapılır: karmaşık sayı sınıfı oluşturmak için kullanım İşleç aşırı yüklemesi](../../../csharp/programming-guide/statements-expressions-operators/how-to-use-operator-overloading-to-create-a-complex-number-class.md).</span><span class="sxs-lookup"><span data-stu-id="67ec2-132">For more information, see [How to: Use Operator Overloading to Create a Complex Number Class](../../../csharp/programming-guide/statements-expressions-operators/how-to-use-operator-overloading-to-create-a-complex-number-class.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="67ec2-133">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="67ec2-133">See also</span></span>

[<span data-ttu-id="67ec2-134">C# programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="67ec2-134">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
[<span data-ttu-id="67ec2-135">Deyimler, ifadeler ve işleçler</span><span class="sxs-lookup"><span data-stu-id="67ec2-135">Statements, Expressions, and Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/index.md)  
[<span data-ttu-id="67ec2-136">İşleçler</span><span class="sxs-lookup"><span data-stu-id="67ec2-136">Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/operators.md)  
[<span data-ttu-id="67ec2-137">C# işleçleri</span><span class="sxs-lookup"><span data-stu-id="67ec2-137">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
[<span data-ttu-id="67ec2-138">Neden aşırı yüklenmiş işleçler her zaman C# ' ta statik misiniz?</span><span class="sxs-lookup"><span data-stu-id="67ec2-138">Why are overloaded operators always static in C#?</span></span>](http://go.microsoft.com/fwlink/?LinkId=112383)