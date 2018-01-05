---
title: "Windows Forms'ta Olayların Sırası"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- events [Windows Forms], order of
- focus event order
- application shutdown event order
- sequence [Windows Forms], of events
- validation events [Windows Forms], order of
- application startup event order
ms.assetid: e81db09b-4453-437f-b78a-62d7cd5c9829
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 03d2661752e5c0acb36fe76a8fa72b0638b4ad54
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="order-of-events-in-windows-forms"></a><span data-ttu-id="22812-102">Windows Forms'ta Olayların Sırası</span><span class="sxs-lookup"><span data-stu-id="22812-102">Order of Events in Windows Forms</span></span>
<span data-ttu-id="22812-103">Windows Forms uygulamalarında olayları ortaya geliştiricilere bu olayların her biri sırayla işleme ile ilgili belirli ilgi sırasıdır.</span><span class="sxs-lookup"><span data-stu-id="22812-103">The order in which events are raised in Windows Forms applications is of particular interest to developers concerned with handling each of these events in turn.</span></span> <span data-ttu-id="22812-104">Bir durum olayların ne zaman formun bölümleri yeniden gibi ince işleme çağırdığında bir tanıma olaylar çalışma zamanında oluşturulur kesin siparişi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="22812-104">When a situation calls for meticulous handling of events, such as when you are redrawing parts of the form, an awareness of the precise order in which events are raised at run time is necessary.</span></span> <span data-ttu-id="22812-105">Bu konu, uygulamalar ve denetimleri ömrü içinde birkaç önemli aşamaları sırasında olayları terabayt bazı ayrıntılar sağlar.</span><span class="sxs-lookup"><span data-stu-id="22812-105">This topic provides some details on the order of events during several important stages in the lifetime of applications and controls.</span></span> <span data-ttu-id="22812-106">Fare giriş olayların sırası hakkında belirli Ayrıntılar için bkz: [Windows Forms'ta fare olayları](../../../docs/framework/winforms/mouse-events-in-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="22812-106">For specific details about the order of mouse input events, see [Mouse Events in Windows Forms](../../../docs/framework/winforms/mouse-events-in-windows-forms.md).</span></span> <span data-ttu-id="22812-107">Windows Forms'ta olayların genel bakış için bkz: [olaylara genel bakış](../../../docs/framework/winforms/events-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="22812-107">For an overview of events in Windows Forms, see [Events Overview](../../../docs/framework/winforms/events-overview-windows-forms.md).</span></span> <span data-ttu-id="22812-108">Olay işleyicileri yapısıyla hakkında daha fazla ayrıntı için bkz: [olay işleyicilerine genel bakış](../../../docs/framework/winforms/event-handlers-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="22812-108">For details about the makeup of event handlers, see [Event Handlers Overview](../../../docs/framework/winforms/event-handlers-overview-windows-forms.md).</span></span>  
  
## <a name="application-startup-and-shutdown-events"></a><span data-ttu-id="22812-109">Uygulama başlatma ve kapatma olayları</span><span class="sxs-lookup"><span data-stu-id="22812-109">Application Startup and Shutdown Events</span></span>  
 <span data-ttu-id="22812-110"><xref:System.Windows.Forms.Form> Ve <xref:System.Windows.Forms.Control> sınıfları bir dizi uygulama başlatma ve kapatma ilgili olayları gösterir.</span><span class="sxs-lookup"><span data-stu-id="22812-110">The <xref:System.Windows.Forms.Form> and <xref:System.Windows.Forms.Control> classes expose a set of events related to application startup and shutdown.</span></span> <span data-ttu-id="22812-111">Bir Windows Forms uygulaması başlatıldığında, ana formun başlangıç olaylar aşağıdaki sırayla oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="22812-111">When a Windows Forms application starts, the startup events of the main form are raised in the following order:</span></span>  
  
-   <xref:System.Windows.Forms.Control.HandleCreated?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Control.BindingContextChanged?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.Load?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Control.VisibleChanged?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.Activated?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.Shown?displayProperty=nameWithType>  
  
 <span data-ttu-id="22812-112">Bir uygulama kapandığında ana formun kapatma olayları aşağıdaki sırayla oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="22812-112">When an application closes, the shutdown events of the main form are raised in the following order:</span></span>  
  
-   <xref:System.Windows.Forms.Form.Closing?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.FormClosing?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.Closed?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.FormClosed?displayProperty=nameWithType>  
  
-   <xref:System.Windows.Forms.Form.Deactivate?displayProperty=nameWithType>  
  
 <span data-ttu-id="22812-113"><xref:System.Windows.Forms.Application.ApplicationExit> Olayı <xref:System.Windows.Forms.Application> sınıfı, ana formu kapatma olayları sonra oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="22812-113">The <xref:System.Windows.Forms.Application.ApplicationExit> event of the <xref:System.Windows.Forms.Application> class is raised after the shutdown events of the main form.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="22812-114">Visual Basic 2005 içeren ek uygulama olayları gibi <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup?displayProperty=nameWithType> ve <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="22812-114">Visual Basic 2005 includes additional application events, such as <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Startup?displayProperty=nameWithType> and <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.Shutdown?displayProperty=nameWithType>.</span></span>  
  
## <a name="focus-and-validation-events"></a><span data-ttu-id="22812-115">Odak ve doğrulama olayları</span><span class="sxs-lookup"><span data-stu-id="22812-115">Focus and Validation Events</span></span>  
 <span data-ttu-id="22812-116">Çağırarak (SEKMESİ, üst karakter + sekme ve benzeri) klavyeyi kullanarak odağı değiştirdiğinizde <xref:System.Windows.Forms.Control.Select%2A> veya <xref:System.Windows.Forms.Control.SelectNextControl%2A> yöntemleri veya ayarlayarak <xref:System.Windows.Forms.ContainerControl.ActiveControl%2A> geçerli formun, odak olayları özelliğine <xref:System.Windows.Forms.Control> sınıfı ortaya aşağıdaki sırayla :</span><span class="sxs-lookup"><span data-stu-id="22812-116">When you change the focus by using the keyboard (TAB, SHIFT+TAB, and so on), by calling the <xref:System.Windows.Forms.Control.Select%2A> or <xref:System.Windows.Forms.Control.SelectNextControl%2A> methods, or by setting the <xref:System.Windows.Forms.ContainerControl.ActiveControl%2A> property to the current form, focus events of the <xref:System.Windows.Forms.Control> class occur in the following order:</span></span>  
  
-   <xref:System.Windows.Forms.Control.Enter>  
  
-   <xref:System.Windows.Forms.Control.GotFocus>  
  
-   <xref:System.Windows.Forms.Control.Leave>  
  
-   <xref:System.Windows.Forms.Control.Validating>  
  
-   <xref:System.Windows.Forms.Control.Validated>  
  
-   <xref:System.Windows.Forms.Control.LostFocus>  
  
 <span data-ttu-id="22812-117">Değiştirdiğinizde odağı fare kullanarak veya çağırarak <xref:System.Windows.Forms.Control.Focus%2A> yöntemi, odak olayları <xref:System.Windows.Forms.Control> sınıfı aşağıdaki sırayla oluşur:</span><span class="sxs-lookup"><span data-stu-id="22812-117">When you change the focus by using the mouse or by calling the <xref:System.Windows.Forms.Control.Focus%2A> method, focus events of the <xref:System.Windows.Forms.Control> class occur in the following order:</span></span>  
  
-   <xref:System.Windows.Forms.Control.Enter>  
  
-   <xref:System.Windows.Forms.Control.GotFocus>  
  
-   <xref:System.Windows.Forms.Control.LostFocus>  
  
-   <xref:System.Windows.Forms.Control.Leave>  
  
-   <xref:System.Windows.Forms.Control.Validating>  
  
-   <xref:System.Windows.Forms.Control.Validated>  
  
## <a name="see-also"></a><span data-ttu-id="22812-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="22812-118">See Also</span></span>  
 [<span data-ttu-id="22812-119">Windows Forms'ta Olay İşleyicileri Oluşturma</span><span class="sxs-lookup"><span data-stu-id="22812-119">Creating Event Handlers in Windows Forms</span></span>](../../../docs/framework/winforms/creating-event-handlers-in-windows-forms.md)
