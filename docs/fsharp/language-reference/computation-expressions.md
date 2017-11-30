---
title: "Hesaplama İfadeleri (F#)"
description: "Hesaplamalar F sıralı ve denetim akışı yapıları ve bağlamaları kullanılarak birleştirilen #'de yazma için uygun sözdizimini oluşturmayı öğrenin."
keywords: "Visual f #, f # işlevsel programlama"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: acabbf5d-fbb8-479f-894c-7251bf16c8c3
ms.openlocfilehash: 15ba2e167efc1d295d81439dcf85bc7272e05265
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="computation-expressions"></a><span data-ttu-id="ce0f7-104">Hesaplama İfadeleri</span><span class="sxs-lookup"><span data-stu-id="ce0f7-104">Computation Expressions</span></span>

<span data-ttu-id="ce0f7-105">F # hesaplama ifadeleri sıralı ve denetim akışı yapıları ve bağlamaları kullanılarak birleştirilen hesaplamalar yazmak için uygun bir sözdizimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-105">Computation expressions in F# provide a convenient syntax for writing computations that can be sequenced and combined using control flow constructs and bindings.</span></span> <span data-ttu-id="ce0f7-106">İçin kullanışlı bir söz dizimi sağlamak için kullanılabilir *monads*, verileri, Denetim ve işlevsel programlarda yan etkileri yönetmek için kullanılan bir işlev programlama özelliği.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-106">They can be used to provide a convenient syntax for *monads*, a functional programming feature that can be used to manage data, control, and side effects in functional programs.</span></span>


## <a name="built-in-workflows"></a><span data-ttu-id="ce0f7-107">Yerleşik iş akışları</span><span class="sxs-lookup"><span data-stu-id="ce0f7-107">Built-in Workflows</span></span>
<span data-ttu-id="ce0f7-108">Sequence ifadeleri bir zaman uyumsuz iş akışları ve sorgu ifadeleri gibi bir hesaplama ifadesi örnektir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-108">Sequence expressions are an example of a computation expression, as are asynchronous workflows and query expressions.</span></span> <span data-ttu-id="ce0f7-109">Daha fazla bilgi için bkz: [sıraları](sequences.md), [zaman uyumsuz iş akışları](asynchronous-workflows.md), ve [sorgu ifadeleri](query-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="ce0f7-109">For more information, see [Sequences](sequences.md), [Asynchronous Workflows](asynchronous-workflows.md), and [Query Expressions](query-expressions.md).</span></span>

<span data-ttu-id="ce0f7-110">Belirli özellikler sequence ifadeleri ve zaman uyumsuz iş akışları için ortaktır ve hesaplama ifadesi temel sözdizimi gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="ce0f7-110">Certain features are common to both sequence expressions and asynchronous workflows and illustrate the basic syntax for a computation expression:</span></span>

```fsharp
builder-name { expression }
```

<span data-ttu-id="ce0f7-111">Önceki sözdizimi verilen ifade hesaplama ifadesi tarafından belirtilen bir türdeki belirtir *Oluşturucu adını*.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-111">The previous syntax specifies that the given expression is a computation expression of a type specified by *builder-name*.</span></span> <span data-ttu-id="ce0f7-112">Hesaplama ifadesi gibi yerleşik bir iş akışı olabilir `seq` veya `async`, ya da tanımladığınız bir şey olabilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-112">The computation expression can be a built-in workflow, such as `seq` or `async`, or it can be something you define.</span></span> <span data-ttu-id="ce0f7-113">*Oluşturucu adını* olarak bilinen özel bir türünün bir örneği tanımlayıcısıdır *Oluşturucu türüyle*.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-113">The *builder-name* is the identifier for an instance of a special type known as the *builder type*.</span></span> <span data-ttu-id="ce0f7-114">Oluşturucusu türü nasıl ifade yürütür denetleyen hesaplama ifadesi parçasının, diğer bir deyişle, kod birleştirilen biçimini yöneten özel yöntemler tanımlayan bir sınıf türüdür.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-114">The builder type is a class type that defines special methods that govern the way the fragments of the computation expression are combined, that is, code that controls how the expression executes.</span></span> <span data-ttu-id="ce0f7-115">Oluşturucu sınıfı açıklamak için başka bir, döngüler ve bağlamaları gibi birçok F # yapıları, işlem özelleştirmenizi sağlar söylemek için yoludur.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-115">Another way to describe a builder class is to say that it enables you to customize the operation of many F# constructs, such as loops and bindings.</span></span>

