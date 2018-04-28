---
title: "Nasıl yapılır: ToolStripPanels'ni birleştirme"
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-winforms
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms], joining together
- ToolStripPanel control [Windows Forms], joining together
ms.assetid: 4eadda6d-e3b8-4151-aaf2-a8d564fbe6b3
caps.latest.revision: 8
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 80a3194b4c300bf72306abd3f080fbff9eca6e52
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2018
---
# <a name="how-to-join-toolstrippanels"></a><span data-ttu-id="c9e48-102">Nasıl yapılır: ToolStripPanels'ni birleştirme</span><span class="sxs-lookup"><span data-stu-id="c9e48-102">How to: Join ToolStripPanels</span></span>
<span data-ttu-id="c9e48-103">Katılmak <xref:System.Windows.Forms.ToolStrip> için denetimler bir <xref:System.Windows.Forms.ToolStripPanel> çalışma zamanında birden çok belge arabirimi (MDI) uygulamaları esnekliğini sağlar.</span><span class="sxs-lookup"><span data-stu-id="c9e48-103">You can join <xref:System.Windows.Forms.ToolStrip> controls to a <xref:System.Windows.Forms.ToolStripPanel> at run time, which provides the flexibility of multiple-document interface (MDI) applications.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9e48-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="c9e48-104">Example</span></span>  
 <span data-ttu-id="c9e48-105">Aşağıdaki kod örneğinde nasıl birleştirileceği gösterilmektedir <xref:System.Windows.Forms.ToolStrip> için denetimler bir <xref:System.Windows.Forms.ToolStripPanel>.</span><span class="sxs-lookup"><span data-stu-id="c9e48-105">The following code example demonstrates how to join <xref:System.Windows.Forms.ToolStrip> controls to a <xref:System.Windows.Forms.ToolStripPanel>.</span></span>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#11)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c9e48-106">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="c9e48-106">Compiling the Code</span></span>  
 <span data-ttu-id="c9e48-107">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="c9e48-107">This example requires:</span></span>  
  
-   <span data-ttu-id="c9e48-108">System.Design, System.Drawing ve System.Windows.Forms derlemelerine başvurular.</span><span class="sxs-lookup"><span data-stu-id="c9e48-108">References to the System.Design, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="c9e48-109">Bu örnek visual Basic veya Visual C# için komut satırından oluşturma hakkında daha fazla bilgi için bkz: [komut satırından derleme](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) veya [komut satırı derleme ile csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="c9e48-109">For information about building this example from the command line for visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="c9e48-110">Bu örnek Visual Studio'da yeni bir projeye kod yapıştırılarak de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9e48-110">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="c9e48-111">Ayrıca bkz. [nasıl yapılır: derleme ve çalıştırma bir tam Windows Forms kod örneği kullanarak Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="c9e48-111">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9e48-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c9e48-112">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStrip>  
 <xref:System.Windows.Forms.ToolStripPanel>  
 [<span data-ttu-id="c9e48-113">Nasıl yapılır: MDI için ToolStripPanels Kullanma</span><span class="sxs-lookup"><span data-stu-id="c9e48-113">How to: Use ToolStripPanels for MDI</span></span>](../../../../docs/framework/winforms/controls/how-to-use-toolstrippanels-for-mdi.md)
