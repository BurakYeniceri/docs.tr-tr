---
title: "Nasıl yapılır: Windows Forms DataGrid Denetimini Veri Kaynağına Bağlama"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- datasets [Windows Forms], binding to DataGrid control
- data binding [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], data binding
- bound controls [Windows Forms], DataGrid control
- Windows Forms controls, data binding
- bound controls [Windows Forms]
- data-bound controls [Windows Forms], DataGrid
ms.assetid: 128cdb07-dfd3-4d60-9d6a-902847667c36
caps.latest.revision: "17"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c136aca0eda9ea906ad8bf6853a263adf6130609
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-bind-the-windows-forms-datagrid-control-to-a-data-source"></a><span data-ttu-id="6244a-102">Nasıl yapılır: Windows Forms DataGrid Denetimini Veri Kaynağına Bağlama</span><span class="sxs-lookup"><span data-stu-id="6244a-102">How to: Bind the Windows Forms DataGrid Control to a Data Source</span></span>
> [!NOTE]
>  <span data-ttu-id="6244a-103"><xref:System.Windows.Forms.DataGridView> Denetimi değiştirir ve işlevlerini ekler <xref:System.Windows.Forms.DataGrid> kontrol; ancak, <xref:System.Windows.Forms.DataGrid> denetim tutulur geriye dönük uyumluluk ve gelecekte kullanım için seçerseniz.</span><span class="sxs-lookup"><span data-stu-id="6244a-103">The <xref:System.Windows.Forms.DataGridView> control replaces and adds functionality to the <xref:System.Windows.Forms.DataGrid> control; however, the <xref:System.Windows.Forms.DataGrid> control is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="6244a-104">Daha fazla bilgi için bkz: [farklar arasında Windows Forms DataGridView ve DataGrid denetimleri](../../../../docs/framework/winforms/controls/differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6244a-104">For more information, see [Differences Between the Windows Forms DataGridView and DataGrid Controls](../../../../docs/framework/winforms/controls/differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span></span>  
  
 <span data-ttu-id="6244a-105">Windows Forms <xref:System.Windows.Forms.DataGrid> denetimi veri kaynağı bilgilerini görüntülemek için özel olarak tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6244a-105">The Windows Forms <xref:System.Windows.Forms.DataGrid> control is specifically designed to display information from a data source.</span></span> <span data-ttu-id="6244a-106">Çağırarak çalışma zamanında denetimi bağlamak <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="6244a-106">You bind the control at run time by calling the <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> method.</span></span> <span data-ttu-id="6244a-107">Çeşitli veri kaynakları verileri görüntüleyebilse de, en tipik veri kümeleri ve veri görünümleri kaynaklardır.</span><span class="sxs-lookup"><span data-stu-id="6244a-107">Although you can display data from a variety of data sources, the most typical sources are datasets and data views.</span></span>  
  
### <a name="to-data-bind-the-datagrid-control-programmatically"></a><span data-ttu-id="6244a-108">DataGrid denetimi program aracılığıyla Data-bind için</span><span class="sxs-lookup"><span data-stu-id="6244a-108">To data-bind the DataGrid control programmatically</span></span>  
  
1.  <span data-ttu-id="6244a-109">Veri kümesini doldurmak için kod yazma.</span><span class="sxs-lookup"><span data-stu-id="6244a-109">Write code to fill the dataset.</span></span>  
  
     <span data-ttu-id="6244a-110">Veri kaynağı bir veri kümesi ya da bir veri kümesi tabloya dayalı bir veri görünümü ise, veri kümesini doldurmak üzere formuna kodu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6244a-110">If the data source is a dataset or a data view based on a dataset table, add code to the form to fill the dataset.</span></span>  
  
     <span data-ttu-id="6244a-111">Kullandığınız tam kod burada veri kümesi alma bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6244a-111">The exact code you use depends on where the dataset is getting data.</span></span> <span data-ttu-id="6244a-112">Veri kümesi bir veritabanından doğrudan doldurulmuş, genellikle çağırmanız `Fill` adlı bir veri kümesi doldurur aşağıdaki örnekteki gibi bir veri bağdaştırıcısı yöntemi `DsCategories1`:</span><span class="sxs-lookup"><span data-stu-id="6244a-112">If the dataset is being populated directly from a database, you typically call the `Fill` method of a data adapter, as in the following example, which populates a dataset called `DsCategories1`:</span></span>  
  
    ```vb  
    sqlDataAdapter1.Fill(DsCategories1)  
    ```  
  
    ```csharp  
    sqlDataAdapter1.Fill(DsCategories1);  
    ```  
  
    ```cpp  
    sqlDataAdapter1->Fill(dsCategories1);  
    ```  
  
     <span data-ttu-id="6244a-113">Veri kümesi bir XML Web hizmetinden doldurulmuş, genellikle kodunuzda Hizmeti'nin bir örneğini oluşturun ve bir veri kümesi döndürülecek yöntemlerinden birini çağırın.</span><span class="sxs-lookup"><span data-stu-id="6244a-113">If the dataset is being filled from an XML Web service, you typically create an instance of the service in your code and then call one of its methods to return a dataset.</span></span> <span data-ttu-id="6244a-114">XML Web hizmeti kümesinden sonra yerel veri kümesine birleştirin.</span><span class="sxs-lookup"><span data-stu-id="6244a-114">You then merge the dataset from the XML Web service into your local dataset.</span></span> <span data-ttu-id="6244a-115">Aşağıdaki örnek adlı bir XML Web hizmeti örneğini nasıl oluşturabileceğinizi gösterir `CategoriesService`, çağrı kendi `GetCategories` yöntemi ve sonuçta elde edilen yerel bir veri kümesine adlı birleştirme `DsCategories1`:</span><span class="sxs-lookup"><span data-stu-id="6244a-115">The following example shows how you can create an instance of an XML Web service called `CategoriesService`, call its `GetCategories` method, and merge the resulting dataset into a local dataset called `DsCategories1`:</span></span>  
  
    ```vb  
    Dim ws As New MyProject.localhost.CategoriesService()  
    ws.Credentials = System.Net.CredentialCache.DefaultCredentials  
    DsCategories1.Merge(ws.GetCategories())  
    ```  
  
    ```csharp  
    MyProject.localhost.CategoriesService ws = new MyProject.localhost.CategoriesService();  
    ws.Credentials = System.Net.CredentialCache.DefaultCredentials;  
    DsCategories1.Merge(ws.GetCategories());  
    ```  
  
    ```cpp  
    MyProject::localhost::CategoriesService^ ws =   
       new MyProject::localhost::CategoriesService();  
    ws->Credentials = System::Net::CredentialCache::DefaultCredentials;  
    dsCategories1->Merge(ws->GetCategories());  
    ```  
  
2.  <span data-ttu-id="6244a-116">Çağrı <xref:System.Windows.Forms.DataGrid> denetimin <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> yöntemi, veri kaynağı ve veri üyesi geçirme.</span><span class="sxs-lookup"><span data-stu-id="6244a-116">Call the <xref:System.Windows.Forms.DataGrid> control's <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> method, passing it the data source and a data member.</span></span> <span data-ttu-id="6244a-117">Bir veri üyesi açıkça geçmesine gerekmiyorsa, boş bir dizeyi geçirmek.</span><span class="sxs-lookup"><span data-stu-id="6244a-117">If you do not need to explicitly pass a data member, pass an empty string.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="6244a-118">Izgaranın ilk kez bağlanıyorsanız, denetimin ayarlayabilirsiniz <xref:System.Windows.Forms.DataGrid.DataSource%2A> ve <xref:System.Windows.Forms.DataGrid.DataMember%2A> özellikleri.</span><span class="sxs-lookup"><span data-stu-id="6244a-118">If you are binding the grid for the first time, you can set the control's <xref:System.Windows.Forms.DataGrid.DataSource%2A> and <xref:System.Windows.Forms.DataGrid.DataMember%2A> properties.</span></span> <span data-ttu-id="6244a-119">Ancak, bunlar ayarlandıktan sonra bu özellikleri sıfırlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6244a-119">However, you cannot reset these properties once they have been set.</span></span> <span data-ttu-id="6244a-120">Bu nedenle, her zaman kullanmanız önerilir <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> yöntemi.</span><span class="sxs-lookup"><span data-stu-id="6244a-120">Therefore, it is recommended that you always use the <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> method.</span></span>  
  
     <span data-ttu-id="6244a-121">Aşağıdaki örnek, nasıl program aracılığıyla adlı bir veri kümesi Müşteriler tablosunda bağlayabilirsiniz gösterir `DsCustomers1`:</span><span class="sxs-lookup"><span data-stu-id="6244a-121">The following example shows how you can programmatically bind to the Customers table in a dataset called `DsCustomers1`:</span></span>  
  
    ```vb  
    DataGrid1.SetDataBinding(DsCustomers1, "Customers")  
    ```  
  
    ```csharp  
    DataGrid1.SetDataBinding(DsCustomers1, "Customers");  
    ```  
  
    ```cpp  
    dataGrid1->SetDataBinding(dsCustomers1, "Customers");  
    ```  
  
     <span data-ttu-id="6244a-122">Müşteriler tablosu veri kümesi yalnızca tabloda ise, kılavuz alternatif olarak bu şekilde bağlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6244a-122">If the Customers table is the only table in the dataset, you could alternatively bind the grid this way:</span></span>  
  
    ```vb  
    DataGrid1.SetDataBinding(DsCustomers1, "")  
    ```  
  
    ```csharp  
    DataGrid1.SetDataBinding(DsCustomers1, "");  
    ```  
  
    ```cpp  
    dataGrid1->SetDataBinding(dsCustomers1, "");  
    ```  
  
3.  <span data-ttu-id="6244a-123">(İsteğe bağlı) Sütun stilleri ve uygun tablo stilleri kılavuzuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6244a-123">(Optional) Add the appropriate table styles and column styles to the grid.</span></span> <span data-ttu-id="6244a-124">Hiçbir tablo stilleri varsa Tablo görürsünüz, ancak en az biçimlendirme ile tüm sütunları görünür.</span><span class="sxs-lookup"><span data-stu-id="6244a-124">If there are no table styles, you will see the table, but with minimal formatting and with all columns visible.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6244a-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="6244a-125">See Also</span></span>  
 [<span data-ttu-id="6244a-126">DataGrid Denetimine Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6244a-126">DataGrid Control Overview</span></span>](../../../../docs/framework/winforms/controls/datagrid-control-overview-windows-forms.md)  
 [<span data-ttu-id="6244a-127">Nasıl yapılır: Windows Forms DataGrid Denetimine Tablo ve Sütun Ekleme</span><span class="sxs-lookup"><span data-stu-id="6244a-127">How to: Add Tables and Columns to the Windows Forms DataGrid Control</span></span>](../../../../docs/framework/winforms/controls/how-to-add-tables-and-columns-to-the-windows-forms-datagrid-control.md)  
 [<span data-ttu-id="6244a-128">DataGrid Denetimi</span><span class="sxs-lookup"><span data-stu-id="6244a-128">DataGrid Control</span></span>](../../../../docs/framework/winforms/controls/datagrid-control-windows-forms.md)  
 [<span data-ttu-id="6244a-129">Windows Forms Veri Bağlama</span><span class="sxs-lookup"><span data-stu-id="6244a-129">Windows Forms Data Binding</span></span>](../../../../docs/framework/winforms/windows-forms-data-binding.md)
