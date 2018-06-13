---
title: 'Nasıl yapılır: Formlar ve Denetimler için İki Kez Arabelleğe Alma ile Grafik Titreşimini Azaltma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing in Windows Forms
- graphics [Windows Forms], reducing double-buffered flicker
ms.assetid: 91083d3a-653f-4f15-a467-0f37b2aa39d6
ms.openlocfilehash: 6e11e364af5dc361a24cdd88d72432d6ba4d4058
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33522860"
---
# <a name="how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls"></a><span data-ttu-id="b5bc9-102">Nasıl yapılır: Formlar ve Denetimler için İki Kez Arabelleğe Alma ile Grafik Titreşimini Azaltma</span><span class="sxs-lookup"><span data-stu-id="b5bc9-102">How to: Reduce Graphics Flicker with Double Buffering for Forms and Controls</span></span>
<span data-ttu-id="b5bc9-103">İki kez arabelleğe alma bellek arabelleği birden çok boyama işlemlerle ilişkili titreşimi sorunları ele almak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-103">Double buffering uses a memory buffer to address the flicker problems associated with multiple paint operations.</span></span> <span data-ttu-id="b5bc9-104">İki kez arabelleğe alma etkinleştirildiğinde, tüm boyama işlemleri ilk ekranda çizim yüzeyini yerine bir arabelleğe işlenir.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-104">When double buffering is enabled, all paint operations are first rendered to a memory buffer instead of the drawing surface on the screen.</span></span> <span data-ttu-id="b5bc9-105">Tüm boyama işlemleri tamamlandıktan sonra Ara belleğe doğrudan ilişkili çizim yüzeyini kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-105">After all paint operations are completed, the memory buffer is copied directly to the drawing surface associated with it.</span></span> <span data-ttu-id="b5bc9-106">Yalnızca bir grafik işlem ekranda gerçekleştirildiğinden, karmaşık boyama işlemlerle ilişkili görüntü titremeyi ortadan kalkar. Çoğu uygulama için varsayılan iki kez arabelleğe alma sağladığı [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] en iyi sonuçlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-106">Because only one graphics operation is performed on the screen, the image flickering associated with complex painting operations is eliminated.For most applications, the default double buffering provided by the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] will provide the best results.</span></span> <span data-ttu-id="b5bc9-107">Varsayılan olarak arabelleğe alınan standart Windows Forms denetimleri çift.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-107">Standard Windows Forms controls are double buffered by default.</span></span> <span data-ttu-id="b5bc9-108">Varsayılan, formlarda arabelleğe alma çift etkinleştirebilirsiniz ve denetimleri iki yolla yazıldı.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-108">You can enable default double buffering in your forms and authored controls in two ways.</span></span> <span data-ttu-id="b5bc9-109">Ya da ayarlayabilirsiniz <xref:System.Windows.Forms.Control.DoubleBuffered%2A> özelliğine `true`, ya da çağırabilirsiniz <xref:System.Windows.Forms.Control.SetStyle%2A> ayarlamak için yöntemin <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> bayrağını `true`.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-109">You can either set the <xref:System.Windows.Forms.Control.DoubleBuffered%2A> property to `true`, or you can call the <xref:System.Windows.Forms.Control.SetStyle%2A> method to set the <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> flag to `true`.</span></span> <span data-ttu-id="b5bc9-110">Her iki yöntem varsayılan çift form veya denetim için arabelleğe almayı etkinleştir ve titreşimsiz grafik işleme sağlayın.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-110">Both methods will enable default double buffering for your form or control and provide flicker-free graphics rendering.</span></span> <span data-ttu-id="b5bc9-111">Çağırma <xref:System.Windows.Forms.Control.SetStyle%2A> yöntemi için yazdığınız tüm işleme kod yalnızca fazla özel denetimler için önerilir.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-111">Calling the <xref:System.Windows.Forms.Control.SetStyle%2A> method is recommended only for custom controls for which you have written all the rendering code.</span></span>  
  
 <span data-ttu-id="b5bc9-112">Animasyon veya gelişmiş bellek yönetimi gibi daha gelişmiş çift arabelleğe alma senaryoları için kendi çift arabelleğe alma mantığını uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-112">For more advanced double buffering scenarios, such as animation or advanced memory management, you can implement your own double buffering logic.</span></span> <span data-ttu-id="b5bc9-113">Daha fazla bilgi için bkz: [nasıl yapılır: el ile arabelleğe alınan grafikleri yönetme](../../../../docs/framework/winforms/advanced/how-to-manually-manage-buffered-graphics.md).</span><span class="sxs-lookup"><span data-stu-id="b5bc9-113">For more information, see [How to: Manually Manage Buffered Graphics](../../../../docs/framework/winforms/advanced/how-to-manually-manage-buffered-graphics.md).</span></span>  
  
### <a name="to-reduce-flicker"></a><span data-ttu-id="b5bc9-114">Titreşimi azaltmak için</span><span class="sxs-lookup"><span data-stu-id="b5bc9-114">To reduce flicker</span></span>  
  
-   <span data-ttu-id="b5bc9-115">Ayarlama <xref:System.Windows.Forms.Control.DoubleBuffered%2A> özelliğine `true`.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-115">Set the <xref:System.Windows.Forms.Control.DoubleBuffered%2A> property to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#31](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#31)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#31](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#31)]  
  
 <span data-ttu-id="b5bc9-116">\- veya -</span><span class="sxs-lookup"><span data-stu-id="b5bc9-116">\- or -</span></span>  
  
-   <span data-ttu-id="b5bc9-117">Çağrı <xref:System.Windows.Forms.Control.SetStyle%2A> ayarlamak için yöntemin <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> bayrağını `true`.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-117">Call the <xref:System.Windows.Forms.Control.SetStyle%2A> method to set the <xref:System.Windows.Forms.ControlStyles.OptimizedDoubleBuffer> flag to `true`.</span></span>  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#32](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#32)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#32](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#32)]  
  
## <a name="see-also"></a><span data-ttu-id="b5bc9-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="b5bc9-118">See Also</span></span>  
 <xref:System.Windows.Forms.Control.DoubleBuffered%2A>  
 <xref:System.Windows.Forms.Control.SetStyle%2A>  
 [<span data-ttu-id="b5bc9-119">İki Kez Arabelleğe Alınan Grafikler</span><span class="sxs-lookup"><span data-stu-id="b5bc9-119">Double Buffered Graphics</span></span>](../../../../docs/framework/winforms/advanced/double-buffered-graphics.md)  
 [<span data-ttu-id="b5bc9-120">Windows Forms’da Grafikler ve Çizim</span><span class="sxs-lookup"><span data-stu-id="b5bc9-120">Graphics and Drawing in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
