---
title: "Nasıl yapılır: aynı anda birçok nesne alma"
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
ms.assetid: 18aff4d8-bde8-461b-9960-ccabb24e9d22
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 780ac9087a235cee1539dfcb591d99542c68efbb
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/17/2018
---
# <a name="how-to-retrieve-many-objects-at-once"></a><span data-ttu-id="38c3a-102">Nasıl yapılır: aynı anda birçok nesne alma</span><span class="sxs-lookup"><span data-stu-id="38c3a-102">How to: Retrieve Many Objects At Once</span></span>
<span data-ttu-id="38c3a-103">Kullanarak bir sorgu birçok nesne alabilirsiniz <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span><span class="sxs-lookup"><span data-stu-id="38c3a-103">You can retrieve many objects in one query by using <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="38c3a-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="38c3a-104">Example</span></span>  
 <span data-ttu-id="38c3a-105">Aşağıdaki kod <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> her ikisi de almak için yöntemini `Customer` ve `Order` nesneleri.</span><span class="sxs-lookup"><span data-stu-id="38c3a-105">The following code uses the <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> method to retrieve both `Customer` and `Order` objects.</span></span>  
  
 [!code-csharp[DLinqQueryConcepts#9](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#9)]
 [!code-vb[DLinqQueryConcepts#9](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#9)]  
  
## <a name="see-also"></a><span data-ttu-id="38c3a-106">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="38c3a-106">See Also</span></span>  
 [<span data-ttu-id="38c3a-107">Sorgu Kavramları</span><span class="sxs-lookup"><span data-stu-id="38c3a-107">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
