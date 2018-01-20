---
title: "Nasıl yapılır: PrimitiveType sonuçları döndüren bir sorgu yürütme"
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
ms.assetid: 7139d585-4034-4dfa-916f-2120a8b72792
caps.latest.revision: "4"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: d8a38d732023cd30812a4ae2fa00b99345556a78
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-execute-a-query-that-returns-primitivetype-results"></a><span data-ttu-id="f0fbd-102">Nasıl yapılır: PrimitiveType sonuçları döndüren bir sorgu yürütme</span><span class="sxs-lookup"><span data-stu-id="f0fbd-102">How to: Execute a Query that Returns PrimitiveType Results</span></span>
<span data-ttu-id="f0fbd-103">Bu konuda kullanarak kavramsal model karşı komut yürütme gösterilmiştir bir <xref:System.Data.EntityClient.EntityCommand>ve nasıl alınacağını <xref:System.Data.Metadata.Edm.PrimitiveType> kullanarak sonuçları bir <xref:System.Data.EntityClient.EntityDataReader>.</span><span class="sxs-lookup"><span data-stu-id="f0fbd-103">This topic shows how to execute a command against a conceptual model by using an <xref:System.Data.EntityClient.EntityCommand>, and how to retrieve the <xref:System.Data.Metadata.Edm.PrimitiveType> results by using an <xref:System.Data.EntityClient.EntityDataReader>.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="f0fbd-104">Bu örnekte kodu çalıştırmak için</span><span class="sxs-lookup"><span data-stu-id="f0fbd-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="f0fbd-105">Ekleme [AdventureWorks satış modeli](http://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) projenize ve kullanmak için projenizin yapılandırma [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="f0fbd-105">Add the [AdventureWorks Sales Model](http://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="f0fbd-106">Daha fazla bilgi için bkz: [nasıl yapılır: Varlık veri modeli Sihirbazı'nı](http://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span><span class="sxs-lookup"><span data-stu-id="f0fbd-106">For more information, see [How to: Use the Entity Data Model Wizard](http://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="f0fbd-107">Uygulamanız için kod sayfasında aşağıdakileri ekleyin `using` deyimleri (`Imports` Visual Basic'te):</span><span class="sxs-lookup"><span data-stu-id="f0fbd-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="f0fbd-108">Örnek</span><span class="sxs-lookup"><span data-stu-id="f0fbd-108">Example</span></span>  
 <span data-ttu-id="f0fbd-109">Bu örnek döndüren bir sorgu yürüten bir <xref:System.Data.Metadata.Edm.PrimitiveType> sonucu.</span><span class="sxs-lookup"><span data-stu-id="f0fbd-109">This example executes a query that returns a <xref:System.Data.Metadata.Edm.PrimitiveType> result.</span></span> <span data-ttu-id="f0fbd-110">Bağımsız değişken olarak aşağıdaki sorguyu geçirdiğiniz `ExecutePrimitiveTypeQuery` işlevi, işlevi görüntüler tüm ortalama fiyat listesi `Products`:</span><span class="sxs-lookup"><span data-stu-id="f0fbd-110">If you pass the following query as an argument to the `ExecutePrimitiveTypeQuery` function, the function displays the average list price of all `Products`:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#EDM_AVG](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#edm_avg)]  
  
 <span data-ttu-id="f0fbd-111">Aşağıdaki gibi parametreli bir sorgu başarılı olursa <xref:System.Data.EntityClient.EntityParameter> nesneleri <xref:System.Data.EntityClient.EntityCommand.Parameters%2A> özellikte <xref:System.Data.EntityClient.EntityCommand> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f0fbd-111">If you pass a parameterized query, like the following, <xref:System.Data.EntityClient.EntityParameter> objects to the <xref:System.Data.EntityClient.EntityCommand.Parameters%2A> property on the <xref:System.Data.EntityClient.EntityCommand> object.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#CASE_WHEN_THEN_ELSE](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#case_when_then_else)]  
  
 [!code-csharp[DP EntityServices Concepts#eSQLPrimitiveTypes](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#esqlprimitivetypes)]
 [!code-vb[DP EntityServices Concepts#eSQLPrimitiveTypes](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#esqlprimitivetypes)]  
  
## <a name="see-also"></a><span data-ttu-id="f0fbd-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="f0fbd-112">See Also</span></span>  
 [<span data-ttu-id="f0fbd-113">Entity SQL Başvurusu</span><span class="sxs-lookup"><span data-stu-id="f0fbd-113">Entity SQL Reference</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
 [<span data-ttu-id="f0fbd-114">Entity Framework için EntityClient Sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="f0fbd-114">EntityClient Provider for the Entity Framework</span></span>](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md)
