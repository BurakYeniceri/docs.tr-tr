---
title: ImeMode Özelliğiyle Asya Karakterlerinin Görüntülenmesi
ms.date: 03/30/2017
helpviewer_keywords:
- Asian languages [Windows Forms], displaying with ImeMode
- Chinese characters [Windows Forms], displaying with ImeMode
- IME mode
- Japanese characters [Windows Forms], displaying with ImeMode
- international applications [Windows Forms], character display
- international characters
- Korean characters
- Asian languages
- Input Method Editor (IME), mode
- localization [Windows Forms], character sets
- globalization [Windows Forms], character sets
ms.assetid: c60ae399-0dab-4f07-9dea-6dbfb15ec0ae
ms.openlocfilehash: d3733f642d4218c851040582ee5637b5486a7804
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2018
ms.locfileid: "36208483"
---
# <a name="display-of-asian-characters-with-the-imemode-property"></a><span data-ttu-id="854a6-102">ImeMode Özelliğiyle Asya Karakterlerinin Görüntülenmesi</span><span class="sxs-lookup"><span data-stu-id="854a6-102">Display of Asian Characters with the ImeMode Property</span></span>
<span data-ttu-id="854a6-103"><xref:System.Windows.Forms.Control.ImeMode%2A> Özelliği formlar ve denetimler tarafından bir Giriş Yöntemi Düzenleyicisi (IME) için belirli bir mod zorlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="854a6-103">The <xref:System.Windows.Forms.Control.ImeMode%2A> property is used by forms and controls to force a specific mode for an input method editor (IME).</span></span> <span data-ttu-id="854a6-104">IME bu yazı sistemleri karakterlerden için normal bir klavye olarak kodlanmış daha fazlasına sahip olduğundan, Çince, Japonca ve Korece komut dosyaları yazmak için temel bir bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="854a6-104">The IME is an essential component for writing Chinese, Japanese, and Korean scripts, since these writing systems have more characters than can be encoded for a regular keyboard.</span></span> <span data-ttu-id="854a6-105">Örneğin, yalnızca ASCII karakterleri belirli metin kutusunda izin vermek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="854a6-105">For example, you may want to allow only ASCII characters in a particular text box.</span></span> <span data-ttu-id="854a6-106">Böyle bir durumda ayarladığınız <xref:System.Windows.Forms.Control.ImeMode%2A> özelliğine <xref:System.Windows.Forms.ImeMode> ve kullanıcıların yalnızca ASCII karakterler için belirli metin kutusuna girmeniz mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="854a6-106">In such a case you can set the <xref:System.Windows.Forms.Control.ImeMode%2A> property to <xref:System.Windows.Forms.ImeMode> and users will only be able to enter ASCII characters for that particular text box.</span></span> <span data-ttu-id="854a6-107">Varsayılan değer olan <xref:System.Windows.Forms.Control.ImeMode%2A> özelliği <xref:System.Windows.Forms.ImeMode>, bu özellik için bir form ayarlarsanız, formdaki tüm denetimler bu ayarı devralır.</span><span class="sxs-lookup"><span data-stu-id="854a6-107">The default value of the <xref:System.Windows.Forms.Control.ImeMode%2A> property is <xref:System.Windows.Forms.ImeMode>, so if you set the property for a form, all controls on the form will inherit that setting.</span></span> <span data-ttu-id="854a6-108">Daha fazla bilgi için bkz: <xref:System.Windows.Forms.Control.ImeMode%2A> ) ve <xref:System.Windows.Forms.ImeMode>.</span><span class="sxs-lookup"><span data-stu-id="854a6-108">For more information, see <xref:System.Windows.Forms.Control.ImeMode%2A> ) and <xref:System.Windows.Forms.ImeMode>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="854a6-109">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="854a6-109">See also</span></span>

[<span data-ttu-id="854a6-110">Windows Forms uygulamaları Genelleştirme</span><span class="sxs-lookup"><span data-stu-id="854a6-110">Globalizing Windows Forms applications</span></span>](globalizing-windows-forms.md)
