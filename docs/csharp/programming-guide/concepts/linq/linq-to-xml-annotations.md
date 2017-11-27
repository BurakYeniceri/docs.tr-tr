---
title: LINQ-XML Annotations3
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-csharp
ms.topic: article
ms.assetid: 54e7b9d0-07f5-488f-9065-b6e6b870f810
caps.latest.revision: "3"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: eadbc55ac6188fa3634745bf8bb222f07675a308
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="linq-to-xml-annotations"></a><span data-ttu-id="18c41-102">LINQ-XML ek açıklamaları</span><span class="sxs-lookup"><span data-stu-id="18c41-102">LINQ to XML Annotations</span></span>
<span data-ttu-id="18c41-103">Ek açıklamalar [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] herhangi bir rastgele nesne rasgele herhangi bir türde bir XML ağacındaki herhangi bir XML bileşeni ilişkilendirmek olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="18c41-103">Annotations in [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] enable you to associate any arbitrary object of any arbitrary type with any XML component in an XML tree.</span></span>  
  
 <span data-ttu-id="18c41-104">Ek açıklamanın bir XML bileşene gibi eklemek için bir <xref:System.Xml.Linq.XElement> veya <xref:System.Xml.Linq.XAttribute>, çağırmanız <xref:System.Xml.Linq.XObject.AddAnnotation%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="18c41-104">To add an annotation to an XML component, such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XAttribute>, you call the <xref:System.Xml.Linq.XObject.AddAnnotation%2A> method.</span></span> <span data-ttu-id="18c41-105">Türe göre ek açıklamalarını alır.</span><span class="sxs-lookup"><span data-stu-id="18c41-105">You retrieve annotations by type.</span></span>  
  
 <span data-ttu-id="18c41-106">Ek Açıklamalar XML bilgi parçası olmadığını unutmayın; Bunlar seri durumdan veya güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="18c41-106">Note that annotations are not part of the XML infoset; they are not serialized or deserialized.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="18c41-107">Yöntemler</span><span class="sxs-lookup"><span data-stu-id="18c41-107">Methods</span></span>  
 <span data-ttu-id="18c41-108">Ek açıklamalar ile çalışırken aşağıdaki yöntemleri kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="18c41-108">You can use the following methods when working with annotations:</span></span>  
  
|<span data-ttu-id="18c41-109">Yöntem</span><span class="sxs-lookup"><span data-stu-id="18c41-109">Method</span></span>|<span data-ttu-id="18c41-110">Açıklama</span><span class="sxs-lookup"><span data-stu-id="18c41-110">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.Linq.XObject.AddAnnotation%2A>|<span data-ttu-id="18c41-111">Ek açıklama listesine bir nesne ekler bir <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="18c41-111">Adds an object to the annotation list of an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.Annotation%2A>|<span data-ttu-id="18c41-112">Belirtilen türden ilk ek açıklama nesnesinin alır bir <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="18c41-112">Gets the first annotation object of the specified type from an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.Annotations%2A>|<span data-ttu-id="18c41-113">Belirtilen tür için ek açıklamalar koleksiyonunu alır bir <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="18c41-113">Gets a collection of annotations of the specified type for an <xref:System.Xml.Linq.XObject>.</span></span>|  
|<xref:System.Xml.Linq.XObject.RemoveAnnotations%2A>|<span data-ttu-id="18c41-114">Belirtilen türden ek açıklamalar kaldırır bir <xref:System.Xml.Linq.XObject>.</span><span class="sxs-lookup"><span data-stu-id="18c41-114">Removes the annotations of the specified type from an <xref:System.Xml.Linq.XObject>.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="18c41-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="18c41-115">See Also</span></span>  
 [<span data-ttu-id="18c41-116">Gelişmiş LINQ-XML programlama (C#)</span><span class="sxs-lookup"><span data-stu-id="18c41-116">Advanced LINQ to XML Programming (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/advanced-linq-to-xml-programming.md)
