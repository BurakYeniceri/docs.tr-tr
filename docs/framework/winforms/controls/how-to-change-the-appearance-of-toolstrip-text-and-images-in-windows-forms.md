---
title: "Nasıl yapılır: Windows Forms'ta ToolStrip Metni ve Görüntülerinin Görünüşünü Değiştirme"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStrip control [Windows Forms], appearance
- toolbars [Windows Forms], images
- examples [Windows Forms], toolbars
- toolbars [Windows Forms], appearance
- ToolStrip control [Windows Forms], images
- ToolStrip control [Windows Forms], text
- toolbars [Windows Forms], text
ms.assetid: d62dc9d1-2edd-4dfa-aed7-1335d6e13d86
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 1d926ce74db9723b6248dbb123513ca38d4adb1d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-change-the-appearance-of-toolstrip-text-and-images-in-windows-forms"></a>Nasıl yapılır: Windows Forms'ta ToolStrip Metni ve Görüntülerinin Görünüşünü Değiştirme
Metin ve görüntüler üzerinde görüntülenip görüntülenmeyeceğini denetleyebilirsiniz bir <xref:System.Windows.Forms.ToolStripItem> ve bunların birbirlerine göre nasıl hizalandığını ve <xref:System.Windows.Forms.ToolStrip>.  
  
### <a name="to-define-what-is-displayed-on-a-toolstripitem"></a>Üzerinde ToolStripItem görüntülenenleri tanımlamak için  
  
-   Ayarlama <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> istenen değeri özelliğine. Olasılıkları şunlardır `Image`, `ImageAndText`, `None`, ve `Text`. Varsayılan, `ImageAndText` değeridir.  
  
    ```vb  
    ToolStripButton2.DisplayStyle = _  
        System.Windows.Forms.ToolStripItemDisplayStyle.Image  
    ```  
  
    ```csharp  
    toolStripButton2.DisplayStyle = System.Windows.Forms.ToolStripItemDisplayStyle.Image;  
    ```  
  
### <a name="to-align-text-on-a-toolstripitem"></a>Bir ToolStripItem üzerine metni hizalama  
  
-   Ayarlama <xref:System.Windows.Forms.ToolStripItem.TextAlign%2A> istenen değeri özelliğine. Olasılıkları üst, Orta ve alt sol, Ortala ve sağa ile herhangi bir bileşimini şunlardır. Varsayılan, `MiddleCenter` değeridir.  
  
    ```vb  
    ToolStripSplitButton1.TextAlign = _  
        System.Drawing.ContentAlignment.MiddleRight  
    ```  
  
    ```csharp  
    toolStripSplitButton1.TextAlign = System.Drawing.ContentAlignment.MiddleRight;  
    ```  
  
### <a name="to-align-an-image-on-a-toolstripitem"></a>ToolStripItem görüntüde hizalamak için  
  
-   Ayarlama <xref:System.Windows.Forms.ToolStripItem.ImageAlign%2A> istenen değeri özelliğine. Olasılıkları üst, Orta ve alt sol, Ortala ve sağa ile herhangi bir bileşimini şunlardır. Varsayılan, `MiddleLeft` değeridir.  
  
    ```vb  
    ToolStripSplitButton1.ImageAlign = _  
        System.Drawing.ContentAlignment.MiddleRight  
    ```  
  
    ```csharp  
    toolStripSplitButton1.ImageAlign = System.Drawing.ContentAlignment.MiddleRight;  
    ```  
  
### <a name="to-define-how-toolstripitem-text-and-images-are-displayed-relative-to-each-other"></a>ToolStripItem metin ve görüntüler diğer göre nasıl görüntüleneceğini tanımlamak için  
  
-   Ayarlama <xref:System.Windows.Forms.ToolStripItem.TextImageRelation%2A> istenen değeri özelliğine. Olasılıkları şunlardır `ImageAboveText`, `ImageBeforeText`, `Overlay`, `TextAboveImage`, ve `TextBeforeImage`. Varsayılan, `ImageBeforeText` değeridir.  
  
    ```vb  
    ToolStripButton1.TextImageRelation = _  
        System.Windows.Forms.TextImageRelation.ImageAboveText  
    ```  
  
    ```csharp  
    toolStripButton1.TextImageRelation = System.Windows.Forms.TextImageRelation.ImageAboveText;  
    ```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Forms.ToolStrip>  
 [ToolStrip denetimine genel bakış](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)  
 [ToolStrip denetim mimarisi](../../../../docs/framework/winforms/controls/toolstrip-control-architecture.md)  
 [ToolStrip Teknoloiji özeti](../../../../docs/framework/winforms/controls/toolstrip-technology-summary.md)
