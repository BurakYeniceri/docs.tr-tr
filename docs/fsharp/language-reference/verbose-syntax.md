---
title: Ayrıntılı Sözdizimi (F#)
description: 'F # programlama dilinin ayrıntılı ve basit söz dizimi arasındaki fark hakkında bilgi edinin.'
ms.date: 05/16/2016
ms.openlocfilehash: e697c6fe619df7ffe12f7d4e2a234a5a5cb401ff
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2018
ms.locfileid: "50196771"
---
# <a name="verbose-syntax"></a>Ayrıntılı Sözdizimi

F # Dili içinde birçok yapıları için kullanılabilir iki tür sözdizimi vardır: *ayrıntılı sözdizimi* ve *basit söz dizimi*. Ayrıntılı sözdizimi gibi yaygın olarak kullanılmaz, ancak için girinti daha az duyarlı olan, avantajına sahiptir. Basit sözdizimi daha kısadır ve girinti başlangıcını ve bitişini yapıları göstermek için kullandığı yerine ek anahtar sözcükler gibi `begin`, `end`, `in`ve benzeri. Basit sözdizimi varsayılan sözdizimidir. Basit sözdizimi etkinleştirilmediğinde Bu konu, F # yapılarını sözdizimi açıklar. Basit sözdizimi etkinleştirseniz bile bazı yapıları için ayrıntılı sözdizimi hala kullanabilmeniz için ayrıntılı sözdizimi her zaman etkindir. Kullanarak basit söz dizimi devre dışı bırakabilirsiniz `#light "off"` yönergesi.

## <a name="table-of-constructs"></a>Yapıları tablosu

Aşağıdaki tabloda, F # dil yapılarının basit ve ayrıntılı sözdizimi bağlamlarda gösterilmektedir. iki biçim arasında bir fark olduğunda. Bu tabloda, açı köşeli ayraçlar (&lt;&gt;) kullanıcı tarafından sağlanan söz dizimi öğeleri alın. Her dil yapısı içinde bu yapıları kullanılan söz dizimi hakkında daha ayrıntılı bilgi için belgelere bakın.

<table>
<tr>
<th>Dil yapısı</th>
<th>Basit sözdizimi</th>
<th>Ayrıntılı sözdizimi</th>
</tr>
<tr>
<td>
Bileşik deyimler
</td>
<td>

```xml
<expression1>
<expression2>
```
</td><td>

```fsharp
<expression1>; <expression2>
```

</td>
</tr>
<tr><td>

iç içe geçmiş `let` bağlamaları

</td><td>

```fsharp
let f x =
    let a = 1
    let b = 2
    x + a + b
```

</td><td>

```fsharp
let f x =
    let a = 1 in
    let b = 2 in
    x + a + b
```

</td>
</tr>
<tr><td>
kod bloğu
</td><td>

```fsharp
(
    <expression1>
    <expression2>
)
```

</td><td>

```fsharp
begin
    <expression1>;
    <expression2>;
end
```
</td>
</tr>
<tr><td>
`for...do`
</td><td>

```fsharp
for counter = start to finish do
    ...
```

</td><td>

```
for counter = start to finish do
    ...
done
```

</td>
</tr>
<tr><td>
`while...do`
</td><td>

```fsharp
while <condition> do
    ...
```

</td><td>

```fsharp
while <condition> do
    ...
done
```

</td>
</tr>
<tr><td>
`for...in`
</td><td>

```fsharp
for var in start .. finish do
    ...
```

</td><td>

```fsharp
for var in start .. finish do
    ...
done
```

</td>
</tr>
<tr><td>
`do`
</td><td>

```fsharp
do
    ...
```

</td><td>

```fsharp
do
    ...
in
```

</td>
</tr>
<tr><td>Kaydı
</td><td>

```fsharp
type <record-name> =
    {
        <field-declarations>
    }
    <value-or-member-definitions>
```

</td><td>

```fsharp
type <record-name> =
    {
        <field-declarations>
    }
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td>sınıf
</td><td>

```fsharp
type <class-name>(<params>) =
    ...
```

</td><td>

```fsharp
type <class-name>(<params>) =
    class
        ...
    end
```

</td>
</tr>
<tr><td>yapı</td><td>

```fsharp
[<StructAttribute>]
type <structure-name> =
    ...
```

</td><td>

```fsharp
type <structure-name> =
    struct
        ...
    end
```

</td>
</tr>
<tr><td>ayrılmış birleşim</td><td>

```fsharp
type <union-name> =
    | ...
    | ...
    ...
    <value-or-member definitions>
```

</td><td>

```fsharp
type <union-name> =
    | ...
    | ...
    ...
    with
        <value-or-member-definitions>
    end    
```

</td>
</tr>
<tr><td>arabirim</td><td>

```fsharp
type <interface-name> =
    ...
```
</td><td>

```fsharp
type <interface-name> =
    interface
        ...
    end
```

</td>
</tr>
<tr><td>nesne ifadesi</td><td>

```fsharp
{ new <type-name>
    with
        <value-or-member-definitions>
        <interface-implementations>
}
```

</td><td>

```fsharp
{ new <type-name>
    with
        <value-or-member-definitions>
    end
    <interface-implementations>
}
```

</td>
</tr>
<tr><td>arabirim uygulaması</td><td>

```fsharp
interface <interface-name>
    with
        <value-or-member-definitions>
```

</td><td>

```fsharp
interface <interface-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td>tür uzantısı</td><td>

```fsharp
type <type-name>
    with
        <value-or-member-definitions>
```

</td><td>

```fsharp
type <type-name>
    with
        <value-or-member-definitions>
    end
```

</td>
</tr>
<tr><td>modül</td><td>

```fsharp
module <module-name> =
    ...
```

</td><td>

```fsharp
module <module-name> =
    begin
        ...
    end
```

</td>
</tr>
</table>

## <a name="see-also"></a>Ayrıca bkz.

- [F# Dili Başvurusu](index.md)
- [Derleyici Yönergeleri](compiler-directives.md)
- [Kod Biçimlendirme Yönergeleri](code-formatting-guidelines.md)
