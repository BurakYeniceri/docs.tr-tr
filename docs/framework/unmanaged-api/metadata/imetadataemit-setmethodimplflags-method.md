---
title: IMetaDataEmit::SetMethodImplFlags Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetMethodImplFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetMethodImplFlags
helpviewer_keywords:
- IMetaDataEmit::SetMethodImplFlags method [.NET Framework metadata]
- SetMethodImpFlags method [.NET Framework metadata]
ms.assetid: 4bc82d9b-9544-4be3-ba51-a2d4d806158a
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 71881fe8c4b883bb91468033a3c17c8d77c35f3c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33445428"
---
# <a name="imetadataemitsetmethodimplflags-method"></a><span data-ttu-id="d7c4d-102">IMetaDataEmit::SetMethodImplFlags Yöntemi</span><span class="sxs-lookup"><span data-stu-id="d7c4d-102">IMetaDataEmit::SetMethodImplFlags Method</span></span>
<span data-ttu-id="d7c4d-103">Belirtilen belirteç tarafından başvurulan devralınan yöntemi uygulama meta verileri imzası güncelleştirir veya ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d7c4d-103">Sets or updates the metadata signature of the inherited method implementation that is referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d7c4d-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d7c4d-104">Syntax</span></span>  
  
```  
HRESULT SetMethodImplFlags (   
    [in]  mdMethodDef   md,   
    [in]  DWORD         dwImplFlags   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d7c4d-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="d7c4d-105">Parameters</span></span>  
 `md`  
 <span data-ttu-id="d7c4d-106">[in] Değiştirilecek yöntemi için belirteci.</span><span class="sxs-lookup"><span data-stu-id="d7c4d-106">[in] The token for the method to be changed.</span></span>  
  
 `dwImplFlags`  
 <span data-ttu-id="d7c4d-107">[in] Değerleri bir birleşimini [Cormethodımpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) yöntemi uygulama özellikleri belirtir numaralandırması.</span><span class="sxs-lookup"><span data-stu-id="d7c4d-107">[in] A combination of the values of the [CorMethodImpl](../../../../docs/framework/unmanaged-api/metadata/cormethodimpl-enumeration.md) enumeration that specifies the method implementation features.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d7c4d-108">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="d7c4d-108">Requirements</span></span>  
 <span data-ttu-id="d7c4d-109">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d7c4d-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d7c4d-110">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d7c4d-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d7c4d-111">**Kitaplığı:** MSCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="d7c4d-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d7c4d-112">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d7c4d-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7c4d-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d7c4d-113">See Also</span></span>  
 [<span data-ttu-id="d7c4d-114">IMetaDataEmit Arabirimi</span><span class="sxs-lookup"><span data-stu-id="d7c4d-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="d7c4d-115">IMetaDataEmit2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="d7c4d-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
