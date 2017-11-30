---
title: "Nasıl yapılır: Özel Denetimden Mürekkep Seçme"
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
- controls [WPF], ink selection
- ink [WPF], selecting from custom control
- custom controls [WPF], ink selection
ms.assetid: 5f3a45c6-6d40-4017-9b47-933f134ceba3
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: dd9693209cc35ecd3c0473133b7c21639a239ff5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-select-ink-from-a-custom-control"></a><span data-ttu-id="16619-102">Nasıl yapılır: Özel Denetimden Mürekkep Seçme</span><span class="sxs-lookup"><span data-stu-id="16619-102">How to: Select Ink from a Custom Control</span></span>
<span data-ttu-id="16619-103">Ekleyerek bir <xref:System.Windows.Ink.IncrementalLassoHitTester> özel denetim için bir kullanıcı mürekkep benzer şekilde, Serbest Şekil aracı ile seçebilmeniz için denetiminizi etkinleştirebilirsiniz <xref:System.Windows.Controls.InkCanvas> mürekkep bir Serbest Şekil ile seçer.</span><span class="sxs-lookup"><span data-stu-id="16619-103">By adding an <xref:System.Windows.Ink.IncrementalLassoHitTester> to your custom control, you can enable your control so that a user can select ink with a lasso tool, similar to the way the <xref:System.Windows.Controls.InkCanvas> selects ink with a lasso.</span></span>  
  
 <span data-ttu-id="16619-104">Bu örnekte, mürekkep etkin bir özel denetim oluşturma konusunda bilgi sahibi olduğunuz varsayılır.</span><span class="sxs-lookup"><span data-stu-id="16619-104">This example assumes you are familiar with creating an ink-enabled custom control.</span></span>  <span data-ttu-id="16619-105">Mürekkep girişi kabul özel bir denetim oluşturmak için bkz: [mürekkep giriş denetim oluşturma](../../../../docs/framework/wpf/advanced/creating-an-ink-input-control.md).</span><span class="sxs-lookup"><span data-stu-id="16619-105">To create a custom control that accepts ink input, see [Creating an Ink Input Control](../../../../docs/framework/wpf/advanced/creating-an-ink-input-control.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="16619-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="16619-106">Example</span></span>  
 <span data-ttu-id="16619-107">Kullanıcı bir Serbest Şekil çizer zaman <xref:System.Windows.Ink.IncrementalLassoHitTester> Serbest Şekil kullanıcı tamamlandıktan sonra hangi vuruşları Serbest Şekil yolunun sınırları içinde olacağını tahmin eder.</span><span class="sxs-lookup"><span data-stu-id="16619-107">When the user draws a lasso, the <xref:System.Windows.Ink.IncrementalLassoHitTester> predicts which strokes will be within the lasso path's boundaries after the user completes the lasso.</span></span>  <span data-ttu-id="16619-108">Serbest Şekil yolunun sınırları içinde olduğu belirlenen vuruşları, seçili olarak düşünülebilir.</span><span class="sxs-lookup"><span data-stu-id="16619-108">Strokes that are determined to be within the lasso path's boundaries can be thought of as being selected.</span></span>  <span data-ttu-id="16619-109">Seçili vuruşları seçilmemiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="16619-109">Selected strokes can also become unselected.</span></span>  <span data-ttu-id="16619-110">Örneğin, kullanıcı Serbest Şekil çizim sırasında yönünü tersine çevirir <xref:System.Windows.Ink.IncrementalLassoHitTester> bazı vuruşları seçimini kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16619-110">For example, if the user reverses direction while drawing the lasso, the <xref:System.Windows.Ink.IncrementalLassoHitTester> may unselect some strokes.</span></span>  
  
 <span data-ttu-id="16619-111"><xref:System.Windows.Ink.IncrementalLassoHitTester> Başlatır <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> özel denetiminizin kullanıcı serbest şekil çizme sırasında yanıt vermesini sağlayan olay.</span><span class="sxs-lookup"><span data-stu-id="16619-111">The <xref:System.Windows.Ink.IncrementalLassoHitTester> raises the <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> event, which enables your custom control to respond while the user is drawing the lasso.</span></span>  <span data-ttu-id="16619-112">Örneğin, kullanıcı seçer ve bunları seçili olanları kaldırdığında gibi vuruşları görünümünü değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="16619-112">For example, you can change the appearance of strokes as the user selects and unselects them.</span></span>  
  
## <a name="managing-the-ink-mode"></a><span data-ttu-id="16619-113">Mürekkep modunu yönetme</span><span class="sxs-lookup"><span data-stu-id="16619-113">Managing the Ink Mode</span></span>  
 <span data-ttu-id="16619-114">Serbest Şekil denetiminizde mürekkep'den farklı görünüyorsa, kullanıcıya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="16619-114">It is helpful to the user if the lasso appears differently than the ink on your control.</span></span> <span data-ttu-id="16619-115">Bunu gerçekleştirmek için özel denetim kullanıcı yazma ya da mürekkep seçme izlemek gerekir.</span><span class="sxs-lookup"><span data-stu-id="16619-115">To accomplish this, your custom control must keep track of whether the user is writing or selecting ink.</span></span> <span data-ttu-id="16619-116">Bunu yapmanın en kolay yolu, iki değeri olan bir numaralandırma bildirmektir: bir kullanıcı mürekkep ve bir kullanıcı mürekkep seçtiğini göstermek için yazma belirtmek için.</span><span class="sxs-lookup"><span data-stu-id="16619-116">The easiest way to do this is to declare an enumeration with two values: one to indicate that the user is writing ink and one to indicate that the user is selecting ink.</span></span>  
  
 [!code-csharp[HowToSelectInk#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#2)]
 [!code-vb[HowToSelectInk#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#2)]  
  
 <span data-ttu-id="16619-117">Sonra iki ekleyin <xref:System.Windows.Ink.DrawingAttributes> sınıfına: bir kullanıcı kullanıcı mürekkep seçtiğinde kullanmak üzere mürekkep yazdığında kullanın.</span><span class="sxs-lookup"><span data-stu-id="16619-117">Next, add two <xref:System.Windows.Ink.DrawingAttributes> to the class: one to use when the user writes ink, one to use when the user selects ink.</span></span>  <span data-ttu-id="16619-118">Oluşturucuda başlatma <xref:System.Windows.Ink.DrawingAttributes> ve her iki <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> aynı olay işleyicisi olayları.</span><span class="sxs-lookup"><span data-stu-id="16619-118">In the constructor, initialize the <xref:System.Windows.Ink.DrawingAttributes> and attach both <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> events to the same event handler.</span></span> <span data-ttu-id="16619-119">Ardından <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> özelliği <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> mürekkep <xref:System.Windows.Ink.DrawingAttributes>.</span><span class="sxs-lookup"><span data-stu-id="16619-119">Then set the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> property of the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> to the ink <xref:System.Windows.Ink.DrawingAttributes>.</span></span>  
  
 [!code-csharp[HowToSelectInk#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#3)]
 [!code-vb[HowToSelectInk#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#3)]  
[!code-csharp[HowToSelectInk#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#4)]
[!code-vb[HowToSelectInk#4](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#4)]  
  
 <span data-ttu-id="16619-120">Seçim modu kullanıma sunan bir özellik ekleyin.</span><span class="sxs-lookup"><span data-stu-id="16619-120">Add a property that exposes the selection mode.</span></span> <span data-ttu-id="16619-121">Kullanıcı seçim modunu değiştirdiğinde ayarlamak <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> özelliği <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> uygun <xref:System.Windows.Ink.DrawingAttributes> nesnesi ve ardından yeniden ekleyin <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> özelliğine <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="16619-121">When the user changes the selection mode, set the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> property of the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> to the appropriate <xref:System.Windows.Ink.DrawingAttributes> object and then reattach the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> Property to the <xref:System.Windows.Controls.InkPresenter>.</span></span>  
  
 [!code-csharp[HowToSelectInk#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#5)]
 [!code-vb[HowToSelectInk#5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#5)]  
  
 <span data-ttu-id="16619-122">Kullanıma <xref:System.Windows.Ink.DrawingAttributes> böylece uygulamaları mürekkep ve seçim vuruşlarını görünümünü belirleyebilir özellikleri olarak.</span><span class="sxs-lookup"><span data-stu-id="16619-122">Expose the <xref:System.Windows.Ink.DrawingAttributes> as properties so applications can determine the appearance of the ink strokes and selection strokes.</span></span>  
  
 [!code-csharp[HowToSelectInk#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#6)]
 [!code-vb[HowToSelectInk#6](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#6)]  
  
 <span data-ttu-id="16619-123">Özelliği bir <xref:System.Windows.Ink.DrawingAttributes> nesnesi değişiklikleri <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> için yeniden gerekir <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="16619-123">When a property of a <xref:System.Windows.Ink.DrawingAttributes> object changes, the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> must be reattached to the <xref:System.Windows.Controls.InkPresenter>.</span></span>  <span data-ttu-id="16619-124">Olay işleyicisi içinde <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> olay, yeniden iliştirmeye <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> için <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="16619-124">In the event handler for the <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> event, reattach the <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> to the <xref:System.Windows.Controls.InkPresenter>.</span></span>  
  
 [!code-csharp[HowToSelectInk#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#7)]
 [!code-vb[HowToSelectInk#7](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#7)]  
  
## <a name="using-the-incrementallassohittester"></a><span data-ttu-id="16619-125">IncrementalLassoHitTester kullanma</span><span class="sxs-lookup"><span data-stu-id="16619-125">Using the IncrementalLassoHitTester</span></span>  
 <span data-ttu-id="16619-126">Oluşturma ve başlatma bir <xref:System.Windows.Ink.StrokeCollection> seçili vuruşları içerir.</span><span class="sxs-lookup"><span data-stu-id="16619-126">Create and initialize a <xref:System.Windows.Ink.StrokeCollection> that contains the selected strokes.</span></span>  
  
 [!code-csharp[HowToSelectInk#8](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#8)]
 [!code-vb[HowToSelectInk#8](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#8)]  
  
 <span data-ttu-id="16619-127">Kullanıcı bir vuruş çizmeye başladığında, mürekkep veya Serbest Şekil tüm seçili vuruşları seçimini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="16619-127">When the user starts to draw a stroke, either ink or the lasso, unselect any selected strokes.</span></span> <span data-ttu-id="16619-128">Ardından, kullanıcı bir serbest şekil çizme varsa, oluşturun bir <xref:System.Windows.Ink.IncrementalLassoHitTester> çağırarak <xref:System.Windows.Ink.StrokeCollection.GetIncrementalLassoHitTester%2A>, abone <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> olay ve arama <xref:System.Windows.Ink.IncrementalHitTester.AddPoints%2A>.</span><span class="sxs-lookup"><span data-stu-id="16619-128">Then, if the user is drawing a lasso, create an <xref:System.Windows.Ink.IncrementalLassoHitTester> by calling <xref:System.Windows.Ink.StrokeCollection.GetIncrementalLassoHitTester%2A>, subscribe to the <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> event, and call <xref:System.Windows.Ink.IncrementalHitTester.AddPoints%2A>.</span></span> <span data-ttu-id="16619-129">Bu kod ayrı bir yöntem olabilir ve çağrılır <xref:System.Windows.UIElement.OnStylusDown%2A> ve <xref:System.Windows.UIElement.OnMouseDown%2A> yöntemleri.</span><span class="sxs-lookup"><span data-stu-id="16619-129">This code can be a separate method and called from the <xref:System.Windows.UIElement.OnStylusDown%2A> and <xref:System.Windows.UIElement.OnMouseDown%2A> methods.</span></span>  
  
 [!code-csharp[HowToSelectInk#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#9)]
 [!code-vb[HowToSelectInk#9](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#9)]  
  
 <span data-ttu-id="16619-130">Kalem noktalarını eklemek <xref:System.Windows.Ink.IncrementalLassoHitTester> kullanıcı serbest şekil çizerken.</span><span class="sxs-lookup"><span data-stu-id="16619-130">Add the stylus points to the <xref:System.Windows.Ink.IncrementalLassoHitTester> while the user draws the lasso.</span></span>  <span data-ttu-id="16619-131">Aşağıdaki yöntemi çağırın <xref:System.Windows.UIElement.OnStylusMove%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, <xref:System.Windows.UIElement.OnMouseMove%2A>, ve <xref:System.Windows.UIElement.OnMouseLeftButtonUp%2A> yöntemleri.</span><span class="sxs-lookup"><span data-stu-id="16619-131">Call the following method from the <xref:System.Windows.UIElement.OnStylusMove%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, <xref:System.Windows.UIElement.OnMouseMove%2A>, and <xref:System.Windows.UIElement.OnMouseLeftButtonUp%2A> methods.</span></span>  
  
 [!code-csharp[HowToSelectInk#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#10)]
 [!code-vb[HowToSelectInk#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#10)]  
  
 <span data-ttu-id="16619-132">Tanıtıcı <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged?displayProperty=nameWithType> kullanıcı seçer ve vuruşları seçili olanları kaldırdığında yanıt olay.</span><span class="sxs-lookup"><span data-stu-id="16619-132">Handle the <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged?displayProperty=nameWithType> event to respond when the user selects and unselects strokes.</span></span>  <span data-ttu-id="16619-133"><xref:System.Windows.Ink.LassoSelectionChangedEventArgs> Sınıfına sahip <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.SelectedStrokes%2A> ve <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.DeselectedStrokes%2A> vuruşları özellikleri seçili olan ve sırasıyla seçilmemiş.</span><span class="sxs-lookup"><span data-stu-id="16619-133">The <xref:System.Windows.Ink.LassoSelectionChangedEventArgs> class has the <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.SelectedStrokes%2A> and <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.DeselectedStrokes%2A> properties that get the strokes that were selected and unselected, respectively.</span></span>  
  
 [!code-csharp[HowToSelectInk#11](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#11)]
 [!code-vb[HowToSelectInk#11](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#11)]  
  
 <span data-ttu-id="16619-134">Kullanıcı serbest şekil çizme tamamlandığında, aboneliğinizi <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> olay ve arama <xref:System.Windows.Ink.IncrementalHitTester.EndHitTesting%2A>.</span><span class="sxs-lookup"><span data-stu-id="16619-134">When the user finishes drawing the lasso, unsubscribe from the <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> event and call <xref:System.Windows.Ink.IncrementalHitTester.EndHitTesting%2A>.</span></span>  
  
 [!code-csharp[HowToSelectInk#12](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#12)]
 [!code-vb[HowToSelectInk#12](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#12)]  
  
## <a name="putting-it-all-together"></a><span data-ttu-id="16619-135">Hepsini birleştirme.</span><span class="sxs-lookup"><span data-stu-id="16619-135">Putting it All Together.</span></span>  
 <span data-ttu-id="16619-136">Aşağıdaki örnek, bir kullanıcının bir Serbest Şekil ile mürekkep seçmesini sağlayan özel bir denetimdir.</span><span class="sxs-lookup"><span data-stu-id="16619-136">The following example is a custom control that enables a user to select ink with a lasso.</span></span>  
  
 [!code-csharp[HowToSelectInk#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#1)]
 [!code-vb[HowToSelectInk#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="16619-137">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="16619-137">See Also</span></span>  
 <xref:System.Windows.Ink.IncrementalLassoHitTester>  
 <xref:System.Windows.Ink.StrokeCollection>  
 <xref:System.Windows.Input.StylusPointCollection>  
 [<span data-ttu-id="16619-138">Mürekkep giriş denetim oluşturma</span><span class="sxs-lookup"><span data-stu-id="16619-138">Creating an Ink Input Control</span></span>](../../../../docs/framework/wpf/advanced/creating-an-ink-input-control.md)