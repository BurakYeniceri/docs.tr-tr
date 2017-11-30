---
title: "&lt;Enforcefıpspolicy&gt; öğesi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- enforceFIPSPolicy element
- FIPS
- <enforceFIPSPolicy> element
- Federal Information Processing Standards (FIPS)
ms.assetid: c35509c4-35cf-43c0-bb47-75e4208aa24e
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9bd593c17d752b35919985aad37f675c62e6ce34
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ltenforcefipspolicygt-element"></a><span data-ttu-id="4092b-102">&lt;Enforcefıpspolicy&gt; öğesi</span><span class="sxs-lookup"><span data-stu-id="4092b-102">&lt;enforceFIPSPolicy&gt; Element</span></span>
<span data-ttu-id="4092b-103">Şifreleme algoritmaları Federal Bilgi işleme standartları (FIPS ile) uymalıdır bir bilgisayar yapılandırmasını gereksinim zorlanıp zorlanmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4092b-103">Specifies whether to enforce a computer configuration requirement that cryptographic algorithms must comply with the Federal Information Processing Standards (FIPS).</span></span>  
  
 <span data-ttu-id="4092b-104">\<Yapılandırma > öğesi</span><span class="sxs-lookup"><span data-stu-id="4092b-104">\<configuration> Element</span></span>  
<span data-ttu-id="4092b-105">\<çalışma zamanı > öğesi</span><span class="sxs-lookup"><span data-stu-id="4092b-105">\<runtime> Element</span></span>  
<span data-ttu-id="4092b-106">\<Enforcefıpspolicy > öğesi</span><span class="sxs-lookup"><span data-stu-id="4092b-106">\<enforceFIPSPolicy> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4092b-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="4092b-107">Syntax</span></span>  
  
