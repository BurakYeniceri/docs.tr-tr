---
title: "IMetaDataEmit::DefineTypeRefByName Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IMetaDataEmit.DefineTypeRefByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineTypeRefByName
helpviewer_keywords:
- DefineTypeRefByName method [.NET Framework metadata]
- IMetaDataEmit::DefineTypeRefByName method [.NET Framework metadata]
ms.assetid: c30a4ce3-2d3e-411a-98df-e62ac4a5dd50
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 46b9fe83a5beb031d4ac21deb903060e2f788e1a
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataemitdefinetyperefbyname-method"></a><span data-ttu-id="4e55b-102">IMetaDataEmit::DefineTypeRefByName Yöntemi</span><span class="sxs-lookup"><span data-stu-id="4e55b-102">IMetaDataEmit::DefineTypeRefByName Method</span></span>
<span data-ttu-id="4e55b-103">Bir meta veri geçerli kapsamı dışında belirtilen kapsamda tanımlanan bir tür için belirteç alır.</span><span class="sxs-lookup"><span data-stu-id="4e55b-103">Gets a metadata token for a type that is defined in the specified scope, which is outside the current scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e55b-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="4e55b-104">Syntax</span></span>  
  
```  
HRESULT DefineTypeRefByName (   
    [in]  mdToken     tkResolutionScope,   
    [in]  LPCWSTR     szName,   
    [out] mdTypeRef   *ptr   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4e55b-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="4e55b-105">Parameters</span></span>  
 `tkResolutionScope`  
 <span data-ttu-id="4e55b-106">[in] Çözümleme kapsamı belirleme belirteci.</span><span class="sxs-lookup"><span data-stu-id="4e55b-106">[in] The token specifying the resolution scope.</span></span> <span data-ttu-id="4e55b-107">Aşağıdaki belirteç türlerini geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="4e55b-107">The following token types are valid:</span></span>  
  
-   <span data-ttu-id="4e55b-108">`mdModuleRef`, türü arayanın tanımlanır aynı bütünleştirilmiş kodda tanımlanmış olması durumunda.</span><span class="sxs-lookup"><span data-stu-id="4e55b-108">`mdModuleRef`, if the type is defined in the same assembly in which the caller is defined.</span></span>  
  
-   <span data-ttu-id="4e55b-109">`mdAssemblyRef`, türü arayanın tanımlanır farklı bir derlemede tanımlanmış olması durumunda.</span><span class="sxs-lookup"><span data-stu-id="4e55b-109">`mdAssemblyRef`, if the type is defined in an assembly other than the one in which the caller is defined.</span></span>  
  
-   <span data-ttu-id="4e55b-110">`mdTypeRef`, tür iç içe geçmiş tür ise.</span><span class="sxs-lookup"><span data-stu-id="4e55b-110">`mdTypeRef`, if the type is a nested type.</span></span>  
  
-   <span data-ttu-id="4e55b-111">`mdModule`, türü arayanın tanımlanır modülünde tanımlanmış olması durumunda.</span><span class="sxs-lookup"><span data-stu-id="4e55b-111">`mdModule`, if the type is defined in the same module in which the caller is defined.</span></span>  
  
-   <span data-ttu-id="4e55b-112">Tür genel olarak tanımlanmışsa null.</span><span class="sxs-lookup"><span data-stu-id="4e55b-112">Null, if the type is defined globally.</span></span>  
  
 `szName`  
 <span data-ttu-id="4e55b-113">[in] Unicode hedef türünün adı.</span><span class="sxs-lookup"><span data-stu-id="4e55b-113">[in] The name of the target type in Unicode.</span></span>  
  
 `ptr`  
 <span data-ttu-id="4e55b-114">[out] Bir işaretçi `mdTypeRef` türüne atanan belirteci.</span><span class="sxs-lookup"><span data-stu-id="4e55b-114">[out] A pointer to the `mdTypeRef` token that is assigned to the type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e55b-115">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="4e55b-115">Requirements</span></span>  
 <span data-ttu-id="4e55b-116">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e55b-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e55b-117">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="4e55b-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="4e55b-118">**Kitaplığı:** MSCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="4e55b-118">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4e55b-119">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e55b-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e55b-120">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4e55b-120">See Also</span></span>  
 [<span data-ttu-id="4e55b-121">IMetaDataEmit Arabirimi</span><span class="sxs-lookup"><span data-stu-id="4e55b-121">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="4e55b-122">IMetaDataEmit2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="4e55b-122">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
