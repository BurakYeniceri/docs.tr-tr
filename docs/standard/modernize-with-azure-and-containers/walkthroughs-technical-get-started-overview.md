---
title: İzlenecek yollar ve teknik başlatılan özeti
description: Azure Bulut ve Windows kapsayıcıları varolan .NET uygulamaları modernize | İzlenecek yollar ve teknik başlatılan özeti
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 27de9d1c5475855a22f2d8a3518982605277f6d9
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2018
---
# <a name="walkthroughs-and-technical-get-started-overview"></a><span data-ttu-id="7b4b8-103">İzlenecek yollar ve teknik başlatılan özeti</span><span class="sxs-lookup"><span data-stu-id="7b4b8-103">Walkthroughs and technical get started overview</span></span>

<span data-ttu-id="7b4b8-104">Bu e-kitap boyutunu sınırlamak için ek teknik belgeler ve tam izlenecek yollar GitHub deposunda kullanılabilir yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-104">To limit the size of this e-book, additional technical documentation and the full walkthroughs were made available in a GitHub repository.</span></span> <span data-ttu-id="7b4b8-105">Bu bölümde açıklanan izlenecek yollar çevrimiçi bir dizi adım adım kurulum Windows kapsayıcıları ve Azure dağıtımına dayalı birden çok ortamlarının kapsar.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-105">The online series of walkthroughs that is described in this chapter covers the step-by-step setup of the multiple environments that are based on Windows Containers, and deployment to Azure.</span></span>

<span data-ttu-id="7b4b8-106">Aşağıdaki bölümlerde ne her gözden geçirme, hedefler ve üst düzey görme hakkında ve ilgili olan görevleri diyagramı sağlar açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-106">The following sections explain what each walkthrough is about, its objectives and high-level vision, and provides a diagram of the tasks that are involved.</span></span> <span data-ttu-id="7b4b8-107">İzlenecek yollar kendilerini alabilirsiniz içinde *eShopModernizing* uygulamaları GitHub deposuna wiki adresindeki [ https://github.com/dotnet-architecture/eShopModernizing/wiki ](https://github.com/dotnet-architecture/eShopModernizing/wiki).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-107">You can get the walkthroughs themselves in the *eShopModernizing* apps GitHub repo wiki at [https://github.com/dotnet-architecture/eShopModernizing/wiki](https://github.com/dotnet-architecture/eShopModernizing/wiki).</span></span>

## <a name="technical-walkthrough-list"></a><span data-ttu-id="7b4b8-108">Teknik kılavuz listesi</span><span class="sxs-lookup"><span data-stu-id="7b4b8-108">Technical walkthrough list</span></span>

<span data-ttu-id="7b4b8-109">Aşağıdaki get-started izlenecek kaldırın ve kapsayıcılar kullanarak kaydırma ve Azure içinde birden çok dağıtım seçenekleri kullanarak Taşı örnek uygulamaları için tutarlı ve kapsamlı teknik Kılavuzu sağlamak.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-109">The following get-started walkthroughs provide consistent and comprehensive technical guidance for sample apps that you can lift and shift by using containers, and then move by using multiple deployment choices in Azure.</span></span>

<span data-ttu-id="7b4b8-110">Her biri aşağıdaki izlenecek github'da kullanılabilir olan yeni örnek eShopLegacy ve eShopModernizing uygulamaları kullanır [ https://github.com/dotnet-architecture/eShopModernizing ](https://github.com/dotnet-architecture/eShopModernizing).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-110">Each of the following walkthroughs uses the new sample eShopLegacy and eShopModernizing apps, which are available on GitHub at [https://github.com/dotnet-architecture/eShopModernizing](https://github.com/dotnet-architecture/eShopModernizing).</span></span>

- <span data-ttu-id="7b4b8-111">**Elektronik Mağaza eski uygulamalara (modernize için temel) turu**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-111">**Tour of eShop legacy apps (baseline apps to modernize)**</span></span>

- <span data-ttu-id="7b4b8-112">**Mevcut ASP.NET web uygulamalarınızı (WebForms & MVC) ile Windows kapsayıcıları containerize**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-112">**Containerize your existing ASP.NET web apps (WebForms & MVC) with Windows Containers**</span></span>

- <span data-ttu-id="7b4b8-113">**Windows kapsayıcılarla mevcut WCF hizmetlerini (N katmanlı uygulamalar) containerize**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-113">**Containerize your existing WCF services (N-Tier apps) with Windows Containers**</span></span>

- <span data-ttu-id="7b4b8-114">**Azure VM'ler kapsayıcıları tabanlı Windows uygulamanızı dağıtma**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-114">**Deploy your Windows Containers-based app to Azure VMs**</span></span>

- <span data-ttu-id="7b4b8-115">**Azure kapsayıcı Hizmeti'nde Kubernetes Windows kapsayıcıları tabanlı uygulamalarınızı dağıtma**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-115">**Deploy your Windows Containers-based apps to Kubernetes in Azure Container Service**</span></span>

- <span data-ttu-id="7b4b8-116">**Azure Service Fabric Windows kapsayıcıları tabanlı uygulamalarınızı dağıtma**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-116">**Deploy your Windows Containers-based apps to Azure Service Fabric**</span></span>


## <a name="walkthrough-1-tour-of-eshop-legacy-apps"></a><span data-ttu-id="7b4b8-117">Gözden geçirme 1: Elektronik Mağaza eski uygulamaları turu</span><span class="sxs-lookup"><span data-stu-id="7b4b8-117">Walkthrough 1: Tour of eShop legacy apps</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="7b4b8-118">Teknik kılavuz kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="7b4b8-118">Technical walkthrough availability</span></span>

<span data-ttu-id="7b4b8-119">Tam teknik Kılavuzu eShopModernizing GitHub deposuna wiki kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-119">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[<span data-ttu-id="7b4b8-120">eShopModernizing wiki izlenecek yollar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-120">eShopModernizing wiki walkthroughs</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki)


### <a name="overview"></a><span data-ttu-id="7b4b8-121">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b4b8-121">Overview</span></span>

<span data-ttu-id="7b4b8-122">Bu kılavuzda, üç örnek eski uygulamalar ilk uyarlamasını keşfedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-122">In this walkthrough, you can explore the initial implementation of three sample legacy applications.</span></span> <span data-ttu-id="7b4b8-123">İlk iki örnek web uygulamaları tek yapılı bir mimariye sahip ve klasik ASP.NET kullanılarak oluşturulmuş.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-123">The first two sample web apps have a monolithic architecture, and were created by using classic ASP.NET.</span></span> <span data-ttu-id="7b4b8-124">ASP.NET ile tabanlı bir uygulamayı 4.x MVC; İkinci uygulama ASP.NET 4.x Web Forms üzerinde temel alır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-124">One application is based on ASP.NET 4.x MVC; the second application is based on ASP.NET 4.x Web Forms.</span></span> <span data-ttu-id="7b4b8-125">İstemci WinForms uygulama ve sunucu tarafı tarafından oluşturulan 3 katmanlı uygulama üçüncü uygulamadır [Windows Communication Foundation (WCF)](../../framework/wcf/whats-wcf.md) hizmet.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-125">The third app is a 3-Tier app composed by a client WinForms app and a server-side [Windows Communication Foundation (WCF)](../../framework/wcf/whats-wcf.md) service.</span></span>

