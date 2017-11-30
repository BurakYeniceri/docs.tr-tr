---
title: "Windows Mağazası Uygulamaları için .NET Framework'te Yansıma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- reflection, Windows Store apps
- .NET for Windows Store apps, TypeInfo class
ms.assetid: 0d07090c-9b47-4ecc-81d1-29d539603c9b
caps.latest.revision: "20"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 80429810a46438cdbf7cf2993e5f3b0779d300c1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="reflection-in-the-net-framework-for-windows-store-apps"></a><span data-ttu-id="42663-102">Windows Mağazası Uygulamaları için .NET Framework'te Yansıma</span><span class="sxs-lookup"><span data-stu-id="42663-102">Reflection in the .NET Framework for Windows Store Apps</span></span>
<span data-ttu-id="42663-103">[!INCLUDE[net_v45](../../../includes/net-v45-md.md)] başlayarak .NET Framework, [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] uygulamasında kullanılmak üzere bir yansıma türü ve üye kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="42663-103">Starting with the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)], the .NET Framework includes a set of reflection types and members for use in [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] apps.</span></span> <span data-ttu-id="42663-104">Bu türleri ve üyeleri de tam .NET Framework olarak kullanılabilir olan [.NET için Windows mağazası uygulamaları](http://go.microsoft.com/fwlink/?LinkID=225700).</span><span class="sxs-lookup"><span data-stu-id="42663-104">These types and members are available in the full .NET Framework as well as in the [.NET for Windows Store apps](http://go.microsoft.com/fwlink/?LinkID=225700).</span></span> <span data-ttu-id="42663-105">Bu belge, bunlar ile .NET Framework 4 ve daha önceki sürümlerdeki karşılıkları arasındaki temel farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="42663-105">This document explains the major differences between these and their counterparts in the .NET Framework 4 and earlier versions.</span></span>  
  
 <span data-ttu-id="42663-106">Bir [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] uygulaması oluşturuyorsanız, [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)]'de bulunan yansıma türlerini ve üyeleri kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="42663-106">If you are creating a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app, you must use the reflection types and members in the [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)].</span></span> <span data-ttu-id="42663-107">Bu türler ve üyeler, gerekli olmasa da aynı zamanda masaüstü uygulamalarında kullanılmak üzere mevcuttur, bu nedenle her iki uygulama türü için de aynı kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42663-107">These types and members are also available, but not required, for use in desktop apps, so you can use the same code for both types of apps.</span></span>  
  
## <a name="typeinfo-and-assembly-loading"></a><span data-ttu-id="42663-108">TypeInfo ve Derleme Yükleme</span><span class="sxs-lookup"><span data-stu-id="42663-108">TypeInfo and Assembly Loading</span></span>  
 <span data-ttu-id="42663-109">[!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)]'de, <xref:System.Reflection.TypeInfo> sınıfı .NET Framework 4 <xref:System.Type> sınıfının bazı işlevlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="42663-109">In the [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)], the <xref:System.Reflection.TypeInfo> class contains some of the functionality of the .NET Framework 4 <xref:System.Type> class.</span></span> <span data-ttu-id="42663-110">Bir <xref:System.Type> nesnesi, tür tanımını kendisi temsil ederken bir <xref:System.Reflection.TypeInfo> nesnesi, tür tanımına bir başvuruyu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="42663-110">A <xref:System.Type> object represents a reference to a type definition, whereas a <xref:System.Reflection.TypeInfo> object represents the type definition itself.</span></span> <span data-ttu-id="42663-111">Bu, başvurdukları derlemenin çalışma zamanı tarafından yüklenmesine gerek olmadan <xref:System.Type> nesnelerini işlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="42663-111">This enables you to manipulate <xref:System.Type> objects without necessarily requiring the runtime to load the assembly they reference.</span></span> <span data-ttu-id="42663-112">İlişkili <xref:System.Reflection.TypeInfo> nesnesini almak, derlemeyi yüklenmeye zorlar.</span><span class="sxs-lookup"><span data-stu-id="42663-112">Getting the associated <xref:System.Reflection.TypeInfo> object forces the assembly to load.</span></span>  
  
 <span data-ttu-id="42663-113"><xref:System.Reflection.TypeInfo>, <xref:System.Type>'da kullanılabilir olan üyelerin birçoğunu içerir ve [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)]'deki yansıma özelliklerinin birçoğu <xref:System.Reflection.TypeInfo> nesnesinin koleksiyonlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="42663-113"><xref:System.Reflection.TypeInfo> contains many of the members available on <xref:System.Type>, and many of the reflection properties in the [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)] return collections of <xref:System.Reflection.TypeInfo> objects.</span></span> <span data-ttu-id="42663-114">Bir <xref:System.Reflection.TypeInfo> nesnesinden <xref:System.Type> nesnesini almak için <xref:System.Reflection.IReflectableType.GetTypeInfo%2A> yöntemini kullanın.</span><span class="sxs-lookup"><span data-stu-id="42663-114">To get a <xref:System.Reflection.TypeInfo> object from a <xref:System.Type> object, use the <xref:System.Reflection.IReflectableType.GetTypeInfo%2A> method.</span></span>  
  
