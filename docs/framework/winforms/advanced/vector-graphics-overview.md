---
title: "Vektör Grafiklerine Genel Bakış"
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
- inclusive-inclusive endpoints
- coordinate systems
- graphics [Windows Forms], vector graphics
ms.assetid: 0195df81-66be-452d-bb53-5a582ebfdc09
caps.latest.revision: "16"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 7bb3247f531a0dac83657e118fb53ebaf708ec9a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="vector-graphics-overview"></a><span data-ttu-id="d39a2-102">Vektör Grafiklerine Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="d39a2-102">Vector Graphics Overview</span></span>
[!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]<span data-ttu-id="d39a2-103">çizgiler, dikdörtgenler ve diğer şekiller bir koordinat sistemi çizer.</span><span class="sxs-lookup"><span data-stu-id="d39a2-103"> draws lines, rectangles, and other shapes on a coordinate system.</span></span> <span data-ttu-id="d39a2-104">Koordinat sistemleri çeşitli arasından seçebilirsiniz, ancak varsayılan koordinat sistemi kaynağını sol üst köşedeki sağa ve aşağı işaret eden y ekseni işaret eden x eksenine sahip.</span><span class="sxs-lookup"><span data-stu-id="d39a2-104">You can choose from a variety of coordinate systems, but the default coordinate system has the origin in the upper-left corner with the x-axis pointing to the right and the y-axis pointing down.</span></span> <span data-ttu-id="d39a2-105">Piksel varsayılan koordinat sistemi ölçü birimidir.</span><span class="sxs-lookup"><span data-stu-id="d39a2-105">The unit of measure in the default coordinate system is the pixel.</span></span>  
  
## <a name="the-building-blocks-of-gdi"></a><span data-ttu-id="d39a2-106">GDI + yapı taşları</span><span class="sxs-lookup"><span data-stu-id="d39a2-106">The Building Blocks of GDI+</span></span>  
 <span data-ttu-id="d39a2-107">![Vektör grafik](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art01.gif "AboutGdip02_Art01")</span><span class="sxs-lookup"><span data-stu-id="d39a2-107">![Vector graphic](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art01.gif "AboutGdip02_Art01")</span></span>  
  
 <span data-ttu-id="d39a2-108">Bir bilgisayar monitörü resim öğelerinin veya piksel olarak adlandırılan nokta dikdörtgen bir dizi görünümünü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d39a2-108">A computer monitor creates its display on a rectangular array of dots called picture elements or pixels.</span></span> <span data-ttu-id="d39a2-109">Sonraki bir izleyiciden ekrandaki piksel sayısı değişir ve tek tek bir monitörde görünür piksel sayısı genellikle bir ölçüde kullanıcı tarafından yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="d39a2-109">The number of pixels that appear on the screen varies from one monitor to the next, and the number of pixels that appear on an individual monitor can usually be configured to some extent by the user.</span></span>  
  
 <span data-ttu-id="d39a2-110">![Vektör grafik](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art02.gif "AboutGdip02_Art02")</span><span class="sxs-lookup"><span data-stu-id="d39a2-110">![Vector graphic](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art02.gif "AboutGdip02_Art02")</span></span>  
  
 <span data-ttu-id="d39a2-111">Kullandığınızda [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] çizgi, dikdörtgen veya eğri çizmek için çizilecek öğeyle ilgili anahtar bazı bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="d39a2-111">When you use [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] to draw a line, rectangle, or curve, you provide certain key information about the item to be drawn.</span></span> <span data-ttu-id="d39a2-112">Örneğin, bir satır, iki nokta sağlayarak belirtebilir ve bir nokta, yükseklik ve genişlik sağlayarak bir dikdörtgen belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d39a2-112">For example, you can specify a line by providing two points, and you can specify a rectangle by providing a point, a height, and a width.</span></span> [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)]<span data-ttu-id="d39a2-113">Satır, dikdörtgende veya eğri göstermek için hangi piksel açılmalıdır belirlemek için görüntüleme sürücü yazılımı ile birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="d39a2-113"> works in conjunction with the display driver software to determine which pixels must be turned on to show the line, rectangle, or curve.</span></span> <span data-ttu-id="d39a2-114">Aşağıdaki çizimde bir satır (4, 2) noktadan noktaya (12, 8) görüntülemek için açık piksel gösterir.</span><span class="sxs-lookup"><span data-stu-id="d39a2-114">The following illustration shows the pixels that are turned on to display a line from the point (4, 2) to the point (12, 8).</span></span>  
  
 <span data-ttu-id="d39a2-115">![Vektör grafik](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art03.gif "AboutGdip02_Art03")</span><span class="sxs-lookup"><span data-stu-id="d39a2-115">![Vector graphic](../../../../docs/framework/winforms/advanced/media/aboutgdip02-art03.gif "AboutGdip02_Art03")</span></span>  
  
 <span data-ttu-id="d39a2-116">Zaman içinde iki boyutlu resimler oluşturmak için en kullanışlı olması için bazı temel yapı taşlarının kanıtlanmış.</span><span class="sxs-lookup"><span data-stu-id="d39a2-116">Over time, certain basic building blocks have proven to be the most useful for creating two-dimensional pictures.</span></span> <span data-ttu-id="d39a2-117">Tarafından desteklenen tüm bu yapı taşları, [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], aşağıdaki listede verilir:</span><span class="sxs-lookup"><span data-stu-id="d39a2-117">These building blocks, which are all supported by [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)], are given in the following list:</span></span>  
  
