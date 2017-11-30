---
title: DrawingVisual Nesnelerini Kullanma
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
- visual layer [WPF], DrawingVisual objects
- DrawingVisual objects in visual layer [WPF]
ms.assetid: 0b4e711d-e640-40cb-81c3-8f5c59909b7d
caps.latest.revision: "17"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: ee46c41d6f0f42bbb9f50bd5862f6eb076b34bb1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="using-drawingvisual-objects"></a><span data-ttu-id="02511-102">DrawingVisual Nesnelerini Kullanma</span><span class="sxs-lookup"><span data-stu-id="02511-102">Using DrawingVisual Objects</span></span>
<span data-ttu-id="02511-103">Bu konu nasıl kullanılacağını bir bakış sunar <xref:System.Windows.Media.DrawingVisual> nesnelerini [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] görsel katmanı.</span><span class="sxs-lookup"><span data-stu-id="02511-103">This topic provides an overview of how to use <xref:System.Windows.Media.DrawingVisual> objects in the [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] visual layer.</span></span>  
  
<a name="drawingvisual_object"></a>   
## <a name="drawingvisual-object"></a><span data-ttu-id="02511-104">DrawingVisual nesnesi</span><span class="sxs-lookup"><span data-stu-id="02511-104">DrawingVisual Object</span></span>  
 <span data-ttu-id="02511-105"><xref:System.Windows.Media.DrawingVisual> Olan şekil, görüntü veya metin işlemek için kullanılan sınıf çizim basit.</span><span class="sxs-lookup"><span data-stu-id="02511-105">The <xref:System.Windows.Media.DrawingVisual> is a lightweight drawing class that is used to render shapes, images, or text.</span></span> <span data-ttu-id="02511-106">Bu sınıf, kendi performansını artırır, düzen veya olay işleme sağlamadığından basit olarak değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="02511-106">This class is considered lightweight because it does not provide layout or event handling, which improves its performance.</span></span> <span data-ttu-id="02511-107">Bu nedenle, çizimler arka planlar ve küçük resim için idealdir.</span><span class="sxs-lookup"><span data-stu-id="02511-107">For this reason, drawings are ideal for backgrounds and clip art.</span></span>  
  
