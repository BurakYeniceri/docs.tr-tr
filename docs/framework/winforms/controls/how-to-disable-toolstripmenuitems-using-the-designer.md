---
title: 'Nasıl yapılır: Tasarımcıyı Kullanarak ToolStripMenuItems Öğelerini Devre Dışı Bırakma'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], disabling in designer
- MenuStrip control [Windows Forms], disabling menu items in designer
- menu items [Windows Forms], disabling
- menus [Windows Forms], disabling items
ms.assetid: 985e311e-7d67-4205-b5a3-d045b68a4a03
ms.openlocfilehash: f97c622719c0f76fe8ce7ea34b9324110508b6e9
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43523300"
---
# <a name="how-to-disable-toolstripmenuitems-using-the-designer"></a>Nasıl yapılır: Tasarımcıyı Kullanarak ToolStripMenuItems Öğelerini Devre Dışı Bırakma
Sınırlamak veya bir kullanıcı, kullanıcı etkinlikleri için yanıt menü öğelerini devre dışı bırakma ve etkinleştirme yapabilir komutları alanlarını genişletmeniz mümkün değildir. Menü öğeleri, varsayılan olarak etkinleştirilir, bunlar oluşturulur, ancak bu aracılığıyla ayarlanabilir <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> özelliği. Bu özellik tasarım zamanında işleyebileceğiniz **özellikleri** penceresi veya program aracılığıyla kod içinde ayarlama. Daha fazla bilgi için [nasıl yapılır: toolstripmenuıtems öğelerini devre dışı](../../../../docs/framework/winforms/controls/how-to-disable-toolstripmenuitems.md).  
  
> [!NOTE]
>  Gördüğünüz iletişim kutuları ve menü komutları, etkin ayarlarınıza ve ürün sürümüne bağlı olarak Yardım menüsünde açıklanana göre farklılık gösterebilir. Ayarlarınızı değiştirmek için seçin **içeri ve dışarı aktarma ayarları** üzerinde **Araçları** menüsü. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-disable-a-menu-item-at-design-time"></a>Tasarım zamanında bir menü öğesi devre dışı bırakmak için  
  
1.  Formda Seçili Menü öğesiyle ayarlamak <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> özelliğini `false`.  
  
    > [!TIP]
    >  Bir menü ilk veya üst düzey menü öğesi devre dışı bırakma içinde menüyü içeren bütün menü öğelerini devre dışı bırakır. Benzer şekilde, alt öğeleri alt öğeleri içeren bir menü öğesi devre dışı bırakma devre dışı bırakır. Kullanıcıya verilen menüsündeki tüm komutları kullanılamıyorsa, bunu bir temiz kullanıcı arabirimi sunar gibi hem gizlemek ve tüm menü devre dışı bırakmak için iyi bir programlama uygulama kabul edilir. Gizleme hem tek başına bir gizleme için bir menü komutu bir kısayol tuşu aracılığıyla erişimi engellemez menüsü devre dışı bırakın. Ayarlama <xref:System.Windows.Forms.ToolStripItem.Visible%2A> özelliği için bir üst düzey menü öğesinin `false` tüm menü gizlemek için.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStripMenuItem>  
 [Nasıl yapılır: ToolStripMenuItems Gizleme](../../../../docs/framework/winforms/controls/how-to-hide-toolstripmenuitems.md)  
 [MenuStrip Denetimine Genel Bakış](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
