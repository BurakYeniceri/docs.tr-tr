---
title: "Docker (Windows için Visual Studio) için Visual Studio araçlarını kullanma"
description: "Microsoft Platformu ve araçları ile kapsayıcılı Docker uygulama yaşam döngüsü"
keywords: "Docker, mikro, ASP.NET, kapsayıcı"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 717675170f19f18fb48c4cea3ddd15bcd9648d71
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/23/2017
---
# <a name="using-visual-studio-tools-for-docker-visual-studio-on-windows"></a><span data-ttu-id="6321a-104">Docker (Windows için Visual Studio) için Visual Studio araçlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="6321a-104">Using Visual Studio Tools for Docker (Visual Studio on Windows)</span></span>

<span data-ttu-id="6321a-105">Docker Visual Studio Code ve Docker CLI kullanırken akışına benzer için Visual Studio Araçları kullanırken Geliştirici iş akışı (aslında, aynı Docker CLI üzerinde temel), ancak başlamak kolaydır, işlemini basitleştirir ve büyük sağlar derleme için üretkenlik çalıştırın ve Görevler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6321a-105">The developer workflow when using Visual Studio Tools for Docker is similar to the workflow when using Visual Studio Code and Docker CLI (in fact, it is based on the same Docker CLI), but it is easier to get started, simplifies the process, and provides greater productivity for the build, run, and compose tasks.</span></span> <span data-ttu-id="6321a-106">Ayrıca yürütün ve kapsayıcılarınızı F5 ve Ctrl + F5 Visual Studio'dan gibi basit eylemleri aracılığıyla hata ayıklama mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="6321a-106">It's also able to execute and debug your containers via simple actions like F5 and Ctrl+F5 from Visual Studio.</span></span> <span data-ttu-id="6321a-107">Daha da ile çalıştırın ve tek bir kapsayıcı hata ayıklamak için ek olarak Visual Studio 2017, ayrıca çalıştırabilir ve çözüm düzeyinde aynı docker-compose.yml dosyası olarak tanımlanmışsa kapsayıcıları (tam çözüm) bir grup aynı anda hata ayıklama.</span><span class="sxs-lookup"><span data-stu-id="6321a-107">Even more, with Visual Studio 2017, in addition to being able to run and debug a single container, you also can run and debug a group of containers (a whole solution) at the same time if they are defined in the same docker-compose.yml file at the solution level.</span></span>

## <a name="configuring-your-local-environment"></a><span data-ttu-id="6321a-108">Yerel ortamınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6321a-108">Configuring your local environment</span></span>

<span data-ttu-id="6321a-109">Windows için Docker en son sürümleri ile Kurulum sonucunun aşağıdaki başvurularında açıklandığı gibi olduğundan Docker uygulamaları geliştirmek için her zamankinden daha kolay olur.</span><span class="sxs-lookup"><span data-stu-id="6321a-109">With the latest versions of Docker for Windows, it is easier than ever to develop Docker applications because the setup is straightforward, as explained in the following references.</span></span>

<span data-ttu-id="6321a-110">**Daha fazla bilgi:** Docker için Windows'u yükleme hakkında daha fazla bilgi için şuraya gidin <https://docs.docker.com/docker-for-windows/>.</span><span class="sxs-lookup"><span data-stu-id="6321a-110">**More info:** To learn more about installing Docker for Windows, go to <https://docs.docker.com/docker-for-windows/>.</span></span>

<span data-ttu-id="6321a-111">Visual Studio 2015 kullanıyorsanız, güncelleştirme 3 veya sonraki bir sürümünü artı Docker için Visual Studio Araçları olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6321a-111">If you're using Visual Studio 2015, you must have Update 3 or a later version plus the Visual Studio Tools for Docker.</span></span>

<span data-ttu-id="6321a-112">**Daha fazla bilgi:** Visual Studio'yu yükleme ile ilgili yönergeler için Git [https://www.visualstudio.com/ \ ürünler/vs-2015-ürün-sürümleri](https://www.visualstudio.com/products/vs-2015-product-editions).</span><span class="sxs-lookup"><span data-stu-id="6321a-112">**More info:** For instructions on installing Visual Studio, go to [https://www.visualstudio.com/\ products/vs-2015-product-editions](https://www.visualstudio.com/products/vs-2015-product-editions).</span></span>

