---
title: "Nasıl yapılır: Sistem Yazı Tiplerini Numaralandırma"
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
- typography [WPF], enumerating system fonts
- fonts [WPF], enumerating
- system fonts [WPF], enumerating
- enumerating [WPF], system fonts
ms.assetid: 36e37791-55b9-4f01-a496-5cc10335e6a6
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: cf917dc2af256cdd0f3a0c579f86847e1bf4f1e5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-enumerate-system-fonts"></a><span data-ttu-id="d37bb-102">Nasıl yapılır: Sistem Yazı Tiplerini Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="d37bb-102">How to: Enumerate System Fonts</span></span>
## <a name="example"></a><span data-ttu-id="d37bb-103">Örnek</span><span class="sxs-lookup"><span data-stu-id="d37bb-103">Example</span></span>  
 <span data-ttu-id="d37bb-104">Aşağıdaki örnek, sistem yazı tipi koleksiyonu yazı tiplerini numaralandırma gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d37bb-104">The following example shows how to enumerate the fonts in the system font collection.</span></span> <span data-ttu-id="d37bb-105">Yazı tipi ailesinin adı her <xref:System.Windows.Media.FontFamily> içinde <xref:System.Windows.Media.Fonts.SystemFontFamilies%2A> birleşik giriş kutusu için bir öğe olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="d37bb-105">The font family name of each <xref:System.Windows.Media.FontFamily> within <xref:System.Windows.Media.Fonts.SystemFontFamilies%2A> is added as an item to a combo box.</span></span>  
  
 [!code-csharp[TextOverview#100](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextOverview/CSharp/Window1.xaml.cs#100)]
 [!code-vb[TextOverview#100](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/TextOverview/visualbasic/window1.xaml.vb#100)]  
  
 <span data-ttu-id="d37bb-106">Yazı tipi ailesini birden fazla sürümünü aynı dizinde bulunuyorsa [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] yazı tipi numaralandırması yazı en son sürümünü döndürür.</span><span class="sxs-lookup"><span data-stu-id="d37bb-106">If multiple versions of the same font family reside in the same directory, the [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] font enumeration returns the most recent version of the font.</span></span> <span data-ttu-id="d37bb-107">Sürüm bilgileri çözümleme sağlamıyorsa son zaman damgalı yazı tipi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="d37bb-107">If the version information does not provide resolution, the font with latest timestamp is returned.</span></span> <span data-ttu-id="d37bb-108">Zaman damgası bilgileri eşdeğer ise alfabetik sıraya göre ilk yazı tipi dosyası döndürülür.</span><span class="sxs-lookup"><span data-stu-id="d37bb-108">If the timestamp information is equivalent, the font file that is first in alphabetical order is returned.</span></span>
