---
title: 'Nasıl yapılır: EdmGen.exe Model ve eşleme dosyalarını doğrulama için kullanın'
ms.date: 03/30/2017
ms.assetid: 2641906a-971a-4d0b-8aee-13fabc02a1cc
ms.openlocfilehash: fda8698381e98c64318f1a26f77f0263e9085074
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43512451"
---
# <a name="how-to-use-edmgenexe-to-validate-model-and-mapping-files"></a><span data-ttu-id="2d78c-102">Nasıl yapılır: EdmGen.exe Model ve eşleme dosyalarını doğrulama için kullanın</span><span class="sxs-lookup"><span data-stu-id="2d78c-102">How to: Use EdmGen.exe to Validate Model and Mapping Files</span></span>
<span data-ttu-id="2d78c-103">Bu konu nasıl kullanılacağını gösterir [EDM Oluşturucu (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) model ve eşleme dosyalarını doğrulama aracı.</span><span class="sxs-lookup"><span data-stu-id="2d78c-103">This topic shows how to use the [EDM Generator (EdmGen.exe)](../../../../../docs/framework/data/adonet/ef/edm-generator-edmgen-exe.md) tool to validate the model and mapping files.</span></span> <span data-ttu-id="2d78c-104">Daha fazla bilgi için [varlık veri modeli](../../../../../docs/framework/data/adonet/entity-data-model.md).</span><span class="sxs-lookup"><span data-stu-id="2d78c-104">For more information, see [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).</span></span>  
  
### <a name="to-validate-the-school-model-using-edmgenexe"></a><span data-ttu-id="2d78c-105">Okul modeli EdmGen.exe kullanarak doğrulamak için</span><span class="sxs-lookup"><span data-stu-id="2d78c-105">To validate the School model using EdmGen.exe</span></span>  
  
1.  <span data-ttu-id="2d78c-106">School veritabanını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2d78c-106">Create the School database.</span></span> <span data-ttu-id="2d78c-107">Daha fazla bilgi için [School örnek veritabanını oluşturma](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span><span class="sxs-lookup"><span data-stu-id="2d78c-107">For more information, see [Creating the School Sample Database](https://msdn.microsoft.com/library/c1bec483-a0ea-4660-aa0b-7b0a8b68fed0).</span></span>  
  
2.  <span data-ttu-id="2d78c-108">Okul modeli oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d78c-108">Generate the School model.</span></span> <span data-ttu-id="2d78c-109">Daha fazla bilgi için [nasıl yapılır: kullanımı Model ve eşleme dosyalarını üretmek için Edmgen.exe'yi](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span><span class="sxs-lookup"><span data-stu-id="2d78c-109">For more information, see [How to: Use EdmGen.exe to Generate the Model and Mapping Files](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-the-model-and-mapping-files.md).</span></span>  
  
3.  <span data-ttu-id="2d78c-110">Komut isteminde satır sonları olmadan aşağıdaki komutu yürütün:</span><span class="sxs-lookup"><span data-stu-id="2d78c-110">At the command prompt, execute the following command without line breaks:</span></span>  
  
    ```console
    "%windir%\Microsoft.NET\Framework\v4.0.30319\edmgen.exe" /mode:ValidateArtifacts /inssdl:.\School.ssdl /inmsl:.\School.msl /incsdl:.\School.csdl  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="2d78c-111">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="2d78c-111">See Also</span></span>  
 [<span data-ttu-id="2d78c-112">Nasıl yapılır: el ile bir Entity Framework projesinin yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2d78c-112">How to: Manually Configure an Entity Framework Project</span></span>](https://msdn.microsoft.com/library/73f6ae1d-b3b2-4577-aebd-ad5a75954e9e)  
 [<span data-ttu-id="2d78c-113">ADO.NET varlık veri modeli araçları</span><span class="sxs-lookup"><span data-stu-id="2d78c-113">ADO.NET Entity Data Model  Tools</span></span>](https://msdn.microsoft.com/library/91076853-0881-421b-837a-f582f36be527)  
 [<span data-ttu-id="2d78c-114">Nasıl yapılır: sorgu performansını artırmak için görünümleri önceden oluştur</span><span class="sxs-lookup"><span data-stu-id="2d78c-114">How to: Pre-Generate Views to Improve Query Performance</span></span>](https://msdn.microsoft.com/library/b18a9d16-e10b-4043-ba91-b632f85a2579)  
 [<span data-ttu-id="2d78c-115">Nasıl yapılır: EdmGen.exe kullanarak Nesne Katmanı Kodu Oluşturma</span><span class="sxs-lookup"><span data-stu-id="2d78c-115">How to: Use EdmGen.exe to Generate Object-Layer Code</span></span>](../../../../../docs/framework/data/adonet/ef/how-to-use-edmgen-exe-to-generate-object-layer-code.md)
