---
title: 'Nasıl yapılır: 3B Görünümde Kamera Konumuna ve Yönüne Animasyon Ekleme'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], camera position in 3-D scenes
- camera direction [WPF], animating in 3-D scenes
- 3-D scenes [WPF], animating camera position
- 3-D scenes [WPF], animating camera direction
- camera position [WPF], animating in 3-D scenes
- animation [WPF], camera direction in 3-D scenes
ms.assetid: 480224b7-a5e5-4165-ba7f-ef760ddff94a
ms.openlocfilehash: 429139da809a78474f4f6a082fb6e3c08c72d431
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33558884"
---
# <a name="how-to-animate-camera-position-and-direction-in-a-3d-scene"></a>Nasıl yapılır: 3B Görünümde Kamera Konumuna ve Yönüne Animasyon Ekleme
Aşağıdaki örnek, kamera konumunu hareketli hale getirmeyi ve 3B Sahne işaret ettiği yönü animasyon gösterilmektedir. Bu kullanılarak yapılır <xref:System.Windows.Media.Animation.Point3DAnimation> ve <xref:System.Windows.Media.Animation.Vector3DAnimation> animasyon için <xref:System.Windows.Media.Media3D.ProjectionCamera.Position%2A> ve <xref:System.Windows.Media.Media3D.ProjectionCamera.LookDirection%2A> özelliklerini sırasıyla <xref:System.Windows.Media.Media3D.PerspectiveCamera>. Bunun gibi bir animasyon, bir olaya yanıt olarak izleyicisinin görünüm değiştirmek için kullanabilirsiniz.  
  
## <a name="example"></a>Örnek  
 [!code-xaml[Animation3DGallery_snip#PointVector3DAnimationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/PointVector3DAnimationExample.xaml#pointvector3danimationexamplewholepage)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Media.Animation.Vector3DAnimation>  
 <xref:System.Windows.Media.Animation.Point3DAnimation>  
 [Anahtar Çerçeveler Kullanarak Kamera Konumuna ve Yönüne Animasyon Ekleme](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-camera-position-and-direction-using-key-frames.md)  
 [3B Grafiklere Genel Bakış](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
