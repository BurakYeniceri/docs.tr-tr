---
title: 'Nasıl yapılır: Bir Görselden Bit Eşlem Oluşturma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [WPF], rendering from visuals
- visuals [WPF], rendering to bitmaps
ms.assetid: 103fc7f5-7306-4026-9d61-2005e79959f3
ms.openlocfilehash: 4735474d00712598cb5e41fad289e8f568d83a48
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559772"
---
# <a name="how-to-create-a-bitmap-from-a-visual"></a>Nasıl yapılır: Bir Görselden Bit Eşlem Oluşturma
Bu örnek, bir bit eşlem nasıl oluşturabileceğinizi gösterir bir <xref:System.Windows.Media.Visual>. A <xref:System.Windows.Media.DrawingVisual> ile işlenen <xref:System.Windows.Media.FormattedText>. <xref:System.Windows.Media.Visual> Sonra işlenen <xref:System.Windows.Media.Imaging.RenderTargetBitmap> verilen metni bir bit eşlem oluşturma.  
  
## <a name="example"></a>Örnek  
 [!code-csharp[ImagingSnippetGallery_procedural_snip#CreateRTBImage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/CSharp/RenderTargetBitmapExample.cs#creatertbimage)]
 [!code-vb[ImagingSnippetGallery_procedural_snip#CreateRTBImage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ImagingSnippetGallery_procedural_snip/VB/RenderTargetBitmapExample.vb#creatertbimage)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Media.DrawingContext>  
 [Görüntülemeye Genel Bakış](../../../../docs/framework/wpf/graphics-multimedia/imaging-overview.md)  
 [Çizim Nesnelerine Genel Bakış](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [DrawingVisual Nesnelerini Kullanma](../../../../docs/framework/wpf/graphics-multimedia/using-drawingvisual-objects.md)
