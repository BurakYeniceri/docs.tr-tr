---
title: -warn (C# Derleyici Seçenekleri)
ms.date: 07/20/2015
f1_keywords:
- /warn
helpviewer_keywords:
- warning level [C#]
- /w compiler option [C#]
- -w compiler option [C#]
- -warn compiler option [C#]
- /warn compiler option [C#]
- w compiler option [C#]
- warn compiler option [C#]
ms.assetid: 5f80ff59-4991-4382-9f9a-77da18446e71
ms.openlocfilehash: 14656fa25ea1d01339bd63efb999e938e1243db8
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43865614"
---
# <a name="-warn-c-compiler-options"></a>-warn (C# Derleyici Seçenekleri)
**-Warn** seçeneği, derleyicinin görüntülenecek uyarı düzeyini belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```console  
-warn:option  
```  
  
## <a name="arguments"></a>Arguments  
 `option`  
 Derleme için görüntülenmesini istediğiniz uyarı düzeyini: yalnızca yüksek önem düzeyindeki uyarılar; düşük numaralarını göster daha yüksek numaralar daha fazla uyarıyı gösterir. Geçerli değerler 0-4:  
  
|Uyarı düzeyi|Açıklama|  
|-------------------|-------------|  
|0|Tüm uyarı iletilerini arabellek devre dışı bırakır.|  
|1.|Önemli uyarı iletileri görüntülenir.|  
|2|1. düzey uyarıları ve bazı, görüntüler, sınıf üyeleri gizleme hakkında uyarılar gibi daha az öneme sahip uyarılar.|  
|3|Düzey 2 uyarıları görüntüler belirli, uyarılar için her zaman değerlendirin ifadeler hakkında gibi daha az öneme sahip uyarılar ayrıca `true` veya `false`.|  
|4 (varsayılan)|Tüm görüntüler, 3 uyarıları ve bilgilendirici uyarılar düzey.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bir hata veya uyarı hakkında bilgi almak için Yardım dizini hata kodunu bakabilirsiniz. Bir hata veya uyarı hakkında bilgi almak diğer yolları için bkz. [C# derleyici hataları](../../../csharp/language-reference/compiler-messages/index.md).  
  
 Kullanım [- warnaserror](../../../csharp/language-reference/compiler-options/warnaserror-compiler-option.md) tüm uyarıları hata olarak değerlendirilecek. Kullanım [- nowarn](../../../csharp/language-reference/compiler-options/nowarn-compiler-option.md) belirli uyarıları devre dışı.  
  
 **-w** öğesinin kısa biçimidir **-warn**.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Bu derleyici seçeneğini Visual Studio geliştirme ortamında ayarlamak için  
  
1.  Projenin açın **özellikleri** sayfası.  
  
2.  Tıklayın **derleme** özellik sayfası.  
  
3.  Değiştirme **uyarı düzeyi** özelliği.  
  
 Bu derleyici seçeneğini program üzerinden ayarlamak konusunda daha fazla bilgi için bkz: <xref:VSLangProj80.CSharpProjectConfigurationProperties3.WarningLevel%2A>.  
  
## <a name="example"></a>Örnek  
 Derleme `in.cs` ve derleyicinin yalnızca 1. düzey uyarıları göster:  
  
```console  
csc -warn:1 in.cs  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  

- [C# Derleyici Seçenekleri](../../../csharp/language-reference/compiler-options/index.md)  
- [Proje ve Çözüm Özelliklerini Yönetme](/visualstudio/ide/managing-project-and-solution-properties)
