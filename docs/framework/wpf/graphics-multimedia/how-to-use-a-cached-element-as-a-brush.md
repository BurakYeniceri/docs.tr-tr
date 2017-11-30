---
title: "Nasıl yapılır: Önbelleğe Alınan Öğeyi Fırça Olarak Kullanma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- BitmapCache [WPF], using
- cached element [WPF], use as a brush
- BitmapCacheBrush [WPF], using
- CacheMode [WPF], using
ms.assetid: d36e944a-866e-4baf-98c4-fd6a75f6fdd0
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 4d0f0c60e9df6a1ec816b1f9cf5769c93b382ae5
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-use-a-cached-element-as-a-brush"></a><span data-ttu-id="ce1e2-102">Nasıl yapılır: Önbelleğe Alınan Öğeyi Fırça Olarak Kullanma</span><span class="sxs-lookup"><span data-stu-id="ce1e2-102">How to: Use a Cached Element as a Brush</span></span>
<span data-ttu-id="ce1e2-103">Kullanım <xref:System.Windows.Media.BitmapCacheBrush> önbelleğe alınan öğeyi verimli bir şekilde yeniden sınıfı.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-103">Use the <xref:System.Windows.Media.BitmapCacheBrush> class to reuse a cached element efficiently.</span></span> <span data-ttu-id="ce1e2-104">Bir öğenin önbelleğe almak için yeni bir örneğini oluşturmak <xref:System.Windows.Media.BitmapCache> sınıfı ve öğenin atayın <xref:System.Windows.UIElement.CacheMode%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-104">To cache an element, create a new instance of the <xref:System.Windows.Media.BitmapCache> class and assign it to the element's <xref:System.Windows.UIElement.CacheMode%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ce1e2-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="ce1e2-105">Example</span></span>  
 <span data-ttu-id="ce1e2-106">Aşağıdaki kod örneğinde, önbelleğe alınan öğe yeniden gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-106">The following code example shows how to reuse a cached element.</span></span> <span data-ttu-id="ce1e2-107">Önbelleğe alınan öğe bir <xref:System.Windows.Controls.Image> büyük bir görüntü görüntüleyen denetim.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-107">The cached element is an <xref:System.Windows.Controls.Image> control that displays a large image.</span></span> <span data-ttu-id="ce1e2-108"><xref:System.Windows.Controls.Image> Denetim önbelleğe alınma bir bit eşlem olarak kullanarak <xref:System.Windows.Media.BitmapCache> sınıfı ve önbellek yeniden atayarak bunu bir <xref:System.Windows.Media.BitmapCacheBrush>.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-108">The <xref:System.Windows.Controls.Image> control is cached as a bitmap by using the <xref:System.Windows.Media.BitmapCache> class, and the cache is reused by assigning it to a <xref:System.Windows.Media.BitmapCacheBrush>.</span></span> <span data-ttu-id="ce1e2-109">Fırça etkili bir biçimde yeniden göstermek için yirmi beş düğmelerinin arka plan atanır.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-109">The brush is assigned to the background of twenty-five buttons to show efficient reuse.</span></span>  
  
 [!code-xaml[System.Windows.Media.BitmapCacheBrush#_BitmapCacheBrushXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcachebrush/cs/window1.xaml#_bitmapcachebrushxaml)]  
  
## <a name="see-also"></a><span data-ttu-id="ce1e2-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-110">See Also</span></span>  
 <xref:System.Windows.Media.BitmapCache>  
 <xref:System.Windows.Media.BitmapCacheBrush>  
 <xref:System.Windows.UIElement.CacheMode%2A>  
 [<span data-ttu-id="ce1e2-111">Nasıl yapılır: performans öğenin önbelleğe alarak işleme geliştirmek</span><span class="sxs-lookup"><span data-stu-id="ce1e2-111">How to: Improve Rendering Performance by Caching an Element</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-improve-rendering-performance-by-caching-an-element.md)