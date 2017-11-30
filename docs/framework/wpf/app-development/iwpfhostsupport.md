---
title: IWpfHostSupport
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: IWpfHostSupport interface [WPF]
ms.assetid: cc5a0281-de81-4cc1-87e4-0e46b1a811e9
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 85d4ed09d6c5ca17e148d531e6aac483ff737d51
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2017
---
# <a name="iwpfhostsupport"></a><span data-ttu-id="5a8fd-102">IWpfHostSupport</span><span class="sxs-lookup"><span data-stu-id="5a8fd-102">IWpfHostSupport</span></span>
<span data-ttu-id="5a8fd-103">Ana bilgisayar uygulamaları [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] PresentationHost.exe üzerinden içerik PresentationHost.exe ve ana bilgisayar arasında tümleştirme noktası sağlamak için bu arabirimi uygulayan.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-103">Applications that host [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] content via PresentationHost.exe implement this interface to provide a point of integration between the host and PresentationHost.exe.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5a8fd-104">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="5a8fd-104">Remarks</span></span>  
 [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)]<span data-ttu-id="5a8fd-105">Web tarayıcıları gibi uygulamaları barındırabilir [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] dahil olmak üzere içerik [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] ve XAML kaybedilir.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-105"> applications such as Web browsers can host [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] content, including [!INCLUDE[TLA#tla_xbap#plural](../../../../includes/tlasharptla-xbapsharpplural-md.md)] and loose XAML.</span></span> <span data-ttu-id="5a8fd-106">Ana bilgisayara [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] içerik [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] uygulamaları oluşturma örneği [WebBrowser denetimi](http://go.microsoft.com/fwlink/?LinkId=97911).</span><span class="sxs-lookup"><span data-stu-id="5a8fd-106">To host [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] content, [!INCLUDE[TLA#tla_win32](../../../../includes/tlasharptla-win32-md.md)] applications create an instance of the [WebBrowser control](http://go.microsoft.com/fwlink/?LinkId=97911).</span></span> <span data-ttu-id="5a8fd-107">Barındırılacak şekilde [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] barındırılan sağlar PresentationHost.exe örneği oluşturur [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] görüntülenmek üzere ana içerik [WebBrowser denetimi](http://go.microsoft.com/fwlink/?LinkId=97911).</span><span class="sxs-lookup"><span data-stu-id="5a8fd-107">To be hosted, [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] creates an instance of PresentationHost.exe, which provides the hosted [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] content to the host for display in the [WebBrowser control](http://go.microsoft.com/fwlink/?LinkId=97911).</span></span>  
  
 <span data-ttu-id="5a8fd-108">Tarafından etkinleştirilen tümleştirme `IWpfHostSupport` PresentationHost.exe'ye izin verir:</span><span class="sxs-lookup"><span data-stu-id="5a8fd-108">The integration enabled by `IWpfHostSupport` allows PresentationHost.exe to:</span></span>  
  
-   <span data-ttu-id="5a8fd-109">Bul ve ana uygulamanın ilgilendiği ham giriş aygıtlarını (İnsan Arabirimi aygıtları) ile kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-109">Discover and register with the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
-   <span data-ttu-id="5a8fd-110">Giriş kayıtlı ham giriş aygıtlarını ve uygun iletileri yönlendirmek için konak uygulama iletilerini.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-110">Receive input messages from the registered raw input devices and forward appropriate messages to the host application.</span></span>  
  
-   <span data-ttu-id="5a8fd-111">Özel ilerleme durumu ve hata kullanıcı arabirimleri için ana bilgisayar uygulaması sorgu.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-111">Query the host application for custom progress and error user interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5a8fd-112">Bu API yalnızca hedeflenen ve yerel istemci makinesinde kullanımı desteklenen</span><span class="sxs-lookup"><span data-stu-id="5a8fd-112">This API is only intended and supported for use on the local client machine</span></span>  
  
## <a name="members"></a><span data-ttu-id="5a8fd-113">Üyeler</span><span class="sxs-lookup"><span data-stu-id="5a8fd-113">Members</span></span>  
  
|<span data-ttu-id="5a8fd-114">Üye</span><span class="sxs-lookup"><span data-stu-id="5a8fd-114">Member</span></span>|<span data-ttu-id="5a8fd-115">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5a8fd-115">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="5a8fd-116">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="5a8fd-116">GetRawInputDevices</span></span>](../../../../docs/framework/wpf/app-development/getrawinputdevices.md)|<span data-ttu-id="5a8fd-117">Ana uygulamanın ilgilendiği ham giriş aygıtlarını (İnsan Arabirimi aygıtları) keşfetmek için PresentationHost.exe'ye izin verir.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-117">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>|  
|[<span data-ttu-id="5a8fd-118">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="5a8fd-118">FilterInputMessage</span></span>](../../../../docs/framework/wpf/app-development/filterinputmessage.md)|<span data-ttu-id="5a8fd-119">E_NOTIMPL sürece bir ileti alındığında PresentationHost.exe tarafından çağrılır.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-119">Called by PresentationHost.exe whenever a message is received unless E_NOTIMPL is returned.</span></span>|  
|[<span data-ttu-id="5a8fd-120">GetCustomUI</span><span class="sxs-lookup"><span data-stu-id="5a8fd-120">GetCustomUI</span></span>](../../../../docs/framework/wpf/app-development/getcustomui.md)|<span data-ttu-id="5a8fd-121">Varsayılan olarak, PresentationHost.exe kendi dağıtımının ilerleme durumunu ve dağıtım hatası WPF içeriği dağıtıldığında görüntülenen kullanıcı arabirimleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="5a8fd-121">By default, PresentationHost.exe provides its own deployment progress and deployment error user interfaces that are displayed when WPF content is deployed.</span></span>|