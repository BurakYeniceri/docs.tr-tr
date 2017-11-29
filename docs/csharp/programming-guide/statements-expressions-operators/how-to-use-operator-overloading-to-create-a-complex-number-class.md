---
title: "Nasıl yapılır: Karmaşık Sayı Sınıfı Oluşturmak için İşleç Aşırı Yüklemesi Kullanma (C# Programlama Kılavuzu)"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- complex numbers [C#]
- classes [C#], operator overloading
- operator overloading [C#], complex numbers
- operator overloading [C#], using to create classes
- operators [C#], overloading to create a complex number class
ms.assetid: c9b8d982-5112-413f-bae3-b42ae3248ddf
caps.latest.revision: "15"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 2053684a9b20c3ec8f4d8ac275832516b3f2c265
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-use-operator-overloading-to-create-a-complex-number-class-c-programming-guide"></a><span data-ttu-id="f0df6-102">Nasıl yapılır: Karmaşık Sayı Sınıfı Oluşturmak için İşleç Aşırı Yüklemesi Kullanma (C# Programlama Kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="f0df6-102">How to: Use Operator Overloading to Create a Complex Number Class (C# Programming Guide)</span></span>
<span data-ttu-id="f0df6-103">Bu örnek, bir karmaşık sayı sınıfı oluşturmak için işleç aşırı yüklemesi nasıl kullanabileceğinizi gösterir `Complex` karmaşık toplama tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f0df6-103">This example shows how you can use operator overloading to create a complex number class `Complex` that defines complex addition.</span></span> <span data-ttu-id="f0df6-104">Program sanal görüntüler ve geçersiz kılma kullanarak sayıları ve ayrıca gerçek bölümlerini neden `ToString` yöntemi.</span><span class="sxs-lookup"><span data-stu-id="f0df6-104">The program displays the imaginary and the real parts of the numbers and the addition result using an override of the `ToString` method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0df6-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="f0df6-105">Example</span></span>  
 [!code-csharp[csProgGuideStatements#16](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-use-operator-overloading-to-create-a-complex-number-class_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f0df6-106">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="f0df6-106">See Also</span></span>  
 [<span data-ttu-id="f0df6-107">C# programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="f0df6-107">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="f0df6-108">C# işleçleri</span><span class="sxs-lookup"><span data-stu-id="f0df6-108">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="f0df6-109">işleci (C# Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="f0df6-109">operator (C# Reference)</span></span>](../../../csharp/language-reference/keywords/operator.md)  
 [<span data-ttu-id="f0df6-110">Neden aşırı yüklenmiş işleçler her zaman C# ' ta statik misiniz?</span><span class="sxs-lookup"><span data-stu-id="f0df6-110">Why are overloaded operators always static in C#?</span></span>](http://go.microsoft.com/fwlink/?LinkId=112383)
