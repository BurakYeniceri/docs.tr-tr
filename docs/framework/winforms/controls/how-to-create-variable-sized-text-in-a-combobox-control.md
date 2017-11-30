---
title: "Nasıl yapılır: ComboBox Denetiminde Değişken Boyutlu Metin Oluşturma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: vb
helpviewer_keywords:
- text [Windows Forms], drawing in combo boxes
- examples [Windows Forms], ComboBox control
- combo boxes [Windows Forms], drawing text
- ComboBox control [Windows Forms], examples [C#]
- ComboBox control [Windows Forms], drawing custom text
ms.assetid: ce39b9ea-e626-49fe-bd5a-f567f6d157df
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: a6f0dcfd24414ef868a1a5414af4fcde1b9a14ec
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-create-variable-sized-text-in-a-combobox-control"></a><span data-ttu-id="5d0cc-102">Nasıl yapılır: ComboBox Denetiminde Değişken Boyutlu Metin Oluşturma</span><span class="sxs-lookup"><span data-stu-id="5d0cc-102">How to: Create Variable Sized Text in a ComboBox Control</span></span>
<span data-ttu-id="5d0cc-103">Örnek metin özel çizim gösterir bir <xref:System.Windows.Forms.ComboBox> denetim.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-103">This example demonstrates custom drawing of text in a <xref:System.Windows.Forms.ComboBox> control.</span></span> <span data-ttu-id="5d0cc-104">Bir öğe belirli bir ölçütü karşıladığında büyük yazı tipiyle çizilmiş ve kırmızı açık.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-104">When an item meets a certain criteria, it is drawn in a larger font and turned red.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5d0cc-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="5d0cc-105">Example</span></span>  
  
```vb  
Private Sub ComboBox1_MeasureItem(ByVal sender As Object, ByVal e As _  
System.Windows.Forms.MeasureItemEventArgs) Handles ComboBox1.MeasureItem  
    Dim bFont As New Font("Arial", 8, FontStyle.Bold)  
    Dim lFont As New Font("Arial", 12, FontStyle.Bold)  
    Dim siText As SizeF  
  
    If ComboBox1.Items().Item(e.Index) = "Two" Then  
        siText = e.Graphics.MeasureString(ComboBox1.Items().Item(e.Index), _  
lFont)  
    Else  
        siText = e.Graphics.MeasureString(ComboBox1.Items().Item(e.Index), bFont)  
    End If  
  
    e.ItemHeight = siText.Height  
    e.ItemWidth = siText.Width  
End Sub  
  
Private Sub ComboBox1_DrawItem(ByVal sender As Object, ByVal e As _  
System.Windows.Forms.DrawItemEventArgs) Handles ComboBox1.DrawItem  
    Dim g As Graphics = e.Graphics  
    Dim bFont As New Font("Arial", 8, FontStyle.Bold)  
    Dim lFont As New Font("Arial", 12, FontStyle.Bold)  
  
    If ComboBox1.Items().Item(e.Index) = "Two" Then  
        g.DrawString(ComboBox1.Items.Item(e.Index), lfont, Brushes.Red, _  
e.Bounds.X, e.Bounds.Y)  
    Else  
        g.DrawString(ComboBox1.Items.Item(e.Index), bFont, Brushes.Black, e.Bounds.X, e.Bounds.Y)  
    End If  
End Sub  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5d0cc-106">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="5d0cc-106">Compiling the Code</span></span>  
 <span data-ttu-id="5d0cc-107">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-107">This example requires:</span></span>  
  
-   <span data-ttu-id="5d0cc-108">Bir Windows formu.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-108">A Windows form.</span></span>  
  
-   <span data-ttu-id="5d0cc-109">A <xref:System.Windows.Forms.ComboBox> adlı Denetim `ListBox1` üç öğelerle <xref:System.Windows.Forms.ComboBox.Items%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-109">A <xref:System.Windows.Forms.ComboBox> control named `ListBox1` with three items in the <xref:System.Windows.Forms.ComboBox.Items%2A> property.</span></span> <span data-ttu-id="5d0cc-110">Bu örnekte, üç öğe adlı `"One", Two", and Three"`.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-110">In this example, the three items are named `"One", Two", and Three"`.</span></span> <span data-ttu-id="5d0cc-111"><xref:System.Windows.Forms.ComboBox.DrawMode%2A> Özelliği `ComboBox1` ayarlanmalıdır <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable>.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-111">The <xref:System.Windows.Forms.ComboBox.DrawMode%2A> property of `ComboBox1` must be set to <xref:System.Windows.Forms.DrawMode.OwnerDrawVariable>.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="5d0cc-112">Bu teknik da geçerlidir <xref:System.Windows.Forms.ListBox> denetim — yerine, bir <xref:System.Windows.Forms.ListBox> için <xref:System.Windows.Forms.ComboBox>.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-112">This technique is also applicable to the <xref:System.Windows.Forms.ListBox> control — you can substitute a <xref:System.Windows.Forms.ListBox> for the <xref:System.Windows.Forms.ComboBox>.</span></span>  
  
-   <span data-ttu-id="5d0cc-113">Başvurular <xref:System.Windows.Forms?displayProperty=nameWithType> ve <xref:System.Drawing?displayProperty=nameWithType> ad alanları.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-113">References to the <xref:System.Windows.Forms?displayProperty=nameWithType> and <xref:System.Drawing?displayProperty=nameWithType> namespaces.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5d0cc-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-114">See Also</span></span>  
 <xref:System.Windows.Forms.ComboBox.DrawItem>  
 <xref:System.Windows.Forms.DrawItemEventArgs>  
 <xref:System.Windows.Forms.ComboBox.MeasureItem>  
 [<span data-ttu-id="5d0cc-115">Yerleşik sahip çizimi destekli denetimler</span><span class="sxs-lookup"><span data-stu-id="5d0cc-115">Controls with Built-In Owner-Drawing Support</span></span>](../../../../docs/framework/winforms/controls/controls-with-built-in-owner-drawing-support.md)  
 [<span data-ttu-id="5d0cc-116">ListBox denetimi</span><span class="sxs-lookup"><span data-stu-id="5d0cc-116">ListBox Control</span></span>](../../../../docs/framework/winforms/controls/listbox-control-windows-forms.md)  
 [<span data-ttu-id="5d0cc-117">ComboBox denetimi</span><span class="sxs-lookup"><span data-stu-id="5d0cc-117">ComboBox Control</span></span>](../../../../docs/framework/winforms/controls/combobox-control-windows-forms.md)