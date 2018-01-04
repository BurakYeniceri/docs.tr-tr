---
title: "Harita anahtar DataSet kısıtlamaları için XML Şeması (XSD) kısıtlamaları"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 22664196-f270-4ebc-a169-70e16a83dfa1
caps.latest.revision: "4"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: 249cb8419d4f032c37a922c9aa640f02f6efbd56
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="map-key-xml-schema-xsd-constraints-to-dataset-constraints"></a><span data-ttu-id="1a170-102">Harita anahtar DataSet kısıtlamaları için XML Şeması (XSD) kısıtlamaları</span><span class="sxs-lookup"><span data-stu-id="1a170-102">Map key XML Schema (XSD) Constraints to DataSet Constraints</span></span>
<span data-ttu-id="1a170-103">Şemada, bir öğenin anahtar kısıtlaması belirtin veya kullanarak öznitelik **anahtar** öğesi.</span><span class="sxs-lookup"><span data-stu-id="1a170-103">In a schema, you can specify a key constraint on an element or attribute using the **key** element.</span></span> <span data-ttu-id="1a170-104">Öğesi veya özniteliği bir anahtar kısıtlaması belirtilen şema örnek benzersiz değerlere sahip olmalıdır ve null değerler olamaz.</span><span class="sxs-lookup"><span data-stu-id="1a170-104">The element or attribute on which a key constraint is specified must have unique values in any schema instance, and cannot have null values.</span></span>  
  
 <span data-ttu-id="1a170-105">Bir anahtar kısıtlaması tanımlandığı sütunu null değerler olamaz anahtar kısıtlaması benzersiz kısıtlama benzerdir.</span><span class="sxs-lookup"><span data-stu-id="1a170-105">The key constraint is similar to the unique constraint, except that the column on which a key constraint is defined cannot have null values.</span></span>  
  
 <span data-ttu-id="1a170-106">Aşağıdaki tabloda ana hatlarını **msdata** belirleyebilirsiniz öznitelikleri **anahtar** öğesi.</span><span class="sxs-lookup"><span data-stu-id="1a170-106">The following table outlines the **msdata** attributes that you can specify in the **key** element.</span></span>  
  
|<span data-ttu-id="1a170-107">Öznitelik adı</span><span class="sxs-lookup"><span data-stu-id="1a170-107">Attribute name</span></span>|<span data-ttu-id="1a170-108">Açıklama</span><span class="sxs-lookup"><span data-stu-id="1a170-108">Description</span></span>|  
|--------------------|-----------------|  
|<span data-ttu-id="1a170-109">**MSDATA:ConstraintName**</span><span class="sxs-lookup"><span data-stu-id="1a170-109">**msdata:ConstraintName**</span></span>|<span data-ttu-id="1a170-110">Bu öznitelik belirtilen değeri kısıtlama adı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a170-110">If this attribute is specified, its value is used as the constraint name.</span></span> <span data-ttu-id="1a170-111">Aksi takdirde, **adı** özniteliği, kısıtlama adı değerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a170-111">Otherwise, the **name** attribute provides the value of the constraint name.</span></span>|  
|<span data-ttu-id="1a170-112">**MSDATA**</span><span class="sxs-lookup"><span data-stu-id="1a170-112">**msdata:PrimaryKey**</span></span>|<span data-ttu-id="1a170-113">Varsa `PrimaryKey="true"` var, **IsPrimaryKey** kısıtlaması özelliği ayarlanmış **doğru**, böylece birincil anahtar yapma.</span><span class="sxs-lookup"><span data-stu-id="1a170-113">If `PrimaryKey="true"` is present, the **IsPrimaryKey** constraint property is set to **true**, thus making it a primary key.</span></span> <span data-ttu-id="1a170-114">**AllowDBNull** column özelliği ayarlanmış **yanlış**, birincil anahtarlar null değerler olamaz.</span><span class="sxs-lookup"><span data-stu-id="1a170-114">The **AllowDBNull** column property is set to **false**, because primary keys cannot have null values.</span></span>|  
  
 <span data-ttu-id="1a170-115">Bir anahtar kısıtlaması belirtilmişse şema dönüştürülmesi kapsamında, eşleme işlemi tablo ile birlikte benzersiz bir kısıtlama oluşturur **AllowDBNull** sütun özelliğinin ayarlandığı **false** her sütun için kısıtlama.</span><span class="sxs-lookup"><span data-stu-id="1a170-115">In converting schema in which a key constraint is specified, the mapping process creates a unique constraint on the table with the **AllowDBNull** column property set to **false** for each column in the constraint.</span></span> <span data-ttu-id="1a170-116">**IsPrimaryKey** de UNIQUE kısıtlaması özelliği ayarlanmış **false** belirttiğiniz sürece `msdata:PrimaryKey="true"` üzerinde **anahtar** öğesi.</span><span class="sxs-lookup"><span data-stu-id="1a170-116">The **IsPrimaryKey** property of the unique constraint is also set to **false** unless you have specified `msdata:PrimaryKey="true"` on the **key** element.</span></span> <span data-ttu-id="1a170-117">Bu kısıtlama, şemasında aynıdır `PrimaryKey="true"`.</span><span class="sxs-lookup"><span data-stu-id="1a170-117">This is identical to a unique constraint in the schema in which `PrimaryKey="true"`.</span></span>  
  
 <span data-ttu-id="1a170-118">Aşağıdaki şema örnekte **anahtar** öğesi belirtir anahtar kısıtlaması **CustomerID** öğesi.</span><span class="sxs-lookup"><span data-stu-id="1a170-118">In the following schema example, the **key** element specifies the key constraint on the **CustomerID** element.</span></span>  
  