<span data-ttu-id="ce0f7-116">Hesaplama ifadeleri iki tür bazı ortak dil yapıları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-116">In computation expressions, two forms are available for some common language constructs.</span></span> <span data-ttu-id="ce0f7-117">Değişken yapıları kullanarak çağırabileceği bir!</span><span class="sxs-lookup"><span data-stu-id="ce0f7-117">You can invoke the variant constructs by using a !</span></span> <span data-ttu-id="ce0f7-118">(bang) belirli anahtar sözcükleri gibi soneki `let!`, `do!`ve benzeri.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-118">(bang) suffix on certain keywords, such as `let!`, `do!`, and so on.</span></span> <span data-ttu-id="ce0f7-119">Bu özel formlar bu işlemlerin normal yerleşik davranışını değiştirmek için oluşturucu sınıfında tanımlanan belirli işlevleri neden.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-119">These special forms cause certain functions defined in the builder class to replace the ordinary built-in behavior of these operations.</span></span> <span data-ttu-id="ce0f7-120">Bu formlar benzer `yield!` biçiminde `yield` dizisi ifadelerinde kullanılan anahtar sözcük.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-120">These forms resemble the `yield!` form of the `yield` keyword that is used in sequence expressions.</span></span> <span data-ttu-id="ce0f7-121">Daha fazla bilgi için bkz: [sıraları](sequences.md).</span><span class="sxs-lookup"><span data-stu-id="ce0f7-121">For more information, see [Sequences](sequences.md).</span></span>


## <a name="creating-a-new-type-of-computation-expression"></a><span data-ttu-id="ce0f7-122">Yeni bir hesaplama ifadesi türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="ce0f7-122">Creating a New Type of Computation Expression</span></span>
<span data-ttu-id="ce0f7-123">Oluşturucu sınıfı oluşturarak ve sınıf üzerinde belirli özel yöntemlerini tanımlama kendi hesaplama ifadeleri özelliklerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-123">You can define the characteristics of your own computation expressions by creating a builder class and defining certain special methods on the class.</span></span> <span data-ttu-id="ce0f7-124">Oluşturucu sınıfı, isteğe bağlı olarak aşağıdaki tabloda listelendiği gibi yöntemleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-124">The builder class can optionally define the methods as listed in the following table.</span></span>

<span data-ttu-id="ce0f7-125">Aşağıdaki tabloda, bir iş akışı Oluşturucu sınıfta kullanılabilir yöntemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-125">The following table describes methods that can be used in a workflow builder class.</span></span>


