---
title: IMetaDataEmit::DeleteFieldMarshal Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DeleteFieldMarshal
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DeleteFieldMarshal
helpviewer_keywords:
- IMetaDataEmit::DeleteFieldMarshal method [.NET Framework metadata]
- DeleteFieldMarshal method [.NET Framework metadata]
ms.assetid: 7c75aef9-c742-4b33-a14b-56ff94b0f725
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: dc88baea130adbec3dd8e4065ac0eb14ece7b8ba
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444857"
---
# <a name="imetadataemitdeletefieldmarshal-method"></a><span data-ttu-id="08461-102">IMetaDataEmit::DeleteFieldMarshal Yöntemi</span><span class="sxs-lookup"><span data-stu-id="08461-102">IMetaDataEmit::DeleteFieldMarshal Method</span></span>
<span data-ttu-id="08461-103">Belirtilen belirteç tarafından başvurulan nesne için meta veri imzası hazırlama PInvoke bozar.</span><span class="sxs-lookup"><span data-stu-id="08461-103">Destroys the PInvoke marshaling metadata signature for the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="08461-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="08461-104">Syntax</span></span>  
  
```  
HRESULT DeleteFieldMarshal (  
    [in]  mdToken     tk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="08461-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="08461-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="08461-106">[in] Bir `mdFieldDef` veya `mdParamDef` alan veya parametre sıralama meta verileri imza silmek temsil eden belirteci.</span><span class="sxs-lookup"><span data-stu-id="08461-106">[in] An `mdFieldDef` or `mdParamDef` token that represents the field or parameter for which to delete the marshaling metadata signature.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="08461-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="08461-107">Requirements</span></span>  
 <span data-ttu-id="08461-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="08461-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="08461-109">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="08461-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="08461-110">**Kitaplığı:** MSCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="08461-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="08461-111">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="08461-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="08461-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="08461-112">See Also</span></span>  
 [<span data-ttu-id="08461-113">IMetaDataEmit Arabirimi</span><span class="sxs-lookup"><span data-stu-id="08461-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="08461-114">IMetaDataEmit2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="08461-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
