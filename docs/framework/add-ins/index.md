---
title: "Eklentiler ve Genişletilebilirlik"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- extensibility [.NET Framework], add-ins
- add-ins [.NET Framework]
- add-ins [.NET Framework], about
- hosts [.NET Framework], compared to add-ins
- .NET Framework, add-ins
- add-in pipeline [.NET Framework], about
- add-ins [.NET Framework], compared to hosts
- .NET Framework, extensibility
- versioning [.NET Framework], add-ins
ms.assetid: 8dd45b02-7218-40f9-857d-40d7b98b850b
caps.latest.revision: "42"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9bd09d0da70869ba193b414d8a2ce6c25cbb6b38
ms.sourcegitcommit: bbde43da655ae7bea1977f7af7345eb87bd7fd5f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2017
---
# <a name="add-ins-and-extensibility"></a><span data-ttu-id="e78fd-102">Eklentiler ve Genişletilebilirlik</span><span class="sxs-lookup"><span data-stu-id="e78fd-102">Add-ins and Extensibility</span></span>
<span data-ttu-id="e78fd-103"><a name="top"></a>Eklentiler genişletilmiş özellikler veya bir ana bilgisayar uygulaması için hizmetleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-103"><a name="top"></a> Add-ins provide extended features or services for a host application.</span></span> <span data-ttu-id="e78fd-104">[!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] Geliştiriciler eklentiler geliştirmek ve bunları kendi ana bilgisayar uygulamasında etkinleştirmek için kullanabileceğiniz bir programlama modelidir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-104">The [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] provides a programming model that developers can use to develop add-ins and activate them in their host application.</span></span> <span data-ttu-id="e78fd-105">Model bu konak ve eklenti arasındaki iletişim ardışık düzeni oluşturarak elde eder.</span><span class="sxs-lookup"><span data-stu-id="e78fd-105">The model achieves this by constructing a communication pipeline between the host and the add-in.</span></span> <span data-ttu-id="e78fd-106">Model türler kullanılarak uygulanır <xref:System.AddIn>, <xref:System.AddIn.Hosting>, <xref:System.AddIn.Pipeline>, ve <xref:System.AddIn.Contract> ad alanları.</span><span class="sxs-lookup"><span data-stu-id="e78fd-106">The model is implemented by using the types in the <xref:System.AddIn>, <xref:System.AddIn.Hosting>, <xref:System.AddIn.Pipeline>, and <xref:System.AddIn.Contract> namespaces.</span></span>  
  
 <span data-ttu-id="e78fd-107">Bu genel bakışta aşağıdaki bölümleri içerir:</span><span class="sxs-lookup"><span data-stu-id="e78fd-107">This overview contains the following sections:</span></span>  
  
