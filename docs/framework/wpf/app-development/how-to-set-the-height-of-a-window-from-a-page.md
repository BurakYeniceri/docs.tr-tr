---
title: "Nasıl yapılır: bir sayfadan bir pencere yüksekliğini ayarlama"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- windows [WPF], setting height from a page
- pages [WPF], setting window height from
- height of window [WPF], setting from a page
ms.assetid: 4e4488ff-ab5c-4ee9-81a4-e1addb55c5cc
caps.latest.revision: "4"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 002e75542c1dbbe1cfaa122898801dd5babf054f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-set-the-height-of-a-window-from-a-page"></a>Nasıl yapılır: bir sayfadan bir pencere yüksekliğini ayarlama
Bu örnek penceresinden yüksekliğinin nasıl ayarlanacağını gösterir bir <xref:System.Windows.Controls.Page>.  
  
## <a name="example"></a>Örnek  
 A <xref:System.Windows.Controls.Page> ayarlayarak ana penceresinin yüksekliğini belirleyebilir <xref:System.Windows.Controls.Page.WindowHeight%2A>. Bu özellik tanır <xref:System.Windows.Controls.Page> , onu barındıran pencere türünün açık bilgisine sahip değil.  
  
> [!NOTE]
>  Kullanarak bir pencerenin yüksekliğini ayarlamak için <xref:System.Windows.Controls.Page.WindowHeight%2A>, <xref:System.Windows.Controls.Page> pencerenin alt öğesi olması gerekir.  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowHeightXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowHeightPage.xaml#setpagewindowheightxaml)]
