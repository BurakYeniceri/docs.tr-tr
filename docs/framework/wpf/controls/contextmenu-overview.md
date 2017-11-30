---
title: "ContextMenu Genel Bakışı"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], ContextMenu
- ContextMenu controls [WPF], about ContextMenu controls
ms.assetid: 16909c42-799a-4561-91e0-7d69dcfeea91
caps.latest.revision: "25"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: f3061b7fed225f00bf6bb91efe529de35a5a036a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="contextmenu-overview"></a><span data-ttu-id="25446-102">ContextMenu Genel Bakışı</span><span class="sxs-lookup"><span data-stu-id="25446-102">ContextMenu Overview</span></span>
<span data-ttu-id="25446-103"><xref:System.Windows.Controls.ContextMenu> Sınıf bağlamı özgü kullanarak işlevselliği kullanıma sunan bir öğeyi temsil eder <xref:System.Windows.Controls.Menu>.</span><span class="sxs-lookup"><span data-stu-id="25446-103">The <xref:System.Windows.Controls.ContextMenu> class represents the element that exposes functionality by using a context-specific <xref:System.Windows.Controls.Menu>.</span></span> <span data-ttu-id="25446-104">Genellikle, bir kullanıcı sunan <xref:System.Windows.Controls.ContextMenu> içinde [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] fare düğmesini sağ tıklanarak.</span><span class="sxs-lookup"><span data-stu-id="25446-104">Typically, a user exposes the <xref:System.Windows.Controls.ContextMenu> in the [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] by right-clicking the mouse button.</span></span> <span data-ttu-id="25446-105">Bu konu tanıtır <xref:System.Windows.Controls.ContextMenu> öğesi ve içinde kullanma örnekleri sağlar [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] ve kod.</span><span class="sxs-lookup"><span data-stu-id="25446-105">This topic introduces the <xref:System.Windows.Controls.ContextMenu> element and provides examples of how to use it in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] and code.</span></span>  
  
  
  
<a name="contextmenu_control"></a>   
## <a name="contextmenu-control"></a><span data-ttu-id="25446-106">ContextMenu denetimi</span><span class="sxs-lookup"><span data-stu-id="25446-106">ContextMenu Control</span></span>  
 <span data-ttu-id="25446-107">A <xref:System.Windows.Controls.ContextMenu> belirli bir denetime bağlı.</span><span class="sxs-lookup"><span data-stu-id="25446-107">A <xref:System.Windows.Controls.ContextMenu> is attached to a specific control.</span></span> <span data-ttu-id="25446-108"><xref:System.Windows.Controls.ContextMenu> Öğeleri sağlar, kullanıcılar, komutları veya örneğin, belirli bir denetim ile ilişkili olan seçenekleri belirtin öğelerin bir listesi sunmak bir <xref:System.Windows.Controls.Button>.</span><span class="sxs-lookup"><span data-stu-id="25446-108">The <xref:System.Windows.Controls.ContextMenu> element enables you to present users with a list of items that specify commands or options that are associated with a particular control, for example, a <xref:System.Windows.Controls.Button>.</span></span> <span data-ttu-id="25446-109">Kullanıcılar menüyü görünür yapmak için denetimi sağ tıklatın.</span><span class="sxs-lookup"><span data-stu-id="25446-109">Users right-click the control to make the menu appear.</span></span> <span data-ttu-id="25446-110">Genellikle, tıklatarak bir <xref:System.Windows.Controls.MenuItem> bir alt açar veya bir komutu gerçekleştirmek bir uygulamanın neden olur.</span><span class="sxs-lookup"><span data-stu-id="25446-110">Typically, clicking a <xref:System.Windows.Controls.MenuItem> opens a submenu or causes an application to carry out a command.</span></span>  
  
