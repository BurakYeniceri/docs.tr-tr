---
title: 'Nasıl yapılır: Windows Forms ToolTip Bileşeninin Gecikmesini Değiştirme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolTip component [Windows Forms], delay values
- tooltips [Windows Forms], delay values
- examples [Windows Forms], tooltips
ms.assetid: 08979ba7-dd84-477b-ab17-8d06e759be99
ms.openlocfilehash: 20dcd941b142daa672312edb618a1c3e4597442d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33530435"
---
# <a name="how-to-change-the-delay-of-the-windows-forms-tooltip-component"></a><span data-ttu-id="17082-102">Nasıl yapılır: Windows Forms ToolTip Bileşeninin Gecikmesini Değiştirme</span><span class="sxs-lookup"><span data-stu-id="17082-102">How to: Change the Delay of the Windows Forms ToolTip Component</span></span>
<span data-ttu-id="17082-103">Windows Forms için ayarlayabileceğiniz birden çok gecikme değerler <xref:System.Windows.Forms.ToolTip> bileşeni.</span><span class="sxs-lookup"><span data-stu-id="17082-103">There are multiple delay values that you can set for a Windows Forms <xref:System.Windows.Forms.ToolTip> component.</span></span> <span data-ttu-id="17082-104">Bu özellikleri milisaniye ölçü birimidir.</span><span class="sxs-lookup"><span data-stu-id="17082-104">The unit of measure for all these properties is milliseconds.</span></span> <span data-ttu-id="17082-105"><xref:System.Windows.Forms.ToolTip.InitialDelay%2A> Özelliği belirler ne kadar süreyle kullanıcı için görüntülenecek araç ipucu dize ilişkili denetim noktasına gerekir.</span><span class="sxs-lookup"><span data-stu-id="17082-105">The <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> property determines how long the user must point at the associated control for the ToolTip string to appear.</span></span> <span data-ttu-id="17082-106"><xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> Özelliği ayarlar geçen bir araç ipucu ilişkili denetimden fareyi hareket ederken görünmesi sonraki araç ipucu dizeleri için milisaniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="17082-106">The <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> property sets the number of milliseconds it takes for subsequent ToolTip strings to appear as the mouse moves from one ToolTip-associated control to another.</span></span> <span data-ttu-id="17082-107"><xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> Özelliği, araç ipucu dize gösterilir süreyi belirler.</span><span class="sxs-lookup"><span data-stu-id="17082-107">The <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> property determines the length of time the ToolTip string is shown.</span></span> <span data-ttu-id="17082-108">Ayrı ayrı veya değerini ayarlayarak bu değerleri ayarlayabileceğiniz <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> özellik; özellikler ayarlandığında tabanlı atanan değer diğer gecikme <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="17082-108">You can set these values individually, or by setting the value of the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property; the other delay properties are set based on the value assigned to the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property.</span></span> <span data-ttu-id="17082-109">Örneğin, <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> N değerine ayarlayın <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> N olarak ayarlanmışsa <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> değerine ayarlanmış <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> beş tarafından bölünmüş (veya N/5), ve <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> beş kez değeri olan bir değer ayarlamak <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> özelliği (veya 5N).</span><span class="sxs-lookup"><span data-stu-id="17082-109">For example, when <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> is set to a value N, <xref:System.Windows.Forms.ToolTip.InitialDelay%2A> is set to N, <xref:System.Windows.Forms.ToolTip.ReshowDelay%2A> is set to the value of <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> divided by five (or N/5), and <xref:System.Windows.Forms.ToolTip.AutoPopDelay%2A> is set to a value that is five times the value of the <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> property (or 5N).</span></span>  
  
### <a name="to-set-the-delay"></a><span data-ttu-id="17082-110">Gecikme ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="17082-110">To set the delay</span></span>  
  
1.  <span data-ttu-id="17082-111">Bu örnekte gösterildiği gibi aşağıdaki özellikleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="17082-111">Set the following properties as shown in this example.</span></span>  
  
    ```vb  
    ToolTip1.InitialDelay = 500  
    ToolTip1.ReshowDelay = 100  
    ToolTip1.AutoPopDelay = 5000  
    ```  
  
    ```csharp  
    ToolTip1.InitialDelay = 500;  
    ToolTip1.ReshowDelay = 100;  
    ToolTip1.AutoPopDelay = 5000;  
    ```  
  
    ```cpp  
    toolTip1->InitialDelay = 500;  
    toolTip1->ReshowDelay = 100;  
    toolTip1->AutoPopDelay = 5000;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="17082-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="17082-112">See Also</span></span>  
 [<span data-ttu-id="17082-113">ToolTip Bileşenine Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="17082-113">ToolTip Component Overview</span></span>](../../../../docs/framework/winforms/controls/tooltip-component-overview-windows-forms.md)  
 [<span data-ttu-id="17082-114">Nasıl yapılır: Tasarım Zamanında Windows Formundaki Denetimler için ToolTips Ayarlama</span><span class="sxs-lookup"><span data-stu-id="17082-114">How to: Set ToolTips for Controls on a Windows Form at Design Time</span></span>](../../../../docs/framework/winforms/controls/how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)  
 [<span data-ttu-id="17082-115">ToolTip Bileşeni</span><span class="sxs-lookup"><span data-stu-id="17082-115">ToolTip Component</span></span>](../../../../docs/framework/winforms/controls/tooltip-component-windows-forms.md)
