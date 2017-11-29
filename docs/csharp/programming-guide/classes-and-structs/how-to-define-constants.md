---
title: "Nasıl yapılır: C# İçinde Sabitleri Tanımlama"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- C# language, constants
- constants [C#]
ms.assetid: 43f511be-346c-4b8a-995e-aded94542ece
caps.latest.revision: "7"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: ff12d0b6882289da9ed924f1c7de00edc5dc1e2e
ms.sourcegitcommit: 7e99f66ef09d2903e22c789c67ff5a10aa953b2f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2017
---
# <a name="how-to-define-constants-in-c"></a><span data-ttu-id="4afb7-102">Nasıl yapılır: C# İçinde Sabitleri Tanımlama</span><span class="sxs-lookup"><span data-stu-id="4afb7-102">How to: Define Constants in C#</span></span>
<span data-ttu-id="4afb7-103">Sabit değerleri belirlenmiş alanları derleme zamanı ve hiçbir zaman değiştirilemez vardır.</span><span class="sxs-lookup"><span data-stu-id="4afb7-103">Constants are fields whose values are set at compile time and can never be changed.</span></span> <span data-ttu-id="4afb7-104">Sabitler sayısal değişmez değerleri ("Sihirli sayı") yerine anlamlı bir ad için özel değerler sağlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="4afb7-104">Use constants to provide meaningful names instead of numeric literals ("magic numbers") for special values.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4afb7-105">C# [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) önişlemci yönergesi, genellikle C ve C++ kullanılan şekilde sabitleri tanımlamak için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4afb7-105">In C# the [#define](../../../csharp/language-reference/preprocessor-directives/preprocessor-define.md) preprocessor directive cannot be used to define constants in the way that is typically used in C and C++.</span></span>  
  
 <span data-ttu-id="4afb7-106">Tam sayı türleri sabit değerleri tanımlamak için (`int`, `byte`, vb.) bir numaralandırılmış türünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="4afb7-106">To define constant values of integral types (`int`, `byte`, and so on) use an enumerated type.</span></span> <span data-ttu-id="4afb7-107">Daha fazla bilgi için bkz: [enum](../../../csharp/language-reference/keywords/enum.md).</span><span class="sxs-lookup"><span data-stu-id="4afb7-107">For more information, see [enum](../../../csharp/language-reference/keywords/enum.md).</span></span>  
  
 <span data-ttu-id="4afb7-108">İntegral olmayan sabitleri tanımlamak için adlı tek bir statik sınıf grup için bir yaklaşım ise `Constants`.</span><span class="sxs-lookup"><span data-stu-id="4afb7-108">To define non-integral constants, one approach is to group them in a single static class named `Constants`.</span></span> <span data-ttu-id="4afb7-109">Bu sınıf adıyla sabitlere yapılan tüm başvurular başında aşağıdaki örnekte gösterildiği gibi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4afb7-109">This will require that all references to the constants be prefaced with the class name, as shown in the following example.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4afb7-110">Örnek</span><span class="sxs-lookup"><span data-stu-id="4afb7-110">Example</span></span>  
 [!code-csharp[csProgGuideObjects#89](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-define-constants_1.cs)]  
  
 <span data-ttu-id="4afb7-111">Sınıf adı niteleyici kullanımını sizin ve başkalarının sabiti kullanan sabittir ve değiştirilemez anladığınızdan emin olun yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="4afb7-111">The use of the class name qualifier helps ensure that you and others who use the constant understand that it is constant and cannot be modified.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4afb7-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4afb7-112">See Also</span></span>  
 [<span data-ttu-id="4afb7-113">Sınıflar ve yapılar</span><span class="sxs-lookup"><span data-stu-id="4afb7-113">Classes and Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/index.md)
