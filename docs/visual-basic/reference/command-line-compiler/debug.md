---
title: /debug (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- debug compiler switches
- /debug compiler option [Visual Basic]
- -debug compiler option [Visual Basic]
- debug compiler option [Visual Basic]
ms.assetid: c2b0bea5-1d5e-499f-9bd5-4f6c6b715ea2
caps.latest.revision: "18"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: f1c90b28f1df18e7e0a4f9e22730e1c3476fa650
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="debug-visual-basic"></a><span data-ttu-id="751cd-102">/debug (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="751cd-102">/debug (Visual Basic)</span></span>
<span data-ttu-id="751cd-103">Hata ayıklama bilgileri oluşturmak ve çıktı dosyasında yerleştirmek derleyici neden olur.</span><span class="sxs-lookup"><span data-stu-id="751cd-103">Causes the compiler to generate debugging information and place it in the output file(s).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="751cd-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="751cd-104">Syntax</span></span>  
  
```  
/debug[+ | -]  
' -or-  
/debug:[full | pdbonly]  
```  
  
## <a name="arguments"></a><span data-ttu-id="751cd-105">Arguments</span><span class="sxs-lookup"><span data-stu-id="751cd-105">Arguments</span></span>  
  
|<span data-ttu-id="751cd-106">Terim</span><span class="sxs-lookup"><span data-stu-id="751cd-106">Term</span></span>|<span data-ttu-id="751cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="751cd-107">Definition</span></span>|  
|---|---|  
|<span data-ttu-id="751cd-108">`+` &#124; `-`</span><span class="sxs-lookup"><span data-stu-id="751cd-108">`+` &#124; `-`</span></span>|<span data-ttu-id="751cd-109">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="751cd-109">Optional.</span></span> <span data-ttu-id="751cd-110">Belirtme `+` veya `/debug` hata ayıklama bilgileri oluşturmak ve bir .pdb dosyasını yerleştirmek derleyici neden olur.</span><span class="sxs-lookup"><span data-stu-id="751cd-110">Specifying `+` or `/debug` causes the compiler to generate debugging information and place it in a .pdb file.</span></span> <span data-ttu-id="751cd-111">Belirtme `-` değil belirtme aynı etkiye sahip `/debug`.</span><span class="sxs-lookup"><span data-stu-id="751cd-111">Specifying `-` has the same effect as not specifying `/debug`.</span></span>|  
|<span data-ttu-id="751cd-112">`full` &#124; `pdbonly`</span><span class="sxs-lookup"><span data-stu-id="751cd-112">`full` &#124; `pdbonly`</span></span>|<span data-ttu-id="751cd-113">İsteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="751cd-113">Optional.</span></span> <span data-ttu-id="751cd-114">Derleyici tarafından üretilen hata ayıklama bilgi türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="751cd-114">Specifies the type of debugging information generated by the compiler.</span></span> <span data-ttu-id="751cd-115">Belirtmezseniz, `/debug:pdbonly`, varsayılan `full`, çalışan programa bir hata ayıklayıcısı eklemeniz sağlar.</span><span class="sxs-lookup"><span data-stu-id="751cd-115">If you do not specify `/debug:pdbonly`, the default is `full`, which enables you to attach a debugger to the running program.</span></span> <span data-ttu-id="751cd-116">`pdbonly` Bağımsız değişkene izin veriyor kaynak kodu hata ayıklama Hata Ayıklayıcısı'ndaki program başlatılır, ancak yalnızca çalışan program için hata ayıklayıcı iliştirildiğinde assembly dili kodunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="751cd-116">The `pdbonly` argument allows source-code debugging when the program is started in the debugger, but it displays assembly-language code only when the running program is attached to the debugger.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="751cd-117">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="751cd-117">Remarks</span></span>  
 <span data-ttu-id="751cd-118">Hata ayıklama yapıları oluşturmak için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="751cd-118">Use this option to create debug builds.</span></span> <span data-ttu-id="751cd-119">Belirtmezseniz, `/debug`, `/debug+`, veya `/debug:full`, programınızın çıktı dosyasında hata ayıklama mümkün olmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="751cd-119">If you do not specify `/debug`, `/debug+`, or `/debug:full`, you will be unable to debug the output file of your program.</span></span>  
  
 <span data-ttu-id="751cd-120">Varsayılan olarak, hata ayıklama bilgileri değil yayılan (`/debug-`).</span><span class="sxs-lookup"><span data-stu-id="751cd-120">By default, debugging information is not emitted (`/debug-`).</span></span> <span data-ttu-id="751cd-121">Hata ayıklama bilgilerini göster için belirtmeniz `/debug` veya `/debug+`.</span><span class="sxs-lookup"><span data-stu-id="751cd-121">To emit debugging information, specify `/debug` or `/debug+`.</span></span>  
  
 <span data-ttu-id="751cd-122">Bir uygulamanın hata ayıklama performansını yapılandırma hakkında daha fazla bilgi için bkz: [bir görüntü Debug kolaylaştırma](../../../framework/debug-trace-profile/making-an-image-easier-to-debug.md).</span><span class="sxs-lookup"><span data-stu-id="751cd-122">For information on how to configure the debug performance of an application, see [Making an Image Easier to Debug](../../../framework/debug-trace-profile/making-an-image-easier-to-debug.md).</span></span>  
  
|<span data-ttu-id="751cd-123">Tümleşik geliştirme ortamı/Debug Visual Studio'da ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="751cd-123">To set /debug in the Visual Studio integrated development environment</span></span>|  
|---|  
|<span data-ttu-id="751cd-124">1.  Seçili bir proje ile **Çözüm Gezgini**, **proje** menüsünde tıklatın **özellikleri**.</span><span class="sxs-lookup"><span data-stu-id="751cd-124">1.  With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.</span></span> <span data-ttu-id="751cd-125">Daha fazla bilgi için bkz: [Proje Tasarımcısı giriş](http://msdn.microsoft.com/en-us/898dd854-c98d-430c-ba1b-a913ce3c73d7).</span><span class="sxs-lookup"><span data-stu-id="751cd-125">For more information, see [Introduction to the Project Designer](http://msdn.microsoft.com/en-us/898dd854-c98d-430c-ba1b-a913ce3c73d7).</span></span><br /><span data-ttu-id="751cd-126">2.  Tıklatın **derleme** sekmesi.</span><span class="sxs-lookup"><span data-stu-id="751cd-126">2.  Click the **Compile** tab.</span></span><br /><span data-ttu-id="751cd-127">3.  Tıklatın **Gelişmiş derleme seçenekleri**.</span><span class="sxs-lookup"><span data-stu-id="751cd-127">3.  Click **Advanced Compile Options**.</span></span><br /><span data-ttu-id="751cd-128">4.  Değer değiştirme **hata ayıklama bilgisi üret** kutusu.</span><span class="sxs-lookup"><span data-stu-id="751cd-128">4.  Modify the value in the **Generate Debug Info** box.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="751cd-129">Örnek</span><span class="sxs-lookup"><span data-stu-id="751cd-129">Example</span></span>  
 <span data-ttu-id="751cd-130">Aşağıdaki örnek çıkış dosyasında hata ayıklama bilgilerini koyar `App.exe`.</span><span class="sxs-lookup"><span data-stu-id="751cd-130">The following example puts debugging information in output file `App.exe`.</span></span>  
  
```  
vbc /debug /out:app.exe test.vb  
```  
  
## <a name="see-also"></a><span data-ttu-id="751cd-131">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="751cd-131">See Also</span></span>  
 [<span data-ttu-id="751cd-132">Visual Basic komut satırı derleyicisi</span><span class="sxs-lookup"><span data-stu-id="751cd-132">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="751cd-133">/ bugreport</span><span class="sxs-lookup"><span data-stu-id="751cd-133">/bugreport</span></span>](../../../visual-basic/reference/command-line-compiler/bugreport.md)  
 [<span data-ttu-id="751cd-134">Örnek derleme komut satırları</span><span class="sxs-lookup"><span data-stu-id="751cd-134">Sample Compilation Command Lines</span></span>](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)