---
title: '&lt;kimlik&gt; için &lt;sertifika&gt;'
ms.date: 03/30/2017
ms.assetid: 4aeccaf7-8f23-495c-aa5f-5bd8b5d4a10c
ms.openlocfilehash: e7d8e7abbc95521d85dc5999c36687f9becea9fb
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2018
---
# <a name="ltcertificategt-for-ltidentitygt"></a><span data-ttu-id="9af19-102">&lt;kimlik&gt; için &lt;sertifika&gt;</span><span class="sxs-lookup"><span data-stu-id="9af19-102">&lt;certificate&gt; for &lt;identity&gt;</span></span>
<span data-ttu-id="9af19-103">Bir istemci sunucuya doğrulamak için kullanılan bir X.509 sertifikası belirtir.</span><span class="sxs-lookup"><span data-stu-id="9af19-103">Specifies an X.509 certificate used to validate a server to a client.</span></span>  
  
 <span data-ttu-id="9af19-104">Öğe değerini ayarlama hakkında daha fazla bilgi için bkz: [hizmet kimliği ve kimlik doğrulama](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="9af19-104">For more information about setting the element value, see [Service Identity and Authentication](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).</span></span>  
  
 <span data-ttu-id="9af19-105">\<Kimliği ></span><span class="sxs-lookup"><span data-stu-id="9af19-105">\<identity></span></span>  
<span data-ttu-id="9af19-106">\<Sertifika ></span><span class="sxs-lookup"><span data-stu-id="9af19-106">\<certificate></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9af19-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="9af19-107">Syntax</span></span>  
  
```xml  
<certificate encodedValue = "String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9af19-108">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="9af19-108">Attributes and Elements</span></span>  
 <span data-ttu-id="9af19-109">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9af19-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9af19-110">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="9af19-110">Attributes</span></span>  
  
|<span data-ttu-id="9af19-111">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="9af19-111">Attribute</span></span>|<span data-ttu-id="9af19-112">Açıklama</span><span class="sxs-lookup"><span data-stu-id="9af19-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9af19-113">encodedValue</span><span class="sxs-lookup"><span data-stu-id="9af19-113">encodedValue</span></span>|<span data-ttu-id="9af19-114">Bir Base64'ın sertifikasını kodlaması.</span><span class="sxs-lookup"><span data-stu-id="9af19-114">A Base64 encoding of the certificate.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9af19-115">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="9af19-115">Child Elements</span></span>  
 <span data-ttu-id="9af19-116">Yok.</span><span class="sxs-lookup"><span data-stu-id="9af19-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="9af19-117">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="9af19-117">Parent Elements</span></span>  
  
|<span data-ttu-id="9af19-118">Öğe</span><span class="sxs-lookup"><span data-stu-id="9af19-118">Element</span></span>|<span data-ttu-id="9af19-119">Açıklama</span><span class="sxs-lookup"><span data-stu-id="9af19-119">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9af19-120">\<Kimliği ></span><span class="sxs-lookup"><span data-stu-id="9af19-120">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|<span data-ttu-id="9af19-121">İstemci tarafından doğrulanmasını hizmetin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9af19-121">Specifies the identity of the service to be authenticated by the client.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9af19-122">Örnek</span><span class="sxs-lookup"><span data-stu-id="9af19-122">Example</span></span>  
 <span data-ttu-id="9af19-123">Aşağıdaki kod, bir istemci sunucuya doğrulamak için kullanılan bir sertifika kodlanmış gösterimi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9af19-123">The following code specifies the encoded representation of a certificate used to validate a server to a client.</span></span>  
  
```xml  
<identity>  
  <certificate encodedValue = " MIIBxjCCAXSgAwIBAgIQmXJgyu9tro1M98GifjtuoDAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC1Jvb3QgQWdlbmN5MB4XDTA2MDUxNzIxNDQyNVoXDTM5MTIzMTIzNTk1OVowKTEQMA4GA1UEChMHQ29udG9zbzEVMBMGA1UEAxMMaWRlbnRpdHkuY29tMIGfMA0GCSqGSIb3DQEBAQUAA4GNADCBiQKBgQDBmivcb8hYbh11hqVoDuB7zmJ2y230f" />  
</identity>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9af19-124">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="9af19-124">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 <xref:System.ServiceModel.EndpointIdentity>  
 [<span data-ttu-id="9af19-125">Kimlik Doğrulama ile Hizmet Kimliği</span><span class="sxs-lookup"><span data-stu-id="9af19-125">Service Identity and Authentication</span></span>](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [<span data-ttu-id="9af19-126">\<Kimliği ></span><span class="sxs-lookup"><span data-stu-id="9af19-126">\<identity></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)
