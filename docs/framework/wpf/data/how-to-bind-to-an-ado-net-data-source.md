---
title: "Nasıl yapılır: ADO.NET Veri Kaynağına Bağlama"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], binding to ADO.NET data sources
- ADO.NET data sources [WPF], binding to
- binding [WPF], to ADO.NET data sources
ms.assetid: a70c6d7b-7b38-4fdf-b655-4804db7c8315
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0eb555bb9f21385d2d0b66fe0dd39112c8350dec
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-bind-to-an-adonet-data-source"></a><span data-ttu-id="13425-102">Nasıl yapılır: ADO.NET Veri Kaynağına Bağlama</span><span class="sxs-lookup"><span data-stu-id="13425-102">How to: Bind to an ADO.NET Data Source</span></span>
<span data-ttu-id="13425-103">Bu örnek nasıl bağlanacağını gösterir bir [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] <xref:System.Windows.Controls.ListBox> denetimini bir [!INCLUDE[TLA#tla_adonet](../../../../includes/tlasharptla-adonet-md.md)] `DataSet`.</span><span class="sxs-lookup"><span data-stu-id="13425-103">This example shows how to bind a [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] <xref:System.Windows.Controls.ListBox> control to an [!INCLUDE[TLA#tla_adonet](../../../../includes/tlasharptla-adonet-md.md)] `DataSet`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="13425-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="13425-104">Example</span></span>  
 <span data-ttu-id="13425-105">Bu örnekte, bir `OleDbConnection` nesne olan veri kaynağına bağlanmak için kullanılan bir `Access MDB` bağlantı dizesinde belirtilen dosya.</span><span class="sxs-lookup"><span data-stu-id="13425-105">In this example, an `OleDbConnection` object is used to connect to the data source which is an `Access MDB` file that is specified in the connection string.</span></span> <span data-ttu-id="13425-106">Bağlantı kurulduktan sonra bir `OleDbDataAdpater` nesnesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="13425-106">After the connection is established, an `OleDbDataAdpater` object is created.</span></span> <span data-ttu-id="13425-107">`OleDbDataAdpater` Nesne yürüten bir select [!INCLUDE[TLA#tla_sql](../../../../includes/tlasharptla-sql-md.md)] veritabanından kayıt kümesi almak için bildirimi.</span><span class="sxs-lookup"><span data-stu-id="13425-107">The `OleDbDataAdpater` object executes a select [!INCLUDE[TLA#tla_sql](../../../../includes/tlasharptla-sql-md.md)] statement to retrieve the recordset from the database.</span></span> <span data-ttu-id="13425-108">Sonuçlardan [!INCLUDE[TLA2#tla_sql](../../../../includes/tla2sharptla-sql-md.md)] komutu depolanır bir `DataTable` , `DataSet` çağırarak `Fill` yöntemi `OleDbDataAdapter`.</span><span class="sxs-lookup"><span data-stu-id="13425-108">The results from the [!INCLUDE[TLA2#tla_sql](../../../../includes/tla2sharptla-sql-md.md)] command are stored in a `DataTable` of the `DataSet` by calling the `Fill` method of the `OleDbDataAdapter`.</span></span> <span data-ttu-id="13425-109">`DataTable` Bu örnekte adlı `BookTable`.</span><span class="sxs-lookup"><span data-stu-id="13425-109">The `DataTable` in this example is named `BookTable`.</span></span> <span data-ttu-id="13425-110">Bu örnek daha sonra Ayarlar <xref:System.Windows.FrameworkElement.DataContext%2A> özelliği <xref:System.Windows.Controls.ListBox> için `DataSet` nesnesi.</span><span class="sxs-lookup"><span data-stu-id="13425-110">The example then sets the <xref:System.Windows.FrameworkElement.DataContext%2A> property of the <xref:System.Windows.Controls.ListBox> to the `DataSet` object.</span></span>  
  
 [!code-csharp[ADODataSet#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ADODataSet#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ADODataSet/VisualBasic/Window1.xaml.vb#1)]  
  
 <span data-ttu-id="13425-111">Biz sonra bağlayabilirsiniz <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> özelliği <xref:System.Windows.Controls.ListBox> için `BookTable` , `DataSet`:</span><span class="sxs-lookup"><span data-stu-id="13425-111">We can then bind the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> property of the <xref:System.Windows.Controls.ListBox> to `BookTable` of the `DataSet`:</span></span>  
  
 [!code-xaml[ADODataSet#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="13425-112">`BookItemTemplate`olan <xref:System.Windows.DataTemplate> verinin nasıl göründüğünü tanımlar:</span><span class="sxs-lookup"><span data-stu-id="13425-112">`BookItemTemplate` is the <xref:System.Windows.DataTemplate> that defines how the data appears:</span></span>  
  
 [!code-xaml[ADODataSet#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ADODataSet/CSharp/Window1.xaml#3)]  
  
 <span data-ttu-id="13425-113">`IntColorConverter` Dönüştüren bir `int` bir renk.</span><span class="sxs-lookup"><span data-stu-id="13425-113">The `IntColorConverter` converts an `int` to a color.</span></span> <span data-ttu-id="13425-114">Bu dönüştürücü kullanarak <xref:System.Windows.Controls.TextBlock.Background%2A> üçüncü rengini <xref:System.Windows.Controls.TextBlock> yeşil görünür değilse değerini `NumPages` Aksi takdirde değerinden 350 ve kırmızı olur.</span><span class="sxs-lookup"><span data-stu-id="13425-114">With the use of this converter, the <xref:System.Windows.Controls.TextBlock.Background%2A> color of the third <xref:System.Windows.Controls.TextBlock> appears green if the value of `NumPages` is less than 350 and red otherwise.</span></span> <span data-ttu-id="13425-115">Dönüştürücü uyarlamasını burada gösterilmiyor.</span><span class="sxs-lookup"><span data-stu-id="13425-115">The implementation of the converter is not shown here.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13425-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="13425-116">See Also</span></span>  
 <xref:System.Windows.Data.BindingListCollectionView>  
 [<span data-ttu-id="13425-117">Veri bağlama genel bakış</span><span class="sxs-lookup"><span data-stu-id="13425-117">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [<span data-ttu-id="13425-118">Nasıl Yapılır Konuları</span><span class="sxs-lookup"><span data-stu-id="13425-118">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)