```xml  
<enforceFIPSPolicy enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4092b-108">Öznitelikler ve Öğeler</span><span class="sxs-lookup"><span data-stu-id="4092b-108">Attributes and Elements</span></span>  
 <span data-ttu-id="4092b-109">Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4092b-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4092b-110">Öznitelikler</span><span class="sxs-lookup"><span data-stu-id="4092b-110">Attributes</span></span>  
  
|<span data-ttu-id="4092b-111">Öznitelik</span><span class="sxs-lookup"><span data-stu-id="4092b-111">Attribute</span></span>|<span data-ttu-id="4092b-112">Açıklama</span><span class="sxs-lookup"><span data-stu-id="4092b-112">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4092b-113">Etkin</span><span class="sxs-lookup"><span data-stu-id="4092b-113">enabled</span></span>|<span data-ttu-id="4092b-114">Gerekli öznitelik.</span><span class="sxs-lookup"><span data-stu-id="4092b-114">Required attribute.</span></span><br /><br /> <span data-ttu-id="4092b-115">Şifreleme algoritmaları FIPS ile uyumlu bir bilgisayar yapılandırma gereksinim zorlama etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4092b-115">Specifies whether to enable the enforcement of a computer configuration requirement that cryptographic algorithms must be compliant with FIPS.</span></span>|  
  
## <a name="enabled-attribute"></a><span data-ttu-id="4092b-116">etkin Öznitelik</span><span class="sxs-lookup"><span data-stu-id="4092b-116">enabled Attribute</span></span>  
  
|<span data-ttu-id="4092b-117">Değer</span><span class="sxs-lookup"><span data-stu-id="4092b-117">Value</span></span>|<span data-ttu-id="4092b-118">Açıklama</span><span class="sxs-lookup"><span data-stu-id="4092b-118">Description</span></span>|  
|-----------|-----------------|  
|`true`|<span data-ttu-id="4092b-119">Bu gereksinim, bilgisayarınızı FIPS uyumlu olacak şekilde şifreleme algoritmaları gerektirecek şekilde yapılandırılmışsa, zorlanır.</span><span class="sxs-lookup"><span data-stu-id="4092b-119">If your computer is configured to require cryptographic algorithms to be FIPS compliant, that requirement is enforced.</span></span> <span data-ttu-id="4092b-120">Sınıf oluşturucuları FIPS ile uyumlu olmayan bir algoritma uyguluyorsa veya `Create` o bilgisayarda çalıştırdığınızda bu sınıf için yöntemleri throw özel durumları.</span><span class="sxs-lookup"><span data-stu-id="4092b-120">If a class implements an algorithm that is not compliant with FIPS, the constructors or `Create` methods for that class throw exceptions when they are run on that computer.</span></span> <span data-ttu-id="4092b-121">Bu varsayılandır.</span><span class="sxs-lookup"><span data-stu-id="4092b-121">This is the default.</span></span>|  
|`false`|<span data-ttu-id="4092b-122">Uygulama tarafından kullanılan şifreleme algoritmalarını bağımsız olarak bilgisayar yapılandırması FIPS ile uyumlu olmasını gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="4092b-122">Cryptographic algorithms that are used by the application are not required to be compliant with FIPS, regardless of computer configuration.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4092b-123">Alt Öğeler</span><span class="sxs-lookup"><span data-stu-id="4092b-123">Child Elements</span></span>  
 <span data-ttu-id="4092b-124">Yok.</span><span class="sxs-lookup"><span data-stu-id="4092b-124">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4092b-125">Üst Öğeler</span><span class="sxs-lookup"><span data-stu-id="4092b-125">Parent Elements</span></span>  
  
|<span data-ttu-id="4092b-126">Öğe</span><span class="sxs-lookup"><span data-stu-id="4092b-126">Element</span></span>|<span data-ttu-id="4092b-127">Açıklama</span><span class="sxs-lookup"><span data-stu-id="4092b-127">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="4092b-128">Her yapılandırma dosyasında yer alan ve ortak dil çalışma zamanı ve .NET Framework uygulamaları tarafından kullanılan kök öğe.</span><span class="sxs-lookup"><span data-stu-id="4092b-128">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="4092b-129">Derleme bağlama ve atık toplama hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="4092b-129">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4092b-130">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="4092b-130">Remarks</span></span>  
 <span data-ttu-id="4092b-131">.NET Framework 2.0 ile başlayarak, şifreleme algoritmaları uygulayan sınıflar oluşturulmasını bilgisayarı yapılandırma tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="4092b-131">Starting with the .NET Framework 2.0, the creation of classes that implement cryptographic algorithms is controlled by the configuration of the computer.</span></span> <span data-ttu-id="4092b-132">Bilgisayar algoritmaları FIPS ile uyumlu olmasını gerektirecek şekilde yapılandırılmış ve bir sınıf FIPS ile uyumlu olmayan bir algoritma uygular, bu sınıfın örneğini oluşturma girişimi herhangi bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4092b-132">If the computer is configured to require algorithms to be compliant with FIPS, and a class implements an algorithm that is not compliant with FIPS, any attempt to create an instance of that class throws an exception.</span></span> <span data-ttu-id="4092b-133">Oluşturucular throw bir <xref:System.InvalidOperationException> özel durumu ve `Create` yöntemleri throw bir <xref:System.Reflection.TargetInvocationException> özel durum ile bir iç <xref:System.InvalidOperationException> özel durum.</span><span class="sxs-lookup"><span data-stu-id="4092b-133">Constructors throw an <xref:System.InvalidOperationException> exception, and `Create` methods throw a <xref:System.Reflection.TargetInvocationException> exception with an inner <xref:System.InvalidOperationException> exception.</span></span>  
  
 <span data-ttu-id="4092b-134">Uygulamanız, yapılandırmaları FIPS ile uyumlu olmasını gerektir bilgisayarlarda çalışan ve uygulamanızın FIPS ile uyumlu olmayan bir algoritma kullanıyorsa, bu öğe, yapılandırma dosyanızda gelen ortak dil çalışma zamanı (CLR) önlemek için kullanabilirsiniz FIPS uyumluluk zorlama.</span><span class="sxs-lookup"><span data-stu-id="4092b-134">If your application runs on computers whose configurations require compliance with FIPS, and your application uses an algorithm that is not compliant with FIPS, you can use this element in your configuration file to prevent the common language runtime (CLR) from enforcing FIPS compliance.</span></span> <span data-ttu-id="4092b-135">Bu öğe sunulmuştur [!INCLUDE[net_v20SP1_long](../../../../../includes/net-v20sp1-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4092b-135">This element was introduced in the [!INCLUDE[net_v20SP1_long](../../../../../includes/net-v20sp1-long-md.md)].</span></span>  
  
## <a name="example"></a><span data-ttu-id="4092b-136">Örnek</span><span class="sxs-lookup"><span data-stu-id="4092b-136">Example</span></span>  
 <span data-ttu-id="4092b-137">Aşağıdaki örnek, FIPS uyumluluğu zorlamayı CLR önlemek gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4092b-137">The following example shows how to prevent the CLR from enforcing FIPS compliance.</span></span>  
  
```xml  
<configuration>  
    <runtime>  
        <enforceFIPSPolicy enabled="false"/>  
    </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="4092b-138">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4092b-138">See Also</span></span>  
 [<span data-ttu-id="4092b-139">Çalışma Zamanı Ayarları Şeması</span><span class="sxs-lookup"><span data-stu-id="4092b-139">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="4092b-140">Yapılandırma dosyası şeması</span><span class="sxs-lookup"><span data-stu-id="4092b-140">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="4092b-141">Şifreleme modeli</span><span class="sxs-lookup"><span data-stu-id="4092b-141">Cryptography Model</span></span>](../../../../../docs/standard/security/cryptography-model.md)