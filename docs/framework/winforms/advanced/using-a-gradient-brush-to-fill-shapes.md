---
title: "Şekilleri Doldurmak için Gradyan Fırçası Kullanma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- brushes [Windows Forms], gradient brushes
- gradient brushes
- examples [Windows Forms], gradient brushes
ms.assetid: 2c6037b9-05bd-44c0-a22a-19584b722524
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 5a1c4ab7c2ee6f7164b6158dcb4ca4721be12650
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2017
---
# <a name="using-a-gradient-brush-to-fill-shapes"></a><span data-ttu-id="9a7d7-102">Şekilleri Doldurmak için Gradyan Fırçası Kullanma</span><span class="sxs-lookup"><span data-stu-id="9a7d7-102">Using a Gradient Brush to Fill Shapes</span></span>
<span data-ttu-id="9a7d7-103">Bir şekli kademeli olarak değişen bir renkle doldurmak için gradyan fırçası kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-103">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="9a7d7-104">Örneğin, bir şekli şeklin sol kenarından sağ kenarı hareket ederken, yavaş yavaş değişir renkle doldurma için yatay bir gradyan kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-104">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="9a7d7-105">Dikdörtgene siyah olan sol kenar düşünün (kırmızı, yeşil ve mavi bileşenleri tarafından temsil edilen 0, 0, 0) ve bir sağ kenar diğer bir deyişle kırmızı (255, 0, 0 tarafından gösterilen).</span><span class="sxs-lookup"><span data-stu-id="9a7d7-105">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="9a7d7-106">Dikdörtgen 256 piksel genişliğinde ise, verilen piksel kırmızı bileşeninin bir solunda piksel kırmızı bileşeninin fazla olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-106">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="9a7d7-107">Bir satırda soldaki piksel renk bileşenleri (0, 0, 0) varsa, ikinci piksel (1, 0, 0) sahip, üçüncü piksel (2, 0, 0) sahip vb. renk bileşenleri (255, 0, 0) sahip bir sağdaki piksel ulaşana kadar.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-107">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="9a7d7-108">Bu Ara değerli renk değerleri renk gradyan olun.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-108">These interpolated color values make up the color gradient.</span></span>  
  
 <span data-ttu-id="9a7d7-109">Yatay, dikey taşımak veya belirli bir Eğimli satırını paralel olarak doğrusal gradyan rengi değişir.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-109">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="9a7d7-110">Sınır bir yolu ve iç hakkında taşırken yol gradyanı rengi değişir.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-110">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="9a7d7-111">Yol gradyanları çok çeşitli efektler elde etmek için özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-111">You can customize path gradients to achieve a wide variety of effects.</span></span>  
  
 <span data-ttu-id="9a7d7-112">Aşağıdaki çizimde bir dikdörtgen doğrusal gradyan fırçası ile doldurulur ve yolun gradyan fırçası ile elips doldurulmuş gösterir.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-112">The following illustration shows a rectangle filled with a linear gradient brush and an ellipse filled with a path gradient brush.</span></span>  
  
 <span data-ttu-id="9a7d7-113">![Gradyan](../../../../docs/framework/winforms/advanced/media/gradient2.png "gradient2")</span><span class="sxs-lookup"><span data-stu-id="9a7d7-113">![Gradient](../../../../docs/framework/winforms/advanced/media/gradient2.png "gradient2")</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9a7d7-114">Bu Bölümde</span><span class="sxs-lookup"><span data-stu-id="9a7d7-114">In This Section</span></span>  
 [<span data-ttu-id="9a7d7-115">Nasıl yapılır: doğrusal gradyan oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a7d7-115">How to: Create a Linear Gradient</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-a-linear-gradient.md)  
 <span data-ttu-id="9a7d7-116">Doğrusal gradyan kullanarak bir oluşturmayı gösteren <xref:System.Drawing.Drawing2D.LinearGradientBrush> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-116">Shows how to create a linear gradient using the <xref:System.Drawing.Drawing2D.LinearGradientBrush> class.</span></span>  
  
 [<span data-ttu-id="9a7d7-117">Nasıl yapılır: yol gradyanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a7d7-117">How to: Create a Path Gradient</span></span>](../../../../docs/framework/winforms/advanced/how-to-create-a-path-gradient.md)  
 <span data-ttu-id="9a7d7-118">Kullanarak bir yol gradyanı oluşturma açıklanmaktadır <xref:System.Drawing.Drawing2D.PathGradientBrush> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-118">Describes how to create a path gradient using the <xref:System.Drawing.Drawing2D.PathGradientBrush> class.</span></span>  
  
 [<span data-ttu-id="9a7d7-119">Nasıl yapılır: bir Gradyana gama düzeltmesi uygulama</span><span class="sxs-lookup"><span data-stu-id="9a7d7-119">How to: Apply Gamma Correction to a Gradient</span></span>](../../../../docs/framework/winforms/advanced/how-to-apply-gamma-correction-to-a-gradient.md)  
 <span data-ttu-id="9a7d7-120">Gama düzeltmesi ile bir gradyan fırçası kullanımı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-120">Explains how to use gamma correction with a gradient brush.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="9a7d7-121">Başvuru</span><span class="sxs-lookup"><span data-stu-id="9a7d7-121">Reference</span></span>  
 <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>  
 <span data-ttu-id="9a7d7-122">Bu sınıf için bir açıklama içerir ve tüm üyeleri bağlantılar içerir.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-122">Contains a description of this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Drawing2D.PathGradientBrush?displayProperty=nameWithType>  
 <span data-ttu-id="9a7d7-123">Bu sınıf için bir açıklama içerir ve tüm üyeleri bağlantılar içerir.</span><span class="sxs-lookup"><span data-stu-id="9a7d7-123">Contains a description of this class and has links to all of its members.</span></span>