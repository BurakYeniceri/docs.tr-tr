---
title: "Nasıl yapılır: 3B Görünümde Malzeme Özelliklerine Animasyon Ekleme"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Material properties [WPF], animating in 3-D scenes
- animation [WPF], Material properties in 3-D scenes
- 3-D scenes [WPF], animating Material properties
ms.assetid: 229fd6eb-7401-4992-b0c9-8b28de230c0f
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 16d7ba089730a58106448d8a6889b362042532e2
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-animate-material-properties-in-a-3-d-scene"></a><span data-ttu-id="d8ed3-102">Nasıl yapılır: 3B Görünümde Malzeme Özelliklerine Animasyon Ekleme</span><span class="sxs-lookup"><span data-stu-id="d8ed3-102">How to: Animate Material Properties in a 3-D Scene</span></span>
<span data-ttu-id="d8ed3-103">Bu örnek animasyon gösterilmektedir <xref:System.Windows.Media.Brush.Opacity%2A> özelliği <xref:System.Windows.Media.Media3D.Material> uygulanan bir [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modeli.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-103">This example shows how to animate the <xref:System.Windows.Media.Brush.Opacity%2A> property of the <xref:System.Windows.Media.Media3D.Material> applied to a [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] model.</span></span>  
  
 <span data-ttu-id="d8ed3-104">Aşağıdaki kod örneğinde tanımlar <xref:System.Windows.Media.LinearGradientBrush> olarak kullanılan <xref:System.Windows.Media.Media3D.Material> 3B nesneye uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-104">The following code example defines the <xref:System.Windows.Media.LinearGradientBrush> used as the <xref:System.Windows.Media.Media3D.Material> applied to the 3D object.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline1)]  
  
 <span data-ttu-id="d8ed3-105"><xref:System.Windows.Media.Brush.Opacity%2A> Bu özelliği <xref:System.Windows.Media.LinearGradientBrush> aşağıdaki kod örneği kullanılarak animasyonlu.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-105">The <xref:System.Windows.Media.Brush.Opacity%2A> property of this <xref:System.Windows.Media.LinearGradientBrush> is animated using the code example below.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleInline2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexampleinline2)]  
  
## <a name="example"></a><span data-ttu-id="d8ed3-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="d8ed3-106">Example</span></span>  
 <span data-ttu-id="d8ed3-107">Aşağıdaki kod tüm örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#AnimateMaterialExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/AnimateMaterialExample.xaml#animatematerialexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="d8ed3-108">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d8ed3-108">See Also</span></span>  
 [<span data-ttu-id="d8ed3-109">3B Görünümü Oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8ed3-109">Create a 3-D Scene</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)  
 [<span data-ttu-id="d8ed3-110">3B Grafiklere Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="d8ed3-110">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