## <a name="query-methods"></a><span data-ttu-id="42663-115">Sorgu yöntemleri</span><span class="sxs-lookup"><span data-stu-id="42663-115">Query Methods</span></span>  
 <span data-ttu-id="42663-116">[!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)]'da, dizileri döndüren yöntemler yerine <xref:System.Collections.Generic.IEnumerable%601> öğesini döndüren yansıma özelliklerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="42663-116">In the [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)], you use the reflection properties that return <xref:System.Collections.Generic.IEnumerable%601> collections instead of methods that return arrays.</span></span> <span data-ttu-id="42663-117">Yansıma bağlamları, büyük derlemeler veya türler için bu koleksiyonların yavaş çapraz geçişini uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="42663-117">Reflection contexts can implement lazy traversal of these collections for large assemblies or types.</span></span>  
  
 <span data-ttu-id="42663-118">Yansıma özellikleri, özel bir nesne için, kalıtım ağacına dönmek yerince yalnızca belirtilen yöntemleri kullanırlar.</span><span class="sxs-lookup"><span data-stu-id="42663-118">The reflection properties return only the declared methods on a particular object instead of traversing the inheritance tree.</span></span> <span data-ttu-id="42663-119">Ayrıca, filtreleme için <xref:System.Reflection.BindingFlags> parametrelerini kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="42663-119">Moreover, they do not use <xref:System.Reflection.BindingFlags> parameters for filtering.</span></span> <span data-ttu-id="42663-120">Bunun yerine filtreleme işlemi, döndürülen koleksiyonlarda LINQ sorguları kullanılarak kullanıcı kodu içinde yer alır.</span><span class="sxs-lookup"><span data-stu-id="42663-120">Instead, filtering takes place in user code, by using LINQ queries on the returned collections.</span></span> <span data-ttu-id="42663-121">Çalışma zamanıyla oluşan yansıma nesneleri için (örneğin, `typeof(Object)`'in sonucu olarak) devralma ağacının çapraz geçişi en iyi, <xref:System.Reflection.RuntimeReflectionExtensions> sınıfının yardımcı yöntemleri kullanılarak gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="42663-121">For reflection objects that originate with the runtime (for example, as the result of `typeof(Object)`), traversing the inheritance tree is best accomplished by using the helper methods of the <xref:System.Reflection.RuntimeReflectionExtensions> class.</span></span> <span data-ttu-id="42663-122">Özelleştirilmiş yansıma bağlamlarından gelen nesnelerin tüketicileri bu yöntemleri kullanamaz ve kendileri devralma ağacını kendileri geçirmeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="42663-122">Consumers of objects from customized reflection contexts cannot use these methods, and must traverse the inheritance tree themselves.</span></span>  
  
## <a name="restrictions"></a><span data-ttu-id="42663-123">Kısıtlamalar</span><span class="sxs-lookup"><span data-stu-id="42663-123">Restrictions</span></span>  
 <span data-ttu-id="42663-124">Bir [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] uygulamasında, bazı .NET Framework türlerine ve üyelerine erişim sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="42663-124">In a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app, access to some .NET Framework types and members is restricted.</span></span> <span data-ttu-id="42663-125">Örneğin, bir [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)] nesnesini kullanarak, <xref:System.Reflection.MethodInfo>'a dahil edilmeyen .NET Framework yöntemlerini çağıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="42663-125">For example, you cannot call .NET Framework methods that are not included in [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)], by using a <xref:System.Reflection.MethodInfo> object.</span></span> <span data-ttu-id="42663-126">Ayrıca, [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] ve <xref:System.Runtime.InteropServices.Marshal> üyeleri gibi, bir <xref:System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMarshal> uygulamasının bağlamında güvenli olarak nitelendirilmeyen belirli tür ve üyeler engellenir.</span><span class="sxs-lookup"><span data-stu-id="42663-126">In addition, certain types and members that are not considered safe within the context of a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] app are blocked, as are <xref:System.Runtime.InteropServices.Marshal> and <xref:System.Runtime.InteropServices.WindowsRuntime.WindowsRuntimeMarshal> members.</span></span> <span data-ttu-id="42663-127">Bu kısıtlama yalnızca .NET Framework türlerini ve üyelerini etkiler; normalde yaptığınız gibi kodunuzu veya üçüncü taraf kodunu çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42663-127">This restriction affects only .NET Framework types and members; you can call your code or third-party code as you normally would.</span></span>  
  
