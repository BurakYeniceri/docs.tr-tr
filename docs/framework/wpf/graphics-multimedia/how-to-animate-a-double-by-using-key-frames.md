---
title: "Nasıl yapılır: Anahtar Çerçeveler Kullanarak bir Çifte Animasyon Ekleme"
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
- Doubles [WPF], animating with key frames
- animation [WPF], Doubles with key frames
- key frames [WPF], animating Doubles with
ms.assetid: 3a1a7dba-7694-4907-8a2f-3408baebfa82
caps.latest.revision: "16"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 2c4ec6554ee024450e397ee7757649be7537eaae
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-animate-a-double-by-using-key-frames"></a><span data-ttu-id="eac2f-102">Nasıl yapılır: Anahtar Çerçeveler Kullanarak bir Çifte Animasyon Ekleme</span><span class="sxs-lookup"><span data-stu-id="eac2f-102">How to: Animate a Double by Using Key Frames</span></span>
<span data-ttu-id="eac2f-103">Bu örnek götüren bir özelliğin değerini animasyon gösterilmektedir bir <xref:System.Double> anahtar çerçeveler kullanarak.</span><span class="sxs-lookup"><span data-stu-id="eac2f-103">This example shows how to animate the value of a property that takes a <xref:System.Double> by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eac2f-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="eac2f-104">Example</span></span>  
 <span data-ttu-id="eac2f-105">Aşağıdaki örnek bir dikdörtgen ekran boyunca taşır.</span><span class="sxs-lookup"><span data-stu-id="eac2f-105">The following example moves a rectangle across a screen.</span></span> <span data-ttu-id="eac2f-106">Örnek kullanır <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> animasyon sınıfı <xref:System.Windows.Media.TranslateTransform.X%2A> özelliği bir <xref:System.Windows.Media.TranslateTransform> uygulanan bir <xref:System.Windows.Shapes.Rectangle>.</span><span class="sxs-lookup"><span data-stu-id="eac2f-106">The example uses the <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.TranslateTransform.X%2A> property of a <xref:System.Windows.Media.TranslateTransform> applied to a <xref:System.Windows.Shapes.Rectangle>.</span></span> <span data-ttu-id="eac2f-107">Süresiz olarak yinelenen Bu animasyon üç ana kare aşağıdaki şekilde kullanır:</span><span class="sxs-lookup"><span data-stu-id="eac2f-107">This animation, which repeats indefinitely, uses three key frames in the following manner:</span></span>  
  
1.  <span data-ttu-id="eac2f-108">İlk üç saniye boyunca bir örneğini kullanan <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame> dikdörtgeni yol boyunca bir hızda başlangıç konumundan 500 konumuna taşımak için sınıf.</span><span class="sxs-lookup"><span data-stu-id="eac2f-108">During the first three seconds, uses an instance of the <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame> class to move the rectangle along a path at a steady rate from its starting position to the 500 position.</span></span> <span data-ttu-id="eac2f-109">Gibi doğrusal anahtar çerçeveler <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame> değerler arasında yumuşak bir doğrusal geçiş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eac2f-109">Linear key frames like <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame> create a smooth linear transition between values.</span></span>  
  
2.  <span data-ttu-id="eac2f-110">Dördüncü saniye sonunda bir örneğini kullanan <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame> dikdörtgeni sonraki konumuna aniden taşımak için sınıf.</span><span class="sxs-lookup"><span data-stu-id="eac2f-110">At the end of the fourth second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame> class to suddenly move the rectangle to the next position.</span></span> <span data-ttu-id="eac2f-111">Gibi ayrık anahtar çerçeveler <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame> değerler arasında ani atlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="eac2f-111">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame> create sudden jumps between values.</span></span> <span data-ttu-id="eac2f-112">Bu örnekte, dikdörtgen başlangıç konumunda ve aniden 500 konumunda görünür.</span><span class="sxs-lookup"><span data-stu-id="eac2f-112">In this example, the rectangle is at the starting position and then suddenly appears at the 500 position.</span></span>  
  
3.  <span data-ttu-id="eac2f-113">Son iki saniye içinde bir örneğini kullanan <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame> dikdörtgeni başlangıç konumuna geri taşımak için sınıf.</span><span class="sxs-lookup"><span data-stu-id="eac2f-113">In the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame> class to move the rectangle back to its starting position.</span></span> <span data-ttu-id="eac2f-114">Gibi Eğri anahtar çerçeveler <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame> değerini göre değerler arasında değişken geçiş oluşturmak <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame.KeySpline%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="eac2f-114">Spline key frames like <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame> create a variable transition between values according to the value of the <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="eac2f-115">Bu örnekte, dikdörtgen yavaş taşıyarak başlar ve ardından katlanarak zaman diliminin sonuna doğru hızlanır.</span><span class="sxs-lookup"><span data-stu-id="eac2f-115">In this example, the rectangle begins by moving slowly and then speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-csharp[keyframes_snip#AltDoubleAnimationUsingKeyFramesWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/AltDoubleAnimationUsingKeyFramesExample.cs#altdoubleanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#AltDoubleAnimationUsingKeyFramesWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/altdoubleanimationusingkeyframesexample.vb#altdoubleanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#AltDoubleAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/AltDoubleAnimationUsingKeyFramesExample.xaml#altdoubleanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="eac2f-116">Tam bir örnek için bkz: [ana kare animasyon örneği](http://go.microsoft.com/fwlink/?LinkID=160012).</span><span class="sxs-lookup"><span data-stu-id="eac2f-116">For the complete sample, see [KeyFrame Animation Sample](http://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
 <span data-ttu-id="eac2f-117">Diğer animasyon örnekleriyle tutarlılık için bu örnek kodu sürümlerini kullanan bir <xref:System.Windows.Media.Animation.Storyboard> uygulanacak nesne <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>.</span><span class="sxs-lookup"><span data-stu-id="eac2f-117">For consistency with other animation examples, the code versions of this example use a <xref:System.Windows.Media.Animation.Storyboard> object to apply the <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>.</span></span> <span data-ttu-id="eac2f-118">Alternatif olarak, kodda tek bir animasyonu uygularken, bunu kullanmak daha basittir <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> kullanmak yerine yöntemi bir <xref:System.Windows.Media.Animation.Storyboard>.</span><span class="sxs-lookup"><span data-stu-id="eac2f-118">Alternatively, when applying a single animation in code, it is simpler to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method instead of using a <xref:System.Windows.Media.Animation.Storyboard>.</span></span> <span data-ttu-id="eac2f-119">Bir örnek için bkz: [özelliği olmadan kullanarak bir film şeridi animasyon](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-without-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="eac2f-119">For an example, see [Animate a Property Without Using a Storyboard](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-without-using-a-storyboard.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eac2f-120">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="eac2f-120">See Also</span></span>  
 <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>  
 <xref:System.Windows.Shapes.Rectangle>  
 <xref:System.Windows.Media.Animation.LinearDoubleKeyFrame>  
 <xref:System.Windows.Media.Animation.DiscreteDoubleKeyFrame>  
 <xref:System.Windows.Media.Animation.SplineDoubleKeyFrame>  
 [<span data-ttu-id="eac2f-121">Anahtar çerçeve animasyonları genel bakış</span><span class="sxs-lookup"><span data-stu-id="eac2f-121">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [<span data-ttu-id="eac2f-122">Anahtar çerçeve nasıl yapılır konuları</span><span class="sxs-lookup"><span data-stu-id="eac2f-122">Key-Frame How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)