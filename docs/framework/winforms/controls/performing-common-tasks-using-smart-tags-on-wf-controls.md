---
title: "İzlenecek yol: Windows Forms Denetimlerindeki Akıllı Etiketleri Kullanarak Ortak Görevleri Gerçekleştirme"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- DesignerAction object model
- smart tags
- designer actions
ms.assetid: cac337e6-00f6-4584-80f4-75728f5ea113
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 2e6b815be85576f037e0f24668c44756b95abd6e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="walkthrough-performing-common-tasks-using-smart-tags-on-windows-forms-controls"></a><span data-ttu-id="fa2ea-102">İzlenecek yol: Windows Forms Denetimlerindeki Akıllı Etiketleri Kullanarak Ortak Görevleri Gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="fa2ea-102">Walkthrough: Performing Common Tasks Using Smart Tags on Windows Forms Controls</span></span>
<span data-ttu-id="fa2ea-103">Windows Forms uygulamanız için formlar ve denetimler oluşturmak gibi art arda gerçekleştirecek pek çok görev vardır.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-103">As you construct forms and controls for your Windows Forms application, there are many tasks you will perform repeatedly.</span></span> <span data-ttu-id="fa2ea-104">Bunlar, karşınıza çıkacak sık gerçekleştirilen görevlerden bazıları şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fa2ea-104">These are some of the commonly performed tasks you will encounter:</span></span>  
  
-   <span data-ttu-id="fa2ea-105">Ekleyerek veya üzerinde bir sekme kaldırarak bir <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-105">Adding or removing a tab on a <xref:System.Windows.Forms.TabControl>.</span></span>  
  
-   <span data-ttu-id="fa2ea-106">Bir denetim kendi üst yerleştirme.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-106">Docking a control to its parent.</span></span>  
  
-   <span data-ttu-id="fa2ea-107">Yönünü değiştirme bir <xref:System.Windows.Forms.SplitContainer> denetim.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-107">Changing the orientation of a <xref:System.Windows.Forms.SplitContainer> control.</span></span>  
  
 <span data-ttu-id="fa2ea-108">Geliştirme hızlandırmak için tasarım zamanında bunları tek bir hareketi gibi genel görevleri gerçekleştirmenize olanak sağlayan bağlama duyarlı menüler olan akıllı etiketler birçok denetim sunar.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-108">To speed development, many controls offer smart tags, which are context-sensitive menus that allow you to perform common tasks like these in a single gesture at design time.</span></span> <span data-ttu-id="fa2ea-109">Bu görevleri adlı *akıllı etiket fiiller*.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-109">These tasks are called *smart-tag verbs*.</span></span>  
  
 <span data-ttu-id="fa2ea-110">Akıllı etiketler Tasarımcısı'nda ömrü için bir denetim örneğine eklenen kalır ve her zaman kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-110">Smart tags remain attached to a control instance for its lifetime in the designer and are always available.</span></span>  
  
 <span data-ttu-id="fa2ea-111">Bu örneklerde gösterilen görevler aşağıdakileri içerir:</span><span class="sxs-lookup"><span data-stu-id="fa2ea-111">Tasks illustrated in this walkthrough include:</span></span>  
  
-   <span data-ttu-id="fa2ea-112">Windows Forms projesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa2ea-112">Creating a Windows Forms project</span></span>  
  
-   <span data-ttu-id="fa2ea-113">Akıllı etiketleri kullanarak</span><span class="sxs-lookup"><span data-stu-id="fa2ea-113">Using smart tags</span></span>  
  
