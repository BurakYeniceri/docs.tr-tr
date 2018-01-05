---
title: "Nasıl yapılır: Windows Forms DataGridView Denetiminde Yeni Satırlar İçin Varsayılan Değerleri Belirtme"
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
helpviewer_keywords:
- data grids [Windows Forms], default values for new rows
- DataGridView control [Windows Forms], data entry
- rows [Windows Forms], specifying default values
- DataGridView control [Windows Forms], default values for new rows
ms.assetid: 8d127963-d9f8-4e4e-9f7f-beb66688f1f2
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 26f2ab0247c9d13a90560337c103a970afc8996c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-specify-default-values-for-new-rows-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="3ead9-102">Nasıl yapılır: Windows Forms DataGridView Denetiminde Yeni Satırlar İçin Varsayılan Değerleri Belirtme</span><span class="sxs-lookup"><span data-stu-id="3ead9-102">How to: Specify Default Values for New Rows in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="3ead9-103">Uygulama varsayılan değerleri yeni eklenen satırların doldurduğunda veri girişi daha kullanışlı hale getirebilir.</span><span class="sxs-lookup"><span data-stu-id="3ead9-103">You can make data entry more convenient when the application fills in default values for newly added rows.</span></span> <span data-ttu-id="3ead9-104">İle <xref:System.Windows.Forms.DataGridView> sınıfı, doldurabilirsiniz varsayılan değerlerle <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> olay.</span><span class="sxs-lookup"><span data-stu-id="3ead9-104">With the <xref:System.Windows.Forms.DataGridView> class, you can fill in default values with the <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> event.</span></span> <span data-ttu-id="3ead9-105">Kullanıcı yeni kayıtlar için satır girdiğinde, bu olay tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="3ead9-105">This event is raised when the user enters the row for new records.</span></span> <span data-ttu-id="3ead9-106">Kodunuzu bu olay işlediğinde, seçtiğiniz değerlerle istenen hücreleri doldurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ead9-106">When your code handles this event, you can populate desired cells with values of your choosing.</span></span>  
  
 <span data-ttu-id="3ead9-107">Aşağıdaki kod örneği kullanarak yeni satırlar için varsayılan değerler belirtmek gösterilmiştir <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> olay.</span><span class="sxs-lookup"><span data-stu-id="3ead9-107">The following code example demonstrates how to specify default values for new rows using the <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded> event.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ead9-108">Örnek</span><span class="sxs-lookup"><span data-stu-id="3ead9-108">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#120](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#120)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#120](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#120)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3ead9-109">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="3ead9-109">Compiling the Code</span></span>  
 <span data-ttu-id="3ead9-110">Bu örnek gerektirir:</span><span class="sxs-lookup"><span data-stu-id="3ead9-110">This example requires:</span></span>  
  
-   <span data-ttu-id="3ead9-111">A <xref:System.Windows.Forms.DataGridView> adlı Denetim `dataGridView1`.</span><span class="sxs-lookup"><span data-stu-id="3ead9-111">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
-   <span data-ttu-id="3ead9-112">A `NewCustomerId` benzersiz oluşturmak için işlevi `CustomerID` değerleri.</span><span class="sxs-lookup"><span data-stu-id="3ead9-112">A `NewCustomerId` function for generating unique `CustomerID` values.</span></span>  
  
-   <span data-ttu-id="3ead9-113">Başvurular <xref:System?displayProperty=nameWithType> ve <xref:System.Windows.Forms?displayProperty=nameWithType> derlemeler.</span><span class="sxs-lookup"><span data-stu-id="3ead9-113">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ead9-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="3ead9-114">See Also</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridView.DefaultValuesNeeded?displayProperty=nameWithType>  
 [<span data-ttu-id="3ead9-115">Windows Forms DataGridView Denetiminde Veri Girişi</span><span class="sxs-lookup"><span data-stu-id="3ead9-115">Data Entry in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/data-entry-in-the-windows-forms-datagridview-control.md)  
 [<span data-ttu-id="3ead9-116">Windows Forms DataGridView Denetiminde Yeni Kayıtlar için Satır Kullanma</span><span class="sxs-lookup"><span data-stu-id="3ead9-116">Using the Row for New Records in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