```xml  
<xs:schema id="cod"  
            xmlns:xs="http://www.w3.org/2001/XMLSchema"   
            xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">  
  <xs:element name="Customers">  
    <xs:complexType>  
      <xs:sequence>  
        <xs:element name="CustomerID" type="xs:string" minOccurs="0" />  
        <xs:element name="CompanyName" type="xs:string" minOccurs="0" />  
       <xs:element name="Phone" type="xs:string" />  
     </xs:sequence>  
   </xs:complexType>  
 </xs:element>  
<xs:element name="MyDataSet" msdata:IsDataSet="true">  
  <xs:complexType>  
    <xs:choice maxOccurs="unbounded">  
      <xs:element ref="Customers" />  
    </xs:choice>  
  </xs:complexType>  
   <xs:key  msdata:PrimaryKey="true"  
       msdata:ConstraintName="KeyCustID"  
          name="KeyConstCustomerID" >  
     <xs:selector xpath=".//Customers" />  
     <xs:field xpath="CustomerID" />  
    </xs:key>  
 </xs:element>  
</xs:schema>   
```  
  
 <span data-ttu-id="1a170-119">**Anahtar** öğesi belirttiğinden değerlerini **CustomerID** alt öğesi olan **müşteriler** öğesi benzersiz değerlere sahip olmalıdır ve null değerler olamaz.</span><span class="sxs-lookup"><span data-stu-id="1a170-119">The **key** element specifies that the values of the **CustomerID** child element of the **Customers** element must have unique values and cannot have null values.</span></span> <span data-ttu-id="1a170-120">XML Şeması Tanım Dili (XSD) şeması çevirme içinde eşleme işlemi aşağıdaki tabloda oluşturur:</span><span class="sxs-lookup"><span data-stu-id="1a170-120">In translating the XML Schema definition language (XSD) schema, the mapping process creates the following table:</span></span>  
  
```  
Customers(CustomerID, CompanyName, Phone)  
```  
  
 <span data-ttu-id="1a170-121">XML şema eşleme da oluşturur bir **UniqueConstraint** üzerinde **CustomerID** sütun, aşağıda gösterildiği gibi <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="1a170-121">The XML Schema mapping also creates a **UniqueConstraint** on the **CustomerID** column, as shown in the following <xref:System.Data.DataSet>.</span></span> <span data-ttu-id="1a170-122">(Kolaylık sağlamak için yalnızca ilgili özellikleri gösterilir.)</span><span class="sxs-lookup"><span data-stu-id="1a170-122">(For simplicity, only relevant properties are shown.)</span></span>  
  
```  
      DataSetName: MyDataSet  
TableName: customers  
  ColumnName: CustomerID  
      AllowDBNull: False  
      Unique: True  
  ConstraintName: KeyCustID  
      Table: customers  
      Columns: CustomerID   
      IsPrimaryKey: True  
```  
  
 <span data-ttu-id="1a170-123">İçinde **DataSet** , oluşturulduğunda, **IsPrimaryKey** özelliği **UniqueConstraint** ayarlanır **true** çünkü şeması belirtir `msdata:PrimaryKey="true"` içinde **anahtar** öğesi.</span><span class="sxs-lookup"><span data-stu-id="1a170-123">In the **DataSet** that is generated, the **IsPrimaryKey** property of the **UniqueConstraint** is set to **true** because the schema specifies `msdata:PrimaryKey="true"` in the **key** element.</span></span>  
  
 <span data-ttu-id="1a170-124">Değeri **ConstraintName** özelliği **UniqueConstraint** içinde **DataSet** değeri **msdata:ConstraintName** Belirtilen öznitelik **anahtar** schema öğesinde.</span><span class="sxs-lookup"><span data-stu-id="1a170-124">The value of the **ConstraintName** property of the **UniqueConstraint** in the **DataSet** is the value of the **msdata:ConstraintName** attribute specified in the **key** element in the schema.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1a170-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="1a170-125">See Also</span></span>  
 [<span data-ttu-id="1a170-126">XML Şeması (XSD) Kısıtlamalarını DataSet Kısıtlamaları ile Eşleme</span><span class="sxs-lookup"><span data-stu-id="1a170-126">Mapping XML Schema (XSD) Constraints to DataSet Constraints</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/mapping-xml-schema-xsd-constraints-to-dataset-constraints.md)  
 [<span data-ttu-id="1a170-127">XML Şemasından (XSD) DataSet İlişkileri Oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a170-127">Generating DataSet Relations from XML Schema (XSD)</span></span>](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/generating-dataset-relations-from-xml-schema-xsd.md)  
 [<span data-ttu-id="1a170-128">ADO.NET yönetilen sağlayıcıları ve veri kümesi Geliştirici Merkezi</span><span class="sxs-lookup"><span data-stu-id="1a170-128">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
