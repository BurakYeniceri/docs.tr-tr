---
title: "class (C# Başvurusu)"
ms.date: 07/18/2017
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords:
- class_CSharpKeyword
- class
helpviewer_keywords: class keyword [C#]
ms.assetid: b95d8815-de18-4c3f-a8cc-a0a53bdf8690
caps.latest.revision: "30"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: ae4b019ee88b6f331a76c750ab94fc76a3343adb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="class-c-reference"></a><span data-ttu-id="87bd0-102">class (C# Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="87bd0-102">class (C# Reference)</span></span>

<span data-ttu-id="87bd0-103">Sınıfları, anahtar sözcüğünü kullanarak bildirildiğinde `class`, aşağıdaki örnekte gösterildiği gibi:</span><span class="sxs-lookup"><span data-stu-id="87bd0-103">Classes are declared using the keyword `class`, as shown in the following example:</span></span>

```csharp
class TestClass
{
    // Methods, properties, fields, events, delegates 
    // and nested classes go here.
}
```

## <a name="remarks"></a><span data-ttu-id="87bd0-104">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="87bd0-104">Remarks</span></span>
<span data-ttu-id="87bd0-105">C# içinde yalnızca tek devralma izin verilir.</span><span class="sxs-lookup"><span data-stu-id="87bd0-105">Only single inheritance is allowed in C#.</span></span> <span data-ttu-id="87bd0-106">Diğer bir deyişle, bir sınıf bir taban sınıftan yalnızca uygulama devralabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87bd0-106">In other words, a class can inherit implementation from one base class only.</span></span> <span data-ttu-id="87bd0-107">Ancak, bir sınıfın birden fazla arabirimi uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87bd0-107">However, a class can implement more than one interface.</span></span> <span data-ttu-id="87bd0-108">Aşağıdaki tabloda sınıf devralma ve arabirim uygulamasına örnekleri gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="87bd0-108">The following table shows examples of class inheritance and interface implementation:</span></span>

|<span data-ttu-id="87bd0-109">Devralma</span><span class="sxs-lookup"><span data-stu-id="87bd0-109">Inheritance</span></span>|<span data-ttu-id="87bd0-110">Örnek</span><span class="sxs-lookup"><span data-stu-id="87bd0-110">Example</span></span>|
|-----------------|-------------|
|<span data-ttu-id="87bd0-111">Yok.</span><span class="sxs-lookup"><span data-stu-id="87bd0-111">None</span></span>|`class ClassA { }`|
|<span data-ttu-id="87bd0-112">Tek</span><span class="sxs-lookup"><span data-stu-id="87bd0-112">Single</span></span>|`class DerivedClass: BaseClass { }`|
|<span data-ttu-id="87bd0-113">None, iki arabirimlerini uygular</span><span class="sxs-lookup"><span data-stu-id="87bd0-113">None, implements two interfaces</span></span>|`class ImplClass: IFace1, IFace2 { }`|
|<span data-ttu-id="87bd0-114">Tek bir arabirim uygular</span><span class="sxs-lookup"><span data-stu-id="87bd0-114">Single, implements one interface</span></span>|`class ImplDerivedClass: BaseClass, IFace1 { }`|

<span data-ttu-id="87bd0-115">Diğer sınıflar içinde iç içe değil doğrudan bir ad alanındaki bildirme sınıfları olabilir ya da [ortak](../../../csharp/language-reference/keywords/public.md) veya [iç](../../../csharp/language-reference/keywords/internal.md).</span><span class="sxs-lookup"><span data-stu-id="87bd0-115">Classes that you declare directly within a namespace, not nested within other classes, can be either [public](../../../csharp/language-reference/keywords/public.md) or [internal](../../../csharp/language-reference/keywords/internal.md).</span></span> <span data-ttu-id="87bd0-116">Sınıflardır `internal` varsayılan olarak.</span><span class="sxs-lookup"><span data-stu-id="87bd0-116">Classes are `internal` by default.</span></span>

<span data-ttu-id="87bd0-117">Sınıf üyeleri, iç içe geçmiş sınıflar dahil olabilir [ortak](../../../csharp/language-reference/keywords/public.md), `protected internal`, [korumalı](../../../csharp/language-reference/keywords/protected.md), [iç](../../../csharp/language-reference/keywords/internal.md), [özel](../../../csharp/language-reference/keywords/private.md), veya `private protected`.</span><span class="sxs-lookup"><span data-stu-id="87bd0-117">Class members, including nested classes, can be [public](../../../csharp/language-reference/keywords/public.md), `protected internal`, [protected](../../../csharp/language-reference/keywords/protected.md), [internal](../../../csharp/language-reference/keywords/internal.md), [private](../../../csharp/language-reference/keywords/private.md), or `private protected`.</span></span> <span data-ttu-id="87bd0-118">Üye olan [özel](../../../csharp/language-reference/keywords/private.md) varsayılan olarak.</span><span class="sxs-lookup"><span data-stu-id="87bd0-118">Members are [private](../../../csharp/language-reference/keywords/private.md) by default.</span></span>

<span data-ttu-id="87bd0-119">Daha fazla bilgi için bkz: [erişim değiştiricileri](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span><span class="sxs-lookup"><span data-stu-id="87bd0-119">For more information, see [Access Modifiers](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md).</span></span>

<span data-ttu-id="87bd0-120">Tür parametreleri olan genel sınıfları bildirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87bd0-120">You can declare generic classes that have type parameters.</span></span> <span data-ttu-id="87bd0-121">Daha fazla bilgi için bkz: [Genel sınıflar](../../../csharp/programming-guide/generics/generic-classes.md).</span><span class="sxs-lookup"><span data-stu-id="87bd0-121">For more information, see [Generic Classes](../../../csharp/programming-guide/generics/generic-classes.md).</span></span>

<span data-ttu-id="87bd0-122">Bir sınıf bildirimleri aşağıdaki üyeleri içerebilir:</span><span class="sxs-lookup"><span data-stu-id="87bd0-122">A class can contain declarations of the following members:</span></span>

- [<span data-ttu-id="87bd0-123">Oluşturucular</span><span class="sxs-lookup"><span data-stu-id="87bd0-123">Constructors</span></span>](../../../csharp/programming-guide/classes-and-structs/constructors.md)

- [<span data-ttu-id="87bd0-124">Sabitleri</span><span class="sxs-lookup"><span data-stu-id="87bd0-124">Constants</span></span>](../../../csharp/programming-guide/classes-and-structs/constants.md)

- [<span data-ttu-id="87bd0-125">Alanları</span><span class="sxs-lookup"><span data-stu-id="87bd0-125">Fields</span></span>](../../../csharp/programming-guide/classes-and-structs/fields.md)

- [<span data-ttu-id="87bd0-126">Sonlandırıcılar</span><span class="sxs-lookup"><span data-stu-id="87bd0-126">Finalizers</span></span>](../../../csharp/programming-guide/classes-and-structs/destructors.md)

- [<span data-ttu-id="87bd0-127">Yöntemleri</span><span class="sxs-lookup"><span data-stu-id="87bd0-127">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)

- [<span data-ttu-id="87bd0-128">Özellikleri</span><span class="sxs-lookup"><span data-stu-id="87bd0-128">Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/properties.md)

- [<span data-ttu-id="87bd0-129">Dizin oluşturucular</span><span class="sxs-lookup"><span data-stu-id="87bd0-129">Indexers</span></span>](../../../csharp/programming-guide/indexers/index.md)

- [<span data-ttu-id="87bd0-130">İşleçler</span><span class="sxs-lookup"><span data-stu-id="87bd0-130">Operators</span></span>](../../../csharp/programming-guide/statements-expressions-operators/operators.md)

- [<span data-ttu-id="87bd0-131">Olayları</span><span class="sxs-lookup"><span data-stu-id="87bd0-131">Events</span></span>](../../../csharp/programming-guide/events/index.md)

- [<span data-ttu-id="87bd0-132">Temsilciler</span><span class="sxs-lookup"><span data-stu-id="87bd0-132">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)

- [<span data-ttu-id="87bd0-133">Sınıfları</span><span class="sxs-lookup"><span data-stu-id="87bd0-133">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)

- [<span data-ttu-id="87bd0-134">Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="87bd0-134">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)

- [<span data-ttu-id="87bd0-135">Yapılar</span><span class="sxs-lookup"><span data-stu-id="87bd0-135">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)

## <a name="example"></a><span data-ttu-id="87bd0-136">Örnek</span><span class="sxs-lookup"><span data-stu-id="87bd0-136">Example</span></span>
<span data-ttu-id="87bd0-137">Aşağıdaki örnek bildiren sınıfı alanları, Oluşturucular ve yöntemleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="87bd0-137">The following example demonstrates declaring class fields, constructors, and methods.</span></span> <span data-ttu-id="87bd0-138">Ayrıca nesne örnek oluşturma ve yazdırma örnek verilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="87bd0-138">It also demonstrates object instantiation and printing instance data.</span></span> <span data-ttu-id="87bd0-139">Bu örnekte, iki sınıf bildirilir.</span><span class="sxs-lookup"><span data-stu-id="87bd0-139">In this example, two classes are declared.</span></span> <span data-ttu-id="87bd0-140">İlk sınıf `Child`, iki özel alan içeriyor (`name` ve `age`), iki ortak oluşturucular ve bir genel yöntem.</span><span class="sxs-lookup"><span data-stu-id="87bd0-140">The first class, `Child`, contains two private fields (`name` and `age`), two public constructors and one public method.</span></span> <span data-ttu-id="87bd0-141">İkinci sınıfı `StringTest`, kapsamak için kullanılmış `Main`.</span><span class="sxs-lookup"><span data-stu-id="87bd0-141">The second class, `StringTest`, is used to contain `Main`.</span></span>

[!code-csharp[csrefKeywordsTypes#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/class_1.cs)]

## <a name="comments"></a><span data-ttu-id="87bd0-142">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="87bd0-142">Comments</span></span>
<span data-ttu-id="87bd0-143">Önceki örnekte dikkat özel alanlar (`name` ve `age`) yalnızca genel yöntemi aracılığıyla erişilebilir `Child` sınıfı.</span><span class="sxs-lookup"><span data-stu-id="87bd0-143">Notice that in the previous example the private fields (`name` and `age`) can only be accessed through the public method of the `Child` class.</span></span> <span data-ttu-id="87bd0-144">Örneğin, çocuğunuzun adı, yazdırma olamaz `Main` yöntemi, böyle bir deyimi kullanarak:</span><span class="sxs-lookup"><span data-stu-id="87bd0-144">For example, you cannot print the child's name, from the `Main` method, using a statement like this:</span></span>

```csharp
Console.Write(child1.name);   // Error
```

<span data-ttu-id="87bd0-145">Özel üyelerine erişme `Child` gelen `Main` yalnızca sağlayabileceğinizden varsa `Main` sınıf üyesi olan.</span><span class="sxs-lookup"><span data-stu-id="87bd0-145">Accessing private members of `Child` from `Main` would only be possible if `Main` were a member of the class.</span></span>

<span data-ttu-id="87bd0-146">Türleri bildirilen bir erişim değiştiricisi varsayılan olmayan bir sınıf içinde `private`, bu örnekte veri üyeleri durumda olacaktır `private` anahtar sözcüğü kaldırılmışsa.</span><span class="sxs-lookup"><span data-stu-id="87bd0-146">Types declared inside a class without an access modifier default to `private`, so the data members in this example would still be `private` if the keyword were removed.</span></span>

<span data-ttu-id="87bd0-147">Son olarak, varsayılan oluşturucu kullanılarak oluşturulan nesne için dikkat edin (`child3`), alan başlatılır yaş varsayılan olarak sıfır.</span><span class="sxs-lookup"><span data-stu-id="87bd0-147">Finally, notice that for the object created using the default constructor (`child3`), the age field was initialized to zero by default.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="87bd0-148">C# Dil Belirtimi</span><span class="sxs-lookup"><span data-stu-id="87bd0-148">C# Language Specification</span></span>
[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]

## <a name="see-also"></a><span data-ttu-id="87bd0-149">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="87bd0-149">See Also</span></span>
 [<span data-ttu-id="87bd0-150">C# başvurusu</span><span class="sxs-lookup"><span data-stu-id="87bd0-150">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="87bd0-151">C# programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="87bd0-151">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="87bd0-152">C# anahtar sözcükleri</span><span class="sxs-lookup"><span data-stu-id="87bd0-152">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="87bd0-153">Başvuru türleri</span><span class="sxs-lookup"><span data-stu-id="87bd0-153">Reference Types</span></span>](../../../csharp/language-reference/keywords/reference-types.md)