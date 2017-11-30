---
title: "Nasıl yapılır: BindingSource ve ResetItem Metodunu Kullanarak Değişiklik Bildirimleri Verme"
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
- change notifications [Windows Forms], raising
- data binding [Windows Forms], change notifications
- BindingSource component [Windows Forms], raising change notifications with
- data sources [Windows Forms], detecting changes
- change notifications
ms.assetid: ab8b4096-37ff-4e30-aabc-de79a2f2e972
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0ea2e260c5ca2622d650542d0cd18baca1a49288
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-raise-change-notifications-using-the-bindingsource-resetitem-method"></a><span data-ttu-id="2ef02-102">Nasıl yapılır: BindingSource ve ResetItem Metodunu Kullanarak Değişiklik Bildirimleri Verme</span><span class="sxs-lookup"><span data-stu-id="2ef02-102">How to: Raise Change Notifications Using the BindingSource ResetItem Method</span></span>
<span data-ttu-id="2ef02-103">Öğeler değişti, eklendiğinde veya bazı veri kaynakları, denetimleri için değişiklik bildirimleri yükseltmeyin.</span><span class="sxs-lookup"><span data-stu-id="2ef02-103">Some data sources for your controls do not raise change notifications when items are changed, added, or deleted.</span></span> <span data-ttu-id="2ef02-104">İle <xref:System.Windows.Forms.BindingSource> bileşeni, bu tür veri kaynaklarına bağlayın ve kodunuzdan bir değişiklik bildirimi oluştur.</span><span class="sxs-lookup"><span data-stu-id="2ef02-104">With the <xref:System.Windows.Forms.BindingSource> component, you can bind to such data sources and raise a change notification from your code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2ef02-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="2ef02-105">Example</span></span>  
 <span data-ttu-id="2ef02-106">Kullanarak bu formu gösteren bir <xref:System.Windows.Forms.BindingSource> bir listeye bağlamak için bileşen bir <xref:System.Windows.Forms.DataGridView> denetim.</span><span class="sxs-lookup"><span data-stu-id="2ef02-106">This form demonstrates using a <xref:System.Windows.Forms.BindingSource> component to bind a list to a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="2ef02-107">Listenin değişiklik bildirimleri oluşturmaz böylece <xref:System.Windows.Forms.BindingSource.ResetItem%2A> yöntemi <xref:System.Windows.Forms.BindingSource> listedeki bir öğe değiştirildiğinde çağrılır.</span><span class="sxs-lookup"><span data-stu-id="2ef02-107">The list does not raise change notifications, so the <xref:System.Windows.Forms.BindingSource.ResetItem%2A> method on the <xref:System.Windows.Forms.BindingSource> is called when an item in the list is changed.</span></span> <span data-ttu-id="2ef02-108">biçimindeki telefon numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="2ef02-108">.</span></span>  
  
 [!code-cpp[System.Windows.Forms.DataConnector.ResetItem#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetItem/CPP/form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.DataConnector.ResetItem#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetItem/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnector.ResetItem#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnector.ResetItem/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2ef02-109">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="2ef02-109">Compiling the Code</span></span>  
 <span data-ttu-id="2ef02-110">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="2ef02-110">This example requires:</span></span>  
  
-   <span data-ttu-id="2ef02-111">Sistem, System.Data, System.Drawing ve System.Windows.Forms derlemelerine başvurular.</span><span class="sxs-lookup"><span data-stu-id="2ef02-111">References to the System, System.Data, System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
 <span data-ttu-id="2ef02-112">Bu örnek için komut satırından oluşturma hakkında bilgi için [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] veya [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)], bkz: [komut satırından derleme](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) veya [komut satırı derleme ile csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span><span class="sxs-lookup"><span data-stu-id="2ef02-112">For information about building this example from the command line for [!INCLUDE[vbprvb](../../../../includes/vbprvb-md.md)] or [!INCLUDE[csprcs](../../../../includes/csprcs-md.md)], see [Building from the Command Line](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) or [Command-line Building With csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md).</span></span> <span data-ttu-id="2ef02-113">Bu örnek ayrıca oluşturmak [!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] yeni bir proje kodunu yapıştırma tarafından.</span><span class="sxs-lookup"><span data-stu-id="2ef02-113">You can also build this example in [!INCLUDE[vsprvs](../../../../includes/vsprvs-md.md)] by pasting the code into a new project.</span></span>  <span data-ttu-id="2ef02-114">Ayrıca bkz. [nasıl yapılır: derleme ve çalıştırma bir tam Windows Forms kod örneği kullanarak Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="2ef02-114">Also see [How to: Compile and Run a Complete Windows Forms Code Example Using Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2ef02-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="2ef02-115">See Also</span></span>  
 <xref:System.Windows.Forms.BindingNavigator>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.BindingSource>  
 [<span data-ttu-id="2ef02-116">BindingSource bileşeni</span><span class="sxs-lookup"><span data-stu-id="2ef02-116">BindingSource Component</span></span>](../../../../docs/framework/winforms/controls/bindingsource-component.md)  
 [<span data-ttu-id="2ef02-117">Nasıl yapılır: Windows Forms denetimini bir türe bağlama</span><span class="sxs-lookup"><span data-stu-id="2ef02-117">How to: Bind a Windows Forms Control to a Type</span></span>](../../../../docs/framework/winforms/controls/how-to-bind-a-windows-forms-control-to-a-type.md)
