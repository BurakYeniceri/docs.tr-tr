---
title: 'Nasıl yapılır: Veri Girişi İçin Yeniden Boyutlandırılabilir Windows Formu Oluşturma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms]
- layout [Windows Forms], resizing
- forms [Windows Forms], creating resizable
- Windows Forms, resizable
ms.assetid: babdf198-404c-485d-a914-ed370c6ecd99
ms.openlocfilehash: a7768b3c6be10373e742cbeea0028d1aee0b261d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33531797"
---
# <a name="how-to-create-a-resizable-windows-form-for-data-entry"></a><span data-ttu-id="89498-102">Nasıl yapılır: Veri Girişi İçin Yeniden Boyutlandırılabilir Windows Formu Oluşturma</span><span class="sxs-lookup"><span data-stu-id="89498-102">How to: Create a Resizable Windows Form for Data Entry</span></span>
<span data-ttu-id="89498-103">İyi bir düzen de kendi üst formu boyutlarındaki değişiklikleri yanıtlar.</span><span class="sxs-lookup"><span data-stu-id="89498-103">A good layout responds well to changes in the dimensions of its parent form.</span></span> <span data-ttu-id="89498-104">Kullanabileceğiniz <xref:System.Windows.Forms.TableLayoutPanel> yeniden boyutlandırma ve, denetimleri tutarlı bir şekilde formun boyutları değiştikçe konumlandırmak form düzenini düzenlemek için denetim.</span><span class="sxs-lookup"><span data-stu-id="89498-104">You can use the <xref:System.Windows.Forms.TableLayoutPanel> control to arrange the layout of your form to resize and position your controls in a consistent way as the form's dimensions change.</span></span> <span data-ttu-id="89498-105"><xref:System.Windows.Forms.TableLayoutPanel> Denetimidir de yararlıdır denetimlerinizi içerikte neden değişiklikleri yerleşiminde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="89498-105">The <xref:System.Windows.Forms.TableLayoutPanel> control is also useful when changes in the contents of your controls cause changes in the layout.</span></span> <span data-ttu-id="89498-106">Bu yordamda kapsamdaki işlemi Visual Studio ortamında yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="89498-106">The process covered in this procedure can be done within the Visual Studio environment.</span></span>  <span data-ttu-id="89498-107">Ayrıca bkz. [izlenecek yol: veri girişi için yeniden boyutlandırılabilir Windows formu oluşturma](http://msdn.microsoft.com/library/991eahec\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="89498-107">Also see [Walkthrough: Creating a Resizable Windows Form for Data Entry](http://msdn.microsoft.com/library/991eahec\(v=vs.110\)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="89498-108">Örnek</span><span class="sxs-lookup"><span data-stu-id="89498-108">Example</span></span>  
 <span data-ttu-id="89498-109">Aşağıdaki örnekte nasıl kullanılacağını gösteren bir <xref:System.Windows.Forms.TableLayoutPanel> iyi zaman formun kullanıcı göre yeniden boyutlandırır yanıt verdiğini bir düzen oluşturmak için denetim.</span><span class="sxs-lookup"><span data-stu-id="89498-109">The following example demonstrates how to use a <xref:System.Windows.Forms.TableLayoutPanel> control to build a layout that responds well when the user resizes the form.</span></span> <span data-ttu-id="89498-110">Ayrıca, yerelleştirmeye iyi cevap veren bir düzen gösterir.</span><span class="sxs-lookup"><span data-stu-id="89498-110">It also demonstrates a layout that responds well to localization.</span></span>  
  
 [!code-cpp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/cpp/basicdataentryform.cpp#1)]
 [!code-csharp[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/CS/basicdataentryform.cs#1)]
 [!code-vb[System.Windows.Forms.TableLayoutPanel.DataEntryForm#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.TableLayoutPanel.DataEntryForm/VB/basicdataentryform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="89498-111">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="89498-111">Compiling the Code</span></span>  
 <span data-ttu-id="89498-112">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="89498-112">This example requires:</span></span>  
  
-   <span data-ttu-id="89498-113">Sistem, System.Data, System.Drawing ve System.Windows.Forms derlemelerine başvurular.</span><span class="sxs-lookup"><span data-stu-id="89498-113">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="89498-114">Visual Basic veya Visual C# için bu örnek komut satırından oluşturma hakkında daha fazla bilgi için bkz: [komut satırından derleme](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) veya [komut satırı derleme ile csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="89498-114">For information about building this example from the command line for Visual Basic or Visual C#, see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="89498-115">Bu örnek Visual Studio'da yeni bir projeye kod yapıştırılarak de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89498-115">You can also build this example in Visual Studio by pasting the code into a new project.</span></span>  <span data-ttu-id="89498-116">Ayrıca bkz. [nasıl yapılır: derleme ve çalıştırma bir tam Windows Forms kod örneği kullanarak Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="89498-116">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89498-117">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="89498-117">See Also</span></span>  
 <xref:System.Windows.Forms.FlowLayoutPanel>  
 <xref:System.Windows.Forms.TableLayoutPanel>  
 [<span data-ttu-id="89498-118">Nasıl yapılır: TableLayoutPanel Denetiminde Alt Denetimleri Sabitleme ve Yerleştirme</span><span class="sxs-lookup"><span data-stu-id="89498-118">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../../../../docs/framework/winforms/controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)  
 [<span data-ttu-id="89498-119">Nasıl yapılır: Yerelleştirmeye İyi Cevap Veren Bir Windows Forms Düzeni Tasarlama</span><span class="sxs-lookup"><span data-stu-id="89498-119">How to: Design a Windows Forms Layout that Responds Well to Localization</span></span>](../../../../docs/framework/winforms/controls/how-to-design-a-windows-forms-layout-that-responds-well-to-localization.md)  
 [<span data-ttu-id="89498-120">Microsoft Windows kullanıcı deneyimi, kullanıcı arabirimi geliştiricilerin ve tasarımcıların resmi yönergeleri. Redmond, WA: Microsoft Press, 1999. (USBN: 0-7356-0566-1)</span><span class="sxs-lookup"><span data-stu-id="89498-120">Microsoft Windows User Experience, Official Guidelines for User Interface Developers and Designers. Redmond, WA: Microsoft Press, 1999. (USBN: 0-7356-0566-1)</span></span>](http://www.microsoft.com/mspress/southpacific/books/book11588.htm)
