---
title: "Nasıl yapılır: bir iletişim kutusu açın"
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
- opening dialog boxes [WPF]
- dialog boxes [WPF], opening
ms.assetid: 6b1557d2-da98-4ef4-9f68-4089f04ab9ea
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: d318f35f8f009f0f2c77210ca8b6b29bedfb7619
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-open-a-dialog-box"></a>Nasıl yapılır: bir iletişim kutusu açın
Bu örnek, bir iletişim kutusunu açmak gösterilmiştir.  
  
## <a name="example"></a>Örnek  
 Bir iletişim kutusu örneği tarafından açılan bir penceredir <xref:System.Windows.Window> ve çağırma <xref:System.Windows.Window.ShowDialog%2A> yöntemi. <xref:System.Windows.Window.ShowDialog%2A>bir pencere açılır ve yeni iletişim kutusu kapatılana kadar döndürmez. Bu pencere olarak da bilinen türünde bir *kalıcı* penceresinde ve kullanıcı girişini kısıtlar.  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewdialogboxcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewdialogboxcode)]  
  
## <a name="net-framework-security"></a>.NET Framework Güvenliği  
 Çağırma <xref:System.Windows.Window.ShowDialog%2A> tüm windows ve kullanıcı girdi olaylarını kısıtlama olmaksızın kullanma izni gerektirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İletişim kutusu sonucunu döndürür](../../../../docs/framework/wpf/app-development/how-to-return-a-dialog-box-result.md)