## <a name="example"></a><span data-ttu-id="42663-128">Örnek</span><span class="sxs-lookup"><span data-stu-id="42663-128">Example</span></span>  
 <span data-ttu-id="42663-129">Bu örnek, devralınan yöntemler ve özellikler dahil olmak üzere [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)] türünün yöntemlerini ve özelliklerini almak için <xref:System.Globalization.Calendar> öğesinde yansıma türlerini ve üyelerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="42663-129">This example uses the reflection types and members in the [!INCLUDE[net_win8_profile](../../../includes/net-win8-profile-md.md)] to retrieve the methods and properties of the <xref:System.Globalization.Calendar> type, including inherited methods and properties.</span></span> <span data-ttu-id="42663-130">Bu kodu çalıştırmak için için kod dosyası yapıştırın bir [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] içeren sayfasını bir [Windows.UI.Xaml.Controls.Textblock](http://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.controls.textblock.aspx) adlı Denetim `textblock1` yansıma adlı bir projede.</span><span class="sxs-lookup"><span data-stu-id="42663-130">To run this code, paste it into the code file for a [!INCLUDE[win8_appname_long](../../../includes/win8-appname-long-md.md)] page that contains a [Windows.UI.Xaml.Controls.Textblock](http://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.controls.textblock.aspx) control named `textblock1` in a project named Reflection.</span></span> <span data-ttu-id="42663-131">Yalnızca bu kodu farklı bir ada sahip bir proje içinde yapıştırırsanız, projenizin eşleştirmek için ad alanı adı değiştirdiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="42663-131">If you paste this code inside a project with a different name, just make sure you change the namespace name to match your project.</span></span>  
  
 [!code-csharp[System.ReflectionWinStoreApp#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.reflectionwinstoreapp/cs/mainpage.xaml.cs#1)]
 [!code-vb[System.ReflectionWinStoreApp#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.reflectionwinstoreapp/vb/mainpage.xaml.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="42663-132">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="42663-132">See Also</span></span>  
 [<span data-ttu-id="42663-133">Yansıma</span><span class="sxs-lookup"><span data-stu-id="42663-133">Reflection</span></span>](../../../docs/framework/reflection-and-codedom/reflection.md)  
 [<span data-ttu-id="42663-134">.NET için Windows mağazası uygulamaları – desteklenen API'leri</span><span class="sxs-lookup"><span data-stu-id="42663-134">.NET for Windows Store apps – supported APIs</span></span>](http://go.microsoft.com/fwlink/?LinkID=225700)