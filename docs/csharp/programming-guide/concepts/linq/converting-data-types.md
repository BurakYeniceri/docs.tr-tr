---
title: "Dönüştürme veri türleri (C#)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-csharp
ms.topic: article
ms.assetid: 46e5682f-77a1-4302-8f93-a2b53c408808
caps.latest.revision: "3"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 4733694c2a9fd7c83520b0bf2edea6ebffb47041
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="converting-data-types-c"></a><span data-ttu-id="59a9b-102">Dönüştürme veri türleri (C#)</span><span class="sxs-lookup"><span data-stu-id="59a9b-102">Converting Data Types (C#)</span></span>
<span data-ttu-id="59a9b-103">Dönüştürme yöntemleri giriş nesnelerin türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="59a9b-103">Conversion methods change the type of input objects.</span></span>  
  
 <span data-ttu-id="59a9b-104">LINQ sorgularını dönüştürme işlemlerinde çeşitli uygulamalar yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="59a9b-104">Conversion operations in LINQ queries are useful in a variety of applications.</span></span> <span data-ttu-id="59a9b-105">Bazı örnekler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="59a9b-105">Following are some examples:</span></span>  
  
-   <span data-ttu-id="59a9b-106"><xref:System.Linq.Enumerable.AsEnumerable%2A?displayProperty=nameWithType> Yöntemi, bir türün özel bir standart sorgu işleci uyarlamasını gizlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="59a9b-106">The <xref:System.Linq.Enumerable.AsEnumerable%2A?displayProperty=nameWithType> method can be used to hide a type's custom implementation of a standard query operator.</span></span>  
  
-   <span data-ttu-id="59a9b-107"><xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType> Yöntemi, LINQ sorgusu için koleksiyonları parametresiz etkinleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="59a9b-107">The <xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType> method can be used to enable non-parameterized collections for LINQ querying.</span></span>  
  
-   <span data-ttu-id="59a9b-108"><xref:System.Linq.Enumerable.ToArray%2A?displayProperty=nameWithType>, <xref:System.Linq.Enumerable.ToDictionary%2A?displayProperty=nameWithType>, <xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType>, Ve <xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType> yöntemleri, sorgu numaralandırılan kadar yerine onu ertelemeyi hemen sorgu yürütme zorlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="59a9b-108">The <xref:System.Linq.Enumerable.ToArray%2A?displayProperty=nameWithType>, <xref:System.Linq.Enumerable.ToDictionary%2A?displayProperty=nameWithType>, <xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType>, and <xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType> methods can be used to force immediate query execution instead of deferring it until the query is enumerated.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="59a9b-109">Yöntemler</span><span class="sxs-lookup"><span data-stu-id="59a9b-109">Methods</span></span>  
 <span data-ttu-id="59a9b-110">Aşağıdaki tabloda veri türü dönüşümleri gerçekleştirmek standart sorgu işleci yöntemlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="59a9b-110">The following table lists the standard query operator methods that perform data-type conversions.</span></span>  
  
 <span data-ttu-id="59a9b-111">Bu tabloda, adları "As" başlayın dönüştürme yöntemleri kaynak koleksiyonu statik türünü değiştirme ancak bunu numaralandırmak değil.</span><span class="sxs-lookup"><span data-stu-id="59a9b-111">The conversion methods in this table whose names start with "As" change the static type of the source collection but do not enumerate it.</span></span> <span data-ttu-id="59a9b-112">"Kaynak toplamasını ve öğeleri karşılık gelen koleksiyona koymak için" ile adları başlayan yöntemleri yazın.</span><span class="sxs-lookup"><span data-stu-id="59a9b-112">The methods whose names start with "To" enumerate the source collection and put the items into the corresponding collection type.</span></span>  
  
|<span data-ttu-id="59a9b-113">Yöntem adı</span><span class="sxs-lookup"><span data-stu-id="59a9b-113">Method Name</span></span>|<span data-ttu-id="59a9b-114">Açıklama</span><span class="sxs-lookup"><span data-stu-id="59a9b-114">Description</span></span>|<span data-ttu-id="59a9b-115">C# sorgu ifade sözdizimi</span><span class="sxs-lookup"><span data-stu-id="59a9b-115">C# Query Expression Syntax</span></span>|<span data-ttu-id="59a9b-116">Daha Fazla Bilgi</span><span class="sxs-lookup"><span data-stu-id="59a9b-116">More Information</span></span>|  
|-----------------|-----------------|---------------------------------|----------------------|  
|<span data-ttu-id="59a9b-117">AsEnumerable</span><span class="sxs-lookup"><span data-stu-id="59a9b-117">AsEnumerable</span></span>|<span data-ttu-id="59a9b-118">Olarak yazılan giriş döndürür <xref:System.Collections.Generic.IEnumerable%601>.</span><span class="sxs-lookup"><span data-stu-id="59a9b-118">Returns the input typed as <xref:System.Collections.Generic.IEnumerable%601>.</span></span>|<span data-ttu-id="59a9b-119">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-119">Not applicable.</span></span>|<xref:System.Linq.Enumerable.AsEnumerable%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-120">AsQueryable</span><span class="sxs-lookup"><span data-stu-id="59a9b-120">AsQueryable</span></span>|<span data-ttu-id="59a9b-121">(Genel) dönüştürür <xref:System.Collections.IEnumerable> (Genel) <xref:System.Linq.IQueryable>.</span><span class="sxs-lookup"><span data-stu-id="59a9b-121">Converts a (generic) <xref:System.Collections.IEnumerable> to a (generic) <xref:System.Linq.IQueryable>.</span></span>|<span data-ttu-id="59a9b-122">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-122">Not applicable.</span></span>|<xref:System.Linq.Queryable.AsQueryable%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-123">Cast</span><span class="sxs-lookup"><span data-stu-id="59a9b-123">Cast</span></span>|<span data-ttu-id="59a9b-124">Belirtilen tür için bir koleksiyonun öğelerini çevirir.</span><span class="sxs-lookup"><span data-stu-id="59a9b-124">Casts the elements of a collection to a specified type.</span></span>|<span data-ttu-id="59a9b-125">Açıkça belirtilmiş aralık değişkeni kullanın.</span><span class="sxs-lookup"><span data-stu-id="59a9b-125">Use an explicitly typed range variable.</span></span> <span data-ttu-id="59a9b-126">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="59a9b-126">For example:</span></span><br /><br /> `from string str in words`|<xref:System.Linq.Enumerable.Cast%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.Cast%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-127">OfType</span><span class="sxs-lookup"><span data-stu-id="59a9b-127">OfType</span></span>|<span data-ttu-id="59a9b-128">Değerleri yeteneklerini bir belirtilen türe göre filtreler.</span><span class="sxs-lookup"><span data-stu-id="59a9b-128">Filters values, depending on their ability to be cast to a specified type.</span></span>|<span data-ttu-id="59a9b-129">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-129">Not applicable.</span></span>|<xref:System.Linq.Enumerable.OfType%2A?displayProperty=nameWithType><br /><br /> <xref:System.Linq.Queryable.OfType%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-130">ToArray</span><span class="sxs-lookup"><span data-stu-id="59a9b-130">ToArray</span></span>|<span data-ttu-id="59a9b-131">Bir koleksiyonu bir diziye dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="59a9b-131">Converts a collection to an array.</span></span> <span data-ttu-id="59a9b-132">Bu yöntem, sorgu yürütme zorlar.</span><span class="sxs-lookup"><span data-stu-id="59a9b-132">This method forces query execution.</span></span>|<span data-ttu-id="59a9b-133">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-133">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToArray%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-134">Todictionary öğesini</span><span class="sxs-lookup"><span data-stu-id="59a9b-134">ToDictionary</span></span>|<span data-ttu-id="59a9b-135">Öğeler haline getirir bir <xref:System.Collections.Generic.Dictionary%602> bir anahtar Seçici işlevine bağlı.</span><span class="sxs-lookup"><span data-stu-id="59a9b-135">Puts elements into a <xref:System.Collections.Generic.Dictionary%602> based on a key selector function.</span></span> <span data-ttu-id="59a9b-136">Bu yöntem, sorgu yürütme zorlar.</span><span class="sxs-lookup"><span data-stu-id="59a9b-136">This method forces query execution.</span></span>|<span data-ttu-id="59a9b-137">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-137">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToDictionary%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-138">ToList</span><span class="sxs-lookup"><span data-stu-id="59a9b-138">ToList</span></span>|<span data-ttu-id="59a9b-139">Bir koleksiyona dönüştüren bir <xref:System.Collections.Generic.List%601>.</span><span class="sxs-lookup"><span data-stu-id="59a9b-139">Converts a collection to a <xref:System.Collections.Generic.List%601>.</span></span> <span data-ttu-id="59a9b-140">Bu yöntem, sorgu yürütme zorlar.</span><span class="sxs-lookup"><span data-stu-id="59a9b-140">This method forces query execution.</span></span>|<span data-ttu-id="59a9b-141">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-141">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToList%2A?displayProperty=nameWithType>|  
|<span data-ttu-id="59a9b-142">ToLookup</span><span class="sxs-lookup"><span data-stu-id="59a9b-142">ToLookup</span></span>|<span data-ttu-id="59a9b-143">Öğeler haline getirir bir <xref:System.Linq.Lookup%602> (bir-çok sözlük) dayalı bir anahtar Seçici işlevdir.</span><span class="sxs-lookup"><span data-stu-id="59a9b-143">Puts elements into a <xref:System.Linq.Lookup%602> (a one-to-many dictionary) based on a key selector function.</span></span> <span data-ttu-id="59a9b-144">Bu yöntem, sorgu yürütme zorlar.</span><span class="sxs-lookup"><span data-stu-id="59a9b-144">This method forces query execution.</span></span>|<span data-ttu-id="59a9b-145">Yok.</span><span class="sxs-lookup"><span data-stu-id="59a9b-145">Not applicable.</span></span>|<xref:System.Linq.Enumerable.ToLookup%2A?displayProperty=nameWithType>|  
  
## <a name="query-expression-syntax-example"></a><span data-ttu-id="59a9b-146">Sorgu ifade sözdizimi örneği</span><span class="sxs-lookup"><span data-stu-id="59a9b-146">Query Expression Syntax Example</span></span>  
 <span data-ttu-id="59a9b-147">Aşağıdaki kod örneğinde açıkça belirtilmiş aralık değişkeni bir alt türü yalnızca alt üzerinde kullanılabilir üyesi erişmeden önce türe için kullanır.</span><span class="sxs-lookup"><span data-stu-id="59a9b-147">The following code example uses an explicitly-typed range variable  to cast a type to a subtype before accessing a member that is available only on the subtype.</span></span>  
  
```csharp  
class Plant  
{  
    public string Name { get; set; }  
}  
  
class CarnivorousPlant : Plant  
{  
    public string TrapType { get; set; }  
}  
  
static void Cast()  
{  
    Plant[] plants = new Plant[] {  
        new CarnivorousPlant { Name = "Venus Fly Trap", TrapType = "Snap Trap" },  
        new CarnivorousPlant { Name = "Pitcher Plant", TrapType = "Pitfall Trap" },  
        new CarnivorousPlant { Name = "Sundew", TrapType = "Flypaper Trap" },  
        new CarnivorousPlant { Name = "Waterwheel Plant", TrapType = "Snap Trap" }  
    };  
  
    var query = from CarnivorousPlant cPlant in plants  
                where cPlant.TrapType == "Snap Trap"  
                select cPlant;  
  
    foreach (Plant plant in query)  
        Console.WriteLine(plant.Name);  
  
    /* This code produces the following output:  
  
        Venus Fly Trap  
        Waterwheel Plant  
    */  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="59a9b-148">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="59a9b-148">See Also</span></span>  
 <xref:System.Linq>  
 [<span data-ttu-id="59a9b-149">Standart sorgu işleçlerine genel bakış (C#)</span><span class="sxs-lookup"><span data-stu-id="59a9b-149">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)  
 [<span data-ttu-id="59a9b-150">from yan tümcesi</span><span class="sxs-lookup"><span data-stu-id="59a9b-150">from clause</span></span>](../../../../csharp/language-reference/keywords/from-clause.md)  
 [<span data-ttu-id="59a9b-151">LINQ Sorgu ifadeleri</span><span class="sxs-lookup"><span data-stu-id="59a9b-151">LINQ Query Expressions</span></span>](../../../../csharp/programming-guide/linq-query-expressions/index.md)  
 [<span data-ttu-id="59a9b-152">Nasıl yapılır: LINQ (C#) ile ArrayList sorgulama</span><span class="sxs-lookup"><span data-stu-id="59a9b-152">How to: Query an ArrayList with LINQ (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-query-an-arraylist-with-linq.md)