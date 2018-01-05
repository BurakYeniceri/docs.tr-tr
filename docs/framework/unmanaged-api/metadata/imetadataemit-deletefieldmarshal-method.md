---
title: "IMetaDataEmit::DeleteFieldMarshal Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DeleteFieldMarshal
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: ce60aace95f4da8c021026cf9bfc6c195de5b05f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataemitdeletefieldmarshal-method"></a><span data-ttu-id="ad8f1-102">IMetaDataEmit::DeleteFieldMarshal Yöntemi</span><span class="sxs-lookup"><span data-stu-id="ad8f1-102">IMetaDataEmit::DeleteFieldMarshal Method</span></span>
<span data-ttu-id="ad8f1-103">Belirtilen belirteç tarafından başvurulan nesne için meta veri imzası hazırlama PInvoke bozar.</span><span class="sxs-lookup"><span data-stu-id="ad8f1-103">Destroys the PInvoke marshaling metadata signature for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad8f1-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ad8f1-104">Syntax</span></span>  
  
```  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad8f1-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="ad8f1-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="ad8f1-106">[in] Bir `mdFieldDef` veya `mdParamDef` alan veya parametre sıralama meta verileri imza silmek temsil eden belirteci.</span><span class="sxs-lookup"><span data-stu-id="ad8f1-106">[in] An `mdFieldDef` or `mdParamDef` token that represents the field or parameter for which to delete the marshaling metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad8f1-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="ad8f1-107">Requirements</span></span>  
 <span data-ttu-id="ad8f1-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ad8f1-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ad8f1-109">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="ad8f1-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ad8f1-110">**Kitaplığı:** MSCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="ad8f1-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ad8f1-111">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ad8f1-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad8f1-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ad8f1-112">See Also</span></span>  
 [<span data-ttu-id="ad8f1-113">IMetaDataEmit Arabirimi</span><span class="sxs-lookup"><span data-stu-id="ad8f1-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="ad8f1-114">IMetaDataEmit2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="ad8f1-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
