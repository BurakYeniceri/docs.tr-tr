---
title: "Nasıl yapılır: Özel Gönderilmiş Olay Oluşturma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- routed events [WPF], creating
- events [WPF], routing
ms.assetid: b79f459a-1c3f-4045-b2d4-1659cc8eaa3c
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: ecd335cb08056cb8b7c696555d666f54cad81b87
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-create-a-custom-routed-event"></a><span data-ttu-id="5b0d0-102">Nasıl yapılır: Özel Gönderilmiş Olay Oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b0d0-102">How to: Create a Custom Routed Event</span></span>
<span data-ttu-id="5b0d0-103">Olay yönlendirme desteklemek kendi özel olayınız için kaydetmeniz gerekir. bir <xref:System.Windows.RoutedEvent> kullanarak <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-103">For your custom event to support event routing, you need to register a <xref:System.Windows.RoutedEvent> using the <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> method.</span></span> <span data-ttu-id="5b0d0-104">Bu örnek özel yönlendirilmiş olay oluşturma temelleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-104">This example demonstrates the basics of creating a custom routed event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5b0d0-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="5b0d0-105">Example</span></span>  
 <span data-ttu-id="5b0d0-106">Aşağıdaki örnekte gösterildiği gibi önce kaydetmeniz bir <xref:System.Windows.RoutedEvent> kullanarak <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-106">As shown in the following example, you first register a <xref:System.Windows.RoutedEvent> using the <xref:System.Windows.EventManager.RegisterRoutedEvent%2A> method.</span></span> <span data-ttu-id="5b0d0-107">Kural tarafından <xref:System.Windows.RoutedEvent> statik alan adı son eki ile bitmelidir ***olay***.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-107">By convention, the <xref:System.Windows.RoutedEvent> static field name should end with the suffix ***Event***.</span></span> <span data-ttu-id="5b0d0-108">Bu örnekte, olay adıdır `Tap` ve olayın yönlendirme stratejisi <xref:System.Windows.RoutingStrategy.Bubble>.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-108">In this example, the name of the event is `Tap` and the routing strategy of the event is <xref:System.Windows.RoutingStrategy.Bubble>.</span></span> <span data-ttu-id="5b0d0-109">Kayıt çağrısından sonra Ekle ve Kaldır sağlayabilirsiniz [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] olayı için olay erişimcileri.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-109">After the registration call, you can provide add-and-remove [!INCLUDE[TLA#tla_clr](../../../../includes/tlasharptla-clr-md.md)] event accessors for the event.</span></span>  
  
 <span data-ttu-id="5b0d0-110">Aracılığıyla olayı olsa bile unutmayın `OnTap` söz konusu örnekte, nasıl olayınızın yükseltmek veya olayınızın değişiklikleri nasıl yanıt verdiği sanal yöntemi gereksinimlerinize göre değişir.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-110">Note that even though the event is raised through the `OnTap` virtual method in this particular example, how you raise your event or how your event responds to changes depends on your needs.</span></span>  
  
 <span data-ttu-id="5b0d0-111">Ayrıca bu örnek temel olarak, tüm bir alt uyguladığını unutmayın <xref:System.Windows.Controls.Button>; o alt sınıf ayrı bir derleme yerleşik ve özel bir sınıf ayrı olarak örneği [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] sayfası.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-111">Note also that this example basically implements an entire subclass of <xref:System.Windows.Controls.Button>; that subclass is built as a separate assembly and then instantiated as a custom class on a separate [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] page.</span></span> <span data-ttu-id="5b0d0-112">Altsınıflanmış denetimler diğer denetimlerden oluşan ağaçlara eklenebilir ve bu durumda, çok aynı olay Yönlendirme yetenekleri bu denetimlerinde özel olaylar olarak herhangi bir yerel sahip kavramı göstermeye budur [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] öğesi.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-112">This is to illustrate the concept that subclassed controls can be inserted into trees composed of other controls, and that in this situation, custom events on these controls have the very same event routing capabilities as any native [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] element does.</span></span>  
  
 [!code-csharp[RoutedEventCustom#CustomClass](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventCustom/CSharp/SDKSampleLibrary/class1.cs#customclass)]
 [!code-vb[RoutedEventCustom#CustomClass](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventCustom/VB/SDKSampleLibrary/Class1.vb#customclass)]  
  
 [!code-xaml[RoutedEventCustom#Page](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventCustom/CSharp/RoutedEventCustomApp/default.xaml#page)]  
  
 <span data-ttu-id="5b0d0-113">Tünel olayları oluşturulur aynı yolla ancak ile <xref:System.Windows.RoutedEvent.RoutingStrategy%2A> kümesine <xref:System.Windows.RoutingStrategy.Tunnel> kayıt çağrısında.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-113">Tunneling events are created the same way, but with <xref:System.Windows.RoutedEvent.RoutingStrategy%2A> set to <xref:System.Windows.RoutingStrategy.Tunnel> in the registration call.</span></span> <span data-ttu-id="5b0d0-114">Kurala göre olaylar tünel [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] "Önizleme" sözcüğüyle öneki.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-114">By convention, tunneling events in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] are prefixed with the word "Preview".</span></span>  
  
 <span data-ttu-id="5b0d0-115">Nasıl kabarcıklanma olayları çalışma örneği görmek için bkz: [yönlendirilmiş olayını işle](../../../../docs/framework/wpf/advanced/how-to-handle-a-routed-event.md).</span><span class="sxs-lookup"><span data-stu-id="5b0d0-115">To see an example of how bubbling events work, see [Handle a Routed Event](../../../../docs/framework/wpf/advanced/how-to-handle-a-routed-event.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b0d0-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5b0d0-116">See Also</span></span>  
 [<span data-ttu-id="5b0d0-117">Yönlendirilmiş Olaylara Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5b0d0-117">Routed Events Overview</span></span>](../../../../docs/framework/wpf/advanced/routed-events-overview.md)  
 [<span data-ttu-id="5b0d0-118">Girişe Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5b0d0-118">Input Overview</span></span>](../../../../docs/framework/wpf/advanced/input-overview.md)  
 [<span data-ttu-id="5b0d0-119">Denetim Yazımına Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="5b0d0-119">Control Authoring Overview</span></span>](../../../../docs/framework/wpf/controls/control-authoring-overview.md)