<a name="drawingvisual_host_container"></a>   
## <a name="drawingvisual-host-container"></a><span data-ttu-id="02511-108">DrawingVisual Konak Kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="02511-108">DrawingVisual Host Container</span></span>  
 <span data-ttu-id="02511-109">Kullanmak için <xref:System.Windows.Media.DrawingVisual> nesneleri, bir konak kapsayıcı nesneleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="02511-109">In order to use <xref:System.Windows.Media.DrawingVisual> objects, you need to create a host container for the objects.</span></span> <span data-ttu-id="02511-110">Konak kapsayıcı nesnesi öğesinden türetilmelidir <xref:System.Windows.FrameworkElement> düzeni ve olay işleme desteği sağlayan sınıf <xref:System.Windows.Media.DrawingVisual> oturumda sınıfı.</span><span class="sxs-lookup"><span data-stu-id="02511-110">The host container object must derive from the <xref:System.Windows.FrameworkElement> class, which provides the layout and event handling support that the <xref:System.Windows.Media.DrawingVisual> class lacks.</span></span> <span data-ttu-id="02511-111">Ana amacı alt nesneleri içerecek şekilde olduğundan konak kapsayıcı nesnesi herhangi bir görünür özelliği görüntülemez.</span><span class="sxs-lookup"><span data-stu-id="02511-111">The host container object does not display any visible properties, since its main purpose is to contain child objects.</span></span> <span data-ttu-id="02511-112">Ancak, <xref:System.Windows.UIElement.Visibility%2A> konak kapsayıcısının özelliği ayarlanmalıdır <xref:System.Windows.Visibility.Visible>; Aksi halde, alt öğelerin hiçbiri görünür olur.</span><span class="sxs-lookup"><span data-stu-id="02511-112">However, the <xref:System.Windows.UIElement.Visibility%2A> property of the host container must be set to <xref:System.Windows.Visibility.Visible>; otherwise, none of its child elements will be visible.</span></span>  
  
 <span data-ttu-id="02511-113">Görsel nesneler için bir konak kapsayıcı nesnesi oluşturduğunuzda, görsel nesne başvurularını depolamak gereken bir <xref:System.Windows.Media.VisualCollection>.</span><span class="sxs-lookup"><span data-stu-id="02511-113">When you create a host container object for visual objects, you need to store the visual object references in a <xref:System.Windows.Media.VisualCollection>.</span></span> <span data-ttu-id="02511-114">Kullanım <xref:System.Windows.Media.VisualCollection.Add%2A> konak kapsayıcısı için görsel bir nesne eklemek için yöntem.</span><span class="sxs-lookup"><span data-stu-id="02511-114">Use the <xref:System.Windows.Media.VisualCollection.Add%2A> method to add a visual object to the host container.</span></span> <span data-ttu-id="02511-115">Aşağıdaki örnekte, bir konak kapsayıcı nesnesi oluşturulur ve üç görsel nesne eklenir, <xref:System.Windows.Media.VisualCollection>.</span><span class="sxs-lookup"><span data-stu-id="02511-115">In the following example, a host container object is created, and three visual objects are added to its <xref:System.Windows.Media.VisualCollection>.</span></span>  
  
 [!code-csharp[DrawingVisualSample#100](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingVisualSample/CSharp/Window1.xaml.cs#100)]
 [!code-vb[DrawingVisualSample#100](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DrawingVisualSample/visualbasic/window1.xaml.vb#100)]  
  
> [!NOTE]
>  <span data-ttu-id="02511-116">Önceki kod örneğinde ayıklandığı tam kod örnek için bkz [Test kullanarak isabet sınaması örneği isabet](http://go.microsoft.com/fwlink/?LinkID=159994).</span><span class="sxs-lookup"><span data-stu-id="02511-116">For the complete code sample from which the preceding code example was extracted, see [Hit Test Using DrawingVisuals Sample](http://go.microsoft.com/fwlink/?LinkID=159994).</span></span>  
  
<a name="creating_drawingvisual_objects"></a>   
## <a name="creating-drawingvisual-objects"></a><span data-ttu-id="02511-117">DrawingVisual nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="02511-117">Creating DrawingVisual Objects</span></span>  
 <span data-ttu-id="02511-118">Oluştururken bir <xref:System.Windows.Media.DrawingVisual> nesnesi çizim içerik yok.</span><span class="sxs-lookup"><span data-stu-id="02511-118">When you create a <xref:System.Windows.Media.DrawingVisual> object, it has no drawing content.</span></span> <span data-ttu-id="02511-119">Nesnenin alarak metin, grafik veya görüntü içeriği ekleyebilirsiniz <xref:System.Windows.Media.DrawingContext> ve içine çizim.</span><span class="sxs-lookup"><span data-stu-id="02511-119">You can add text, graphics, or image content by retrieving the object's <xref:System.Windows.Media.DrawingContext> and drawing into it.</span></span> <span data-ttu-id="02511-120">A <xref:System.Windows.Media.DrawingContext> çağrılarak döndürülür <xref:System.Windows.Media.DrawingVisual.RenderOpen%2A> yöntemi bir <xref:System.Windows.Media.DrawingVisual> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02511-120">A <xref:System.Windows.Media.DrawingContext> is returned by calling the <xref:System.Windows.Media.DrawingVisual.RenderOpen%2A> method of a <xref:System.Windows.Media.DrawingVisual> object.</span></span>  
  
 <span data-ttu-id="02511-121">Bir dikdörtgen çizmek için <xref:System.Windows.Media.DrawingContext>, kullanın <xref:System.Windows.Media.DrawingContext.DrawRectangle%2A> yöntemi <xref:System.Windows.Media.DrawingContext> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02511-121">To draw a rectangle into the <xref:System.Windows.Media.DrawingContext>, use the <xref:System.Windows.Media.DrawingContext.DrawRectangle%2A> method of the <xref:System.Windows.Media.DrawingContext> object.</span></span> <span data-ttu-id="02511-122">Diğer içerik türlerine çizim için benzer yöntemler mevcut.</span><span class="sxs-lookup"><span data-stu-id="02511-122">Similar methods exist for drawing other types of content.</span></span> <span data-ttu-id="02511-123">İşiniz bittiğinde içine içerik çizmeyi <xref:System.Windows.Media.DrawingContext>, çağrı <xref:System.Windows.Media.DrawingContext.Close%2A> kapatmak için yöntemi <xref:System.Windows.Media.DrawingContext> ve içeriği kalır.</span><span class="sxs-lookup"><span data-stu-id="02511-123">When you are finished drawing content into the <xref:System.Windows.Media.DrawingContext>, call the <xref:System.Windows.Media.DrawingContext.Close%2A> method to close the <xref:System.Windows.Media.DrawingContext> and persist the content.</span></span>  
  
 <span data-ttu-id="02511-124">Aşağıdaki örnekte, bir <xref:System.Windows.Media.DrawingVisual> nesnesi oluşturulur ve bir dikdörtgen çizilir kendi <xref:System.Windows.Media.DrawingContext>.</span><span class="sxs-lookup"><span data-stu-id="02511-124">In the following example, a <xref:System.Windows.Media.DrawingVisual> object is created, and a rectangle is drawn into its <xref:System.Windows.Media.DrawingContext>.</span></span>  
  
 [!code-csharp[DrawingVisualSample#101](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingVisualSample/CSharp/Window1.xaml.cs#101)]
 [!code-vb[DrawingVisualSample#101](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DrawingVisualSample/visualbasic/window1.xaml.vb#101)]  
  
<a name="creating_overrides"></a>   
## <a name="creating-overrides-for-frameworkelement-members"></a><span data-ttu-id="02511-125">Geçersiz kılmaları FrameworkElement üyeler için oluşturma</span><span class="sxs-lookup"><span data-stu-id="02511-125">Creating Overrides for FrameworkElement Members</span></span>  
 <span data-ttu-id="02511-126">Konak kapsayıcı nesnesi, kendi görsel nesneler koleksiyonunu yönetilmesinden sorumludur.</span><span class="sxs-lookup"><span data-stu-id="02511-126">The host container object is responsible for managing its collection of visual objects.</span></span> <span data-ttu-id="02511-127">Bu konak kapsayıcı üye türetilmiş için geçersiz kılmalarını uygulamasını gerektirir <xref:System.Windows.FrameworkElement> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="02511-127">This requires that the host container implement member overrides for the derived <xref:System.Windows.FrameworkElement> class.</span></span>  
  
 <span data-ttu-id="02511-128">Aşağıdaki listede iki üyeleri geçersiz kılmanız gerekir açıklanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="02511-128">The following list describes the two members you must override:</span></span>  
  
-   <span data-ttu-id="02511-129"><xref:System.Windows.FrameworkElement.GetVisualChild%2A>: Belirtilen dizindeki bir alt koleksiyonda alt öğelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="02511-129"><xref:System.Windows.FrameworkElement.GetVisualChild%2A>: Returns a child at the specified index from the collection of child elements.</span></span>  
  
-   <span data-ttu-id="02511-130"><xref:System.Windows.FrameworkElement.VisualChildrenCount%2A>: Bu öğe içindeki görsel alt öğe sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="02511-130"><xref:System.Windows.FrameworkElement.VisualChildrenCount%2A>: Gets the number of visual child elements within this element.</span></span>  
  
 <span data-ttu-id="02511-131">Aşağıdaki örnekte, iki için geçersiz kılar <xref:System.Windows.FrameworkElement> üyeleri uygulanır.</span><span class="sxs-lookup"><span data-stu-id="02511-131">In the following example, overrides for the two <xref:System.Windows.FrameworkElement> members are implemented.</span></span>  
  
 [!code-csharp[DrawingVisualSample#102](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingVisualSample/CSharp/Window1.xaml.cs#102)]
 [!code-vb[DrawingVisualSample#102](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DrawingVisualSample/visualbasic/window1.xaml.vb#102)]  
  
<a name="providing_hit_testing_support"></a>   
## <a name="providing-hit-testing-support"></a><span data-ttu-id="02511-132">İsabet testi desteği sağlama</span><span class="sxs-lookup"><span data-stu-id="02511-132">Providing Hit Testing Support</span></span>  
 <span data-ttu-id="02511-133">Konak kapsayıcı nesnesi görünür bir özellik görüntülemez olsa bile olay işleme sağlayabilir; ancak, kendi <xref:System.Windows.UIElement.Visibility%2A> özelliği ayarlanmalıdır <xref:System.Windows.Visibility.Visible>.</span><span class="sxs-lookup"><span data-stu-id="02511-133">The host container object can provide event handling even if it does not display any visible properties—however, its <xref:System.Windows.UIElement.Visibility%2A> property must be set to <xref:System.Windows.Visibility.Visible>.</span></span> <span data-ttu-id="02511-134">Bu işleme yordamı sol fare düğmesini sürümü gibi fare olayları yakalayabilir konak kapsayıcı için bir olay oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="02511-134">This allows you to create an event handling routine for the host container that can trap mouse events, such as the release of the left mouse button.</span></span> <span data-ttu-id="02511-135">Olay işleme yordamı, ardından çağırarak isabet testi uygulayabilirsiniz <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="02511-135">The event handling routine can then implement hit testing by invoking the <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> method.</span></span> <span data-ttu-id="02511-136">Yöntemin <xref:System.Windows.Media.HitTestResultCallback> parametresi isabet testi sonuç eylemini belirlemek için kullanabileceğiniz kullanıcı tanımlı bir yordam gösterir.</span><span class="sxs-lookup"><span data-stu-id="02511-136">The method's <xref:System.Windows.Media.HitTestResultCallback> parameter refers to a user-defined procedure that you can use to determine the resulting action of a hit test.</span></span>  
  
 <span data-ttu-id="02511-137">Aşağıdaki örnekte, isabet sınama desteğini konak kapsayıcı nesnesi ve alt öğelerini için uygulanır.</span><span class="sxs-lookup"><span data-stu-id="02511-137">In the following example, hit testing support is implemented for the host container object and its children.</span></span>  
  
 [!code-csharp[DrawingVisualSample#103](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingVisualSample/CSharp/Window1.xaml.cs#103)]
 [!code-vb[DrawingVisualSample#103](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DrawingVisualSample/visualbasic/window1.xaml.vb#103)]  
  
## <a name="see-also"></a><span data-ttu-id="02511-138">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="02511-138">See Also</span></span>  
 <xref:System.Windows.Media.DrawingVisual>  
 <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A>  
 [<span data-ttu-id="02511-139">WPF Grafik işleme genel bakış</span><span class="sxs-lookup"><span data-stu-id="02511-139">WPF Graphics Rendering Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview.md)  
 [<span data-ttu-id="02511-140">Görsel katmanda isabet sınaması</span><span class="sxs-lookup"><span data-stu-id="02511-140">Hit Testing in the Visual Layer</span></span>](../../../../docs/framework/wpf/graphics-multimedia/hit-testing-in-the-visual-layer.md)