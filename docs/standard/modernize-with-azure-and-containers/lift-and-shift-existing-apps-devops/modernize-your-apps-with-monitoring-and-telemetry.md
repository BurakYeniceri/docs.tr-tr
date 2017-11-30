---
title: "Uygulamalarınızı izleme ve telemetri ile modernize"
description: "Kapsayıcılı .NET uygulamaları için .NET mikro mimarisi | Uygulamalarınızı izleme ve telemetri ile modernize"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/26/2017
ms.openlocfilehash: 03a6f2be9dc6c020cfe93a2597d1288943e527c8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="modernize-your-apps-with-monitoring-and-telemetry"></a><span data-ttu-id="7cbf2-103">Uygulamalarınızı izleme ve telemetri ile modernize</span><span class="sxs-lookup"><span data-stu-id="7cbf2-103">Modernize your apps with monitoring and telemetry</span></span>

<span data-ttu-id="7cbf2-104">Üretimde bir uygulamayı çalıştırdığınızda, uygulamanızın nasıl gerçekleştirme hakkında Öngörüler olması önemlidir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-104">When you run an application in production, it's critical that you have insights about how your application is performing.</span></span> <span data-ttu-id="7cbf2-105">Yüksek bir düzeyde çalışıyor?</span><span class="sxs-lookup"><span data-stu-id="7cbf2-105">Is it performing at a high level?</span></span> <span data-ttu-id="7cbf2-106">Kullanıcıların hatalarla karşılaşıyor ya da uygulama kararlı ve güvenilir?</span><span class="sxs-lookup"><span data-stu-id="7cbf2-106">Are users getting errors, or is the application stable and reliable?</span></span> <span data-ttu-id="7cbf2-107">Zengin performans izleme, güçlü uyarı ve uygulamanızı kullanılabilir ve beklendiği gibi gerçekleştirme olmasına yardımcı olmak için panolar gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-107">You need rich performance monitoring, powerful alerting, and dashboards to help ensure that your application is available and performing as expected.</span></span> <span data-ttu-id="7cbf2-108">Ayrıca, hızlı bir şekilde bir sorun olup olmadığını, kaç tane müşteriler etkilenir ve bulmak ve sorunu düzeltmek için kök neden analizi yapmak belirlemek mümkün olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-108">You also need to be able to see quickly if there's a problem, determine how many customers are affected, and perform a root-cause analysis to find and fix the issue.</span></span>

## <a name="monitor-your-application-with-application-insights"></a><span data-ttu-id="7cbf2-109">Uygulamanızı Application Insights ile izleme</span><span class="sxs-lookup"><span data-stu-id="7cbf2-109">Monitor your application with Application Insights</span></span>

<span data-ttu-id="7cbf2-110">Application Insights kuran genişletilebilir bir uygulama performansı Yönetimi (APM) hizmetini birden çok platformda çalışan web geliştiricileri için olur.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-110">Application Insights is an extensible Application Performance Management (APM) service for web developers who work on multiple platforms.</span></span> <span data-ttu-id="7cbf2-111">Canlı web uygulamanızı izlemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-111">Use it to monitor your live web application.</span></span> <span data-ttu-id="7cbf2-112">Application Insights, performans anormalliklerini otomatik olarak algılar.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-112">Application Insights automatically detects performance anomalies.</span></span> <span data-ttu-id="7cbf2-113">Sorunları tanılamanıza yardımcı ve kullanıcıların gerçekte uygulamanızla ne anlamanıza yardımcı olması için güçlü analytics araçlar içerir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-113">It includes powerful analytics tools to help you diagnose issues, and to help you understand what users actually do with your app.</span></span> <span data-ttu-id="7cbf2-114">Application Insights sürekli performansını ve kullanımını geliştirmemize yardımcı olmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-114">Application Insights is designed to help you continuously improve performance and usability.</span></span> <span data-ttu-id="7cbf2-115">Uygulamalar için çok çeşitli platformlar, .NET, Node.js ve J2EE, olup olmadığı gibi üzerinde çalışır şirket içi barındırılan veya bulutta.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-115">It works for apps on a wide variety of platforms, including .NET, Node.js, and J2EE, whether hosted on-premises or in the cloud.</span></span> <span data-ttu-id="7cbf2-116">Application Insights DevOps işlemlerinizi ile tümleşir ve geliştirme araçları, çeşitli bağlantı noktalarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-116">Application Insights integrates with your DevOps processes, and has connection points to a variety of development tools.</span></span>

<span data-ttu-id="7cbf2-117">Şekil 4-10 Application Insights uygulamanızı nasıl izler ve nasıl bir Pano bu Öngörüler kontrollerinden örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-117">Figure 4-10 shows an example of how Application Insights monitors your application and how it surfaces those insights to a dashboard.</span></span>

