---
title: Parametrenin türü &#39; &lt;parametername&gt; &#39; CLS uyumlu değil
ms.date: 07/20/2015
f1_keywords:
- vbc40028
- bc40028
helpviewer_keywords:
- BC40028
ms.assetid: dfa1f6f9-bb88-44ad-b85f-149144363d41
ms.openlocfilehash: 13a4e35cd27ed5aa135cec77c4415f223cba70f2
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43403042"
---
# <a name="type-of-parameter-39ltparameternamegt39-is-not-cls-compliant"></a>Parametrenin türü &#39; &lt;parametername&gt; &#39; CLS uyumlu değil
Bir yordam olarak işaretlenmiş `<CLSCompliant(True)>` ancak bir parametre olarak işaretlenmiş bir tür ile bildirir `<CLSCompliant(False)>`işaret konulmadıysa veya uyumlu olmayan bir tür olduğu için uygun değil.  
  
 İle uyumlu olması için bir yordam için [dil bağımsızlığı ve dilden bağımsız bileşenler](../../../standard/language-independence-and-language-independent-components.md) (CLS), yalnızca CLS uyumlu türler kullanmalıdır. Bu parametre türleri, dönüş türü ve tüm yerel değişkenlerin türleri için geçerlidir.  
  
 Aşağıdaki Visual Basic veri türleri CLS uyumlu değildir:  
  
-   [SByte Veri Türü](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [UInteger Veri Türü](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [ULong Veri Türü](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [UShort Veri Türü](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 Uyguladığınızda <xref:System.CLSCompliantAttribute> bir programlama öğesine özniteliğin ayarladığınız `isCompliant` ya da parametre `True` veya `False` uyumluluk veya uyumsuzluk belirtmek için. Bu parametre için varsayılan yok ve bir değer sağlamanız gerekir.  
  
 Geçerli <xref:System.CLSCompliantAttribute> bir öğe için uyumsuz olarak değerlendirilir.  
  
 Varsayılan olarak, bu iletiyi bir uyarıdır. Uyarıları gizleme veya uyarıları hata olarak değerlendirmesini hakkında daha fazla bilgi için bkz: [Visual Basic'teki uyarıları yapılandırma](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **Hata Kimliği:** BC40028  
  
## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için  
  
-   Yordamın bu belirli türünde bir parametre almalıdır, kaldırmanız <xref:System.CLSCompliantAttribute>. Yordamı, CLS uyumlu olamaz.  
  
-   Yordamı CLS uyumlu olması gerekiyorsa, bu parametrenin türü en yakın CLS uyumlu türüne değiştirin. Örneğin, içinde yerine, `UInteger` kullanmanız mümkün olabilir `Integer` 2.147.483.647 yukarıda değer aralığı gerekmiyorsa. Genişletilmiş aralık gerekiyorsa, değiştirebileceğiniz `UInteger` ile `Long`.  
  
-   Otomasyon ve COM nesneleri ile arabirim, bazı türleri farklı veri genişliği kıyasla olduğunu aklınızda bulundurun [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]. Örneğin, `int` 16 bit diğer ortamlarda genellikle olur. Böyle bir bileşenin bir 16 bitlik tamsayı kabul ediyorsanız, olarak bildirin `Short` yerine `Integer` Yönetilen Visual Basic kodunuzda.