---
title: '#If... Then... #Else yönergeleri'
ms.date: 04/11/2018
ms.prod: .net
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vb.#EndIf
- '#End If'
- '#Then'
- '#ElseIf'
- vb.#ElseIf
- vb.#Else
- vb.#If
helpviewer_keywords:
- Visual Basic code, compiling
- '#If directive [Visual Basic]'
- conditional compilation [Visual Basic], directives
- '#End if directive [Visual Basic]'
- selective compiling
- else directive (#else)
- '#Else directive [Visual Basic]'
ms.assetid: 10bba104-e3fd-451b-b672-faa472530502
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 884c7ed6f0a346f2d35f01006cea23e47907d13f
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2018
---
# <a name="ifthenelse-directives"></a><span data-ttu-id="27307-102">#If...Then...#Else Yönergeleri</span><span class="sxs-lookup"><span data-stu-id="27307-102">#If...Then...#Else Directives</span></span>
<span data-ttu-id="27307-103">Visual Basic kodu seçili bloklarını koşullu olarak derler.</span><span class="sxs-lookup"><span data-stu-id="27307-103">Conditionally compiles selected blocks of Visual Basic code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="27307-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="27307-104">Syntax</span></span>  
  
```  
#If expression Then  
   statements  
[ #ElseIf expression Then  
   [ statements ]  
...  
#ElseIf expression Then  
   [ statements ] ]  
[ #Else  
   [ statements ] ]  
#End If  
```  
  
## <a name="parts"></a><span data-ttu-id="27307-105">Bölümler</span><span class="sxs-lookup"><span data-stu-id="27307-105">Parts</span></span>  
 `expression`  
 <span data-ttu-id="27307-106">İçin gerekli `#If` ve `#ElseIf` deyimleri, isteğe bağlı başka bir yerde.</span><span class="sxs-lookup"><span data-stu-id="27307-106">Required for `#If` and `#ElseIf` statements, optional elsewhere.</span></span> <span data-ttu-id="27307-107">Özel olarak bir veya daha fazla koşullu derleyici sabitleri, değişmez değerleri ve değerlendiren işleçleri oluşan herhangi bir ifade `True` veya `False`.</span><span class="sxs-lookup"><span data-stu-id="27307-107">Any expression, consisting exclusively of one or more conditional compiler constants, literals, and operators, that evaluates to `True` or `False`.</span></span>  
  
 `statements`  
 <span data-ttu-id="27307-108">İçin gerekli `#If` deyimi engellemek, isteğe bağlı başka bir yerde.</span><span class="sxs-lookup"><span data-stu-id="27307-108">Required for `#If` statement block, optional elsewhere.</span></span> <span data-ttu-id="27307-109">Visual Basic programı çizgi veya ilişkili ifade değerlendirilirse derlenen derleyici yönergeleri `True`.</span><span class="sxs-lookup"><span data-stu-id="27307-109">Visual Basic program lines or compiler directives that are compiled if the associated expression evaluates to `True`.</span></span>  
  
 `#End If`  
 <span data-ttu-id="27307-110">Sonlandırır `#If` deyimi bloğu.</span><span class="sxs-lookup"><span data-stu-id="27307-110">Terminates the `#If` statement block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="27307-111">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="27307-111">Remarks</span></span>  
 <span data-ttu-id="27307-112">Yüzeyinde davranışını `#If...Then...#Else` yönergeleri görünür aynı aynı `If...Then...Else` deyimleri.</span><span class="sxs-lookup"><span data-stu-id="27307-112">On the surface, the behavior of the `#If...Then...#Else` directives appears the same as that of the `If...Then...Else` statements.</span></span> <span data-ttu-id="27307-113">Ancak, `#If...Then...#Else` yönergeleri değerlendirmek derleyicisi tarafından derlenen ancak `If...Then...Else` deyimleri çalışma zamanında koşulları değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="27307-113">However, the `#If...Then...#Else` directives evaluate what is compiled by the compiler, whereas the `If...Then...Else` statements evaluate conditions at run time.</span></span>  
  
 <span data-ttu-id="27307-114">Koşullu derleme genellikle farklı platformlar için aynı programı derlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27307-114">Conditional compilation is typically used to compile the same program for different platforms.</span></span> <span data-ttu-id="27307-115">Önlemek için de kullanılan yürütülebilir bir dosya olarak görünmesini kodda hata ayıklama.</span><span class="sxs-lookup"><span data-stu-id="27307-115">It is also used to prevent debugging code from appearing in an executable file.</span></span> <span data-ttu-id="27307-116">Boyutu veya performans üzerinde hiçbir etkisi olmaz şekilde koşullu derleme sırasında dışlanan kod tamamen son yürütülebilir dosyasından atlandı.</span><span class="sxs-lookup"><span data-stu-id="27307-116">Code excluded during conditional compilation is completely omitted from the final executable file, so it has no effect on size or performance.</span></span>  
  
 <span data-ttu-id="27307-117">Tüm değerlendirme sonucunu bağımsız olarak tüm ifadeler kullanarak değerlendirilir `Option Compare Binary`.</span><span class="sxs-lookup"><span data-stu-id="27307-117">Regardless of the outcome of any evaluation, all expressions are evaluated using `Option Compare Binary`.</span></span> <span data-ttu-id="27307-118">`Option Compare` Deyimi ifadelerinde etkilemez `#If` ve `#ElseIf` deyimleri.</span><span class="sxs-lookup"><span data-stu-id="27307-118">The `Option Compare` statement does not affect expressions in `#If` and `#ElseIf` statements.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="27307-119">Hiçbir tek satırlı biçiminde `#If`, `#Else`, `#ElseIf`, ve `#End If` yönergeleri bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="27307-119">No single-line form of the `#If`, `#Else`, `#ElseIf`, and `#End If` directives exists.</span></span> <span data-ttu-id="27307-120">Başka bir kod herhangi yönergesi olarak aynı satırda görünebilir.</span><span class="sxs-lookup"><span data-stu-id="27307-120">No other code can appear on the same line as any of the directives.</span></span> 

<span data-ttu-id="27307-121">Koşullu derleme bloğundaki ifadeleri tam mantıksal deyimler olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="27307-121">The statements within a conditional compilation block must be complete logical statements.</span></span> <span data-ttu-id="27307-122">Örneğin, yalnızca bir işlev özniteliklerini koşullu derlenemiyor, ancak koşullu özniteliklerini birlikte işlevi bildirebilir:</span><span class="sxs-lookup"><span data-stu-id="27307-122">For example, you cannot conditionally compile only the attributes of a function, but you can conditionally declare the function along with its attributes:</span></span>

```vb
   #If DEBUG Then
   <WebMethod()>
   Public Function SomeFunction() As String
   #Else
   <WebMethod(CacheDuration:=86400)>
   Public Function SomeFunction() As String
   #End If
```

## <a name="example"></a><span data-ttu-id="27307-123">Örnek</span><span class="sxs-lookup"><span data-stu-id="27307-123">Example</span></span>
 <span data-ttu-id="27307-124">Bu örnekte `#If...Then...#Else` yapı belirli deyimleri derlenip derlenmeyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="27307-124">This example uses the `#If...Then...#Else` construct to determine whether to compile certain statements.</span></span>  
  
 [!code-vb[VbVbalrConditionalComp#1](../../../visual-basic/language-reference/directives/codesnippet/VisualBasic/if-then-else-directives_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="27307-125">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="27307-125">See Also</span></span>  
[<span data-ttu-id="27307-126">#Const Yönergesi</span><span class="sxs-lookup"><span data-stu-id="27307-126">#Const Directive</span></span>](../../../visual-basic/language-reference/directives/const-directive.md)  
[<span data-ttu-id="27307-127">If...Then...Else Deyimi</span><span class="sxs-lookup"><span data-stu-id="27307-127">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)  
<span data-ttu-id="27307-128">[Koşullu derleme](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md) </span><span class="sxs-lookup"><span data-stu-id="27307-128">[Conditional Compilation](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md) </span></span>  
<xref:System.Diagnostics.ConditionalAttribute?displayProperty=nameWithType>   


