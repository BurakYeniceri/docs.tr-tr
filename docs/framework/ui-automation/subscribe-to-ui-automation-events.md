---
title: UI Otomasyon Olaylarına Abone Olma
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, subscribing to events
- subscribing to UI Automation events
- events, subscribing to
- listening for events
ms.assetid: b688effa-b3e8-4b05-944d-05ed89a245aa
author: Xansky
ms.author: mhopkins
ms.openlocfilehash: 9f2a48066356d594a3aeaa003089053297bf4ff8
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47171770"
---
# <a name="subscribe-to-ui-automation-events"></a>UI Otomasyon Olaylarına Abone Olma
> [!NOTE]
>  Bu belge yönetilen kullanmak isteyen .NET Framework için tasarlanan [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] tanımlanan sınıflar <xref:System.Windows.Automation> ad alanı. En son bilgileri [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], bkz: [Windows Automation API: UI Otomasyonu](https://go.microsoft.com/fwlink/?LinkID=156746).  
  
 Bu konuda, UI Otomasyon sağlayıcıları tarafından oluşturulan olaylara abone olunacağı gösterilmektedir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, bir düğme gibi bir denetim çağrılır ve formunu kapandığında kaldırır, olayı için olay işleyicisi kaydeder. Olay tarafından tanımlanan bir <xref:System.Windows.Automation.AutomationEvent> bir parametre olarak geçirilen <xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>.  
  
 [!code-csharp[UIAClient_snip#101](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#101)]
 [!code-vb[UIAClient_snip#101](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#101)]  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek nasıl kullanılacağını gösterir [!INCLUDE[TLA#tla_uiautomation](../../../includes/tlasharptla-uiautomation-md.md)] odak her değiştiğinde başlatan bir olaya abone olmak için. Olay işleyicisi, uygulamayı kapatma veya kullanıcı Arabirimi olaylarının bildirim artık gerekli olmadığında çağrılabilen bir yöntem'kaydı silindi.  
  
 [!code-csharp[UIAClient_snip#102](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClient_snip/CSharp/ClientForm.cs#102)]
 [!code-vb[UIAClient_snip#102](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClient_snip/VisualBasic/ClientForm.vb#102)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Automation.Automation.AddAutomationEventHandler%2A>  
 <xref:System.Windows.Automation.Automation.RemoveAllEventHandlers%2A>  
 <xref:System.Windows.Automation.Automation.RemoveAutomationEventHandler%2A>  
 [UI Otomasyonu Olaylarına Genel Bakış](../../../docs/framework/ui-automation/ui-automation-events-overview.md)
