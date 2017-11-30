---
title: "Hatalı kayıt numarası"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vbrID63
ms.assetid: 1fcc33f8-822a-4de9-a6e3-228ddb5824a6
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: be04987353498775ec7dcef50b6acc1e6b4ec149
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="bad-record-number"></a><span data-ttu-id="bfa03-102">Hatalı kayıt numarası</span><span class="sxs-lookup"><span data-stu-id="bfa03-102">Bad record number</span></span>
<span data-ttu-id="bfa03-103">Kayıt sayısı `a FileGet`, `FilePut`, `FileGetObject`, veya `FilePutObject` açıklamadır sıfıra eşit veya daha az.</span><span class="sxs-lookup"><span data-stu-id="bfa03-103">The record number in `a FileGet`, `FilePut`, `FileGetObject`, or `FilePutObject` statement is less than or equal to zero.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="bfa03-104">Bu hatayı düzeltmek için</span><span class="sxs-lookup"><span data-stu-id="bfa03-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="bfa03-105">Kayıt sayısı oluşturmak için kullanılan hesaplama denetleyin.</span><span class="sxs-lookup"><span data-stu-id="bfa03-105">Check the calculations used in generating the record number.</span></span> <span data-ttu-id="bfa03-106">Kayıt sayısını içeren veya kayıt sayıları hesaplamak için kullanılan değişken yazımını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="bfa03-106">Verify spelling of the variables containing the record number or used in calculating record numbers.</span></span> <span data-ttu-id="bfa03-107">Yanlış yazılmış bir değişken adı örtük olarak bildirilen ve kullandığınız sürece, sıfıra başlatıldı `Option Explicit On` modülünde.</span><span class="sxs-lookup"><span data-stu-id="bfa03-107">A misspelled variable name is implicitly declared and initialized to zero, unless you used `Option Explicit On` in the module.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bfa03-108">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="bfa03-108">See Also</span></span>  
 [<span data-ttu-id="bfa03-109">Option Explicit deyimi</span><span class="sxs-lookup"><span data-stu-id="bfa03-109">Option Explicit Statement</span></span>](../../visual-basic/language-reference/statements/option-explicit-statement.md)
