---
title: "Yönetilen HTML Belgesi Nesne Modelindeki Çerçevelere Erişme"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- HTML [Windows Forms], dOM
- managed HTML DOM
- HTML [Windows Forms], managed
- HTML DOM [Windows Forms], managed
- frames [Windows Forms], accessing
- DOM [Windows Forms], accessing frames in managed HTML
ms.assetid: cdeeaa22-0be4-4bbf-9a75-4ddc79199f8d
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: c8766e33f0fb253d532ff7161ed0a1e7842d0c50
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="accessing-frames-in-the-managed-html-document-object-model"></a><span data-ttu-id="27731-102">Yönetilen HTML Belgesi Nesne Modelindeki Çerçevelere Erişme</span><span class="sxs-lookup"><span data-stu-id="27731-102">Accessing Frames in the Managed HTML Document Object Model</span></span>
<span data-ttu-id="27731-103">Bazı HTML belgeleri çıkışı oluşur *çerçeveleri*, ya da kendi ayrı HTML belgeleri tutabilir windows.</span><span class="sxs-lookup"><span data-stu-id="27731-103">Some HTML documents are composed out of *frames*, or windows that can hold their own distinct HTML documents.</span></span> <span data-ttu-id="27731-104">Çerçeveler kullanarak diğer çerçeveler sürekli içeriklerini değiştirme sırasında bir veya daha fazla parça sayfasının bir gezinti çubuğu gibi statik kalır HTML sayfaları oluşturmak kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="27731-104">Using frames makes it easy to create HTML pages in which one or more pieces of the page remain static, such as a navigation bar, while other frames constantly change their content.</span></span>  
  
 <span data-ttu-id="27731-105">HTML yazarlarının çerçeveler iki yoldan biriyle oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="27731-105">HTML authors can create frames in one of two ways:</span></span>  
  
-   <span data-ttu-id="27731-106">Kullanarak `FRAMESET` ve `FRAME` sabit pencerelerini etiketler.</span><span class="sxs-lookup"><span data-stu-id="27731-106">Using the `FRAMESET` and `FRAME` tags, which create fixed windows.</span></span>  
  
 <span data-ttu-id="27731-107">veya</span><span class="sxs-lookup"><span data-stu-id="27731-107">-or-</span></span>  
  
-   <span data-ttu-id="27731-108">Kullanarak `IFRAME` çalışma zamanında konumlandırılmasına kayan bir pencere oluşturur etiketi.</span><span class="sxs-lookup"><span data-stu-id="27731-108">Using the `IFRAME` tag, which creates a floating window that can be repositioned at run time.</span></span>  
  
1.  <span data-ttu-id="27731-109">Çerçeve HTML belgeleri içerdiğinden, bunlar belge nesne modeli (DOM) pencere öğeleri ve çerçeve öğeler temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="27731-109">Because frames contain HTML documents, they are represented in the Document Object Model (DOM) as both window elements and frame elements.</span></span>  
  
2.  <span data-ttu-id="27731-110">Eriştiğinizde bir `FRAME` veya `IFRAME` çerçeveler koleksiyonunu kullanarak etiketi <xref:System.Windows.Forms.HtmlWindow>, çerçeveye karşılık gelen pencere öğesi alınıyor.</span><span class="sxs-lookup"><span data-stu-id="27731-110">When you access a `FRAME` or `IFRAME` tag by using the Frames collection of <xref:System.Windows.Forms.HtmlWindow>, you are retrieving the window element corresponding to the frame.</span></span> <span data-ttu-id="27731-111">Bu özelliklerin tümü çerçevenin dinamik, geçerli URL, belge ve boyutu gibi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="27731-111">This represents all of the frame's dynamic properties, such as its current URL, document, and size.</span></span>  
  
3.  <span data-ttu-id="27731-112">Eriştiğinizde bir `FRAME` veya `IFRAME` kullanarak etiketi <xref:System.Windows.Forms.HtmlWindow.WindowFrameElement%2A> özelliği <xref:System.Windows.Forms.HtmlWindow>, <xref:System.Windows.Forms.HtmlElement.Children%2A> koleksiyonu veya gibi yöntemler <xref:System.Windows.Forms.HtmlElementCollection.GetElementsByName%2A> veya <xref:System.Windows.Forms.HtmlDocument.GetElementById%2A>, çerçeve öğesi alınıyor.</span><span class="sxs-lookup"><span data-stu-id="27731-112">When you access a `FRAME` or `IFRAME` tag by using the <xref:System.Windows.Forms.HtmlWindow.WindowFrameElement%2A> property of <xref:System.Windows.Forms.HtmlWindow>, the <xref:System.Windows.Forms.HtmlElement.Children%2A> collection, or methods such as <xref:System.Windows.Forms.HtmlElementCollection.GetElementsByName%2A> or <xref:System.Windows.Forms.HtmlDocument.GetElementById%2A>, you are retrieving the frame element.</span></span> <span data-ttu-id="27731-113">Bu, özgün HTML dosyasında belirtilen URL gibi çerçeve statik özelliklerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="27731-113">This represents the static properties of the frame, including the URL specified in the original HTML file.</span></span>  
  
