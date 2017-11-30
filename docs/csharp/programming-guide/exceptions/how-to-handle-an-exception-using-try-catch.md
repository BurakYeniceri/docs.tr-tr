---
title: "Nasıl yapılır: bir özel durum kullanılarak try-catch (C# programlama Kılavuzu) işleme"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- exception handling [C#], try/catch blocks
- exceptions [C#], try/catch blocks
- try/catch blocks [C#]
ms.assetid: ca8e3773-980e-4767-8633-7408540e9818
caps.latest.revision: "14"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 9098bbcf5cefb85211f9d3bb9cac15943ba02172
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-handle-an-exception-using-trycatch-c-programming-guide"></a><span data-ttu-id="37c4a-102">Nasıl yapılır: try/catch Kullanarak Özel Durum İşleme (C# Programlama Kılavuzu)</span><span class="sxs-lookup"><span data-stu-id="37c4a-102">How to: Handle an Exception Using try/catch (C# Programming Guide)</span></span>
<span data-ttu-id="37c4a-103">Amacı bir [try-catch](../../../csharp/language-reference/keywords/try-catch.md) taşıdır yakalamak ve çalışma kod tarafından oluşturulan özel bir durumu işlemek için.</span><span class="sxs-lookup"><span data-stu-id="37c4a-103">The purpose of a [try-catch](../../../csharp/language-reference/keywords/try-catch.md) block is to catch and handle an exception generated by working code.</span></span> <span data-ttu-id="37c4a-104">Bazı özel durumlar işlenebilir bir `catch` bloğu ve sorun çözüldüğünde yeniden atılmış olan özel durum; ancak, daha sık yapabileceğiniz tek şey uygun özel durum atılır emin olun.</span><span class="sxs-lookup"><span data-stu-id="37c4a-104">Some exceptions can be handled in a `catch` block and the problem solved without the exception being re-thrown; however, more often the only thing that you can do is make sure that the appropriate exception is thrown.</span></span>  
  
## <a name="example"></a><span data-ttu-id="37c4a-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="37c4a-105">Example</span></span>  
 <span data-ttu-id="37c4a-106">Bu örnekte, <xref:System.IndexOutOfRangeException> en uygun özel durum değil: <xref:System.ArgumentOutOfRangeException> tarafından hataya neden olduğundan daha fazla yöntemi için mantıklı `index` bağımsız değişkeni geçirilen çağıran tarafından.</span><span class="sxs-lookup"><span data-stu-id="37c4a-106">In this example, <xref:System.IndexOutOfRangeException> is not the most appropriate exception: <xref:System.ArgumentOutOfRangeException> makes more sense for the method because the error is caused by the `index` argument passed in by the caller.</span></span>  
  
 [!code-csharp[csProgGuideExceptions#5](../../../csharp/programming-guide/exceptions/codesnippet/CSharp/how-to-handle-an-exception-using-try-catch_1.cs)]  
  
## <a name="comments"></a><span data-ttu-id="37c4a-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="37c4a-107">Comments</span></span>  
 <span data-ttu-id="37c4a-108">Bir özel duruma neden olan kod sınırlanan `try` bloğu.</span><span class="sxs-lookup"><span data-stu-id="37c4a-108">The code that causes an exception is enclosed in the `try` block.</span></span> <span data-ttu-id="37c4a-109">A `catch` deyimi eklenir hemen sonra işlemek üzere `IndexOutOfRangeException`, meydana gelmesi durumunda.</span><span class="sxs-lookup"><span data-stu-id="37c4a-109">A `catch` statement is added immediately after to handle `IndexOutOfRangeException`, if it occurs.</span></span> <span data-ttu-id="37c4a-110">`catch` Engelleme tanıtıcıları `IndexOutOfRangeException` ve daha uygun oluşturur `ArgumentOutOfRangeException` özel durum yerine.</span><span class="sxs-lookup"><span data-stu-id="37c4a-110">The `catch` block handles the `IndexOutOfRangeException` and throws the more appropriate `ArgumentOutOfRangeException` exception instead.</span></span> <span data-ttu-id="37c4a-111">Arayan mümkün olduğunca fazla bilgi sağlamak için özgün özel durum olarak belirtmeyi göz önünde bulundurun <xref:System.Exception.InnerException%2A> yeni özel durum.</span><span class="sxs-lookup"><span data-stu-id="37c4a-111">In order to provide the caller with as much information as possible, consider specifying the original exception as the <xref:System.Exception.InnerException%2A> of the new exception.</span></span> <span data-ttu-id="37c4a-112">Çünkü <xref:System.Exception.InnerException%2A> özelliği [readonly](../../../csharp/language-reference/keywords/readonly.md), yeni özel durum oluşturucuda atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="37c4a-112">Because the <xref:System.Exception.InnerException%2A> property is [readonly](../../../csharp/language-reference/keywords/readonly.md), you must assign it in the constructor of the new exception.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="37c4a-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="37c4a-113">See Also</span></span>  
 [<span data-ttu-id="37c4a-114">C# programlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="37c4a-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="37c4a-115">Özel durumlar ve özel durum işleme</span><span class="sxs-lookup"><span data-stu-id="37c4a-115">Exceptions and Exception Handling</span></span>](../../../csharp/programming-guide/exceptions/index.md)  
 [<span data-ttu-id="37c4a-116">Özel durum işleme</span><span class="sxs-lookup"><span data-stu-id="37c4a-116">Exception Handling</span></span>](../../../csharp/programming-guide/exceptions/exception-handling.md)