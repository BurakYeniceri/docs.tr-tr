---
title: "Nasıl yapılır: Windows Forms NumericUpDown Denetiminin Biçimini Ayarlama"
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
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 001cc32aa9e1f31695f3b349480b6dd5154b31a8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a><span data-ttu-id="f6797-102">Nasıl yapılır: Windows Forms NumericUpDown Denetiminin Biçimini Ayarlama</span><span class="sxs-lookup"><span data-stu-id="f6797-102">How to: Set the Format for the Windows Forms NumericUpDown Control</span></span>
<span data-ttu-id="f6797-103">Windows Forms'ta değerlerin nasıl görüntüleneceğini yapılandırabilirsiniz <xref:System.Windows.Forms.NumericUpDown> denetim.</span><span class="sxs-lookup"><span data-stu-id="f6797-103">You can configure how values are displayed in the Windows Forms <xref:System.Windows.Forms.NumericUpDown> control.</span></span> <span data-ttu-id="f6797-104"><xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> Özelliği, kaç tane numaraları görünür ondalık ayırıcıdan sonra belirler; varsayılan değer 0'dır.</span><span class="sxs-lookup"><span data-stu-id="f6797-104">The <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> property determines how many numbers appear after the decimal point; the default is 0.</span></span> <span data-ttu-id="f6797-105"><xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> Özelliği, her üç ondalık basamak arasında bir ayırıcı eklenip eklenmeyeceğini belirler; varsayılan `false`.</span><span class="sxs-lookup"><span data-stu-id="f6797-105">The <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> property determines whether a separator will be inserted between every three decimal digits; the default is `false`.</span></span> <span data-ttu-id="f6797-106">Denetim değerleri ondalık biçiminde yerine onaltılık görüntüleyebilirsiniz <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> özelliği ayarlanmış `true`; varsayılan `false`.</span><span class="sxs-lookup"><span data-stu-id="f6797-106">The control can display values in hexadecimal instead of decimal format, if the <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> property is set to `true`; the default is `false`.</span></span>  
  
### <a name="to-format-the-numeric-value"></a><span data-ttu-id="f6797-107">Sayısal değer biçimlendirmek için</span><span class="sxs-lookup"><span data-stu-id="f6797-107">To format the numeric value</span></span>  
  
-   <span data-ttu-id="f6797-108">Ayarlayarak ondalık bir değeri görüntülemek <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> özelliği bir tamsayı ve ayarı için <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> özelliğine `true` veya `false`.</span><span class="sxs-lookup"><span data-stu-id="f6797-108">Display a decimal value by setting the <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> property to an integer and setting the <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> property to `true` or `false`.</span></span>  
  
    ```vb  
    NumericUpDown1.DecimalPlaces = 2  
    NumericUpDown1.ThousandsSeparator = True  
    ```  
  
    ```csharp  
    numericUpDown1.DecimalPlaces = 2;  
    numericUpDown1.ThousandsSeparator = true;  
    ```  
  
    ```cpp  
    numericUpDown1->DecimalPlaces = 2;  
    numericUpDown1->ThousandsSeparator = true;  
    ```  
  
     <span data-ttu-id="f6797-109">veya</span><span class="sxs-lookup"><span data-stu-id="f6797-109">-or-</span></span>  
  
-   <span data-ttu-id="f6797-110">Bir onaltılık değer ayarlayarak görüntüler <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> özelliğine `true`.</span><span class="sxs-lookup"><span data-stu-id="f6797-110">Display a hexadecimal value by setting the <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> property to `true`.</span></span>  
  
    ```vb  
    NumericUpDown1.Hexadecimal = True  
    ```  
  
    ```csharp  
    numericUpDown1.Hexadecimal = true;  
    ```  
  
    ```cpp  
    numericUpDown1->Hexadecimal = true;  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="f6797-111">Değeri, onaltılık olarak form üzerinde görüntülenir olsa bile, tüm testler gerçekleştirdiğiniz <xref:System.Windows.Forms.NumericUpDown.Value%2A> özellik ondalık değerini test.</span><span class="sxs-lookup"><span data-stu-id="f6797-111">Even if the value is displayed on the form as hexadecimal, any tests you perform on the <xref:System.Windows.Forms.NumericUpDown.Value%2A> property will be testing its decimal value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6797-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="f6797-112">See Also</span></span>  
 <xref:System.Windows.Forms.NumericUpDown>  
 [<span data-ttu-id="f6797-113">NumericUpDown denetimi</span><span class="sxs-lookup"><span data-stu-id="f6797-113">NumericUpDown Control</span></span>](../../../../docs/framework/winforms/controls/numericupdown-control-windows-forms.md)  
 [<span data-ttu-id="f6797-114">NumericUpDown denetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f6797-114">NumericUpDown Control Overview</span></span>](../../../../docs/framework/winforms/controls/numericupdown-control-overview-windows-forms.md)