|<span data-ttu-id="ce0f7-126">**Yöntemi**</span><span class="sxs-lookup"><span data-stu-id="ce0f7-126">**Method**</span></span>|<span data-ttu-id="ce0f7-127">**Tipik imza**</span><span class="sxs-lookup"><span data-stu-id="ce0f7-127">**Typical signature(s)**</span></span>|<span data-ttu-id="ce0f7-128">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="ce0f7-128">**Description**</span></span>|
|----|----|----|
|`Bind`|`M<'T> * ('T -> M<'U>) -> M<'U>`|<span data-ttu-id="ce0f7-129">İçin adlı `let!` ve `do!` hesaplama ifadelerde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-129">Called for `let!` and `do!` in computation expressions.</span></span>|
|`Delay`|`(unit -> M<'T>) -> M<'T>`|<span data-ttu-id="ce0f7-130">Hesaplama ifadesi bir işlevi olarak sarmalar.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-130">Wraps a computation expression as a function.</span></span>|
|`Return`|`'T -> M<'T>`|<span data-ttu-id="ce0f7-131">İçin adlı `return` hesaplama ifadelerde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-131">Called for `return` in computation expressions.</span></span>|
|`ReturnFrom`|`M<'T> -> M<'T>`|<span data-ttu-id="ce0f7-132">İçin adlı `return!` hesaplama ifadelerde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-132">Called for `return!` in computation expressions.</span></span>|
|`Run`|<span data-ttu-id="ce0f7-133">`M<'T> -> M<'T>`veya</span><span class="sxs-lookup"><span data-stu-id="ce0f7-133">`M<'T> -> M<'T>` or</span></span><br /><br />`M<'T> -> 'T`|<span data-ttu-id="ce0f7-134">Hesaplama ifadesi yürütür.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-134">Executes a computation expression.</span></span>|
|`Combine`|<span data-ttu-id="ce0f7-135">`M<'T> * M<'T> -> M<'T>`veya</span><span class="sxs-lookup"><span data-stu-id="ce0f7-135">`M<'T> * M<'T> -> M<'T>` or</span></span><br /><br />`M<unit> * M<'T> -> M<'T>`|<span data-ttu-id="ce0f7-136">Hesaplama ifadeleri sıralaması için çağrılır.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-136">Called for sequencing in computation expressions.</span></span>|
|`For`|<span data-ttu-id="ce0f7-137">`seq<'T> * ('T -> M<'U>) -> M<'U>`veya</span><span class="sxs-lookup"><span data-stu-id="ce0f7-137">`seq<'T> * ('T -> M<'U>) -> M<'U>` or</span></span><br /><br />`seq<'T> * ('T -> M<'U>) -> seq<M<'U>>`|<span data-ttu-id="ce0f7-138">İçin adlı `for...do` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-138">Called for `for...do` expressions in computation expressions.</span></span>|
|`TryFinally`|`M<'T> * (unit -> unit) -> M<'T>`|<span data-ttu-id="ce0f7-139">İçin adlı `try...finally` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-139">Called for `try...finally` expressions in computation expressions.</span></span>|
|`TryWith`|`M<'T> * (exn -> M<'T>) -> M<'T>`|<span data-ttu-id="ce0f7-140">İçin adlı `try...with` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-140">Called for `try...with` expressions in computation expressions.</span></span>|
|`Using`|`'T * ('T -> M<'U>) -> M<'U> when 'U :> IDisposable`|<span data-ttu-id="ce0f7-141">İçin adlı `use` hesaplama ifadeleri bağlama.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-141">Called for `use` bindings in computation expressions.</span></span>|
|`While`|`(unit -> bool) * M<'T> -> M<'T>`|<span data-ttu-id="ce0f7-142">İçin adlı `while...do` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-142">Called for `while...do` expressions in computation expressions.</span></span>|
|`Yield`|`'T -> M<'T>`|<span data-ttu-id="ce0f7-143">İçin adlı `yield` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-143">Called for `yield` expressions in computation expressions.</span></span>|
|`YieldFrom`|`M<'T> -> M<'T>`|<span data-ttu-id="ce0f7-144">İçin adlı `yield!` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-144">Called for `yield!` expressions in computation expressions.</span></span>|
|`Zero`|`unit -> M<'T>`|<span data-ttu-id="ce0f7-145">İçin boş adlı `else` , dallandırır `if...then` hesaplama ifadeleri ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-145">Called for empty `else` branches of `if...then` expressions in computation expressions.</span></span>|
<span data-ttu-id="ce0f7-146">Birçok Oluşturucu sınıftaki yöntemlerin kullanın ve dönüş bir `M<'T>` genellikle birleştirilen, hesaplamalar tür örneğin belirtir ayrı olarak tanımlanan bir tür olduğundan, yapı `Async<'T>` zaman uyumsuz iş akışları için ve `Seq<'T>` Sıralı iş akışları.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-146">Many of the methods in a builder class use and return an `M<'T>` construct, which is typically a separately defined type that characterizes the kind of computations being combined, for example, `Async<'T>` for asynchronous workflows and `Seq<'T>` for sequence workflows.</span></span> <span data-ttu-id="ce0f7-147">Böylece bir yapı döndürülen iş akışı nesnesi sonraki geçirilebilir bu yöntemleri imzalarını birleştirilmiş ve birbirleri ile iç içe geçmiş için etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-147">The signatures of these methods enable them to be combined and nested with each other, so that the workflow object returned from one construct can be passed to the next.</span></span> <span data-ttu-id="ce0f7-148">Hesaplama ifadesi ayrıştırırken derleyici, yukarıdaki tabloda yöntemlere ve hesaplama ifadesi kodu kullanarak, bir dizi iç içe geçmiş işlev çağrısı ifade dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-148">The compiler, when it parses a computation expression, converts the expression into a series of nested function calls by using the methods in the preceding table and the code in the computation expression.</span></span>

