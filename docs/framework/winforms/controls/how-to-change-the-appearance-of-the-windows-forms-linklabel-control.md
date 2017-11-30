---
title: "Nasıl yapılır: Windows Forms LinkLabel Denetiminin Görünüşünü Değiştirme"
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
- LinkLabel properties
- LinkLabel control [Windows Forms], changing appearance of links
- links [Windows Forms], changing appearance
- examples [Windows Forms], LinkLabel control
- LinkLabel control [Windows Forms], examples
ms.assetid: fdc5854f-5162-4457-8cbe-1042feb2d132
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 42aaef183178e7170d3046b4c5daefc8647f7cc1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-linklabel-control"></a><span data-ttu-id="a3b7c-102">Nasıl yapılır: Windows Forms LinkLabel Denetiminin Görünüşünü Değiştirme</span><span class="sxs-lookup"><span data-stu-id="a3b7c-102">How to: Change the Appearance of the Windows Forms LinkLabel Control</span></span>
<span data-ttu-id="a3b7c-103">Tarafından görüntülenen metni değiştirebilirsiniz <xref:System.Windows.Forms.LinkLabel> çeşitli amaçlarla uyacak şekilde denetim.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-103">You can change the text displayed by the <xref:System.Windows.Forms.LinkLabel> control to suit a variety of purposes.</span></span> <span data-ttu-id="a3b7c-104">Örneğin, kullanıcıya metin altı çizili olan belirli bir renk görünmesi metin ayarlayarak tıklanabilecek belirtmek yaygın bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-104">For example, it is common practice to indicate to the user that text can be clicked by setting the text to appear in a specific color with an underline.</span></span> <span data-ttu-id="a3b7c-105">Metin kullanıcı sonra farklı bir renk rengi değişir.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-105">After the user clicks the text, the color changes to a different color.</span></span> <span data-ttu-id="a3b7c-106">Bu davranışı denetlemek için beş farklı özellikleri ayarlayabilirsiniz: <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A>, <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>, <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>, ve <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> özellikleri.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-106">To control this behavior, you can set five different properties: the <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A>, <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>, <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>, <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>, and <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> properties.</span></span>  
  
### <a name="to-change-the-appearance-of-a-linklabel-control"></a><span data-ttu-id="a3b7c-107">LinkLabel denetiminin görünümünü değiştirmek için</span><span class="sxs-lookup"><span data-stu-id="a3b7c-107">To change the appearance of a LinkLabel control</span></span>  
  
1.  <span data-ttu-id="a3b7c-108">Ayarlama <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> ve <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> istediğiniz renkleri özellikleri.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-108">Set the <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> and <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> properties to the colors you want.</span></span>  
  
     <span data-ttu-id="a3b7c-109">Bu ya da program aracılığıyla veya tasarım zamanında de yapılabilir **özellikleri** penceresi.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-109">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    ' You can set the color using decimal values for red, green, and blue  
    LinkLabel1.LinkColor = Color.FromArgb(0, 0, 255)  
    ' Or you can set the color using defined constants  
    LinkLabel1.VisitedLinkColor = Color.Purple  
    ```  
  
    ```csharp  
    // You can set the color using decimal values for red, green, and blue  
    linkLabel1.LinkColor = Color.FromArgb(0, 0, 255);  
    // Or you can set the color using defined constants  
    linkLabel1.VisitedLinkColor = Color.Purple;  
    ```  
  
    ```cpp  
    // You can set the color using decimal values for red, green, and blue  
    linkLabel1->LinkColor = Color::FromArgb(0, 0, 255);  
    // Or you can set the color using defined constants  
    linkLabel1->VisitedLinkColor = Color::Purple;  
    ```  
  
2.  <span data-ttu-id="a3b7c-110">Ayarlama <xref:System.Windows.Forms.LinkLabel.Text%2A> uygun bir resim yazısı özelliğini.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-110">Set the <xref:System.Windows.Forms.LinkLabel.Text%2A> property to an appropriate caption.</span></span>  
  
     <span data-ttu-id="a3b7c-111">Bu ya da program aracılığıyla veya tasarım zamanında de yapılabilir **özellikleri** penceresi.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-111">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    LinkLabel1.Text = "Click here to see more."  
    ```  
  
    ```csharp  
    linkLabel1.Text = "Click here to see more.";  
    ```  
  
    ```cpp  
    linkLabel1->Text = "Click here to see more.";  
    ```  
  
