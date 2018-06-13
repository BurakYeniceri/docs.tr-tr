---
title: 'Nasıl yapılır: bir sayfanın yüklenmesini durdurmak'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pages [WPF], stopping from loading
- methods [WPF], Stoploading
- events [WPF], NavigationStopped
- NavigationStopped properties [WPF]
- stopping pages from loading [WPF]
- loading [WPF], stopping
ms.assetid: e2b695b0-517e-462c-8ccf-90cc8d6ba864
ms.openlocfilehash: e5cd7d1b881b816636c3acdd4d33565304ca9b63
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33545551"
---
# <a name="how-to-stop-a-page-from-loading"></a><span data-ttu-id="dcb5e-102">Nasıl yapılır: bir sayfanın yüklenmesini durdurmak</span><span class="sxs-lookup"><span data-stu-id="dcb5e-102">How to: Stop a Page from Loading</span></span>
<span data-ttu-id="dcb5e-103">Bu örnek nasıl çağrılacağını gösterir <xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> indirilmesi bitmeden önce içerik için Gezinti durdurmak için yöntem.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-103">This example shows how to call the <xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> method to stop navigation to content before it has finished being downloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dcb5e-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="dcb5e-104">Example</span></span>  
 <span data-ttu-id="dcb5e-105"><xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> İstenen içeriğin indirilmesini durdurur ve neden <xref:System.Windows.Navigation.NavigationWindow.NavigationStopped> çıkarılmasına olay.</span><span class="sxs-lookup"><span data-stu-id="dcb5e-105"><xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> stops the download of the requested content, and causes the <xref:System.Windows.Navigation.NavigationWindow.NavigationStopped> event to be raised.</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateStopLoadingCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/MainWindow.xaml.cs#navigatestoploadingcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateStopLoadingCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/mainwindow.xaml.vb#navigatestoploadingcode)]