## <a name="frames-and-security"></a><span data-ttu-id="27731-114">Çerçeve ve güvenlik</span><span class="sxs-lookup"><span data-stu-id="27731-114">Frames and Security</span></span>  
 <span data-ttu-id="27731-115">Yönetilen HTML DOM olarak bilinen bir güvenlik önlemi uygulayan olgu tarafından çerçeveler erişimi karmaşık *çerçeveler arası komut dosyası güvenlik*.</span><span class="sxs-lookup"><span data-stu-id="27731-115">Access to frames is complicated by the fact that the managed HTML DOM implements a security measure known as *cross-frame scripting security*.</span></span> <span data-ttu-id="27731-116">Bir belge içeriyorsa bir `FRAMESET` iki veya daha fazla ile `FRAME`s farklı etki alanlarında, bunlar `FRAME`s birbiriyle çalışamazsınız.</span><span class="sxs-lookup"><span data-stu-id="27731-116">If a document contains a `FRAMESET` with two or more `FRAME`s in different domains, these `FRAME`s cannot interact with one another.</span></span> <span data-ttu-id="27731-117">Diğer bir deyişle, bir `FRAME` Web sitesinden görüntüler içerik bilgilerinde erişemiyor bir `FRAME` http://www.adatum.com/ gibi bir üçüncü taraf site barındıran.</span><span class="sxs-lookup"><span data-stu-id="27731-117">In other words, a `FRAME` that displays content from your Web site cannot access information in a `FRAME` that hosts a third-party site such as http://www.adatum.com/.</span></span> <span data-ttu-id="27731-118">Bu güvenlik düzeyinde uygulanır <xref:System.Windows.Forms.HtmlWindow> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="27731-118">This security is implemented at the level of the <xref:System.Windows.Forms.HtmlWindow> class.</span></span> <span data-ttu-id="27731-119">Hakkında genel bilgi edinebilirsiniz bir `FRAME` URL'sini, ancak gibi başka bir Web sitesi barındırma erişemiyor olacaktır, <xref:System.Windows.Forms.HtmlWindow.Document%2A> veya boyutu ya da kendi barındırma konumu değiştirmek `FRAME` veya `IFRAME`.</span><span class="sxs-lookup"><span data-stu-id="27731-119">You can obtain general information about a `FRAME` hosting another Web site, such as its URL, but you will be unable to access its <xref:System.Windows.Forms.HtmlWindow.Document%2A> or change the size or location of its hosting `FRAME` or `IFRAME`.</span></span>  
  
 <span data-ttu-id="27731-120">Bu kuralı kullanarak açın windows için de geçerlidir <xref:System.Windows.Forms.HtmlWindow.Open%2A> ve <xref:System.Windows.Forms.HtmlWindow.OpenNew%2A> yöntemleri.</span><span class="sxs-lookup"><span data-stu-id="27731-120">This rule also applies to windows that you open using the <xref:System.Windows.Forms.HtmlWindow.Open%2A> and <xref:System.Windows.Forms.HtmlWindow.OpenNew%2A> methods.</span></span> <span data-ttu-id="27731-121">Açtığınız pencere barındırılan sayfasından farklı bir etki alanında ise <xref:System.Windows.Forms.WebBrowser> denetimi, olmayacak bu pencereyi taşıyabilir veya içeriğini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="27731-121">If the window you open is in a different domain from the page hosted in the <xref:System.Windows.Forms.WebBrowser> control, you will not be able to move that window or examine its contents.</span></span> <span data-ttu-id="27731-122">Kullanıyorsanız bu kısıtlamaları da zorlanır <xref:System.Windows.Forms.WebBrowser> Windows Forms tabanlı uygulamanızı dağıtmak için kullanılan Web sitesinden farklı bir Web sitesini görüntülemek için denetim.</span><span class="sxs-lookup"><span data-stu-id="27731-122">These restrictions are also enforced if you use the <xref:System.Windows.Forms.WebBrowser> control to display a Web site that is different from the Web site used to deploy your Windows Forms-based application.</span></span> <span data-ttu-id="27731-123">Kullanırsanız [!INCLUDE[ndptecclick](../../../../includes/ndptecclick-md.md)] uygulamanız bir Web sitesinden ve yüklemek için dağıtım teknolojisini kullanan <xref:System.Windows.Forms.WebBrowser> Web sitesini B görüntülemek için access Web sitesinin B'nin veri mümkün olmaz.</span><span class="sxs-lookup"><span data-stu-id="27731-123">If you use [!INCLUDE[ndptecclick](../../../../includes/ndptecclick-md.md)] deployment technology to install your application from Web site A, and you use the <xref:System.Windows.Forms.WebBrowser> to display Web site B, you will not be able to access Web site B's data.</span></span>  
  
 <span data-ttu-id="27731-124">Siteler arası komut dosyası hakkında daha fazla bilgi için bkz:[hakkında çerçeveler arası komut dosyası oluşturma ve güvenlik](http://msdn.microsoft.com/library/ms533028.aspx).</span><span class="sxs-lookup"><span data-stu-id="27731-124">For more information about cross-site scripting, see[About Cross-Frame Scripting and Security](http://msdn.microsoft.com/library/ms533028.aspx).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27731-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="27731-125">See Also</span></span>  
 [<span data-ttu-id="27731-126">ÇERÇEVE öğesi &#124; çerçeve nesnesi</span><span class="sxs-lookup"><span data-stu-id="27731-126">FRAME Element &#124; frame Object</span></span>](http://msdn.microsoft.com/library/ms535250.aspx)  
 [<span data-ttu-id="27731-127">Yönetilen HTML belgesi nesne modelini kullanma</span><span class="sxs-lookup"><span data-stu-id="27731-127">Using the Managed HTML Document Object Model</span></span>](../../../../docs/framework/winforms/controls/using-the-managed-html-document-object-model.md)