-   [<span data-ttu-id="e78fd-108">Eklenti modeli</span><span class="sxs-lookup"><span data-stu-id="e78fd-108">Add-in Model</span></span>](#addin_model)  
  
-   [<span data-ttu-id="e78fd-109">Eklentiler ve ana bilgisayarlar arasında ayrım</span><span class="sxs-lookup"><span data-stu-id="e78fd-109">Distinguishing Between Add-ins and Hosts</span></span>](#distinguishing_between_addins_and_hosts)  
  
-   [<span data-ttu-id="e78fd-110">İlgili Konular</span><span class="sxs-lookup"><span data-stu-id="e78fd-110">Related Topics</span></span>](#related_topics)  
  
-   [<span data-ttu-id="e78fd-111">Başvuru</span><span class="sxs-lookup"><span data-stu-id="e78fd-111">Reference</span></span>](#reference)  
  
> [!NOTE]
>  <span data-ttu-id="e78fd-112">Konumundaki yapı ardışık'ın eklenti ek örnek kod ve müşteri teknolojisi önizlemeleri araçların bulabilirsiniz [CodePlex üzerinde Yönetilen Genişletilebilirlik ve eklenti Framework site](http://go.microsoft.com/fwlink/?LinkId=121190).</span><span class="sxs-lookup"><span data-stu-id="e78fd-112">You can find additional sample code, and customer technology previews of tools for building add-in pipelines, at the [Managed Extensibility and Add-In Framework site on CodePlex](http://go.microsoft.com/fwlink/?LinkId=121190).</span></span>  
  
<a name="addin_model"></a>   
## <a name="add-in-model"></a><span data-ttu-id="e78fd-113">Eklenti modeli</span><span class="sxs-lookup"><span data-stu-id="e78fd-113">Add-in Model</span></span>  
 <span data-ttu-id="e78fd-114">Eklenti ve ana bilgisayar arasındaki tüm iletişimi sorumlu olan eklenti ardışık düzeni (iletişim ardışık olarak da bilinir) oluşturan kesimleri bir dizi eklenti modeli oluşur.</span><span class="sxs-lookup"><span data-stu-id="e78fd-114">The add-in model consists of a series of segments that make up the add-in pipeline (also known as the communication pipeline), that is responsible for all communication between the add-in and the host.</span></span> <span data-ttu-id="e78fd-115">Ardışık düzen, eklenti ve ana bilgisayar arasında veri değişimi kesimleri simetrik iletişimi modelidir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-115">The pipeline is a symmetrical communication model of segments that exchange data between an add-in and its host.</span></span> <span data-ttu-id="e78fd-116">Bu kesimler konak ile eklenti geliştirme sürüm desteği gerekli Soyutlama Katmanı ve eklentisinin yalıtım sağlar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-116">Developing these segments between the host and the add-in provides the required layers of abstraction that support versioning and isolation of the add-in.</span></span>  
  
 <span data-ttu-id="e78fd-117">Aşağıdaki çizimde, ardışık düzen gösterir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-117">The following illustration shows the pipeline.</span></span>  
  
 <span data-ttu-id="e78fd-118">![Ekleme &#45; ardışık düzen modeli. ] (../../../docs/framework/add-ins/media/addin1.png "AddIn1")</span><span class="sxs-lookup"><span data-stu-id="e78fd-118">![Add&#45;in pipeline model.](../../../docs/framework/add-ins/media/addin1.png "AddIn1")</span></span>  
<span data-ttu-id="e78fd-119">Eklenti ardışık düzeni</span><span class="sxs-lookup"><span data-stu-id="e78fd-119">Add-in pipeline</span></span>  
  
 <span data-ttu-id="e78fd-120">Bu kesimler derlemelerde aynı uygulama etki alanında olması gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-120">The assemblies for these segments are not required to be in the same application domain.</span></span> <span data-ttu-id="e78fd-121">Kendi yeni uygulama etki alanına, var olan bir uygulama etki alanına veya ana bilgisayarın uygulama etki alanına bile bir eklenti yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e78fd-121">You can load an add-in into its own new application domain, into an existing application domain, or even into the host's application domain.</span></span> <span data-ttu-id="e78fd-122">Kaynakları ve güvenlik kapsamları paylaşmak eklentileri sağlayan aynı uygulama etki alanına, birden çok eklentileri yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-122">You can load multiple add-ins into the same application domain, which enables the add-ins to share resources and security contexts.</span></span>  
  
 <span data-ttu-id="e78fd-123">Eklenti modelini destekler ve önerir, konak ve yalıtım sınırı (remoting sınır olarak da bilinir) olarak adlandırılan eklentiyi arasında isteğe bağlı bir sınır.</span><span class="sxs-lookup"><span data-stu-id="e78fd-123">The add-in model supports, and recommends, an optional boundary between the host and the add-in, which is called the isolation boundary (also known as a remoting boundary).</span></span> <span data-ttu-id="e78fd-124">Bu sınır, bir uygulama etki alanı ya da işlem sınırı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-124">This boundary can be an application domain or process boundary.</span></span>  
  
 <span data-ttu-id="e78fd-125">Ardışık Düzen ortasında sözleşme segment ana bilgisayarın uygulama etki alanı ve eklentinin uygulama etki alanı yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-125">The contract segment in the middle of the pipeline is loaded into both the host's application domain and the add-in's application domain.</span></span> <span data-ttu-id="e78fd-126">Sanal yöntemler sözleşmesini tanımlayan, konak ve birbirleriyle türleri exchange eklentisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e78fd-126">The contract defines the virtual methods that the host and the add-in use to exchange types with each other.</span></span>  
  
 <span data-ttu-id="e78fd-127">Yalıtım sınırı iletilecek türleri sözleşmeleri veya seri hale getirilebilir türler olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e78fd-127">To pass through the isolation boundary, types must be either contracts or serializable types.</span></span> <span data-ttu-id="e78fd-128">Sözleşmeleri olmayan türler veya seri hale getirilebilir türler sözleşmelerine ardışık bağdaştırıcısı segmentlerinde dönüştürülmelidir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-128">Types that are not contracts or serializable types must be converted to contracts by the adapter segments in the pipeline.</span></span>  
  
 <span data-ttu-id="e78fd-129">Ardışık Düzen görünümü parçalarını soyut taban sınıfları veya ana bilgisayar ve eklenti anlaşma tarafından tanımlanan paylaştıkları, yöntemleri bir görünümünü sağlayan arabirimleri markalarıdır.</span><span class="sxs-lookup"><span data-stu-id="e78fd-129">The view segments of the pipeline are abstract base classes or interfaces that provide the host and the add-in with a view of the methods that they share, as defined by the contract.</span></span>  
  
 <span data-ttu-id="e78fd-130">Geliştirme hakkında daha fazla bilgi için kanal kesimleri, bkz: [ardışık düzen geliştirme](../../../docs/framework/add-ins/pipeline-development.md).</span><span class="sxs-lookup"><span data-stu-id="e78fd-130">For more information about developing pipeline segments, see [Pipeline Development](../../../docs/framework/add-ins/pipeline-development.md).</span></span>  
  
 <span data-ttu-id="e78fd-131">Aşağıdaki bölümlerde eklenti modeli özelliklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-131">The sections that follow describe the features of the add-in model.</span></span>  
  
### <a name="independent-versioning"></a><span data-ttu-id="e78fd-132">Bağımsız sürüm oluşturma</span><span class="sxs-lookup"><span data-stu-id="e78fd-132">Independent Versioning</span></span>  
 <span data-ttu-id="e78fd-133">Eklenti modeli, konakları ve sürüme eklentileri bağımsız olarak olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-133">The add-in model allows hosts and add-ins to version independently.</span></span> <span data-ttu-id="e78fd-134">Sonuç olarak, eklenti modeli aşağıdaki senaryolara olanak sağlar:</span><span class="sxs-lookup"><span data-stu-id="e78fd-134">As a result, the add-in model enables the following scenarios:</span></span>  
  
-   <span data-ttu-id="e78fd-135">Bir bağdaştırıcı oluşturma ana bilgisayarı, önceki bir sürümü için yerleşik bir eklenti kullanmak bir konak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-135">Creating an adapter that enables a host to use an add-in built for a previous version of the host.</span></span>  
  
-   <span data-ttu-id="e78fd-136">Bir bağdaştırıcı oluşturma konak daha sonraki bir sürümü için yerleşik bir eklenti kullanmak bir konak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-136">Creating an adapter that enables a host to use an add-in built for a later version of the host.</span></span>  
  
-   <span data-ttu-id="e78fd-137">Eklentiler kullanmak bir konak sağlayan bir bağdaştırıcısı oluşturmak için farklı bir konak yerleşiktir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-137">Creating an adapter that enables a host to use add-ins built for a different host.</span></span>  
  
### <a name="discovery-and-activation"></a><span data-ttu-id="e78fd-138">Bulma ve etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e78fd-138">Discovery and Activation</span></span>  
 <span data-ttu-id="e78fd-139">Bir eklenti, bir bilgi deposundan bulunan eklentileri temsil eden bir koleksiyon uygulamasından bir belirteç kullanarak etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e78fd-139">You can activate an add-in by using a token from a collection that represents the add-ins found from an information store.</span></span> <span data-ttu-id="e78fd-140">Eklentiler Eklenti ana bilgisayarın görünümü tanımlayan tür için arama yaparak bulunamadı.</span><span class="sxs-lookup"><span data-stu-id="e78fd-140">Add-ins are found by searching for the type that defines the host's view of the add-in.</span></span> <span data-ttu-id="e78fd-141">Bir özel eklenti tarafından eklenti tanımlayan tür bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e78fd-141">You can also find a specific add-in by the type that defines the add-in.</span></span> <span data-ttu-id="e78fd-142">Bilgi deposunu iki önbellek dosyaları içerir: ardışık düzen mağazaya ve eklenti.</span><span class="sxs-lookup"><span data-stu-id="e78fd-142">The information store consists of two cache files: the pipeline store and the add-in store.</span></span>  
  
 <span data-ttu-id="e78fd-143">Güncelleştirme ve bilgi deposunu yeniden oluşturma hakkında daha fazla bilgi için bkz: [eklenti bulma](http://msdn.microsoft.com/en-us/5d268dde-11df-4c4d-a022-f58d88bbc421).</span><span class="sxs-lookup"><span data-stu-id="e78fd-143">For information about updating and rebuilding the information store, see [Add-in Discovery](http://msdn.microsoft.com/en-us/5d268dde-11df-4c4d-a022-f58d88bbc421).</span></span> <span data-ttu-id="e78fd-144">Eklentiler etkinleştirme hakkında daha fazla bilgi için bkz: [eklentisini etkinleştirme](http://msdn.microsoft.com/en-us/bedcbcdf-5964-4215-b5f3-3299798b2b3f) ve [nasıl yapılır: farklı yalıtım ve güvenlik ile eklentileri etkinleştirmek](http://msdn.microsoft.com/en-us/7afe7ec8-5158-4350-9119-5df0ecab8aa5).</span><span class="sxs-lookup"><span data-stu-id="e78fd-144">For information about activating add-ins, see [Add-in Activation](http://msdn.microsoft.com/en-us/bedcbcdf-5964-4215-b5f3-3299798b2b3f) and [How to: Activate Add-ins with Different Isolation and Security](http://msdn.microsoft.com/en-us/7afe7ec8-5158-4350-9119-5df0ecab8aa5).</span></span>  
  
### <a name="isolation-levels-and-external-processes"></a><span data-ttu-id="e78fd-145">Yalıtım düzeylerinde ve dış işlemleri</span><span class="sxs-lookup"><span data-stu-id="e78fd-145">Isolation Levels and External Processes</span></span>  
 <span data-ttu-id="e78fd-146">Eklenti modeli birkaç eklentileri veya ek bileşeni ve ana bilgisayar arasında yalıtım düzeyini destekler. Az yalıtılmış başlayarak, bu düzeylerin aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="e78fd-146">The add-in model supports several levels of isolation between an add-in and its host or between add-ins. Starting from the least isolated, these levels are as follows:</span></span>  
  
-   <span data-ttu-id="e78fd-147">Eklenti aynı uygulama etki alanı konağı olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="e78fd-147">The add-in runs in the same application domain as the host.</span></span> <span data-ttu-id="e78fd-148">Farklı uygulama etki alanları kullandığınızda aldığınız kaldırma yetenekleri ve yalıtım kaybetmek çünkü bu önerilmez.</span><span class="sxs-lookup"><span data-stu-id="e78fd-148">This is not recommended because you lose the isolation and unloading capabilities that you get when you use different application domains.</span></span>  
  
-   <span data-ttu-id="e78fd-149">Birden çok eklentiler, ana bilgisayar tarafından kullanılan uygulama etki alanından farklı aynı uygulama etki alanına yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-149">Multiple add-ins are loaded into the same application domain that is different from the application domain used by the host.</span></span>  
  
-   <span data-ttu-id="e78fd-150">Her eklenti yalnızca kendi uygulama etki alanına yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-150">Each add-in is loaded exclusively into its own application domain.</span></span> <span data-ttu-id="e78fd-151">En yaygın yalıtım düzeyini budur.</span><span class="sxs-lookup"><span data-stu-id="e78fd-151">This is the most common level of isolation.</span></span>  
  
-   <span data-ttu-id="e78fd-152">Birden çok eklentiler bir dış işlem aynı uygulama etki alanına yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-152">Multiple add-ins are loaded into the same application domain in an external process.</span></span>  
  
-   <span data-ttu-id="e78fd-153">Her eklenti özel olarak bir dış işlem kendi uygulama etki alanına yüklenir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-153">Each add-in is loaded exclusively into its own application domain in an external process.</span></span> <span data-ttu-id="e78fd-154">Bu en yalıtılmış bir senaryodur.</span><span class="sxs-lookup"><span data-stu-id="e78fd-154">This is the most isolated scenario.</span></span>  
  
 <span data-ttu-id="e78fd-155">Dış işlemlere kullanma hakkında daha fazla bilgi için bkz: [nasıl yapılır: farklı yalıtım ve güvenlik ile eklentileri etkinleştirme](http://msdn.microsoft.com/en-us/7afe7ec8-5158-4350-9119-5df0ecab8aa5).</span><span class="sxs-lookup"><span data-stu-id="e78fd-155">For more information about using external processes, see [How to: Activate Add-ins with Different Isolation and Security](http://msdn.microsoft.com/en-us/7afe7ec8-5158-4350-9119-5df0ecab8aa5).</span></span>  
  
### <a name="lifetime-management"></a><span data-ttu-id="e78fd-156">Ömür Yönetimi</span><span class="sxs-lookup"><span data-stu-id="e78fd-156">Lifetime Management</span></span>  
 <span data-ttu-id="e78fd-157">Uygulama etki alanı ve işlem sınırları eklenti modeli yayılan olduğundan atık toplama kendisi tarafından serbest bırakır ve nesneleri geri kazanmak için yeterli değil.</span><span class="sxs-lookup"><span data-stu-id="e78fd-157">Because the add-in model spans application domain and process boundaries, garbage collection by itself is not sufficient to release and reclaim objects.</span></span> <span data-ttu-id="e78fd-158">Eklenti modeli belirteçleri ve başvuru sayımı kullanır bir yaşam süresi management mekanizma sağlar ve genellikle ek programlama gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="e78fd-158">The add-in model provides a lifetime management mechanism that uses tokens and reference counting, and usually does not require additional programming.</span></span> <span data-ttu-id="e78fd-159">Daha fazla bilgi için bkz: [yaşam süresi Management](http://msdn.microsoft.com/en-us/57a9c87e-394c-4fef-89f2-aa4223a2aeb5).</span><span class="sxs-lookup"><span data-stu-id="e78fd-159">For more information, see [Lifetime Management](http://msdn.microsoft.com/en-us/57a9c87e-394c-4fef-89f2-aa4223a2aeb5).</span></span>  
  
 [<span data-ttu-id="e78fd-160">Başa dön</span><span class="sxs-lookup"><span data-stu-id="e78fd-160">Back to top</span></span>](#top)  
  
<a name="distinguishing_between_addins_and_hosts"></a>   
## <a name="distinguishing-between-add-ins-and-hosts"></a><span data-ttu-id="e78fd-161">Eklentiler ve ana bilgisayarlar arasında ayrım</span><span class="sxs-lookup"><span data-stu-id="e78fd-161">Distinguishing Between Add-ins and Hosts</span></span>  
 <span data-ttu-id="e78fd-162">Bir eklenti ve bir ana bilgisayar arasındaki farkı yalnızca ana bilgisayarın bir eklenti etkinleştiren olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="e78fd-162">The difference between an add-in and a host is merely that the host is the one that activates the add-in.</span></span> <span data-ttu-id="e78fd-163">Konak bir sözcük işleme uygulama ve onun yazım denetleyicileri gibi iki daha büyük olabilir; veya konağın bir medya oynatıcı katıştırır bir anlık ileti sistemi istemcisi gibi iki daha küçük olabilir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-163">The host can be the larger of the two, such as a word processing application and its spell checkers; or the host can be the smaller of the two, such as an instant messaging client that embeds a media player.</span></span> <span data-ttu-id="e78fd-164">Eklenti modeli eklentileri hem istemci hem de sunucu senaryolarda destekler.</span><span class="sxs-lookup"><span data-stu-id="e78fd-164">The add-in model supports add-ins in both client and server scenarios.</span></span> <span data-ttu-id="e78fd-165">Posta sunucusu virüs taraması, istenmeyen posta filtreleri ve IP koruması sağlama eklentiler sunucu eklentileri örneklerindendir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-165">Examples of server add-ins include add-ins that provide mail servers with virus scanning, spam filters, and IP protection.</span></span> <span data-ttu-id="e78fd-166">İstemci eklenti örnekleri başvuru eklentiler için sözcük işlemci, grafik programları ve oyunları ve virüs yerel e-posta istemcileri için tarama için özel özellikler içerir.</span><span class="sxs-lookup"><span data-stu-id="e78fd-166">Client add-in examples include reference add-ins for word processors, specialized features for graphics programs and games, and virus scanning for local e-mail clients.</span></span>  
  
 [<span data-ttu-id="e78fd-167">Başa dön</span><span class="sxs-lookup"><span data-stu-id="e78fd-167">Back to top</span></span>](#top)  
  
<a name="related_topics"></a>   
## <a name="related-topics"></a><span data-ttu-id="e78fd-168">İlgili Konular</span><span class="sxs-lookup"><span data-stu-id="e78fd-168">Related Topics</span></span>  
  
|<span data-ttu-id="e78fd-169">Başlık</span><span class="sxs-lookup"><span data-stu-id="e78fd-169">Title</span></span>|<span data-ttu-id="e78fd-170">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e78fd-170">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="e78fd-171">Ardışık Düzen geliştirme</span><span class="sxs-lookup"><span data-stu-id="e78fd-171">Pipeline Development</span></span>](../../../docs/framework/add-ins/pipeline-development.md)|<span data-ttu-id="e78fd-172">Eklenti konak uygulamaya bölümlerinin iletişim kanalı açıklar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-172">Describes the communication pipeline of segments from the host application to the add-in.</span></span> <span data-ttu-id="e78fd-173">Kod örnekleri ardışık düzenini oluşturmak ve ardışık düzeninde kesimleri dağıtmak anlatan izlenecek konularda sağlar [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)].</span><span class="sxs-lookup"><span data-stu-id="e78fd-173">Provides code examples in walkthrough topics that describe how to construct the pipeline and how to deploy segments to the pipeline in [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)].</span></span>|  
|[<span data-ttu-id="e78fd-174">Uygulama etki alanları ve derlemeler</span><span class="sxs-lookup"><span data-stu-id="e78fd-174">Application Domains and Assemblies</span></span>](http://msdn.microsoft.com/en-us/433b04ae-4ba8-4849-9dbd-79194f240346)|<span data-ttu-id="e78fd-175">Güvenlik, güvenilirlik ve sürüm oluşturma için bir yalıtım sınırı sağlayan uygulama etki alanları ve derlemeler arasındaki ilişkiyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="e78fd-175">Describes the relationship between application domains, which provide an isolation boundary for security, reliability, and versioning, and assemblies.</span></span>|  
  
 [<span data-ttu-id="e78fd-176">Başa dön</span><span class="sxs-lookup"><span data-stu-id="e78fd-176">Back to top</span></span>](#top)  
  
<a name="reference"></a>   
## <a name="reference"></a><span data-ttu-id="e78fd-177">Başvuru</span><span class="sxs-lookup"><span data-stu-id="e78fd-177">Reference</span></span>  
 <xref:System.AddIn?displayProperty=nameWithType>  
  
 <xref:System.AddIn.Contract?displayProperty=nameWithType>  
  
 <xref:System.AddIn.Hosting?displayProperty=nameWithType>  
  
 <xref:System.AddIn.Pipeline?displayProperty=nameWithType>  
  
 [<span data-ttu-id="e78fd-178">Başa dön</span><span class="sxs-lookup"><span data-stu-id="e78fd-178">Back to top</span></span>](#top)