-   <span data-ttu-id="d39a2-118">satırları</span><span class="sxs-lookup"><span data-stu-id="d39a2-118">Lines</span></span>  
  
-   <span data-ttu-id="d39a2-119">Dikdörtgenler</span><span class="sxs-lookup"><span data-stu-id="d39a2-119">Rectangles</span></span>  
  
-   <span data-ttu-id="d39a2-120">Üç nokta</span><span class="sxs-lookup"><span data-stu-id="d39a2-120">Ellipses</span></span>  
  
-   <span data-ttu-id="d39a2-121">Yaylar</span><span class="sxs-lookup"><span data-stu-id="d39a2-121">Arcs</span></span>  
  
-   <span data-ttu-id="d39a2-122">Çokgenler</span><span class="sxs-lookup"><span data-stu-id="d39a2-122">Polygons</span></span>  
  
-   <span data-ttu-id="d39a2-123">Ana Eğriler</span><span class="sxs-lookup"><span data-stu-id="d39a2-123">Cardinal splines</span></span>  
  
-   <span data-ttu-id="d39a2-124">Bezier eğrileri</span><span class="sxs-lookup"><span data-stu-id="d39a2-124">Bezier splines</span></span>  
  
## <a name="methods-for-drawing-with-a-graphics-object"></a><span data-ttu-id="d39a2-125">Bir grafik nesnesi ile çizim için yöntemleri</span><span class="sxs-lookup"><span data-stu-id="d39a2-125">Methods For Drawing with a Graphics Object</span></span>  
 <span data-ttu-id="d39a2-126"><xref:System.Drawing.Graphics> Sınıfını [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] önceki listedeki öğeleri çizmek için aşağıdaki yöntemleri sağlar: <xref:System.Drawing.Graphics.DrawLine%2A>, <xref:System.Drawing.Graphics.DrawRectangle%2A>, <xref:System.Drawing.Graphics.DrawEllipse%2A>, <xref:System.Drawing.Graphics.DrawPolygon%2A>, <xref:System.Drawing.Graphics.DrawArc%2A>, <xref:System.Drawing.Graphics.DrawCurve%2A> (için ana Eğriler), ve <xref:System.Drawing.Graphics.DrawBezier%2A>.</span><span class="sxs-lookup"><span data-stu-id="d39a2-126">The <xref:System.Drawing.Graphics> class in [!INCLUDE[ndptecgdiplus](../../../../includes/ndptecgdiplus-md.md)] provides the following methods for drawing the items in the previous list: <xref:System.Drawing.Graphics.DrawLine%2A>, <xref:System.Drawing.Graphics.DrawRectangle%2A>, <xref:System.Drawing.Graphics.DrawEllipse%2A>, <xref:System.Drawing.Graphics.DrawPolygon%2A>, <xref:System.Drawing.Graphics.DrawArc%2A>, <xref:System.Drawing.Graphics.DrawCurve%2A> (for cardinal splines), and <xref:System.Drawing.Graphics.DrawBezier%2A>.</span></span> <span data-ttu-id="d39a2-127">Bu yöntemlerin her biri aşırı yüklendi; diğer bir deyişle, her bir yöntemin birkaç farklı parametre listesi destekler.</span><span class="sxs-lookup"><span data-stu-id="d39a2-127">Each of these methods is overloaded; that is, each method supports several different parameter lists.</span></span> <span data-ttu-id="d39a2-128">Örneğin, bir çeşitlemesi <xref:System.Drawing.Graphics.DrawLine%2A> yöntemi alır bir <xref:System.Drawing.Pen> nesne ve başka bir çeşitlemesi sırasında dört tamsayılar <xref:System.Drawing.Graphics.DrawLine%2A> yöntemi alır bir <xref:System.Drawing.Pen> nesne ve iki <xref:System.Drawing.Point> nesneleri.</span><span class="sxs-lookup"><span data-stu-id="d39a2-128">For example, one variation of the <xref:System.Drawing.Graphics.DrawLine%2A> method receives a <xref:System.Drawing.Pen> object and four integers, while another variation of the <xref:System.Drawing.Graphics.DrawLine%2A> method receives a <xref:System.Drawing.Pen> object and two <xref:System.Drawing.Point> objects.</span></span>  
  
 <span data-ttu-id="d39a2-129">Tek bir çağrısında birden çok öğe çizin çoğul yardımcı yöntemler çizgiler, dikdörtgenler ve Bézier eğrisi çizme yöntemleri vardır: <xref:System.Drawing.Graphics.DrawLines%2A>, <xref:System.Drawing.Graphics.DrawRectangles%2A>, ve <xref:System.Drawing.Graphics.DrawBeziers%2A>.</span><span class="sxs-lookup"><span data-stu-id="d39a2-129">The methods for drawing lines, rectangles, and Bézier splines have plural companion methods that draw several items in a single call: <xref:System.Drawing.Graphics.DrawLines%2A>, <xref:System.Drawing.Graphics.DrawRectangles%2A>, and <xref:System.Drawing.Graphics.DrawBeziers%2A>.</span></span> <span data-ttu-id="d39a2-130">Ayrıca, <xref:System.Drawing.Graphics.DrawCurve%2A> yöntemi sahip bir yardımcı yöntem <xref:System.Drawing.Graphics.DrawClosedCurve%2A>, kapandığında başlatmaya eğrinin bitiş noktasına bağlanarak eğri noktası.</span><span class="sxs-lookup"><span data-stu-id="d39a2-130">Also, the <xref:System.Drawing.Graphics.DrawCurve%2A> method has a companion method, <xref:System.Drawing.Graphics.DrawClosedCurve%2A>, that closes a curve by connecting the ending point of the curve to the starting point.</span></span>  
  
 <span data-ttu-id="d39a2-131">Tüm çizim yöntemlerinden birini <xref:System.Drawing.Graphics> sınıfı ile birlikte çalışma bir <xref:System.Drawing.Pen> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d39a2-131">All of the drawing methods of the <xref:System.Drawing.Graphics> class work in conjunction with a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="d39a2-132">Herhangi bir şey çizmek için en az iki nesne oluşturmanız gerekir: bir <xref:System.Drawing.Graphics> nesne ve <xref:System.Drawing.Pen> nesne.</span><span class="sxs-lookup"><span data-stu-id="d39a2-132">To draw anything, you must create at least two objects: a <xref:System.Drawing.Graphics> object and a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="d39a2-133"><xref:System.Drawing.Pen> Nesnesi çizgi genişliğini ve çizilecek öğesinin rengini gibi özniteliklerini depolar.</span><span class="sxs-lookup"><span data-stu-id="d39a2-133">The <xref:System.Drawing.Pen> object stores attributes, such as line width and color, of the item to be drawn.</span></span> <span data-ttu-id="d39a2-134"><xref:System.Drawing.Pen> Nesnesi, çizim yöntemi için bağımsız değişkenlerden biri geçirilir.</span><span class="sxs-lookup"><span data-stu-id="d39a2-134">The <xref:System.Drawing.Pen> object is passed as one of the arguments to the drawing method.</span></span> <span data-ttu-id="d39a2-135">Örneğin, bir çeşitlemesi <xref:System.Drawing.Graphics.DrawLine%2A> yöntemi alır bir <xref:System.Drawing.Pen> nesne ve 100, 50 yüksekliğini ve sol üst köşesindeki genişliği ile bir dikdörtgen çizer aşağıdaki örnekte gösterildiği gibi dört tamsayılar (20, 10):</span><span class="sxs-lookup"><span data-stu-id="d39a2-135">For example, one variation of the <xref:System.Drawing.Graphics.DrawLine%2A> method receives a <xref:System.Drawing.Pen> object and four integers as shown in the following example, which draws a rectangle with a width of 100, a height of 50 and an upper-left corner of (20, 10):</span></span>  
  
 [!code-csharp[LinesCurvesAndShapes#11](../../../../samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#11)]
 [!code-vb[LinesCurvesAndShapes#11](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#11)]  
  
## <a name="see-also"></a><span data-ttu-id="d39a2-136">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d39a2-136">See Also</span></span>  
 <xref:System.Drawing.Graphics?displayProperty=nameWithType>  
 <xref:System.Drawing.Pen?displayProperty=nameWithType>  
 [<span data-ttu-id="d39a2-137">Çizgiler, eğriler ve şekiller</span><span class="sxs-lookup"><span data-stu-id="d39a2-137">Lines, Curves, and Shapes</span></span>](../../../../docs/framework/winforms/advanced/lines-curves-and-shapes.md)  
 [<span data-ttu-id="d39a2-138">Nasıl yapılır: çizim için grafik nesneleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d39a2-138">How to: Create Graphics Objects for Drawing</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-graphics-objects-for-drawing.md)