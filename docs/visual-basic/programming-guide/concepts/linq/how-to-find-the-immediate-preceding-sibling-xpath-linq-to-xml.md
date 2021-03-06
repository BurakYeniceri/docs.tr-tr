---
title: 'Nasıl yapılır: önceki eşdüzeyi (XPath-LINQ to XML) bulunamadı (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: ec046283-9fe2-4440-b295-860bf700099d
ms.openlocfilehash: 47ba557343d0f691c2ee0f2c56102df313ecfb30
ms.sourcegitcommit: f6343b070f3c66877338a05c8bfb0be9985255e2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/24/2018
ms.locfileid: "39220928"
---
# <a name="how-to-find-the-immediate-preceding-sibling-xpath-linq-to-xml-visual-basic"></a>Nasıl yapılır: önceki eşdüzeyi (XPath-LINQ to XML) bulunamadı (Visual Basic)
Bazen bir düğüme önceki eşdüzeyi bulma istersiniz. XPath başlangıcı yerine sonundan önceki eşdüzey eksenleri için konumsal doğrulamaları semantiği fark nedeniyle [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], bu daha ilgi çekici karşılaştırmalar biridir.  
  
## <a name="example"></a>Örnek  
 Bu örnekte, [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] sorgu kullandığı <xref:System.Linq.Enumerable.Last%2A> son düğümü tarafından döndürülen bir koleksiyonda bulunacak işleci <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A>. Aksine, XPath ifadesi hemen önceki öğeyi bulmak için 1 değerini bir koşul kullanır.  
  
```vb  
Dim root As XElement = _   
    <Root>  
        <Child1/>  
        <Child2/>  
        <Child3/>  
        <Child4/>  
    </Root>  
Dim child4 As XElement = root.Element("Child4")  
  
' LINQ to XML query  
Dim el1 As XElement = child4.ElementsBeforeSelf().Last()  
  
' XPath expression  
Dim el2 As XElement = _  
    DirectCast(child4.XPathEvaluate("preceding-sibling::*[1]"),  _  
    IEnumerable).Cast(Of XElement)().First()  
  
If el1 Is el2 Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
Console.WriteLine(el1)  
```  
  
 Bu örnek aşağıdaki çıktıyı üretir:  
  
```  
Results are identical  
<Child3 />  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [LINQ to XML için XPath kullanıcıları (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
