---
title: 'Nasıl yapılır: bir alt öğe (XPath-LINQ-XML) listesi Bul (C#)'
ms.date: 07/20/2015
ms.assetid: 7c589dd8-f680-4cdb-9d6a-78d57e2555e8
ms.openlocfilehash: 742b0843e3287bd8de6c7b1f5d3706d66e5d344f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33340053"
---
# <a name="how-to-find-a-list-of-child-elements-xpath-linq-to-xml-c"></a><span data-ttu-id="791a8-102">Nasıl yapılır: bir alt öğe (XPath-LINQ-XML) listesi Bul (C#)</span><span class="sxs-lookup"><span data-stu-id="791a8-102">How to: Find a List of Child Elements (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="791a8-103">Bu konuda XPath alt öğeleri eksene karşılaştırır [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <xref:System.Xml.Linq.XContainer.Elements%2A> ekseni.</span><span class="sxs-lookup"><span data-stu-id="791a8-103">This topic compares the XPath child elements axis to the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] <xref:System.Xml.Linq.XContainer.Elements%2A> axis.</span></span>  
  
 <span data-ttu-id="791a8-104">XPath ifadesi şöyledir: `./*`</span><span class="sxs-lookup"><span data-stu-id="791a8-104">The XPath expression is: `./*`</span></span>  
  
## <a name="example"></a><span data-ttu-id="791a8-105">Örnek</span><span class="sxs-lookup"><span data-stu-id="791a8-105">Example</span></span>  
 <span data-ttu-id="791a8-106">Bu örnekte tüm alt öğeleri bulur `Address` öğesi.</span><span class="sxs-lookup"><span data-stu-id="791a8-106">This example finds all of the child elements of the `Address` element.</span></span>  
  
 <span data-ttu-id="791a8-107">Bu örnekte aşağıdaki XML belgesi kullanır: [örnek XML dosyası: birden çok satınalma siparişi (LINQ-XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="791a8-107">This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span></span>  
  
```csharp  
XDocument cpo = XDocument.Load("PurchaseOrders.xml");  
XElement po = cpo.Root.Element("PurchaseOrder").Element("Address");  
  
// LINQ to XML query  
IEnumerable<XElement> list1 = po.Elements();  
  
// XPath expression  
IEnumerable<XElement> list2 = po.XPathSelectElements("./*");  
  
if (list1.Count() == list2.Count() &&  
        list1.Intersect(list2).Count() == list1.Count())  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
foreach (XElement el in list1)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="791a8-108">Bu örnek şu çıkışı üretir:</span><span class="sxs-lookup"><span data-stu-id="791a8-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
<Name>Ellen Adams</Name>  
<Street>123 Maple Street</Street>  
<City>Mill Valley</City>  
<State>CA</State>  
<Zip>10999</Zip>  
<Country>USA</Country>  
```  
  
## <a name="see-also"></a><span data-ttu-id="791a8-109">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="791a8-109">See Also</span></span>  
 [<span data-ttu-id="791a8-110">LINQ-XML XPath kullanıcıların (C#)</span><span class="sxs-lookup"><span data-stu-id="791a8-110">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