<span data-ttu-id="6321a-113">Docker için Visual Studio araçlarını yükleme hakkında daha fazla bilgi görmek için Git <http://aka.ms/vstoolsfordocker> ve <https://docs.microsoft.com/dotnet/articles/core/docker/visual-studio-tools-for-docker>.</span><span class="sxs-lookup"><span data-stu-id="6321a-113">To see more about installing Visual Studio Tools for Docker, go to <http://aka.ms/vstoolsfordocker> and <https://docs.microsoft.com/dotnet/articles/core/docker/visual-studio-tools-for-docker>.</span></span>

<span data-ttu-id="6321a-114">Visual Studio 2017 kullanıyorsanız, Docker destek zaten dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6321a-114">If you're using Visual Studio 2017, Docker support is already included.</span></span>

## <a name="using-docker-tools-in-visual-studio-2015"></a><span data-ttu-id="6321a-115">Visual Studio 2015'te Docker araçlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="6321a-115">Using Docker Tools in Visual Studio 2015</span></span>

<span data-ttu-id="6321a-116">Docker için Visual Studio Araçları geliştirmek ve yerel olarak Linux Docker ana bilgisayar veya VM ya da Windows Kapsayıcılarınızı doğrudan Windows'da Linux için Docker kapsayıcılarınızı doğrulamak için tutarlı bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="6321a-116">The Visual Studio Tools for Docker provides a consistent way to develop and validate locally your Docker containers for Linux in a Linux Docker host or VM, or your Windows Containers directly on Windows.</span></span>

<span data-ttu-id="6321a-117">Tek bir kapsayıcı kullanıyorsanız, .NET Core projenize Docker desteğini etkinleştirmek için başlamak için gereken ilk şey olur.</span><span class="sxs-lookup"><span data-stu-id="6321a-117">If you're using a single container, the first thing you need to begin is to turn on Docker support into your .NET Core project.</span></span> <span data-ttu-id="6321a-118">Bunu yapmak için Şekil 4-25 gösterildiği gibi proje dosyasını sağ tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6321a-118">To do this, right-click your project file, as shown in Figure 4-25.</span></span>

![https://i1.visualstudiogallery.msdn.s-MSFT.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4/image/File/205468/1/Add-docker-support.PNG](./media/image31.png)

<span data-ttu-id="6321a-120">Şekil 4-25: açma, Visual Studio projesi için Docker desteği</span><span class="sxs-lookup"><span data-stu-id="6321a-120">Figure 4-25: Turning on Docker support for your Visual Studio project</span></span>

## <a name="using-docker-tools-in-visual-studio-2017"></a><span data-ttu-id="6321a-121">Visual Studio 2017 içinde Docker araçlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="6321a-121">Using Docker Tools in Visual Studio 2017</span></span>

<span data-ttu-id="6321a-122">Eklediğinizde Docker destek hizmeti projesine çözümünüzde (bkz. Şekil 4-26), Visual Studio değil yalnızca ekleme DockerFile dosyayı projenize, bunu ayrıca bir hizmet bölümü çözümünüzün docker-compose.yml dosyaları (veya bunlar almadıysanız dosyalar oluşturma ekleme var).</span><span class="sxs-lookup"><span data-stu-id="6321a-122">When you add Docker support to a service project in your solution (see Figure 4-26), Visual Studio is not just adding a DockerFile file to your project, it also is adding a service section in your solution's docker-compose.yml files (or creating the files if they didn't exist).</span></span> <span data-ttu-id="6321a-123">Multicontainer çözümünüzü oluşturmaya başlamak için kolay bir yoludur.; ardından docker-compose.yml dosyaları açmak ve bunları ile ek özellikler güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="6321a-123">It's an easy way to begin composing your multicontainer solution; you then can open the docker-compose.yml files and update them with additional features.</span></span>

![](./media/image32.png)

<span data-ttu-id="6321a-124">Şekil 4-26: Visual Studio 2017 proje Docker çözümü desteği kapatma</span><span class="sxs-lookup"><span data-stu-id="6321a-124">Figure 4-26: Turning on Docker Solution support in a Visual Studio 2017 project</span></span>

