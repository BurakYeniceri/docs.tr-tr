---
title: "Düğüm alma dizine göre sıralanmış"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 5412c90f-2703-4aa8-a9c4-1b8a35183c37
caps.latest.revision: "4"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 780af689f6aff86e2e96738c356df4a81128f4ef
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/23/2017
---
# <a name="ordered-node-retrieval-by-index"></a><span data-ttu-id="8283b-102">Düğüm alma dizine göre sıralanmış</span><span class="sxs-lookup"><span data-stu-id="8283b-102">Ordered Node Retrieval by Index</span></span>
<span data-ttu-id="8283b-103">World Wide Web Konsorsiyumu (W3C) XML belge nesne modeli (DOM) tarafından işlenen sırasız kümesi aksine düğümleri sıralı bir listesi işleme yeteneği olan bir listesi ayrıca açıklanır **XmlNamedNodeMap**.</span><span class="sxs-lookup"><span data-stu-id="8283b-103">The World Wide Web Consortium (W3C) XML Document Object Model (DOM) also describes a NodeList, which has the ability to handle an ordered list of nodes, as opposed to the unordered set handled by the **XmlNamedNodeMap**.</span></span> <span data-ttu-id="8283b-104">Microsoft .NET Framework listesi adlı **XmlNodeList**.</span><span class="sxs-lookup"><span data-stu-id="8283b-104">The NodeList in the Microsoft .NET Framework is called **XmlNodeList**.</span></span> <span data-ttu-id="8283b-105">Yöntemleri ve döndüren özellikleri bir **XmlNodeList** şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8283b-105">Methods and properties that return an **XmlNodeList** are:</span></span>  
  
-   <span data-ttu-id="8283b-106">XmlNode.ChildNodes</span><span class="sxs-lookup"><span data-stu-id="8283b-106">XmlNode.ChildNodes</span></span>  
  
-   <span data-ttu-id="8283b-107">XmlDocument.GetElementsByTagName</span><span class="sxs-lookup"><span data-stu-id="8283b-107">XmlDocument.GetElementsByTagName</span></span>  
  
-   <span data-ttu-id="8283b-108">XmlElement.GetElementsByTagName</span><span class="sxs-lookup"><span data-stu-id="8283b-108">XmlElement.GetElementsByTagName</span></span>  
  
-   <span data-ttu-id="8283b-109">XmlNode.SelectNodes</span><span class="sxs-lookup"><span data-stu-id="8283b-109">XmlNode.SelectNodes</span></span>  
  
 <span data-ttu-id="8283b-110">**XmlNodeList** sahip bir **sayısı** düğümler üzerinden yineleme döngüler yazmak için kullanılan özellik **XmlNodeList**, aşağıdaki kod örneğinde gösterildiği gibi:</span><span class="sxs-lookup"><span data-stu-id="8283b-110">The **XmlNodeList** has a **Count** property that can be used to write loops to iterate over the nodes in the **XmlNodeList**, as shown in the following code sample:</span></span>  
  
```vb  
Dim doc as XmlDocument = new XmlDocument()  
   doc.Load("books.xml")  
  
    ' Retrieve all book titles.  
    Dim root as XmlElement = doc.DocumentElement  
    Dim elemList as XmlNodeList = root.GetElementsByTagName("title")  
    Dim i as integer  
    for i=0  to elemList.Count-1  
        ' Display all book titles in the Node List.  
        Console.WriteLine(elemList.ItemOf(i).InnerXml)  
    next  
```  
  
```csharp  
XmlDocument doc = new XmlDocument();  
doc.Load("books.xml");  
// Retrieve all book titles.  
XmlElement root = doc.DocumentElement;  
XmlNodeList elemList = root.GetElementsByTagName("title");  
for (int i=0; i < elemList.Count; i++)  
{     
   // Display all book titles in the Node List.  
   Console.WriteLine(elemList[i].InnerXml);  
}   
```  
  
 <span data-ttu-id="8283b-111">Ek olarak **sayısı** özelliği var. bir **GetEnumerator** sağlayan yöntemi `foreach` düğümler koleksiyon üzerinden yineleme stil **XmlNodeList**.</span><span class="sxs-lookup"><span data-stu-id="8283b-111">In addition to the **Count** property, there is a **GetEnumerator** method that provides a, `foreach` style iteration over the collection of nodes in the **XmlNodeList**.</span></span> <span data-ttu-id="8283b-112">Aşağıdaki kod örneğinde kullanımı gösterilmiştir `foreach` deyimi.</span><span class="sxs-lookup"><span data-stu-id="8283b-112">The following code example shows the use of the `foreach` statement.</span></span>  
  
```vb  
Dim doc As New XmlDocument()  
doc.Load("books.xml")  
  
' Get book titles.  
Dim root As XmlElement = doc.DocumentElement  
Dim elemList As XmlNodeList = root.GetElementsByTagName("title")  
Dim ienum As IEnumerator = elemList.GetEnumerator()  
' Loop over the XmlNodeList using the enumerator ienum          
While ienum.MoveNext()  
    ' Display the book title.  
    Dim title As XmlNode = CType(ienum.Current, XmlNode)  
    Console.WriteLine(title.InnerText)  
End While  
```  
  
```csharp  
{  
     XmlDocument doc = new XmlDocument();  
     doc.Load("books.xml");  
  
     // Get book titles.  
     XmlElement root = doc.DocumentElement;  
     XmlNodeList elemList = root.GetElementsByTagName("title");  
     IEnumerator ienum = elemList.GetEnumerator();    
     // Loop over the XmlNodeList using the enumerator ienum          
     while (ienum.MoveNext())  
     {  
          // Display the book title.  
           XmlNode title = (XmlNode) ienum.Current;  
           Console.WriteLine(title.InnerText);  
     }  
  }  
```  
  
 <span data-ttu-id="8283b-113">Kullanılabilir özellikler ve yöntemler hakkında daha fazla bilgi için **XmlNodeList**, bkz: <xref:System.Xml.XmlNodeList>.</span><span class="sxs-lookup"><span data-stu-id="8283b-113">For more information on the methods and properties available on the **XmlNodeList**, see <xref:System.Xml.XmlNodeList>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8283b-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="8283b-114">See Also</span></span>  
 [<span data-ttu-id="8283b-115">XML Belge Nesne Modeli (DOM)</span><span class="sxs-lookup"><span data-stu-id="8283b-115">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