![Application Insights izleme Panosu](./media/image10.png)

> <span data-ttu-id="7cbf2-119">**Şekil 4-10.**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-119">**Figure 4-10.**</span></span> <span data-ttu-id="7cbf2-120">Application Insights izleme Panosu</span><span class="sxs-lookup"><span data-stu-id="7cbf2-120">Application Insights monitoring dashboard</span></span>

## <a name="monitor-your-docker-infrastructure-with-log-analytics-and-its-container-monitoring-solution"></a><span data-ttu-id="7cbf2-121">Günlük analizi ve kapsayıcı izleme çözümünün ile Docker altyapısını izleme</span><span class="sxs-lookup"><span data-stu-id="7cbf2-121">Monitor your Docker infrastructure with Log Analytics and its Container Monitoring solution</span></span>

<span data-ttu-id="7cbf2-122">[Azure günlük analizi](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview) parçası olan [izleme çözümüne genel Microsoft Azure](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview).</span><span class="sxs-lookup"><span data-stu-id="7cbf2-122">[Azure Log Analytics](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview) is part of the [Microsoft Azure overall monitoring solution](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview).</span></span> <span data-ttu-id="7cbf2-123">Bu bir ayrıca bir hizmet olduğundan [Operations Management Suite (OMS)](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview).</span><span class="sxs-lookup"><span data-stu-id="7cbf2-123">It's also a service in [Operations Management Suite (OMS)](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview).</span></span> <span data-ttu-id="7cbf2-124">Günlük analizi bulut izler ve ortamları (OMS şirket içi için) kullanılabilirlik ve performans sağlanmasına yardımcı olmak için şirket içi.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-124">Log Analytics monitors cloud and on-premises environments (OMS for on-premises) to help maintain availability and performance.</span></span> <span data-ttu-id="7cbf2-125">Bulut ve şirket içi ortamları ve analiz arasında birden çok kaynak sağlamak için diğer İzleme Araçları'ndan kaynaklar tarafından oluşturulan veri toplar.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-125">It collects data generated by resources in your cloud and on-premises environments and from other monitoring tools to provide analysis across multiple sources.</span></span>

<span data-ttu-id="7cbf2-126">Azure altyapı günlükleri ile ilgili olarak, günlük analizi, bir Azure hizmeti diğer Azure hizmetleriyle günlük ve ölçüm verilerini alır (aracılığıyla [Azure İzleyici](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)), Azure Vm'leri, Docker kapsayıcıları ve şirket içi veya diğer bulut altyapıları.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-126">In relation to Azure infrastructure logs, Log Analytics, as an Azure service, ingests log and metric data from other Azure services (via [Azure Monitor](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)), Azure VMs, Docker containers, and on-premises or other cloud infrastructures.</span></span> <span data-ttu-id="7cbf2-127">Günlük analizi esnek günlük arama ve çıkış-yepyeni analytics bu veriler üzerinde sunar.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-127">Log Analytics offers flexible log search and out-of-the box analytics on top of this data.</span></span> <span data-ttu-id="7cbf2-128">Bu veri kaynakları genelinde çözümlemek için kullanabileceğiniz, karmaşık sorgular tüm günlükleri sağlar ve önceden uyarabilir zengin araçları belirtilen koşullara göre sağlar.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-128">It provides rich tools that you can use to analyze data across sources, it allows complex queries across all logs, and it can proactively alert based on specified conditions.</span></span> <span data-ttu-id="7cbf2-129">Özel veri deposunda burada sorgulamak ve bu görselleştirme Merkezi günlük analizi, hatta toplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-129">You can even collect custom data in the central Log Analytics repository, where you can query and visualize it.</span></span> <span data-ttu-id="7cbf2-130">Ayrıca, hemen güvenlik Öngörüler elde etmek için günlük analizi yerleşik çözümleri avantajlarından ve altyapınızı işlevselliğini alabilir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-130">You also can take advantage of the Log Analytics built-in solutions to immediately gain insights into the security and functionality of your infrastructure.</span></span>

<span data-ttu-id="7cbf2-131">Günlük analizi OMS portalı veya herhangi bir tarayıcısında çalıştırmak, Azure portalı erişmek ve, yapılandırma ayarlarını erişimi olan ve birden çok araç çözümlemek ve toplanan verilerde işlem yapmak için sağlayın.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-131">You can access Log Analytics through the OMS portal or the Azure portal, which run in any browser, and provide you with access to configuration settings and multiple tools to analyze and act on collected data.</span></span>

