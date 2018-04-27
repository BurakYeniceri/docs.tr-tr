---
title: Derleme için gerekli referans &#39; &lt;assemblyIdentity&gt; &#39; türünü içeren &#39; &lt;typename&gt;&#39;, ancak uygun bir başvuru arasındaki belirsizlik nedeniyle bulunamadı projeleri &#39; &lt;projectname1&gt; &#39; ve &#39; &lt;projectname2&gt;&#39;
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30969
- vbc30969
helpviewer_keywords:
- BC30969
ms.assetid: 1b29dbc5-8268-45fe-bfc2-b2070a5c845c
caps.latest.revision: 11
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 69b1184d47e427bd985c3b18135d4a0ac4d91410
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2018
---
# <a name="reference-required-to-assembly-39ltassemblyidentitygt39-containing-type-39lttypenamegt39-but-a-suitable-reference-could-not-be-found-due-to-ambiguity-between-projects-39ltprojectname1gt39-and-39ltprojectname2gt39"></a><span data-ttu-id="33082-102">Derleme için gerekli referans &#39; &lt;assemblyIdentity&gt; &#39; türünü içeren &#39; &lt;typename&gt;&#39;, ancak uygun bir başvuru arasındaki belirsizlik nedeniyle bulunamadı projeleri &#39; &lt;projectname1&gt; &#39; ve &#39; &lt;projectname2&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="33082-102">Reference required to assembly &#39;&lt;assemblyidentity&gt;&#39; containing type &#39;&lt;typename&gt;&#39;, but a suitable reference could not be found due to ambiguity between projects &#39;&lt;projectname1&gt;&#39; and &#39;&lt;projectname2&gt;&#39;</span></span>
<span data-ttu-id="33082-103">Sınıfı, yapısı, arabirim, numaralandırma veya projenizin dışında tanımlı temsilci, gibi bir tür bir ifade kullanır.</span><span class="sxs-lookup"><span data-stu-id="33082-103">An expression uses a type, such as a class, structure, interface, enumeration, or delegate, that is defined outside your project.</span></span> <span data-ttu-id="33082-104">Ancak, birden fazla derleme bu türünü tanımlamak için proje başvuruları sahip.</span><span class="sxs-lookup"><span data-stu-id="33082-104">However, you have project references to more than one assembly defining that type.</span></span>  
  
 <span data-ttu-id="33082-105">Alıntı projeleri aynı ada sahip derlemeler üretir.</span><span class="sxs-lookup"><span data-stu-id="33082-105">The cited projects produce assemblies with the same name.</span></span> <span data-ttu-id="33082-106">Bu nedenle, derleyicinin türü için kullanmak üzere hangi derleme erişme belirleyemiyor.</span><span class="sxs-lookup"><span data-stu-id="33082-106">Therefore, the compiler cannot determine which assembly to use for the type you are accessing.</span></span>  
  
 <span data-ttu-id="33082-107">Başka bir derlemede tanımlanan bir türü erişmek için Visual Basic derleyici bu derleme başvurusu olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="33082-107">To access a type defined in another assembly, the Visual Basic compiler must have a reference to that assembly.</span></span> <span data-ttu-id="33082-108">Bu, projeler arasında döngüsel başvuru neden olmaz tek ve anlaşılır bir başvurusu olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="33082-108">This must be a single, unambiguous reference that does not cause circular references among projects.</span></span>  
  
 <span data-ttu-id="33082-109">**Hata Kimliği:** BC30969</span><span class="sxs-lookup"><span data-stu-id="33082-109">**Error ID:** BC30969</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="33082-110">Bu hatayı düzeltmek için</span><span class="sxs-lookup"><span data-stu-id="33082-110">To correct this error</span></span>  
  
1.  <span data-ttu-id="33082-111">Başvurmak için en iyi derleme projeniz için hangi proje üreten belirler.</span><span class="sxs-lookup"><span data-stu-id="33082-111">Determine which project produces the best assembly for your project to reference.</span></span> <span data-ttu-id="33082-112">Bu karar, dosya erişim kolaylığı ve güncelleştirme sıklığını gibi ölçütlere kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="33082-112">For this decision, you might use criteria such as ease of file access and frequency of updates.</span></span>  
  
2.  <span data-ttu-id="33082-113">Proje Özellikleri'nde, kullanmakta olduğunuz türü tanımlayan derleme içeren dosyaya bir başvuru ekleyin.</span><span class="sxs-lookup"><span data-stu-id="33082-113">In your project properties, add a reference to the file that contains the assembly that defines the type you are using.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33082-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="33082-114">See Also</span></span>  
 [<span data-ttu-id="33082-115">Bir projedeki başvuruları yönetme</span><span class="sxs-lookup"><span data-stu-id="33082-115">Managing references in a project</span></span>](/visualstudio/ide/managing-references-in-a-project)  
 [<span data-ttu-id="33082-116">Bildirilmiş Öğelere Başvurular</span><span class="sxs-lookup"><span data-stu-id="33082-116">References to Declared Elements</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)  
   
 [<span data-ttu-id="33082-117">Proje ve Çözüm Özelliklerini Yönetme</span><span class="sxs-lookup"><span data-stu-id="33082-117">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)  
 [<span data-ttu-id="33082-118">Bozuk Başvurularda Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="33082-118">Troubleshooting Broken References</span></span>](/visualstudio/ide/troubleshooting-broken-references)
