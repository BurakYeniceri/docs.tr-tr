---
title: '&lt;msmqIntegrationBinding&gt; &lt;taşıma&gt;'
ms.date: 03/30/2017
ms.assetid: 054579e3-7fdd-47df-99ca-952706ba5c8e
ms.openlocfilehash: 8f6fcb19f67caba34334b649cc2e452c9e10bf93
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/06/2018
ms.locfileid: "48845618"
---
# <a name="lttransportgt-of-ltmsmqintegrationbindinggt"></a>&lt;msmqIntegrationBinding&gt; &lt;taşıma&gt;
Message Queuing tümleştirme taşıma güvenlik ayarlarını tanımlar.  
  
 \<system.ServiceModel>  
\<bağlamaları >  
msmqIntegrationBinding  
\<bağlama >  
\<Güvenlik >  
\<taşıma >  
  
## <a name="syntax"></a>Sözdizimi  
  
```xml  
<security>  
    <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"  
        msmqEncryptionAlgorithm="RC4Stream/AES"  
        msmqProtectionLevel="None/Sign/EncryptAndSign"  
        msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />  
</security>  
```  
  
## <a name="attributes-and-elements"></a>Öznitelikler ve Öğeler  
 Öznitelikler, alt ve üst öğeler aşağıdaki bölümlerde açıklanmaktadır.  
  
### <a name="attributes"></a>Öznitelikler  
  
|Öznitelik|Açıklama|  
|---------------|-----------------|  
|`msmqAuthenticationMode`|İletinin MSMQ taşıma tarafından nasıl doğrulacağını belirtir. Bu ayarlanırsa `None`, değerini `msmqProtectionLevel` özniteliği de ayarlanması gerekir `None`.<br /><br /> Geçerli değerler şunlardır:<br /><br /> -Hiçbiri: Kimlik doğrulaması yok.<br />-WindowsDomain: SID iletiyle ilişkili için X.509 sertifikası almak için Active Directory kimlik doğrulama mekanizması kullanır. Bu, daha sonra kullanıcı emin olmak için ACL kuyruğun kuyruğa yazmak için yeterli izne sahip olmadığını denetlemek için kullanılır.<br />-Sertifika: Kanal sertifikayı sertifika deposundan alır.<br /><br /> WindowsDomain varsayılan değerdir. Bu öznitelik türünde <xref:System.ServiceModel.MsmqAuthenticationMode>.|  
|`msmqEncryptionAlgorithm`|Etkin ileti şifreleme için iletileri ileti sıra yöneticileri arasında transfer ederken kullanılan algoritmayı belirtir. Geçerli değerler şunlardır:<br /><br /> -RC4Stream<br />-AES<br /><br /> RC4Stream varsayılan değerdir. Bu öznitelik türünde <xref:System.ServiceModel.MsmqEncryptionAlgorithm>.|  
|`msmqProtectionLevel`|İletinin MSMQ taşıma düzeyinde güvenliği nasıl belirtir. İleti bütünlüğü hem takası EncryptAndSign sağlar ancak şifreleme ileti bütünlüğü sağlar; diğer bir deyişle, ileti gönderen gerçekten gelir ve gönderen kim kendisinin kendisinin olduğunu söylüyor.<br /><br /> -Geçerli değerler şunlardır:<br />-Hiçbiri: Koruma yok.<br />-Oturum: İletileri imzalanmıştır.<br />-EncryptAndSign: İletileri şifrelenir ve imzalanmış.<br /><br /> Oturum varsayılan değerdir. Bu öznitelik ProtectionLevel türüdür.|  
|`msmqSecureHashAlgorithm`|-İmzanın bir parçası Özet işlem alanında kullanılan algoritmayı belirtir. Geçerli değerler şunlardır:<br />-MD5<br />-   SHA1<br />-   SHA256<br />-   SHA512<br /><br /> Varsayılan, SHA1 değeridir. Bu öznitelik türünde <xref:System.ServiceModel.MsmqSecureHashAlgorithm>.|  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-elements"></a>Üst Öğeler  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<Güvenlik >](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-basichttpbinding.md)|MSMQ bağlama için güvenlik ayarlarını tanımlar.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu öğe, Message Queuing tümleştirme taşıma güvenlik ayarlarını saklar. Ayarları Message Queuing tümleştirme ve sıraya alınan taşımalar için aynıdır. Kimlik doğrulama modu, şifreleme algoritması, güvenli karma algoritması ve koruma düzeyi ayarlamanıza olanak sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>  
 <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationSecurity.Transport%2A>  
 <xref:System.ServiceModel.Configuration.MsmqIntegrationSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.MsmqTransportSecurity>  
 [Hizmet ve İstemcileri Güvenli Hale Getirme](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [Hizmet ve İstemcileri Güvenli Hale Getirme](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [Bağlamalar](../../../../../docs/framework/wcf/bindings.md)  
 [Sistem Tarafından Sağlanan Bağlamaları Yapılandırma](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [Hizmetler ve İstemcileri Yapılandırmak için Bağlamaları Kullanma](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [\<bağlama >](../../../../../docs/framework/misc/binding.md)
