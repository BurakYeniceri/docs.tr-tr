---
title: '&lt;behaviorExtensions&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 59f2791a-c78f-40d7-aa80-0d9cd10135d9
caps.latest.revision: "9"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: ed7c75fb7070b43b850a8f5b812abf0a52c3c16f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ltbehaviorextensionsgt"></a><span data-ttu-id="98315-102">&lt;behaviorExtensions&gt;</span><span class="sxs-lookup"><span data-stu-id="98315-102">&lt;behaviorExtensions&gt;</span></span>
<span data-ttu-id="98315-103">Kullanıcı tanımlı davranış öğeleri oluşturmak kullanıcı davranışı uzantıları sağlar.</span><span class="sxs-lookup"><span data-stu-id="98315-103">Behavior extensions enable the user to create user-defined behavior elements.</span></span> <span data-ttu-id="98315-104">Standart Windows Communication Foundation (WCF) davranışı öğeleri yanı sıra bu öğeler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="98315-104">These elements can be used alongside the standard Windows Communication Foundation (WCF) behavior elements.</span></span> <span data-ttu-id="98315-105">`behaviorExtensions` Bölümü sağlayacak şekilde yapılandırmada kullanılan öğe tanımlar.</span><span class="sxs-lookup"><span data-stu-id="98315-105">The `behaviorExtensions` section defines the element such that it can be used in configuration.</span></span> <span data-ttu-id="98315-106">Tipik davranış uzantısı bir örneği burada verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="98315-106">Here is an example of a typical behavior extension.</span></span>  
  
```xml  
<system.serviceModel>  
    <extensions>  
        <behaviorExtensions>  
            <add name="myBehavior" type="Microsoft.ServiceModel.Samples.MyBehaviorSection, MyBehavior,  
                Version=1.0.0.0, Culture=neutral, PublicKeyToken=null" />  
       </behaviorExtensions>  
    </extensions>  
</system.serviceModel>  
```  
  
 <span data-ttu-id="98315-107">Yapılandırma yeteneklerini öğesine eklemek için yazma ve yapılandırma öğesi kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="98315-107">To add configuration abilities to the element, you need to write and register a configuration element.</span></span> <span data-ttu-id="98315-108">Bunun hakkında daha fazla bilgi için bkz: <xref:System.Configuration> belgeleri.</span><span class="sxs-lookup"><span data-stu-id="98315-108">For more information on this, see the <xref:System.Configuration> documentation.</span></span>  
  
 <span data-ttu-id="98315-109">Öğesini ve kendi yapılandırma türü tanımlandıktan sonra uzantı, aşağıdaki örnekte gösterildiği gibi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="98315-109">After the element and its configuration type are defined, the extension can be used, as shown in the following example.</span></span>  
  
```xml  
<behaviors>  
    <behavior configurationName="testChannelBehavior">  
        <myBehavior />  
        <channelSecurity cacheCookies="false" detectReplays="false" maxCachedNonces="9"  
            maxClockSkew="00:00:03" maxCookieCachingTime="00:07:24" replayWindow="00:07:22.2190000" />  
    </behavior>  
</behaviors>  
```  
  
## <a name="security"></a><span data-ttu-id="98315-110">Güvenlik</span><span class="sxs-lookup"><span data-stu-id="98315-110">Security</span></span>  
 <span data-ttu-id="98315-111">Tam nitelikli derleme adları türlerinde kaydederken kullanmanız önemle tavsiye edilir `machine.config` ve `app.config` dosyaları.</span><span class="sxs-lookup"><span data-stu-id="98315-111">It is strongly recommended that you use fully qualified assembly names when registering types in the `machine.config` and `app.config` files.</span></span> <span data-ttu-id="98315-112">Türü benzersiz olarak tanımlanmazsa, CLR türü Yükleyicisi için belirtilen sırayla aşağıdaki konumlarda arar:</span><span class="sxs-lookup"><span data-stu-id="98315-112">If the type is not uniquely defined, the CLR type loader searches for it in the following locations in the specified order:</span></span>  
  
 <span data-ttu-id="98315-113">Derleme türü bilinen, yükleyici yapılandırma dosyanın yeniden yönlendirme konumları, GAC, yapılandırma bilgilerini ve uygulamanın ana dizin kullanılarak geçerli derleme arar.</span><span class="sxs-lookup"><span data-stu-id="98315-113">If the assembly of the type is known, the loader searches the configuration file's redirect locations, GAC, the current assembly using configuration information, and the application base directory.</span></span> <span data-ttu-id="98315-114">Derleme bilinmiyorsa, yükleyici geçerli derleme, mscorlib ve tarafından döndürülen konumu arar `TypeResolve` olay işleyicisi.</span><span class="sxs-lookup"><span data-stu-id="98315-114">If the assembly is unknown, the loader searches the current assembly, mscorlib, and the location returned by the `TypeResolve` event handler.</span></span> <span data-ttu-id="98315-115">Tür iletme mekanizması ve AppDomain.TypeResolve olay gibi kancaları ile bu CLR arama sırası değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="98315-115">This CLR search order can be modified with hooks such as the Type Forwarding mechanism and the AppDomain.TypeResolve event.</span></span>  
  
 <span data-ttu-id="98315-116">Bir saldırgan, CLR arama sırası yararlanma ve yetkisiz kodunu yürütün.</span><span class="sxs-lookup"><span data-stu-id="98315-116">An attacker can exploit the CLR search order and execute unauthorized code.</span></span> <span data-ttu-id="98315-117">Tam (tanımlayıcı) adlarının benzersiz olarak kullanarak bir türü tanımlar ve daha da sisteminizin güvenliğini artırır.</span><span class="sxs-lookup"><span data-stu-id="98315-117">Using fully qualified (strong) names uniquely identifies a type and further increases security of your system.</span></span>  
  
 <span data-ttu-id="98315-118">Daha fazla bilgi için bkz: [nasıl çalışma zamanı bulur derlemeleri](http://go.microsoft.com/fwlink/?LinkId=95336) ve <xref:System.AppDomain.TypeResolve>.</span><span class="sxs-lookup"><span data-stu-id="98315-118">For more information, see [How the Runtime Locates Assemblies](http://go.microsoft.com/fwlink/?LinkId=95336) and <xref:System.AppDomain.TypeResolve>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98315-119">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="98315-119">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.BehaviorExtensionElement>  
 [<span data-ttu-id="98315-120">Yapılandırma ve çalışma zamanını davranışlarla genişletme</span><span class="sxs-lookup"><span data-stu-id="98315-120">Configuring and Extending the Runtime with Behaviors</span></span>](../../../../../docs/framework/wcf/extending/configuring-and-extending-the-runtime-with-behaviors.md)