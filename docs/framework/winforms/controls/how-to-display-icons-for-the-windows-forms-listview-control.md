---
title: "Nasıl yapılır: Windows Forms ListView Denetimi için Simgeler Görüntüleme"
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
- ListView control [Windows Forms], displaying icons
- icons [Windows Forms], displaying for ListView controls
- lists [Windows Forms], displaying icons
- ImageList component [Windows Forms], with ListView control
- list views [Windows Forms], displaying icons
ms.assetid: 9d577542-8595-429b-99e5-078770ec9d35
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0d9a8bdc54f3f321b37bda897aac1f340f7a46aa
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-display-icons-for-the-windows-forms-listview-control"></a><span data-ttu-id="6def3-102">Nasıl yapılır: Windows Forms ListView Denetimi için Simgeler Görüntüleme</span><span class="sxs-lookup"><span data-stu-id="6def3-102">How to: Display Icons for the Windows Forms ListView Control</span></span>
<span data-ttu-id="6def3-103">Windows Forms <xref:System.Windows.Forms.ListView> denetim, üç görüntü listelerinden simgeler görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="6def3-103">The Windows Forms <xref:System.Windows.Forms.ListView> control can display icons from three image lists.</span></span> <span data-ttu-id="6def3-104">Belirtilen görüntü listesinden görüntü listesi, Ayrıntılar ve SmallIcon görünümleri görüntülemek <xref:System.Windows.Forms.ListView.SmallImageList%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="6def3-104">The List, Details, and SmallIcon views display images from the image list specified in the <xref:System.Windows.Forms.ListView.SmallImageList%2A> property.</span></span> <span data-ttu-id="6def3-105">Belirtilen görüntü listesinden görüntü LargeIcon görüntüleyen <xref:System.Windows.Forms.ListView.LargeImageList%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="6def3-105">The LargeIcon view displays images from the image list specified in the <xref:System.Windows.Forms.ListView.LargeImageList%2A> property.</span></span> <span data-ttu-id="6def3-106">Bir liste görünümü de kümesinde simgeler, ek bir dizi görüntüleyebilirsiniz <xref:System.Windows.Forms.ListView.StateImageList%2A> büyük veya küçük simgeleri yanındaki özelliği.</span><span class="sxs-lookup"><span data-stu-id="6def3-106">A list view can also display an additional set of icons, set in the <xref:System.Windows.Forms.ListView.StateImageList%2A> property, next to the large or small icons.</span></span> <span data-ttu-id="6def3-107">Görüntü listeleri hakkında daha fazla bilgi için bkz: [ImageList bileşeni](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md) ve [nasıl yapılır: Windows Forms ImageList bileşeni ile görüntüleri ekleme veya kaldırma](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span><span class="sxs-lookup"><span data-stu-id="6def3-107">For more information about image lists, see [ImageList Component](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md) and [How to: Add or Remove Images with the Windows Forms ImageList Component](../../../../docs/framework/winforms/controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md).</span></span>  
  
### <a name="to-display-images-in-a-list-view"></a><span data-ttu-id="6def3-108">Görüntüleri listesini görüntülemek için</span><span class="sxs-lookup"><span data-stu-id="6def3-108">To display images in a list view</span></span>  
  
1.  <span data-ttu-id="6def3-109">Uygun özelliğini ayarlayın —<xref:System.Windows.Forms.ListView.SmallImageList%2A>, <xref:System.Windows.Forms.ListView.LargeImageList%2A>, veya <xref:System.Windows.Forms.ListView.StateImageList%2A>— varolan <xref:System.Windows.Forms.ImageList> kullanmak istediğiniz bileşeni.</span><span class="sxs-lookup"><span data-stu-id="6def3-109">Set the appropriate property—<xref:System.Windows.Forms.ListView.SmallImageList%2A>, <xref:System.Windows.Forms.ListView.LargeImageList%2A>, or <xref:System.Windows.Forms.ListView.StateImageList%2A>—to the existing <xref:System.Windows.Forms.ImageList> component you wish to use.</span></span>  
  
     <span data-ttu-id="6def3-110">Bu özellikleri Özellikler penceresini tasarımcıyla veya kodu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6def3-110">These properties can be set in the designer with the Properties window, or in code.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#41)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#41)]  
  
2.  <span data-ttu-id="6def3-111">Ayarlama <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> veya <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> ilişkili bir simgesi var her liste öğesi için özelliği.</span><span class="sxs-lookup"><span data-stu-id="6def3-111">Set the <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> or <xref:System.Windows.Forms.ListViewItem.StateImageIndex%2A> property for each list item that has an associated icon.</span></span>  
  
     <span data-ttu-id="6def3-112">Bu özellikler ayarlanabilir, kod veya içinde **ListViewItem Koleksiyonu Düzenleyicisi**.</span><span class="sxs-lookup"><span data-stu-id="6def3-112">These properties can be set in code, or within the **ListViewItem Collection Editor**.</span></span> <span data-ttu-id="6def3-113">Açmak için **ListViewItem Koleksiyonu Düzenleyicisi**, üç nokta düğmesini (![VisualStudioEllipsesButton ekran](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) yanındaki<xref:System.Windows.Forms.ListView.Items%2A>özelliği **özellikleri** penceresi.</span><span class="sxs-lookup"><span data-stu-id="6def3-113">To open the **ListViewItem Collection Editor**, click the ellipsis button (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.ListView.Items%2A> property on the **Properties** window.</span></span>  
  
     [!code-csharp[System.Windows.Forms.ListViewLegacyTopics#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/CS/Class1.cs#42)]
     [!code-vb[System.Windows.Forms.ListViewLegacyTopics#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListViewLegacyTopics/VB/Class1.vb#42)]  
  
## <a name="see-also"></a><span data-ttu-id="6def3-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="6def3-114">See Also</span></span>  
 [<span data-ttu-id="6def3-115">ListView denetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6def3-115">ListView Control Overview</span></span>](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)  
 [<span data-ttu-id="6def3-116">Nasıl yapılır: ekleme ve kaldırma öğeleri Windows Forms ListView denetimi</span><span class="sxs-lookup"><span data-stu-id="6def3-116">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)  
 [<span data-ttu-id="6def3-117">Nasıl yapılır: sütunları Windows Forms ListView denetimine ekleme</span><span class="sxs-lookup"><span data-stu-id="6def3-117">How to: Add Columns to the Windows Forms ListView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-add-columns-to-the-windows-forms-listview-control.md)  
 [<span data-ttu-id="6def3-118">Nasıl yapılır: bir TreeView veya ListView denetimi (Windows Forms) özel bilgi ekleme</span><span class="sxs-lookup"><span data-stu-id="6def3-118">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)  
 [<span data-ttu-id="6def3-119">ImageList bileşeni</span><span class="sxs-lookup"><span data-stu-id="6def3-119">ImageList Component</span></span>](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md)
