---
title: "AssemblyOptions Numaralandırması"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: AssemblyOptions
api_location: alink.dll
api_type: COM
f1_keywords: AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ccbbcabd3fbb372322ca6334f6ab6db4fdafc2f1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="369c3-102">AssemblyOptions Numaralandırması</span><span class="sxs-lookup"><span data-stu-id="369c3-102">AssemblyOptions Enumeration</span></span>
<span data-ttu-id="369c3-103">Derleme seçenekleri numaralandırır.</span><span class="sxs-lookup"><span data-stu-id="369c3-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="369c3-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="369c3-104">Syntax</span></span>  
  
```  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="369c3-105">Alanlar</span><span class="sxs-lookup"><span data-stu-id="369c3-105">Fields</span></span>  
  
|<span data-ttu-id="369c3-106">Alan</span><span class="sxs-lookup"><span data-stu-id="369c3-106">Field</span></span>|<span data-ttu-id="369c3-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="369c3-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="369c3-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="369c3-108">optAssemTitle</span></span>|<span data-ttu-id="369c3-109">Dize - derleme başlığı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="369c3-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="369c3-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="369c3-110">optAssemDescription</span></span>|<span data-ttu-id="369c3-111">Dize - derleme açıklaması içerir.</span><span class="sxs-lookup"><span data-stu-id="369c3-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="369c3-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="369c3-112">optAssemConfig</span></span>|<span data-ttu-id="369c3-113">Dize - derleme yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="369c3-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="369c3-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="369c3-114">optAssemOS</span></span>|<span data-ttu-id="369c3-115">Olarak kodlanmış bir dize -: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span><span class="sxs-lookup"><span data-stu-id="369c3-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="369c3-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="369c3-116">optAssemProcessor</span></span>|<span data-ttu-id="369c3-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="369c3-117">ULONG</span></span>|  
|<span data-ttu-id="369c3-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="369c3-118">optAssemLocale</span></span>|<span data-ttu-id="369c3-119">Dize - derleme yerel içerir.</span><span class="sxs-lookup"><span data-stu-id="369c3-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="369c3-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="369c3-120">optAssemVersion</span></span>|<span data-ttu-id="369c3-121">Olarak kodlanmış bir dize -: "Major.Minor.Build.Revision".</span><span class="sxs-lookup"><span data-stu-id="369c3-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="369c3-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="369c3-122">optAssemCompany</span></span>|<span data-ttu-id="369c3-123">Dize - şirket içerir.</span><span class="sxs-lookup"><span data-stu-id="369c3-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="369c3-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="369c3-124">optAssemProduct</span></span>|<span data-ttu-id="369c3-125">Dize - ürün adı içeriyor.</span><span class="sxs-lookup"><span data-stu-id="369c3-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="369c3-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="369c3-126">optAssemProductVersion</span></span>|<span data-ttu-id="369c3-127">Dize (InformationalVersion olarak da bilinir).</span><span class="sxs-lookup"><span data-stu-id="369c3-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="369c3-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="369c3-128">optAssemCopyright</span></span>|<span data-ttu-id="369c3-129">Dize - telif hakkı bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="369c3-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="369c3-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="369c3-130">optAssemTrademark</span></span>|<span data-ttu-id="369c3-131">Dize - ticari marka bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="369c3-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="369c3-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="369c3-132">optAssemKeyFile</span></span>|<span data-ttu-id="369c3-133">String (dosya adı).</span><span class="sxs-lookup"><span data-stu-id="369c3-133">String (file name).</span></span>|  
|<span data-ttu-id="369c3-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="369c3-134">optAssemKeyName</span></span>|<span data-ttu-id="369c3-135">Dize (anahtar adı).</span><span class="sxs-lookup"><span data-stu-id="369c3-135">String (The key name).</span></span>|  
|<span data-ttu-id="369c3-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="369c3-136">optAssemAlgID</span></span>|<span data-ttu-id="369c3-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="369c3-137">ULONG</span></span>|  
|<span data-ttu-id="369c3-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="369c3-138">optAssemFlags</span></span>|<span data-ttu-id="369c3-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="369c3-139">ULONG</span></span>|  
|<span data-ttu-id="369c3-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="369c3-140">optAssemHalfSign</span></span>|<span data-ttu-id="369c3-141">Bool (DelaySign da bilinir).</span><span class="sxs-lookup"><span data-stu-id="369c3-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="369c3-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="369c3-142">optAssemFileVersion</span></span>|<span data-ttu-id="369c3-143">"Major.Minor.Build.Revision"--ProductVersion aynı olarak kodlanmış bir dize -.</span><span class="sxs-lookup"><span data-stu-id="369c3-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="369c3-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="369c3-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="369c3-145">"Major.Minor.Build.Revision" kodlanmış bir dize -.</span><span class="sxs-lookup"><span data-stu-id="369c3-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="369c3-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="369c3-146">optLastAssemOption</span></span>|<span data-ttu-id="369c3-147">Bir sayaç öğelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="369c3-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="369c3-148">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="369c3-148">Requirements</span></span>  
 <span data-ttu-id="369c3-149">**Başlık:** alink.h</span><span class="sxs-lookup"><span data-stu-id="369c3-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="369c3-150">**Kitaplık**: alink.dll</span><span class="sxs-lookup"><span data-stu-id="369c3-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="369c3-151">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="369c3-151">See Also</span></span>  
 [<span data-ttu-id="369c3-152">Al.exe (derleme bağlayıcı)</span><span class="sxs-lookup"><span data-stu-id="369c3-152">Al.exe (Assembly Linker)</span></span>](../../../../docs/framework/tools/al-exe-assembly-linker.md)