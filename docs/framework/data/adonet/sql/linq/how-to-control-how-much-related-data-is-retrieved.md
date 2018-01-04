---
title: "Nasıl yapılır: ilgili ne kadar veri alındığını denetleme"
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
ms.assetid: efdc203e-3da9-4477-815e-54f10c3d7c6c
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: b35c6e4bcb316823a42dc8501fa08df5a87f3275
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-control-how-much-related-data-is-retrieved"></a><span data-ttu-id="3d14f-102">Nasıl yapılır: ilgili ne kadar veri alındığını denetleme</span><span class="sxs-lookup"><span data-stu-id="3d14f-102">How to: Control How Much Related Data Is Retrieved</span></span>
<span data-ttu-id="3d14f-103">Kullanım <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> yöntemi ana hedefiniz ilgili hangi verileri belirtmek için aynı anda alınan.</span><span class="sxs-lookup"><span data-stu-id="3d14f-103">Use the <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> method to specify which data related to your main target should be retrieved at the same time.</span></span> <span data-ttu-id="3d14f-104">Örneğin, müşterilerin siparişler hakkında bilgi gerekir biliyorsanız, kullanabileceğiniz <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> sipariş bilgileri, müşteri bilgileri aynı zamanda alınır emin olmak için.</span><span class="sxs-lookup"><span data-stu-id="3d14f-104">For example, if you know you will need information about customers' orders, you can use <xref:System.Data.Linq.DataLoadOptions.LoadWith%2A> to make sure that the order information is retrieved at the same time as the customer information.</span></span> <span data-ttu-id="3d14f-105">Bu yaklaşımın iki bilgi için veritabanı içinde yalnızca bir seyahat sonuçlanır.</span><span class="sxs-lookup"><span data-stu-id="3d14f-105">This approach results in only one trip to the database for both sets of information.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3d14f-106">Müşteriler hedeflediğinizde siparişleri alma gibi bir büyük projeksiyon olarak çapraz ürün alarak sorgunuzu ana hedefe ilgili verileri alabilir.</span><span class="sxs-lookup"><span data-stu-id="3d14f-106">You can retrieve data related to the main target of your query by retrieving a cross-product as one large projection, such as retrieving orders when you target customers.</span></span> <span data-ttu-id="3d14f-107">Ancak bu yaklaşım genellikle dezavantajları vardır.</span><span class="sxs-lookup"><span data-stu-id="3d14f-107">But this approach often has disadvantages.</span></span> <span data-ttu-id="3d14f-108">Örneğin, yalnızca tahminleri ve değil, değiştirilebilir ve tarafından kalıcı varlıkları sonucu olan [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="3d14f-108">For example, the results are just projections and not entities that can be changed and persisted by [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span></span> <span data-ttu-id="3d14f-109">Ve çok fazla ihtiyacınız olmayan veri alma.</span><span class="sxs-lookup"><span data-stu-id="3d14f-109">And you can be retrieving lots of data that you do not need.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d14f-110">Örnek</span><span class="sxs-lookup"><span data-stu-id="3d14f-110">Example</span></span>  
 <span data-ttu-id="3d14f-111">Aşağıdaki örnekte, tüm `Orders` tüm `Customers` kimin Londra'da buluna alınır sorgunun yürütüldüğü zaman.</span><span class="sxs-lookup"><span data-stu-id="3d14f-111">In the following example, all the `Orders` for all the `Customers` who are located in London are retrieved when the query is executed.</span></span> <span data-ttu-id="3d14f-112">Sonuç olarak, art arda gelen erişimi `Orders` özelliği bir `Customer` nesne yeni bir veritabanı sorgusu tetiklemez.</span><span class="sxs-lookup"><span data-stu-id="3d14f-112">As a result, successive access to the `Orders` property on a `Customer` object does not trigger a new database query.</span></span>  
  
 [!code-csharp[System.Data.Linq.DataLoadOptions#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.dataloadoptions/cs/program.cs#2)]
 [!code-vb[System.Data.Linq.DataLoadOptions#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.dataloadoptions/vb/module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="3d14f-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="3d14f-113">See Also</span></span>  
 [<span data-ttu-id="3d14f-114">Veritabanını Sorgulama</span><span class="sxs-lookup"><span data-stu-id="3d14f-114">Querying the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
