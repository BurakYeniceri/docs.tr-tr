---
title: "TreeItem Denetim Türü için UI Otomasyon Desteği"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-bcl
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- control types, Tree Item
- Tree Item control type
- UI Automation, Tree Item control type
ms.assetid: 229f341a-477f-434e-b877-4db9973068eb
caps.latest.revision: "22"
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: 779774d38c7c57b602e5d30717af21a1281daaa7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ui-automation-support-for-the-treeitem-control-type"></a><span data-ttu-id="a84af-102">TreeItem Denetim Türü için UI Otomasyon Desteği</span><span class="sxs-lookup"><span data-stu-id="a84af-102">UI Automation Support for the TreeItem Control Type</span></span>
> [!NOTE]
>  <span data-ttu-id="a84af-103">Bu belge yönetilen kullanmak isteyen .NET Framework için tasarlanan [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tanımlanan sınıflar <xref:System.Windows.Automation> ad alanı.</span><span class="sxs-lookup"><span data-stu-id="a84af-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="a84af-104">Hakkında en yeni bilgiler için [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], bkz: [Windows Otomasyon API: UI Otomasyonu](http://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="a84af-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](http://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="a84af-105">Bu konu hakkında bilgi sağlar. [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] Treeıtem denetim türü için destek.</span><span class="sxs-lookup"><span data-stu-id="a84af-105">This topic provides information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] support for the TreeItem control type.</span></span> <span data-ttu-id="a84af-106">İçinde [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], Denetim türü bir denetimi kullanmak için karşılaması gereken koşulları kümesidir <xref:System.Windows.Automation.AutomationElement.ControlTypeProperty> özelliği.</span><span class="sxs-lookup"><span data-stu-id="a84af-106">In [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], a control type is a set of conditions that a control must meet in order to use the <xref:System.Windows.Automation.AutomationElement.ControlTypeProperty> property.</span></span> <span data-ttu-id="a84af-107">Koşullar özel yönergeleri dahil [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağaç yapısı, [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] özellik değerlerini ve denetim düzenleri.</span><span class="sxs-lookup"><span data-stu-id="a84af-107">The conditions include specific guidelines for [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree structure, [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] property values and control patterns.</span></span>  
  
 <span data-ttu-id="a84af-108">Treeıtem denetim türü bir ağaç kapsayıcı içindeki bir düğümü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a84af-108">The TreeItem control type represents a node within a tree container.</span></span> <span data-ttu-id="a84af-109">Her düğümün alt düğümleri olarak adlandırılan, diğer düğümler içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a84af-109">Each node might contain other nodes, called child nodes.</span></span> <span data-ttu-id="a84af-110">Üst düğüm ya da alt düğümleri içeren düğümleri görüntülenebilir genişletilmiş olarak veya daraltılmış.</span><span class="sxs-lookup"><span data-stu-id="a84af-110">Parent nodes, or nodes that contain child nodes, can be displayed as expanded or collapsed.</span></span>  
  
 <span data-ttu-id="a84af-111">Aşağıdaki bölümlerde gerekli tanımlamak [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağaç yapısı, özellikleri, Denetim desenleri ve olayları Treeıtem denetim türü için.</span><span class="sxs-lookup"><span data-stu-id="a84af-111">The following sections define the required [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree structure, properties, control patterns, and events for the TreeItem control type.</span></span> <span data-ttu-id="a84af-112">[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] Gereksinimleri tüm ağaç öğesi denetimleri için geçerli olup olmadığını [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)], veya [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)].</span><span class="sxs-lookup"><span data-stu-id="a84af-112">The [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] requirements apply to all tree item controls, whether [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)], [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)], or [!INCLUDE[TLA#tla_winforms](../../../includes/tlasharptla-winforms-md.md)].</span></span>  
  
<a name="Required_UI_Automation_Tree_Structure"></a>   
## <a name="required-ui-automation-tree-structure"></a><span data-ttu-id="a84af-113">Gerekli UI Otomasyon ağaç yapısı</span><span class="sxs-lookup"><span data-stu-id="a84af-113">Required UI Automation Tree Structure</span></span>  
 <span data-ttu-id="a84af-114">Denetim Görünüm ve içerik görünümünü aşağıdaki tabloda gösterilmektedir [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağaç öğesine ilgilidir ağaç denetler ve her bir görünümde bulunabilir açıklar.</span><span class="sxs-lookup"><span data-stu-id="a84af-114">The following table depicts the control view and the content view of the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree that pertains to tree item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a84af-115">Daha fazla bilgi için [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağaç bkz [UI Otomasyon ağacına genel bakış](../../../docs/framework/ui-automation/ui-automation-tree-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a84af-115">For more information on the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree, see [UI Automation Tree Overview](../../../docs/framework/ui-automation/ui-automation-tree-overview.md).</span></span>  
  
|<span data-ttu-id="a84af-116">Denetim Görünüm</span><span class="sxs-lookup"><span data-stu-id="a84af-116">Control View</span></span>|<span data-ttu-id="a84af-117">İçerik görünümü</span><span class="sxs-lookup"><span data-stu-id="a84af-117">Content View</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="a84af-118">Treeıtem</span><span class="sxs-lookup"><span data-stu-id="a84af-118">TreeItem</span></span><br /><br /> <span data-ttu-id="a84af-119">-Onay kutusu (0 veya 1)</span><span class="sxs-lookup"><span data-stu-id="a84af-119">-   CheckBox (0 or 1)</span></span><br /><span data-ttu-id="a84af-120">-İmage (0 veya 1)</span><span class="sxs-lookup"><span data-stu-id="a84af-120">-   Image (0 or 1)</span></span><br /><span data-ttu-id="a84af-121">-Düğmesi (0 veya 1)</span><span class="sxs-lookup"><span data-stu-id="a84af-121">-   Button (0 or 1)</span></span><br /><span data-ttu-id="a84af-122">-Treeıtem (0 veya daha fazla)</span><span class="sxs-lookup"><span data-stu-id="a84af-122">-   TreeItem (0 or more)</span></span>|<span data-ttu-id="a84af-123">Treeıtem</span><span class="sxs-lookup"><span data-stu-id="a84af-123">TreeItem</span></span><br /><br /> <span data-ttu-id="a84af-124">-Treeıtem (0 veya daha fazla)</span><span class="sxs-lookup"><span data-stu-id="a84af-124">-   TreeItem (0 or more)</span></span>|  
  
 <span data-ttu-id="a84af-125">Ağaç öğesi denetimlerini içerik görünümünde sıfır veya daha fazla ağaç öğesi alt olabilir [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağacı.</span><span class="sxs-lookup"><span data-stu-id="a84af-125">Tree item controls can have zero or more tree item children in the content view of the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree.</span></span> <span data-ttu-id="a84af-126">Ağaç öğesi denetim varsa işlevselliği denetim düzenleri kullanıma sunulan ötesine aşağıda listelenen sonra denetimi veri öğesi denetim türüne göre.</span><span class="sxs-lookup"><span data-stu-id="a84af-126">If the tree item control has functionality beyond what is exposed in the control patterns listed below, then the control should be based on the Data Item control type.</span></span>  
  
 <span data-ttu-id="a84af-127">Bunlar genişletilmiş ve görünür hale (veya görünüme kaydırılabileceğini kadar) daraltılmış ağaç öğeleri denetim veya içerik görünümünde görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="a84af-127">Collapsed tree items will not display in the control view or content view until they become expanded and visible (or, can be scrolled into view).</span></span>  
  
 <span data-ttu-id="a84af-128">Denetim görünüm ilişkili bir görüntü veya düğmesi de dahil olmak üzere bir denetim için ek ayrıntılar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a84af-128">The control view can contain additional details for a control, including an associated image or a button.</span></span> <span data-ttu-id="a84af-129">Örneğin, bir anahat görünümde bir öğe genişletmek veya anahattı daraltmak için bir düğmeye yanı sıra bir görüntü içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a84af-129">For example, an item in an outline view might contain an image as well as a button to expand or collapse the outline.</span></span> <span data-ttu-id="a84af-130">Bilgileri zaten üst ağaç öğesi tarafından temsil edilen çünkü bu ayrıntı nesneleri içerik görünümünde görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="a84af-130">These detail objects don't appear in the content view because the information is already represented by the parent tree item.</span></span> <span data-ttu-id="a84af-131">Ekranı kaydırılan ağaç öğeleri, Denetim ve içerik görünümlerinde görünür [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağacı ve olmalıdır <xref:System.Windows.Automation.AutomationElement.IsOffscreenProperty> true olarak ayarlanmış.</span><span class="sxs-lookup"><span data-stu-id="a84af-131">Tree items that are scrolled off the screen will appear in both the control and content views of the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree and should have the <xref:System.Windows.Automation.AutomationElement.IsOffscreenProperty> set to true.</span></span>  
  
<a name="Required_UI_Automation_Properties"></a>   
## <a name="required-ui-automation-properties"></a><span data-ttu-id="a84af-132">Gerekli UI Otomasyon özellikleri</span><span class="sxs-lookup"><span data-stu-id="a84af-132">Required UI Automation Properties</span></span>  
 <span data-ttu-id="a84af-133">Aşağıdaki tabloda [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] , değer veya tanımı liste denetimleri için özellikle ilgili özellikler.</span><span class="sxs-lookup"><span data-stu-id="a84af-133">The following table lists the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] properties whose value or definition is especially relevant to list controls.</span></span> <span data-ttu-id="a84af-134">Daha fazla bilgi için [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] özellikleri, görmek [istemciler için UI Otomasyon özellikleri](../../../docs/framework/ui-automation/ui-automation-properties-for-clients.md).</span><span class="sxs-lookup"><span data-stu-id="a84af-134">For more information on [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] properties, see [UI Automation Properties for Clients](../../../docs/framework/ui-automation/ui-automation-properties-for-clients.md).</span></span>  
  
|[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]<span data-ttu-id="a84af-135">Özelliği</span><span class="sxs-lookup"><span data-stu-id="a84af-135"> Property</span></span>|<span data-ttu-id="a84af-136">Değer</span><span class="sxs-lookup"><span data-stu-id="a84af-136">Value</span></span>|<span data-ttu-id="a84af-137">Notlar</span><span class="sxs-lookup"><span data-stu-id="a84af-137">Notes</span></span>|  
|------------------------------------------------------------------------------------|-----------|-----------|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.AutomationIdProperty>|<span data-ttu-id="a84af-138">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-138">See notes.</span></span>|<span data-ttu-id="a84af-139">Bu özelliğin değeri bir uygulamadaki tüm denetimler arasında benzersiz olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a84af-139">The value of this property needs to be unique across all controls in an application.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.BoundingRectangleProperty>|<span data-ttu-id="a84af-140">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-140">See notes.</span></span>|<span data-ttu-id="a84af-141">Tam denetimi içeren en dıştaki dikdörtgen.</span><span class="sxs-lookup"><span data-stu-id="a84af-141">The outermost rectangle that contains the whole control.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.ClickablePointProperty>|<span data-ttu-id="a84af-142">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-142">See notes.</span></span>|<span data-ttu-id="a84af-143">Bu özellik seçimi durumunun değişmesine veya odaklanmış olur öğesi neden olur öğenin konumunu döndürmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a84af-143">This property must return a location of the item that will cause the item to change selection state or become focused.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.ControlTypeProperty>|<span data-ttu-id="a84af-144">Treeıtem</span><span class="sxs-lookup"><span data-stu-id="a84af-144">TreeItem</span></span>|<span data-ttu-id="a84af-145">Bu değer tüm UI çerçeveler için aynıdır.</span><span class="sxs-lookup"><span data-stu-id="a84af-145">This value is the same for all UI frameworks.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.IsContentElementProperty>|<span data-ttu-id="a84af-146">Doğru</span><span class="sxs-lookup"><span data-stu-id="a84af-146">True</span></span>|<span data-ttu-id="a84af-147">Liste denetimi her zaman içerik görünümünde dahil [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağacı.</span><span class="sxs-lookup"><span data-stu-id="a84af-147">The list control is always included in the content view of the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.IsControlElementProperty>|<span data-ttu-id="a84af-148">Doğru</span><span class="sxs-lookup"><span data-stu-id="a84af-148">True</span></span>|<span data-ttu-id="a84af-149">Liste denetimi her zaman denetim görünümünde dahil [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] ağacı.</span><span class="sxs-lookup"><span data-stu-id="a84af-149">The list control is always included in the control view of the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tree.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.IsOffscreenProperty>|<span data-ttu-id="a84af-150">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-150">See notes.</span></span>|<span data-ttu-id="a84af-151">Ağaç öğesi denetim ekranı zaman kaydırılan belirtmek için bu özelliği ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a84af-151">This property is set to indicate when a tree item control is scrolled off the screen.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.IsKeyboardFocusableProperty>|<span data-ttu-id="a84af-152">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-152">See notes.</span></span>|<span data-ttu-id="a84af-153">Klavye odağı denetimi alamıyorsa, bu özelliği desteklemelidir.</span><span class="sxs-lookup"><span data-stu-id="a84af-153">If the control can receive keyboard focus, it must support this property.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.ItemTypeProperty>|<span data-ttu-id="a84af-154">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-154">See notes.</span></span>|<span data-ttu-id="a84af-155">Ağaç öğesi denetim, belirli bir nesne türü olduğunu göstermek için görsel bir simge kullanıyorsa, bu özellik desteklenmesi gerekir ve nesne belirtmek.</span><span class="sxs-lookup"><span data-stu-id="a84af-155">If the tree item control uses a visual icon to indicate that is a particular type of object, then this property must be supported and indicate what the object is.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.LabeledByProperty>|`Null`|<span data-ttu-id="a84af-156">Ağaç öğesi kendi kendine etiketleme denetimleridir.</span><span class="sxs-lookup"><span data-stu-id="a84af-156">Tree item controls are self-labeling.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.LocalizedControlTypeProperty>|<span data-ttu-id="a84af-157">"ağaç öğesi"</span><span class="sxs-lookup"><span data-stu-id="a84af-157">"tree item"</span></span>|<span data-ttu-id="a84af-158">Treeıtem denetim türü için karşılık gelen yerelleştirilmiş dize.</span><span class="sxs-lookup"><span data-stu-id="a84af-158">Localized string corresponding to the TreeItem control type.</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.NameProperty>|<span data-ttu-id="a84af-159">Notlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="a84af-159">See notes.</span></span>|<span data-ttu-id="a84af-160">Bu özellik her ağaç öğesi denetim için görüntülenen metin kullanıma sunar.</span><span class="sxs-lookup"><span data-stu-id="a84af-160">This property exposes the text displayed for each tree item control.</span></span>|  
  
<a name="Required_UI_Automation_Control_Patterns"></a>   
## <a name="required-ui-automation-control-patterns"></a><span data-ttu-id="a84af-161">Gerekli UI Otomasyon denetim düzenleri</span><span class="sxs-lookup"><span data-stu-id="a84af-161">Required UI Automation Control Patterns</span></span>  
 <span data-ttu-id="a84af-162">Aşağıdaki tabloda [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] denetim düzenleri liste denetimleri tarafından desteklenmesi için gerekli.</span><span class="sxs-lookup"><span data-stu-id="a84af-162">The following table lists the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] control patterns required to be supported by list controls.</span></span> <span data-ttu-id="a84af-163">Denetim desenleri hakkında daha fazla bilgi için bkz: [UI Otomasyon denetim düzenlerine genel bakış](../../../docs/framework/ui-automation/ui-automation-control-patterns-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a84af-163">For more information on control patterns, see [UI Automation Control Patterns Overview](../../../docs/framework/ui-automation/ui-automation-control-patterns-overview.md).</span></span>  
  
|<span data-ttu-id="a84af-164">Denetim düzeni/deseni özelliği</span><span class="sxs-lookup"><span data-stu-id="a84af-164">Control Pattern/Pattern Property</span></span>|<span data-ttu-id="a84af-165">Destek/değer</span><span class="sxs-lookup"><span data-stu-id="a84af-165">Support/Value</span></span>|<span data-ttu-id="a84af-166">Notlar</span><span class="sxs-lookup"><span data-stu-id="a84af-166">Notes</span></span>|  
|---------------------------------------|--------------------|-----------|  
|<xref:System.Windows.Automation.Provider.IInvokeProvider>|<span data-ttu-id="a84af-167">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-167">Depends</span></span>|<span data-ttu-id="a84af-168">Ağaç öğesi ayrı, işlem yapılabilir komut varsa, bu denetim deseni uygular.</span><span class="sxs-lookup"><span data-stu-id="a84af-168">Implement this control pattern if the tree item has a separate, actionable command.</span></span>|  
|<xref:System.Windows.Automation.Provider.IExpandCollapseProvider>|<span data-ttu-id="a84af-169">Evet</span><span class="sxs-lookup"><span data-stu-id="a84af-169">Yes</span></span>|<span data-ttu-id="a84af-170">Tüm öğeleri ağacı genişletilmiş veya daraltılmış.</span><span class="sxs-lookup"><span data-stu-id="a84af-170">All tree items can be expanded or collapsed.</span></span>|  
|<xref:System.Windows.Automation.Provider.IExpandCollapseProvider.ExpandCollapseState%2A>|<span data-ttu-id="a84af-171">Genişletilmiş daraltılmış veya yaprak düğümü</span><span class="sxs-lookup"><span data-stu-id="a84af-171">Expanded, Collapsed, or Leaf Node</span></span>|<span data-ttu-id="a84af-172">Bunlar genişletilmiş daraltılmış veya ağaç öğeleri yaprak düğümlerin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a84af-172">Tree items will be leaf nodes when they are not expanded or collapsed.</span></span>|  
|<xref:System.Windows.Automation.Provider.IScrollItemProvider>|<span data-ttu-id="a84af-173">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-173">Depends</span></span>|<span data-ttu-id="a84af-174">Kaydırma denetim düzenini ağaç kapsayıcı destekliyorsa, bu denetim deseni uygular.</span><span class="sxs-lookup"><span data-stu-id="a84af-174">Implement this control pattern if the tree container supports the Scroll control pattern.</span></span>|  
|<xref:System.Windows.Automation.Provider.ISelectionItemProvider>|<span data-ttu-id="a84af-175">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-175">Depends</span></span>|<span data-ttu-id="a84af-176">Kullanıcı ağaç kapsayıcıya döndüğünde korunur etkin bir seçim olması mümkündür, bu denetim deseni uygular.</span><span class="sxs-lookup"><span data-stu-id="a84af-176">Implement this control pattern if it is possible to have an active selection that is maintained when the user returns to the tree container.</span></span>|  
|<xref:System.Windows.Automation.Provider.ISelectionItemProvider.SelectionContainer%2A>|<span data-ttu-id="a84af-177">Evet</span><span class="sxs-lookup"><span data-stu-id="a84af-177">Yes</span></span>|<span data-ttu-id="a84af-178">Bu özellik kapsayıcıdaki tüm öğeler için aynı kapsayıcı açığa çıkarır.</span><span class="sxs-lookup"><span data-stu-id="a84af-178">This property will expose the same container for all items within the container.</span></span>|  
|<xref:System.Windows.Automation.Provider.IToggleProvider>|<span data-ttu-id="a84af-179">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-179">Depends</span></span>|<span data-ttu-id="a84af-180">Ağaç öğesi ilişkili bir onay kutusu varsa, bu denetim deseni uygular.</span><span class="sxs-lookup"><span data-stu-id="a84af-180">Implement this control pattern if the tree item has an associated check box.</span></span>|  
  
<a name="Required_UI_Automation_Events"></a>   
## <a name="required-ui-automation-events"></a><span data-ttu-id="a84af-181">Gerekli UI Otomasyon olayları</span><span class="sxs-lookup"><span data-stu-id="a84af-181">Required UI Automation Events</span></span>  
 <span data-ttu-id="a84af-182">Aşağıdaki tabloda [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] olayları tüm ağaç öğesi denetimleri tarafından desteklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a84af-182">The following table lists the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] events required to be supported by all tree item controls.</span></span> <span data-ttu-id="a84af-183">Olaylar hakkında daha fazla bilgi için bkz: [UI Otomasyonu olaylarına genel bakış](../../../docs/framework/ui-automation/ui-automation-events-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a84af-183">For more information about events, see [UI Automation Events Overview](../../../docs/framework/ui-automation/ui-automation-events-overview.md).</span></span>  
  
|[!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]<span data-ttu-id="a84af-184">Olay</span><span class="sxs-lookup"><span data-stu-id="a84af-184"> Event</span></span>|<span data-ttu-id="a84af-185">Destek</span><span class="sxs-lookup"><span data-stu-id="a84af-185">Support</span></span>|<span data-ttu-id="a84af-186">Notlar</span><span class="sxs-lookup"><span data-stu-id="a84af-186">Notes</span></span>|  
|---------------------------------------------------------------------------------|-------------|-----------|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.AutomationFocusChangedEvent>|<span data-ttu-id="a84af-187">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-187">Required</span></span>|<span data-ttu-id="a84af-188">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-188">None</span></span>|  
|<span data-ttu-id="a84af-189"><xref:System.Windows.Automation.AutomationElementIdentifiers.BoundingRectangleProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-189"><xref:System.Windows.Automation.AutomationElementIdentifiers.BoundingRectangleProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-190">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-190">Required</span></span>|<span data-ttu-id="a84af-191">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-191">None</span></span>|  
|<span data-ttu-id="a84af-192"><xref:System.Windows.Automation.AutomationElementIdentifiers.IsEnabledProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-192"><xref:System.Windows.Automation.AutomationElementIdentifiers.IsEnabledProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-193">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-193">Required</span></span>|<span data-ttu-id="a84af-194">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-194">None</span></span>|  
|<span data-ttu-id="a84af-195"><xref:System.Windows.Automation.AutomationElementIdentifiers.IsOffscreenProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-195"><xref:System.Windows.Automation.AutomationElementIdentifiers.IsOffscreenProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-196">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-196">Required</span></span>|<span data-ttu-id="a84af-197">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-197">None</span></span>|  
|<span data-ttu-id="a84af-198"><xref:System.Windows.Automation.AutomationElementIdentifiers.ItemStatusProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-198"><xref:System.Windows.Automation.AutomationElementIdentifiers.ItemStatusProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-199">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-199">Depends</span></span>|<span data-ttu-id="a84af-200">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-200">None</span></span>|  
|<span data-ttu-id="a84af-201"><xref:System.Windows.Automation.AutomationElementIdentifiers.NameProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-201"><xref:System.Windows.Automation.AutomationElementIdentifiers.NameProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-202">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-202">Required</span></span>|<span data-ttu-id="a84af-203">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-203">None</span></span>|  
|<xref:System.Windows.Automation.AutomationElementIdentifiers.StructureChangedEvent>|<span data-ttu-id="a84af-204">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-204">Required</span></span>|<span data-ttu-id="a84af-205">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-205">None</span></span>|  
|<span data-ttu-id="a84af-206"><xref:System.Windows.Automation.ExpandCollapsePatternIdentifiers.ExpandCollapseStateProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-206"><xref:System.Windows.Automation.ExpandCollapsePatternIdentifiers.ExpandCollapseStateProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-207">Gerekli</span><span class="sxs-lookup"><span data-stu-id="a84af-207">Required</span></span>|<span data-ttu-id="a84af-208">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-208">None</span></span>|  
|<xref:System.Windows.Automation.InvokePatternIdentifiers.InvokedEvent>|<span data-ttu-id="a84af-209">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-209">Depends</span></span>|<span data-ttu-id="a84af-210">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-210">None</span></span>|  
|<span data-ttu-id="a84af-211"><xref:System.Windows.Automation.MultipleViewPatternIdentifiers.CurrentViewProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-211"><xref:System.Windows.Automation.MultipleViewPatternIdentifiers.CurrentViewProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-212">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-212">Depends</span></span>|<span data-ttu-id="a84af-213">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-213">None</span></span>|  
|<xref:System.Windows.Automation.SelectionItemPatternIdentifiers.ElementAddedToSelectionEvent>|<span data-ttu-id="a84af-214">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-214">Depends</span></span>|<span data-ttu-id="a84af-215">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-215">None</span></span>|  
|<xref:System.Windows.Automation.SelectionItemPatternIdentifiers.ElementRemovedFromSelectionEvent>|<span data-ttu-id="a84af-216">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-216">Depends</span></span>|<span data-ttu-id="a84af-217">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-217">None</span></span>|  
|<xref:System.Windows.Automation.SelectionItemPatternIdentifiers.ElementSelectedEvent>|<span data-ttu-id="a84af-218">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-218">Depends</span></span>|<span data-ttu-id="a84af-219">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-219">None</span></span>|  
|<span data-ttu-id="a84af-220"><xref:System.Windows.Automation.TogglePatternIdentifiers.ToggleStateProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-220"><xref:System.Windows.Automation.TogglePatternIdentifiers.ToggleStateProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-221">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-221">Depends</span></span>|<span data-ttu-id="a84af-222">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-222">None</span></span>|  
|<span data-ttu-id="a84af-223"><xref:System.Windows.Automation.ValuePatternIdentifiers.ValueProperty>özellik değişti olayı.</span><span class="sxs-lookup"><span data-stu-id="a84af-223"><xref:System.Windows.Automation.ValuePatternIdentifiers.ValueProperty> property-changed event.</span></span>|<span data-ttu-id="a84af-224">Bağlıdır</span><span class="sxs-lookup"><span data-stu-id="a84af-224">Depends</span></span>|<span data-ttu-id="a84af-225">Yok.</span><span class="sxs-lookup"><span data-stu-id="a84af-225">None</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="a84af-226">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a84af-226">See Also</span></span>  
 <xref:System.Windows.Automation.ControlType.TreeItem>  
 [<span data-ttu-id="a84af-227">UI Otomasyon denetim türlerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="a84af-227">UI Automation Control Types Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-control-types-overview.md)  
 [<span data-ttu-id="a84af-228">UI Otomasyon genel bakış</span><span class="sxs-lookup"><span data-stu-id="a84af-228">UI Automation Overview</span></span>](../../../docs/framework/ui-automation/ui-automation-overview.md)