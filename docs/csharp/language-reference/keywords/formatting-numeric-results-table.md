---
title: Biçimlendirme sayısal sonuçlar tablosunu (C# Başvurusu)
description: C# standart sayısal biçim dizeleri hakkında bilgi edinin
ms.date: 09/20/2018
helpviewer_keywords:
- formatting [C#]
- numeric formatting [C#]
- String.Format method
ms.assetid: 120ba537-4448-4c62-8676-7a8fdd98f496
ms.openlocfilehash: 6f1cb5b49139cf9661e678cfc0ecc884a2749622
ms.sourcegitcommit: daa8788af67ac2d1cecd24f9f3409babb2f978c9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2018
ms.locfileid: "47863708"
---
# <a name="formatting-numeric-results-table-c-reference"></a>Biçimlendirme sayısal sonuçlar tablosunu (C# Başvurusu)

Aşağıdaki tablo, sayısal sonuçlarını biçimlendirme için desteklenen biçim belirticileri gösterir. Biçimlendirilmiş sonuç son sütunda "en-US" karşılık gelen <xref:System.Globalization.CultureInfo>.

|Biçim belirteci|Açıklama|Örnekler|Sonuç|  
|----------------------|-----------------|--------------|------------|  
|C ya da c|Para Birimi|`string s = $"{2.5:C}";`<br /><br /> `string s = $"{-2.5:C}";`|$2.50<br /><br /> ($2.50)|  
|D veya d|Ondalık|`string s = $"{25:D5}";`|00025|  
|E veya e|Üstel|`string s = $"{250000:E2}";`|2.50E + 005|  
|F veya f|Sabit nokta|`string s = $"{2.5:F2}";`<br /><br /> `string s = $"{2.5:F0}";`|2.50<br /><br /> 3|  
|G veya g|Genel|`string s = $"{2.5:G}";`|2,5|  
|N veya n|Sayısal|`string s = $"{2500000:N}";`|2,500,000.00|  
|P ya da p|Yüzde|`string s = $"{0.25:P}";`|%25.00|  
|R veya r|Gidiş|`string s = $"{2.5:R}";`|2,5|  
|X ya da x|Onaltılık|`string s = $"{250:X}";`<br /><br /> `string s = $"{0xffff:X}";`|FA<br /><br /> FFFF|  

## <a name="remarks"></a>Açıklamalar

Bir biçim belirticisi bir biçim dizesi oluşturmak için kullanın. Biçim dizesi aşağıdaki şekildedir: `Axx`burada

- `A` Biçimlendirme sayısal değere uygulanmış türünü denetleyen biçim belirticisi ' dir.
- `xx` biçimlendirilmiş çıktı basamak sayısını etkiler. duyarlık belirticisi ' dir. Duyarlık belirticisi aralıkları 0 ile 99 değeri.

Ondalık ("D" veya "d") ve ("X" veya "x") onaltılı biçim belirticileri yalnızca integral türleri için desteklenir. Gidiş dönüş ("R" veya "r") biçim tanımlayıcısı sadece desteklenen <xref:System.Single>, <xref:System.Double>, ve <xref:System.Numerics.BigInteger> türleri.

Standart sayısal biçim dizeleri tarafından desteklenir:

- Bazı aşırı yüklemeleri `ToString` tüm sayısal türlerin yöntemi. Örneğin, bir sayısal biçim dizesi sağlayabilirsiniz <xref:System.Int32.ToString%28System.String%29?displayProperty=nameWithType> ve <xref:System.Int32.ToString%28System.String%2CSystem.IFormatProvider%29?displayProperty=nameWithType> yöntemleri.

- .NET [bileşik biçimlendirme özelliği](../../../standard/base-types/composite-formatting.md), tarafından desteklenen <xref:System.String.Format%2A?displayProperty=nameWithType> örneğin bir yöntem.

- [İlişkilendirilmiş dizeler](../tokens/interpolated.md).

Daha fazla bilgi için [standart sayısal biçim dizeleri](../../../standard/base-types/standard-numeric-format-strings.md).

## <a name="see-also"></a>Ayrıca bkz.

- [C# başvurusu](../index.md)
- [C# Programlama Kılavuzu](../../programming-guide/index.md)
- [Türler için başvuru tabloları](reference-tables-for-types.md)
- [Biçimlendirme türleri](../../../standard/base-types/formatting-types.md)
- [Bileşik biçimlendirme](../../../standard/base-types/composite-formatting.md)
- [Dize ilişkilendirme](../tokens/interpolated.md)
- [string](string.md)
