---
title: "&lt;Clear&gt; öğesi için &lt;dinleyicileri&gt; için &lt;kaynağı&gt;"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/sources/source/listeners/clear
helpviewer_keywords:
- <clear> element for <listeners> for <source>
- clear element for <listeners> for <source>
ms.assetid: 76796bb2-9c0b-4526-8135-8bf18b16d8d9
caps.latest.revision: "7"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: 3cc809a6e896119c5d31c700f3e2ced171da9f7c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="ltcleargt-element-for-ltlistenersgt-for-ltsourcegt"></a><span data-ttu-id="e69bd-102">&lt;Clear&gt; öğesi için &lt;dinleyicileri&gt; için &lt;kaynağı&gt;</span><span class="sxs-lookup"><span data-stu-id="e69bd-102">&lt;clear&gt; Element for &lt;listeners&gt; for &lt;source&gt;</span></span>
<span data-ttu-id="e69bd-103">Temizler `Listeners` koleksiyonu için bir izleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="e69bd-103">Clears the `Listeners` collection for a trace source.</span></span>  
  
 <span data-ttu-id="e69bd-104">\<Yapılandırma ></span><span class="sxs-lookup"><span data-stu-id="e69bd-104">\<configuration></span></span>  
<span data-ttu-id="e69bd-105">\<System.Diagnostics ></span><span class="sxs-lookup"><span data-stu-id="e69bd-105">\<system.diagnostics></span></span>  
<span data-ttu-id="e69bd-106">\<Kaynakları ></span><span class="sxs-lookup"><span data-stu-id="e69bd-106">\<sources></span></span>  
<span data-ttu-id="e69bd-107">\<Kaynak ></span><span class="sxs-lookup"><span data-stu-id="e69bd-107">\<source></span></span>  
<span data-ttu-id="e69bd-108">\<dinleyicileri ></span><span class="sxs-lookup"><span data-stu-id="e69bd-108">\<listeners></span></span>  
<span data-ttu-id="e69bd-109">\<Clear ></span><span class="sxs-lookup"><span data-stu-id="e69bd-109">\<clear></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e69bd-110">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e69bd-110">Syntax</span></span>  
  
```xml  
<clear/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e69bd-111">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="e69bd-111">Attributes and Elements</span></span>  
 <span data-ttu-id="e69bd-112">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e69bd-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e69bd-113">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="e69bd-113">Attributes</span></span>  
 <span data-ttu-id="e69bd-114">Yok.</span><span class="sxs-lookup"><span data-stu-id="e69bd-114">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="e69bd-115">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="e69bd-115">Child Elements</span></span>  
 <span data-ttu-id="e69bd-116">Yok.</span><span class="sxs-lookup"><span data-stu-id="e69bd-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="e69bd-117">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="e69bd-117">Parent Elements</span></span>  
  
|<span data-ttu-id="e69bd-118">Öğe</span><span class="sxs-lookup"><span data-stu-id="e69bd-118">Element</span></span>|<span data-ttu-id="e69bd-119">Açıklama</span><span class="sxs-lookup"><span data-stu-id="e69bd-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="e69bd-120">Her yapılandırma dosyasında yer alan ve ortak dil çalışma zamanı ve .NET Framework uygulamaları tarafından kullanılan kök öğe.</span><span class="sxs-lookup"><span data-stu-id="e69bd-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`system.diagnostics`|<span data-ttu-id="e69bd-121">Toplamak, depolamak ve iletileri ve izleme anahtarı ayarlandığı düzeyi rota izleme dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e69bd-121">Specifies trace listeners that collect, store, and route messages and the level where a trace switch is set.</span></span>|  
|`sources`|<span data-ttu-id="e69bd-122">İzleme iletileri başlatmak izleme kaynaklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="e69bd-122">Contains trace sources that initiate tracing messages.</span></span>|  
|`source`|<span data-ttu-id="e69bd-123">İzleme iletileri başlatan bir izleme kaynağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e69bd-123">Specifies a trace source that initiates tracing messages.</span></span>|  
|`listeners`|<span data-ttu-id="e69bd-124">Toplamak, depolamak ve iletileri yönlendirmek dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e69bd-124">Specifies listeners that collect, store, and route messages.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e69bd-125">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="e69bd-125">Remarks</span></span>  
 <span data-ttu-id="e69bd-126">`<clear>` Öğeyi kaldırır gelen tüm dinleyicileri `Listeners` koleksiyonu için bir izleme kaynağı dahil olmak üzere <xref:System.Diagnostics.DefaultTraceListener>.</span><span class="sxs-lookup"><span data-stu-id="e69bd-126">The `<clear>` element removes all listeners from the `Listeners` collection for a trace source, including the <xref:System.Diagnostics.DefaultTraceListener>.</span></span> <span data-ttu-id="e69bd-127">Kullanabileceğiniz `<clear>` kullanmadan önce öğesi `<add>` öğe koleksiyonda diğer etkin dinleyicileri olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e69bd-127">You can use the `<clear>` element before using the `<add>` element to be certain there are no other active listeners in the collection.</span></span>  
  
## <a name="configuration-file"></a><span data-ttu-id="e69bd-128">Yapılandırma Dosyası</span><span class="sxs-lookup"><span data-stu-id="e69bd-128">Configuration File</span></span>  
 <span data-ttu-id="e69bd-129">Bu öğe makine yapılandırma dosyası (Machine.config) ve uygulama yapılandırma dosyasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e69bd-129">This element can be used in the machine configuration file (Machine.config) and the application configuration file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e69bd-130">Örnek</span><span class="sxs-lookup"><span data-stu-id="e69bd-130">Example</span></span>  
 <span data-ttu-id="e69bd-131">Aşağıdaki örnekte nasıl kullanılacağını gösterir `<clear>` kullanmadan önce öğesi `<add>` dinleyicileri eklemek için öğeleri `console` ve `textListener` için `Listeners` izleme kaynağı toplamalarında `TraceSourceApp`.</span><span class="sxs-lookup"><span data-stu-id="e69bd-131">The following example shows how to use the `<clear>` element before using the `<add>` elements to add the listeners `console` and `textListener` to the `Listeners` collection for the trace source `TraceSourceApp`.</span></span>  
  
```xml  
<configuration>  
  <system.diagnostics>  
    <sources>  
       <source name="TraceSourceApp" switchName="sourceSwitch"   
         switchType="System.Diagnostics.SourceSwitch">  
        <listeners>  
          <clear/>  
          <add name="console"   
            type="System.Diagnostics.ConsoleTraceListener"/>  
          <add name="textListener"/>  
        </listeners>  
      </source>  
    </sources>  
    <sharedListeners>  
      <add name="textListener"   
        type="System.Diagnostics.TextWriterTraceListener"   
        initializeData="myListener.log"/>  
    </sharedListeners>  
    <switches>  
      <add name="sourceSwitch" value="Warning"/>  
    </switches>  
  </system.diagnostics>  
</configuration>   
```  
  
## <a name="see-also"></a><span data-ttu-id="e69bd-132">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e69bd-132">See Also</span></span>  
 <xref:System.Diagnostics.TraceSource>  
 <xref:System.Diagnostics.TraceListener>  
 [<span data-ttu-id="e69bd-133">İzleme ve Hata Ayıklama Ayarları Şeması</span><span class="sxs-lookup"><span data-stu-id="e69bd-133">Trace and Debug Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)  
 [<span data-ttu-id="e69bd-134">İzleme Dinleyicileri</span><span class="sxs-lookup"><span data-stu-id="e69bd-134">Trace Listeners</span></span>](../../../../../docs/framework/debug-trace-profile/trace-listeners.md)
