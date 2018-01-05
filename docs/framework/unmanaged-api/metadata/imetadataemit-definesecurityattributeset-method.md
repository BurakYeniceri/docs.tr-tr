---
title: "IMetaDataEmit::DefineSecurityAttributeSet Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DefineSecurityAttributeSet
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DefineSecurityAttributeSet
helpviewer_keywords:
- IMetaDataEmit::DefineSecurityAttributeSet method [.NET Framework metadata]
- DefineSecurityAttributeSet method [.NET Framework metadata]
ms.assetid: 27064ca2-4186-4433-90a7-3b297785e891
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4863ee416bba7fe66326c1d11ec3aa0037d022a1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataemitdefinesecurityattributeset-method"></a><span data-ttu-id="dec94-102">IMetaDataEmit::DefineSecurityAttributeSet Yöntemi</span><span class="sxs-lookup"><span data-stu-id="dec94-102">IMetaDataEmit::DefineSecurityAttributeSet Method</span></span>
<span data-ttu-id="dec94-103">Belirtilen belirteç tarafından başvurulan nesne eklemek için güvenlik izinleri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dec94-103">Creates a set of security permissions to attach to the object referenced by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dec94-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="dec94-104">Syntax</span></span>  
  
```  
HRESULT DefineSecurityAttributeSet (   
    [in]  mdToken       tkObj,   
    [in]  COR_SECATTR   rSecAttrs[],   
    [in]  ULONG         cSecAttrs,   
    [out] ULONG         *pulErrorAttr   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dec94-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="dec94-105">Parameters</span></span>  
 `tkObj`  
 <span data-ttu-id="dec94-106">[in] Güvenlik bilgileri iliştirildiği belirteci.</span><span class="sxs-lookup"><span data-stu-id="dec94-106">[in] The token to which the security information is attached.</span></span>  
  
 `rSecAttrs`  
 <span data-ttu-id="dec94-107">[in] Bir dizi `COR_SECATTR` yapıları.</span><span class="sxs-lookup"><span data-stu-id="dec94-107">[in] An array of `COR_SECATTR` structures.</span></span>  
  
 `cSecAttrs`  
 <span data-ttu-id="dec94-108">[in] Öğe sayısı `rSecAttrs`.</span><span class="sxs-lookup"><span data-stu-id="dec94-108">[in] The number of elements in `rSecAttrs`.</span></span>  
  
 `pulErrorAttr`  
 <span data-ttu-id="dec94-109">[out] Yöntem başarısız olursa, dizinde belirtir `rSecAttrs` soruna neden öğesi.</span><span class="sxs-lookup"><span data-stu-id="dec94-109">[out] If the method fails, specifies the index in `rSecAttrs` of the element that caused the problem.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dec94-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="dec94-110">Requirements</span></span>  
 <span data-ttu-id="dec94-111">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dec94-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dec94-112">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="dec94-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dec94-113">**Kitaplığı:** MSCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="dec94-113">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="dec94-114">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dec94-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dec94-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="dec94-115">See Also</span></span>  
 [<span data-ttu-id="dec94-116">IMetaDataEmit Arabirimi</span><span class="sxs-lookup"><span data-stu-id="dec94-116">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="dec94-117">IMetaDataEmit2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="dec94-117">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
