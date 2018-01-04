---
title: "Bir sayısal sırada değerlerinin toplamı işlem"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 24e335b0-984e-4825-8721-0a91b533b7c3
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: 6b28c6f9626919ee52be2a42eb2f68aecc9acbf6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="compute-the-sum-of-values-in-a-numeric-sequence"></a><span data-ttu-id="432b4-102">Bir sayısal sırada değerlerinin toplamı işlem</span><span class="sxs-lookup"><span data-stu-id="432b4-102">Compute the Sum of Values in a Numeric Sequence</span></span>
<span data-ttu-id="432b4-103">Kullanım <xref:System.Linq.Enumerable.Sum%2A> bir sırada sayısal değerlerinin toplamı işlem işleci.</span><span class="sxs-lookup"><span data-stu-id="432b4-103">Use the <xref:System.Linq.Enumerable.Sum%2A> operator to compute the sum of numeric values in a sequence.</span></span>  
  
 <span data-ttu-id="432b4-104">Aşağıdaki özellikleri Not `Sum` işlecinde [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]:</span><span class="sxs-lookup"><span data-stu-id="432b4-104">Note the following characteristics of the `Sum` operator in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]:</span></span>  
  
-   <span data-ttu-id="432b4-105">Standart sorgu işleci Toplama işleci `Sum` için boş bir dizi veya yalnızca null içeren bir dizi sıfır değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="432b4-105">The Standard Query Operator aggregate operator `Sum` evaluates to zero for an empty sequence or a sequence that contains only nulls.</span></span> <span data-ttu-id="432b4-106">İçinde [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], SQL semantiği sol değişmez.</span><span class="sxs-lookup"><span data-stu-id="432b4-106">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], the semantics of SQL are left unchanged.</span></span> <span data-ttu-id="432b4-107">Bu nedenle, `Sum` null yerine sıfır yalnızca null içeren bir dizi veya boş bir dizi için değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="432b4-107">For this reason, `Sum` evaluates to null instead of to zero for an empty sequence or for a sequence that contains only nulls.</span></span>  
  
-   <span data-ttu-id="432b4-108">Ara sonuçların SQL sınırlamalar uygulanır Toplamaların [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="432b4-108">SQL limitations on intermediate results apply to aggregates in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span> <span data-ttu-id="432b4-109">32 bit tamsayı miktarların toplamı hesaplanan 64-bit sonuçları kullanarak ve taşma için oluşabilir [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] çevrilmesi `Sum`.</span><span class="sxs-lookup"><span data-stu-id="432b4-109">Sum of 32-bit integer quantities is not computed by using 64-bit results, and overflow can occur for the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] translation of `Sum`.</span></span> <span data-ttu-id="432b4-110">Standart sorgu işleci uygulama karşılık gelen bellek içi dizisi taşma neden olmaz olsa bile bu olasılığı bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="432b4-110">This possibility exists even if the Standard Query Operator implementation does not cause an overflow for the corresponding in-memory sequence.</span></span>  
  
## <a name="example"></a><span data-ttu-id="432b4-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="432b4-111">Example</span></span>  
 <span data-ttu-id="432b4-112">Aşağıdaki örnekte tüm siparişler, toplam nakliye bulur `Order` tablo.</span><span class="sxs-lookup"><span data-stu-id="432b4-112">The following example finds the total freight of all orders in the `Order` table.</span></span>  
  
 <span data-ttu-id="432b4-113">Northwind örnek veritabanı karşı bu sorguyu çalıştırmak, çıktısı şöyledir: `64942.6900`.</span><span class="sxs-lookup"><span data-stu-id="432b4-113">If you run this query against the Northwind sample database, the output is: `64942.6900`.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#12](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#12)]
 [!code-vb[DLinqQueryExamples#12](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#12)]  
  
## <a name="example"></a><span data-ttu-id="432b4-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="432b4-114">Example</span></span>  
 <span data-ttu-id="432b4-115">Aşağıdaki örnek, tüm ürünleri için sipariş birimlerin toplam sayısını bulur.</span><span class="sxs-lookup"><span data-stu-id="432b4-115">The following example finds the total number of units on order for all products.</span></span>  
  
 <span data-ttu-id="432b4-116">Northwind örnek veritabanı karşı bu sorguyu çalıştırmak, çıktısı şöyledir: `780`.</span><span class="sxs-lookup"><span data-stu-id="432b4-116">If you run this query against the Northwind sample database, the output is: `780`.</span></span>  
  
 <span data-ttu-id="432b4-117">Cast gerekir Not `short` türleri (örneğin, `UnitsOnOrder`) çünkü `Sum` kısa türleri için hiçbir aşırı yüklemesi vardır.</span><span class="sxs-lookup"><span data-stu-id="432b4-117">Note that you must cast `short` types (for example, `UnitsOnOrder`) because `Sum` has no overload for short types.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#13](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#13)]
 [!code-vb[DLinqQueryExamples#13](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#13)]  
  
## <a name="see-also"></a><span data-ttu-id="432b4-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="432b4-118">See Also</span></span>  
 [<span data-ttu-id="432b4-119">Toplu Sorgular</span><span class="sxs-lookup"><span data-stu-id="432b4-119">Aggregate Queries</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/aggregate-queries.md)  
 [<span data-ttu-id="432b4-120">Örnek Veritabanları İndirme</span><span class="sxs-lookup"><span data-stu-id="432b4-120">Downloading Sample Databases</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/downloading-sample-databases.md)
