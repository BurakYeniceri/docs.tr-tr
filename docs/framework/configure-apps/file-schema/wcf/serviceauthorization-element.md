---
title: "&lt;serviceAuthorization&gt; öğesi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 18cddad5-ddcb-4839-a0ac-1d6f6ab783ca
caps.latest.revision: "26"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: cdbe676fa73c040737c947902d64b2c0e689e2a9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ltserviceauthorizationgt-element"></a><span data-ttu-id="0c6f5-102">&lt;serviceAuthorization&gt; öğesi</span><span class="sxs-lookup"><span data-stu-id="0c6f5-102">&lt;serviceAuthorization&gt; element</span></span>
<span data-ttu-id="0c6f5-103">Hizmet işlemlerine erişimi yetkilendirme ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-103">Specifies settings that authorize access to service operations</span></span>  
  
 <span data-ttu-id="0c6f5-104">\<Sistem. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="0c6f5-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="0c6f5-105">\<davranışları ></span><span class="sxs-lookup"><span data-stu-id="0c6f5-105">\<behaviors></span></span>  
<span data-ttu-id="0c6f5-106">\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="0c6f5-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="0c6f5-107">\<davranışı ></span><span class="sxs-lookup"><span data-stu-id="0c6f5-107">\<behavior></span></span>  
<span data-ttu-id="0c6f5-108">\<serviceAuthorization ></span><span class="sxs-lookup"><span data-stu-id="0c6f5-108">\<serviceAuthorization></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0c6f5-109">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0c6f5-109">Syntax</span></span>  
  
