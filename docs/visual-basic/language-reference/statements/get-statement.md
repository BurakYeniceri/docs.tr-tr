---
title: Get Deyimi
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vb.Get
helpviewer_keywords:
- Get statement [Visual Basic], syntax
- Get statement [Visual Basic]
- properties [Visual Basic], read-only
- read-only properties
- Get keyword [Visual Basic]
- property procedures [Visual Basic], Get statements
ms.assetid: 56b05cdc-bd64-4dfd-bb12-824eacec6f94
caps.latest.revision: "19"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: c1ff062a5e3bf41794bd5b4c90f1e188d6d97480
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="get-statement"></a><span data-ttu-id="47ebf-102">Get Deyimi</span><span class="sxs-lookup"><span data-stu-id="47ebf-102">Get Statement</span></span>
<span data-ttu-id="47ebf-103">Bildiren bir `Get` özellik yordamı bir özelliğin değerini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="47ebf-103">Declares a `Get` property procedure used to retrieve the value of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47ebf-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="47ebf-104">Syntax</span></span>  
  
```  
[ <attributelist> ] [ accessmodifier ] Get()  
    [ statements ]  
End Get  
```  
  
## <a name="parts"></a><span data-ttu-id="47ebf-105">Bölümler</span><span class="sxs-lookup"><span data-stu-id="47ebf-105">Parts</span></span>  
  
