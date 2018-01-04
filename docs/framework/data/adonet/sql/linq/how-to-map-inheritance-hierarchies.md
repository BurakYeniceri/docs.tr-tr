---
title: "Nasıl yapılır: eşleme devralma hiyerarşileri"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: b27c779b-9355-4dc7-b95f-7dfd504b6e48
dev_langs:
- csharp
- vb
caps.latest.revision: "4"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: 93f3eb40e96c0735218464c8ee69a3e6fe358a03
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-map-inheritance-hierarchies"></a><span data-ttu-id="4ac4b-102">Nasıl yapılır: eşleme devralma hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="4ac4b-102">How to: Map Inheritance Hierarchies</span></span>
<span data-ttu-id="4ac4b-103">Devralma eşleme uygulamak için [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)], öznitelikleri ve öznitelik özellikleri Devralma Hiyerarşisi kök sınıfının aşağıdaki adımlarda açıklandığı gibi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-103">To implement inheritance mapping in [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)], you must specify the attributes and attribute properties on the root class of the inheritance hierarchy as described in the following steps.</span></span> <span data-ttu-id="4ac4b-104">Kullanan geliştiriciler [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)] kullanabilirsiniz [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] devralma hiyerarşileri eşlemek için.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-104">Developers using [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)] can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to map inheritance hierarchies.</span></span> <span data-ttu-id="4ac4b-105">Bkz: [nasıl yapılır: devralma O/R Tasarımcısı kullanarak yapılandırma](/visualstudio/data-tools/how-to-configure-inheritance-by-using-the-o-r-designer).</span><span class="sxs-lookup"><span data-stu-id="4ac4b-105">See [How to: Configure inheritance by using the O/R Designer](/visualstudio/data-tools/how-to-configure-inheritance-by-using-the-o-r-designer).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4ac4b-106">Hiçbir özel öznitelikler veya özellikleri üzerinde alt sınıfların gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-106">No special attributes or properties are required on the subclasses.</span></span> <span data-ttu-id="4ac4b-107">Alt sınıfların olmadığı özellikle Not <xref:System.Data.Linq.Mapping.TableAttribute> özniteliği.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-107">Note especially that subclasses do not have the <xref:System.Data.Linq.Mapping.TableAttribute> attribute.</span></span>  
  
### <a name="to-map-an-inheritance-hierarchy"></a><span data-ttu-id="4ac4b-108">Devralma Hiyerarşisi eşlemek için</span><span class="sxs-lookup"><span data-stu-id="4ac4b-108">To map an inheritance hierarchy</span></span>  
  
1.  <span data-ttu-id="4ac4b-109">Ekleme <xref:System.Data.Linq.Mapping.TableAttribute> özniteliği için kök sınıfı.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-109">Add the <xref:System.Data.Linq.Mapping.TableAttribute> attribute to the root class.</span></span>  
  
2.  <span data-ttu-id="4ac4b-110">Ayrıca kök sınıfına ekleyin bir <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> her sınıf hiyerarşisi yapısındaki özniteliği.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-110">Also to the root class, add an <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> attribute for each class in the hierarchy structure.</span></span>  
  
3.  <span data-ttu-id="4ac4b-111">Her <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> özniteliği, tanımlayan bir <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-111">For each <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> attribute, define a <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A> property.</span></span>  
  
     <span data-ttu-id="4ac4b-112">Bu özellik veritabanı tablosunda görüntülenen bir değeri tutan <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDiscriminator%2A> hangi sınıfı ya da bir alt kümesi için bu veri satırının ait göstermek için sütun.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-112">This property holds a value that appears in the database table in the <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDiscriminator%2A> column to indicate which class or subclass this row of data belongs to.</span></span>  
  
4.  <span data-ttu-id="4ac4b-113">Her <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> özniteliği, ayrıca bir <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Type%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-113">For each <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> attribute, also add a <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Type%2A> property.</span></span>  
  
     <span data-ttu-id="4ac4b-114">Bu özellik, hangi sınıfı ya da bir alt anahtar değeri güveninin belirten bir değeri tutar.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-114">This property holds a value that specifies which class or subclass the key value signifies.</span></span>  
  
5.  <span data-ttu-id="4ac4b-115">Yalnızca birinde <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> öznitelikleri, ekleme bir <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.IsDefault%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-115">On only one of the <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute> attributes, add an <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.IsDefault%2A> property.</span></span>  
  
     <span data-ttu-id="4ac4b-116">Belirlemek için bu özelliği hizmet veren bir *geri dönüş* veritabanı tablosunun Ayrıştırıcıyı değerinden herhangi eşleşmediğinde eşleme <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A> devralma eşlemeleri değeri.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-116">This property serves to designate a *fallback* mapping when the discriminator value from the database table does not match any <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A> value in the inheritance mappings.</span></span>  
  
6.  <span data-ttu-id="4ac4b-117">Ekleme bir <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDiscriminator%2A> özelliği için bir <xref:System.Data.Linq.Mapping.ColumnAttribute> özniteliği.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-117">Add an <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDiscriminator%2A> property for a <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
     <span data-ttu-id="4ac4b-118">Bu özellik bu tutan sütun olduğunu güveninin <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A> değeri.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-118">This property signifies that this is the column that holds the <xref:System.Data.Linq.Mapping.InheritanceMappingAttribute.Code%2A> value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4ac4b-119">Örnek</span><span class="sxs-lookup"><span data-stu-id="4ac4b-119">Example</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4ac4b-120">Kullanıyorsanız [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)], kullanabileceğiniz [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] devralma yapılandırmak için.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-120">If you are using [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)], you can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to configure inheritance.</span></span> <span data-ttu-id="4ac4b-121">Bkz: [nasıl yapılır: devralma O/R Tasarımcısı kullanarak yapılandırma](/visualstudio/data-tools/how-to-configure-inheritance-by-using-the-o-r-designer)</span><span class="sxs-lookup"><span data-stu-id="4ac4b-121">See [How to: Configure inheritance by using the O/R Designer](/visualstudio/data-tools/how-to-configure-inheritance-by-using-the-o-r-designer)</span></span>  
  
 <span data-ttu-id="4ac4b-122">Aşağıdaki kod örneğinde, `Vehicle` kök sınıf olarak tanımlandığını ve hiyerarşi için açıklamak için önceki adımları uygulanmıştır [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="4ac4b-122">In the following code example, `Vehicle` is defined as the root class, and the previous steps have been implemented to describe the hierarchy for [!INCLUDE[vbteclinq](../../../../../../includes/vbteclinq-md.md)].</span></span>  
  
 [!code-csharp[DLinqCustomize#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#4)]
 [!code-vb[DLinqCustomize#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="4ac4b-123">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4ac4b-123">See Also</span></span>  
 [<span data-ttu-id="4ac4b-124">Devralma Desteği</span><span class="sxs-lookup"><span data-stu-id="4ac4b-124">Inheritance Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/inheritance-support.md)  
 [<span data-ttu-id="4ac4b-125">Nasıl yapılır: Kod Düzenleyicisini Kullanarak Varlık Sınıflarını Özelleştirme</span><span class="sxs-lookup"><span data-stu-id="4ac4b-125">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
