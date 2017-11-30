---
title: "LINQ ve Genel Türler (C#)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- LINQ [C#], generic types
- generic types [LINQ]
- generics [LINQ]
ms.assetid: 660e3799-25ca-462c-8c4a-8bce04fbb031
caps.latest.revision: "18"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e62a1573fa5ebf51a5f0f23b133c274730cfbeb6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="linq-and-generic-types-c"></a><span data-ttu-id="d4548-102">LINQ ve Genel Türler (C#)</span><span class="sxs-lookup"><span data-stu-id="d4548-102">LINQ and Generic Types (C#)</span></span>
[!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]<span data-ttu-id="d4548-103">sorguları, 2.0 sürümünde tanıtılan genel türler temel [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d4548-103"> queries are based on generic types, which were introduced in version 2.0 of the [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)].</span></span> <span data-ttu-id="d4548-104">Sorgu yazma başlamadan önce bilgisi genel türler derinlemesine gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d4548-104">You do not need an in-depth knowledge of generics before you can start writing queries.</span></span> <span data-ttu-id="d4548-105">Ancak, iki temel kavramlarını anladığınızdan isteyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="d4548-105">However, you may want to understand two basic concepts:</span></span>  
  
1.  <span data-ttu-id="d4548-106">Oluştururken bir genel koleksiyon sınıfının bir örneği gibi <xref:System.Collections.Generic.List%601>, "T" listesi tutacak nesnelerin türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d4548-106">When you create an instance of a generic collection class such as <xref:System.Collections.Generic.List%601>, you replace the "T" with the type of objects that the list will hold.</span></span> <span data-ttu-id="d4548-107">Örneğin, dizelerinin listesini olarak ifade edilir `List<string>`ve listesini `Customer` nesneleri olarak ifade edilir `List<Customer>`.</span><span class="sxs-lookup"><span data-stu-id="d4548-107">For example, a list of strings is expressed as `List<string>`, and a list of `Customer` objects is expressed as `List<Customer>`.</span></span> <span data-ttu-id="d4548-108">Genel listesini kesin türü belirtilmiş ve kendi öğeleri olarak depolamak koleksiyonlar üzerinden birçok avantaj sunar <xref:System.Object>.</span><span class="sxs-lookup"><span data-stu-id="d4548-108">A generic list is strongly typed and provides many benefits over collections that store their elements as <xref:System.Object>.</span></span> <span data-ttu-id="d4548-109">Eklemeyi denediğinizde bir `Customer` için bir `List<string>`, derleme zamanı sırasında bir hata iletisi alır.</span><span class="sxs-lookup"><span data-stu-id="d4548-109">If you try to add a `Customer` to a `List<string>`, you will get an error at compile time.</span></span> <span data-ttu-id="d4548-110">Çalışma zamanı tür-atama gerçekleştirmek olmadığı için kullanımı kolay genel koleksiyonlar var.</span><span class="sxs-lookup"><span data-stu-id="d4548-110">It is easy to use generic collections because you do not have to perform run-time type-casting.</span></span>  
  
2.  <span data-ttu-id="d4548-111"><xref:System.Collections.Generic.IEnumerable%601>arabirimi kullanarak sıralanması genel koleksiyon sınıfları sağlar `foreach` deyimi.</span><span class="sxs-lookup"><span data-stu-id="d4548-111"><xref:System.Collections.Generic.IEnumerable%601> is the interface that enables generic collection classes to be enumerated by using the `foreach` statement.</span></span> <span data-ttu-id="d4548-112">Genel koleksiyon sınıfları Destek <xref:System.Collections.Generic.IEnumerable%601> yalnızca olarak genel olmayan koleksiyonu sınıfları gibi <xref:System.Collections.ArrayList> Destek <xref:System.Collections.IEnumerable>.</span><span class="sxs-lookup"><span data-stu-id="d4548-112">Generic collection classes support <xref:System.Collections.Generic.IEnumerable%601> just as non-generic collection classes such as <xref:System.Collections.ArrayList> support <xref:System.Collections.IEnumerable>.</span></span>  
  
 <span data-ttu-id="d4548-113">Genel türler hakkında daha fazla bilgi için bkz: [genel türler](../../../../csharp/programming-guide/generics/index.md).</span><span class="sxs-lookup"><span data-stu-id="d4548-113">For more information about generics, see [Generics](../../../../csharp/programming-guide/generics/index.md).</span></span>  
  
## <a name="ienumerablet-variables-in-linq-queries"></a><span data-ttu-id="d4548-114">IEnumerable < T\> LINQ sorgularını değişkenleri</span><span class="sxs-lookup"><span data-stu-id="d4548-114">IEnumerable<T\> variables in LINQ Queries</span></span>  
 [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)]<span data-ttu-id="d4548-115">sorgu değişkenleri olarak yazılan <xref:System.Collections.Generic.IEnumerable%601> veya türetilmiş bir tür gibi <xref:System.Linq.IQueryable%601>.</span><span class="sxs-lookup"><span data-stu-id="d4548-115"> query variables are typed as <xref:System.Collections.Generic.IEnumerable%601> or a derived type such as <xref:System.Linq.IQueryable%601>.</span></span> <span data-ttu-id="d4548-116">Olarak yazılan bir sorgu değişkeni gördüğünüzde `IEnumerable<Customer>`, yalnızca yürütüldüğünde, sorgu, sıfır veya daha fazla dizisini üretecektir gelir `Customer` nesneleri.</span><span class="sxs-lookup"><span data-stu-id="d4548-116">When you see a query variable that is typed as `IEnumerable<Customer>`, it just means that the query, when it is executed, will produce a sequence of zero or more `Customer` objects.</span></span>  
  
 [!code-csharp[csLINQGettingStarted#34](../../../../csharp/programming-guide/concepts/linq/codesnippet/CSharp/linq-and-generic-types_1.cs)]  
  
 <span data-ttu-id="d4548-117">Daha fazla bilgi için bkz: [LINQ Sorgu işlemlerinde tür ilişkileri](../../../../csharp/programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d4548-117">For more information, see [Type Relationships in LINQ Query Operations](../../../../csharp/programming-guide/concepts/linq/type-relationships-in-linq-query-operations.md).</span></span>  
  
## <a name="letting-the-compiler-handle-generic-type-declarations"></a><span data-ttu-id="d4548-118">Derleyici tanıtıcı genel tür bildirimleri izin vererek</span><span class="sxs-lookup"><span data-stu-id="d4548-118">Letting the Compiler Handle Generic Type Declarations</span></span>  
 <span data-ttu-id="d4548-119">İsterseniz, kullanarak genel sözdizimi önleyebilirsiniz [var](../../../../csharp/language-reference/keywords/var.md) anahtar sözcüğü.</span><span class="sxs-lookup"><span data-stu-id="d4548-119">If you prefer, you can avoid generic syntax by using the [var](../../../../csharp/language-reference/keywords/var.md) keyword.</span></span> <span data-ttu-id="d4548-120">`var` Anahtar sözcüğü bir sorgu değişkeninin türü belirtilen veri kaynağı bakarak gerçekleştirip derleyici bildirir `from` yan tümcesi.</span><span class="sxs-lookup"><span data-stu-id="d4548-120">The `var` keyword instructs the compiler to infer the type of a query variable by looking at the data source specified in the `from` clause.</span></span> <span data-ttu-id="d4548-121">Aşağıdaki örnek önceki örnekteki gibi aynı derlenmiş kod üretir:</span><span class="sxs-lookup"><span data-stu-id="d4548-121">The following example produces the same compiled code as the previous example:</span></span>  
  
 [!code-csharp[csLINQGettingStarted#35](../../../../csharp/programming-guide/concepts/linq/codesnippet/CSharp/linq-and-generic-types_2.cs)]  
  
 <span data-ttu-id="d4548-122">`var` Anahtar sözcüğü, değişkenin türü açık olduğunda veya ne zaman Grup sorgular tarafından üretilen olanlar gibi iç içe geçmiş genel türler açıkça belirtmek bu önemli değildir yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="d4548-122">The `var` keyword is useful when the type of the variable is obvious or when it is not that important to explicitly specify nested generic types such as those that are produced by group queries.</span></span> <span data-ttu-id="d4548-123">Kullanırsanız, genel olarak, öneririz `var`, kodunuzu daha başkalarının okunmasını zorlaştırabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d4548-123">In general, we recommend that if you use `var`, realize that it can make your code more difficult for others to read.</span></span> <span data-ttu-id="d4548-124">Daha fazla bilgi için bkz: [örtük olarak yazılan yerel değişkenler](../../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md).</span><span class="sxs-lookup"><span data-stu-id="d4548-124">For more information, see [Implicitly Typed Local Variables](../../../../csharp/programming-guide/classes-and-structs/implicitly-typed-local-variables.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4548-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d4548-125">See Also</span></span>  
 [<span data-ttu-id="d4548-126">C# üzerinde LINQ ile çalışmaya başlama</span><span class="sxs-lookup"><span data-stu-id="d4548-126">Getting Started with LINQ in C#</span></span>](../../../../csharp/programming-guide/concepts/linq/getting-started-with-linq.md)  
 [<span data-ttu-id="d4548-127">Genel türler</span><span class="sxs-lookup"><span data-stu-id="d4548-127">Generics</span></span>](../../../../csharp/programming-guide/generics/index.md)