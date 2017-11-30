---
title: "Nasıl yapılır: çağrı kullanıcı tanımlı işlevler satır içi"
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
ms.assetid: f80d4327-b6a5-4aa8-a743-e95d09a2a02e
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: b39d71cd0f9aee855133c646fbec6a7f4f6f3c40
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-call-user-defined-functions-inline"></a><span data-ttu-id="e5be2-102">Nasıl yapılır: çağrı kullanıcı tanımlı işlevler satır içi</span><span class="sxs-lookup"><span data-stu-id="e5be2-102">How to: Call User-Defined Functions Inline</span></span>
<span data-ttu-id="e5be2-103">Kullanıcı tanımlı işlevler satır içi çağırabilirsiniz olsa da, sorgu yürütülür kadar yürütme ertelenmiş sorguda içerdiği işlevleri yürütülmez.</span><span class="sxs-lookup"><span data-stu-id="e5be2-103">Although you can call user-defined functions inline, functions that are included in a query whose execution is deferred are not executed until the query is executed.</span></span> <span data-ttu-id="e5be2-104">Daha fazla bilgi için bkz: [LINQ sorgularını (C#) giriş](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).</span><span class="sxs-lookup"><span data-stu-id="e5be2-104">For more information, see [Introduction to LINQ Queries (C#)](~/docs/csharp/programming-guide/concepts/linq/introduction-to-linq-queries.md).</span></span>  
  
 <span data-ttu-id="e5be2-105">Aynı işlevin bir sorgu dışında çağırdığınızda [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] yöntemi çağrısı ifadesinden basit bir sorgu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5be2-105">When you call the same function outside a query, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] creates a simple query from the method call expression.</span></span> <span data-ttu-id="e5be2-106">SQL söz dizimi aşağıdaki gibidir (parametre `@p0` geçirilen sabiti bağlı):</span><span class="sxs-lookup"><span data-stu-id="e5be2-106">The following is the SQL syntax (the parameter `@p0` is bound to the constant passed in):</span></span>  
  
```  
SELECT dbo.ReverseCustName(@p0)  
```  
  
 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="e5be2-107">Aşağıdaki oluşturur:</span><span class="sxs-lookup"><span data-stu-id="e5be2-107"> creates the following:</span></span>  
  
 [!code-csharp[DLinqUDFS#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqUDFS/cs/Program.cs#4)]
 [!code-vb[DLinqUDFS#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqUDFS/vb/Module1.vb#4)]  
  
## <a name="example"></a><span data-ttu-id="e5be2-108">Örnek</span><span class="sxs-lookup"><span data-stu-id="e5be2-108">Example</span></span>  
 <span data-ttu-id="e5be2-109">Aşağıdaki [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] sorgu için oluşturulan kullanıcı tanımlı işlev yöntemini çağırın satır içi görebilirsiniz `ReverseCustName`.</span><span class="sxs-lookup"><span data-stu-id="e5be2-109">In the following [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] query, you can see an inline call to the generated user-defined function method `ReverseCustName`.</span></span> <span data-ttu-id="e5be2-110">Sorgu yürütme ertelenmiş çünkü işlev hemen yürütülemiyor.</span><span class="sxs-lookup"><span data-stu-id="e5be2-110">The function is not executed immediately because query execution is deferred.</span></span> <span data-ttu-id="e5be2-111">SQL veritabanındaki kullanıcı tanımlı işlev çağrısı için bu sorguyu çevirir için oluşturulmuş (sorgu aşağıdaki SQL kodunu bakın).</span><span class="sxs-lookup"><span data-stu-id="e5be2-111">The SQL built for this query translates to a call to the user-defined function in the database (see the SQL code following the query).</span></span>  
  
 [!code-csharp[DLinqUDFS#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqUDFS/cs/Program.cs#5)]
 [!code-vb[DLinqUDFS#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqUDFS/vb/Module1.vb#5)]  
  
```  
SELECT [t0].[ContactName],  
    dbo.ReverseCustName([t0].[ContactTitle]) AS [Title]  
FROM [Customers] AS [t0]  
```  
  
## <a name="see-also"></a><span data-ttu-id="e5be2-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e5be2-112">See Also</span></span>  
 [<span data-ttu-id="e5be2-113">Kullanıcı tanımlı işlevler</span><span class="sxs-lookup"><span data-stu-id="e5be2-113">User-Defined Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/user-defined-functions.md)