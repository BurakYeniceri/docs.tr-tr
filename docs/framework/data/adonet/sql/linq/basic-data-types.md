---
title: Temel veri türleri
ms.date: 03/30/2017
ms.assetid: eca2c472-9548-4800-bd31-5d8d9f11752b
ms.openlocfilehash: 977f99f129d591898953ed24ad5acdaa3ae9a88a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33366000"
---
# <a name="basic-data-types"></a>Temel veri türleri
Transact-SQL önce LINQ to SQL sorguları Çevir çünkü bunlar Microsoft SQL Server üzerinde yürütülür. LINQ-SQL temel veri türleri için SQL Server mu aynı yerleşik işlevlerinin çoğunu destekler.  
  
## <a name="casting"></a>Atama  
 SQL Server içinde benzer geçerli bir dönüştürme ise açık veya kapalı atamaları bir hedef CLR türü bir kaynaktan CLR türü etkinleştirilir. CLR atama hakkında daha fazla bilgi için bkz: [CType işlevi](~/docs/visual-basic/language-reference/functions/ctype-function.md) (Visual Basic) ve [olarak](~/docs/csharp/language-reference/keywords/as.md). Dönüştürme işleminden sonra atamaları doğal olarak hedef türe eşleme diğer CLR ifadeleri davranışını eşleşecek şekilde bir CLR ifadesi üzerinde gerçekleştirilen işlemler davranışını değiştirin. Atamalar da devralma eşleme bağlamında çevrilebilir. Böylece alt özgü verilerine erişilebilir nesneler için daha özel varlık türlerinde çevirebilirsiniz.  
  
## <a name="equality-operators"></a>Eşitlik İşleçleri  
 LINQ-SQL, SQL sorguları için LINQ içinde temel veri türleri hakkında aşağıdaki eşitlik işleçleri destekler:  
  
-   Eşit ve eşitsizlik işleci: eşitlik ve eşitsizlik işleçleri için sayısal desteklenir <xref:System.Boolean>, <xref:System.DateTime>, ve <xref:System.TimeSpan> türleri. Visual Basic işleçler hakkında daha fazla bilgi için `=` ve `<>`, bkz: [Karşılaştırma işleçleri](~/docs/visual-basic/language-reference/operators/comparison-operators.md). C# Karşılaştırma işleçleri hakkında daha fazla bilgi için `==` ve `!=`, bkz: [== işleci](~/docs/csharp/language-reference/operators/equality-comparison-operator.md) ve [! = işleci](~/docs/csharp/language-reference/operators/not-equal-operator.md)sırasıyla  
  
-   Is işleci: `IS` işleci devralma eşleme kullanıldığında, desteklenen bir çeviri içeriyor. Bu doğrudan ayrıştırıcı sütunun sınama yerine bir nesne belirli bir varlık türü ve ayrıştırıcı sütunun bir denetim için çevrilen olup olmadığını belirlemek için kullanılabilir. Visual Basic ve C# işleçleri hakkında daha fazla bilgi için bkz: [Is işlecini](~/docs/visual-basic/language-reference/operators/is-operator.md) ve [olan](~/docs/csharp/language-reference/keywords/is.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [SQL-CLR Tür Eşlemesi](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mapping.md)  
 [Veri Türleri ve İşlevleri](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
