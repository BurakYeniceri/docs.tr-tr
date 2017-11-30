---
title: "Nasıl yapılır: Özel Denetim Üzerinde Mürekkep Silme"
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
- custom controls [WPF], erasing ink on
- ink [WPF], erasing on custom control
ms.assetid: d88c50f9-b4d8-4962-a28b-67d6a15a5fe0
caps.latest.revision: "4"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 23d234d97d6b25394df87016f0671d86b10a2853
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-erase-ink-on-a-custom-control"></a>Nasıl yapılır: Özel Denetim Üzerinde Mürekkep Silme
<xref:System.Windows.Ink.IncrementalStrokeHitTester> Şu anda çizilmiş vuruşun başka bir vuruş kesiştiğinden olup olmadığını belirler.  Bir denetimi oluşturma vuruşun bölümlerini silmek bir kullanıcı sağlar, bu yararlı olur, bir kullanıcı yolu gerçekleştirebileceğiniz bir <xref:System.Windows.Controls.InkCanvas> zaman <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> ayarlanır <xref:System.Windows.Controls.InkCanvasEditingMode.EraseByPoint>.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek vuruşları bölümlerini silmek kullanıcının sağlayan özel bir denetim oluşturur.  Bu örnek, başlatıldığında mürekkep içeren bir denetim oluşturur.  Mürekkep toplayan bir denetim oluşturmak için bkz: [mürekkep giriş denetimi oluşturma](../../../../docs/framework/wpf/advanced/creating-an-ink-input-control.md).  
  
 [!code-csharp[HowToEraseInk#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToEraseInk/CSharp/InkEraser.cs#1)]
 [!code-vb[HowToEraseInk#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HowToEraseInk/VisualBasic/InkEraser.vb#1)]