|<span data-ttu-id="47ebf-106">Terim</span><span class="sxs-lookup"><span data-stu-id="47ebf-106">Term</span></span>|<span data-ttu-id="47ebf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="47ebf-107">Definition</span></span>|  
|---|---|  
|`attributelist`|<span data-ttu-id="47ebf-108">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="47ebf-108">Optional.</span></span> <span data-ttu-id="47ebf-109">Bkz: [öznitelik listesi](../../../visual-basic/language-reference/statements/attribute-list.md).</span><span class="sxs-lookup"><span data-stu-id="47ebf-109">See [Attribute List](../../../visual-basic/language-reference/statements/attribute-list.md).</span></span>|  
|`accessmodifier`|<span data-ttu-id="47ebf-110">İsteğe bağlı en `Get` ve `Set` bu özellik deyimlerinde.</span><span class="sxs-lookup"><span data-stu-id="47ebf-110">Optional on at most one of the `Get` and `Set` statements in this property.</span></span> <span data-ttu-id="47ebf-111">Aşağıdakilerden biri olabilir:</span><span class="sxs-lookup"><span data-stu-id="47ebf-111">Can be one of the following:</span></span><br /><br /> <span data-ttu-id="47ebf-112">-   [Korumalı](../../../visual-basic/language-reference/modifiers/protected.md)</span><span class="sxs-lookup"><span data-stu-id="47ebf-112">-   [Protected](../../../visual-basic/language-reference/modifiers/protected.md)</span></span><br /><span data-ttu-id="47ebf-113">-   [Arkadaş](../../../visual-basic/language-reference/modifiers/friend.md)</span><span class="sxs-lookup"><span data-stu-id="47ebf-113">-   [Friend](../../../visual-basic/language-reference/modifiers/friend.md)</span></span><br /><span data-ttu-id="47ebf-114">-   [Özel](../../../visual-basic/language-reference/modifiers/private.md)</span><span class="sxs-lookup"><span data-stu-id="47ebf-114">-   [Private](../../../visual-basic/language-reference/modifiers/private.md)</span></span><br />-   `Protected Friend`<br /><br /> <span data-ttu-id="47ebf-115">Bkz: [erişim düzeyini Visual Basic'te](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span><span class="sxs-lookup"><span data-stu-id="47ebf-115">See [Access levels in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md).</span></span>|  
|`statements`|<span data-ttu-id="47ebf-116">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="47ebf-116">Optional.</span></span> <span data-ttu-id="47ebf-117">Çalıştırılan bir veya daha fazla deyimleri `Get` özellik yordamı çağrılır.</span><span class="sxs-lookup"><span data-stu-id="47ebf-117">One or more statements that run when the `Get` property procedure is called.</span></span>|  
|`End Get`|<span data-ttu-id="47ebf-118">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="47ebf-118">Required.</span></span> <span data-ttu-id="47ebf-119">Tanımını sonlandırır `Get` özellik yordamı.</span><span class="sxs-lookup"><span data-stu-id="47ebf-119">Terminates the definition of the `Get` property procedure.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="47ebf-120">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="47ebf-120">Remarks</span></span>  
 <span data-ttu-id="47ebf-121">Her özellik olmalıdır bir `Get` özellik yordamı özelliği işaretlenmemişse `WriteOnly`.</span><span class="sxs-lookup"><span data-stu-id="47ebf-121">Every property must have a `Get` property procedure unless the property is marked `WriteOnly`.</span></span> <span data-ttu-id="47ebf-122">`Get` Yordamı özelliğinin geçerli değeri döndürmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="47ebf-122">The `Get` procedure is used to return the current value of the property.</span></span>  
  
 <span data-ttu-id="47ebf-123">Visual Basic otomatik olarak çağıran bir özelliğin `Get` özelliğin değerini bir deyim istediğinde, yordam.</span><span class="sxs-lookup"><span data-stu-id="47ebf-123">Visual Basic automatically calls a property's `Get` procedure when an expression requests the property's value.</span></span>  
  
 <span data-ttu-id="47ebf-124">Özellik bildirimi gövdesi yalnızca özelliğin içerebilir `Get` ve `Set` yordamları arasında [Property deyimi](../../../visual-basic/language-reference/statements/property-statement.md) ve `End Property` deyimi.</span><span class="sxs-lookup"><span data-stu-id="47ebf-124">The body of the property declaration can contain only the property's `Get` and `Set` procedures between the [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md) and the `End Property` statement.</span></span> <span data-ttu-id="47ebf-125">Bu yordamlar dışında her şey depolanamıyor.</span><span class="sxs-lookup"><span data-stu-id="47ebf-125">It cannot store anything other than those procedures.</span></span> <span data-ttu-id="47ebf-126">Özellikle, bu özelliğin geçerli değeri depolanamıyor.</span><span class="sxs-lookup"><span data-stu-id="47ebf-126">In particular, it cannot store the property's current value.</span></span> <span data-ttu-id="47ebf-127">Özellik yordamları birini içinde depolamak, bir özellik yordamı, erişemediği için bu değeri özellik dışında depolamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="47ebf-127">You must store this value outside the property, because if you store it inside either of the property procedures, the other property procedure cannot access it.</span></span> <span data-ttu-id="47ebf-128">Değeri depolamak için normal yaklaşımdır bir [özel](../../../visual-basic/language-reference/modifiers/private.md) değişkeni bildirilen özelliği ile aynı düzeyde.</span><span class="sxs-lookup"><span data-stu-id="47ebf-128">The usual approach is to store the value in a [Private](../../../visual-basic/language-reference/modifiers/private.md) variable declared at the same level as the property.</span></span> <span data-ttu-id="47ebf-129">Tanımlamanız gerekir bir `Get` yordamı uygulandığı özelliği içinde.</span><span class="sxs-lookup"><span data-stu-id="47ebf-129">You must define a `Get` procedure inside the property to which it applies.</span></span>  
  
 <span data-ttu-id="47ebf-130">`Get` Yordamı kullanmadığınız sürece, içeren özelliğinin erişim düzeyini varsayılan olarak `accessmodifier` içinde `Get` deyimi.</span><span class="sxs-lookup"><span data-stu-id="47ebf-130">The `Get` procedure defaults to the access level of its containing property unless you use `accessmodifier` in the `Get` statement.</span></span>  
  
## <a name="rules"></a><span data-ttu-id="47ebf-131">Kurallar</span><span class="sxs-lookup"><span data-stu-id="47ebf-131">Rules</span></span>  
  
-   <span data-ttu-id="47ebf-132">**Karışık erişim düzeyleri.**</span><span class="sxs-lookup"><span data-stu-id="47ebf-132">**Mixed Access Levels.**</span></span> <span data-ttu-id="47ebf-133">Bir okuma-yazma özelliği tanımlıyorsanız, isteğe bağlı olarak farklı erişim düzeyi için ya da belirtebilirsiniz `Get` veya `Set` yordamı, ancak ikisini birden değil.</span><span class="sxs-lookup"><span data-stu-id="47ebf-133">If you are defining a read-write property, you can optionally specify a different access level for either the `Get` or the `Set` procedure, but not both.</span></span> <span data-ttu-id="47ebf-134">Bunu yaparsanız, yordam erişim düzeyi özelliğin erişim düzeyinden daha kısıtlayıcı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="47ebf-134">If you do this, the procedure access level must be more restrictive than the property's access level.</span></span> <span data-ttu-id="47ebf-135">Örneğin, özellik bildirilirse `Friend`, bildirebilirsiniz `Get` yordam `Private`, ama `Public`.</span><span class="sxs-lookup"><span data-stu-id="47ebf-135">For example, if the property is declared `Friend`, you can declare the `Get` procedure `Private`, but not `Public`.</span></span>  
  
     <span data-ttu-id="47ebf-136">Tanımlıyorsanız, bir `ReadOnly` özelliği, `Get` yordamı tüm özelliğini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="47ebf-136">If you are defining a `ReadOnly` property, the `Get` procedure represents the entire property.</span></span> <span data-ttu-id="47ebf-137">Farklı bir erişim düzeyini bildiremezsiniz `Get`, özellik için iki erişim düzeyleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="47ebf-137">You cannot declare a different access level for `Get`, because that would set two access levels for the property.</span></span>  
  
-   <span data-ttu-id="47ebf-138">**Dönüş türü.**</span><span class="sxs-lookup"><span data-stu-id="47ebf-138">**Return Type.**</span></span> <span data-ttu-id="47ebf-139">[Property deyimi](../../../visual-basic/language-reference/statements/property-statement.md) döndürdüğü değerin veri türü bildirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47ebf-139">The [Property Statement](../../../visual-basic/language-reference/statements/property-statement.md) can declare the data type of the value it returns.</span></span> <span data-ttu-id="47ebf-140">`Get` Yordamı otomatik olarak döndürür veri türü.</span><span class="sxs-lookup"><span data-stu-id="47ebf-140">The `Get` procedure automatically returns that data type.</span></span> <span data-ttu-id="47ebf-141">Herhangi bir veri türü veya bir numaralandırma, yapısı, sınıf veya arabirim adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47ebf-141">You can specify any data type or the name of an enumeration, structure, class, or interface.</span></span>  
  
     <span data-ttu-id="47ebf-142">Varsa `Property` deyimi belirtmiyor `returntype`, yordam döndürür `Object`.</span><span class="sxs-lookup"><span data-stu-id="47ebf-142">If the `Property` statement does not specify `returntype`, the procedure returns `Object`.</span></span>  
  
## <a name="behavior"></a><span data-ttu-id="47ebf-143">Davranış</span><span class="sxs-lookup"><span data-stu-id="47ebf-143">Behavior</span></span>  
  
-   <span data-ttu-id="47ebf-144">**Bir yordam döndürülüyor.**</span><span class="sxs-lookup"><span data-stu-id="47ebf-144">**Returning from a Procedure.**</span></span> <span data-ttu-id="47ebf-145">Zaman `Get` yordamı çağıran kodu döndürür, özellik değeri istenen deyimi içinde yürütme devam eder.</span><span class="sxs-lookup"><span data-stu-id="47ebf-145">When the `Get` procedure returns to the calling code, execution continues within the statement that requested the property value.</span></span>  
  
     <span data-ttu-id="47ebf-146">`Get`özellik yordamları kullanarak bir değer dönebilirsiniz [dönüş deyimi](../../../visual-basic/language-reference/statements/return-statement.md) veya dönüş değeri özellik adına atayarak.</span><span class="sxs-lookup"><span data-stu-id="47ebf-146">`Get` property procedures can return a value using either the [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md) or by assigning the return value to the property name.</span></span> <span data-ttu-id="47ebf-147">Daha fazla bilgi için bkz: "Dönüş değeri" [Function deyimi](../../../visual-basic/language-reference/statements/function-statement.md).</span><span class="sxs-lookup"><span data-stu-id="47ebf-147">For more information, see "Return Value" in [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md).</span></span>  
  
     <span data-ttu-id="47ebf-148">`Exit Property` Ve `Return` deyimleri neden hemen bir çıkış bir özellik yordam.</span><span class="sxs-lookup"><span data-stu-id="47ebf-148">The `Exit Property` and `Return` statements cause an immediate exit from a property procedure.</span></span> <span data-ttu-id="47ebf-149">Herhangi bir sayıda `Exit Property` ve `Return` deyimleri yordamda herhangi bir yerinde görünebilir ve karıştırabilir miyim `Exit Property` ve `Return` deyimleri.</span><span class="sxs-lookup"><span data-stu-id="47ebf-149">Any number of `Exit Property` and `Return` statements can appear anywhere in the procedure, and you can mix `Exit Property` and `Return` statements.</span></span>  
  
-   <span data-ttu-id="47ebf-150">**Dönüş değeri.**</span><span class="sxs-lookup"><span data-stu-id="47ebf-150">**Return Value.**</span></span> <span data-ttu-id="47ebf-151">Bir değer almak için bir `Get` yordamı, özellik adı değerini atayın veya olmasını bir [dönüş deyimi](../../../visual-basic/language-reference/statements/return-statement.md).</span><span class="sxs-lookup"><span data-stu-id="47ebf-151">To return a value from a `Get` procedure, you can either assign the value to the property name or include it in a [Return Statement](../../../visual-basic/language-reference/statements/return-statement.md).</span></span> <span data-ttu-id="47ebf-152">`Return` Deyimi aynı anda atar `Get` yordamı dönüş değeri ve yordamdan çıkar.</span><span class="sxs-lookup"><span data-stu-id="47ebf-152">The `Return` statement simultaneously assigns the `Get` procedure return value and exits the procedure.</span></span>  
  
     <span data-ttu-id="47ebf-153">Kullanırsanız `Exit Property` özellik adı için bir değer atama olmadan `Get` yordamı özelliğin veri türü için varsayılan değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="47ebf-153">If you use `Exit Property` without assigning a value to the property name, the `Get` procedure returns the default value for the property's data type.</span></span> <span data-ttu-id="47ebf-154">Daha fazla bilgi için bkz: "Dönüş değeri" [Function deyimi](../../../visual-basic/language-reference/statements/function-statement.md).</span><span class="sxs-lookup"><span data-stu-id="47ebf-154">For more information, see "Return Value" in [Function Statement](../../../visual-basic/language-reference/statements/function-statement.md).</span></span>  
  
     <span data-ttu-id="47ebf-155">Aşağıdaki örnekte, iki yolla salt okunur özelliği gösterilmektedir `quoteForTheDay` özel değişkende tutulan değeri dönebilirsiniz `quoteValue`.</span><span class="sxs-lookup"><span data-stu-id="47ebf-155">The following example illustrates two ways the read-only property `quoteForTheDay` can return the value held in the private variable `quoteValue`.</span></span>  
  
     [!code-vb[VbVbalrStatements#27](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_1.vb)]  
  
     [!code-vb[VbVbalrStatements#28](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_2.vb)]  
  
     [!code-vb[VbVbalrStatements#29](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_3.vb)]  
  
## <a name="example"></a><span data-ttu-id="47ebf-156">Örnek</span><span class="sxs-lookup"><span data-stu-id="47ebf-156">Example</span></span>  
 <span data-ttu-id="47ebf-157">Aşağıdaki örnek kullanır `Get` deyimi bir özelliğin değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="47ebf-157">The following example uses the `Get` statement to return the value of a property.</span></span>  
  
 [!code-vb[VbVbalrStatements#30](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/get-statement_4.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="47ebf-158">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="47ebf-158">See Also</span></span>  
 [<span data-ttu-id="47ebf-159">Set deyimi</span><span class="sxs-lookup"><span data-stu-id="47ebf-159">Set Statement</span></span>](../../../visual-basic/language-reference/statements/set-statement.md)  
 [<span data-ttu-id="47ebf-160">Property deyimi</span><span class="sxs-lookup"><span data-stu-id="47ebf-160">Property Statement</span></span>](../../../visual-basic/language-reference/statements/property-statement.md)  
 [<span data-ttu-id="47ebf-161">Exit deyimi</span><span class="sxs-lookup"><span data-stu-id="47ebf-161">Exit Statement</span></span>](../../../visual-basic/language-reference/statements/exit-statement.md)  
 [<span data-ttu-id="47ebf-162">Nesneler ve sınıflar</span><span class="sxs-lookup"><span data-stu-id="47ebf-162">Objects and Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/index.md)  
 [<span data-ttu-id="47ebf-163">İzlenecek yol: Sınıfları tanımlama</span><span class="sxs-lookup"><span data-stu-id="47ebf-163">Walkthrough: Defining Classes</span></span>](../../../visual-basic/programming-guide/language-features/objects-and-classes/walkthrough-defining-classes.md)