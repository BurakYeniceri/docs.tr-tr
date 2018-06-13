---
title: 'Nasıl yapılır: Kalem Oluşturma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- graphics [Windows Forms], creating pens
- pens [Windows Forms], creating
- Pen object
ms.assetid: 7fbea8b7-7ac1-4413-9c17-733a850381e3
ms.openlocfilehash: aff1771af12a9f59127a9f21f4b692d6214c457d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33520984"
---
# <a name="how-to-create-a-pen"></a><span data-ttu-id="20bc0-102">Nasıl yapılır: Kalem Oluşturma</span><span class="sxs-lookup"><span data-stu-id="20bc0-102">How to: Create a Pen</span></span>
<span data-ttu-id="20bc0-103">Bu örnekte bir <xref:System.Drawing.Pen> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="20bc0-103">This example creates a <xref:System.Drawing.Pen> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="20bc0-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="20bc0-104">Example</span></span>  
 [!code-cpp[System.Drawing.ConceptualHowTos#3](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#3)]
 [!code-csharp[System.Drawing.ConceptualHowTos#3](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#3)]
 [!code-vb[System.Drawing.ConceptualHowTos#3](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#3)]  
  
## <a name="robust-programming"></a><span data-ttu-id="20bc0-105">Güçlü Programlama</span><span class="sxs-lookup"><span data-stu-id="20bc0-105">Robust Programming</span></span>  
 <span data-ttu-id="20bc0-106">Sistem kaynakları gibi kullanabilecek nesneleri kullanmayı bitirdikten sonra <xref:System.Drawing.Pen> nesneleri çağrı <xref:System.Drawing.Pen.Dispose%2A> bunlardaki.</span><span class="sxs-lookup"><span data-stu-id="20bc0-106">After you have finished using objects that consume system resources, such as <xref:System.Drawing.Pen> objects, you should call <xref:System.Drawing.Pen.Dispose%2A> on them.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20bc0-107">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="20bc0-107">See Also</span></span>  
 <xref:System.Drawing.Pen>  
 [<span data-ttu-id="20bc0-108">Grafik Programlamaya Başlarken</span><span class="sxs-lookup"><span data-stu-id="20bc0-108">Getting Started with Graphics Programming</span></span>](../../../../docs/framework/winforms/advanced/getting-started-with-graphics-programming.md)  
 [<span data-ttu-id="20bc0-109">GDI+'da Kalemler, Çizgiler ve Dikdörtgenler</span><span class="sxs-lookup"><span data-stu-id="20bc0-109">Pens, Lines, and Rectangles in GDI+</span></span>](../../../../docs/framework/winforms/advanced/pens-lines-and-rectangles-in-gdi.md)
