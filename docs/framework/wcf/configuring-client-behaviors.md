---
title: "İstemci Davranışlarını Yapılandırma"
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
ms.assetid: df5b32fa-e73b-4e8e-b66f-357c748e0173
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 6f16f32128c7223fa600802ae593d36286847dc8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="configuring-client-behaviors"></a><span data-ttu-id="899d5-102">İstemci Davranışlarını Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="899d5-102">Configuring Client Behaviors</span></span>
[!INCLUDE[indigo1](../../../includes/indigo1-md.md)]<span data-ttu-id="899d5-103">iki yolla davranışları yapılandırır: tanımlı davranış yapılandırmalara--başvuran ya da `<behavior>` bölüm bir istemci uygulama yapılandırma dosyası – veya program aracılığıyla çağrı yapan uygulamanın.</span><span class="sxs-lookup"><span data-stu-id="899d5-103"> configures behaviors in two ways: either by referring to behavior configurations -- which are defined in the `<behavior>` section of a client application configuration file – or programmatically in the calling application.</span></span> <span data-ttu-id="899d5-104">Bu konu, her iki yaklaşımın açıklar.</span><span class="sxs-lookup"><span data-stu-id="899d5-104">This topic describes both approaches.</span></span>  
  
 <span data-ttu-id="899d5-105">Bir yapılandırma dosyası kullanırken davranışını yapılandırma adlandırılmış yapılandırma ayarları koleksiyonudur.</span><span class="sxs-lookup"><span data-stu-id="899d5-105">When using a configuration file, behavior configuration is a named collection of configuration settings.</span></span> <span data-ttu-id="899d5-106">Her davranış yapılandırmasının adı benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="899d5-106">The name of each behavior configuration must be unique.</span></span> <span data-ttu-id="899d5-107">Bu dize, kullanılır `behaviorConfiguration` uç nokta için davranış bağlamak için bir uç nokta yapılandırması özniteliğidir.</span><span class="sxs-lookup"><span data-stu-id="899d5-107">This string is used in the `behaviorConfiguration` attribute of an endpoint configuration to link the endpoint to the behavior.</span></span>  
  
## <a name="example"></a><span data-ttu-id="899d5-108">Örnek</span><span class="sxs-lookup"><span data-stu-id="899d5-108">Example</span></span>  
 <span data-ttu-id="899d5-109">Aşağıdaki yapılandırma kodunu adlı bir davranış tanımlar `myBehavior`.</span><span class="sxs-lookup"><span data-stu-id="899d5-109">The following configuration code defines a behavior called `myBehavior`.</span></span> <span data-ttu-id="899d5-110">İstemci uç noktası bu davranışı başvuran `behaviorConfiguration` özniteliği.</span><span class="sxs-lookup"><span data-stu-id="899d5-110">The client endpoint references this behavior in the `behaviorConfiguration` attribute.</span></span>  
  
```xml  
<configuration>  
    <system.serviceModel>  
        <behaviors>  
            <endpointBehaviors>  
                <behavior name="myBehavior">  
                    <clientVia />  
                </behavior>  
            </endpointBehaviors>  
        </behaviors>  
        <bindings>  
            <basicHttpBinding>  
                <binding name="myBinding" maxReceivedMessageSize="10000" />  
            </basicHttpBinding>  
        </bindings>  
        <client>  
            <endpoint address="myAddress" binding="basicHttpBinding" bindingConfiguration="myBinding" behaviorConfiguration="myBehavior" contract="myContract" />  
        </client>  
    </system.serviceModel>  
</configuration>  
```  
  
## <a name="using-behaviors-programmatically"></a><span data-ttu-id="899d5-111">Davranışları program aracılığıyla kullanarak</span><span class="sxs-lookup"><span data-stu-id="899d5-111">Using Behaviors Programmatically</span></span>  
 <span data-ttu-id="899d5-112">Ayrıca yapılandırma veya uygun bularak davranışları programlı olarak Ekle `Behaviors` özellikte [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] istemci nesnesi veya istemci açmadan önce istemci kanal fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="899d5-112">You can also configure or insert behaviors programmatically by locating the appropriate `Behaviors` property on the [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] client object or on the client channel factory object prior to opening the client.</span></span>  
  
## <a name="example"></a><span data-ttu-id="899d5-113">Örnek</span><span class="sxs-lookup"><span data-stu-id="899d5-113">Example</span></span>  
 <span data-ttu-id="899d5-114">Aşağıdaki kod örneğinde nasıl erişerek bir davranış program aracılığıyla ekleneceğini gösterir <xref:System.ServiceModel.Description.ServiceEndpoint.Behaviors%2A> özelliği <xref:System.ServiceModel.Description.ServiceEndpoint> döndürülen <xref:System.ServiceModel.ChannelFactory.Endpoint%2A> kanal nesnesinin oluşturulmasını önce özelliği.</span><span class="sxs-lookup"><span data-stu-id="899d5-114">The following code example shows how to programmatically insert a behavior by accessing the <xref:System.ServiceModel.Description.ServiceEndpoint.Behaviors%2A> property on the <xref:System.ServiceModel.Description.ServiceEndpoint> returned from the <xref:System.ServiceModel.ChannelFactory.Endpoint%2A> property prior to the creation of the channel object.</span></span>  
  
 [!code-csharp[ChannelFactoryBehaviors#10](../../../samples/snippets/csharp/VS_Snippets_CFX/channelfactorybehaviors/cs/client.cs#10)]
 [!code-vb[ChannelFactoryBehaviors#10](../../../samples/snippets/visualbasic/VS_Snippets_CFX/channelfactorybehaviors/vb/client.vb#10)]  
  
## <a name="see-also"></a><span data-ttu-id="899d5-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="899d5-115">See Also</span></span>  
 [<span data-ttu-id="899d5-116">\<davranışları ></span><span class="sxs-lookup"><span data-stu-id="899d5-116">\<behaviors></span></span>](../../../docs/framework/configure-apps/file-schema/wcf/behaviors.md)