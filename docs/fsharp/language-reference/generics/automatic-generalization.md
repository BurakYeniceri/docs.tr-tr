---
title: Otomatik Genelleştirme (F#)
description: 'Birden çok tür mümkün olduğunda çalışmaları için nasıl F # otomatik olarak bağımsız değişkenleri ve işlevleri türlerini genelleştirir öğrenin.'
ms.date: 05/16/2016
ms.openlocfilehash: 84de9cbb2b9fcf2488393f7dbdfc3b610cdcffb0
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43855783"
---
# <a name="automatic-generalization"></a>Otomatik Genelleştirme

F # işlevleri ve ifadeleri türlerini değerlendirilecek tür çıkarımı kullanır. Bu konuda, böylece birden çok tür mümkün olduğunda çalıştıkları nasıl F # otomatik olarak bağımsız değişkenleri ve işlevleri türlerini genelleştirir açıklanmaktadır.

## <a name="automatic-generalization"></a>Otomatik Genelleştirme

Bir işlev üzerinde tür çıkarımı gerçekleştirdiğinde, F # derleyicisi, verilen bir parametre genel olup olmadığını belirler. Derleyici, her parametreyi inceler ve işlev bu parametrenin türünü üzerinde bir bağımlılık olup olmadığını belirler. Kullanmıyorsa, türü genel olarak algılanır.

Aşağıdaki kod örneği, genel olarak derleyici çıkarsar bir işlev gösterir.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet101.fs)]

Tür çıkarımı yapılan olmasını `'a -> 'a -> 'a`.

Türü, aynı bilinmeyen türde iki bağımsız değişkeni alır ve aynı türde bir değer döndüren bir işlev olduğunu gösterir. Önceki işlevi olabilir nedenlerden biri dolayısıyla genel, büyük-işleci (`>`) kendisi geneldir. Büyük-işleci imza olandan `'a -> 'a -> bool`. Tüm işleçler geneldir ve bir işlevdeki kod ile birlikte bir genel olmayan işlev veya işleci bir parametre türü kullanıyorsa, bu parametre türü genelleştirilemediği.

Çünkü `max` olan genel, türleriyle gibi kullanılabilir `int`, `float`ve benzeri, aşağıdaki örneklerde gösterildiği gibi.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet102.fs)]

Ancak, iki bağımsız değişkenler aynı türde olmalıdır. İmza `'a -> 'a -> 'a`değil `'a -> 'b -> 'a`. Bu nedenle, türleri eşleşmediğinden aşağıdaki kod bir hata oluşturur.

```fsharp
// Error: type mismatch.
let biggestIntFloat = max 2.0 3
```

`max` İşlevi büyük destekleyen herhangi bir türü ile de çalışır-işleci. Bu nedenle, ayrıca, bir dizesine, aşağıdaki kodda gösterildiği gibi kullanabilirsiniz.

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-3/snippet104.fs)]

## <a name="value-restriction"></a>Değer kısıtlama

Basit değişmez değerler ve açık bağımsız değişken içeren tam işlev tanımları, derleyici otomatik Genelleştirme gerçekleştirir.

Başka bir deyişle, yeterince belirli bir tür olması zorunlu değildir, ancak aynı zamanda genelleştirilebilir değil, kodu derlemek denerseniz derleyici bir hata verir. Bu kısıtlama için değerler olarak otomatik Genelleştirme üzerinde bu sorun için hata iletisini başvurduğu *değer kısıtlaması*.

Genellikle, bir yapı genel olmasını istiyoruz, ancak derleyici bunu genelleştirmek için yeterli bilgiye sahip olduğunda veya bir jenerik olmayan yapısı yeterli tür bilgisi yanlışlıkla atladığınızda değer kısıtlama hatası gerçekleşir. Değer kısıtlama hatası çözüme daha tam tür çıkarımı sorun aşağıdaki yollardan biriyle sınırlamak için daha net bilgi sağlamak için verilmiştir:

- Bir tür açık tür açıklamanın bir değer ya da parametre ekleyerek jenerik olmayan olacak şekilde kısıtlar.

- Sorun kullanıyorsa, genel bir işlev, işlev bileşimi veya önişlemcinin tanımlamak için bir nongeneralizable yapısı curried işlev bağımsız değişkenleri uygulanır, bir normal işlev tanımı işlevi yeniden deneyin.

- Sorun genelleştirilmesini karmaşık bir ifade ise, ek, kullanılmayan bir parametre ekleyerek bir işleve olun.

- Açık genel tür parametreleri ekleyin. Bu seçeneği nadiren kullanılır.

- Aşağıdaki kod örnekleri, bu senaryoların her birini göstermektedir.

1. durum: Bir ifade çok karmaşık. Bu örnekte, listenin `counter` olması amaçlanmıştır `int option ref`, ancak basit bir değişmez değer tanımlı değil.

```fsharp
let counter = ref None
// Adding a type annotation fixes the problem:
let counter : int option ref = ref None
```

Durum 2: genel bir işlev tanımlamak için bir nongeneralizable yapısı kullanma. İşlev bağımsız değişkenlerinin kısmi uygulaması içerdiğinden bu örnekte, nongeneralizable yapıdır.

```fsharp
let maxhash = max << hash
// The following is acceptable because the argument for maxhash is explicit:
let maxhash obj = (max << hash) obj
```

3. durum: bir ek, kullanılmayan parametre ekleniyor. Bu ifade için genelleştirme kadar basit olmadığı için derleyici değeri kısıtlama hatası verir.

```fsharp
let emptyList10 = Array.create 10 []
// Adding an extra (unused) parameter makes it a function, which is generalizable.
let emptyList10 () = Array.create 10 []
```

Durum 4: Tür parametreleri ekleme.

```fsharp
let arrayOf10Lists = Array.create 10 []
// Adding a type parameter and type annotation lets you write a generic value.
let arrayOf10Lists<'T> = Array.create 10 ([]:'T list)
```

En son durumda değer gibi birçok farklı türlerde değerler örnek oluşturmak için kullanılabilir bir türü işlevi olur:

```fsharp
let intLists = arrayOf10Lists<int>
let floatLists = arrayOf10Lists<float>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Tür Çıkarımı](../type-inference.md)
- [Genel Türler](index.md)
- [Statik Olarak Çözümlenmiş Tür Parametreleri](statically-resolved-type-parameters.md)
- [Kısıtlamalar](constraints.md)
