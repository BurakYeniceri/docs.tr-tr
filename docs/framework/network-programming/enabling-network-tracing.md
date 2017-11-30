---
title: "Ağ izlemeyi etkinleştirme"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- trace destinations
- sending traces to log file
- trace listeners, network tracing
- network tracing, enabling
- CLR Debugger
- default listeners
- logs, trace
- destination for tracing output
ms.assetid: 5fff458c-51a6-4134-ba47-8a6137ddc41e
caps.latest.revision: "12"
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: da6c9723849694a764a3cb1c050abdb447776113
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="enabling-network-tracing"></a><span data-ttu-id="20002-102">Ağ izlemeyi etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="20002-102">Enabling Network Tracing</span></span>
<span data-ttu-id="20002-103">Ağ izleme yöntem çağrılarını ve yönetilen bir uygulama tarafından oluşturulan tüm ağ trafiği hakkındaki bilgilere erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="20002-103">Network tracing provides access to information about method invocations and network traffic generated by a managed application.</span></span> <span data-ttu-id="20002-104">Uygulamanızdaki ağ izlemeyi etkinleştirmek için aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="20002-104">You must complete the following tasks to enable network tracing in your application:</span></span>  
  
-   <span data-ttu-id="20002-105">İzlemenin etkin kodunuzu derleyin.</span><span class="sxs-lookup"><span data-stu-id="20002-105">Compile your code with tracing enabled.</span></span> <span data-ttu-id="20002-106">Bkz: [nasıl yapılır: izleme ve hata ayıklama ile koşullu derleme](../../../docs/framework/debug-trace-profile/how-to-compile-conditionally-with-trace-and-debug.md) izlemeyi etkinleştirmek için gereken derleyici anahtarları hakkında daha fazla bilgi için.</span><span class="sxs-lookup"><span data-stu-id="20002-106">See [How to: Compile Conditionally with Trace and Debug](../../../docs/framework/debug-trace-profile/how-to-compile-conditionally-with-trace-and-debug.md) for more information about the compiler switches required to enable tracing.</span></span>  
  
-   <span data-ttu-id="20002-107">İzleme çıktısı için bir hedef belirtin.</span><span class="sxs-lookup"><span data-stu-id="20002-107">Specify a destination for tracing output.</span></span>  
  
-   <span data-ttu-id="20002-108">Ağ izleme davranışını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="20002-108">Configure the behavior of network tracing.</span></span> <span data-ttu-id="20002-109">Bkz: [nasıl yapılır: yapılandırma ağ izleme](../../../docs/framework/network-programming/how-to-configure-network-tracing.md) ayrıntılı bilgi için.</span><span class="sxs-lookup"><span data-stu-id="20002-109">See [How to: Configure Network Tracing](../../../docs/framework/network-programming/how-to-configure-network-tracing.md) for detailed information.</span></span>  
  
 <span data-ttu-id="20002-110">İzleme dinleyicileri da adlandırılan en yaygın izleme hedefleri varsayılan dinleyici ve günlük dosyası ' dir.</span><span class="sxs-lookup"><span data-stu-id="20002-110">The most common trace destinations, also referred to as trace listeners, are the default listener and the log file.</span></span>  
  
 <span data-ttu-id="20002-111">İzleme dinleyicisi belirtmezseniz, izleme varsayılan dinleyicisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="20002-111">Tracing uses the default listener if you do not specify a trace listener.</span></span> <span data-ttu-id="20002-112">CLR hata ayıklayıcısı .NET Framework SDK ile birlikte gelen veya DBwin32.exe Windows SDK ile birlikte gelen gibi yönetilen bir kod etkin hata ayıklayıcı'kodunuzu yürüterek varsayılan dinleyicisi gönderilen iletileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20002-112">You can view messages sent to the default listener by executing your code in a managed code-enabled debugger such as the CLR Debugger shipped with the .NET Framework SDK, or DBwin32.exe shipped with the Windows SDK.</span></span> <span data-ttu-id="20002-113">CLR hata ayıklayıcısı kullanarak, izleme iletilerini görünür **çıkış** penceresi.</span><span class="sxs-lookup"><span data-stu-id="20002-113">Using the CLR Debugger, the trace messages appear in the **Output** window.</span></span>  
  
 <span data-ttu-id="20002-114">İzlemelerini almak için bir dosya kullanmayı tercih ederseniz, bir günlük dosyası yapılandırma ayarlarını kullanarak aşağıdaki örnekte gösterildiği gibi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20002-114">If you prefer to use a file to receive traces, you can specify a log file by using configuration settings, as shown in the following example.</span></span> <span data-ttu-id="20002-115">(Yapılandırma dosyaları hakkında genel bilgiler için bkz: [yapılandırma dosyalarını](../../../docs/framework/configure-apps/index.md).)</span><span class="sxs-lookup"><span data-stu-id="20002-115">(For a general discussion of configuration files, see [Configuration Files](../../../docs/framework/configure-apps/index.md).)</span></span>  
  
 <span data-ttu-id="20002-116">Bir günlük dosyasına izlemeleri göndermek için aşağıdaki düğüm eklemek `<system.diagnostics>` düğümü uygun yapılandırma dosyasının (uygulama veya makine).</span><span class="sxs-lookup"><span data-stu-id="20002-116">To send traces to a log file, add the following node to the `<system.diagnostics>` node of the appropriate configuration file (application or machine).</span></span> <span data-ttu-id="20002-117">Gereksinimlerinize uygun olarak dosyanın (trace.log) adını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20002-117">You can change the name of the file (trace.log) to suit your needs.</span></span>  
  
```xml  
<system.diagnostics>  
  <trace autoflush="true" indentsize="4">  
    <listeners>  
      <add name="file" type="System.Diagnostics.TextWriterTraceListener" initializeData="trace.log"/>  
    </listeners>   
  </trace>  
</system.diagnostics>  
```  
  
## <a name="see-also"></a><span data-ttu-id="20002-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="20002-118">See Also</span></span>  
 [<span data-ttu-id="20002-119">Ağ izleme yorumlama</span><span class="sxs-lookup"><span data-stu-id="20002-119">Interpreting Network Tracing</span></span>](../../../docs/framework/network-programming/interpreting-network-tracing.md)  
 [<span data-ttu-id="20002-120">.NET Framework'te ağ izleme</span><span class="sxs-lookup"><span data-stu-id="20002-120">Network Tracing in the .NET Framework</span></span>](../../../docs/framework/network-programming/network-tracing.md)  
 [<span data-ttu-id="20002-121">İzleme ve izleme giriş</span><span class="sxs-lookup"><span data-stu-id="20002-121">Introduction to Instrumentation and Tracing</span></span>](http://msdn.microsoft.com/en-us/e924e57c-33cf-4b0e-9e7f-a45d13e38f2c)