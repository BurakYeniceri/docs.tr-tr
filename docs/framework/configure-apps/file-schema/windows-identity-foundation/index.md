---
title: Windows Identity Foundation Yapılandırma Şeması
ms.date: 03/30/2017
ms.assetid: 4d4f6d76-49a5-4bad-b345-097b2e2844e9
author: BrucePerlerMS
manager: mbaldwin
ms.openlocfilehash: 8881339a5dcf21df17e7200847fc46854ead17e3
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2018
ms.locfileid: "43468449"
---
# <a name="windows-identity-foundation-configuration-schema"></a>Windows Identity Foundation Yapılandırma Şeması
Bu bölümdeki konularda, Windows Identity Foundation (WIF) yapılandırma şeması hakkında bilgi sağlar. Ayrıca bir uygulamayı WIF sınıfları framework tarafından kullanıma sunulan aracılığıyla kullanmak için yapılandırabilirsiniz. Bu sınıfları, ilgili öğeleri şemada kabul bölümlerde belirtilmiştir. WIF yapılandırma şeması tarafından kullanıma sunulan yapısı aşağıdaki gösterildiği temel XML etiketi. Öznitelikleri göz ardı edilir. Vurgulanan açıklamaları şema ana bileşenleri gösterir.  
  
```xml  
<system.identityModel>  
    <!-- Service Configuration -->  
    <identityConfiguration>  
        <caches>  
            <sessionSecurityTokenCache />  
            <tokenReplayCache />  
        </caches>  
  
        <certificateValidation>  
            <certificateValidator />   
        </certificateValidation>  
  
        <claimsAuthenticationManager />  
  
        <claimsAuthorizationManager>  
            <optionalConfigurationElement>  
        </claimsAuthorizationManager>  
  
        <claimTypeRequired>  
            <claimType />   
        </claimTypeRequired>  
  
        <tokenReplayDetection />  
  
        <!-- Security Token Handler Collection Configuration -->  
        <securityTokenHandlers>  
            <add>  
                <!-- Can take an optional configuration element which can be one of  
                     the following or a custom element -->  
                <samlSecurityTokenHandlerRequirement>  
                    <nameClaimType>  
                    <roleClaimType>   
                </samlSecurityTokenHandlerRequirement>  
  
                <sessionSecurityTokenHandlerRequirement />  
                <x509SecurityTokenHandlerRequirement />  
                <userNameSecurityTokenHandlerRequirement />  
            </add>  
            <clear />  
            <remove />  
            <securityTokenHandlerConfiguration>  
                <audienceUris>  
                    <add>  
                    <clear>  
                    <remove>  
                </audienceUris>  
  
                <caches>  
                    <sessionSecurityTokenCache />  
                    <tokenReplayCache />  
                </caches>  
  
                <certificateValidation>  
                    <certificateValidator>   
                </certificateValidation>  
  
                <issuerNameRegistry>  
                    <!-- Can take an optional configuration element which can be   
                         the <trustedIssuers> element to configure a configuration-based  
                         issuer name registry or can be a custom element -->  
                    <trustedIssuers>  
                        <add>  
                        <clear>  
                        <remove>  
                    </trustedIssuers>  
                </issuerNameRegistry>  
  
                <issuerTokenResolver />  
                <serviceTokenResolver />  
                <tokenReplayDetection />  
            </securityTokenHandlerConfiguration>  
        </securityTokenHandlers>  
    </identityConfiguration>  
</system.identityModel>  
  
<system.identityModel.services>  
    <!-- Federation Authentication Configuration -->  
    <federatedAuthentication>  
        <cookieHandler>  
            <chunkedCookieHandler />  
            <customCookieHandler />  
        </cookieHandler>  
  
        <serviceCertificate>  
            <certificateReference>  
        </serviceCertificate>  
  
        <wsFederation />  
    </federatedAuthentication>  
</system.identityModel.services>  
```  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [\<System.IdentityModel >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/system-identitymodel.md) seçenekleri uygulamalarda WIF etkinleştirme yapılandırması sağlar.  
  
 [\<System.IdentityModel.Services >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/system-identitymodel-services.md) WIF kullanarak pasif Federasyon yapılandırması sağlar. Oturum kimlik doğrulama Modülü (SAM) ve şirket dışı kimlik doğrulaması Modülü (WSFAM) yapılandırır.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Yapılandırma, yönetim ve Yönetimi](https://msdn.microsoft.com/library/1e03c389-de2c-4096-aaff-86b087e1bea0) yapılandırmak ve WIF uygulamaları ve hizmetleri yönetmek nasıl açıklar.
