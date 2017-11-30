---
title: "ADO.NET'e LINQ (Portal Sayfası)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-csharp
ms.topic: article
ms.assetid: 6bd269b4-3509-4688-b672-836008704182
caps.latest.revision: "3"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 649497f28ef5f9758ba6d6df13a91a1246d12136
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="linq-to-adonet-portal-page"></a><span data-ttu-id="4662b-102">ADO.NET'e LINQ (Portal Sayfası)</span><span class="sxs-lookup"><span data-stu-id="4662b-102">LINQ to ADO.NET (Portal Page)</span></span>
[!INCLUDE[linq_adonet](~/includes/linq-adonet-md.md)]<span data-ttu-id="4662b-103">herhangi bir numaralandırılabilir nesnesinde üzerinden sorgu sağlar [!INCLUDE[vstecado](~/includes/vstecado-md.md)] kullanarak [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] programlama modeli.</span><span class="sxs-lookup"><span data-stu-id="4662b-103"> enables you to query over any enumerable object in [!INCLUDE[vstecado](~/includes/vstecado-md.md)] by using the [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] programming model.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4662b-104">[!INCLUDE[linq_adonet](~/includes/linq-adonet-md.md)] Belgeleri, .NET Framework SDK ADO.NET bölümünde bulunur: [LINQ ve ADO.NET](http://msdn.microsoft.com/library/bf0c8f93-3ff7-49f3-8aed-f2b7ac938dec).</span><span class="sxs-lookup"><span data-stu-id="4662b-104">The [!INCLUDE[linq_adonet](~/includes/linq-adonet-md.md)] documentation is located in the ADO.NET section of the .NET Framework SDK: [LINQ and ADO.NET](http://msdn.microsoft.com/library/bf0c8f93-3ff7-49f3-8aed-f2b7ac938dec).</span></span>  
  
 <span data-ttu-id="4662b-105">Üç ayrı ADO.NET vardır [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] teknolojileri: [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)], [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)], ve [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4662b-105">There are three separate ADO.NET [!INCLUDE[vbteclinqext](~/includes/vbteclinqext-md.md)] technologies: [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)], [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)], and [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)].</span></span> [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)]<span data-ttu-id="4662b-106">daha zengin, en iyi duruma getirilmiş üzerinden sorgulama sağlar <xref:System.Data.DataSet>, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] doğrudan sorgu olanak tanır [!INCLUDE[ssNoVersion](~/includes/ssnoversion-md.md)] veritabanı şemalarını ve [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)] sorgu sayesinde bir [!INCLUDE[adonet_edm](~/includes/adonet-edm-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4662b-106"> provides richer, optimized querying over the <xref:System.Data.DataSet>, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] enables you to directly query [!INCLUDE[ssNoVersion](~/includes/ssnoversion-md.md)] database schemas, and [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)] allows you to query an [!INCLUDE[adonet_edm](~/includes/adonet-edm-md.md)].</span></span>  
  
## <a name="linq-to-dataset"></a><span data-ttu-id="4662b-107">LINQ - DataSet</span><span class="sxs-lookup"><span data-stu-id="4662b-107">LINQ to DataSet</span></span>  
 <span data-ttu-id="4662b-108"><xref:System.Data.DataSet> En yaygın olarak kullanılan bileşenlerinde biri [!INCLUDE[vstecado](~/includes/vstecado-md.md)], ve olan bağlantısı kesilmiş programlama anahtar öğesi modeli [!INCLUDE[vstecado](~/includes/vstecado-md.md)] üzerine kurulmuştur.</span><span class="sxs-lookup"><span data-stu-id="4662b-108">The <xref:System.Data.DataSet> is one of the most widely used components in [!INCLUDE[vstecado](~/includes/vstecado-md.md)], and is a key element of the disconnected programming model that [!INCLUDE[vstecado](~/includes/vstecado-md.md)] is built on.</span></span> <span data-ttu-id="4662b-109">Bu teklifleriyle, ancak rağmen <xref:System.Data.DataSet> sorgu yeteneği sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="4662b-109">Despite this prominence, however, the <xref:System.Data.DataSet> has limited query capabilities.</span></span>  
  
 [!INCLUDE[linq_dataset](~/includes/linq-dataset-md.md)]<span data-ttu-id="4662b-110">daha zengin sorgu özelliklerini oluşturmanıza olanak sağlayan <xref:System.Data.DataSet> diğer birçok veri kaynakları için kullanılabilir aynı sorgu işlevini kullanarak.</span><span class="sxs-lookup"><span data-stu-id="4662b-110"> enables you to build richer query capabilities into <xref:System.Data.DataSet> by using the same query functionality that is available for many other data sources.</span></span>  
  
 <span data-ttu-id="4662b-111">Daha fazla bilgi için bkz: [LINQ-DataSet](../../../../framework/data/adonet/linq-to-dataset.md).</span><span class="sxs-lookup"><span data-stu-id="4662b-111">For more information, see [LINQ to DataSet](../../../../framework/data/adonet/linq-to-dataset.md).</span></span>  
  