<span data-ttu-id="6321a-125">Bu eylem, yalnızca DockerFile projenize ekler, bir genel docker-çözüm düzeyinde ayarlanan compose.yml için gerekli yapılandırma satırlık bir kod da ekler.</span><span class="sxs-lookup"><span data-stu-id="6321a-125">This action not only adds the DockerFile to your project, it also adds the required configuration lines of code to a global docker-compose.yml set at the solution level.</span></span>

<span data-ttu-id="6321a-126">Ayrıca Docker desteği Visual Studio 2017 ' bir ASP.NET Core projesi oluştururken, Şekil 4-27'de gösterildiği gibi kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6321a-126">You also can turn on Docker support when creating an ASP.NET Core project in Visual Studio 2017, as shown in Figure 4-27.</span></span>

![](./media/image33.png)

<span data-ttu-id="6321a-127">Şekil 4-27: açma bir projesi oluştururken, Docker desteği</span><span class="sxs-lookup"><span data-stu-id="6321a-127">Figure 4-27: Turning on Docker support when creating a project</span></span>

<span data-ttu-id="6321a-128">Çözüm Gezgini'nde yeni düğümü ağacı eklenen docker-compose.yml dosyalarla ayrıca Visual Studio çözümünüzde Docker destek ekledikten sonra Şekil 4-28'de gösterildiği gibi görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="6321a-128">After you add Docker support to your solution in Visual Studio, you also will see a new node tree in Solution Explorer with the added docker-compose.yml files, as depicted in Figure 4-28.</span></span>

![](./media/image34.PNG)

<span data-ttu-id="6321a-129">Şekil 4-28: docker-compose.yml dosyaları şimdi Çözüm Gezgini'nde görüntüler.</span><span class="sxs-lookup"><span data-stu-id="6321a-129">Figure 4-28: docker-compose.yml files now display in Solution Explorer</span></span>

<span data-ttu-id="6321a-130">Bir multicontainer dağıtabilirsiniz çalıştırdığınızda tek docker-compose.yml dosyası kullanarak uygulama docker-oluşturun; değerleri (Geliştirme karşı üretim) ortamını ve yürütme bağlı olarak kılabilir ancak, Visual Studio, bir grup ekler türü (hata ayıklama ve yayın).</span><span class="sxs-lookup"><span data-stu-id="6321a-130">You could deploy a multicontainer application by using a single docker-compose.yml file when you run docker-compose up; however, Visual Studio adds a group of them, so you can override values depending on the environment (development versus production) and the execution type (release versus debug).</span></span> <span data-ttu-id="6321a-131">Bu yetenek, daha iyi sonraki bölümde açıklanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6321a-131">This capability will be better explained in later chapters.</span></span>

<span data-ttu-id="6321a-132">**Daha fazla bilgi:** Hizmetleri uygulaması ve Docker için Visual Studio Araçları kullanımı hakkında daha fazla ayrıntı için aşağıdaki makaleleri okuyun:</span><span class="sxs-lookup"><span data-stu-id="6321a-132">**More info:** For further details on the services implementation and use of Visual Studio Tools for Docker, read the following articles:</span></span>

<span data-ttu-id="6321a-133">Yapı, hata ayıklama, güncelleştirme ve yenileme yerel bir Docker kapsayıcısı uygulamalarında: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span><span class="sxs-lookup"><span data-stu-id="6321a-133">Build, debug, update, and refresh apps in a local Docker container: [https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh/](https://docs.microsoft.com/azure/vs-azure-tools-docker-edit-and-refresh)</span></span>

<span data-ttu-id="6321a-134">Bir ASP.NET kapsayıcısı uzak bir Docker konağına dağıtın: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span><span class="sxs-lookup"><span data-stu-id="6321a-134">Deploy an ASP.NET container to a remote Docker host: [https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker/](https://docs.microsoft.com/azure/vs-azure-tools-docker-hosting-web-apps-in-docker)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="6321a-135">[Önceki] (docker-apps-iç-döngü-workflow.md) [sonraki] (set-up-windows-containers-with-powershell.md)</span><span class="sxs-lookup"><span data-stu-id="6321a-135">[Previous] (docker-apps-inner-loop-workflow.md) [Next] (set-up-windows-containers-with-powershell.md)</span></span>
