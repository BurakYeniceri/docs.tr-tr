---
title: (Çağrılıyor XSLT) XmlReader'a serileştirme (Visual Basic)
ms.date: 07/20/2015
ms.assetid: 8b64f95a-e8f6-40f7-99f9-a8002c63af96
ms.openlocfilehash: 05754593f4f30683ffabecaa8e16c35bf836a3f8
ms.sourcegitcommit: 2d8b7488d94101b534ca3e9780b1c1e840233405
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2018
ms.locfileid: "39198852"
---
# <a name="serializing-to-an-xmlreader-invoking-xslt-visual-basic"></a><span data-ttu-id="7f048-102">(Çağrılıyor XSLT) XmlReader'a serileştirme (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7f048-102">Serializing to an XmlReader (Invoking XSLT) (Visual Basic)</span></span>
<span data-ttu-id="7f048-103">Kullanırken <xref:System.Xml?displayProperty=nameWithType> birlikte çalışabilirlik özelliklerini [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], kullanabileceğiniz <xref:System.Xml.Linq.XNode.CreateReader%2A> oluşturmak için bir <xref:System.Xml.XmlReader>.</span><span class="sxs-lookup"><span data-stu-id="7f048-103">When you use the <xref:System.Xml?displayProperty=nameWithType> interoperability capabilities of [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)], you can use <xref:System.Xml.Linq.XNode.CreateReader%2A> to create an <xref:System.Xml.XmlReader>.</span></span> <span data-ttu-id="7f048-104">Buradan okur Modülü <xref:System.Xml.XmlReader> XML ağacından düğümleri okur ve bunları uygun şekilde işler.</span><span class="sxs-lookup"><span data-stu-id="7f048-104">The module that reads from this <xref:System.Xml.XmlReader> reads the nodes from the XML tree and processes them accordingly.</span></span>  
  
## <a name="invoking-an-xslt-transformation"></a><span data-ttu-id="7f048-105">XSLT dönüşümü çağırma</span><span class="sxs-lookup"><span data-stu-id="7f048-105">Invoking an XSLT Transformation</span></span>  
 <span data-ttu-id="7f048-106">Bu yöntem bir olası kullanım XSLT dönüştürmesi çağrılırken içindir.</span><span class="sxs-lookup"><span data-stu-id="7f048-106">One possible use for this method is when invoking an XSLT transformation.</span></span> <span data-ttu-id="7f048-107">Bir XML ağacı oluşturma, oluşturun bir <xref:System.Xml.XmlReader> XML ağacından bir yeni belge oluşturun ve ardından oluşturmak bir <xref:System.Xml.XmlWriter> yeni belgesine yazılacak.</span><span class="sxs-lookup"><span data-stu-id="7f048-107">You can create an XML tree, create an <xref:System.Xml.XmlReader> from the XML tree, create a new document, and then create an <xref:System.Xml.XmlWriter> to write into the new document.</span></span> <span data-ttu-id="7f048-108">Öğesinde geçen XSLT dönüşümü, daha sonra çağırabilirsiniz <xref:System.Xml.XmlReader> ve <xref:System.Xml.XmlWriter>.</span><span class="sxs-lookup"><span data-stu-id="7f048-108">Then, you can invoke the XSLT transformation, passing in <xref:System.Xml.XmlReader> and <xref:System.Xml.XmlWriter>.</span></span> <span data-ttu-id="7f048-109">Dönüştürme başarıyla tamamlandıktan sonra yeni bir XML ağacı dönüşümü sonuçları ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="7f048-109">After the transformation successfully completes, the new XML tree is populated with the results of the transformation.</span></span>  
  
```vb  
Dim xslMarkup As XDocument = _  
    <?xml version='1.0'?>  
    <xsl:stylesheet xmlns:xsl='http://www.w3.org/1999/XSL/Transform' version='1.0'>  
        <xsl:template match='/Parent'>  
            <Root>  
                <C1>  
                    <xsl:value-of select='Child1'/>  
                </C1>  
                <C2>  
                    <xsl:value-of select='Child2'/>  
                </C2>  
            </Root>  
        </xsl:template>  
    </xsl:stylesheet>  
  
Dim xmlTree As XDocument = _  
    <?xml version='1.0'?>  
    <Parent>  
        <Child1>Child1 data</Child1>  
        <Child2>Child2 data</Child2>  
    </Parent>  
  
Dim newTree As XDocument = New XDocument()  
Using writer As XmlWriter = newTree.CreateWriter()  
    ' Load the style sheet.  
    Dim xslt As XslCompiledTransform = New XslCompiledTransform()  
    xslt.Load(xslMarkup.CreateReader())  
  
    ' Execute the transformation and output the results to a writer.  
    xslt.Transform(xmlTree.CreateReader(), writer)  
End Using  
  
Console.WriteLine(newTree)  
```  
  
 <span data-ttu-id="7f048-110">Bu örnek aşağıdaki çıktıyı üretir:</span><span class="sxs-lookup"><span data-stu-id="7f048-110">This example produces the following output:</span></span>  
  
```xml  
<Root>  
  <C1>Child1 data</C1>  
  <C2>Child2 data</C2>  
</Root>  
```  
  
## <a name="see-also"></a><span data-ttu-id="7f048-111">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="7f048-111">See Also</span></span>  
 [<span data-ttu-id="7f048-112">(Visual Basic) XML ağaçlarını serileştirme</span><span class="sxs-lookup"><span data-stu-id="7f048-112">Serializing XML Trees (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/serializing-xml-trees.md)
