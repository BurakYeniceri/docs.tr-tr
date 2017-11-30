---
title: "IsNot İşleci (Visual Basic)"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vb.isnot
helpviewer_keywords: IsNot operator [Visual Basic]
ms.assetid: 8dd2bcdb-0166-48a2-9094-60dfb448f36c
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 969fdebdf15a1f779075c58616ccd16c64976a35
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="isnot-operator-visual-basic"></a><span data-ttu-id="2840f-102">IsNot İşleci (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2840f-102">IsNot Operator (Visual Basic)</span></span>
<span data-ttu-id="2840f-103">İki nesne başvuru değişkenini karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="2840f-103">Compares two object reference variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2840f-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2840f-104">Syntax</span></span>  
  
```  
result = object1 IsNot object2  
```  
  
## <a name="parts"></a><span data-ttu-id="2840f-105">Bölümler</span><span class="sxs-lookup"><span data-stu-id="2840f-105">Parts</span></span>  
 `result`  
 <span data-ttu-id="2840f-106">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="2840f-106">Required.</span></span> <span data-ttu-id="2840f-107">A `Boolean` değeri.</span><span class="sxs-lookup"><span data-stu-id="2840f-107">A `Boolean` value.</span></span>  
  
 `object1`  
 <span data-ttu-id="2840f-108">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="2840f-108">Required.</span></span> <span data-ttu-id="2840f-109">Tüm `Object` değişken veya ifade.</span><span class="sxs-lookup"><span data-stu-id="2840f-109">Any `Object` variable or expression.</span></span>  
  
 `object2`  
 <span data-ttu-id="2840f-110">Gerekli.</span><span class="sxs-lookup"><span data-stu-id="2840f-110">Required.</span></span> <span data-ttu-id="2840f-111">Tüm `Object` değişken veya ifade.</span><span class="sxs-lookup"><span data-stu-id="2840f-111">Any `Object` variable or expression.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2840f-112">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2840f-112">Remarks</span></span>  
 <span data-ttu-id="2840f-113">`IsNot` İşleci belirleyen iki nesne başvuruları farklı nesnelere atıfta durumunda.</span><span class="sxs-lookup"><span data-stu-id="2840f-113">The `IsNot` operator determines if two object references refer to different objects.</span></span> <span data-ttu-id="2840f-114">Ancak, değer karşılaştırmaları gerçekleştirmez.</span><span class="sxs-lookup"><span data-stu-id="2840f-114">However, it does not perform value comparisons.</span></span> <span data-ttu-id="2840f-115">Varsa `object1` ve `object2` hem de tam aynı nesne örneği için bkz `result` olan `False`; yoksa `result` olan `True`.</span><span class="sxs-lookup"><span data-stu-id="2840f-115">If `object1` and `object2` both refer to the exact same object instance, `result` is `False`; if they do not, `result` is `True`.</span></span>  
  
 <span data-ttu-id="2840f-116">`IsNot`tam tersidir `Is` işleci.</span><span class="sxs-lookup"><span data-stu-id="2840f-116">`IsNot` is the opposite of the `Is` operator.</span></span> <span data-ttu-id="2840f-117">Avantajı `IsNot` garip sözdizimiyle önleyebilirsiniz olan `Not` ve `Is`, hangi okumak zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="2840f-117">The advantage of `IsNot` is that you can avoid awkward syntax with `Not` and `Is`, which can be difficult to read.</span></span>  
  
 <span data-ttu-id="2840f-118">Kullanabileceğiniz `Is` ve `IsNot` bağlı erken ve geç bağlama nesnelerini test etmek için işleçler.</span><span class="sxs-lookup"><span data-stu-id="2840f-118">You can use the `Is` and `IsNot` operators to test both early-bound and late-bound objects.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2840f-119">`IsNot` İşleci, döndürülen ifadeleri Karşılaştırılacak kullanılamaz `TypeOf` işleci.</span><span class="sxs-lookup"><span data-stu-id="2840f-119">The `IsNot` operator cannot be used to compare expressions returned from the `TypeOf` operator.</span></span> <span data-ttu-id="2840f-120">Bunun yerine, kullanmanız gereken `Not` ve `Is` işleçler.</span><span class="sxs-lookup"><span data-stu-id="2840f-120">Instead, you must use the `Not` and `Is` operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2840f-121">Örnek</span><span class="sxs-lookup"><span data-stu-id="2840f-121">Example</span></span>  
 <span data-ttu-id="2840f-122">Aşağıdaki kod örneği, her ikisi de kullanır `Is` işleci ve `IsNot` aynı karşılaştırma gerçekleştirmek için işleci.</span><span class="sxs-lookup"><span data-stu-id="2840f-122">The following code example uses both the `Is` operator and the `IsNot` operator to accomplish the same comparison.</span></span>  
  
 [!code-vb[VbVbalrOperators#29](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/isnot-operator_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="2840f-123">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="2840f-123">See Also</span></span>  
 [<span data-ttu-id="2840f-124">Is işleci</span><span class="sxs-lookup"><span data-stu-id="2840f-124">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)  
 [<span data-ttu-id="2840f-125">TypeOf işleci</span><span class="sxs-lookup"><span data-stu-id="2840f-125">TypeOf Operator</span></span>](../../../visual-basic/language-reference/operators/typeof-operator.md)  
 [<span data-ttu-id="2840f-126">Visual Basic'de İşleç önceliği</span><span class="sxs-lookup"><span data-stu-id="2840f-126">Operator Precedence in Visual Basic</span></span>](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [<span data-ttu-id="2840f-127">Nasıl yapılır: iki nesnenin aynı olup olmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="2840f-127">How to: Test Whether Two Objects Are the Same</span></span>](../../../visual-basic/programming-guide/language-features/operators-and-expressions/how-to-test-whether-two-objects-are-the-same.md)