<span data-ttu-id="ce0f7-149">İç içe geçmiş ifade aşağıdaki şekildedir:</span><span class="sxs-lookup"><span data-stu-id="ce0f7-149">The nested expression is of the following form:</span></span>

```fsharp
builder.Run(builder.Delay(fun () -> {| cexpr |}))
```

<span data-ttu-id="ce0f7-150">Yukarıdaki kodda, çağrıları `Run` ve `Delay` hesaplama ifadesi Oluşturucu sınıfında tanımlanmazsa göz ardı edilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-150">In the above code, the calls to `Run` and `Delay` are omitted if they are not defined in the computation expression builder class.</span></span> <span data-ttu-id="ce0f7-151">Burada olarak gösterilen hesaplama ifadesi gövdesini `{| cexpr |}`, oluşturucu sınıfının yöntemlerini içeren çağrıları aşağıdaki tabloda açıklanan çevirileri tarafından çevrilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-151">The body of the computation expression, here denoted as `{| cexpr |}`, is translated into calls involving the methods of the builder class by the translations described in the following table.</span></span> <span data-ttu-id="ce0f7-152">Hesaplama ifadesi `{| cexpr |}` bu çevirileri göre tanımlanan yinelemeli olarak eşleştirilir nerede `expr` F # ifade olan ve `cexpr` hesaplama ifadesi.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-152">The computation expression `{| cexpr |}` is defined recursively according to these translations where `expr` is an F# expression and `cexpr` is a computation expression.</span></span>