<span data-ttu-id="7cbf2-132">[Kapsayıcı izlemesi çözümü](https://docs.microsoft.com/azure/log-analytics/log-analytics-containers) günlük analizi yardımcı olur görüntüleyin ve Docker ve Windows kapsayıcı konaklarınızın tek bir konumda yönetin.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-132">The [Container Monitoring solution](https://docs.microsoft.com/azure/log-analytics/log-analytics-containers) in Log Analytics helps you view and manage your Docker and Windows Container hosts in a single location.</span></span> <span data-ttu-id="7cbf2-133">Bir çözüm gösterilmektedir hangi kapsayıcılar olan çalışan, hangi kapsayıcı görüntü çalıştırdıkları ve kapsayıcıları çalıştırdığı.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-133">The solution shows which containers are running, what container image they're running, and where containers are running.</span></span> <span data-ttu-id="7cbf2-134">Kapsayıcılar ile kullanılan komutları dahil olmak üzere ayrıntılı denetim bilgileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-134">You can view detailed audit information, including commands that are being used with containers.</span></span> <span data-ttu-id="7cbf2-135">Ayrıca, görüntüleme ve Uzaktan Docker ya da Windows ana bilgisayarları görüntülemek gerek kalmadan merkezi günlükleri, arama yaparak kapsayıcıları giderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-135">You also can troubleshoot containers by viewing and searching centralized logs, without needing to remotely view Docker or Windows hosts.</span></span> <span data-ttu-id="7cbf2-136">Bir ana bilgisayar üzerindeki gürültülü ve alan üst limiti aşan kaynakları olabilir kapsayıcıları bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-136">You can find containers that might be noisy and consuming excess resources on a host.</span></span> <span data-ttu-id="7cbf2-137">Ayrıca, merkezi CPU, bellek, depolama ve ağ kullanımını ve kapsayıcıları için performans bilgileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-137">Additionally, you can view centralized CPU, memory, storage, and network usage, and performance information, for containers.</span></span> <span data-ttu-id="7cbf2-138">Windows çalıştıran bilgisayarlarda, merkezileştirme ve Windows Server günlüklerinden karşılaştırmak Hyper-V ve Docker kapsayıcıları.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-138">On computers running Windows, you can centralize and compare logs from Windows Server, Hyper-V, and Docker containers.</span></span> <span data-ttu-id="7cbf2-139">Aşağıdaki kapsayıcı orchestrators çözümünü destekler:</span><span class="sxs-lookup"><span data-stu-id="7cbf2-139">The solution supports the following container orchestrators:</span></span>

-   <span data-ttu-id="7cbf2-140">Docker Swarm</span><span class="sxs-lookup"><span data-stu-id="7cbf2-140">Docker Swarm</span></span>

-   <span data-ttu-id="7cbf2-141">DC/OS</span><span class="sxs-lookup"><span data-stu-id="7cbf2-141">DC/OS</span></span>

-   <span data-ttu-id="7cbf2-142">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="7cbf2-142">Kubernetes</span></span>

-   <span data-ttu-id="7cbf2-143">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7cbf2-143">Service Fabric</span></span>

-   <span data-ttu-id="7cbf2-144">Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="7cbf2-144">Red Hat OpenShift</span></span>

<span data-ttu-id="7cbf2-145">Şekil 4-11 çeşitli kapsayıcı konakları ve aracıları ve OMS arasındaki ilişkileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-145">Figure 4-11 shows the relationships between various container hosts and agents and OMS.</span></span>

![Günlük analizi kapsayıcı izlemesi çözümü](./media/image11.png)

> <span data-ttu-id="7cbf2-147">**Şekil 4-11.**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-147">**Figure 4-11.**</span></span> <span data-ttu-id="7cbf2-148">Günlük analizi kapsayıcı izlemesi çözümü</span><span class="sxs-lookup"><span data-stu-id="7cbf2-148">Log Analytics Container Monitoring solution</span></span>

<span data-ttu-id="7cbf2-149">Günlük analizi kapsayıcı izleme çözümü kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7cbf2-149">You can use the Log Analytics Container Monitoring solution to:</span></span>

-   <span data-ttu-id="7cbf2-150">Konaklarda kapsayıcı tek bir konum hakkında bilgi bakın.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-150">See information about all container hosts in a single location.</span></span>

-   <span data-ttu-id="7cbf2-151">Hangi kapsayıcıları olduğunu biliyorsanız, hangi görüntü çalıştırdıkları çalıştırıp nerede çalışıyor.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-151">Know which containers are running, what image they're running, and where they're running.</span></span>

-   <span data-ttu-id="7cbf2-152">Eylemler için bir denetim izi kapsayıcılarında bakın.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-152">See an audit trail for actions on containers.</span></span>

-   <span data-ttu-id="7cbf2-153">Görüntüleme ve Docker ana bilgisayarları için uzaktan oturum açma olmadan merkezi günlükleri arama yaparak sorunlarını giderin.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-153">Troubleshoot by viewing and searching centralized logs without remote login to the Docker hosts.</span></span>

-   <span data-ttu-id="7cbf2-154">"Gürültülü komşu" olabilir ve bir ana bilgisayar üzerindeki fazla kaynak tüketmeye kapsayıcıları bulun.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-154">Find containers that might be "noisy neighbors," and be consuming excess resources on a host.</span></span>

-   <span data-ttu-id="7cbf2-155">Merkezi CPU, bellek, depolama ve ağ kullanımını ve kapsayıcıları için performans bilgilerini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="7cbf2-155">View centralized CPU, memory, storage, and network usage, and performance information, for containers.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="7cbf2-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7cbf2-156">Additional resources</span></span>

-   <span data-ttu-id="7cbf2-157">**Microsoft Azure'da izleme genel bakış**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-157">**Overview of monitoring in Microsoft Azure**</span></span>

[<span data-ttu-id="7cbf2-158">https://docs.microsoft.com/Azure/Monitoring-and-Diagnostics/Monitoring-Overview</span><span class="sxs-lookup"><span data-stu-id="7cbf2-158">https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview</span></span>](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview)

-   <span data-ttu-id="7cbf2-159">**Application Insights nedir?**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-159">**What is Application Insights?**</span></span>

[<span data-ttu-id="7cbf2-160">https://docs.microsoft.com/Azure/Application-insights/App-insights-Overview</span><span class="sxs-lookup"><span data-stu-id="7cbf2-160">https://docs.microsoft.com/azure/application-insights/app-insights-overview</span></span>](https://docs.microsoft.com/azure/application-insights/app-insights-overview)

-   <span data-ttu-id="7cbf2-161">**Günlük analizi nedir?**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-161">**What is Log Analytics?**</span></span>

[<span data-ttu-id="7cbf2-162">https://docs.microsoft.com/Azure/log-Analytics/log-Analytics-Overview</span><span class="sxs-lookup"><span data-stu-id="7cbf2-162">https://docs.microsoft.com/azure/log-analytics/log-analytics-overview</span></span>](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview)

-   <span data-ttu-id="7cbf2-163">**Kapsayıcı izleme çözümüne günlük analizi**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-163">**Container Monitoring solution in Log Analytics**</span></span>

[<span data-ttu-id="7cbf2-164">https://docs.microsoft.com/Azure/log-Analytics/log-Analytics-Containers</span><span class="sxs-lookup"><span data-stu-id="7cbf2-164">https://docs.microsoft.com/azure/log-analytics/log-analytics-containers</span></span>](https://docs.microsoft.com/azure/log-analytics/log-analytics-containers)

-   <span data-ttu-id="7cbf2-165">**Azure İzleyicisi'ne genel bakış**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-165">**Overview of Azure Monitor**</span></span>

[<span data-ttu-id="7cbf2-166">https://docs.microsoft.com/Azure/Monitoring-and-Diagnostics/Monitoring-Overview-Azure-Monitor</span><span class="sxs-lookup"><span data-stu-id="7cbf2-166">https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor</span></span>](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)

-   <span data-ttu-id="7cbf2-167">**Operations Management Suite (OMS) nedir?**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-167">**What is Operations Management Suite (OMS)?**</span></span>

[<span data-ttu-id="7cbf2-168">https://docs.microsoft.com/Azure/Operations-Management-Suite/Operations-Management-Suite-Overview</span><span class="sxs-lookup"><span data-stu-id="7cbf2-168">https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview</span></span>](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview)

-   <span data-ttu-id="7cbf2-169">**Service Fabric OMS ile Windows Server kapsayıcıları izleme**</span><span class="sxs-lookup"><span data-stu-id="7cbf2-169">**Monitoring Windows Server containers in Service Fabric with OMS**</span></span>

[<span data-ttu-id="7cbf2-170">https://docs.microsoft.com/Azure/Service-fabric/Service-fabric-Diagnostics-Containers-windowsserver</span><span class="sxs-lookup"><span data-stu-id="7cbf2-170">https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-containers-windowsserver</span></span>](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-containers-windowsserver)

>[!div class="step-by-step"]
<span data-ttu-id="7cbf2-171">[Önceki](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
[sonraki](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)</span><span class="sxs-lookup"><span data-stu-id="7cbf2-171">[Previous](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
[Next](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)</span></span>