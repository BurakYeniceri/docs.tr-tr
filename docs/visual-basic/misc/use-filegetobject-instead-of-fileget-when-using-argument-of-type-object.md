---
title: "&#39;kullan; FileGetObject &#39; yerine &#39; FileGet &#39; bağımsız değişken türü &#39; nesne &#39;kullanırken;"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
ms.assetid: 090b8088-895a-482a-9362-606596bac304
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 996e8a50f90c738bbc64c200125a785c0e9bcd58
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="use-39filegetobject39-instead-of-39fileget39-when-using-argument-of-type-39object39"></a><span data-ttu-id="e5704-102">&#39;kullan; FileGetObject &#39; yerine &#39; FileGet &#39; bağımsız değişken türü &#39; nesne &#39;kullanırken;</span><span class="sxs-lookup"><span data-stu-id="e5704-102">Use &#39;FileGetObject&#39; instead of &#39;FileGet&#39; when using argument of type &#39;Object&#39;</span></span>
<span data-ttu-id="e5704-103">`FileGet` Yöntemi içerir türünde bir bağımsız değişken `Object`.</span><span class="sxs-lookup"><span data-stu-id="e5704-103">The `FileGet` method includes an argument of type `Object`.</span></span> <span data-ttu-id="e5704-104">`FileGetObject`yerine kullanılmalıdır `FileGet` belirsizlikleri önlemek için.</span><span class="sxs-lookup"><span data-stu-id="e5704-104">`FileGetObject` should be used in place of `FileGet` to avoid ambiguities.</span></span>  
  
 <span data-ttu-id="e5704-105">İşlevselliği sunduğu bildirimi `My.Computer.Filesystem` büyük kullanım kolaylığı ve performans ya da daha sunar `FileGet` veya `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="e5704-105">Notice that the functionality offered by `My.Computer.Filesystem` offers greater ease of use and performance than either `FileGet` or `FileGetObject`.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e5704-106">Bu hatayı düzeltmek için</span><span class="sxs-lookup"><span data-stu-id="e5704-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="e5704-107">Değiştir `FileGet` ile `FileGetObject`.</span><span class="sxs-lookup"><span data-stu-id="e5704-107">Replace `FileGet` with `FileGetObject`.</span></span>  
  
2.  <span data-ttu-id="e5704-108">Cast `Object` daha belirli bir tür bağımsız değişkeni.</span><span class="sxs-lookup"><span data-stu-id="e5704-108">Cast the `Object` argument to a more specific type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5704-109">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e5704-109">See Also</span></span>  
 [<span data-ttu-id="e5704-110">IN derleme değil: FileGetObject işlevi</span><span class="sxs-lookup"><span data-stu-id="e5704-110">NOT IN BUILD: FileGetObject Function</span></span>](http://msdn.microsoft.com/en-us/3eda786b-d1ee-4b44-9dd7-0ea6bff072c0)  
 [<span data-ttu-id="e5704-111">My.Computer.FileSystem nesnesi</span><span class="sxs-lookup"><span data-stu-id="e5704-111">My.Computer.FileSystem Object</span></span>](../../visual-basic/language-reference/objects/my-computer-filesystem-object.md)