|<span data-ttu-id="ce0f7-153">İfade</span><span class="sxs-lookup"><span data-stu-id="ce0f7-153">Expression</span></span>|<span data-ttu-id="ce0f7-154">Çeviri</span><span class="sxs-lookup"><span data-stu-id="ce0f7-154">Translation</span></span>|
|----------|-----------|
|<code>{&#124; let binding in cexpr &#124;}</code>|<code>let binding in {&#124; cexpr &#124;}</code>|
|<code>{&#124; let! pattern = expr in cexpr &#124;}</code>|<code>builder.Bind(expr, (fun pattern -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; do! expr in cexpr &#124;}</code>|<code>builder.Bind(expr, (fun () -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; yield expr &#124;}</code>|`builder.Yield(expr)`|
|<code>{&#124; yield! expr &#124;}</code>|`builder.YieldFrom(expr)`|
|<code>{&#124; return expr &#124;}<code>|`builder.Return(expr)`|
|<code>{&#124; return! expr &#124;}</code>|`builder.ReturnFrom(expr)`|
|<code>{&#124; use pattern = expr in cexpr &#124;}</code>|<code>builder.Using(expr, (fun pattern -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; use! value = expr in cexpr &#124;}</code>|<code>builder.Bind(expr, (fun value -> builder.Using(value, (fun value -> {&#124; cexpr &#124;}))))</code>|
|<code>{&#124; if expr then cexpr0 &#124;}</code>|<code>if expr then {&#124; cexpr0 &#124;} else binder.Zero()</code>|
|<code>{&#124; if expr then cexpr0 else cexpr1 &#124;}</code>|<code>if expr then {&#124; cexpr0 &#124;} else {&#124; cexpr1 &#124;}</code>|
|<code>{&#124; match expr with &#124; pattern_i -> cexpr_i &#124;}</code>|<code>match expr with &#124; pattern_i -> {&#124; cexpr_i &#124;}</code>|
|<code>{&#124; for pattern in expr do cexpr &#124;}</code>|<code>builder.For(enumeration, (fun pattern -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; for identifier = expr1 to expr2 do cexpr &#124;}<code>|<code>builder.For(enumeration, (fun identifier -> {&#124; cexpr &#124;}))</code>|
|<code>{&#124; while expr do cexpr &#124;}</code>|<code>builder.While(fun () -> expr), builder.Delay({&#124;cexpr &#124;})</code>|
|<code>{&#124; try cexpr with &#124; pattern_i -> expr_i &#124;}</code>|<code>builder.TryWith(builder.Delay({&#124; cexpr &#124;}), (fun value -> match value with &#124; pattern_i -> expr_i &#124; exn -> reraise exn)))</code>|
|<code>{&#124; try cexpr finally expr &#124;}</code>|<code>builder.TryFinally(builder.Delay( {&#124; cexpr &#124;}), (fun () -> expr))</code>|
|<code>{&#124; cexpr1; cexpr2 &#124;}</code>|<code>builder.Combine({&#124;cexpr1 &#124;}, {&#124; cexpr2 &#124;})</code>|
|<code>{&#124; other-expr; cexpr &#124;}</code>|<code>expr; {&#124; cexpr &#124;}</code>|
|<code>{&#124; other-expr &#124;}</code>|`expr; builder.Zero()`|
<span data-ttu-id="ce0f7-155">Önceki tabloda `other-expr` Aksi takdirde tabloda listelenmeyen bir ifade açıklar.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-155">In the previous table, `other-expr` describes an expression that is not otherwise listed in the table.</span></span> <span data-ttu-id="ce0f7-156">Oluşturucu sınıfı, tüm yöntemleri uygulamak ve tüm önceki tabloda listelenen çevirileri desteklemek gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-156">A builder class does not need to implement all of the methods and support all of the translations listed in the previous table.</span></span> <span data-ttu-id="ce0f7-157">Uygulanmamıştır bu yapıları hesaplama türü ifadelerinde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-157">Those constructs that are not implemented are not available in computation expressions of that type.</span></span> <span data-ttu-id="ce0f7-158">Örneğin desteklemek istemiyorsanız `use` hesaplama ifadeleri anahtar sözcük, tanımını atlamak `Use` Oluşturucu sınıfınızda.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-158">For example, if you do not want to support the `use` keyword in your computation expressions, you can omit the definition of `Use` in your builder class.</span></span>

<span data-ttu-id="ce0f7-159">Aşağıdaki kod örneği, bir dizi olabilir adımı aynı anda tek bir adımda hesaplanan olarak bir hesaplama yalıtan bir hesaplama ifadesi gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-159">The following code example shows a computation expression that encapsulates a computation as a series of steps that can be evaluated one step at a time.</span></span> <span data-ttu-id="ce0f7-160">Bir birleşim türü, ayrılmış `OkOrException`, ifade hata durumunu kadarki hesaplanan olarak kodlar.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-160">A discriminated union type, `OkOrException`, encodes the error state of the expression as evaluated so far.</span></span> <span data-ttu-id="ce0f7-161">Bu kodu Oluşturucu yöntemlerin bazıları Demirbaş uygulamaları gibi hesaplama ifadeleri kullanabileceğiniz birkaç tipik desenleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-161">This code demonstrates several typical patterns that you can use in your computation expressions, such as boilerplate implementations of some of the builder methods.</span></span>

```fsharp
// Computations that can be run step by step
type Eventually<'T> =
    | Done of 'T
    | NotYetDone of (unit -> Eventually<'T>)

module Eventually =
    // The bind for the computations. Append 'func' to the
    // computation.
    let rec bind func expr =
        match expr with
        | Done value -> NotYetDone (fun () -> func value)
        | NotYetDone work -> NotYetDone (fun () -> bind func (work()))

    // Return the final value wrapped in the Eventually type.
    let result value = Done value

    type OkOrException<'T> =
        | Ok of 'T
        | Exception of System.Exception

    // The catch for the computations. Stitch try/with throughout
    // the computation, and return the overall result as an OkOrException.
    let rec catch expr =
        match expr with
        | Done value -> result (Ok value)
        | NotYetDone work ->
            NotYetDone (fun () ->
                let res = try Ok(work()) with | exn -> Exception exn
                match res with
                | Ok cont -> catch cont // note, a tailcall
                | Exception exn -> result (Exception exn))

    // The delay operator.
    let delay func = NotYetDone (fun () -> func())

    // The stepping action for the computations.
    let step expr =
        match expr with
        | Done _ -> expr
        | NotYetDone func -> func ()

    // The rest of the operations are boilerplate.
    // The tryFinally operator.
    // This is boilerplate in terms of "result", "catch", and "bind".
    let tryFinally expr compensation =
        catch (expr)
        |> bind (fun res -> 
            compensation();
            match res with
            | Ok value -> result value
            | Exception exn -> raise exn)

    // The tryWith operator.
    // This is boilerplate in terms of "result", "catch", and "bind".
    let tryWith exn handler =
        catch exn
        |> bind (function Ok value -> result value | Exception exn -> handler exn)

    // The whileLoop operator.
    // This is boilerplate in terms of "result" and "bind".
    let rec whileLoop pred body =
        if pred() then body |> bind (fun _ -> whileLoop pred body)
        else result ()

    // The sequential composition operator.
    // This is boilerplate in terms of "result" and "bind".
    let combine expr1 expr2 =
        expr1 |> bind (fun () -> expr2)

    // The using operator.
    let using (resource: #System.IDisposable) func =
        tryFinally (func resource) (fun () -> resource.Dispose())

    // The forLoop operator.
    // This is boilerplate in terms of "catch", "result", and "bind".
    let forLoop (collection:seq<_>) func =
        let ie = collection.GetEnumerator()
        tryFinally 
            (whileLoop 
                (fun () -> ie.MoveNext()) 
                (delay (fun () -> let value = ie.Current in func value)))
            (fun () -> ie.Dispose())

// The builder class.
type EventuallyBuilder() =
    member x.Bind(comp, func) = Eventually.bind func comp
    member x.Return(value) = Eventually.result value
    member x.ReturnFrom(value) = value
    member x.Combine(expr1, expr2) = Eventually.combine expr1 expr2
    member x.Delay(func) = Eventually.delay func
    member x.Zero() = Eventually.result ()
    member x.TryWith(expr, handler) = Eventually.tryWith expr handler
    member x.TryFinally(expr, compensation) = Eventually.tryFinally expr compensation
    member x.For(coll:seq<_>, func) = Eventually.forLoop coll func
    member x.Using(resource, expr) = Eventually.using resource expr

let eventually = new EventuallyBuilder()

let comp = eventually {
    for x in 1..2 do
        printfn " x = %d" x
    return 3 + 4 }

// Try the remaining lines in F# interactive to see how this 
// computation expression works in practice.
let step x = Eventually.step x

// returns "NotYetDone <closure>"
comp |> step

// prints "x = 1"
// returns "NotYetDone <closure>"
comp |> step |> step

// prints "x = 1"
// prints "x = 2"
// returns "NotYetDone <closure>"
comp |> step |> step |> step |> step |> step |> step

// prints "x = 1"
// prints "x = 2"
// returns "Done 7"
comp |> step |> step |> step |> step |> step |> step |> step |> step
```

<span data-ttu-id="ce0f7-162">Bir hesaplama ifadesi ifade döndürür bir temel türe sahip.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-162">A computation expression has an underlying type, which the expression returns.</span></span> <span data-ttu-id="ce0f7-163">Temel alınan tür gerçekleştirilebilir Gecikmeli bir hesaplama veya hesaplanan bir sonucu gösterebilir veya bazı tür bir koleksiyon yineleme yolunu sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-163">The underlying type may represent a computed result or a delayed computation that can be performed, or it may provide a way to iterate through some type of collection.</span></span> <span data-ttu-id="ce0f7-164">Önceki örnekte, temel alınan tür idi **sonunda**.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-164">In the previous example, the underlying type was **Eventually**.</span></span> <span data-ttu-id="ce0f7-165">Bir sıra ifadesi için temel türdür <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-165">For a sequence expression, the underlying type is <xref:System.Collections.Generic.IEnumerable%601?displayProperty=nameWithType>.</span></span> <span data-ttu-id="ce0f7-166">Bir sorgu ifadesi için temel türdür <xref:System.Linq.IQueryable?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-166">For a query expression, the underlying type is <xref:System.Linq.IQueryable?displayProperty=nameWithType>.</span></span> <span data-ttu-id="ce0f7-167">Asychronous iş akışı için temel türdür [ `Async` ](https://msdn.microsoft.com/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7).</span><span class="sxs-lookup"><span data-stu-id="ce0f7-167">For an asychronous workflow, the underlying type is [`Async`](https://msdn.microsoft.com/library/03eb4d12-a01a-4565-a077-5e83f17cf6f7).</span></span> <span data-ttu-id="ce0f7-168">`Async` Nesnesi sonucu hesaplamak için gerçekleştirilecek iş temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-168">The `Async` object represents the work to be performed to compute the result.</span></span> <span data-ttu-id="ce0f7-169">Örneğin, [ `Async.RunSynchronously` ](https://msdn.microsoft.com/library/0a6663a9-50f2-4d38-8bf3-cefd1a51fd6b) bir hesaplama çalıştırmak ve sonucu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-169">For example, you call [`Async.RunSynchronously`](https://msdn.microsoft.com/library/0a6663a9-50f2-4d38-8bf3-cefd1a51fd6b) to execute a computation and return the result.</span></span>

## <a name="custom-operations"></a><span data-ttu-id="ce0f7-170">Özel işlemler</span><span class="sxs-lookup"><span data-stu-id="ce0f7-170">Custom Operations</span></span>
<span data-ttu-id="ce0f7-171">Hesaplama ifadesi üzerinde özel bir işlemi tanımlamak ve bir işleç bir hesaplama ifadesinde olarak özel bir işlemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-171">You can define a custom operation on a computation expression and use a custom operation as an operator in a computation expression.</span></span> <span data-ttu-id="ce0f7-172">Örneğin, sorgu ifadesinde bir sorgu işleci içerebilir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-172">For example, you can include a query operator in a query expression.</span></span> <span data-ttu-id="ce0f7-173">Özel bir işlemi tanımladığınızda, verim tanımlamanız gerekir ve hesaplama ifadesi yöntemleri için.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-173">When you define a custom operation, you must define the Yield and For methods in the computation expression.</span></span> <span data-ttu-id="ce0f7-174">Özel bir işlemi tanımlamak için hesaplama ifadesi Oluşturucu sınıfında koyabilir ve ardından uygulama [ `CustomOperationAttribute` ](https://msdn.microsoft.com/library/199f3927-79df-484b-ba66-85f58cc49b19).</span><span class="sxs-lookup"><span data-stu-id="ce0f7-174">To define a custom operation, put it in a builder class for the computation expression, and then apply the [`CustomOperationAttribute`](https://msdn.microsoft.com/library/199f3927-79df-484b-ba66-85f58cc49b19).</span></span> <span data-ttu-id="ce0f7-175">Bu öznitelik, bir özel işleminde kullanılacak adı bir bağımsız değişken olarak bir dize alır.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-175">This attribute takes a string as an argument, which is the name to be used in a custom operation.</span></span> <span data-ttu-id="ce0f7-176">Bu ad büyük ayracını hesaplama ifadesi başlangıcında kapsam içine gelir.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-176">This name comes into scope at the start of the opening curly brace of the computation expression.</span></span> <span data-ttu-id="ce0f7-177">Bu nedenle, bu bloğa özel bir işlemi ile aynı ada sahip tanımlayıcıları kullanmamalısınız.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-177">Therefore, you shouldn’t use identifiers that have the same name as a custom operation in this block.</span></span> <span data-ttu-id="ce0f7-178">Örneğin, tanımlayıcılar gibi kullanmaktan kaçının `all` veya `last` sorgu ifadelerinde.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-178">For example, avoid the use of identifiers such as `all` or `last` in query expressions.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce0f7-179">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ce0f7-179">See Also</span></span>
[<span data-ttu-id="ce0f7-180">F # dili başvurusu</span><span class="sxs-lookup"><span data-stu-id="ce0f7-180">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="ce0f7-181">Zaman uyumsuz iş akışları</span><span class="sxs-lookup"><span data-stu-id="ce0f7-181">Asynchronous Workflows</span></span>](asynchronous-workflows.md)

[<span data-ttu-id="ce0f7-182">Dizileri</span><span class="sxs-lookup"><span data-stu-id="ce0f7-182">Sequences</span></span>](https://msdn.microsoft.com/library/6b773b6b-9c9a-4af8-bd9e-d96585c166db)

[<span data-ttu-id="ce0f7-183">Sorgu ifadeleri</span><span class="sxs-lookup"><span data-stu-id="ce0f7-183">Query Expressions</span></span>](query-expressions.md)