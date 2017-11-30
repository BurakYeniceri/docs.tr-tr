---
title: "Yöntem temelli sorgu sözdizimi örnekleri: projeksiyonu"
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
ms.assetid: 505491fa-5920-43ce-8a96-c25389e125d8
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 9ee7c60f78f50fc4b31b39251c9e432b78a9632b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="method-based-query-syntax-examples-projection"></a><span data-ttu-id="e7f97-102">Yöntem temelli sorgu sözdizimi örnekleri: projeksiyonu</span><span class="sxs-lookup"><span data-stu-id="e7f97-102">Method-Based Query Syntax Examples: Projection</span></span>
<span data-ttu-id="e7f97-103">Bu konudaki örnekler nasıl kullanılacağını gösteren <xref:System.Linq.Enumerable.Select%2A> ve <xref:System.Linq.Enumerable.SelectMany%2A> methodsto sorgu [AdventureWorks satış modeli](http://msdn.microsoft.com/en-us/f16cd988-673f-4376-b034-129ca93c7832) yöntemi tabanlı sorgu sözdizimini kullanarak.</span><span class="sxs-lookup"><span data-stu-id="e7f97-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Select%2A> and <xref:System.Linq.Enumerable.SelectMany%2A> methodsto query the [AdventureWorks Sales Model](http://msdn.microsoft.com/en-us/f16cd988-673f-4376-b034-129ca93c7832) using method-based query syntax.</span></span> <span data-ttu-id="e7f97-104">Bu örneklerde kullanılan AdventureWorks satış modeli AdventureWorks örnek veritabanını kişi, adres, ürün, SalesOrderHeader ve satış siparişi ayrıntısını tablolarda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e7f97-104">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="e7f97-105">Aşağıdaki örneklerde bu konudaki `using` / `Imports` deyimleri:</span><span class="sxs-lookup"><span data-stu-id="e7f97-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="select"></a><span data-ttu-id="e7f97-106">Seçim</span><span class="sxs-lookup"><span data-stu-id="e7f97-106">Select</span></span>  
  
### <a name="example"></a><span data-ttu-id="e7f97-107">Örnek</span><span class="sxs-lookup"><span data-stu-id="e7f97-107">Example</span></span>  
 <span data-ttu-id="e7f97-108">Aşağıdaki örnek kullanır <xref:System.Linq.Queryable.Select%2A> yöntemi projesine `Product.Name` ve `Product.ProductID` anonim türleri dizisi özelliklerini.</span><span class="sxs-lookup"><span data-stu-id="e7f97-108">The following example uses the <xref:System.Linq.Queryable.Select%2A> method to project the `Product.Name` and `Product.ProductID` properties into a sequence of anonymous types.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectAnonymousTypes_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectanonymoustypes_mq)]
 [!code-vb[DP L2E Examples#SelectAnonymousTypes_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectanonymoustypes_mq)]  
  
### <a name="example"></a><span data-ttu-id="e7f97-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="e7f97-109">Example</span></span>  
 <span data-ttu-id="e7f97-110">Aşağıdaki örnek kullanır <xref:System.Linq.Enumerable.Select%2A> yöntemi yalnızca ürün adlarının dizisini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e7f97-110">The following example uses the <xref:System.Linq.Enumerable.Select%2A> method to return a sequence of only product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectSimple2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectsimple2_mq)]
 [!code-vb[DP L2E Examples#SelectSimple2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectsimple2_mq)]  
  
## <a name="selectmany"></a><span data-ttu-id="e7f97-111">SelectMany</span><span class="sxs-lookup"><span data-stu-id="e7f97-111">SelectMany</span></span>  
  
### <a name="example"></a><span data-ttu-id="e7f97-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="e7f97-112">Example</span></span>  
 <span data-ttu-id="e7f97-113">Aşağıdaki örnek kullanır <xref:System.Linq.Enumerable.SelectMany%2A> tümünü seçmek için yöntemi siparişleri where `TotalDue` değerinden 500,00 değil.</span><span class="sxs-lookup"><span data-stu-id="e7f97-113">The following example uses the <xref:System.Linq.Enumerable.SelectMany%2A> method to select all orders where `TotalDue` is less than 500.00.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom_mq)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom_mq)]  
  
### <a name="example"></a><span data-ttu-id="e7f97-114">Örnek</span><span class="sxs-lookup"><span data-stu-id="e7f97-114">Example</span></span>  
 <span data-ttu-id="e7f97-115">Aşağıdaki örnek kullanır <xref:System.Linq.Enumerable.SelectMany%2A> burada sırasını yapıldı 1 Ekim 2002 veya sonraki sürümlerde tüm siparişleri seçmek için yöntem.</span><span class="sxs-lookup"><span data-stu-id="e7f97-115">The following example uses the <xref:System.Linq.Enumerable.SelectMany%2A> method to select all orders where the order was made on October 1, 2002 or later.</span></span>  
  
 [!code-csharp[DP L2E Examples#SelectManyCompoundFrom2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#selectmanycompoundfrom2_mq)]
 [!code-vb[DP L2E Examples#SelectManyCompoundFrom2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#selectmanycompoundfrom2_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="e7f97-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e7f97-116">See Also</span></span>  
 [<span data-ttu-id="e7f97-117">LINQ to Entities sorguları</span><span class="sxs-lookup"><span data-stu-id="e7f97-117">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)