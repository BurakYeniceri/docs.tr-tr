---
title: 'Nasıl yapılır: Uygulama Oturumları Arasında Uygulama Kapsamı Özelliklerini Koruma ve Geri Yükleme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application-scope properties [WPF], persisting
- persisting application-scope properties [WPF]
- properties [WPF], persisting
- restoring application-scope properties [WPF]
- properties [WPF], restoring
- application-scope properties [WPF], restoring
ms.assetid: 55d5904a-f444-4eb5-abd3-6bc74dd14226
ms.openlocfilehash: ff95833920ead040f1812637721fdd402186898c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33550104"
---
# <a name="how-to-persist-and-restore-application-scope-properties-across-application-sessions"></a><span data-ttu-id="78d58-102">Nasıl yapılır: Uygulama Oturumları Arasında Uygulama Kapsamı Özelliklerini Koruma ve Geri Yükleme</span><span class="sxs-lookup"><span data-stu-id="78d58-102">How to: Persist and Restore Application-Scope Properties Across Application Sessions</span></span>
<span data-ttu-id="78d58-103">Bu örnek uygulama kapsamı özelliklerini uygulama kapatıldığında ve geri yüklemek için bir uygulama sonraki olduğunda uygulama kapsamı özelliklerini başlatma nasıl devam etmek nasıl gösterir.</span><span class="sxs-lookup"><span data-stu-id="78d58-103">This example shows how to persist application-scope properties when an application shuts down, and how to restore application-scope properties when an application is next launch.</span></span>  
  
## <a name="example"></a><span data-ttu-id="78d58-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="78d58-104">Example</span></span>  
 <span data-ttu-id="78d58-105">Uygulama için uygulama kapsamı özelliklerini devam ederse ve yalıtılmış depolama biriminden, geri yükler.</span><span class="sxs-lookup"><span data-stu-id="78d58-105">The application persists application-scope properties to, and restores them from, isolated storage.</span></span> <span data-ttu-id="78d58-106">Yalıtılmış Depolama güvenle dosya erişim izni olmadan uygulamaları tarafından kullanılabilecek bir korumalı depolama alanıdır.</span><span class="sxs-lookup"><span data-stu-id="78d58-106">Isolated storage is a protected storage area that can safely be used by applications without file access permission.</span></span>  
  
 [!code-xaml[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesXAML1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml#persistrestoreappscopepropertiesxaml1)]  
[!code-xaml[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesXAML2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml#persistrestoreappscopepropertiesxaml2)]  
  
 [!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs#persistrestoreappscopepropertiescodebehind1)]
 [!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb#persistrestoreappscopepropertiescodebehind1)]  
[!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs#persistrestoreappscopepropertiescodebehind2)]
[!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb#persistrestoreappscopepropertiescodebehind2)]  
[!code-csharp[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/CSharp/App.xaml.cs#persistrestoreappscopepropertiescodebehind3)]
[!code-vb[HOWTOApplicationModelSnippets#PersistRestoreAppScopePropertiesCODEBEHIND3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOApplicationModelSnippets/visualbasic/application.xaml.vb#persistrestoreappscopepropertiescodebehind3)]
