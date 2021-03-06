---
title: 'Nasıl yapılır: Tür için Değer Eşitliği Tanımlama (C# Programlama Kılavuzu)'
ms.date: 07/20/2015
helpviewer_keywords:
- overriding Equals method [C#]
- object equivalence [C#]
- Equals method [C#] , overriding
- value equality [C#]
- equivalence [C#]
ms.assetid: 4084581e-b931-498b-9534-cf7ef5b68690
ms.openlocfilehash: 365aa5a71eb3d07a79920f565a66fcac67de0b42
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "44042627"
---
# <a name="how-to-define-value-equality-for-a-type-c-programming-guide"></a>Nasıl yapılır: Tür için Değer Eşitliği Tanımlama (C# Programlama Kılavuzu)
Tanımladığınız bir sınıf veya yapı zamanı türü için değer eşitliği (veya eşdeğer) özel bir tanımı oluşturmak için mantıklı olup olmadığını belirleyin. Genellikle, değer eşitliği çeşit bir koleksiyona eklenmesi olması beklenen nesne türü veya alanlar ve özellikler kümesi saklamak için birincil amaçları olduğunda uygulayın. Tüm alanlar ve Özellikler türü karşılaştırması, değer eşitliği tanımınız temel alabilir veya tanımı bir alt kümesi üzerinde temel alabilir. Ancak, her iki durumda da ve sınıflar ve yapılar, uygulamanız beş garantileri denkliğin izlemelidir:  
  
1.  `x.Equals(x)` döndürür `true`. Bu yansıma özelliğin çağırılır.  
  
2.  `x.Equals(y)` aynı değeri döndürür `y.Equals(x)`. Bu simetrik özelliğin çağırılır.  
  
3.  Varsa `(x.Equals(y) && y.Equals(z))` döndürür `true`, ardından `x.Equals(z)` döndürür `true`. Bu geçişli özelliğin çağırılır.  
  
4.  Art arda gelen çağrıları `x.Equals(y)` nesneleri başvurulan x ve y değiştirilmez sürece aynı değeri döndürür.  
  
5.  `x.Equals(null)` döndürür `false`. Ancak, `null.Equals(null)` ; aykırı Yukarıdaki iki kural numara uymaz.  
  
 Önceden tanımladığınız herhangi bir yapının devraldığı değer eşitliği varsayılan bir uygulama sahip <xref:System.ValueType?displayProperty=nameWithType> , geçersiz kılma <xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType> yöntemi. Bu uygulama, tüm alanları ve tür özellikleri incelemek için yansıtma kullanır. Bu uygulama doğru sonuçlar ürettiğinden olsa da, bu özellikle tür için yazdığınız özel bir uygulama ile karşılaştırıldığında yavaştır.  
  
 Uygulama ayrıntıları için değer eşitliği, sınıflar ve yapılar için farklıdır. Ancak, sınıflar ve yapılar aynı temel adımları eşitlik uygulamak için gerektirir:  
  
1.  Geçersiz kılma [sanal](../../../csharp/language-reference/keywords/virtual.md) <xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType> yöntemi. Çoğu durumda, uygulamanıza `bool Equals( object obj )` türe özgü yalnızca çağırmalıdır `Equals` uygulamasıdır yöntemi <xref:System.IEquatable%601?displayProperty=nameWithType> arabirimi. (2. adıma bakın.)  
  
2.  Uygulama <xref:System.IEquatable%601?displayProperty=nameWithType> türe özgü sağlayarak arabirimi `Equals` yöntemi. Gerçek denklik karşılaştırması gerçekleştirildiği budur. Örneğin, yalnızca bir veya iki alanları türünüz karşılaştırarak eşitliği tanımlama karar verebilirsiniz. Özel durumlar oluşturmayın `Equals`. Yalnızca sınıflar için: Bu yöntem yalnızca bir sınıfta bildirilen alanları incelemeniz gerekir. Çağırmalıdır `base.Equals` temel sınıfta olan alanlar incelemek için. (Tür doğrudan öğesinden devralıyorsa bunu <xref:System.Object>, çünkü <xref:System.Object> uygulaması <xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType> başvuru eşitliği denetimi gerçekleştirir.)  
  
3.  İsteğe bağlı ancak önerilir: aşırı [ == ](../../../csharp/language-reference/operators/equality-comparison-operator.md) ve [! =](../../../csharp/language-reference/operators/not-equal-operator.md) işleçleri.  
  
4.  Geçersiz kılma <xref:System.Object.GetHashCode%2A?displayProperty=nameWithType> böylece aynı üretmek değer eşitliğine sahip iki nesnenin karma kodu.  
  
5.  İsteğe bağlı: "büyük" veya "az" tanımlarında desteklemek için uygulama <xref:System.IComparable%601> arabirim türünüz için ve ayrıca aşırı [ <= ](../../../csharp/language-reference/operators/less-than-equal-operator.md) ve [ >= ](../../../csharp/language-reference/operators/greater-than-equal-operator.md) işleçleri .  
  
 İlk örnekte, bir sınıf uygulamasını gösterir. İkinci örnek, bir yapı uygulamasını gösterir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir sınıfta (başvuru türü) değer eşitliği uygulamak gösterilmektedir.  
  
 [!code-csharp[csProgGuideStatements#19](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-define-value-equality-for-a-type_1.cs)]  
  
 Sınıflar (başvuru türleri) üzerinde hem de varsayılan uygulamasını <xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType> yöntemleri değeri eşitlik kontrolüne başvuru bir eşitlik karşılaştırması gerçekleştirir. Bir uygulayan sanal yöntemi geçersiz kıldığında, amacı, değer eşitliği anlamları vermektir.  
  
 `==` Ve `!=` işleçleri sınıfı bunları aşırı değil olsa bile sınıfları ile kullanılabilir. Ancak, bir başvuru eşitliği denetimi gerçekleştirmek için varsayılan davranış şeklindedir. İşlecini aşırı yüklediyseniz bir sınıftaki `Equals` yöntemini aşırı `==` ve `!=` işleçleri, ancak gerekli değildir.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir yapı (değer türü) değer eşitliği uygulamak gösterilmektedir:  
  
 [!code-csharp[csProgGuideStatements#20](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-define-value-equality-for-a-type_2.cs)]  
  
 Yapılar, varsayılan uygulaması için <xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType> (geçersiz kılınan sürümünde olduğu <xref:System.ValueType?displayProperty=nameWithType>) türündeki her alanın değeri karşılaştırmak için yansıma kullanarak bir değer eşitliği denetimi gerçekleştirir. Ne zaman bir uygulayan geçersiz kılan sanal `Equals` yöntemi bir yapı içinde amaçlı olduğundan değeri eşitlik kontrolüne gerçekleştirmenin daha verimli bir yöntem sağlar ve isteğe bağlı olarak bazı alt kümesinde yapının alan veya özellik karşılaştırma taban.  
  
 [ == ](../../../csharp/language-reference/operators/equality-comparison-operator.md) Ve [! =](../../../csharp/language-reference/operators/not-equal-operator.md) işleçleri struct açıkça bunları aşırı sürece yapı üzerinde çalışamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.

- [Eşitlik Karşılaştırmaları](../../../csharp/programming-guide/statements-expressions-operators/equality-comparisons.md)  
- [C# Programlama Kılavuzu](../../../csharp/programming-guide/index.md)
