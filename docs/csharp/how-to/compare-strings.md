---
title: 'Nasıl yapılır: dizeleri - C# Kılavuzu'
description: Karşılaştırın ve dize değerleri içeren veya içermeyen durumda olan veya olmayan kültüre özgü sıralama sipariş hakkında bilgi edinin
ms.date: 03/20/2018
helpviewer_keywords:
- strings [C#], comparison
- comparing strings [C#]
ms.openlocfilehash: 36529414d5b51e9e4ade7447ff6e5e908e5153ab
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188579"
---
# <a name="how-to-compare-strings-in-c"></a>C dizeleri karşılaştırma\#

İki sorulardan birini yanıt için dizeleri karşılaştırmak: "Bu iki dizenin eşit olup?" veya "hangi sırada bu dizeler sıralanırken bunları yerleştirilmesi gerektiğini?"

Bu iki soruları dize karşılaştırmaları etkileyen faktörler tarafından karmaşık:

- Bir sıralı veya dilsel karşılaştırma seçebilirsiniz.
- Servis talebi önemlidir, seçebilirsiniz.
- Kültüre özel karşılaştırma seçebilirsiniz.
- Dilsel karşılaştırmalar, kültüre ve platform bağımlı ' dir.

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

Dizeleri karşılaştırmak, aralarında bir sipariş tanımlayın. Karşılaştırmalar, bir dizi dizeleri sıralamak için kullanılır. Bilinen bir sırada dizisi başladıktan sonra aramak hem yazılım ve insanlar daha kolaydır. Diğer karşılaştırmalar, dizeleri aynı olup olmadığını kontrol edebilirsiniz. Bu benzerlik denetimler için eşitlik benzer, ancak büyük/küçük harf farklılıkları gibi bazı farklılıklar yoksayılabilir.

## <a name="default-ordinal-comparisons"></a>Varsayılan sıralı karşılaştırmalar

En yaygın işlemler <xref:System.String.CompareTo%2A?displayProperty=nameWithType> ve <xref:System.String.Equals%2A?displayProperty=nameWithType> veya <xref:System.String.op_Equality%2A?displayProperty=nameWithType> büyük küçük harfe duyarlı bir karşılaştırma sıralı bir karşılaştırma ve geçerli kültürü kullanır. Sonuçları, aşağıdaki örnekte gösterilir.

[!code-csharp-interactive[Comparing strings using an ordinal comparison](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#1)]

Dizeleri karşılaştırırken sıralı karşılaştırmalar, dilsel kurallar dikkate almaz. Bunlar karakter dizelerini karşılaştırır. Büyük küçük harfe duyarlı karşılaştırmalar, kendi karşılaştırmaları büyük/küçük harf kullanın. En önemli bu varsayılan karşılaştırma yöntemleri hakkında geçerli kültürü kullandıkları için sonuçlar bir yerel ayar ve dil ayarlarını makinenin bağlıdır bunlar çalıştırdığı noktasıdır. Bu karşılaştırmalar karşılaştırmalar için uygun olduğu sıra makineler veya konumları arasında tutarlı olmalıdır.

## <a name="case-insensitive-ordinal-comparisons"></a>Büyük küçük harf duyarsız sıralı karşılaştırmalar

<xref:System.String.Equals%2A?displayProperty=nameWithType> Yöntemi belirtmenizi sağlar bir <xref:System.StringComparison> değeri <xref:System.StringComparison.OrdinalIgnoreCase?displayProperty=nameWithType>
büyük küçük harf duyarsız bir karşılaştırma belirtmek için. Ayrıca statik olan <xref:System.String.Compare%2A> büyük küçük harf duyarsız karşılaştırmalar belirten bir Boole bağımsız değişkeni içeren bir yöntem. Bu, aşağıdaki kodda gösterilmiştir:

[!code-csharp-interactive[Comparing strings ignoring case](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#2)]

## <a name="linguistic-comparisons"></a>Dil karşılaştırmaları

Ayrıca dizeleri dilsel kurallar için geçerli kültürü kullanarak sıralanabilir.
Bu bazen "sözcük sıralama düzeninde." adlandırılır Bir dilsel karşılaştırma gerçekleştirdiğinizde, bazı alfasayısal olmayan Unicode karakterlerine atanan özel ağırlıkların olabilir. Örneğin, kısa çizgi "-" "İleri co-op" ve "coop" birbirinin yanına sıralama düzeninde görüntülenir kendisine atanmış çok küçük ağırlığa sahip olabilir. Ayrıca, bazı Unicode karakterler, alfasayısal bir karakter dizisi için eşdeğer olabilir. Aşağıdaki örnek "Bunlar içinde Sokak dans." ifadesini kullanır. Almanca 'ß' ve "ss". Dilsel olarak (Windows içinde), "ss" için Almanca Essetz eşittir: "en-US" ve "de-DE" hem kültürler 'ß' karakter.

[!code-csharp-interactive[Comparing strings using linguistic rules](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#3)]

Bu örnek, dilsel karşılaştırmalar işletim sistemine bağımlı yapısını gösterir. Etkileşimli pencere için konak, bir Linux ana bilgisayardır. Dil ve sıralı karşılaştırmalar, aynı sonucu verir. Bir Windows konakta aynı Bu örnek, aşağıdaki çıktıyı görürsünüz:

```console
<coop> is less than <co-op> using invariant culture
<coop> is greater than <co-op> using ordinal comparison
<coop> is less than <cop> using invariant culture
<coop> is less than <cop> using ordinal comparison
<co-op> is less than <cop> using invariant culture
<co-op> is less than <cop> using ordinal comparison
```

Sıralı bir karşılaştırma için bir dil karşılaştırmadan değiştirdiğinizde "coop" ve "co-op" Windows, "Kopyala" sıralama düzenini değiştirin. İki Alman cümleleri farklı farklı karşılaştırma türleri kullanarak da karşılaştırın.

## <a name="comparisons-using-specific-cultures"></a>Belirli bir kültür kullanarak karşılaştırma

Bu örnek depolar <xref:System.Globalization.CultureInfo> geçerli kültür için.
Özgün kültür ayarlanabilir ve geçerli iş parçacığı nesnesi üzerinde alınır. Karşılaştırmalar kullanılarak gerçekleştirilen <xref:System.StringComparison.CurrentCulture> kültüre özel karşılaştırma emin olmak için değer.

Kullanılan kültürü dilsel karşılaştırmalar etkiler. Aşağıdaki örnek, "en-US" kültürü ve "de-DE" kültürü kullanarak iki Alman cümleleri karşılaştırma sonuçlarını gösterir:

[!code-csharp-interactive[Comparing strings across cultures](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#4)]

Kültüre duyarlı karşılaştırmaları genellikle dizeleri giriş sıralama ve karşılaştırma için kullanıcılar tarafından kullanıcılar tarafından giriş diğer dizeleri ile kullanılır. Bu dizeler sıralama kuralları ve karakter kullanıcının bilgisayarında yerel ayara bağlı olarak değişebilir. Geçerli iş parçacığı kültürünü bağlı olarak aynı karakterler içeren bile dizelerle sıraladığından. Ayrıca, bir Windows makinede yerel olarak bu örnek kod deneyin ve aşağıdaki sonuçları şunları yapacaksınız:

```console
<coop> is less than <co-op> using en-US culture
<coop> is greater than <co-op> using ordinal comparison
<coop> is less than <cop> using en-US culture
<coop> is less than <cop> using ordinal comparison
<co-op> is less than <cop> using en-US culture
<co-op> is less than <cop> using ordinal comparison
```

Dilsel karşılaştırmalar geçerli kültürü temel bağımlıdır ve işletim sistemi bağımlı olan. Dize karşılaştırmaları ile çalışırken, dikkate almanız gerekir.

## <a name="linguistic-sorting-and-searching-strings-in-arrays"></a>Dilsel sıralama ve dizilerde dizeleri arama

Aşağıdaki örnekler nasıl sıralanacağını gösterir ve geçerli kültürü temel bağımlı bir dilsel karşılaştırma kullanarak bir diziye dizelerini arayın. Statik kullandığınız <xref:System.Array> ele yöntemleri bir <xref:System.StringComparer?displayProperty=nameWithType> parametresi.

Bu örnek geçerli kültürü kullanarak bir dize dizisi sıralama gösterir:

[!code-csharp-interactive[Sorting an array of strings](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#5)]

Dizi sonra ikili arama özelliğini kullanarak girişleri için arama yapabilirsiniz. İkili dosya arama, aranan dize koleksiyonu hangi yarısında içerecektir belirlemek için koleksiyon ortasında başlar. Sonraki her karşılaştırma kesen ve onun yarısı koleksiyonda kalan bölümü.  Dizi kullanarak sıralanır <xref:System.StringComparer.CurrentCulture?displayProperty=nameWithType>. Yerel işlev `ShowWhere` dize bulunduğu hakkında bilgi görüntüler. Dize bulunmadığında, döndürülen değer ise olacağı gösterir, bulunmazsa.

[!code-csharp-interactive[Searching in a sorted array](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#6)]

## <a name="ordinal-sorting-and-searching-in-collections"></a>Sıralı sıralama ve arama koleksiyonları

Aşağıdaki kod <xref:System.Collections.Generic.List%601?displayProperty=nameWithType> dizeleri depolamak için koleksiyon sınıfı. Kullanarak dizeleri sıralama <xref:System.Collections.Generic.List%601.Sort%2A?displayProperty=nameWithType> yöntemi. Bu yöntem, iki dizeyi sıraladığı bir temsilci gerekir. <xref:System.String.CompareTo%2A?displayProperty=nameWithType> Yöntemi, karşılaştırma işlevi sağlar. Örneği çalıştırmak ve sırasını gözlemleyin. Bu sıralama işlemi sıralı büyük küçük harfe duyarlı sıralama kullanır. Statik kullanacağınız <xref:System.String.Compare%2A?displayProperty=nameWithType> farklı karşılaştırma kurallarını belirtmek için yöntemleri.

[!code-csharp-interactive[Sorting a list of strings](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#7)]

Sıralanmış sonra dizeleri listesini ikili arama ile aranabilir. Aşağıdaki örnek, aynı karşılaştırma işlevini kullanarak listelenen sıralanmış aramak nasıl gösterir. Yerel işlev `ShowWhere` burada Aranan metin veya olacaktır gösterir:

[!code-csharp-interactive[csProgGuideStrings#11](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#8)]

Her zaman aynı türde karşılaştırma sıralama ve arama için kullandığınızdan emin olun. Farklı karşılaştırma türleri, sıralama ve arama üretir beklenmeyen sonuçlar için kullanma.

Koleksiyon sınıfları gibi <xref:System.Collections.Hashtable?displayProperty=nameWithType>, <xref:System.Collections.Generic.Dictionary%602?displayProperty=nameWithType>, ve <xref:System.Collections.Generic.List%601?displayProperty=nameWithType> ele oluşturuculara sahip bir <xref:System.StringComparer?displayProperty=nameWithType> öğeleri veya anahtarlarının türü parametresi `string`. Genel olarak, mümkün olduğunda bu oluşturucular kullanın ve gerekir ya da belirtin <xref:System.StringComparer.Ordinal?displayProperty=nameWithType> veya <xref:System.StringComparer.OrdinalIgnoreCase?displayProperty=nameWithType>.

## <a name="reference-equality-and-string-interning"></a>Başvuru eşitliği ve dizenin kopyasını kullanma

Örneklerin hiçbiri kullanılan <xref:System.Object.ReferenceEquals%2A>. Bu yöntem, iki dizenin aynı nesne olup olmadığını belirler. Bu dize karşılaştırmaları içinde tutarsız sonuçlara neden olabilir. Aşağıdaki örnek, gösterir *dize kopyası kullanımı* C# özelliği. Bir program iki veya daha fazla aynı dize değişkeni bildirir, derleyici bunları tümü aynı konumda yer depolar. Çağırarak <xref:System.Object.ReferenceEquals%2A> yöntemi, iki dizeyi gerçekten bellekte aynı nesneye başvurması görebilirsiniz. Kullanım <xref:System.String.Copy%2A?displayProperty=nameWithType> yineleniyorsa önlemek için yöntemi. Kopyası yapıldıktan sonra iki dizenin aynı değer olsa bile farklı depolama konumları sahip. Dizeleri aşağıdaki örneği göstermek için çalıştırma `a` ve `b` olan *interned* aynı depolama alanını paylaşır anlamına gelir. Dizeleri `a` ve `c` değil.

[!code-csharp-interactive[Demonstrating string interning](../../../samples/snippets/csharp/how-to/strings/CompareStrings.cs#9)]

> [!NOTE]
> Dizeleri eşitlik için test ettiğinizde, ne tür bir karşılaştırma gerçekleştirmek istiyorsanız açıkça belirtmeniz yöntemleri kullanmanız gerekir. Kodunuzu daha sürdürülebilir ve okunabilir. Yöntemlerinin aşırı yüklemelerini kullanın <xref:System.String?displayProperty=nameWithType> ve <xref:System.Array?displayProperty=nameWithType> sınıfları süren bir <xref:System.StringComparison> numaralandırma parametre. Gerçekleştirilecek karşılaştırma türünü belirt Kullanmaktan kaçının `==` ve `!=` eşitlik için test ettiğinizde işleçleri. <xref:System.String.CompareTo%2A?displayProperty=nameWithType> Örnek yöntemleri her zaman sıralı büyük küçük harfe duyarlı karşılaştırma yapar. Bunlar birincil dizeleri alfabetik olarak sıralamak için uygundur.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Globalization.CultureInfo?displayProperty=nameWithType>  
- <xref:System.StringComparer?displayProperty=nameWithType>  
- [Dizeler](../programming-guide/strings/index.md)  
- [Dizeleri Karşılaştırma](../../standard/base-types/comparing.md)  
- [Uygulamaları Genelleştirme ve Yerelleştirme](/visualstudio/ide/globalizing-and-localizing-applications)
