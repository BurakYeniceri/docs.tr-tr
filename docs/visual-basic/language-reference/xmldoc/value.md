---
title: "&lt;değer&gt; (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- <value> XML tag
- value XML tag
ms.assetid: 0b84b02e-9e6d-41b5-a926-0d5dc76dacb5
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: a72c6330596e59d26fbae9d13f6b9c8b1987e519
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="ltvaluegt-visual-basic"></a><span data-ttu-id="5edf4-102">&lt;değer&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5edf4-102">&lt;value&gt; (Visual Basic)</span></span>
<span data-ttu-id="5edf4-103">Bir özelliğin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5edf4-103">Specifies the description of a property.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5edf4-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="5edf4-104">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5edf4-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="5edf4-105">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="5edf4-106">Özelliği için bir açıklama.</span><span class="sxs-lookup"><span data-stu-id="5edf4-106">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5edf4-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="5edf4-107">Remarks</span></span>  
 <span data-ttu-id="5edf4-108">Kullanım `<value>` bir özelliğini açıklamak için etiket.</span><span class="sxs-lookup"><span data-stu-id="5edf4-108">Use the `<value>` tag to describe a property.</span></span> <span data-ttu-id="5edf4-109">Visual Studio geliştirme ortamında kod Sihirbazı'nı kullanarak bir özelliği eklediğinizde, onu ekleyeceksiniz Not bir [ \<Özet >](../../../visual-basic/language-reference/xmldoc/summary.md) yeni özellik için etiketi.</span><span class="sxs-lookup"><span data-stu-id="5edf4-109">Note that when you add a property using the code wizard in the Visual Studio development environment, it will add a [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="5edf4-110">Daha sonra el ile eklemeniz bir `<value>` özelliği temsil eden bir değeri açıklamak için etiket.</span><span class="sxs-lookup"><span data-stu-id="5edf4-110">You should then manually add a `<value>` tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="5edf4-111">İle derleme [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) bir dosyaya işlem belgesi açıklamaları için.</span><span class="sxs-lookup"><span data-stu-id="5edf4-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5edf4-112">Örnek</span><span class="sxs-lookup"><span data-stu-id="5edf4-112">Example</span></span>  
 <span data-ttu-id="5edf4-113">Bu örnekte `<value>` hangi değeri açıklamak için etiket `Counter` özelliği ayrı tutma.</span><span class="sxs-lookup"><span data-stu-id="5edf4-113">This example uses the `<value>` tag to describe what value the `Counter` property holds.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/value_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="5edf4-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5edf4-114">See Also</span></span>  
 [<span data-ttu-id="5edf4-115">XML açıklama etiketleri</span><span class="sxs-lookup"><span data-stu-id="5edf4-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