<span data-ttu-id="7b4b8-126">Bu uygulamalar kullanılabilir [eShopModernizing GitHub deposuna](https://github.com/dotnet-architecture/eShopModernizing).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-126">All these applications are available at the [eShopModernizing GitHub repo](https://github.com/dotnet-architecture/eShopModernizing).</span></span>

### <a name="goals"></a><span data-ttu-id="7b4b8-127">Hedefleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-127">Goals</span></span>

<span data-ttu-id="7b4b8-128">Asıl amacı, bu kılavuzda yalnızca bu uygulamalarla ve kendi kod ve yapılandırma hakkında bilgi edinmek için ' dir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-128">The main goal of this walkthrough is simply to get familiar with these apps, and with their code and configuration.</span></span> <span data-ttu-id="7b4b8-129">Böylece oluşturmak ve test amacıyla SQL veritabanı kullanmadan sahte veriler kullanmak uygulamaları yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-129">You can configure the apps so that they generate and use mock data, without using the SQL database, for testing purposes.</span></span> <span data-ttu-id="7b4b8-130">Bu isteğe bağlı yapılandırma bağımlılık ekleme, ayrılmış bir biçimde temel alır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-130">This optional config is based on dependency injection, in a decoupled way.</span></span>

### <a name="scenario-1-aspnet-web-apps"></a><span data-ttu-id="7b4b8-131">Senaryo 1: ASP.NET Web uygulamaları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-131">Scenario 1: ASP.NET Web apps</span></span>

<span data-ttu-id="7b4b8-132">Aşağıdaki şekilde özgün eski ASP.NET web uygulamaları basit bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-132">The figure below shows the simple scenario of the original legacy ASP.NET web applications.</span></span>

> ![Özgün eski ASP.NET web uygulamalarının basit mimarisi senaryosu](./media/image5-1.png)
>

<span data-ttu-id="7b4b8-134">Bir iş etki alanı açısından bakıldığında, hem uygulamalar aynı katalog yönetimi özellikleri sunar.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-134">From a business domain perspective, both apps offer the same catalog management features.</span></span> <span data-ttu-id="7b4b8-135">Elektronik Mağaza Kurumsal ekibi üyelerinin uygulamayı görüntülemek ve ürün kataloğu düzenlemek için kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-135">Members of the eShop enterprise team would use the app to view and edit the product catalog.</span></span> 

<span data-ttu-id="7b4b8-136">Sonraki şekilde, ilk uygulama ekran görüntüleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-136">The next figure shows the initial app screenshots.</span></span>

![ASP.NET MVC ve ASP.NET Web Forms uygulamaları (varolan eski teknolojileri)](./media/image5-2.png)

<span data-ttu-id="7b4b8-138">Bağımlılıklar ASP.NET 4.x veya önceki sürümleri (veya MVC için Web formları için) anlamına gelir kodu tam olarak ASP.NET Core MVC kullanarak yeniden yazılmıştır sürece bu uygulamaları .NET Core üzerinde çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-138">Dependencies in ASP.NET 4.x or earlier versions (either for MVC or for Web Forms) means that these applications won’t run on .NET Core unless the code is fully rewritten by using ASP.NET Core MVC.</span></span> 

### <a name="scenario-2-wcf-service-and-winforms-client-app-3-tier-app"></a><span data-ttu-id="7b4b8-139">Senaryo 2: WCF hizmeti ve WinForms istemci uygulaması (3 katmanlı uygulama)</span><span class="sxs-lookup"><span data-stu-id="7b4b8-139">Scenario 2: WCF service and WinForms client app (3-Tier app)</span></span>

<span data-ttu-id="7b4b8-140">Aşağıdaki şekilde özgün 3 katmanlı eski uygulamayı basit bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-140">The figure below shows the simple scenario of the original 3-Tier legacy application.</span></span>

> ![Bir WCF Hizmeti özgün eski 3 katmanlı uygulama ve bir WinForms istemci uygulaması basit mimarisi senaryosu](./media/image5-1.5.png)
>

### <a name="benefits"></a><span data-ttu-id="7b4b8-142">Yararları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-142">Benefits</span></span>

<span data-ttu-id="7b4b8-143">Bu kılavuzda yararları basit: yalnızca ilk uygulamaları ve kod ile hakkında bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-143">The benefits of this walkthrough are simple: Just get familiar with the code and initial apps.</span></span>

### <a name="next-steps"></a><span data-ttu-id="7b4b8-144">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-144">Next steps</span></span>

<span data-ttu-id="7b4b8-145">Bu içerik daha kapsamlı GitHub Wiki'de keşfedin:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-145">Explore this content more in-depth on the GitHub wiki:</span></span>

  - [<span data-ttu-id="7b4b8-146">ASP.NET MVC taban tur ve Web Forms "eski" uygulamalar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-146">Tour on the baseline ASP.NET MVC and Web Forms “legacy” apps</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/01.-Tour-on-the-ASP.NET-MVC-and-WebForms-apps-implementation-code)
  - [<span data-ttu-id="7b4b8-147">Temel WCF hizmeti ve WinForms (Katman 3) "eski" uygulama turu</span><span class="sxs-lookup"><span data-stu-id="7b4b8-147">Tour on the baseline WCF service and WinForms (3-Tier) “legacy” app</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/21.-Tour-on-the-WCF-service-and-WinForms-apps)


## <a name="walkthrough-2-containerize-your-existing-net-applications-with-windows-containers"></a><span data-ttu-id="7b4b8-148">İzlenecek yol: 2: var olan .NET uygulamalarınız Windows kapsayıcılarla Containerize</span><span class="sxs-lookup"><span data-stu-id="7b4b8-148">Walkthrough 2: Containerize your existing .NET applications with Windows Containers</span></span>

### <a name="overview"></a><span data-ttu-id="7b4b8-149">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b4b8-149">Overview</span></span>

<span data-ttu-id="7b4b8-150">MVC, Web Forms veya WCF, üretim, geliştirme ve test ortamları için temel gelenler varolan .NET uygulamalarının dağıtımını iyileştirmek için Windows kapsayıcıları kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-150">Use Windows Containers to improve deployment of existing .NET applications, like those based on MVC, Web Forms, or WCF, to production, development, and test environments.</span></span>

### <a name="goals"></a><span data-ttu-id="7b4b8-151">Hedefleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-151">Goals</span></span>

<span data-ttu-id="7b4b8-152">Bu kılavuzun amacı, var olan bir .NET Framework uygulamasını containerizing için çeşitli seçenekler göstermektir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-152">The goal of this walkthrough is to show you several options for containerizing an existing .NET Framework application.</span></span> <span data-ttu-id="7b4b8-153">Şunları yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-153">You can:</span></span>

- <span data-ttu-id="7b4b8-154">Uygulamanızı kullanarak containerize [Docker için Visual Studio 2017 Araçları](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 veya sonraki sürümler).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-154">Containerize your application by using [Visual Studio 2017 Tools for Docker](/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker) (Visual Studio 2017 or later versions).</span></span>

- <span data-ttu-id="7b4b8-155">El ile ekleyerek uygulamanızı containerize bir [Dockerfile](https://docs.docker.com/engine/reference/builder/)ve ardından kullanarak [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-155">Containerize your application by manually adding a [Dockerfile](https://docs.docker.com/engine/reference/builder/), and then using the [Docker CLI](https://docs.docker.com/engine/reference/commandline/cli/).</span></span>

- <span data-ttu-id="7b4b8-156">Uygulamanızı kullanarak containerize [Img2Docker](https://github.com/docker/communitytools-image2docker-win) Aracı (Docker açık kaynak aracından).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-156">Containerize your application by using the [Img2Docker](https://github.com/docker/communitytools-image2docker-win) tool (an open-source tool from Docker).</span></span>

<span data-ttu-id="7b4b8-157">Bu kılavuz Docker yaklaşım için Visual Studio 2017 araçları odaklanır, ancak diğer iki yaklaşım Dockerfiles kullanarak in regard to oldukça benzer.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-157">This walkthrough focuses on the Visual Studio 2017 Tools for Docker approach, but the other two approaches are fairly similar in regard to using Dockerfiles.</span></span>

### <a name="scenario-1-containerized-aspnet-web-apps"></a><span data-ttu-id="7b4b8-158">Senaryo 1: Kapsayıcılı ASP.NET web uygulamaları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-158">Scenario 1: Containerized ASP.NET web apps</span></span>

<span data-ttu-id="7b4b8-159">Aşağıdaki şekilde kapsayıcılı Elektronik Mağaza eski web apps uygulamaları senaryosu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-159">Figure below shows the scenario for containerized eShop legacy web apps applications.</span></span>

> ![ASP.NET uygulamaları geliştirme ortamında kapsayıcılı Basitleştirilmiş mimarisi diyagramı](./media/image5-3.png)
>


### <a name="scenario-2-containerized-wcf-service"></a><span data-ttu-id="7b4b8-161">Senaryo 2: Kapsayıcılı WCF Hizmeti</span><span class="sxs-lookup"><span data-stu-id="7b4b8-161">Scenario 2: Containerized WCF service</span></span>

<span data-ttu-id="7b4b8-162">Aşağıdaki şekilde kapsayıcılı WCF Hizmeti ile 3 katmanlı uygulama senaryosu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-162">Figure below shows the scenario for a 3-Tier app with a containerized WCF service.</span></span> 

> ![Basitleştirilmiş bir geliştirme ortamı kapsayıcılı WCF hizmeti mimarisi diyagramı](./media/image5-3.5.png)
>

### <a name="benefits"></a><span data-ttu-id="7b4b8-164">Yararları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-164">Benefits</span></span>

<span data-ttu-id="7b4b8-165">Bir kapsayıcıda tek yapılı uygulamanızı çalıştırmanın avantajı vardır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-165">There are advantages to running your monolithic application in a container.</span></span> <span data-ttu-id="7b4b8-166">İlk olarak, uygulama için bir görüntü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-166">First, you create an image for the application.</span></span> <span data-ttu-id="7b4b8-167">Bu noktadan itibaren her dağıtım aynı ortamda çalışır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-167">From that point on, every deployment runs in the same environment.</span></span> <span data-ttu-id="7b4b8-168">Her kapsayıcı aynı işletim sistemi sürümünü kullanır, yüklü bağımlılıkları aynı sürümü, aynı .NET framework sürümünü kullanır ve aynı işlemi kullanılarak oluşturulmuş.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-168">Every container uses the same OS version, has the same version of dependencies installed, uses the same .NET framework version, and is built by using the same process.</span></span> <span data-ttu-id="7b4b8-169">Temel olarak, uygulamanızın bağımlılıkları Docker görüntüsünü kullanarak denetler.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-169">Basically, you control the dependencies of your application by using a Docker image.</span></span> <span data-ttu-id="7b4b8-170">Kapsayıcılar dağıttığınızda bağımlılıkları uygulamayla ilerler.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-170">The dependencies travel with the application when you deploy the containers.</span></span>

<span data-ttu-id="7b4b8-171">Ek bir faydası, geliştiricilerin uygulama Windows kapsayıcıları tarafından sağlanan tutarlı ortamında çalıştırabilirsiniz ' dir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-171">An additional benefit is that developers can run the application in the consistent environment that's provided by Windows Containers.</span></span> <span data-ttu-id="7b4b8-172">Yalnızca belirli sürümler ile görünür sorunları bir hazırlık veya üretim ortamında görünmesini yerine hemen anlaþýlmaz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-172">Issues that appear only with certain versions can be spotted immediately, instead of surfacing in a staging or production environment.</span></span> <span data-ttu-id="7b4b8-173">Kapsayıcı uygulamaları çalıştırdığınızda, geliştirme ortamları ve geliştirme ekibi üyeleri tarafından kullanılan farklılıkları daha az önemli.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-173">Differences in development environments used by members of the development team matter less when applications run in containers.</span></span>

<span data-ttu-id="7b4b8-174">Kapsayıcılı uygulamaları daha düz genişleme eğri de vardır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-174">Containerized applications also have a flatter scale-out curve.</span></span> <span data-ttu-id="7b4b8-175">Kapsayıcılı uygulamaları, daha fazla uygulama ve hizmet örnekleri (kapsayıcılarında dayanarak) sahip bir VM veya fiziksel makine makine başına normal uygulama dağıtımı ile karşılaştırıldığında olanak verir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-175">Containerized apps enable you to have more application and service instances (based on containers) in a VM or physical machine compared to regular application deployments per machine.</span></span> <span data-ttu-id="7b4b8-176">Bu daha yüksek yoğunluk ve daha az gerekli dönüşür özellikle orchestrators Kubernetes veya Service Fabric gibi kullandığınızda kaynakları.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-176">This translates to higher density and fewer required resources, especially when you use orchestrators like Kubernetes or Service Fabric.</span></span>

<span data-ttu-id="7b4b8-177">İdeal durumlarda verilerin kapsayıcıyla taşınmasını uygulama kodu herhangi bir değişiklik yapmadan gerektirmez (C\#).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-177">Containerization, in ideal situations, does not require making any changes to the application code (C\#).</span></span> <span data-ttu-id="7b4b8-178">Çoğu senaryoda, Docker dağıtım meta veri dosyaları (Dockerfiles ve Docker Compose) yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-178">In most scenarios, you just need the Docker deployment metadata files (Dockerfiles and Docker Compose files).</span></span>

### <a name="next-steps"></a><span data-ttu-id="7b4b8-179">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-179">Next steps</span></span>

<span data-ttu-id="7b4b8-180">Bu içerik daha kapsamlı GitHub Wiki'de keşfedin:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-180">Explore this content more in-depth on the GitHub wiki:</span></span>

  - [<span data-ttu-id="7b4b8-181">.NET Framework web uygulamalarını Windows kapsayıcıları ve Docker ile containerize nasıl</span><span class="sxs-lookup"><span data-stu-id="7b4b8-181">How to containerize the .NET Framework web apps with Windows Containers and Docker</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/02.-How-to-containerize-the-.NET-Framework-web-apps-with-Windows-Containers-and-Docker)
  - [<span data-ttu-id="7b4b8-182">Bir WCF hizmetine Docker desteği ekleme</span><span class="sxs-lookup"><span data-stu-id="7b4b8-182">Adding Docker Support to a WCF service</span></span>](https://github.com/dotnet-architecture/eShopModernizing/wiki/22.-Adding-Docker-Support)



## <a name="walkthrough-3-deploy-your-windows-containers-based-app-to-azure-vms"></a><span data-ttu-id="7b4b8-183">İzlenecek yol: 3: kapsayıcıları tabanlı Windows uygulamanızı Azure VM'ler için dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-183">Walkthrough 3: Deploy your Windows Containers-based app to Azure VMs</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="7b4b8-184">Teknik kılavuz kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="7b4b8-184">Technical walkthrough availability</span></span>

<span data-ttu-id="7b4b8-185">Tam teknik Kılavuzu eShopModernizing GitHub deposuna wiki kullanılabilir: [https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))</span><span class="sxs-lookup"><span data-stu-id="7b4b8-185">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki: [https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))</span></span>

### <a name="overview"></a><span data-ttu-id="7b4b8-186">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b4b8-186">Overview</span></span>

<span data-ttu-id="7b4b8-187">Docker ana bilgisayar üzerinde bir Windows Server 2016 sanal makine (VM) azure'a dağıtma hızlı geliştirme/test/hazırlama ortamlarını ayarlama ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-187">Deploying to a Docker host on a Windows Server 2016 Virtual Machine (VM) in Azure lets you quickly set up development/test/staging environments.</span></span> <span data-ttu-id="7b4b8-188">Bu ayrıca sınayıcılar veya iş kullanıcıları uygulama doğrulamak ortak bir yer sağlar.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-188">It also gives you a common place for testers or business users to validate the app.</span></span> <span data-ttu-id="7b4b8-189">VM'ler, bir hizmet (Iaas) üretim ortamlarında geçerli alt yapı de olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-189">VMs also can be valid Infrastucture as a Service (IaaS) production environments.</span></span>

### <a name="goals"></a><span data-ttu-id="7b4b8-190">Hedefleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-190">Goals</span></span>

<span data-ttu-id="7b4b8-191">Bu kılavuz, Windows Server 2016 veya sonraki sürümler göre Azure vm'lerine Windows kapsayıcıları dağıtırken sahip birden çok alternatifleri göstermek için hedefidir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-191">The goal of this walkthrough is to show you the multiple alternatives you have when you deploy Windows Containers to Azure VMs that are based on Windows Server 2016 or later versions.</span></span>

### <a name="scenarios"></a><span data-ttu-id="7b4b8-192">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-192">Scenarios</span></span>

<span data-ttu-id="7b4b8-193">Bazı senaryolarda bu kılavuzda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-193">Several scenarios are covered in this walkthrough.</span></span>

#### <a name="scenario-a-deploy-to-an-azure-vm-from-a-dev-pc-through-docker-engine-connection"></a><span data-ttu-id="7b4b8-194">Senaryo A: bir Azure VM geliştirme PC Docker altyapısına bağlantısı üzerinden gelen Dağıt</span><span class="sxs-lookup"><span data-stu-id="7b4b8-194">Scenario A: Deploy to an Azure VM from a dev PC through Docker Engine connection</span></span>

![Docker altyapısına bağlantısı üzerinden geliştirme bilgisayarınıza bir Azure VM Dağıtım](./media/image5-4.png)

> <span data-ttu-id="7b4b8-196">**Şekil 5-4.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-196">**Figure 5-4.**</span></span> <span data-ttu-id="7b4b8-197">Docker altyapısına bağlantısı üzerinden geliştirme bilgisayarınıza bir Azure VM Dağıtım</span><span class="sxs-lookup"><span data-stu-id="7b4b8-197">Deploy to an Azure VM from a dev PC through a Docker Engine connection</span></span>

#### <a name="scenario-b-deploy-to-an-azure-vm-through-a-docker-registry"></a><span data-ttu-id="7b4b8-198">Senaryo B: Docker kayıt defteri aracılığıyla bir Azure VM dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-198">Scenario B: Deploy to an Azure VM through a Docker Registry</span></span>

![Bir Azure VM Docker kayıt defteri aracılığıyla dağıtma](./media/image5-5.png)

> <span data-ttu-id="7b4b8-200">**Şekil 5-5.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-200">**Figure 5-5.**</span></span> <span data-ttu-id="7b4b8-201">Bir Azure VM Docker kayıt defteri aracılığıyla dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-201">Deploy to an Azure VM through a Docker Registry</span></span>

#### <a name="scenario-c-deploy-to-an-azure-vm-from-cicd-pipelines-in-visual-studio-team-services"></a><span data-ttu-id="7b4b8-202">Visual Studio Team Services içinde senaryo C: dağıtımı için bir Azure VM CI/CD'sinden ardışık düzenleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-202">Scenario C: Deploy to an Azure VM from CI/CD pipelines in Visual Studio Team Services</span></span>

![Visual Studio Team Services CI/CD ardışık düzen bir Azure VM Dağıtım](./media/image5-6.png)

> <span data-ttu-id="7b4b8-204">**Şekil 5-6.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-204">**Figure 5-6.**</span></span> <span data-ttu-id="7b4b8-205">Visual Studio Team Services CI/CD ardışık düzen bir Azure VM Dağıtım</span><span class="sxs-lookup"><span data-stu-id="7b4b8-205">Deploy to an Azure VM from CI/CD pipelines in Visual Studio Team Services</span></span>

### <a name="azure-vms-for-windows-containers"></a><span data-ttu-id="7b4b8-206">Azure VM'ler Windows kapsayıcıları için</span><span class="sxs-lookup"><span data-stu-id="7b4b8-206">Azure VMs for Windows Containers</span></span>

<span data-ttu-id="7b4b8-207">Azure VM'ler için Windows Windows Server 2016, Windows 10 veya sonraki sürümler göre VM'ler kapsayıcılardır, Docker altyapısına her ikisi de ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-207">Azure VMs for Windows Containers are VMs based on Windows Server 2016, Windows 10, or later versions, both with Docker Engine set up.</span></span> <span data-ttu-id="7b4b8-208">Çoğu durumda, Windows Server 2016 Azure Vm'lerde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-208">In most cases, Windows Server 2016 is used in the Azure VMs.</span></span>

<span data-ttu-id="7b4b8-209">Azure şu anda sağlar adlı bir VM'den **Windows Server 2016 kapsayıcılarla**.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-209">Azure currently provides a VM named **Windows Server 2016 with Containers**.</span></span> <span data-ttu-id="7b4b8-210">Bu VM, Windows Server Core veya Windows Nano Server ile yeni Windows Server kapsayıcı özelliği denemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-210">You can use this VM to try the new Windows Server Container feature, with either Windows Server Core or Windows Nano Server.</span></span> <span data-ttu-id="7b4b8-211">Kapsayıcı işletim sistemi görüntüleri yüklenir ve ardından VM ile Docker kullanıma hazırdır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-211">Container OS images are installed, and then the VM is ready to use with Docker.</span></span>

### <a name="benefits"></a><span data-ttu-id="7b4b8-212">Yararları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-212">Benefits</span></span>

<span data-ttu-id="7b4b8-213">Azure'a dağıtırken, şirket içi Windows Server 2016 VM'ler için Windows kapsayıcıları dağıtılabilir rağmen kullanıma hazır Windows Server kapsayıcı VM'ler ile çalışmaya başlamak için daha kolay bir yolu alın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-213">Although Windows Containers can be deployed to on-premises Windows Server 2016 VMs, when you deploy to Azure, you get an easier way to get started, with ready-to-use Windows Server Container VMs.</span></span> <span data-ttu-id="7b4b8-214">Ayrıca Sınayıcılar ve Azure sanal makine ölçek kümeleri aracılığıyla otomatik ölçeklenebilirlik erişebileceği ortak bir çevrimiçi konumu elde edersiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-214">You also get a common online location that’s accessible to testers, and automatic scalability through Azure virtual machine scale sets.</span></span>

### <a name="next-steps"></a><span data-ttu-id="7b4b8-215">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-215">Next steps</span></span>

<span data-ttu-id="7b4b8-216">Bu içerik daha kapsamlı GitHub Wiki'de keşfedin:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-216">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-How-to-deploy-your-Windows-Containers-based-app-into-Azure-VMs-(Including-CI-CD))

## <a name="walkthrough-4-deploy-your-windows-containers-based-apps-to-azure-container-instances-aci"></a><span data-ttu-id="7b4b8-217">İzlenecek yol: 4: Azure kapsayıcı örnekleri (ACI) Windows kapsayıcıları tabanlı uygulamalarınızı dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-217">Walkthrough 4: Deploy your Windows Containers-based apps to Azure Container Instances (ACI)</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="7b4b8-218">Teknik kılavuz kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="7b4b8-218">Technical walkthrough availability</span></span>

<span data-ttu-id="7b4b8-219">Tam teknik Kılavuzu eShopModernizing GitHub deposuna wiki kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-219">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

<span data-ttu-id="7b4b8-220">[Uygulamaları dağıtma ACI (Azure kapsayıcı örnekleri)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances))</span><span class="sxs-lookup"><span data-stu-id="7b4b8-220">[Deploying the Apps to ACI (Azure Container Instances)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances))</span></span>

### <a name="overview"></a><span data-ttu-id="7b4b8-221">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b4b8-221">Overview</span></span>

<span data-ttu-id="7b4b8-222">[Azure kapsayıcı örnekleri (ACI)](https://docs.microsoft.com/en-us/azure/container-instances/) kapsayıcıları tek tek örneklerini dağıtabileceğiniz kapsayıcıları dev/test/hazırlama ortamına sahip olmak için en hızlı yoludur.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-222">[Azure Container Instances (ACI)](https://docs.microsoft.com/en-us/azure/container-instances/) is the quickest way to have a Containers dev/test/staging environment where you can deploy single instances of containers.</span></span>

### <a name="goals"></a><span data-ttu-id="7b4b8-223">Hedefleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-223">Goals</span></span>

<span data-ttu-id="7b4b8-224">Bu kılavuzda Windows kapsayıcıları Azure kapsayıcı örnekleri (ACI) ve ACI eShopModernizing uygulamalarını nasıl dağıtabileceğini dağıtırken ana senaryo gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-224">This walkthrough shows you the main scenarios when deploying Windows Containers to Azure Container Instances (ACI) and how you can deploy eShopModernizing Apps into ACI.</span></span>

### <a name="scenarios"></a><span data-ttu-id="7b4b8-225">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-225">Scenarios</span></span>

<span data-ttu-id="7b4b8-226">Tek veya tüm uygulamaların (MVC uygulama, WebForms uygulaması veya WCF Hizmeti) dağıtmak gibi ACI eShopModernizing uygulamaları dağıtma hakkında Çeşitlemeler olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-226">There can be variations about deploying the eShopModernizing apps into ACI such as deploying just one or all of the apps (MVC app, WebForms app or WCF service).</span></span> <span data-ttu-id="7b4b8-227">Aşağıda gösterilen aşağıdaki senaryoda, ASP.NET MVC uygulaması artı ikisinin dağıtılan SQL Server kapsayıcı kapsayıcıları (Azure kapsayıcı örnekleri) ACI görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-227">In the following scenario shown below you can see the ASP.NET MVC app plus the SQL Server container both of them deployed as containers into ACI (Azure Container Instances).</span></span>

![Geliştirme ortamından ACI için dağıtma](./media/image5-3.5.6.png)

### <a name="benefits"></a><span data-ttu-id="7b4b8-229">Yararları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-229">Benefits</span></span>

<span data-ttu-id="7b4b8-230">Azure kapsayıcı örnekleri oluşturmak ve sanal makineler sağlamak veya bir üst düzey hizmet benimsemeyi zorunda kalmadan, azure'da Docker kapsayıcıları yönetmek kolay hale getirir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-230">Azure Container Instances makes it easy to create and manage Docker containers in Azure, without having to provision virtual machines or adopt a higher-level service.</span></span> <span data-ttu-id="7b4b8-231">ACI ile doğrudan Azure Windows kapsayıcısında dağıtabilir ve (Windows kapsayıcı görüntünün hazır Docker hub'a veya Azure kapsayıcı gibi Docker defterinde olması koşuluyla, bir tam etki alanı adı (FQDN) ile Internet'e birkaç saniye içinde kullanıma sunma Kayıt defteri).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-231">With ACI, you can directly deploy a Windows container in Azure and expose it to the internet with a fully qualified domain name (FQDN) in a matter of seconds (Provided that you have the Windows Container image ready in a Docker registry like Docker Hub or Azure Container Registry).</span></span>

### <a name="considerations"></a><span data-ttu-id="7b4b8-232">Dikkat Edilecekler</span><span class="sxs-lookup"><span data-stu-id="7b4b8-232">Considerations</span></span>

<span data-ttu-id="7b4b8-233">Tam ya da .NET Framework ile Windows kapsayıcıları dağıtma / ASP.NET veya SQL Server Azure kapsayıcı örnekleri (ACI) içine Docker görüntü olduğu normal bir Docker ana bilgisayar (örneğin, Windows Server 2016 Windows kapsayıcılarla) dağıtma olarak oldukça hızlı değil her zaman (Docker kayıt defterinden çekilen) indirilir ve kendi docker ana (kalıcı olarak çevrimiçi koruma daha ucuz ancak SQL kapsayıcı görüntüsünü (15.1 GB) ve ASP.NET kapsayıcı görüntüsünü (13.9 GB) boyutunu önemli ölçüde büyük Windows Server 2016 ile azure'da Windows kapsayıcıları VM), diğer yandan, üretim dağıtımları için harika seçenekleri olan Kubernetes Azure (AKS/ACS) veya Azure Service Fabric gibi tüm orchestrator gerekeceğinden buraya değil.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-233">Deploying Windows Containers with either full .NET Framework / ASP.NET or SQL Server into Azure Container Instances (ACI) is not quite as fast as deploying to a regular Docker Host (like a Windows Server 2016 with Windows Containers) because the Docker image has to be downloaded (pulled from the Docker registry) every time and the sizes of the SQL container image (15.1 GB) and the ASP.NET container image (13.9 GB) are significantly large, however it is much cheaper than maintaining your own docker host (permanently on-line Windows Server 2016 with Windows Containers VM in Azure) not to mention a whole orchestrator like Kubernetes in Azure (AKS/ACS) or Azure Service Fabric which are, on the other hand, great choices for production deployments.</span></span>

<span data-ttu-id="7b4b8-234">Ana sonuç, Azure kapsayıcı örnekleri CI/CD ardışık düzen ve geliştirme ve Test senaryoları için çok ilgi çekici bir seçenek kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-234">As main conclusion, using Azure Container Instances is a very compelling option for Dev/Test scenarios and for CI/CD pipelines.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7b4b8-235">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-235">Next steps</span></span>

<span data-ttu-id="7b4b8-236">Bu içerik daha kapsamlı GitHub Wiki'de keşfedin:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-236">Explore this content more in-depth on the GitHub wiki:</span></span> 

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-Deploying-the-Apps-to-ACI-(Azure-Container-Instances)TBD)


## <a name="walkthrough-5-deploy-your-windows-containers-based-apps-to-kubernetes-in-azure-container-service"></a><span data-ttu-id="7b4b8-237">5 izlenecek yol: Kubernetes Azure kapsayıcı hizmetinde kapsayıcıları tabanlı Windows uygulamalarınızı dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-237">Walkthrough 5: Deploy your Windows Containers-based apps to Kubernetes in Azure Container Service</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="7b4b8-238">Teknik kılavuz kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="7b4b8-238">Technical walkthrough availability</span></span>

<span data-ttu-id="7b4b8-239">Tam teknik Kılavuzu eShopModernizing GitHub deposuna wiki kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-239">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))

### <a name="overview"></a><span data-ttu-id="7b4b8-240">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b4b8-240">Overview</span></span>

<span data-ttu-id="7b4b8-241">Windows kapsayıcılarında tabanlı bir uygulama hızlı bir şekilde daha uzakta Iaas Vm'lerden taşıma platformlarda kullanmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-241">An application that's based on Windows Containers will quickly need to use platforms, moving even further away from IaaS VMs.</span></span> <span data-ttu-id="7b4b8-242">Bu kolayca yüksek ölçeklenebilirlik elde etmek için gereklidir ve daha iyi ölçeklenebilirlik otomatik ve önemli bir iyileştirme için dağıtımları ve sürüm oluşturma otomatik.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-242">This is needed to easily achieve high scalability and better automated scalability, and for a significant improvement in automated deployments and versioning.</span></span> <span data-ttu-id="7b4b8-243">Orchestrator'ı kullanarak bu hedefleri elde edebilirsiniz [Kubernetes](https://kubernetes.io/), kullanılabilir [Azure kapsayıcı hizmetlerini](https://azure.microsoft.com/services/container-service/).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-243">You can achieve these goals by using the orchestrator [Kubernetes](https://kubernetes.io/), available in [Azure Container Services](https://azure.microsoft.com/services/container-service/).</span></span>

### <a name="goals"></a><span data-ttu-id="7b4b8-244">Hedefleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-244">Goals</span></span>

<span data-ttu-id="7b4b8-245">Kubernetes Windows kapsayıcı tabanlı bir uygulamaya dağıtma hakkında bilgi edinmek için bu kılavuzu belirtilir (olarak da bilinir *K8s*) Azure kapsayıcı Hizmeti'nde.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-245">The goal of this walkthrough is to learn how to deploy a Windows Container–based application to Kubernetes (also called *K8s*) in Azure Container Service.</span></span> <span data-ttu-id="7b4b8-246">Kubernetes için baştan dağıtma iki adımlı bir işlemdir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-246">Deploying to Kubernetes from scratch is a two-step process:</span></span>

1.  <span data-ttu-id="7b4b8-247">Kubernetes küme Azure kapsayıcı hizmeti dağıtın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-247">Deploy a Kubernetes cluster to Azure Container Service.</span></span>

2.  <span data-ttu-id="7b4b8-248">İlgili kaynaklar ve uygulama Kubernetes kümeye dağıtın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-248">Deploy the application and related resources to the Kubernetes cluster.</span></span>

### <a name="scenarios"></a><span data-ttu-id="7b4b8-249">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-249">Scenarios</span></span>

#### <a name="scenario-a-deploy-directly-to-a-kubernetes-cluster-from-a-dev-environment"></a><span data-ttu-id="7b4b8-250">Senaryo A: bir geliştirme ortamı'ndan doğrudan Kubernetes kümeye dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-250">Scenario A: Deploy directly to a Kubernetes cluster from a dev environment</span></span>

![Geliştirme ortamından doğrudan Kubernetes kümeye dağıtma](./media/image5-7.png)

> <span data-ttu-id="7b4b8-252">**Şekil 5-7.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-252">**Figure 5-7.**</span></span> <span data-ttu-id="7b4b8-253">Geliştirme ortamından doğrudan Kubernetes kümeye dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-253">Deploy directly to a Kubernetes cluster from a development environment</span></span>

#### <a name="scenario-b-deploy-to-a-kubernetes-cluster-from-cicd-pipelines-in-team-services"></a><span data-ttu-id="7b4b8-254">Senaryo B: dağıtmak Kubernetes kümeye CI/CD'sinden Team Services içinde ardışık düzenleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-254">Scenario B: Deploy to a Kubernetes cluster from CI/CD pipelines in Team Services</span></span>

![CI/CD ardışık düzen Team Services Kubernetes kümeye dağıtım](./media/image5-8.png)

> <span data-ttu-id="7b4b8-256">**Şekil 5-8.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-256">**Figure 5-8.**</span></span> <span data-ttu-id="7b4b8-257">CI/CD ardışık düzen Team Services Kubernetes kümeye dağıtım</span><span class="sxs-lookup"><span data-stu-id="7b4b8-257">Deploy to a Kubernetes cluster from CI/CD pipelines in Team Services</span></span>

### <a name="benefits"></a><span data-ttu-id="7b4b8-258">Yararları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-258">Benefits</span></span>

<span data-ttu-id="7b4b8-259">Kubernetes bir kümede dağıtılması için birçok avantaj vardır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-259">There are many benefits to deploying to a cluster in Kubernetes.</span></span> <span data-ttu-id="7b4b8-260">En büyük (varolan düğümleri iç ölçeklenebilirlik) kullanmak istiyorsanız ve sayısını düğümlerinin veya sanal makineleri küme (temel kapsayıcı örnek sayısına göre uygulamanın içinde ölçeklenebilen bir üretime hazır ortamı alma avantajdır Genel ölçeklenebilirlik kümenin).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-260">The biggest benefit is that you get a production-ready environment in which you can scale out the application based on the number of container instances you want to use (inner-scalability in the existing nodes), and based on the number of nodes or VMs in the cluster (global scalability of the cluster).</span></span>

<span data-ttu-id="7b4b8-261">Azure kapsayıcı hizmeti popüler açık kaynak Araçlar ve teknolojiler özellikle Azure için en iyi duruma getirir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-261">Azure Container Service optimizes popular open-source tools and technologies specifically for Azure.</span></span> <span data-ttu-id="7b4b8-262">Taşınabilirlik, kapsayıcılarınızı hem uygulama yapılandırmanızı sağlayan açık olan çözüm alın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-262">You get an open solution that offers portability, both for your containers and for your application configuration.</span></span> <span data-ttu-id="7b4b8-263">Boyutu, ana bilgisayar sayısını seçin ve orchestrator araçları-kapsayıcı hizmeti şey işler.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-263">You select the size, the number of hosts, and the orchestrator tools-Container Service handles everything else.</span></span>

<span data-ttu-id="7b4b8-264">Kubernetes ile geliştiriciler fiziksel ve sanal makineler hakkında düşünmekten aşağıdaki özellikleri, diğerlerinin yanı sıra kolaylaştıran kapsayıcı merkezli bir altyapı planlama için ilerleme:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-264">With Kubernetes, developers can progress from thinking about physical and virtual machines, to planning a container-centric infrastructure that facilitates the following capabilities, among others:</span></span>

- <span data-ttu-id="7b4b8-265">Birden çok kapsayıcılara göre uygulamaları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-265">Applications based on multiple containers</span></span>

- <span data-ttu-id="7b4b8-266">Kapsayıcı örnekleri ve yatay otomatik ölçeklendirmeyi çoğaltma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-266">Replicating container instances and horizontal autoscaling</span></span>

- <span data-ttu-id="7b4b8-267">Adlandırma ve (örneğin, iç DNS) bulma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-267">Naming and discovering (for example, internal DNS)</span></span>

- <span data-ttu-id="7b4b8-268">Yükünü dengeleme</span><span class="sxs-lookup"><span data-stu-id="7b4b8-268">Balancing loads</span></span>

- <span data-ttu-id="7b4b8-269">Güncelleştirmeleri alınıyor</span><span class="sxs-lookup"><span data-stu-id="7b4b8-269">Rolling updates</span></span>

- <span data-ttu-id="7b4b8-270">Gizli dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-270">Distributing secrets</span></span>

- <span data-ttu-id="7b4b8-271">Uygulama durumu denetimleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-271">Application health checks</span></span>

## <a name="next-steps"></a><span data-ttu-id="7b4b8-272">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-272">Next steps</span></span>

<span data-ttu-id="7b4b8-273">Bu içerik daha kapsamlı GitHub Wiki'de keşfedin: [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))</span><span class="sxs-lookup"><span data-stu-id="7b4b8-273">Explore this content more in-depth on the GitHub wiki: [https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/04.-How-to-deploy-your-Windows-Containers-based-apps-into-Kubernetes-in-Azure-Container-Service-(Including-C-CD))</span></span>

## <a name="walkthrough-6-deploy-your-windows-containers-based-apps-to-azure-service-fabric"></a><span data-ttu-id="7b4b8-274">İzlenecek yol: 6: Azure Service Fabric Windows kapsayıcıları tabanlı uygulamalarınızı dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-274">Walkthrough 6: Deploy your Windows Containers-based apps to Azure Service Fabric</span></span>

### <a name="technical-walkthrough-availability"></a><span data-ttu-id="7b4b8-275">Teknik kılavuz kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="7b4b8-275">Technical walkthrough availability</span></span>

<span data-ttu-id="7b4b8-276">Tam teknik Kılavuzu eShopModernizing GitHub deposuna wiki kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-276">The full technical walkthrough is available in the eShopModernizing GitHub repo wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

### <a name="overview"></a><span data-ttu-id="7b4b8-277">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="7b4b8-277">Overview</span></span>

<span data-ttu-id="7b4b8-278">Windows kapsayıcılarında hızla tabanlı bir uygulama daha uzakta Iaas Vm'lerden taşıma platformları kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-278">An application based on Windows Containers quickly needs to use platforms, moving even further away from IaaS VMs.</span></span> <span data-ttu-id="7b4b8-279">Bu kolayca yüksek ölçeklenebilirlik elde etmek için gereklidir ve daha iyi ölçeklenebilirlik otomatik ve önemli bir iyileştirme için dağıtımları ve sürüm oluşturma otomatik.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-279">This is needed to easily achieve high scalability and better automated scalability, and for a significant improvement in automated deployments and versioning.</span></span> <span data-ttu-id="7b4b8-280">Azure bulutta kullanılabilir, ancak şirket içi kullanmak de kullanılabilir olan, Azure Service Fabric orchestrator kullanarak veya farklı bir genel bulut bile, bu hedefleri elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-280">You can achieve these goals by using the orchestrator Azure Service Fabric, which is available in the Azure cloud, but also available to use on-premises, or even in a different public cloud.</span></span>

### <a name="goals"></a><span data-ttu-id="7b4b8-281">Hedefleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-281">Goals</span></span>

<span data-ttu-id="7b4b8-282">Bu kılavuzda Windows kapsayıcı tabanlı bir uygulama için Azure Service Fabric kümesi dağıtma hakkında bilgi edinmek için hedefidir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-282">The goal of this walkthrough is to learn how to deploy a Windows Container–based application to a Service Fabric cluster in Azure.</span></span> <span data-ttu-id="7b4b8-283">Service Fabric sıfırdan dağıtma iki adımlı bir işlemdir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-283">Deploying to Service Fabric from scratch is a two-step process:</span></span>

1.  <span data-ttu-id="7b4b8-284">Service Fabric kümesi Azure (veya farklı bir ortam) dağıtın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-284">Deploy a Service Fabric cluster to Azure (or to a different environment).</span></span>

2.  <span data-ttu-id="7b4b8-285">İlgili kaynaklar ve uygulama için Service Fabric kümesi dağıtın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-285">Deploy the application and related resources to the Service Fabric cluster.</span></span>

### <a name="scenarios"></a><span data-ttu-id="7b4b8-286">Senaryolar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-286">Scenarios</span></span>

#### <a name="scenario-a-deploy-directly-to-a-service-fabric-cluster-from-a-dev-environment"></a><span data-ttu-id="7b4b8-287">Senaryo A: Dağıt doğrudan bir Service Fabric kümesi bir geliştirme ortamı'ndan</span><span class="sxs-lookup"><span data-stu-id="7b4b8-287">Scenario A: Deploy directly to a Service Fabric cluster from a dev environment</span></span>

![Geliştirme ortamından doğrudan bir Service Fabric kümesi dağıtma](./media/image5-9.png)

> <span data-ttu-id="7b4b8-289">**Şekil 5-9.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-289">**Figure 5-9.**</span></span> <span data-ttu-id="7b4b8-290">Geliştirme ortamından doğrudan bir Service Fabric kümesi dağıtma</span><span class="sxs-lookup"><span data-stu-id="7b4b8-290">Deploy directly to a Service Fabric cluster from a development environment</span></span>

### <a name="scenario-b-deploy-to-a-service-fabric-cluster-from-cicd-pipelines-in-team-services"></a><span data-ttu-id="7b4b8-291">Senaryo B: dağıtmak için Service Fabric kümesi CI/CD'sinden Team Services içinde ardışık düzenleri</span><span class="sxs-lookup"><span data-stu-id="7b4b8-291">Scenario B: Deploy to a Service Fabric cluster from CI/CD pipelines in Team Services</span></span>

![Service Fabric kümesi için Visual Studio Team Services CI/CD ardışık düzen dağıtım](./media/image5-10.png)

> <span data-ttu-id="7b4b8-293">**Şekil 5-10.**</span><span class="sxs-lookup"><span data-stu-id="7b4b8-293">**Figure 5-10.**</span></span> <span data-ttu-id="7b4b8-294">Service Fabric kümesi için Visual Studio Team Services CI/CD ardışık düzen dağıtım</span><span class="sxs-lookup"><span data-stu-id="7b4b8-294">Deploy to a Service Fabric cluster from CI/CD pipelines in Visual Studio Team Services</span></span>

## <a name="benefits"></a><span data-ttu-id="7b4b8-295">Yararları</span><span class="sxs-lookup"><span data-stu-id="7b4b8-295">Benefits</span></span>

<span data-ttu-id="7b4b8-296">Service Fabric, kümeye dağıtma avantajlarını Kubernetes kullanmanın avantajları için benzerdir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-296">The benefits of deploying to a cluster in Service Fabric are similar to the benefits of using Kubernetes.</span></span> <span data-ttu-id="7b4b8-297">Tek fark, yine de olan Service Fabric Kubernetes sürüm 1.9 Windows kapsayıcı için bir beta aşamasında olan Kubernetes karşılaştırıldığında Windows uygulamaları için daha da olgun bir üretim ortamında olduğunu (aralık 2017).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-297">One difference, though, is that Service Fabric is a more mature production environment for Windows applications compared to Kubernetes, which is in a beta phase for Windows Containers in Kubernetes version 1.9 (December 2017).</span></span> <span data-ttu-id="7b4b8-298">Kubernetes Linux daha da olgun bir ortamdır.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-298">Kubernetes is a more mature environment for Linux.</span></span>

<span data-ttu-id="7b4b8-299">Azure Service Fabric kullanmanın ana Avantajı (varolan düğümleri iç ölçeklenebilirlik) kullanmak istiyorsanız ve sayısına göre kapsayıcı örnek sayısına göre uygulamanın içinde ölçeklenebilen bir üretime hazır ortamı alma olduğu düğümler ve (genel ölçeklenebilirlik kümenin) kümedeki sanal makineleri.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-299">The main benefit of using Azure Service Fabric is that you get a production-ready environment in which you can scale out the application based on the number of container instances you want to use (inner-scalability in the existing nodes), and based on the number of nodes or VMs in the cluster (global scalability of the cluster).</span></span>

<span data-ttu-id="7b4b8-300">Azure Service Fabric taşınabilirlik kapsayıcılarınızı hem uygulama yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-300">Azure Service Fabric offers portability both for your containers and for your application configuration.</span></span> <span data-ttu-id="7b4b8-301">Azure'da küme ya da şirket içi, kendi veri merkezinizde yüklemeyi Service Fabric olabilir.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-301">You can have a Service Fabric cluster in Azure, or install it on-premises in your own datacenter.</span></span> <span data-ttu-id="7b4b8-302">Bile bir Service Fabric kümesi farklı bir buluta gibi yükleyebilirsiniz [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).</span><span class="sxs-lookup"><span data-stu-id="7b4b8-302">You can even install a Service Fabric cluster in a different cloud, like [Amazon AWS](https://blogs.msdn.microsoft.com/azureservicefabric/2017/05/18/tutorial-how-to-create-a-service-fabric-standalone-cluster-with-aws-ec2-instances/).</span></span>

<span data-ttu-id="7b4b8-303">Service Fabric ile geliştiriciler fiziksel ve sanal makineler hakkında düşünmekten aşağıdaki özellikleri, diğerlerinin yanı sıra kolaylaştıran kapsayıcı merkezli bir altyapı planlama için ilerleme:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-303">With Service Fabric, developers can progress from thinking about physical and virtual machines to planning a container-centric infrastructure that facilitates the following capabilities, among others:</span></span>

- <span data-ttu-id="7b4b8-304">Birden çok kapsayıcılara göre uygulamalar.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-304">Applications based on multiple containers.</span></span>

- <span data-ttu-id="7b4b8-305">Kapsayıcı örnekleri ve yatay otomatik ölçeklendirmeyi çoğaltılıyor.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-305">Replicating container instances and horizontal autoscaling.</span></span>

- <span data-ttu-id="7b4b8-306">Adlandırma ve (örneğin, iç DNS) bulma.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-306">Naming and discovering (for example, internal DNS).</span></span>

- <span data-ttu-id="7b4b8-307">Yükü Dengeleme.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-307">Balancing loads.</span></span>

- <span data-ttu-id="7b4b8-308">Güncelleştirmeleri alınıyor.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-308">Rolling updates.</span></span>

- <span data-ttu-id="7b4b8-309">Gizli dağıtma.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-309">Distributing secrets.</span></span>

- <span data-ttu-id="7b4b8-310">Uygulama durumunu denetler.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-310">Application health checks.</span></span>

<span data-ttu-id="7b4b8-311">Aşağıdaki özellikleri Service Fabric (diğer orchestrators karşılaştırıldığında) de özeldir:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-311">The following capabilities are exclusive in Service Fabric (compared to other orchestrators):</span></span>

- <span data-ttu-id="7b4b8-312">Güvenilir hizmetler uygulama modeli üzerinden durum bilgisi olan hizmetler yeteneği.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-312">Stateful services capability, through the Reliable Services application model.</span></span>

- <span data-ttu-id="7b4b8-313">Reliable Actors uygulama modeli üzerinden aktörler deseni.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-313">Actors pattern, through the Reliable Actors application model.</span></span>

- <span data-ttu-id="7b4b8-314">Windows veya Linux kapsayıcıları yanı sıra tam kemik işlemleri dağıtın.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-314">Deploy bare-bone processes, in addition to Windows or Linux containers.</span></span>

- <span data-ttu-id="7b4b8-315">Gelişmiş çalışırken güncelleştirmeleri ve sistem durumu denetimleri.</span><span class="sxs-lookup"><span data-stu-id="7b4b8-315">Advanced rolling updates and health checks.</span></span>

### <a name="next-steps"></a><span data-ttu-id="7b4b8-316">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7b4b8-316">Next steps</span></span>

<span data-ttu-id="7b4b8-317">Bu içerik daha kapsamlı GitHub Wiki'de keşfedin:</span><span class="sxs-lookup"><span data-stu-id="7b4b8-317">Explore this content more in-depth on the GitHub wiki:</span></span>

[https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD)](https://github.com/dotnet-architecture/eShopModernizing/wiki/05.-How-to-deploy-your-Windows-Containers-based-apps-into-Azure-Service-Fabric-(Including-CI-CD))

>[!div class="step-by-step"]
<span data-ttu-id="7b4b8-318">[Önceki](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[sonraki](conclusions.md)</span><span class="sxs-lookup"><span data-stu-id="7b4b8-318">[Previous](lift-and-shift-existing-apps-devops/migrate-to-hybrid-cloud-scenarios.md)
[Next](conclusions.md)</span></span>
