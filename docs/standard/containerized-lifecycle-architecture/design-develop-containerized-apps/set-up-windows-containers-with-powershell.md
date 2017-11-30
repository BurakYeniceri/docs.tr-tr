---
title: "(Standart Docker tabanlı) Windows kapsayıcıları ayarlamak için bir DockerFile Windows PowerShell komutlarını kullanma"
description: "Microsoft Platformu ve araçları ile kapsayıcılı Docker uygulama yaşam döngüsü"
keywords: "Docker, mikro, ASP.NET, kapsayıcı"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/19/2017
ms.openlocfilehash: f7e92b0f1c749e2c00e3afc4ffcfc2fc88d7628f
ms.sourcegitcommit: 6f49c973f62855ffd6c4a322903e7dd50c5c1b50
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2017
---
# <a name="using-windows-powershell-commands-in-a-dockerfile-to-set-up-windows-containers-docker-standard-based"></a><span data-ttu-id="ff435-104">(Standart Docker tabanlı) Windows kapsayıcıları ayarlamak için bir DockerFile Windows PowerShell komutlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="ff435-104">Using Windows PowerShell commands in a DockerFile to set up Windows Containers (Docker standard based)</span></span>

<span data-ttu-id="ff435-105">İle [Windows kapsayıcıları](https://msdn.microsoft.com/en-us/virtualization/windowscontainers/about/about_overview), var olan Windows uygulamalarınız Docker resimlere dönüştürmek ve bunları Docker ekosistemi geri kalanı ile aynı araçlarıyla dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff435-105">With [Windows Containers](https://msdn.microsoft.com/en-us/virtualization/windowscontainers/about/about_overview), you can convert your existing Windows applications to Docker images and deploy them with the same tools as the rest of the Docker ecosystem.</span></span>

<span data-ttu-id="ff435-106">Windows kapsayıcılar kullanmak için Windows PowerShell komutları DockerFile, yazma aşağıdaki örnekte gösterildiği gibi yeterlidir:</span><span class="sxs-lookup"><span data-stu-id="ff435-106">To use Windows Containers, you just need to write Windows PowerShell commands in the DockerFile, as demonstrated in the following example:</span></span>

```
FROM microsoft/windowsservercore
LABEL Description="IIS" Vendor="Microsoft" Version="10"
RUN powershell -Command Add-WindowsFeature Web-Server
CMD [ "ping", "localhost", "-t" ]
```

<span data-ttu-id="ff435-107">Bu durumda, biz IIS yanı sıra bir Windows Server Core temel görüntü yüklemek için Windows PowerShell kullanıyorsanız.</span><span class="sxs-lookup"><span data-stu-id="ff435-107">In this case, we're using Windows PowerShell to install a Windows Server Core base image as well as IIS.</span></span>

<span data-ttu-id="ff435-108">Benzer şekilde, aynı zamanda Windows PowerShell komutlarını geleneksel ASP.NET gibi ek bileşenleri ayarlamak için kullanabileceğinizi 4.x ve .NET 4.6 ya da aşağıda gösterildiği gibi tüm diğer Windows yazılım:</span><span class="sxs-lookup"><span data-stu-id="ff435-108">In a similar way, you also could use Windows PowerShell commands to set up additional components like the traditional ASP.NET 4.x and .NET 4.6 or any other Windows software, as shown here:</span></span>

```
RUN powershell add-windowsfeature web-asp-net45
```

>[!div class="step-by-step"]
<span data-ttu-id="ff435-109">[Önceki] (visual-studio-araçları-için-docker.md) [sonraki] (.. /docker-devops-Workflow/index.MD)</span><span class="sxs-lookup"><span data-stu-id="ff435-109">[Previous] (visual-studio-tools-for-docker.md) [Next] (../docker-devops-workflow/index.md)</span></span>