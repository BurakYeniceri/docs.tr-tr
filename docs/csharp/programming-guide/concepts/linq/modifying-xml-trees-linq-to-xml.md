---
title: (LINQ to XML) XML ağaçlarını değiştirme (C#)
ms.date: 07/20/2015
ms.assetid: 8ec47e6d-2363-4694-be46-8d5ca4d15fc9
ms.openlocfilehash: 55e75762772a071b97eecb7d6d78e28c3002a179
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43505725"
---
# <a name="modifying-xml-trees-linq-to-xml-c"></a>(LINQ to XML) XML ağaçlarını değiştirme (C#)
[!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] bir bellek içi XML ağacı için deposudur. Yükleme veya ayrıştırma bir kaynaktan bir XML ağacı sonra [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] o ağaç yerinde değiştirebilir ve belki de bir dosyaya kaydetme veya uzak bir sunucuya gönderme ağacı seri hale getirme olanak tanır.  
  
 Yerinde bir ağaç değiştirdiğinizde, belirli yöntemler gibi kullanın <xref:System.Xml.Linq.XContainer.Add%2A>.  
  
 Ancak, farklı bir şekilde yeni bir ağaç oluşturmak için işlev yapım kullanılacak olan başka bir yaklaşım yoktur. Ve bağlı olarak, XML ağacına yapmanız gereken değişiklik türlerini ağaç boyutuna bağlı olarak, bu yaklaşım daha sağlam ve geliştirmeyi daha kolay olabilir. İlk konu bu bölümde, bu iki yaklaşımı karşılaştırır.  
  
## <a name="in-this-section"></a>Bu Bölümde  
  
|Konu|Açıklama|  
|-----------|-----------------|  
|[Bellek içi XML Ağacı Değişikliği ve İşlevsel oluşturma (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/in-memory-xml-tree-modification-vs-functional-construction-linq-to-xml.md)|İşlevsel oluşturma bellekte bir XML ağacı değiştirme karşılaştırır.|  
|[(C#) XML ağacına öğe, öznitelik ve düğümleri ekleme](../../../../csharp/programming-guide/concepts/linq/adding-elements-attributes-and-nodes-to-an-xml-tree.md)|XML ağacına öğe, öznitelik veya düğümleri ekleme hakkında bilgi sağlar.|  
|[XML Ağacındaki Öğe, Öznitelik ve Düğümleri Değiştirme](../../../../csharp/programming-guide/concepts/linq/modifying-elements-attributes-and-nodes-in-an-xml-tree.md)|Var olan öğeleri, öznitelikleri ve düğümleri değiştirme hakkında bilgi sağlar.|  
|[XML ağacından (C#) öğe, öznitelik ve düğümleri kaldırma](../../../../csharp/programming-guide/concepts/linq/removing-elements-attributes-and-nodes-from-an-xml-tree.md)|XML ağacından öğe, öznitelik veya düğümleri kaldırma hakkında bilgi sağlar.|  
|[Ad/değer çiftleri Bakımı (C#)](../../../../csharp/programming-guide/concepts/linq/maintaining-name-value-pairs.md)|En iyi yapılandırma bilgileri veya genel ayarlar gibi bir ad/değer çiftleri olarak tutulur, uygulama bilgilerini korumak nasıl açıklar.|  
|[Nasıl yapılır: Namespace değiştirmek için tüm XML ağacının (C#)](../../../../csharp/programming-guide/concepts/linq/how-to-change-the-namespace-for-an-entire-xml-tree.md)|Bir XML ağacı bir ad alanından diğerine taşımak gösterilmektedir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.

- [Programlama Kılavuzu (LINQ to XML) (C#)](../../../../csharp/programming-guide/concepts/linq/programming-guide-linq-to-xml.md)
