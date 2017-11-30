---
title: "&lt;serviceCredentials&gt; için &lt;windowsAuthentication&gt;"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e0709473-0997-4de3-8f49-783527309a48
caps.latest.revision: "9"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: dbc4c3413213aa36468fde6e84671de0e0a31c2f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ltwindowsauthenticationgt-of-ltservicecredentialsgt"></a><span data-ttu-id="3b200-102">&lt;serviceCredentials&gt; için &lt;windowsAuthentication&gt;</span><span class="sxs-lookup"><span data-stu-id="3b200-102">&lt;windowsAuthentication&gt; of &lt;serviceCredentials&gt;</span></span>
<span data-ttu-id="3b200-103">Bir Windows hizmeti kimlik bilgileri ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b200-103">Specifies the settings of a Windows service credential.</span></span>  
  
 <span data-ttu-id="3b200-104">\<Sistem. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="3b200-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="3b200-105">\<davranışları ></span><span class="sxs-lookup"><span data-stu-id="3b200-105">\<behaviors></span></span>  
<span data-ttu-id="3b200-106">\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="3b200-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="3b200-107">\<davranışı ></span><span class="sxs-lookup"><span data-stu-id="3b200-107">\<behavior></span></span>  
<span data-ttu-id="3b200-108">\<serviceCredentials ></span><span class="sxs-lookup"><span data-stu-id="3b200-108">\<serviceCredentials></span></span>  
<span data-ttu-id="3b200-109">\<windowsAuthentication ></span><span class="sxs-lookup"><span data-stu-id="3b200-109">\<windowsAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b200-110">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3b200-110">Syntax</span></span>  
  
```xml  
<windowsAuthentication  
      allowAnonymousLogons="Boolean"  
      includeWindowsGroups="Boolean" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3b200-111">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="3b200-111">Attributes and Elements</span></span>  
 <span data-ttu-id="3b200-112">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3b200-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3b200-113">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="3b200-113">Attributes</span></span>  
  
|<span data-ttu-id="3b200-114">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="3b200-114">Attribute</span></span>|<span data-ttu-id="3b200-115">Açıklama</span><span class="sxs-lookup"><span data-stu-id="3b200-115">Description</span></span>|  
|---------------|-----------------|  
|`includeWindowsGroups`|<span data-ttu-id="3b200-116">Sistem güvenlik bağlamında Windows grupları içerip içermeyeceğini belirten isteğe bağlı Boole öznitelik.</span><span class="sxs-lookup"><span data-stu-id="3b200-116">An optional Boolean attribute that specifies whether the system includes Windows groups in the security context.</span></span> <span data-ttu-id="3b200-117">Varsayılan, `true` değeridir.</span><span class="sxs-lookup"><span data-stu-id="3b200-117">The default is `true`.</span></span><br /><br /> <span data-ttu-id="3b200-118">Bu öznitelik ayarını `true` bir tam Grup genişletme sonuçları gibi bir performans etkisi olur.</span><span class="sxs-lookup"><span data-stu-id="3b200-118">Setting this attribute to `true` has a performance impact as it results in a full-group expansion.</span></span> <span data-ttu-id="3b200-119">Bu öznitelik ayarlanırsa `false` gruplarının listesini oluşturmak ihtiyacınız yoksa bir kullanıcının ait olduğu.</span><span class="sxs-lookup"><span data-stu-id="3b200-119">Set this attribute to `false` if you do not need to establish the list of groups a user belongs to.</span></span>|  
|`allowAnonymousLogons`|<span data-ttu-id="3b200-120">Anonim, kimliği doğrulanmamış arayanlara izin verilip verilmeyeceğini belirten isteğe bağlı Boole özniteliği.</span><span class="sxs-lookup"><span data-stu-id="3b200-120">An optional Boolean attribute that specifies whether anonymous, unauthenticated callers are allowed.</span></span> <span data-ttu-id="3b200-121">Varsayılan, `false` değeridir.</span><span class="sxs-lookup"><span data-stu-id="3b200-121">The default is `false`.</span></span><br /><br /> <span data-ttu-id="3b200-122">Zaman `clientCredentialType` özniteliği bağlaması `Windows`, sistem anonim arayanlara izin vermiyor.</span><span class="sxs-lookup"><span data-stu-id="3b200-122">When the `clientCredentialType` attribute of a binding is set to `Windows`, the system does not allow anonymous callers.</span></span> <span data-ttu-id="3b200-123">Bu, yalnızca etki alanı veya çalışma grubu kimliği doğrulanmış gelir arayanlar sisteme erişmesine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="3b200-123">This means that only domain or workgroup authenticated callers are allowed to access the system.</span></span> <span data-ttu-id="3b200-124">Bu öznitelik kullanarak bu davranışı geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b200-124">You can override this behavior by using this attribute.</span></span><br /><br /> <span data-ttu-id="3b200-125">Bu ayar çok dikkatli kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b200-125">Use this setting with extreme caution.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3b200-126">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="3b200-126">Child Elements</span></span>  
 <span data-ttu-id="3b200-127">Yok.</span><span class="sxs-lookup"><span data-stu-id="3b200-127">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3b200-128">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="3b200-128">Parent Elements</span></span>  
  
|<span data-ttu-id="3b200-129">Öğe</span><span class="sxs-lookup"><span data-stu-id="3b200-129">Element</span></span>|<span data-ttu-id="3b200-130">Açıklama</span><span class="sxs-lookup"><span data-stu-id="3b200-130">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="3b200-131">\<serviceCredentials ></span><span class="sxs-lookup"><span data-stu-id="3b200-131">\<serviceCredentials></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/servicecredentials.md)|<span data-ttu-id="3b200-132">Hizmet ve istemci kimlik doğrulama ile ilgili ayarları kimlik doğrulaması kullanmak için kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b200-132">Specifies the credential to be used in authenticating the service, and the client credential validation-related settings.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3b200-133">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="3b200-133">Remarks</span></span>  
 <span data-ttu-id="3b200-134">Anonim Windows kullanıcıları ayarlayarak erişimine izin verilip verilmeyeceğini belirtmek için bu öğeyi kullanın `allowAnonymousLogons` özniteliği.</span><span class="sxs-lookup"><span data-stu-id="3b200-134">Use this element to specify whether to allow anonymous Windows users access by setting the `allowAnonymousLogons` attribute.</span></span> <span data-ttu-id="3b200-135">Ayrıca kullanıcıların ait olduğu grubu bilgilerini ayarlayarak yetkilendirme bağlamı içinde dahil edilip edilmeyeceğini belirtebilirsiniz `includeWindowsGroups` özniteliği.</span><span class="sxs-lookup"><span data-stu-id="3b200-135">You can also specify whether to include group information to which users belong in the AuthorizationContext by setting the `includeWindowsGroups` attribute.</span></span> <span data-ttu-id="3b200-136">Bu ayarlanırsa `true` (varsayılan ayar), hizmet istemcinin ait olduğu Windows gruplarını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b200-136">If it is set to `true` (the default setting), the service can determine the Windows groups to which the client belongs.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b200-137">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="3b200-137">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.WindowsServiceElement>  
 <xref:System.ServiceModel.Configuration.ServiceCredentialsElement.WindowsAuthentication%2A>  
 <xref:System.ServiceModel.Description.ServiceCredentials.WindowsAuthentication%2A>  
 <xref:System.ServiceModel.Security.WindowsServiceCredential>
