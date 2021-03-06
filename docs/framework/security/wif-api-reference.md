---
title: WIF API Başvurusu
ms.date: 03/30/2017
ms.assetid: a027d902-9314-4bfd-b172-4e81847b1d68
author: BrucePerlerMS
ms.openlocfilehash: 0cd373ae3fd5acb1650f0d8614b34c5d19cf9016
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47195491"
---
# <a name="wif-api-reference"></a>WIF API Başvurusu
Windows Identity Foundation (WIF) sınıfları aşağıdaki derlemeler arasında bölmek: `mscorlib` (mscorlib.dll) `System.IdentityModel` (System.IdentityModel.dll) `System.IdentityModel.Services` (System.IdentityModel.Services.dll) ve `System.ServiceModel` () System.ServiceModel.dll). Bu konuda WIF ad alanları ve kısa açıklamaları sınıfların her ad uzayını içeren bağlantılar sağlar.  
  
> [!IMPORTANT]
>  Aşağıdaki `System.IdentityModel` WCF beyana dayalı kimlik modeli uygulayan sınıflar ad alanlarında bulunur: <xref:System.IdentityModel.Claims?displayProperty=nameWithType>, <xref:System.IdentityModel.Policy?displayProperty=nameWithType>, ve <xref:System.IdentityModel.Selectors?displayProperty=nameWithType>. .NET Framework 4.5 ile başlayarak, WCF beyana dayalı kimlik modelinin yerini WIF almıştır. Sınıfları bu üç ad alanı üzerinde WIF tabanlı çözümler oluştururken kullanmamanız gerekir.  
  
 <xref:System.IdentityModel?displayProperty=nameWithType>  
 Tanımlama bilgisi dönüşümler ve güvenlik belirteci hizmetlerine özel XML sözlük okuyucularına temsil eden sınıfları içerir.  
  
 <xref:System.IdentityModel.Configuration?displayProperty=nameWithType>  
 Uygulamalar ve Windows Identity Foundation (WIF) kullanılarak oluşturulan hizmetler için yapılandırma sağlayan sınıflar içerir. Bu ad alanındaki sınıflar ayarlara altında [ \<identityConfiguration >](../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md) öğesi.  
  
 <xref:System.IdentityModel.Metadata?displayProperty=nameWithType>  
 Bir Federasyon meta veri belgesinin öğelerini temsil eden sınıfları içerir.  
  
 <xref:System.IdentityModel.Protocols.WSTrust?displayProperty=nameWithType>  
 WS-Trust yapıları temsil eden sınıfları içerir.  
  
 <xref:System.IdentityModel.Services?displayProperty=nameWithType>  
 Pasif (WS-Federation) senaryolarında kullanılan sınıfları içerir. Ayarlar altında temsil eden bazı sınıflar da içerir [ \<System.IdentityModel.Services >](../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/system-identitymodel-services.md) öğesi. Bu öğe ayarlarında WS-Federasyon uygulamaları için yapılandırma. `System.IdentityModel.Services.Configuration` Ad alanı, çoğu WS-Federasyon yapılandırmak için kullanılan sınıfları içerir.  
  
 <xref:System.IdentityModel.Services.Configuration?displayProperty=nameWithType>  
 WIF WS-Federasyon protokolünü kullanan uygulamalar için yapılandırma sağlayan sınıflar içerir. Bu ad alanındaki sınıflar ayarlara altında [ \<System.IdentityModel.Services >](../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/system-identitymodel-services.md) öğesi. `System.IdentityModel.Services` Ad alanı, WS-Federasyon yapılandırmak için kullanılan bazı sınıflar da içerir.  
  
 <xref:System.IdentityModel.Services.Tokens?displayProperty=nameWithType>  
 Web grubu senaryoları için özel güvenlik belirteci işleyicileri içerir.  
  
 <xref:System.IdentityModel.Tokens?displayProperty=nameWithType>  
 Güvenlik belirteçleri, güvenlik belirteci işleyicileri ve diğer güvenlik belirteci yapılarını temsil eden sınıfları içerir.  
  
 <xref:System.Security.Claims?displayProperty=nameWithType>  
 Talepler, beyana dayalı kimlikler, talep tabanlı ilkeleri ve diğer beyana dayalı kimlik modeli yapıları temsil eden sınıfları içerir.  
  
 <xref:System.ServiceModel.Security?displayProperty=nameWithType>  
 WCF sözleşmeleri, Kanallar, hizmet konakları ve active (WS-Trust) senaryolarında kullanılan diğer yapıları temsil eden sınıfları içerir. Bu ad alanı, Windows Communication Foundation (WCF) için özeldir ve WIF tarafından kullanılmaz sınıflar da içerir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WIF Yapılandırma Başvurusu](../../../docs/framework/security/wif-configuration-reference.md)  
 [WIF 3.5 ile WIF 4.5 Arasında Ad Alanı Eşleme](../../../docs/framework/security/namespace-mapping-between-wif-3-5-and-wif-4-5.md)
