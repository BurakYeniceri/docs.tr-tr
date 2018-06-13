---
title: İki dizinin kümesi kesişimini döndürür
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d09c344e-3548-4944-a3ed-051880e3f5b8
ms.openlocfilehash: 9fd2a5dc435829d08594ea3c2f1c129328386250
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358790"
---
# <a name="return-the-set-intersection-of-two-sequences"></a><span data-ttu-id="a1c24-102">İki dizinin kümesi kesişimini döndürür</span><span class="sxs-lookup"><span data-stu-id="a1c24-102">Return the Set Intersection of Two Sequences</span></span>
<span data-ttu-id="a1c24-103">Kullanım <xref:System.Linq.Queryable.Intersect%2A> iki sıraları kümesi kesişimi işleci.</span><span class="sxs-lookup"><span data-stu-id="a1c24-103">Use the <xref:System.Linq.Queryable.Intersect%2A> operator to return the set intersection of two sequences.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a1c24-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="a1c24-104">Example</span></span>  
 <span data-ttu-id="a1c24-105">Bu örnekte <xref:System.Linq.Queryable.Intersect%2A> tüm ülkelerde dizisi hangi ikisi de döndürülecek `Customers` ve `Employees` Canlı.</span><span class="sxs-lookup"><span data-stu-id="a1c24-105">This example uses <xref:System.Linq.Queryable.Intersect%2A> to return a sequence of all countries in which both `Customers` and `Employees` live.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#42](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#42)]
 [!code-vb[DLinqQueryExamples#42](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#42)]  
  
 <span data-ttu-id="a1c24-106">İçinde [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], <xref:System.Linq.Queryable.Intersect%2A> işlemi yalnızca kümeleri üzerinde iyi tanımlanmış.</span><span class="sxs-lookup"><span data-stu-id="a1c24-106">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the <xref:System.Linq.Queryable.Intersect%2A> operation is well defined only on sets.</span></span> <span data-ttu-id="a1c24-107">Multisets anlamları tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="a1c24-107">The semantics for multisets is undefined.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a1c24-108">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a1c24-108">See Also</span></span>  
 [<span data-ttu-id="a1c24-109">Sorgu Örnekleri</span><span class="sxs-lookup"><span data-stu-id="a1c24-109">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)  
 [<span data-ttu-id="a1c24-110">Standart Sorgu İşleci Çevirisi</span><span class="sxs-lookup"><span data-stu-id="a1c24-110">Standard Query Operator Translation</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/standard-query-operator-translation.md)
