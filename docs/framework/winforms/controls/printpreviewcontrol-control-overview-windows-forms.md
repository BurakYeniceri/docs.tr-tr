---
title: "PrintPreviewControl Denetimine Genel Bakış (Windows Forms)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: PrintPreviewControl
helpviewer_keywords:
- print preview
- PrintPreviewControl control
ms.assetid: 4513c6c7-5e9b-4f4c-82ca-00f993a26955
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 47bef441b01d8bdcf9a365c341005cff28c64f27
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="printpreviewcontrol-control-overview-windows-forms"></a><span data-ttu-id="c9220-102">PrintPreviewControl Denetimine Genel Bakış (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="c9220-102">PrintPreviewControl Control Overview (Windows Forms)</span></span>
<span data-ttu-id="c9220-103">Windows Forms <xref:System.Windows.Forms.PrintPreviewControl> görüntülemek için kullanılan bir [PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md) yazdırıldığında görüneceği şekilde.</span><span class="sxs-lookup"><span data-stu-id="c9220-103">The Windows Forms <xref:System.Windows.Forms.PrintPreviewControl> is used to display a [PrintDocument](../../../../docs/framework/winforms/controls/printdocument-component-windows-forms.md) as it will appear when printed.</span></span> <span data-ttu-id="c9220-104">Bu denetim yok düğmeler veya diğer kullanıcı arabirimi öğeleri nedenle genellikle kullandığınız sahip <xref:System.Windows.Forms.PrintPreviewControl> yalnızca kendi Baskı Önizleme kullanıcı arabirimini yazmak istiyorsanız.</span><span class="sxs-lookup"><span data-stu-id="c9220-104">This control has no buttons or other user interface elements, so typically you use the <xref:System.Windows.Forms.PrintPreviewControl> only if you wish to write your own print-preview user interface.</span></span> <span data-ttu-id="c9220-105">Standart kullanıcı arabirimi istiyorsanız kullanın bir <xref:System.Windows.Forms.PrintPreviewDialog> denetlemek; bkz [PrintPreviewDialog denetimine genel bakış](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md) bir genel bakış.</span><span class="sxs-lookup"><span data-stu-id="c9220-105">If you want the standard user interface, use a <xref:System.Windows.Forms.PrintPreviewDialog> control; see [PrintPreviewDialog Control Overview](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md) for an overview.</span></span>  
  
## <a name="key-properties"></a><span data-ttu-id="c9220-106">Anahtar Özellikler</span><span class="sxs-lookup"><span data-stu-id="c9220-106">Key Properties</span></span>  
 <span data-ttu-id="c9220-107">Denetimin anahtar özelliği <xref:System.Windows.Forms.PrintPreviewControl.Document%2A>, önizlemesi belgeye ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9220-107">The control's key property is <xref:System.Windows.Forms.PrintPreviewControl.Document%2A>, which sets the document to be previewed.</span></span> <span data-ttu-id="c9220-108">Belge olmalıdır bir <xref:System.Drawing.Printing.PrintDocument> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c9220-108">The document must be a <xref:System.Drawing.Printing.PrintDocument> object.</span></span> <span data-ttu-id="c9220-109">Yazdırma için belgeler oluşturma genel bakış için bkz: [PrintDocument bileşenine genel bakış](../../../../docs/framework/winforms/controls/printdocument-component-overview-windows-forms.md) ve [Windows Forms yazdırma desteği](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md).</span><span class="sxs-lookup"><span data-stu-id="c9220-109">For an overview of creating documents for printing, see [PrintDocument Component Overview](../../../../docs/framework/winforms/controls/printdocument-component-overview-windows-forms.md) and [Windows Forms Print Support](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md).</span></span> <span data-ttu-id="c9220-110"><xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> Ve <xref:System.Windows.Forms.PrintPreviewControl.Rows%2A> özellikleri, yatay ve dikey olarak denetiminde görüntülenen sayfaların sayısını belirler.</span><span class="sxs-lookup"><span data-stu-id="c9220-110">The <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> and <xref:System.Windows.Forms.PrintPreviewControl.Rows%2A> properties determine the number of pages displayed horizontally and vertically on the control.</span></span> <span data-ttu-id="c9220-111">Düzgünleştirme metnin sorunsuz görünmesini sağlayabilirsiniz, ancak daha yavaş görüntü yapabilirsiniz; Bunu kullanmak üzere ayarlanmış <xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A> özelliğine `true`.</span><span class="sxs-lookup"><span data-stu-id="c9220-111">Antialiasing can make the text appear smoother, but it can also make the display slower; to use it, set the <xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A> property to `true`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9220-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c9220-112">See Also</span></span>  
 <xref:System.Windows.Forms.PrintPreviewControl>  
 [<span data-ttu-id="c9220-113">PrintPreviewDialog denetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c9220-113">PrintPreviewDialog Control Overview</span></span>](../../../../docs/framework/winforms/controls/printpreviewdialog-control-overview-windows-forms.md)  
 [<span data-ttu-id="c9220-114">PrintPreviewControl denetimi</span><span class="sxs-lookup"><span data-stu-id="c9220-114">PrintPreviewControl Control</span></span>](../../../../docs/framework/winforms/controls/printpreviewcontrol-control-windows-forms.md)  
 [<span data-ttu-id="c9220-115">İletişim kutusu denetimleri ve bileşenleri</span><span class="sxs-lookup"><span data-stu-id="c9220-115">Dialog-Box Controls and Components</span></span>](../../../../docs/framework/winforms/controls/dialog-box-controls-and-components-windows-forms.md)