## <a name="linq-to-sql"></a><span data-ttu-id="4662b-112">LINQ - SQL</span><span class="sxs-lookup"><span data-stu-id="4662b-112">LINQ to SQL</span></span>  
 [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)]<span data-ttu-id="4662b-113">İlişkisel veri nesneleri olarak yönetmek için bir çalışma zamanı altyapısı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4662b-113"> provides a run-time infrastructure for managing relational data as objects.</span></span> <span data-ttu-id="4662b-114">İçinde [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)], ilişkisel veritabanı veri modelinin Geliştirici programlama dilinde ifade nesne modeli eşlenir.</span><span class="sxs-lookup"><span data-stu-id="4662b-114">In [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)], the data model of a relational database is mapped to an object model expressed in the programming language of the developer.</span></span> <span data-ttu-id="4662b-115">Uygulama yürüttüğünüzde [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] SQL'e dil ile tümleşik sorgu nesne modelinde dönüşür ve yürütme için veritabanı gönderir.</span><span class="sxs-lookup"><span data-stu-id="4662b-115">When you execute the application, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] translates language-integrated queries in the object model into SQL and sends them to the database for execution.</span></span> <span data-ttu-id="4662b-116">Veritabanı sonuçları döndürdüğünde [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] geri yönetebilirsiniz nesnelerine çevirir.</span><span class="sxs-lookup"><span data-stu-id="4662b-116">When the database returns the results, [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)] translates them back into objects that you can manipulate.</span></span>  
  
 [!INCLUDE[vbtecdlinq](~/includes/vbtecdlinq-md.md)]<span data-ttu-id="4662b-117">nesne modelinde devralma ve saklı yordamları ve veritabanındaki kullanıcı tanımlı işlevler için destek içerir.</span><span class="sxs-lookup"><span data-stu-id="4662b-117"> includes support for stored procedures and user-defined functions in the database, and for inheritance in the object model.</span></span>  
  
 <span data-ttu-id="4662b-118">Daha fazla bilgi için bkz: [LINQ-SQL](https://msdn.microsoft.com/library/bb386976).</span><span class="sxs-lookup"><span data-stu-id="4662b-118">For more information, see [LINQ to SQL](https://msdn.microsoft.com/library/bb386976).</span></span>  
  
## <a name="linq-to-entities"></a><span data-ttu-id="4662b-119">LINQ - Varlıklar</span><span class="sxs-lookup"><span data-stu-id="4662b-119">LINQ to Entities</span></span>  
 <span data-ttu-id="4662b-120">Aracılığıyla [!INCLUDE[adonet_edm](~/includes/adonet-edm-md.md)], ilişkisel veri .NET ortamı nesneler olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4662b-120">Through the [!INCLUDE[adonet_edm](~/includes/adonet-edm-md.md)], relational data is exposed as objects in the .NET environment.</span></span> <span data-ttu-id="4662b-121">Bu katman için ideal bir hedef nesnesi haline getirir [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] desteği, iş mantığı oluşturmak için kullanılan dil veritabanından sorguları formüle yayınlamasına izin verme.</span><span class="sxs-lookup"><span data-stu-id="4662b-121">This makes the object layer an ideal target for [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] support, allowing developers to formulate queries against the database from the language used to build the business logic.</span></span> <span data-ttu-id="4662b-122">Bu özellik olarak bilinen [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4662b-122">This capability is known as [!INCLUDE[linq_entities](~/includes/linq-entities-md.md)].</span></span> <span data-ttu-id="4662b-123">Bkz: [LINQ to Entities](../../../../framework/data/adonet/ef/language-reference/linq-to-entities.md) daha fazla bilgi için.</span><span class="sxs-lookup"><span data-stu-id="4662b-123">See [LINQ to Entities](../../../../framework/data/adonet/ef/language-reference/linq-to-entities.md) for more information.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4662b-124">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4662b-124">See Also</span></span>  
 [<span data-ttu-id="4662b-125">LINQ ve ADO.NET</span><span class="sxs-lookup"><span data-stu-id="4662b-125">LINQ and ADO.NET</span></span>](http://msdn.microsoft.com/library/bf0c8f93-3ff7-49f3-8aed-f2b7ac938dec)  
 [<span data-ttu-id="4662b-126">Dil ile tümleşik sorgu (LINQ) (C#)</span><span class="sxs-lookup"><span data-stu-id="4662b-126">Language-Integrated Query (LINQ) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/index.md)