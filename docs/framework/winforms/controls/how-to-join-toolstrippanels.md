---
title: "Nasıl yapılır: ToolStripPanels'ni birleştirme"
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
- toolbars [Windows Forms], joining together
- ToolStripPanel control [Windows Forms], joining together
ms.assetid: 4eadda6d-e3b8-4151-aaf2-a8d564fbe6b3
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 2d77d29526656da0c149ee4b8e940f4ad9e87ca3
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-join-toolstrippanels"></a><span data-ttu-id="34cb6-102">Nasıl yapılır: ToolStripPanels'ni birleştirme</span><span class="sxs-lookup"><span data-stu-id="34cb6-102">How to: Join ToolStripPanels</span></span>
<span data-ttu-id="34cb6-103">Katılmak <xref:System.Windows.Forms.ToolStrip> için denetimler bir <xref:System.Windows.Forms.ToolStripPanel> çalışma zamanında birden çok belge arabirimi (MDI) uygulamaları esnekliğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="34cb6-103">You can join <xref:System.Windows.Forms.ToolStrip> controls to a <xref:System.Windows.Forms.ToolStripPanel> at run time, which provides the flexibility of multiple-document interface (MDI) applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="34cb6-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="34cb6-104">Example</span></span>  
 <span data-ttu-id="34cb6-105">Aşağıdaki kod örneğinde nasıl birleştirileceği gösterilmektedir <xref:System.Windows.Forms.ToolStrip> için denetimler bir <xref:System.Windows.Forms.ToolStripPanel>.</span><span class="sxs-lookup"><span data-stu-id="34cb6-105">The following code example demonstrates how to join <xref:System.Windows.Forms.ToolStrip> controls to a <xref:System.Windows.Forms.ToolStripPanel>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#11)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="34cb6-106">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="34cb6-106">Compiling the Code</span></span>  
 <span data-ttu-id="34cb6-107">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="34cb6-107">This example requires:</span></span>  
  
-   <span data-ttu-id="34cb6-108">System.Design, System.Drawing ve System.Windows.Forms derlemelerine başvurular.</span><span class="sxs-lookup"><span data-stu-id="34cb6-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="34cb6-109">Bu örnek için komut satırından oluşturma hakkında bilgi için [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] veya [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)], bkz: [komut satırından derleme](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) veya [komut satırı derleme ile csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="34cb6-109">For information about building this example from the command line for [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] or [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)], see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="34cb6-110">Bu örnek ayrıca oluşturmak [!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] yeni bir proje kodunu yapıştırma tarafından.</span><span class="sxs-lookup"><span data-stu-id="34cb6-110">You can also build this example in [!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] by pasting the code into a new project.</span></span>  <span data-ttu-id="34cb6-111">Ayrıca bkz. [nasıl yapılır: derleme ve çalıştırma bir tam Windows Forms kod örneği kullanarak Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="34cb6-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34cb6-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="34cb6-112">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.ToolStripPanel>  
 [<span data-ttu-id="34cb6-113">Nasıl yapılır: MDI için ToolStripPanels kullanma</span><span class="sxs-lookup"><span data-stu-id="34cb6-113">How to: Use ToolStripPanels for MDI</span></span>](../../../../docs/framework/winforms/controls/how-to-use-toolstrippanels-for-mdi.md)