3.  <span data-ttu-id="a3b7c-112">Ayarlama <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> resim yazısını hangi parçası bir bağlantı gösterilir belirlemek için özellik.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-112">Set the <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> property to determine which part of the caption will be indicated as a link.</span></span>  
  
     <span data-ttu-id="a3b7c-113"><xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Değeri ile temsil edilir bir <xref:System.Windows.Forms.LinkArea> iki sayı, başlangıç karakteri konumunu ve karakter sayısını içeren.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-113">The <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> value is represented with a <xref:System.Windows.Forms.LinkArea> containing two numbers, the starting character position and the number of characters.</span></span> <span data-ttu-id="a3b7c-114">Bu ya da program aracılığıyla veya tasarım zamanında de yapılabilir **özellikleri** penceresi.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-114">This can be done either programmatically or at design time in the **Properties** window.</span></span>  
  
    ```vb  
    LinkLabel1.LinkArea = new LinkArea(6,4)  
    ```  
  
    ```csharp  
    linkLabel1.LinkArea = new LinkArea(6,4);  
    ```  
  
    ```cpp  
    linkLabel1->LinkArea = LinkArea(6,4);  
    ```  
  
4.  <span data-ttu-id="a3b7c-115">Ayarlama <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> özelliğine <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline>, <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, veya <xref:System.Windows.Forms.LinkBehavior.NeverUnderline>.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-115">Set the <xref:System.Windows.Forms.LinkLabel.LinkBehavior%2A> property to <xref:System.Windows.Forms.LinkBehavior.AlwaysUnderline>, <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, or <xref:System.Windows.Forms.LinkBehavior.NeverUnderline>.</span></span>  
  
     <span data-ttu-id="a3b7c-116">Bu ayarlanırsa <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, tarafından belirlenen resim yazısı parçası <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> işaretçi üzerine getirildiğinde yalnızca altı çizili olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-116">If it is set to <xref:System.Windows.Forms.LinkBehavior.HoverUnderline>, the part of the caption determined by <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> will only be underlined when the pointer rests on it.</span></span>  
  
5.  <span data-ttu-id="a3b7c-117">İçinde <xref:System.Windows.Forms.LinkLabel.LinkClicked> olay işleyici ayarlamayı <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> özelliğine `true`.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-117">In the <xref:System.Windows.Forms.LinkLabel.LinkClicked> event handler, set the <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A> property to `true`.</span></span>  
  
     <span data-ttu-id="a3b7c-118">Bir bağlantıyı ziyaret edildiğinde görünümünü bazı şekilde genellikle renge göre değiştirmek yaygın bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-118">When a link has been visited, it is common practice to change its appearance in some way, usually by color.</span></span> <span data-ttu-id="a3b7c-119">Metin tarafından belirtilen rengi değişir <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-119">The text will change to the color specified by the <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> property.</span></span>  
  
    ```vb  
    Protected Sub LinkLabel1_LinkClicked (ByVal sender As Object, _  
       ByVal e As EventArgs) Handles LinkLabel1.LinkClicked  
       ' Change the color of the link text  
       ' by setting LinkVisited to True.  
       LinkLabel1.LinkVisited = True  
       ' Then do whatever other action is appropriate  
    End Sub  
    ```  
  
    ```csharp  
    protected void LinkLabel1_LinkClicked(object sender, System.EventArgs e)  
    {  
       // Change the color of the link text by setting LinkVisited   
       // to True.  
       linkLabel1.LinkVisited = true;  
       // Then do whatever other action is appropriate  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void linkLabel1_LinkClicked(System::Object ^  sender,  
          System::Windows::Forms::LinkLabelLinkClickedEventArgs ^  e)  
       {  
          // Change the color of the link text by setting LinkVisited   
          // to True.  
          linkLabel1->LinkVisited = true;  
          // Then do whatever other action is appropriate  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="a3b7c-120">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a3b7c-120">See Also</span></span>  
 <xref:System.Windows.Forms.LinkLabel.LinkArea%2A>  
 <xref:System.Windows.Forms.LinkLabel.LinkColor%2A>  
 <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A>  
 <xref:System.Windows.Forms.LinkLabel.LinkVisited%2A>  
 [<span data-ttu-id="a3b7c-121">LinkLabel denetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="a3b7c-121">LinkLabel Control Overview</span></span>](../../../../docs/framework/winforms/controls/linklabel-control-overview-windows-forms.md)  
 [<span data-ttu-id="a3b7c-122">Nasıl yapılır: bir nesneye veya Web sayfası Windows Forms LinkLabel denetimi ile bağlantı</span><span class="sxs-lookup"><span data-stu-id="a3b7c-122">How to: Link to an Object or Web Page with the Windows Forms LinkLabel Control</span></span>](../../../../docs/framework/winforms/controls/link-to-an-object-or-web-page-with-wf-linklabel-control.md)  
 [<span data-ttu-id="a3b7c-123">LinkLabel denetimi</span><span class="sxs-lookup"><span data-stu-id="a3b7c-123">LinkLabel Control</span></span>](../../../../docs/framework/winforms/controls/linklabel-control-windows-forms.md)