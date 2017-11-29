---
title: "Nasıl yapılır: Alt Öğeleri Konumlandırmak için Tuvalin Ekli Özelliklerini Kullanma"
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
- cpp
helpviewer_keywords:
- attached properties [WPF Designer]
- Canvas control [WPF], attached properties
ms.assetid: 48f1d25d-3820-4107-a4cc-d6c1e5664a44
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 85ee852c868f26937494d5d340d2db4210224754
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-use-the-attached-properties-of-canvas-to-position-child-elements"></a>Nasıl yapılır: Alt Öğeleri Konumlandırmak için Tuvalin Ekli Özelliklerini Kullanma
Bu örnek, iliştirilmiş özelliklerini kullanmak gösterilmiştir <xref:System.Windows.Controls.Canvas> alt öğeleri konumlandırmak için.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, dört ekler <xref:System.Windows.Controls.Button> öğeler alt öğelerin üst öğesi olarak <xref:System.Windows.Controls.Canvas>. Her alt öğe, farklı bir ekli özelliğini temsil eden <xref:System.Windows.Controls.Canvas>: <xref:System.Windows.Controls.Canvas.Bottom%2A>, <xref:System.Windows.Controls.Canvas.Left%2A>, <xref:System.Windows.Controls.Canvas.Right%2A>, ve <xref:System.Windows.Controls.Canvas.Top%2A>. Her <xref:System.Windows.Controls.Button> göre üst konumlandırılmış <xref:System.Windows.Controls.Canvas> ve atanan özellik değerine göre.  
  
 [!code-cpp[CanvasAttachedProperties#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/CanvasAttachedProperties/CPP/CanvasAttachedProps.cpp#1)]
 [!code-csharp[CanvasAttachedProperties#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CanvasAttachedProperties/CSharp/CanvasAttachedProps.cs#1)]
 [!code-vb[CanvasAttachedProperties#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasAttachedProperties/VisualBasic/CanvasAttachedProps.vb#1)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Controls.Canvas>  
 <xref:System.Windows.Controls.Canvas.Bottom%2A>  
 <xref:System.Windows.Controls.Canvas.Left%2A>  
 <xref:System.Windows.Controls.Canvas.Right%2A>  
 <xref:System.Windows.Controls.Canvas.Top%2A>  
 <xref:System.Windows.Controls.Button>  
 [Paneller Genel Bakış](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [Nasıl Yapılır Konuları](../../../../docs/framework/wpf/controls/canvas-how-to-topics.md)  
 [Ekli özellikler genel bakış](../../../../docs/framework/wpf/advanced/attached-properties-overview.md)
