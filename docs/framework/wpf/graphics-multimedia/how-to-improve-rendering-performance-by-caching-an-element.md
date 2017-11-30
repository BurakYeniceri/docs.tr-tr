---
title: "Nasıl yapılır: Öğeyi Önbelleğe Alarak İşleme Performansını Artırma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- rendering performance [WPF], caching an element
- BitmapCache [WPF], improving rendering performance
- CacheMode [WPF], improving rendering performance
- performance [WPF], caching an element
- UIElement [WPF], caching
ms.assetid: 4739c1fc-60ba-4c46-aba6-f6c1a2688f19
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: d754d0ed2f3951c39b3eaeae097589adf3510f5b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-improve-rendering-performance-by-caching-an-element"></a><span data-ttu-id="64cd7-102">Nasıl yapılır: Öğeyi Önbelleğe Alarak İşleme Performansını Artırma</span><span class="sxs-lookup"><span data-stu-id="64cd7-102">How to: Improve Rendering Performance by Caching an Element</span></span>
<span data-ttu-id="64cd7-103">Kullanım <xref:System.Windows.Media.BitmapCache> karmaşık bir işleme performansını artırmak için sınıf <xref:System.Windows.UIElement>.</span><span class="sxs-lookup"><span data-stu-id="64cd7-103">Use the <xref:System.Windows.Media.BitmapCache> class to improve rendering performance of a complex <xref:System.Windows.UIElement>.</span></span> <span data-ttu-id="64cd7-104">Bir öğenin önbelleğe almak için yeni bir örneğini oluşturmak <xref:System.Windows.Media.BitmapCache> sınıfı ve öğenin atayın <xref:System.Windows.UIElement.CacheMode%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="64cd7-104">To cache an element, create a new instance of the <xref:System.Windows.Media.BitmapCache> class and assign it to the element's <xref:System.Windows.UIElement.CacheMode%2A> property.</span></span> <span data-ttu-id="64cd7-105">Yeniden kullanabileceğiniz bir <xref:System.Windows.Media.BitmapCache> verimli bir şekilde, bir <xref:System.Windows.Media.BitmapCacheBrush>.</span><span class="sxs-lookup"><span data-stu-id="64cd7-105">You can reuse a <xref:System.Windows.Media.BitmapCache> efficiently in a <xref:System.Windows.Media.BitmapCacheBrush>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="64cd7-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="64cd7-106">Example</span></span>  
 <span data-ttu-id="64cd7-107">Aşağıdaki kod örneğinde, karmaşık bir öğe oluşturun ve performans öğesi animasyonlu artıran bir bitmap olarak önbelleğe gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="64cd7-107">The following code example shows how to create a complex element and cache it as a bitmap, which improves performance when the element is animated.</span></span> <span data-ttu-id="64cd7-108">Şekil geometri birçok köşe ile tutan bir tuval öğedir.</span><span class="sxs-lookup"><span data-stu-id="64cd7-108">The element is a canvas that holds shape geometries with many vertices.</span></span> <span data-ttu-id="64cd7-109">A <xref:System.Windows.Media.BitmapCache> varsayılan değerler atanır <xref:System.Windows.UIElement.CacheMode%2A> Kanvasın ve önbelleğe alınan bit eşlem sorunsuz ölçeklendirme animasyon gösterir.</span><span class="sxs-lookup"><span data-stu-id="64cd7-109">A <xref:System.Windows.Media.BitmapCache> with default values is assigned to the <xref:System.Windows.UIElement.CacheMode%2A> of the canvas, and an animation shows the smooth scaling of the cached bitmap.</span></span>  
  
 [!code-xaml[System.Windows.Media.BitmapCache#_BitmapCacheXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/system.windows.media.bitmapcache/cs/window1.xaml#_bitmapcachexaml)]  
  
## <a name="see-also"></a><span data-ttu-id="64cd7-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="64cd7-110">See Also</span></span>  
 <xref:System.Windows.Media.BitmapCache>  
 <xref:System.Windows.Media.BitmapCacheBrush>  
 <xref:System.Windows.UIElement.CacheMode%2A>  
 [<span data-ttu-id="64cd7-111">Nasıl yapılır: bir önbelleğe alınan öğe fırça olarak kullan</span><span class="sxs-lookup"><span data-stu-id="64cd7-111">How to: Use a Cached Element as a Brush</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-use-a-cached-element-as-a-brush.md)
