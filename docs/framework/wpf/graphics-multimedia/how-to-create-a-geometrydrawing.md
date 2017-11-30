---
title: "Nasıl yapılır: GeometryDrawing Oluşturma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- shapes [WPF], renderable
- renderable shapes [WPF]
- graphics [WPF], GeometryDrawing class
- classes [WPF], GeometryDrawing
ms.assetid: 11d3c096-91ba-4d41-9bba-aeac0db70f97
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 7f0fa86a9786e5440db9fec0cee76c5ed28363b8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-create-a-geometrydrawing"></a><span data-ttu-id="ac82d-102">Nasıl yapılır: GeometryDrawing Oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac82d-102">How to: Create a GeometryDrawing</span></span>
<span data-ttu-id="ac82d-103">Bu örnek oluşturmak ve görüntülemek nasıl gösterir bir <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="ac82d-103">This example shows how to create and display a <xref:System.Windows.Media.GeometryDrawing>.</span></span> <span data-ttu-id="ac82d-104">A <xref:System.Windows.Media.GeometryDrawing> şekil dolgu ve anahat ile ilişkilendirerek oluşturmanızı sağlayan bir <xref:System.Windows.Media.Pen> ve <xref:System.Windows.Media.Brush> ile bir <xref:System.Windows.Media.Geometry>.</span><span class="sxs-lookup"><span data-stu-id="ac82d-104">A <xref:System.Windows.Media.GeometryDrawing> enables you to create shape with a fill and an outline by associating a <xref:System.Windows.Media.Pen> and a <xref:System.Windows.Media.Brush> with a <xref:System.Windows.Media.Geometry>.</span></span> <span data-ttu-id="ac82d-105"><xref:System.Windows.Media.GeometryDrawing.Geometry%2A> Şeklin yapısını açıklar <xref:System.Windows.Media.GeometryDrawing.Brush%2A> şeklin dolgu açıklar ve <xref:System.Windows.Media.GeometryDrawing.Pen%2A> şeklin anahat açıklar.</span><span class="sxs-lookup"><span data-stu-id="ac82d-105">The <xref:System.Windows.Media.GeometryDrawing.Geometry%2A> describes the shape's structure, the <xref:System.Windows.Media.GeometryDrawing.Brush%2A> describes the shape's fill, and the <xref:System.Windows.Media.GeometryDrawing.Pen%2A> describes the shape's outline.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ac82d-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="ac82d-106">Example</span></span>  
 <span data-ttu-id="ac82d-107">Aşağıdaki örnek kullanan bir <xref:System.Windows.Media.GeometryDrawing> şekil işlemek için.</span><span class="sxs-lookup"><span data-stu-id="ac82d-107">The following example uses a <xref:System.Windows.Media.GeometryDrawing> to render a shape.</span></span> <span data-ttu-id="ac82d-108">Şeklin tarafından açıklanan bir <xref:System.Windows.Media.GeometryGroup> ve iki <xref:System.Windows.Media.EllipseGeometry> nesneleri.</span><span class="sxs-lookup"><span data-stu-id="ac82d-108">The shape is described by a <xref:System.Windows.Media.GeometryGroup> and two <xref:System.Windows.Media.EllipseGeometry> objects.</span></span> <span data-ttu-id="ac82d-109">Şeklin iç ile boyanır bir <xref:System.Windows.Media.LinearGradientBrush> ve anahattı ile çizilmiş bir <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>.</span><span class="sxs-lookup"><span data-stu-id="ac82d-109">The shape's interior is painted with a <xref:System.Windows.Media.LinearGradientBrush> and its outline is drawn with a <xref:System.Windows.Media.Brushes.Black%2A> <xref:System.Windows.Media.Pen>.</span></span> <span data-ttu-id="ac82d-110"><xref:System.Windows.Media.GeometryDrawing> Kullanılarak görüntülenen bir <xref:System.Windows.Media.ImageDrawing> ve bir <xref:System.Windows.Controls.Image> öğesi.</span><span class="sxs-lookup"><span data-stu-id="ac82d-110">The <xref:System.Windows.Media.GeometryDrawing> is displayed using an <xref:System.Windows.Media.ImageDrawing> and an <xref:System.Windows.Controls.Image> element.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/GeometryDrawingExample.cs#geometrydrawingexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GeometryDrawingExampleWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/GeometryDrawingExample.xaml#geometrydrawingexamplewholepage)]  
  
 <span data-ttu-id="ac82d-111">Elde edilen aşağıda gösterilmiştir <xref:System.Windows.Media.GeometryDrawing>.</span><span class="sxs-lookup"><span data-stu-id="ac82d-111">The following illustration shows the resulting <xref:System.Windows.Media.GeometryDrawing>.</span></span>  
  
 <span data-ttu-id="ac82d-112">![İki elips GeometryDrawing](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span><span class="sxs-lookup"><span data-stu-id="ac82d-112">![A GeometryDrawing of two ellipses](../../../../docs/framework/wpf/graphics-multimedia/media/graphicsmm-geodraw.jpg "graphicsmm_geodraw")</span></span>  
  
 <span data-ttu-id="ac82d-113">Daha karmaşık çizimler oluşturmak için tek bir bileşik kullanarak çizim birden çok çizim nesneleri birleştirebilirsiniz bir <xref:System.Windows.Media.DrawingGroup>.</span><span class="sxs-lookup"><span data-stu-id="ac82d-113">To create more complex drawings, you can combine multiple drawing objects into a single composite drawing using a <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac82d-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ac82d-114">See Also</span></span>  
 <xref:System.Windows.Media.DrawingGroup>  
 [<span data-ttu-id="ac82d-115">Çizim nesnelerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="ac82d-115">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [<span data-ttu-id="ac82d-116">Geometri genel bakış</span><span class="sxs-lookup"><span data-stu-id="ac82d-116">Geometry Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/geometry-overview.md)  
 [<span data-ttu-id="ac82d-117">Bileşik çizim oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac82d-117">Create a Composite Drawing</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-composite-drawing.md)