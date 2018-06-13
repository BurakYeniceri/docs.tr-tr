---
title: 'Nasıl yapılır: Bir Windows Forms LinkLabel Denetiminden Web Sayfası Görüntüleme (Visual Basic)'
ms.date: 03/30/2017
dev_langs:
- vb
f1_keywords:
- LinkLabel1_LinkClicked
helpviewer_keywords:
- examples [Windows Forms], LinkLabel control
- Web pages [Windows Forms], displaying
- linking [Windows Forms], to Web pages from forms
- Windows Forms, linking to Web pages
- LinkLabel control [Windows Forms], examples
ms.assetid: 477a7398-5971-4de3-b24c-f49f32bdb28a
ms.openlocfilehash: a9964c8d333ea87dd995ec9111acc1a8ac1e79b0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33524189"
---
# <a name="how-to-display-a-web-page-from-a-windows-forms-linklabel-control-visual-basic"></a><span data-ttu-id="0dbba-102">Nasıl yapılır: Bir Windows Forms LinkLabel Denetiminden Web Sayfası Görüntüleme (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0dbba-102">How to: Display a Web Page from a Windows Forms LinkLabel Control (Visual Basic)</span></span>
<span data-ttu-id="0dbba-103">Bir kullanıcı bir Windows Forms tıkladığında bu örnek bir Web sayfasında varsayılan tarayıcıda görüntüler. <xref:System.Windows.Forms.LinkLabel> denetim.</span><span class="sxs-lookup"><span data-stu-id="0dbba-103">This example displays a Web page in the default browser when a user clicks a Windows Forms <xref:System.Windows.Forms.LinkLabel> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0dbba-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="0dbba-104">Example</span></span>  
  
```vb  
Private Sub Form1_Load(ByVal sender As System.Object, ByVal e _  
As System.EventArgs) Handles MyBase.Load  
    LinkLabel1.Text = "Click here to get more info."  
    LinkLabel1.Links.Add(6, 4, "www.microsoft.com")  
End Sub  
Private Sub LinkLabel1_LinkClicked(ByVal sender As System.Object, ByVal _  
e As System.Windows.Forms.LinkLabelLinkClickedEventArgs) Handles _  
LinkLabel1.LinkClicked  
    System.Diagnostics.Process.Start(e.Link.LinkData.ToString())  
End Sub  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0dbba-105">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="0dbba-105">Compiling the Code</span></span>  
 <span data-ttu-id="0dbba-106">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="0dbba-106">This example requires:</span></span>  
  
-   <span data-ttu-id="0dbba-107">Adlı bir Windows formu `Form1`.</span><span class="sxs-lookup"><span data-stu-id="0dbba-107">A Windows Form named `Form1`.</span></span>  
  
-   <span data-ttu-id="0dbba-108">A <xref:System.Windows.Forms.LinkLabel> adlı Denetim `LinkLabel1`.</span><span class="sxs-lookup"><span data-stu-id="0dbba-108">A <xref:System.Windows.Forms.LinkLabel> control named `LinkLabel1`.</span></span>  
  
-   <span data-ttu-id="0dbba-109">Etkin bir Internet bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="0dbba-109">An active Internet connection.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="0dbba-110">.NET Framework Güvenliği</span><span class="sxs-lookup"><span data-stu-id="0dbba-110">.NET Framework Security</span></span>  
 <span data-ttu-id="0dbba-111">Çağrı <xref:System.Diagnostics.Process.Start%2A> yöntemi, tam güven gerektirir.</span><span class="sxs-lookup"><span data-stu-id="0dbba-111">The call to the <xref:System.Diagnostics.Process.Start%2A> method requires full trust.</span></span> <span data-ttu-id="0dbba-112">Daha fazla bilgi için bkz. <xref:System.Security.SecurityException>.</span><span class="sxs-lookup"><span data-stu-id="0dbba-112">For more information, see <xref:System.Security.SecurityException>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0dbba-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="0dbba-113">See Also</span></span>  
 <xref:System.Windows.Forms.LinkLabel>  
 [<span data-ttu-id="0dbba-114">LinkLabel Denetimi</span><span class="sxs-lookup"><span data-stu-id="0dbba-114">LinkLabel Control</span></span>](../../../../docs/framework/winforms/controls/linklabel-control-windows-forms.md)
