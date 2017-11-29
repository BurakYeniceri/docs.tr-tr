---
title: "Gerçek Koordinat Dönüştürmesini Kullanma"
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
- graphics [Windows Forms], world transformation
- world transformation [Windows Forms], examples
ms.assetid: 1e717711-1361-448e-aa49-0f3ec43110c9
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: b5b2a8de0644e71a5e6ae1a5ca796f580f0c4f23
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="using-the-world-transformation"></a>Gerçek Koordinat Dönüştürmesini Kullanma
Dünya dönüşümü özelliğidir <xref:System.Drawing.Graphics> sınıfı. Dünya dönüşümü belirtin sayıları depolanmış bir <xref:System.Drawing.Drawing2D.Matrix> 3 × 3 matris temsil eden nesne. <xref:System.Drawing.Drawing2D.Matrix> Ve <xref:System.Drawing.Graphics> sınıflarının sayıları world dönüştürme matrisini ayarlamak için çeşitli yöntemler vardır.  
  
## <a name="different-types-of-transformations"></a>Farklı tür dönüşümleri  
 Aşağıdaki örnekte, kod ilk 50 × 50 Dikdörtgen oluşturur ve başlangıç (0, 0) bulur. Kaynak istemci alanını sol üst köşesinde ' dir.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.MiscLegacyTopics#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#11)]  
  
 Aşağıdaki kod dikdörtgen x yönünde 1.75 faktörüyle genişleyen veya y yönünde 0,5 faktörüyle dikdörtgen bir ölçeklendirme dönüştürmesi uygular:  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.MiscLegacyTopics#12](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#12)]  
  
 X yönünde uzun ve özgün daha y yönünde kısa bir dikdörtgen sonucudur.  
  
 Ölçeklendirme yerine dikdörtgeni döndürmek için aşağıdaki kodu kullanın:  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.MiscLegacyTopics#13](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#13)]  
  
 Dikdörtgen çevirmek için aşağıdaki kodu kullanın:  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.MiscLegacyTopics#14](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#14)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Drawing.Drawing2D.Matrix>  
 [Koordinat sistemleri ve dönüştürmeler](../../../../docs/framework/winforms/advanced/coordinate-systems-and-transformations.md)  
 [Yönetilen GDI +'da dönüştürmeleri kullanma](../../../../docs/framework/winforms/advanced/using-transformations-in-managed-gdi.md)
