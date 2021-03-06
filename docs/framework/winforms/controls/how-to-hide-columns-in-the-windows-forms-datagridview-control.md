---
title: 'Nasıl yapılır: Windows Forms DataGridView Denetiminde Sütunları Gizleme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], hiding columns
- data grids [Windows Forms], hiding columns
- columns [Windows Forms], hiding
ms.assetid: 3f94143a-2ef0-49a5-a22a-b2e6f9289642
ms.openlocfilehash: 2ddf4b0701ea563465ca3023c73f588f4e0f3a5f
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43504584"
---
# <a name="how-to-hide-columns-in-the-windows-forms-datagridview-control"></a>Nasıl yapılır: Windows Forms DataGridView Denetiminde Sütunları Gizleme
Bazen yalnızca bazı Windows Forms'ta mevcut olan sütunları görüntülemek isteyeceksiniz <xref:System.Windows.Forms.DataGridView> denetimi. Örneğin, bir çalışan göstermek isteyebilirsiniz maaş sütun diğer kullanıcılardan gizleyerek sırasında yönetim kimlik bilgilerine sahip kullanıcılar için. Alternatif olarak, denetimi yalnızca bazılarının görüntülemek istediğiniz çok sayıda sütun içeren bir veri kaynağına bağlamak isteyebilirsiniz. Bu durumda, genellikle görüntülenmesinde ilgilenmediğiniz yerine, bunları gizlemek sütunları kaldırır.  
  
 İçinde <xref:System.Windows.Forms.DataGridView> denetimi <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A> bir sütunun değerini özellik bu sütunun görüntülenip görüntülenmeyeceğini belirtir.  
  
 Visual Studio'da bu görevi için desteği yoktur.  Ayrıca bkz: [nasıl yapılır: Windows Forms DataGridView denetimi kullanarak Tasarımcı Gizle sütunları](https://msdn.microsoft.com/library/kaswfbes\(v=vs.110\)).  
  
### <a name="to-hide-a-column-programmatically"></a>Program aracılığıyla bir sütunu gizlemek için  
  
-   Ayarlama <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType> özelliğini `false`. Gizlemek için bir `CustomerID` veri bağlama sırasında otomatik olarak oluşturulan bir sütuna yerleştirin aşağıdaki kod örneğinde bir <xref:System.Windows.Forms.DataGridView.DataBindingComplete> olay işleyicisi.  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#063](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#063)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#063](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#063)]  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
-   A <xref:System.Windows.Forms.DataGridView> adlı Denetim `dataGridView1` adlı bir sütun içeren `CustomerID`.  
  
-   Başvurular <xref:System?displayProperty=nameWithType> ve <xref:System.Windows.Forms?displayProperty=nameWithType> derlemeler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Forms.DataGridView>  
 <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>  
 [Windows Forms DataGridView Denetimindeki Temel Sütun, Satır ve Hücre Özellikleri](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)  
 [Nasıl yapılır: Otomatik Oluşturulan Sütunları Windows Forms DataGridView Denetiminden Kaldırma](../../../../docs/framework/winforms/controls/remove-autogenerated-columns-from-a-wf-datagridview-control.md)  
 [Nasıl yapılır: Windows Forms DataGridView Denetiminde Sütunların Sırasını Değiştirme](../../../../docs/framework/winforms/controls/how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md)
