---
title: Kullanım &#39;FileGetObject&#39; yerine &#39;FileGet&#39; türünde bağımsız değişken kullanırken &#39;nesnesi&#39;
ms.date: 07/20/2015
ms.assetid: 090b8088-895a-482a-9362-606596bac304
ms.openlocfilehash: 2edb80f6df95774e0ea5a7b51e57925845d7ba75
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33640423"
---
# <a name="use-39filegetobject39-instead-of-39fileget39-when-using-argument-of-type-39object39"></a><span data-ttu-id="ad80e-102">Kullanım &#39;FileGetObject&#39; yerine &#39;FileGet&#39; türünde bağımsız değişken kullanırken &#39;nesnesi&#39;</span><span class="sxs-lookup"><span data-stu-id="ad80e-102">Use &#39;FileGetObject&#39; instead of &#39;FileGet&#39; when using argument of type &#39;Object&#39;</span></span>
<span data-ttu-id="ad80e-103">`FileGet` Yöntemi içerir türünde bir bağımsız değişken `Object`.</span><span class="sxs-lookup"><span data-stu-id="ad80e-103">The `FileGet` method includes an argument of type `Object`.</span></span> <span data-ttu-id="ad80e-104">`FileGetObject` yerine kullanılmalıdır `FileGet` belirsizlikleri önlemek için.</span><span class="sxs-lookup"><span data-stu-id="ad80e-104">`FileGetObject` should be used in place of `FileGet` to avoid ambiguities.</span></span>  
  
 <span data-ttu-id="ad80e-105">İşlevselliği sunduğu bildirimi `My.Computer.Filesystem` büyük kullanım kolaylığı ve performans ya da daha sunar `FileGet` veya `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="ad80e-105">Notice that the functionality offered by `My.Computer.Filesystem` offers greater ease of use and performance than either `FileGet` or `FileGetObject`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="ad80e-106">Bu hatayı düzeltmek için</span><span class="sxs-lookup"><span data-stu-id="ad80e-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="ad80e-107">Değiştir `FileGet` ile `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="ad80e-107">Replace `FileGet` with `FileGetObject`.</span></span>  
  
2.  <span data-ttu-id="ad80e-108">Cast `Object` daha belirli bir tür bağımsız değişkeni.</span><span class="sxs-lookup"><span data-stu-id="ad80e-108">Cast the `Object` argument to a more specific type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad80e-109">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ad80e-109">See Also</span></span>  
   
 [<span data-ttu-id="ad80e-110">My.Computer.FileSystem</span><span class="sxs-lookup"><span data-stu-id="ad80e-110">My.Computer.FileSystem</span></span>](xref:Microsoft.VisualBasic.FileIO.FileSystem)
