---
title: '&lt;exposedMethod&gt;'
ms.date: 03/30/2017
ms.assetid: 61c938cd-4ee9-4b06-ab28-922ef491ab11
ms.openlocfilehash: 2a26ca90f6a66592c246cc9e5aef50cfa53b4bdd
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2018
---
# <a name="ltexposedmethodgt"></a><span data-ttu-id="5766c-102">&lt;exposedMethod&gt;</span><span class="sxs-lookup"><span data-stu-id="5766c-102">&lt;exposedMethod&gt;</span></span>
<span data-ttu-id="5766c-103">Bir Web hizmeti olarak bir COM bileşeni arabirimde kullanıma sunulduğunda sunulan bir COM + yöntemi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5766c-103">Represents a COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>  
  
 <span data-ttu-id="5766c-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="5766c-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="5766c-105">\<comContracts ></span><span class="sxs-lookup"><span data-stu-id="5766c-105">\<comContracts></span></span>  
<span data-ttu-id="5766c-106">\<comContract ></span><span class="sxs-lookup"><span data-stu-id="5766c-106">\<comContract></span></span>  
<span data-ttu-id="5766c-107">\<yöntemleri ></span><span class="sxs-lookup"><span data-stu-id="5766c-107">\<methods></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5766c-108">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="5766c-108">Syntax</span></span>  
  
```xml  
<comContracts>  
  <comContract>  
      <exposedMethods>  
         <exposedMethod name="string" />  
      </exposedMethods>  
  </comContract>  
</comContracts>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="5766c-109">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="5766c-109">Attributes and Elements</span></span>  
 <span data-ttu-id="5766c-110">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5766c-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="5766c-111">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="5766c-111">Attributes</span></span>  
  
|<span data-ttu-id="5766c-112">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="5766c-112">Attribute</span></span>|<span data-ttu-id="5766c-113">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5766c-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="5766c-114">name</span><span class="sxs-lookup"><span data-stu-id="5766c-114">name</span></span>|<span data-ttu-id="5766c-115">Bir Web hizmeti olarak bir COM bileşeni arabirimde kullanıma sunulduğunda sunulan COM + yöntemini içeren bir dize.</span><span class="sxs-lookup"><span data-stu-id="5766c-115">A string that contains the COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="5766c-116">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="5766c-116">Child Elements</span></span>  
 <span data-ttu-id="5766c-117">Yok.</span><span class="sxs-lookup"><span data-stu-id="5766c-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="5766c-118">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="5766c-118">Parent Elements</span></span>  
  
|<span data-ttu-id="5766c-119">Öğe</span><span class="sxs-lookup"><span data-stu-id="5766c-119">Element</span></span>|<span data-ttu-id="5766c-120">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5766c-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="5766c-121">\<exposedMethods ></span><span class="sxs-lookup"><span data-stu-id="5766c-121">\<exposedMethods></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethods.md)|<span data-ttu-id="5766c-122">Bir koleksiyonu [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) öğeleri.</span><span class="sxs-lookup"><span data-stu-id="5766c-122">A collection of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="5766c-123">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="5766c-123">Remarks</span></span>  
 <span data-ttu-id="5766c-124">COM + tümleştirme Yapılandırma Aracı (ComSvcConfig.exe) oluşturulan hizmet sözleşmesini görünmesi bir COM arabirimden belirli yöntemleri eklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5766c-124">The COM+ integration configuration tool (ComSvcConfig.exe) can be used to add specific methods from a COM interface to appear on the generated service contract.</span></span>  
  
 <span data-ttu-id="5766c-125">Örneğin, üç adlandırılmış yöntemleri eklemek için aşağıdaki komutu kullanabilirsiniz `IFinances` COM arabirimde `ItemOrders`. Oluşturulan servis sözleşmesi finansal bileşeni.</span><span class="sxs-lookup"><span data-stu-id="5766c-125">For example, you can use the following command to add the three named methods from the `IFinances` COM interface on the `ItemOrders`.Financial component, to the generated service contract.</span></span>  
  
 `ComSvcConfig.exe /i /application:OnlineStore /contract:ItemOrders.Financial,IFinances.{TransferFunds,AddFunds,RemoveFunds} /hosting:complus`  
  
 <span data-ttu-id="5766c-126">Sonra da ComSvcConfig.exe çalıştırdığınızda, yukarıda açıklanan yöntemleri olarak listeleniyor aşağıdaki hizmet sözleşmesini ürettiği [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) öğeleri.</span><span class="sxs-lookup"><span data-stu-id="5766c-126">When you also run the ComSvcConfig.exe, it then generates the following service contract listing the previously mentioned methods as [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span>  
  
```xml  
<comContract contractType="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}" name="IFinances" namespace="http://contoso.com/services/financial">  
    <exposedMethod name="TransferFunds"/>  
    <exposedMethod name="AddFunds"/>  
    <exposedMethod name="RemoveFunds"/>  
</comContract>  
```  
  
 <span data-ttu-id="5766c-127">Hizmet başlatma zamanında çalışma zamanı hizmet sözleşmesi üzerinden yansıtma ve yalnızca listesinde yer yöntemleri ekleyerek oluşturmaya çalıştığında [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) öğeleri.</span><span class="sxs-lookup"><span data-stu-id="5766c-127">At service initialization time, the runtime attempts to generate a service contract by reflecting over and adding only the methods included in the list of [\<exposedMethod>](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) elements.</span></span> <span data-ttu-id="5766c-128">İzleme, hizmet sözleşmesini dahil edilmeyen her arabirim yöntemi için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5766c-128">A trace is produced for every interface method that is not included on the service contract.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5766c-129">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5766c-129">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComMethodElementCollection>  
 <xref:System.ServiceModel.Configuration.ComMethodElement>  
 [<span data-ttu-id="5766c-130">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="5766c-130">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="5766c-131">COM+ Uygulamaları ile Tümleştirme</span><span class="sxs-lookup"><span data-stu-id="5766c-131">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="5766c-132">Nasıl yapılır: COM+ Hizmet Ayarlarını Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="5766c-132">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
