---
title: dynamic (C# Başvurusu)
ms.date: 07/20/2015
f1_keywords:
- dynamic_CSharpKeyword
helpviewer_keywords:
- dynamic [C#]
- dynamic keyword [C#]
ms.assetid: 9e797102-cc83-4964-bf58-afe4f54d16bc
ms.openlocfilehash: 840ecd6ab929b00e1be96c23eb06ccf362380f8e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44195354"
---
# <a name="dynamic-c-reference"></a>dynamic (C# Başvurusu)

`dynamic` Türü içinde gerçekleşir derleme zamanı tür denetimini atlamasına için işlemleri sağlar. Bunun yerine, bu işlemlerin çalışma zamanında çözümlenir. `dynamic` Türü Office Otomasyon API'leri gibi COM API'leri ve aynı zamanda IronPython kitaplıkları gibi dinamik API'lerine ve erişim HTML belge nesne modeli (DOM) basitleştirir.

Tür `dynamic` türü gibi davranır `object` çoğu durumda. Ancak, türündeki ifadeler içeren işlemler `dynamic` değil çözümlenir veya derleyici tarafından teslim türü. Çalışma zamanı derleyici paketleri birlikte bilgi işlemi ve bu bilgileri daha sonra işlemi değerlendirmek için kullanılır. Türü değişkenlerindeki işleminin bir parçası olarak `dynamic` türündeki değişkenler derlenmiş `object`. Bu nedenle, yazın `dynamic` yalnızca çalışma zamanında değil derleme zamanında var.

Aşağıdaki örnek türünün değişkenini karşılaştırır `dynamic` türünde bir değişkene `object`. Derleme zamanında her bir değişken türünü doğrulamak için üzerine fare işaretçisini getirin `dyn` veya `obj` içinde `WriteLine` deyimleri. IntelliSense gösterir **dinamik** için `dyn` ve **nesne** için `obj`.

[!code-csharp[csrefKeywordsTypes#21](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/dynamic1.cs#21)]

`WriteLine` Deyimleri çalışma zamanı türlerini görüntüler `dyn` ve `obj`. Bu noktada, her ikisi de aynı türde olan tamsayı. Aşağıdaki çıkış üretilir:

`System.Int32`

`System.Int32`

Arasındaki farkı görmek için `dyn` ve `obj` derleme zamanında bildirimler arasında aşağıdaki iki satırı ekleyin ve `WriteLine` önceki örnekte deyimleri.

```csharp
dyn = dyn + 3;
obj = obj + 3;
```

 Derleyici Hatası tamsayı ve bir nesne ifadesinde denenen eklenmesi için bildirilen `obj + 3`. Ancak, herhangi bir hata için bildirilen `dyn + 3`. İçeren ifade `dyn` çünkü derleme zamanında işaretlenmediği türünü `dyn` olduğu `dynamic`.

## <a name="context"></a>Bağlam

`dynamic` Anahtar sözcüğü, doğrudan veya aşağıdaki durumlarda oluşturulmuş bir türü bir bileşeni olarak görünebilir:

- Bildirimler, bir özellik, alan, dizin oluşturucu, parametre türü olarak dönüş değeri, yerel değişken veya kısıtlama türü. Aşağıdaki sınıf tanımı kullanan `dynamic` birkaç farklı bildirimlerinde.

    [!code-csharp[csrefKeywordsTypes#22](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/dynamic1.cs#22)]

- Açık tür dönüştürmeleri içinde bir dönüştürmenin hedef türü.

    [!code-csharp[csrefKeywordsTypes#23](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/dynamic1.cs#23)]

- Burada türleri hizmet değerler olarak gibi sağ tarafında bağlamda bir `is` işleci veya bir `as` işleci veya bağımsız değişken olarak `typeof` kapsamında oluşturulan bir tür. Örneğin, `dynamic` aşağıdaki ifadelerde kullanılabilir.

    [!code-csharp[csrefKeywordsTypes#24](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/dynamic1.cs#24)]

## <a name="example"></a>Örnek

Aşağıdaki örnekte `dynamic` birkaç bildirimlerinde. `Main` Yöntemi de derleme zamanı tür denetimini çalışma zamanı tür denetimi ile karşılaştırır.

[!code-csharp[csrefKeywordsTypes#25](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsTypes/CS/dynamic2.cs#25)]

Daha fazla bilgi ve örnekler için bkz. [türünü kullanarak dinamik](../../../csharp/programming-guide/types/using-type-dynamic.md).

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Dynamic.ExpandoObject?displayProperty=nameWithType>  
- <xref:System.Dynamic.DynamicObject?displayProperty=nameWithType>  
- [Tür dinamiği kullanma](../../../csharp/programming-guide/types/using-type-dynamic.md)  
- [object](../../../csharp/language-reference/keywords/object.md)  
- [is](../../../csharp/language-reference/keywords/is.md)  
- [as](../../../csharp/language-reference/keywords/as.md)  
- [typeof](../../../csharp/language-reference/keywords/typeof.md)  
- [Nasıl yapılır: desen eşleştirme, kullanarak güvenli bir şekilde atama, ve işleçler](../../how-to/safely-cast-using-pattern-matching-is-and-as-operators.md)  
- [İzlenecek yol: Nesneler oluşturma ve dinamik kullanma](../../../csharp/programming-guide/types/walkthrough-creating-and-using-dynamic-objects.md)
