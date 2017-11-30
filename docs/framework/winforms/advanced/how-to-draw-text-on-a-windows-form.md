---
title: "Nasıl yapılır: Bir Windows Formunda Metin Çizme"
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
- cpp
helpviewer_keywords:
- forms [Windows Forms], drawing text
- text [Windows Forms], drawing
ms.assetid: 5d2447a9-21a1-4adc-b954-5516f2bb9b2c
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 23919145a04bb4b3d1674b153649aca2228364eb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-draw-text-on-a-windows-form"></a><span data-ttu-id="ec9e0-102">Nasıl yapılır: Bir Windows Formunda Metin Çizme</span><span class="sxs-lookup"><span data-stu-id="ec9e0-102">How to: Draw Text on a Windows Form</span></span>
<span data-ttu-id="ec9e0-103">Aşağıdaki kod örneğinde nasıl kullanılacağını gösterir <xref:System.Drawing.Graphics.DrawString%2A> yöntemi <xref:System.Drawing.Graphics> bir form üzerinde metin çizmek için.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-103">The following code example shows how to use the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> to draw text on a form.</span></span> <span data-ttu-id="ec9e0-104">Alternatif olarak, kullanabileceğiniz <xref:System.Windows.Forms.TextRenderer> bir formunda metin çizme.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-104">Alternatively, you can use <xref:System.Windows.Forms.TextRenderer> for drawing text on a form.</span></span> <span data-ttu-id="ec9e0-105">Daha fazla bilgi için bkz: [nasıl yapılır: GDI ile metin çizme](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="ec9e0-105">For more information, see [How to: Draw Text with GDI](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec9e0-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="ec9e0-106">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#7](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#7)]
 [!code-csharp[System.Drawing.ConceptualHowTos#7](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#7)]
 [!code-vb[System.Drawing.ConceptualHowTos#7](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#7)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ec9e0-107">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="ec9e0-107">Compiling the Code</span></span>  
 <span data-ttu-id="ec9e0-108">Çağıramazsınız <xref:System.Drawing.Graphics.DrawString%2A> yönteminde <xref:System.Windows.Forms.Form.Load> olay işleyicisi.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-108">You cannot call the <xref:System.Drawing.Graphics.DrawString%2A> method in the <xref:System.Windows.Forms.Form.Load> event handler.</span></span> <span data-ttu-id="ec9e0-109">Formu yeniden boyutlandırılmış veya başka bir form tarafından getirilmemeli çizilmiş içeriği yeniden değil.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-109">The drawn content will not be redrawn if the form is resized or obscured by another form.</span></span> <span data-ttu-id="ec9e0-110">İçeriğinizi otomatik olarak yeniden boyamak yapmak için geçersiz kılmalıdır <xref:System.Windows.Forms.Control.OnPaint%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-110">To make your content automatically repaint, you should override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="ec9e0-111">Güçlü Programlama</span><span class="sxs-lookup"><span data-stu-id="ec9e0-111">Robust Programming</span></span>  
 <span data-ttu-id="ec9e0-112">Aşağıdaki koşullar özel bir duruma neden olabilir:</span><span class="sxs-lookup"><span data-stu-id="ec9e0-112">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="ec9e0-113">Arial yazı tipi yüklü değil.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-113">The Arial font is not installed.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec9e0-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ec9e0-114">See Also</span></span>  
 <xref:System.Drawing.Graphics.DrawString%2A>  
 <xref:System.Windows.Forms.TextRenderer.DrawText%2A>  
 <xref:System.Drawing.StringFormat.FormatFlags%2A>  
 <xref:System.Drawing.StringFormatFlags>  
 <xref:System.Windows.Forms.TextFormatFlags>  
 <xref:System.Windows.Forms.Control.OnPaint%2A>  
 [<span data-ttu-id="ec9e0-115">Grafik programlamaya Başlarken</span><span class="sxs-lookup"><span data-stu-id="ec9e0-115">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)  
 [<span data-ttu-id="ec9e0-116">Nasıl yapılır: GDI ile metin çizme</span><span class="sxs-lookup"><span data-stu-id="ec9e0-116">How to: Draw Text with GDI</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)
