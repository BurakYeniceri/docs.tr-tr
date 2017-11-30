---
title: "Soyut ve Korumalı Sınıflar ve Sınıf Üyeleri (C# Programlama Kılavuzu)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- abstract classes [C#]
- sealed classes [C#]
- C# language, abstract classes
- C# language, sealed
ms.assetid: 99aa52f7-b435-43f9-936e-2470af734c4e
caps.latest.revision: "14"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: dac7570c018bd577faac4540e4d800cc11143578
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="abstract-and-sealed-classes-and-class-members-c-programming-guide"></a><span data-ttu-id="4eab6-102">Soyut ve Korumalı Sınıflar ve Sınıf Üyeleri (C# Programlama Kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="4eab6-102">Abstract and Sealed Classes and Class Members (C# Programming Guide)</span></span>
<span data-ttu-id="4eab6-103">[Soyut](../../../csharp/language-reference/keywords/abstract.md) anahtar sözcüğü sınıfları oluşturmanıza olanak sağlar ve [sınıfı](../../../csharp/language-reference/keywords/class.md) tamamlanmamış ve türetilen bir sınıfta uygulanmalı üyeleri.</span><span class="sxs-lookup"><span data-stu-id="4eab6-103">The [abstract](../../../csharp/language-reference/keywords/abstract.md) keyword enables you to create classes and [class](../../../csharp/language-reference/keywords/class.md) members that are incomplete and must be implemented in a derived class.</span></span>  
  
 <span data-ttu-id="4eab6-104">[Korumalı](../../../csharp/language-reference/keywords/sealed.md) anahtar sözcüğü bir sınıf ya da daha önce işaretlenen belirli sınıfı üyeleri devralma önlemek etkinleştirir [sanal](../../../csharp/language-reference/keywords/virtual.md).</span><span class="sxs-lookup"><span data-stu-id="4eab6-104">The [sealed](../../../csharp/language-reference/keywords/sealed.md) keyword enables you to prevent the inheritance of a class or certain class members that were previously marked [virtual](../../../csharp/language-reference/keywords/virtual.md).</span></span>  
  
## <a name="abstract-classes-and-class-members"></a><span data-ttu-id="4eab6-105">Soyut sınıflar ve sınıf üyeleri</span><span class="sxs-lookup"><span data-stu-id="4eab6-105">Abstract Classes and Class Members</span></span>  
 <span data-ttu-id="4eab6-106">Sınıfları bildirilebilir soyut olarak anahtar sözcüğü koyarak `abstract` sınıf tanımını önce.</span><span class="sxs-lookup"><span data-stu-id="4eab6-106">Classes can be declared as abstract by putting the keyword `abstract` before the class definition.</span></span> <span data-ttu-id="4eab6-107">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4eab6-107">For example:</span></span>  
  
 [!code-csharp[csProgGuideInheritance#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/abstract-and-sealed-classes-and-class-members_1.cs)]  
  
 <span data-ttu-id="4eab6-108">Bir Özet sınıfın örneği oluşturulamıyor.</span><span class="sxs-lookup"><span data-stu-id="4eab6-108">An abstract class cannot be instantiated.</span></span> <span data-ttu-id="4eab6-109">Bir Özet sınıf amacı bir taban sınıfın birden çok türetilen sınıflar paylaşabilirsiniz ortak bir tanımı sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="4eab6-109">The purpose of an abstract class is to provide a common definition of a base class that multiple derived classes can share.</span></span> <span data-ttu-id="4eab6-110">Örneğin, bir sınıf kitaplığı birçok işlevlerini parametre olarak kullanılan soyut bir sınıf tanımlama ve türetilmiş bir sınıf oluşturarak, kendi uygulama sınıfının sağlamak için bu kitaplığı kullanarak programcıları gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4eab6-110">For example, a class library may define an abstract class that is used as a parameter to many of its functions, and require programmers using that library to provide their own implementation of the class by creating a derived class.</span></span>  
  
 <span data-ttu-id="4eab6-111">Soyut sınıfların soyut yöntemler de tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="4eab6-111">Abstract classes may also define abstract methods.</span></span> <span data-ttu-id="4eab6-112">Bu anahtar sözcüğü ekleyerek gerçekleştirilir `abstract` önce yönteminin dönüş türü.</span><span class="sxs-lookup"><span data-stu-id="4eab6-112">This is accomplished by adding the keyword `abstract` before the return type of the method.</span></span> <span data-ttu-id="4eab6-113">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4eab6-113">For example:</span></span>  
  
 [!code-csharp[csProgGuideInheritance#14](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/abstract-and-sealed-classes-and-class-members_2.cs)]  
  
 <span data-ttu-id="4eab6-114">Soyut yöntemler hiçbir uygulama sahip, bu nedenle yöntem tanımı normal yöntem bloğu yerine noktalı izlenir.</span><span class="sxs-lookup"><span data-stu-id="4eab6-114">Abstract methods have no implementation, so the method definition is followed by a semicolon instead of a normal method block.</span></span> <span data-ttu-id="4eab6-115">Soyut sınıftan türetilen sınıflar tüm soyut yöntemler uygulamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4eab6-115">Derived classes of the abstract class must implement all abstract methods.</span></span> <span data-ttu-id="4eab6-116">Soyut bir sınıf sanal bir yöntem bir taban sınıftan, soyut sınıf ile soyut bir yöntem sanal yöntemi geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-116">When an abstract class inherits a virtual method from a base class, the abstract class can override the virtual method with an abstract method.</span></span> <span data-ttu-id="4eab6-117">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4eab6-117">For example:</span></span>  
  
 [!code-csharp[csProgGuideInheritance#15](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/abstract-and-sealed-classes-and-class-members_3.cs)]  
  
 <span data-ttu-id="4eab6-118">Varsa bir `virtual` yöntemi bildirilen `abstract`, soyut sınıfından devralan herhangi bir sınıf için hala sanal.</span><span class="sxs-lookup"><span data-stu-id="4eab6-118">If a `virtual` method is declared `abstract`, it is still virtual to any class inheriting from the abstract class.</span></span> <span data-ttu-id="4eab6-119">Soyut bir yöntem devralan bir sınıf yöntemi'nın özgün uygulaması erişemiyor — önceki örnekte, `DoWork` F çağıramaz sınıfındaki `DoWork` sınıfı D. üzerinde Bu şekilde, bir Özet sınıf sanal yöntemler için yeni yöntemi uygulamaları sağlamak için türetilen sınıflar zorlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-119">A class inheriting an abstract method cannot access the original implementation of the method—in the previous example, `DoWork` on class F cannot call `DoWork` on class D. In this way, an abstract class can force derived classes to provide new method implementations for virtual methods.</span></span>  
  
## <a name="sealed-classes-and-class-members"></a><span data-ttu-id="4eab6-120">Korumalı sınıflar ve sınıf üyeleri</span><span class="sxs-lookup"><span data-stu-id="4eab6-120">Sealed Classes and Class Members</span></span>  
 <span data-ttu-id="4eab6-121">Sınıflar olarak bildirilebilir [korumalı](../../../csharp/language-reference/keywords/sealed.md) anahtar sözcüğü koyarak `sealed` sınıf tanımını önce.</span><span class="sxs-lookup"><span data-stu-id="4eab6-121">Classes can be declared as [sealed](../../../csharp/language-reference/keywords/sealed.md) by putting the keyword `sealed` before the class definition.</span></span> <span data-ttu-id="4eab6-122">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4eab6-122">For example:</span></span>  
  
 [!code-csharp[csProgGuideInheritance#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/abstract-and-sealed-classes-and-class-members_4.cs)]  
  
 <span data-ttu-id="4eab6-123">Korumalı bir sınıfın temel sınıf olarak kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-123">A sealed class cannot be used as a base class.</span></span> <span data-ttu-id="4eab6-124">Bu nedenle, bu da bir Özet sınıf olamaz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-124">For this reason, it cannot also be an abstract class.</span></span> <span data-ttu-id="4eab6-125">Sealed sınıfları türetme engeller.</span><span class="sxs-lookup"><span data-stu-id="4eab6-125">Sealed classes prevent derivation.</span></span> <span data-ttu-id="4eab6-126">Bir temel sınıf olarak hiçbir zaman kullanılabilir olduğundan, bazı çalışma zamanı iyileştirmeleri biraz daha hızlı arama korumalı sınıf üyeleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-126">Because they can never be used as a base class, some run-time optimizations can make calling sealed class members slightly faster.</span></span>  
  
 <span data-ttu-id="4eab6-127">Yöntemi, dizin oluşturucu, özelliği veya olayda sanal temel sınıf üyesi geçersiz kılma türetilmiş bir sınıf, üye korumalı olarak bildirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-127">A method, indexer, property, or event, on a derived class that is overriding a virtual member of the base class can declare that member as sealed.</span></span> <span data-ttu-id="4eab6-128">Bu üye için daha fazla türetilmiş bir sınıf sanal yönünü üzerindeki geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="4eab6-128">This negates the virtual aspect of the member for any further derived class.</span></span> <span data-ttu-id="4eab6-129">Bu koyarak gerçekleştirilir `sealed` önce anahtar sözcüğü [geçersiz kılma](../../../csharp/language-reference/keywords/override.md) sınıf üyesi bildirim anahtar sözcük.</span><span class="sxs-lookup"><span data-stu-id="4eab6-129">This is accomplished by putting the `sealed` keyword before the [override](../../../csharp/language-reference/keywords/override.md) keyword in the class member declaration.</span></span> <span data-ttu-id="4eab6-130">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4eab6-130">For example:</span></span>  
  
 [!code-csharp[csProgGuideInheritance#17](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/abstract-and-sealed-classes-and-class-members_5.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="4eab6-131">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4eab6-131">See Also</span></span>  
 [<span data-ttu-id="4eab6-132">C# programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="4eab6-132">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="4eab6-133">Sınıflar ve yapılar</span><span class="sxs-lookup"><span data-stu-id="4eab6-133">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)  
 [<span data-ttu-id="4eab6-134">Devralma</span><span class="sxs-lookup"><span data-stu-id="4eab6-134">Inheritance</span></span>](../../../csharp/programming-guide/classes-and-structs/inheritance.md)  
 [<span data-ttu-id="4eab6-135">Yöntemleri</span><span class="sxs-lookup"><span data-stu-id="4eab6-135">Methods</span></span>](../../../csharp/programming-guide/classes-and-structs/methods.md)  
 [<span data-ttu-id="4eab6-136">Alanları</span><span class="sxs-lookup"><span data-stu-id="4eab6-136">Fields</span></span>](../../../csharp/programming-guide/classes-and-structs/fields.md)  
 [<span data-ttu-id="4eab6-137">Nasıl yapılır: soyut özellikleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="4eab6-137">How to: Define Abstract Properties</span></span>](../../../csharp/programming-guide/classes-and-structs/how-to-define-abstract-properties.md)