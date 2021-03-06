---
title: (C#) WordprocessingML belgelerinin şekli
ms.date: 07/20/2015
ms.assetid: 3791b5e0-c502-469b-bb75-a7bf6fdd0a94
ms.openlocfilehash: aeb047f23f60ba6951950a85a6e2ef57fcbd9dda
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46002963"
---
# <a name="shape-of-wordprocessingml-documents-c"></a>(C#) WordprocessingML belgelerinin şekli
Bu konu, WordprocessingML belgesinin XML şeklini tanıtır.  
  
## <a name="microsoft-office-formats"></a>Microsoft Office biçimleri  
 Office Open XML (Open XML yaygın olarak adlandırılır) 2007 Microsoft Office sistemi için yerel dosya biçimidir. Açık XML'dir biçimi XML tabanlı bir Ecma standart ve şu anda ISO IEC standartları sürecinden. Open XML içinde sözcük işleme dosyaları için biçimlendirme dili WordprocessingML çağrılır. Bu öğreticide WordprocessingML kaynak dosyaları örnekler için giriş olarak kullanılır.  
  
 Microsoft Office 2003 kullanıyorsanız, Word, Excel ve PowerPoint 2007 dosya biçimleri için Microsoft Office Uyumluluk Paketi yüklediyseniz, belgeleri Office Open XML biçiminde kaydedebilirsiniz.  
  
## <a name="the-shape-of-wordprocessingml-documents"></a>WordprocessingML belgelerinin şekli  
 WordprocessingML belgelerinin şekli anlamak için ilk şeydir. WordprocessingML belgesinin gövde öğesi içeren (adlı `w:body`) belgenin paragrafları içeren. Her bir paragrafına içeren bir veya daha fazla metin çalışıyor (adlı `w:r`). Çalıştıran her metin içeren bir veya daha fazla metin parçaları (adlı `w:t`).  
  
 Çok basit WordprocessingML belgesinin verilmiştir:  
  
```xml  
<?xml version="1.0" encoding="utf-8" standalone="yes"?>  
<w:document  
xmlns:ve="http://schemas.openxmlformats.org/markup-compatibility/2006"  
xmlns:o="urn:schemas-microsoft-com:office:office"  
xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"  
xmlns:m="http://schemas.openxmlformats.org/officeDocument/2006/math"  
xmlns:v="urn:schemas-microsoft-com:vml"  
xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"  
xmlns:w10="urn:schemas-microsoft-com:office:word"  
xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"  
xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml">  
  <w:body>  
    <w:p w:rsidR="00E22EB6"  
         w:rsidRDefault="00E22EB6">  
      <w:r>  
        <w:t>This is a paragraph.</w:t>  
      </w:r>  
    </w:p>  
    <w:p w:rsidR="00E22EB6"  
         w:rsidRDefault="00E22EB6">  
      <w:r>  
        <w:t>This is another paragraph.</w:t>  
      </w:r>  
    </w:p>  
  </w:body>  
</w:document>  
```  
  
 Bu belge, iki paragraf içerir. Her ikisi de çalıştıran tek bir metin içeren ve tek bir metin parçası çalıştırmak her metin içerir.  
  
 XML formundaki WordprocessingML belgesinin içeriğini görmek için en kolay yolu bir Microsoft Word kaydedin kullanarak ve ardından XML konsola yazdırır aşağıdaki programı çalıştırın oluşturmaktır.  
  
 Bu örnekte WindowsBase derlemede bulunan sınıfları kullanır. Türleri kullanan <xref:System.IO.Packaging?displayProperty=nameWithType> ad alanı.  
  
```csharp  
const string documentRelationshipType =  
  "http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument";  
const string wordmlNamespace =  
  "http://schemas.openxmlformats.org/wordprocessingml/2006/main";  
XNamespace w = wordmlNamespace;  
  
using (Package wdPackage = Package.Open("SampleDoc.docx", FileMode.Open, FileAccess.Read))  
{  
    PackageRelationship relationship =  
        wdPackage  
        .GetRelationshipsByType(documentRelationshipType)  
        .FirstOrDefault();  
    if (relationship != null)  
    {  
        Uri documentUri =  
            PackUriHelper.ResolvePartUri(  
                new Uri("/", UriKind.Relative),  
                relationship.TargetUri);  
        PackagePart documentPart = wdPackage.GetPart(documentUri);  
  
        //  Get the officeDocument part from the package.  
        //  Load the XML in the part into an XDocument instance.  
        XDocument xdoc =  
            XDocument.Load(XmlReader.Create(documentPart.GetStream()));  
        Console.WriteLine(xdoc.Root);  
    }  
}  
```  
  
## <a name="external-resources"></a>Dış Kaynaklar  
 [Office (2007) açık XML dosya biçimleri](https://msdn.microsoft.com/library/ms406049.aspx)  
 [WordprocessingML genel bakış](https://msdn.microsoft.com/library/aa212812(office.11).aspx)  
 [WordProcessingML dosya anatomisi](http://officeopenxml.com/anatomyofOOXML.php)  
 [WordprocessingML giriş](http://ericwhite.com/blog/introduction-to-wordprocessingml-series/)  
 [Office 2003: XML şemaları başvuru indirme sayfası](https://www.microsoft.com/en-us/download/details.aspx?id=101)  
  
## <a name="see-also"></a>Ayrıca Bkz.

- [Öğretici: WordprocessingML belgesindeki (C#) içerik düzenleme](../../../../csharp/programming-guide/concepts/linq/tutorial-manipulating-content-in-a-wordprocessingml-document.md)
