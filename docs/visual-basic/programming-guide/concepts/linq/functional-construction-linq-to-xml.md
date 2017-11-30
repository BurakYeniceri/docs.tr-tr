---
title: "İşlev yapımı (LINQ-XML) (Visual Basic)"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: feac4273-39ab-43ae-bab7-4059c807a785
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d5c68fb71fd59d08574cee9eec933cee25e504d9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="functional-construction-linq-to-xml-visual-basic"></a><span data-ttu-id="6a3d0-102">İşlev yapımı (LINQ-XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6a3d0-102">Functional Construction (LINQ to XML) (Visual Basic)</span></span>
[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)]<span data-ttu-id="6a3d0-103">adlı XML öğeleri oluşturmak için güçlü bir yol sağlar *işlevsel yapım*.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-103"> provides a powerful way to create XML elements called *functional construction*.</span></span> <span data-ttu-id="6a3d0-104">Bir XML ağacı tek bir deyimde oluşturabilme işlevsel yapıdır.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-104">Functional construction is the ability to create an XML tree in a single statement.</span></span>  
  
 <span data-ttu-id="6a3d0-105">Birkaç temel özellikleri vardır [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] işlevsel yapım etkinleştirmek programlama arabirimi:</span><span class="sxs-lookup"><span data-stu-id="6a3d0-105">There are several key features of the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] programming interface that enable functional construction:</span></span>  
  
-   <span data-ttu-id="6a3d0-106"><xref:System.Xml.Linq.XElement> Oluşturucusu çeşitli içerik için bağımsız değişkenleri alır.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-106">The <xref:System.Xml.Linq.XElement> constructor takes various types of arguments for content.</span></span> <span data-ttu-id="6a3d0-107">Örneğin, başka bir geçirebilirsiniz <xref:System.Xml.Linq.XElement> bir alt öğesi olur nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-107">For example, you can pass another <xref:System.Xml.Linq.XElement> object, which becomes a child element.</span></span> <span data-ttu-id="6a3d0-108">Geçirebilirsiniz bir <xref:System.Xml.Linq.XAttribute> öğesinin özniteliği hale nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-108">You can pass an <xref:System.Xml.Linq.XAttribute> object, which becomes an attribute of the element.</span></span> <span data-ttu-id="6a3d0-109">Veya herhangi bir dizeye dönüştürülür ve öğenin metin içeriğini olur, nesne türü geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-109">Or you can pass any other type of object, which is converted to a string and becomes the text content of the element.</span></span>  
  
-   <span data-ttu-id="6a3d0-110"><xref:System.Xml.Linq.XElement> Oluşturucusu geçen bir `params` türünde dizi <xref:System.Object>, böylece oluşturucuya herhangi bir sayıda nesnelerini geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-110">The <xref:System.Xml.Linq.XElement> constructor takes a `params` array of type <xref:System.Object>, so that you can pass any number of objects to the constructor.</span></span> <span data-ttu-id="6a3d0-111">Bu, karmaşık içeriğe sahip bir öğe oluşturmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-111">This enables you to create an element that has complex content.</span></span>  
  
-   <span data-ttu-id="6a3d0-112">Bir nesne uyguluyorsa <xref:System.Collections.Generic.IEnumerable%601>nesne koleksiyonunda numaralandırılan ve koleksiyondaki tüm öğeleri eklenir.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-112">If an object implements <xref:System.Collections.Generic.IEnumerable%601>, the collection in the object is enumerated, and all items in the collection are added.</span></span> <span data-ttu-id="6a3d0-113">Koleksiyon içeriyorsa <xref:System.Xml.Linq.XElement> veya <xref:System.Xml.Linq.XAttribute> nesneleri, koleksiyondaki her öğe ayrı olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-113">If the collection contains <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XAttribute> objects, each item in the collection is added separately.</span></span> <span data-ttu-id="6a3d0-114">Sonuçlarını geçirmenize olanak tanır bu önemlidir, çünkü bir [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] sorgu oluşturucuya.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-114">This is important because it lets you pass the results of a [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] query to the constructor.</span></span>  
  
 <span data-ttu-id="6a3d0-115">Bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="6a3d0-115">The following is an example:</span></span>  
  
 <span data-ttu-id="6a3d0-116">Bir XML ağacı oluşturmak için ve ayrıca sonuçlarını kullanan kodu yazmak için XML değişmez değerleri kullanarak kod yazmak için bu özellikleri etkinleştirmek [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] sorgular bir XML ağacı oluşturduğunuzda:</span><span class="sxs-lookup"><span data-stu-id="6a3d0-116">These features enable you to write code using XML literals to create an XML tree, and also to write code that uses the results of [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] queries when you create an XML tree:</span></span>  
  
```vb  
Dim srcTree As XElement = _  
    <Root>  
        <Element>1</Element>  
        <Element>2</Element>  
        <Element>3</Element>  
        <Element>4</Element>  
        <Element>5</Element>  
    </Root>  
Dim xmlTree As XElement = _  
    <Root>  
        <Child>1</Child>  
        <Child>2</Child>  
        <%= From el In srcTree.Elements() _  
            Where CInt(el) > 2 _  
            Select el %>  
    </Root>  
Console.WriteLine(xmlTree)  
```  
  
 <span data-ttu-id="6a3d0-117">Bu örnek şu çıkışı üretir:</span><span class="sxs-lookup"><span data-stu-id="6a3d0-117">This example produces the following output:</span></span>  
  
```xml  
<Root>  
  <Child>1</Child>  
  <Child>2</Child>  
  <Element>3</Element>  
  <Element>4</Element>  
  <Element>5</Element>  
</Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6a3d0-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="6a3d0-118">See Also</span></span>  
 [<span data-ttu-id="6a3d0-119">Oluşturma XML ağaçları (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="6a3d0-119">Creating XML Trees (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/creating-xml-trees.md)