---
title: 'Nasıl yapılır: EntityCommand kullanarak parametreli varlık SQL sorgusu yürütme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: e93fea43-7e03-4d7d-9fee-2517b8b88cba
ms.openlocfilehash: 12304064a20adf66ac5db2195ae2d103ffa22c09
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/05/2018
ms.locfileid: "43774004"
---
# <a name="how-to-execute-a-parameterized-entity-sql-query-using-entitycommand"></a><span data-ttu-id="a660e-102">Nasıl yapılır: EntityCommand kullanarak parametreli varlık SQL sorgusu yürütme</span><span class="sxs-lookup"><span data-stu-id="a660e-102">How to: Execute a Parameterized Entity SQL Query Using EntityCommand</span></span>
<span data-ttu-id="a660e-103">Bu konu nasıl çalıştırılacağını gösteren bir [!INCLUDE[esql](../../../../../includes/esql-md.md)] kullanarak parametreleri olan sorgu bir <xref:System.Data.EntityClient.EntityCommand> nesne.</span><span class="sxs-lookup"><span data-stu-id="a660e-103">This topic shows how to execute an [!INCLUDE[esql](../../../../../includes/esql-md.md)] query that has parameters by using an <xref:System.Data.EntityClient.EntityCommand> object.</span></span>  
  
### <a name="to-run-the-code-in-this-example"></a><span data-ttu-id="a660e-104">Bu örnekte, kodu çalıştırmak için</span><span class="sxs-lookup"><span data-stu-id="a660e-104">To run the code in this example</span></span>  
  
1.  <span data-ttu-id="a660e-105">Ekleme [AdventureWorks satışları modeli](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) projenize ve projenizi kullanmak üzere yapılandırma [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a660e-105">Add the [AdventureWorks Sales Model](https://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) to your project and configure your project to use the [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].</span></span> <span data-ttu-id="a660e-106">Daha fazla bilgi için [nasıl yapılır: Varlık veri modeli Sihirbazı'nı](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span><span class="sxs-lookup"><span data-stu-id="a660e-106">For more information, see [How to: Use the Entity Data Model Wizard](https://msdn.microsoft.com/library/dadb058a-c5d9-4c5c-8b01-28044112231d).</span></span>  
  
2.  <span data-ttu-id="a660e-107">Uygulamanız için kod sayfasında, aşağıdakileri ekleyin `using` deyimleri (`Imports` Visual Basic'te):</span><span class="sxs-lookup"><span data-stu-id="a660e-107">In the code page for your application, add the following `using` statements (`Imports` in Visual Basic):</span></span>  
  
     [!code-csharp[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#namespaces)]
     [!code-vb[DP EntityServices Concepts#Namespaces](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#namespaces)]  
  
## <a name="example"></a><span data-ttu-id="a660e-108">Örnek</span><span class="sxs-lookup"><span data-stu-id="a660e-108">Example</span></span>  
 <span data-ttu-id="a660e-109">Aşağıdaki örnek, iki parametre ile bir sorgu dizesi oluşturmak gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a660e-109">The following example shows how to construct a query string with two parameters.</span></span> <span data-ttu-id="a660e-110">Ardından oluşturur bir <xref:System.Data.EntityClient.EntityCommand>, iki parametre için ekler <xref:System.Data.EntityClient.EntityParameter> , koleksiyonu <xref:System.Data.EntityClient.EntityCommand>ve koleksiyonu yineleme `Contact` öğeleri.</span><span class="sxs-lookup"><span data-stu-id="a660e-110">It then creates an <xref:System.Data.EntityClient.EntityCommand>, adds two parameters to the <xref:System.Data.EntityClient.EntityParameter> collection of that <xref:System.Data.EntityClient.EntityCommand>, and iterates through the collection of `Contact` items.</span></span>  
  
 [!code-csharp[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts/cs/source.cs#parameterizedquerywithentitycommand)]
 [!code-vb[DP EntityServices Concepts#ParameterizedQueryWithEntityCommand](../../../../../samples/snippets/visualbasic/VS_Snippets_Data/dp entityservices concepts/vb/source.vb#parameterizedquerywithentitycommand)]  
  
## <a name="see-also"></a><span data-ttu-id="a660e-111">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a660e-111">See Also</span></span>  
 [<span data-ttu-id="a660e-112">Nasıl yapılır: bir parametreli sorguyu yürütme</span><span class="sxs-lookup"><span data-stu-id="a660e-112">How to: Execute a Parameterized Query</span></span>](https://msdn.microsoft.com/library/42048f03-c65c-4d98-b50a-3e7d537a63e8)  
 [<span data-ttu-id="a660e-113">Entity SQL Dili</span><span class="sxs-lookup"><span data-stu-id="a660e-113">Entity SQL Language</span></span>](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md)
