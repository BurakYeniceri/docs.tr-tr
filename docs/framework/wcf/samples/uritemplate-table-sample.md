---
title: "UriTemplate Tablo Örneği"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5dd1d38f-1989-4c64-820d-821f5a02216a
caps.latest.revision: "12"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: c4561590228531066014e69c03fcef0a6142cd70
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="uritemplate-table-sample"></a><span data-ttu-id="d8b2a-102">UriTemplate Tablo Örneği</span><span class="sxs-lookup"><span data-stu-id="d8b2a-102">UriTemplate Table Sample</span></span>
<span data-ttu-id="d8b2a-103"><xref:System.UriTemplateTable> Sınıfı, bir dizi birlikte çalışmaya yönelik bir sözlük benzeri ilişkilendirilebilir tablo yapısı sağlar `UriTemplate` örnekleri.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-103">The <xref:System.UriTemplateTable> class provides a dictionary-like associative table structure for working with a set of `UriTemplate` instances.</span></span> <span data-ttu-id="d8b2a-104">Belirli Tekdüzen Kaynak Tanımlayıcıları (URI'ler) verimli bir şekilde tablosundaki tüm şablonları karşı eşleştirilir ve eşleşen şablonuyla ilişkili veriler alınabilir.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-104">Specific Uniform Resource Identifiers (URIs) can be matched efficiently against all templates in the table, and data associated with the matched template can be retrieved.</span></span>  
  
 <span data-ttu-id="d8b2a-105">Bu örnek ile ilgili aşağıdaki temel kavramları göstermektedir `UriTemplateTable` sınıfı:</span><span class="sxs-lookup"><span data-stu-id="d8b2a-105">This sample demonstrates the following key concepts related to the `UriTemplateTable` class:</span></span>  
  
-   <span data-ttu-id="d8b2a-106">Örnek oluşturma söz dizimi bir `UriTemplateTable`.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-106">Syntax for instantiating a `UriTemplateTable`.</span></span>  
  
-   <span data-ttu-id="d8b2a-107">Doldurma bir `UriTemplateTable` bir anahtar/değer çifti kümesi ile.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-107">Populating a `UriTemplateTable` with a set of key/value pairs.</span></span>  
  
-   <span data-ttu-id="d8b2a-108">Tabloyu kullanarak karşı bir aday URI eşleşen <xref:System.UriTemplateTable.MatchSingle%2A>.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-108">Matching a candidate URI against the table using <xref:System.UriTemplateTable.MatchSingle%2A>.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="d8b2a-109">Ayarlamak için derleme ve örnek çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d8b2a-109">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="d8b2a-110">Çözüm C# veya Visual Basic .NET sürümünü oluşturmak için'ndaki yönergeleri izleyin [Windows Communication Foundation örnekleri derleme](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-110">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
2.  <span data-ttu-id="d8b2a-111">Tek veya çapraz makine yapılandırmada örneği çalıştırmak için'ndaki yönergeleri izleyin [Windows Communication Foundation örneklerini çalıştırma](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-111">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d8b2a-112">Örnekler, bilgisayarınızda yüklü.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-112">The samples may already be installed on your computer.</span></span> <span data-ttu-id="d8b2a-113">Devam etmeden önce aşağıdaki (varsayılan) dizin denetleyin.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-113">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="d8b2a-114">Bu dizin mevcut değilse, Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnek](http://go.microsoft.com/fwlink/?LinkId=150780) tüm indirmek için [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-114">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="d8b2a-115">Bu örnek aşağıdaki dizinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-115">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Web\UriTemplateTable`  
  
## <a name="see-also"></a><span data-ttu-id="d8b2a-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-116">See Also</span></span>  
 [<span data-ttu-id="d8b2a-117">UriTemplate tablosu dağıtıcısı</span><span class="sxs-lookup"><span data-stu-id="d8b2a-117">UriTemplate Table Dispatcher</span></span>](../../../../docs/framework/wcf/samples/uritemplate-table-dispatcher-sample.md)  
 [<span data-ttu-id="d8b2a-118">UriTemplate</span><span class="sxs-lookup"><span data-stu-id="d8b2a-118">UriTemplate</span></span>](../../../../docs/framework/wcf/samples/uritemplate-sample.md)