---
title: "ÇAKIŞMALAR (varlık SQL)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 41743e89-79cb-4d7b-8a27-355b45024b61
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: b3544eac58fe168c5f2e6a355e8cf97b4598bb76
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="overlaps-entity-sql"></a><span data-ttu-id="d3515-102">ÇAKIŞMALAR (varlık SQL)</span><span class="sxs-lookup"><span data-stu-id="d3515-102">OVERLAPS (Entity SQL)</span></span>
<span data-ttu-id="d3515-103">İki koleksiyon ortak öğeler sahip olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="d3515-103">Determines whether two collections have common elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3515-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d3515-104">Syntax</span></span>  
  
```  
expression OVERLAPS expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="d3515-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="d3515-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="d3515-106">Başka bir sorgu ifadesinden döndürülen koleksiyonu ile karşılaştırmak için bir koleksiyon döndürür herhangi bir geçerli sorgu ifade.</span><span class="sxs-lookup"><span data-stu-id="d3515-106">Any valid query expression that returns a collection to compare with the collection returned from another query expression.</span></span> <span data-ttu-id="d3515-107">Tüm ifadeler aynı türde veya ortak bir temel veya türetilmiş türünde olması gerekir `expression`.</span><span class="sxs-lookup"><span data-stu-id="d3515-107">All expressions must be of the same type or of a common base or derived type as `expression`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d3515-108">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="d3515-108">Return Value</span></span>  
 <span data-ttu-id="d3515-109">`true`iki koleksiyon ortak öğeler varsa; Aksi takdirde `false`.</span><span class="sxs-lookup"><span data-stu-id="d3515-109">`true` if the two collections have common elements; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d3515-110">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="d3515-110">Remarks</span></span>  
 <span data-ttu-id="d3515-111">İşlevsel olarak eşdeğerdir aşağıdaki ÇAKIŞMALAR sağlar:</span><span class="sxs-lookup"><span data-stu-id="d3515-111">OVERLAPS provides functionally equivalent tothe following:</span></span>  
  
 `EXISTS ( expression INTERSECT expression )`  
  
 <span data-ttu-id="d3515-112">ÇAKIŞMALAR biridir [!INCLUDE[esql](../../../../../../includes/esql-md.md)] işleçleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d3515-112">OVERLAPS is one of the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators.</span></span> <span data-ttu-id="d3515-113">Tüm [!INCLUDE[esql](../../../../../../includes/esql-md.md)] kümesi işleçleri soldan sağa değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="d3515-113">All [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators are evaluated from left to right.</span></span> <span data-ttu-id="d3515-114">Öncelik bilgilerini [!INCLUDE[esql](../../../../../../includes/esql-md.md)] işleçleri, bakın [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="d3515-114">For precedence information for the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] set operators, see [EXCEPT](../../../../../../docs/framework/data/adonet/ef/language-reference/except-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3515-115">Örnek</span><span class="sxs-lookup"><span data-stu-id="d3515-115">Example</span></span>  
 <span data-ttu-id="d3515-116">Aşağıdaki varlık SQL sorgusunu ÇAKIŞMALAR işleci belirler için iki koleksiyon ortak bir değere sahip olup olmadığını kullanır.</span><span class="sxs-lookup"><span data-stu-id="d3515-116">The following Entity SQL query uses the OVERLAPS operator to determines whether two collections have a common value.</span></span> <span data-ttu-id="d3515-117">Sorgu AdventureWorks satış modelini temel alır.</span><span class="sxs-lookup"><span data-stu-id="d3515-117">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="d3515-118">Derlemek ve bunu çalıştırmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="d3515-118">To compile and run this, follow these steps:</span></span>  
  
1.  <span data-ttu-id="d3515-119">Yordamı izleyin [nasıl yapılır: Sorgu döndürür StructuralType sonucu](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="d3515-119">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="d3515-120">Aşağıdaki sorgu bağımsız değişken olarak geçirmek `ExecuteStructuralTypeQuery` yöntemi:</span><span class="sxs-lookup"><span data-stu-id="d3515-120">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#OVERLAPS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#overlaps)]  
  
## <a name="see-also"></a><span data-ttu-id="d3515-121">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d3515-121">See Also</span></span>  
 [<span data-ttu-id="d3515-122">Varlık SQL Başvurusu</span><span class="sxs-lookup"><span data-stu-id="d3515-122">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)