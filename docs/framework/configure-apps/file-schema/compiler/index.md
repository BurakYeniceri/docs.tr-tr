---
title: Derleyici ve Dil Sağlayıcısı Ayarları Şeması
ms.date: 03/30/2017
helpviewer_keywords:
- configuration settings [.NET Framework], compilers
- compiler configuration elements, schema
- compiler configuration elements
- language providers
- compiler configuration settings, schema
- configuration schema [.NET Framework], compiler settings
- language providers, settings schema
- compiler configuration settings
ms.assetid: c020b139-8699-4f0d-9ac9-70d0c5b2a8c8
author: mcleblanc
ms.author: markl
ms.openlocfilehash: 8992c9e47e2b62e90191a67fc7353e138502ebf1
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50185673"
---
# <a name="compiler-and-language-provider-settings-schema"></a>Derleyici ve Dil Sağlayıcısı Ayarları Şeması
Compiler configuration öğeleri kullanılabilir dil sağlayıcıları için derleyici ve dil sağlayıcısı ayarları belirtin. Her derleyici yapılandırma öğesi kodu belirtir. sağlayıcı türü adı, derleyici parametreler, desteklenen dil adları ve dosya uzantıları desteklenir.  
  
 .NET Framework ilk derleyici ayarları makine yapılandırma dosyasındaki (Machine.config) tanımlar. Geliştiriciler ve derleyici satıcıları ekleyebilirsiniz yapılandırma ayarları için yeni bir <xref:System.CodeDom.Compiler.CodeDomProvider> uygulaması. Kullanım <xref:System.CodeDom.Compiler.CodeDomProvider.GetAllCompilerInfo%2A?displayProperty=nameWithType> dil sağlayıcısı ve derleyici yapılandırma ayarlarını bir bilgisayardaki program aracılığıyla listeleme yöntemi.  
  
 [\<Yapılandırma > öğesi](../../../../../docs/framework/configure-apps/file-schema/configuration-element.md)  
  
 [\<System.codeDom >](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)  
  
 [\<System.codeDom >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)  
  
 [\<Derleyici >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)  
  
|Öğe|Açıklama|  
|-------------|-----------------|  
|[\<System.codeDom >](../../../../../docs/framework/configure-apps/file-schema/compiler/system-codedom-element.md)|Kullanılabilir dil sağlayıcıları için derleyici yapılandırma ayarlarını belirtir.|  
|[\<System.codeDom >](../../../../../docs/framework/configure-apps/file-schema/compiler/compilers-element.md)|Compiler configuration öğeleri için kapsayıcı; sıfır veya daha fazlasını içeren [ \<derleyici >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md) öğeleri.|  
|[\<Derleyici >](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)|Compiler configuration öznitelikleri için dil sağlayıcısı belirtir.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, tipik bir derleyici yapılandırma öğesi gösterir.  
  
```xml  
<configuration>  
   <system.codedom>  
     <compilers>  
       <!-- zero or more compiler elements -->  
       <compiler  
          language="c#;cs;csharp"  
          extension=".cs"  
          type="Microsoft.CSharp.CSharpCodeProvider, System, Version=1.0.5000.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"  
          compilerOptions=""  
          warningLevel="1" />  
     </compilers>  
   </system.codedom>  
</configuration>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
- <xref:System.CodeDom.Compiler.CompilerInfo>  
- <xref:System.CodeDom.Compiler.CodeDomProvider>  
- [Yapılandırma Dosyası Şeması](../../../../../docs/framework/configure-apps/file-schema/index.md)  
- [\<Derleyici > öğesi](../../../../../docs/framework/configure-apps/file-schema/compiler/compiler-element.md)
