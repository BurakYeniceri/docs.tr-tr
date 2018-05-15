---
title: '&lt;authorizationPolicies&gt;'
ms.date: 03/30/2017
ms.assetid: 5b367489-54d7-408b-8f56-cb157dd68eaf
ms.openlocfilehash: 8e1bc702db899c4b0b3ee539fdc89cdda6c4cf10
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2018
---
# <a name="ltauthorizationpoliciesgt"></a><span data-ttu-id="13568-102">&lt;authorizationPolicies&gt;</span><span class="sxs-lookup"><span data-stu-id="13568-102">&lt;authorizationPolicies&gt;</span></span>
<span data-ttu-id="13568-103">Bu yapılandırma bölümü kullanılarak eklenebilir yetkilendirme ilkesi türleri koleksiyonunu içeren `add` anahtar sözcüğü.</span><span class="sxs-lookup"><span data-stu-id="13568-103">This configuration section contains a collection of authorization policy types, which can be added using the `add` keyword.</span></span> <span data-ttu-id="13568-104">Her bir yetkilendirme ilkesi gereken tek bir içeren `policyType` bir dize özniteliği.</span><span class="sxs-lookup"><span data-stu-id="13568-104">Each authorization policy contains a single required `policyType` attribute that is a string.</span></span> <span data-ttu-id="13568-105">Öznitelik, bir giriş talep kümesini bir dönüştürme talep başka bir dizi içine sağlayan bir yetkilendirme ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="13568-105">The attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="13568-106">Erişim denetimi verilen veya reddedilen oturum tabanlı.</span><span class="sxs-lookup"><span data-stu-id="13568-106">Access control can be granted or denied based on that.</span></span> <span data-ttu-id="13568-107">Bir yetkilendirme ilkesi nasıl çalıştığı hakkında daha fazla bilgi için bkz: <xref:System.IdentityModel.Policy.IAuthorizationPolicy> ve [yetkilendirme ilkesi](../../../../../docs/framework/wcf/samples/authorization-policy.md).</span><span class="sxs-lookup"><span data-stu-id="13568-107">For more information on how an authorization policy works, see <xref:System.IdentityModel.Policy.IAuthorizationPolicy> and [Authorization Policy](../../../../../docs/framework/wcf/samples/authorization-policy.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13568-108">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="13568-108">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement>  
 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior.ExternalAuthorizationPolicies%2A>  
 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>  
 <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>  
 <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement.AuthorizationPolicies%2A>  
 <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElementCollection>  
 <xref:System.IdentityModel.Policy.IAuthorizationPolicy>  
 [<span data-ttu-id="13568-109">Hizmet İşlemlerine Erişimi Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="13568-109">Authorizing Access to Service Operations</span></span>](../../../../../docs/framework/wcf/samples/authorizing-access-to-service-operations.md)  
 [<span data-ttu-id="13568-110">Nasıl yapılır: Bir Hizmet için Özel Yetkilendirme Yöneticisi Oluşturma</span><span class="sxs-lookup"><span data-stu-id="13568-110">How to: Create a Custom Authorization Manager for a Service</span></span>](../../../../../docs/framework/wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md)  
 [<span data-ttu-id="13568-111">\<ekleme ></span><span class="sxs-lookup"><span data-stu-id="13568-111">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-authorizationpolicies.md)  
 [<span data-ttu-id="13568-112">Yetkilendirme İlkesi</span><span class="sxs-lookup"><span data-stu-id="13568-112">Authorization Policy</span></span>](../../../../../docs/framework/wcf/samples/authorization-policy.md)