-   <span data-ttu-id="fa2ea-114">Akıllı etiketler devre dışı bırakma ve etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="fa2ea-114">Enabling and Disabling Smart Tags</span></span>  
  
 <span data-ttu-id="fa2ea-115">İşiniz bittiğinde, bu önemli yerleşim özellikleri tarafından oynadığı rol anlaşılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-115">When you are finished, you will have an understanding of the role played by these important layout features.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fa2ea-116">Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-116">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="fa2ea-117">Ayarlarınızı değiştirmek için tercih **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-117">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="fa2ea-118">Daha fazla bilgi için bkz: [Visual Studio'da geliştirme ayarlarını özelleştirme](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span><span class="sxs-lookup"><span data-stu-id="fa2ea-118">For more information, see [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/en-us/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span></span>  
  
## <a name="creating-the-project"></a><span data-ttu-id="fa2ea-119">Projeyi Oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa2ea-119">Creating the Project</span></span>  
 <span data-ttu-id="fa2ea-120">Projeyi oluşturmak ve formu ayarlamak için ilk adımdır bakın.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-120">The first step is to create the project and set up the form.</span></span>  
  
#### <a name="to-create-the-project"></a><span data-ttu-id="fa2ea-121">Proje oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="fa2ea-121">To create the project</span></span>  
  
1.  <span data-ttu-id="fa2ea-122">"SmartTagsExample" adlı bir Windows tabanlı bir uygulama projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-122">Create a Windows-based application project called "SmartTagsExample".</span></span> <span data-ttu-id="fa2ea-123">Ayrıntılar için bkz [nasıl yapılır: bir Windows uygulaması projesi oluşturduğunuzda](http://msdn.microsoft.com/en-us/b2f93fed-c635-4705-8d0e-cf079a264efa).</span><span class="sxs-lookup"><span data-stu-id="fa2ea-123">For details, see [How to: Create a Windows Application Project](http://msdn.microsoft.com/en-us/b2f93fed-c635-4705-8d0e-cf079a264efa).</span></span>  
  
2.  <span data-ttu-id="fa2ea-124">Formda seçin **Windows Form Tasarımcısı**.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-124">Select the form in the **Windows Forms Designer**.</span></span>  
  
## <a name="using-smart-tags"></a><span data-ttu-id="fa2ea-125">Akıllı etiketleri kullanarak</span><span class="sxs-lookup"><span data-stu-id="fa2ea-125">Using Smart Tags</span></span>  
 <span data-ttu-id="fa2ea-126">Akıllı etiketler her zaman bunları teklif denetimlerinde tasarım zamanında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-126">Smart tags are always available at design time on controls that offer them.</span></span>  
  
#### <a name="to-use-smart-tags"></a><span data-ttu-id="fa2ea-127">Akıllı etiketleri kullanma</span><span class="sxs-lookup"><span data-stu-id="fa2ea-127">To use smart tags</span></span>  
  
1.  <span data-ttu-id="fa2ea-128">Sürükleme bir <xref:System.Windows.Forms.TabControl> gelen **araç** formunuza.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-128">Drag a <xref:System.Windows.Forms.TabControl> from the **Toolbox** onto your form.</span></span> <span data-ttu-id="fa2ea-129">Akıllı etiket karakteri unutmayın (![akıllı etiket karakteri](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) görünen üzerinde yan, <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-129">Note the smart-tag glyph (![Smart Tag Glyph](../../../../docs/framework/winforms/controls/media/vs-winformsmttagglyph.gif "VS_WinFormSmtTagGlyph")) that appears on the side of the <xref:System.Windows.Forms.TabControl>.</span></span>  
  
2.  <span data-ttu-id="fa2ea-130">Akıllı etiket karakteri'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-130">Click the smart-tag glyph.</span></span> <span data-ttu-id="fa2ea-131">Karakter yanında görüntülenen kısayol menüsünden seçin **sekmesi Ekle** öğesi.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-131">In the shortcut menu that appears next to the glyph, select the **Add Tab** item.</span></span> <span data-ttu-id="fa2ea-132">Yeni bir sekme sayfası eklenir gözlemlemek <xref:System.Windows.Forms.TabControl>.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-132">Observe that a new tab page is added to the <xref:System.Windows.Forms.TabControl>.</span></span>  
  
3.  <span data-ttu-id="fa2ea-133">Sürükleme bir <xref:System.Windows.Forms.TableLayoutPanel> gelen denetim **araç** formunuza.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-133">Drag a <xref:System.Windows.Forms.TableLayoutPanel> control from the **Toolbox** onto your form.</span></span>  
  
4.  <span data-ttu-id="fa2ea-134">Akıllı etiket karakteri'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-134">Click the smart-tag glyph.</span></span> <span data-ttu-id="fa2ea-135">Karakter yanında görüntülenen kısayol menüsünden seçin **Sütun Ekle** öğesi.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-135">In the shortcut menu that appears next to the glyph, select the **Add Column** item.</span></span> <span data-ttu-id="fa2ea-136">Yeni bir sütun eklenir gözlemlemek <xref:System.Windows.Forms.TableLayoutPanel> denetim.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-136">Observe that a new column is added to the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>  
  
5.  <span data-ttu-id="fa2ea-137">Sürükleme bir <xref:System.Windows.Forms.SplitContainer> gelen denetim **araç** formunuza.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-137">Drag a <xref:System.Windows.Forms.SplitContainer> control from the **Toolbox** onto your form.</span></span>  
  
6.  <span data-ttu-id="fa2ea-138">Akıllı etiket karakteri'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-138">Click the smart-tag glyph.</span></span> <span data-ttu-id="fa2ea-139">Karakter yanında görüntülenen kısayol menüsünden seçin **Yatay bölümlendirici yönlendirmesini** öğesi.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-139">In the shortcut menu that appears next to the glyph, select the **Horizontal splitter orientation** item.</span></span> <span data-ttu-id="fa2ea-140">Görüntülendiğini <xref:System.Windows.Forms.SplitContainer> denetimin ayırıcıyı olduğu şimdi yatay yönelimli.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-140">Observe that the <xref:System.Windows.Forms.SplitContainer> control's splitter bar is now oriented horizontally.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fa2ea-141">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="fa2ea-141">See Also</span></span>  
 <xref:System.Windows.Forms.TextBox>  
 <xref:System.Windows.Forms.TabControl>  
 <xref:System.Windows.Forms.SplitContainer>  
 <xref:System.ComponentModel.Design.DesignerActionList>  
 [<span data-ttu-id="fa2ea-142">İzlenecek yol: Bir Windows Forms bileşenine akıllı etiketler ekleme</span><span class="sxs-lookup"><span data-stu-id="fa2ea-142">Walkthrough: Adding Smart Tags to a Windows Forms Component</span></span>](http://msdn.microsoft.com/library/a6814169-fa7d-4527-808c-637ca5c95f63)