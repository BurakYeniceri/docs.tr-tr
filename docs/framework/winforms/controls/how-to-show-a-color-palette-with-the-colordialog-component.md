---
title: 'Nasıl Yapılır: ColorDialog Bileşeni ile Renk Paleti Gösterme'
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
- cpp
helpviewer_keywords:
- palettes [Windows Forms], showing color
- color dialog box [Windows Forms], showing color palettes
- colors [Windows Forms], allowing users to select
- color palettes [Windows Forms], dialog box
- ColorDialog component [Windows Forms], showing color palettes
- color palettes [Windows Forms], showing in ColorDialog component
- colors [Windows Forms], showing palettes
ms.assetid: ee050f61-dbc8-4436-ba22-51360981ab48
caps.latest.revision: 15
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: f3f75c6ec29b82c70d4160ccc40ddb9ced0ea711
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-show-a-color-palette-with-the-colordialog-component"></a><span data-ttu-id="f6d5e-102">Nasıl Yapılır: ColorDialog Bileşeni ile Renk Paleti Gösterme</span><span class="sxs-lookup"><span data-stu-id="f6d5e-102">How to: Show a Color Palette with the ColorDialog Component</span></span>
<span data-ttu-id="f6d5e-103">[ColorDialog](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md) bileşen renk paletini görüntüler ve kullanıcının seçildi renk içeren bir özellik döndürür.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-103">The [ColorDialog](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md) component displays a palette of colors and returns a property containing the color the user has selected.</span></span>  
  
### <a name="to-choose-a-color-using-the-colordialog-component"></a><span data-ttu-id="f6d5e-104">ColorDialog bileşeni kullanarak bir renk seçmek için</span><span class="sxs-lookup"><span data-stu-id="f6d5e-104">To choose a color using the ColorDialog component</span></span>  
  
1.  <span data-ttu-id="f6d5e-105">İletişim kutusunu kullanarak görüntüleme <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-105">Display the dialog box using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
2.  <span data-ttu-id="f6d5e-106">Kullanım <xref:System.Windows.Forms.DialogResult> iletişim kutusunun nasıl kapatıldığını belirlemek için özellik.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-106">Use the <xref:System.Windows.Forms.DialogResult> property to determine how the dialog box was closed.</span></span>  
  
3.  <span data-ttu-id="f6d5e-107">Kullanım <xref:System.Windows.Forms.ColorDialog.Color%2A> özelliği <xref:System.Windows.Forms.ColorDialog> seçilen rengini ayarlamak için bileşen.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-107">Use the <xref:System.Windows.Forms.ColorDialog.Color%2A> property of the <xref:System.Windows.Forms.ColorDialog> component to set the chosen color.</span></span>  
  
     <span data-ttu-id="f6d5e-108">Aşağıdaki örnekte <xref:System.Windows.Forms.Button> denetimin <xref:System.Windows.Forms.Control.Click> olay işleyicisi açılır bir <xref:System.Windows.Forms.ColorDialog> bileşeni.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-108">In the example below, the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event handler opens a <xref:System.Windows.Forms.ColorDialog> component.</span></span> <span data-ttu-id="f6d5e-109">Bir renk seçilen ve kullanıcı olduğunda tıklar **Tamam**, <xref:System.Windows.Forms.Button> denetimin arka plan rengi, seçilen renk ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-109">When a color is chosen and the user clicks **OK**, the <xref:System.Windows.Forms.Button> control's background color is set to the chosen color.</span></span> <span data-ttu-id="f6d5e-110">Formunuz sahip örnek varsayar bir <xref:System.Windows.Forms.Button> denetim ve <xref:System.Windows.Forms.ColorDialog> bileşeni.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-110">The example assumes your form has a <xref:System.Windows.Forms.Button> control and a <xref:System.Windows.Forms.ColorDialog> component.</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
    ByVal e As System.EventArgs) Handles Button1.Click  
       If ColorDialog1.ShowDialog() = DialogResult.OK Then  
          Button1.BackColor = ColorDialog1.Color  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       if(colorDialog1.ShowDialog() == DialogResult.OK)  
       {  
          button1.BackColor = colorDialog1.Color;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,   
          System::EventArgs ^ e)  
       {  
          if(colorDialog1->ShowDialog() == DialogResult::OK)  
          {  
             button1->BackColor = colorDialog1->Color;  
          }  
       }  
    ```  
  
     <span data-ttu-id="f6d5e-111">(Visual C# [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) formun oluşturucuda olay işleyicisi kaydetmek için aşağıdaki kodu yerleştirin.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-111">(Visual C#, [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click +=   
       gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="f6d5e-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="f6d5e-112">See Also</span></span>  
 <xref:System.Windows.Forms.ColorDialog>  
 [<span data-ttu-id="f6d5e-113">ColorDialog Bileşeni</span><span class="sxs-lookup"><span data-stu-id="f6d5e-113">ColorDialog Component</span></span>](../../../../docs/framework/winforms/controls/colordialog-component-windows-forms.md)