```xml  
<serviceAuthorization  
     impersonateCallerForAllOperations="Boolean"  
      principalPermissionMode="None/UseWindowsGroups/UseAspNetRoles/Custom"  
      roleProviderName="String"  
      serviceAuthorizationManagerType="String" />  
      <authorizationPolicies>  
         <add policyType="String" />  
      </authorizationPolicies>  
</serviceAuthorization>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="0c6f5-110">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="0c6f5-110">Attributes and Elements</span></span>  
 <span data-ttu-id="0c6f5-111">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="0c6f5-112">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="0c6f5-112">Attributes</span></span>  
  
|<span data-ttu-id="0c6f5-113">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="0c6f5-113">Attribute</span></span>|<span data-ttu-id="0c6f5-114">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0c6f5-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="0c6f5-115">impersonateCallerForAllOperations</span><span class="sxs-lookup"><span data-stu-id="0c6f5-115">impersonateCallerForAllOperations</span></span>|<span data-ttu-id="0c6f5-116">Hizmetindeki tüm işlemleri çağıran kimliğine bürünmek olmadığını belirten bir Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-116">A Boolean value that specifies if all the operations in the service impersonate the caller.</span></span> <span data-ttu-id="0c6f5-117">Varsayılan, `false` değeridir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-117">The default is `false`.</span></span><br /><br /> <span data-ttu-id="0c6f5-118">Belirli bir hizmet işlemine arayan taklit ettiğinde, iş parçacığı içeriği belirtilen hizmet yürütmeden önce çağıran bağlamına anahtarlanır.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-118">When a specific service operation impersonates the caller, the thread context is switched to the caller context before executing the specified service.</span></span>|  
|<span data-ttu-id="0c6f5-119">principalPermissionMode</span><span class="sxs-lookup"><span data-stu-id="0c6f5-119">principalPermissionMode</span></span>|<span data-ttu-id="0c6f5-120">Sunucu üzerinde işlemler gerçekleştirmek için kullanılan sorumluyu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-120">Sets the principal used to carry out operations on the server.</span></span> <span data-ttu-id="0c6f5-121">Değerler aşağıdakileri içerir:</span><span class="sxs-lookup"><span data-stu-id="0c6f5-121">Values include the following:</span></span><br /><br /> <span data-ttu-id="0c6f5-122">-Yok</span><span class="sxs-lookup"><span data-stu-id="0c6f5-122">-   None</span></span><br /><span data-ttu-id="0c6f5-123">-UseWindowsGroups</span><span class="sxs-lookup"><span data-stu-id="0c6f5-123">-   UseWindowsGroups</span></span><br /><span data-ttu-id="0c6f5-124">-UseAspNetRoles</span><span class="sxs-lookup"><span data-stu-id="0c6f5-124">-   UseAspNetRoles</span></span><br /><span data-ttu-id="0c6f5-125">-Özel</span><span class="sxs-lookup"><span data-stu-id="0c6f5-125">-   Custom</span></span><br /><br /> <span data-ttu-id="0c6f5-126">UseWindowsGroups varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-126">The default value is UseWindowsGroups.</span></span> <span data-ttu-id="0c6f5-127">Değer <xref:System.ServiceModel.Description.PrincipalPermissionMode>.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-127">The value is of type <xref:System.ServiceModel.Description.PrincipalPermissionMode>.</span></span> <span data-ttu-id="0c6f5-128">Bu öznitelik kullanma hakkında daha fazla bilgi için bkz: [nasıl yapılır: PrincipalPermissionAttribute sınıfı ile erişimi kısıtla](../../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md).</span><span class="sxs-lookup"><span data-stu-id="0c6f5-128">For more information on using this attribute, see [How to: Restrict Access with the PrincipalPermissionAttribute Class](../../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md).</span></span>|  
|<span data-ttu-id="0c6f5-129">roleProviderName</span><span class="sxs-lookup"><span data-stu-id="0c6f5-129">roleProviderName</span></span>|<span data-ttu-id="0c6f5-130">Bir Windows Communication Foundation (WCF) uygulaması için rol bilgileri sağlayan rol sağlayıcısı adını belirten dize.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-130">A string that specifies the name of the role provider, which provides role information for a Windows Communication Foundation (WCF) application.</span></span> <span data-ttu-id="0c6f5-131">Varsayılan boş bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-131">The default is an empty string.</span></span>|  
|<span data-ttu-id="0c6f5-132">ServiceAuthorizationManagerType</span><span class="sxs-lookup"><span data-stu-id="0c6f5-132">ServiceAuthorizationManagerType</span></span>|<span data-ttu-id="0c6f5-133">Hizmet Yetkilendirme Yöneticisi'ni türünü içeren bir dize.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-133">A string containing the type of the service authorization manager.</span></span> <span data-ttu-id="0c6f5-134">Daha fazla bilgi için bkz. <xref:System.ServiceModel.ServiceAuthorizationManager>.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-134">For more information, see <xref:System.ServiceModel.ServiceAuthorizationManager>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="0c6f5-135">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="0c6f5-135">Child Elements</span></span>  
  
|<span data-ttu-id="0c6f5-136">Öğe</span><span class="sxs-lookup"><span data-stu-id="0c6f5-136">Element</span></span>|<span data-ttu-id="0c6f5-137">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0c6f5-137">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0c6f5-138">authorizationPolicies</span><span class="sxs-lookup"><span data-stu-id="0c6f5-138">authorizationPolicies</span></span>|<span data-ttu-id="0c6f5-139">Kullanılarak eklenebilir yetkilendirme ilkesi türleri koleksiyonunu içeren `add` anahtar sözcüğü.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-139">Contains a collection of authorization policy types, which can be added using the `add` keyword.</span></span> <span data-ttu-id="0c6f5-140">Her bir yetkilendirme ilkesi gereken tek bir içeren `policyType` bir dize özniteliği.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-140">Each authorization policy contains a single required `policyType` attribute that is a string.</span></span> <span data-ttu-id="0c6f5-141">Öznitelik, bir giriş talep kümesini bir dönüştürme talep başka bir dizi içine sağlayan bir yetkilendirme ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-141">The attribute specifies an authorization policy, which enables transformation of one set of input claims into another set of claims.</span></span> <span data-ttu-id="0c6f5-142">Erişim denetimi verilen veya reddedilen oturum tabanlı.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-142">Access control can be granted or denied based on that.</span></span> <span data-ttu-id="0c6f5-143">Daha fazla bilgi için bkz. <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-143">For more information, see <xref:System.ServiceModel.Configuration.AuthorizationPolicyTypeElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="0c6f5-144">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="0c6f5-144">Parent Elements</span></span>  
  
|<span data-ttu-id="0c6f5-145">Öğe</span><span class="sxs-lookup"><span data-stu-id="0c6f5-145">Element</span></span>|<span data-ttu-id="0c6f5-146">Açıklama</span><span class="sxs-lookup"><span data-stu-id="0c6f5-146">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="0c6f5-147">\<davranışı ></span><span class="sxs-lookup"><span data-stu-id="0c6f5-147">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="0c6f5-148">Bir hizmet davranışını için ayarlar koleksiyonu içerir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-148">Contains a collection of settings for the behavior of a service.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0c6f5-149">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="0c6f5-149">Remarks</span></span>  
 <span data-ttu-id="0c6f5-150">Bu bölümde, yetkilendirme, özel rol sağlayıcıları ve kimliğe bürünme etkileyen öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-150">This section contains elements affecting authorization, custom role providers, and impersonation.</span></span>  
  
 <span data-ttu-id="0c6f5-151">`principalPermissionMode` Özniteliği, korumalı bir yöntemin kullanılması, yetkilendirirken kullanmak için kullanıcı gruplarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-151">The `principalPermissionMode` attribute specifies the groups of users to use when authorizing use of a protected method.</span></span> <span data-ttu-id="0c6f5-152">Varsayılan değer `UseWindowsGroups` ve "Yöneticiler" veya "Kullanıcı" gibi Windows grupları için bir kaynağa erişmeye çalışırken bir kimlik aranır belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-152">The default value is `UseWindowsGroups` and specifies that Windows groups, such as "Administrators" or "Users," are searched for an identity trying to access a resource.</span></span> <span data-ttu-id="0c6f5-153">Ayrıca belirtebilirsiniz `UseAspNetRoles` altında yapılandırılmış bir özel rol sağlayıcıyı kullanacak şekilde \<system.web > aşağıdaki kodda gösterildiği gibi öğesi.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-153">You can also specify `UseAspNetRoles` to use a custom role provider that is configured under the \<system.web> element, as shown in the following code.</span></span>  
  
```xml  
<system.web>  
  <membership defaultProvider="SqlProvider"   
   userIsOnlineTimeWindow="15">  
     <providers>  
       <clear />  
       <add   
          name="SqlProvider"   
          type="System.Web.Security.SqlMembershipProvider"   
          connectionStringName="SqlConn"  
          applicationName="MembershipProvider"  
          enablePasswordRetrieval="false"  
          enablePasswordReset="false"  
          requiresQuestionAndAnswer="false"  
          requiresUniqueEmail="true"  
          passwordFormat="Hashed" />  
     </providers>  
   </membership>  
  <!-- Other configuration code not shown.-->  
