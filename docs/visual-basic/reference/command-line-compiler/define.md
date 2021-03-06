---
title: -tanımlama (Visual Basic)
ms.date: 03/10/2018
helpviewer_keywords:
- -d compiler option [Visual Basic]
- /d compiler option [Visual Basic]
- -define compiler option [Visual Basic]
- d compiler option [Visual Basic]
- /define compiler option [Visual Basic]
- define compiler option [Visual Basic]
ms.assetid: f735c57d-1cf9-4f2f-a26f-0de630fd4077
ms.openlocfilehash: 4cab6bc968275bc12af4365fd3da5e3b5ff417f2
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50195183"
---
# <a name="-define-visual-basic"></a>-tanımlama (Visual Basic)
Koşullu derleyici sabitlerini tanımlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
-define:["]symbol[=value][,symbol[=value]]["]  
' -or-  
-d:["]symbol[=value][,symbol[=value]]["]  
```  
  
## <a name="arguments"></a>Arguments  
  
|Terim|Tanım|  
|---|---|  
|`symbol`|Gerekli. Tanımlamak için simge.|  
|`value`|İsteğe bağlı. Atanacak değer `symbol`. Varsa `value` bir dizedir, geçen dilerle ters eğik çizgi /-tırnak içine alınmalıdır (\\") tırnak işaretleri yerine. Değer belirtilmezse sonra olacak şekilde gerçekleştirilen True.|  
  
## <a name="remarks"></a>Açıklamalar  
 `-define` Seçeneğinin etkisi bir kullanmaya benzer bir `#Const` önişlemci yönergesi ile tanımlanan, sabitleri dışında kaynak dosyanızdaki `-define` herkese açık ve projedeki tüm dosyalar için geçerlidir.  
  
 Bu seçenekle tarafından oluşturulan simgeleri kullanabilirsiniz `#If`... `Then`... `#Else` yönergesi, kaynak dosyaları koşullu olarak derleyebilirsiniz.  
  
 `-d` öğesinin kısa biçimidir `-define`.  
  
 Birden çok sembolleriyle tanımlayabilirsiniz `-define` sembol tanımlarını ayırmak için virgül kullanarak.  
  
|Ayarlama / Visual Studio tümleşik geliştirme ortamında tanımlamak için|  
|---|  
|1.  Seçili bir projeyi **Çözüm Gezgini**. Üzerinde **proje** menüsünü tıklatın **özellikleri**. <br />2.  Tıklayın **derleme** sekmesi.<br />3.  **Gelişmiş**'e tıklayın.<br />4.  Değer değiştirme **özel sabitleri** kutusu.|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod, tanımlar ve sonra iki koşullu derleyici sabitlerini kullanır.  
  
 [!code-vb[VbVbalrCompiler#45](../../../visual-basic/reference/command-line-compiler/codesnippet/VisualBasic/define_1.vb)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Basic komut satırı derleyicisi](../../../visual-basic/reference/command-line-compiler/index.md)  
 [#If...Then...#Else Yönergesi](../../../visual-basic/language-reference/directives/if-then-else-directives.md)  
 [#Const Yönergesi](../../../visual-basic/language-reference/directives/const-directive.md)  
 [Örnek Derleme Komut Satırları](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