<a name="creating_contextmenus"></a>   
## <a name="creating-contextmenus"></a><span data-ttu-id="25446-111">ContextMenus oluşturma</span><span class="sxs-lookup"><span data-stu-id="25446-111">Creating ContextMenus</span></span>  
 <span data-ttu-id="25446-112">Aşağıdaki örnekler nasıl oluşturulacağı bir <xref:System.Windows.Controls.ContextMenu> alt menüler ile.</span><span class="sxs-lookup"><span data-stu-id="25446-112">The following examples show how to create a <xref:System.Windows.Controls.ContextMenu> with submenus.</span></span> <span data-ttu-id="25446-113"><xref:System.Windows.Controls.ContextMenu> Denetimleri düğme denetimlerine iliştirilir.</span><span class="sxs-lookup"><span data-stu-id="25446-113">The <xref:System.Windows.Controls.ContextMenu> controls are attached to button controls.</span></span>  
  
 [!code-xaml[ContextMenu#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ContextMenu/CSharp/Pane1.xaml#1)]  
  
 [!code-csharp[ContextMenu#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ContextMenu/CSharp/Pane1.xaml.cs#2)]
 [!code-vb[ContextMenu#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ContextMenu/VisualBasic/Pane1.xaml.vb#2)]  
  
<a name="applying_styles_to_contextmenu"></a>   
## <a name="applying-styles-to-a-contextmenu"></a><span data-ttu-id="25446-114">Bir ContextMenu uygulanan stilleri</span><span class="sxs-lookup"><span data-stu-id="25446-114">Applying Styles to a ContextMenu</span></span>  
 <span data-ttu-id="25446-115">Bir denetimi kullanarak <xref:System.Windows.Style>, önemli ölçüde görünümünü ve davranışını değiştirebilirsiniz bir <xref:System.Windows.Controls.ContextMenu> özel bir denetim yazma olmadan.</span><span class="sxs-lookup"><span data-stu-id="25446-115">By using a control <xref:System.Windows.Style>, you can dramatically change the appearance and behavior of a <xref:System.Windows.Controls.ContextMenu> without writing a custom control.</span></span> <span data-ttu-id="25446-116">Görsel özellikler ayarlamaya ek olarak, bir denetim bölümlerine stilleri de uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25446-116">In addition to setting visual properties, you can also apply styles to parts of a control.</span></span> <span data-ttu-id="25446-117">Örneğin, özelliklerini kullanarak denetim bölümlerini davranışını değiştirebilir veya bölümlerine ekleme veya düzenini değiştirme bir <xref:System.Windows.Controls.ContextMenu>.</span><span class="sxs-lookup"><span data-stu-id="25446-117">For example, you can change the behavior of parts of the control by using properties, or you can add parts to, or change the layout of, a <xref:System.Windows.Controls.ContextMenu>.</span></span> <span data-ttu-id="25446-118">Aşağıdaki örnekler stil eklemek için çeşitli yollar <xref:System.Windows.Controls.ContextMenu> kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="25446-118">The following examples show several ways to add styles to <xref:System.Windows.Controls.ContextMenu> controls.</span></span>  
  
 <span data-ttu-id="25446-119">İlk örnek adlı bir stil tanımlar `SimpleSysResources`, geçerli sistem ayarları stil kodunuzu nasıl kullanılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="25446-119">The first example defines a style called `SimpleSysResources`, which shows how to use the current system settings in your style.</span></span> <span data-ttu-id="25446-120">Örnek atar <xref:System.Windows.SystemColors.MenuHighlightBrushKey%2A> olarak <xref:System.Windows.Controls.Control.Background%2A> renk ve <xref:System.Windows.SystemColors.MenuTextBrushKey%2A> olarak <xref:System.Windows.Controls.Control.Foreground%2A> rengini <xref:System.Windows.Controls.ContextMenu>.</span><span class="sxs-lookup"><span data-stu-id="25446-120">The example assigns <xref:System.Windows.SystemColors.MenuHighlightBrushKey%2A> as the <xref:System.Windows.Controls.Control.Background%2A> color and <xref:System.Windows.SystemColors.MenuTextBrushKey%2A> as the <xref:System.Windows.Controls.Control.Foreground%2A> color of the <xref:System.Windows.Controls.ContextMenu>.</span></span>  
  
```xaml  
<Style x:Key="SimpleSysResources" TargetType="{x:Type MenuItem}">  
  <Setter Property = "Background" Value=   
    "{DynamicResource {x:Static SystemColors.MenuHighlightBrushKey}}"/>  
  <Setter Property = "Foreground" Value=   
    "{DynamicResource {x:Static SystemColors.MenuTextBrushKey}}"/>  
</Style>  
```  
  
 <span data-ttu-id="25446-121">Aşağıdaki örnek kullanır <xref:System.Windows.Trigger> öğesinin görünümünü değiştirmek için bir <xref:System.Windows.Controls.Menu> üzerinde ortaya olaylarına yanıt olarak <xref:System.Windows.Controls.ContextMenu>.</span><span class="sxs-lookup"><span data-stu-id="25446-121">The following example uses the <xref:System.Windows.Trigger> element to change the appearance of a <xref:System.Windows.Controls.Menu> in response to events that are raised on the <xref:System.Windows.Controls.ContextMenu>.</span></span> <span data-ttu-id="25446-122">Ne zaman bir kullanıcı hareket fare görünümünü menüye <xref:System.Windows.Controls.ContextMenu> öğelerini değişiklikleri.</span><span class="sxs-lookup"><span data-stu-id="25446-122">When a user moves the mouse over the menu, the appearance of the <xref:System.Windows.Controls.ContextMenu> items changes.</span></span>  
  
```xaml  
<Style x:Key="Triggers" TargetType="{x:Type MenuItem}">  
  <Style.Triggers>  
    <Trigger Property="MenuItem.IsMouseOver" Value="true">  
      <Setter Property = "FontSize" Value="16"/>  
      <Setter Property = "FontStyle" Value="Italic"/>  
      <Setter Property = "Foreground" Value="Red"/>  
    </Trigger>  
  </Style.Triggers>  
</Style>  
```  
  
## <a name="see-also"></a><span data-ttu-id="25446-123">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="25446-123">See Also</span></span>  
 <xref:System.Windows.Controls.ContextMenu>  
 <xref:System.Windows.Style>  
 <xref:System.Windows.Controls.Menu>  
 <xref:System.Windows.Controls.MenuItem>  
 [<span data-ttu-id="25446-124">ContextMenu</span><span class="sxs-lookup"><span data-stu-id="25446-124">ContextMenu</span></span>](../../../../docs/framework/wpf/controls/contextmenu.md)  
 [<span data-ttu-id="25446-125">ContextMenu stilleri ve şablonları</span><span class="sxs-lookup"><span data-stu-id="25446-125">ContextMenu Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/contextmenu-styles-and-templates.md)  
 [<span data-ttu-id="25446-126">WPF denetimleri galeri örneği</span><span class="sxs-lookup"><span data-stu-id="25446-126">WPF Controls Gallery Sample</span></span>](http://go.microsoft.com/fwlink/?LinkID=160053)