</system.web>  
```  
  
 <span data-ttu-id="0c6f5-154">Aşağıdaki kodda gösterildiği `roleProviderName` ile kullanılan `principalPermissionMode` özniteliği.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-154">The following code shows the `roleProviderName` used with the `principalPermissionMode` attribute.</span></span>  
  
```xml  
<behaviors>  
   <behavior name="ServiceBehaviour">  
     <serviceAuthorization principalPermissionMode ="UseAspNetRoles"   
                           roleProviderName ="SqlProvider" />  
   </behavior>   
<!-- Other configuration code not shown. -->  
</behaviors>  
```  
  
 <span data-ttu-id="0c6f5-155">Bu yapılandırma öğesini kullanarak bir ayrıntılı örnek için bkz: [hizmet işlemlerine erişimi yetkilendirme](../../../../../docs/framework/wcf/samples/authorizing-access-to-service-operations.md) ve [yetkilendirme ilkesi](../../../../../docs/framework/wcf/samples/authorization-policy.md).</span><span class="sxs-lookup"><span data-stu-id="0c6f5-155">For a detailed example of using this configuration element, see [Authorizing Access to Service Operations](../../../../../docs/framework/wcf/samples/authorizing-access-to-service-operations.md) and [Authorization Policy](../../../../../docs/framework/wcf/samples/authorization-policy.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0c6f5-156">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="0c6f5-156">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceAuthorizationElement>  
 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>  
 [<span data-ttu-id="0c6f5-157">Güvenlik davranışları</span><span class="sxs-lookup"><span data-stu-id="0c6f5-157">Security Behaviors</span></span>](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [<span data-ttu-id="0c6f5-158">Hizmet işlemlerine erişimi yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="0c6f5-158">Authorizing Access to Service Operations</span></span>](../../../../../docs/framework/wcf/samples/authorizing-access-to-service-operations.md)  
 [<span data-ttu-id="0c6f5-159">Nasıl yapılır: bir hizmet için özel Yetkilendirme Yöneticisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c6f5-159">How to: Create a Custom Authorization Manager for a Service</span></span>](../../../../../docs/framework/wcf/extending/how-to-create-a-custom-authorization-manager-for-a-service.md)  
 [<span data-ttu-id="0c6f5-160">Nasıl yapılır: PrincipalPermissionAttribute sınıfı ile erişimi kısıtlama</span><span class="sxs-lookup"><span data-stu-id="0c6f5-160">How to: Restrict Access with the PrincipalPermissionAttribute Class</span></span>](../../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)  
 [<span data-ttu-id="0c6f5-161">Yetkilendirme İlkesi</span><span class="sxs-lookup"><span data-stu-id="0c6f5-161">Authorization Policy</span></span>](../../../../../docs/framework/wcf/samples/authorization-policy.md)