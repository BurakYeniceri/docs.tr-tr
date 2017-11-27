---
title: ICorDebugILCode::GetEHClauses Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: ICorDebugILCode.GetEHClauses
api_location: mscordbi.dll
api_type: COM
ms.assetid: cf7a0e00-06ae-47a5-8037-598b26196802
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 39d30ef572423d8cb988c074971de095f1709e8c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugilcodegetehclauses-method"></a><span data-ttu-id="cc2ad-102">ICorDebugILCode::GetEHClauses Metodu</span><span class="sxs-lookup"><span data-stu-id="cc2ad-102">ICorDebugILCode::GetEHClauses Method</span></span>
<span data-ttu-id="cc2ad-103">[.NET Framework 4.5.2 ve sonraki sürümlerinde desteklenen]</span><span class="sxs-lookup"><span data-stu-id="cc2ad-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="cc2ad-104">Özel durum işleme bu Ara dile (IL) tanımlanır (EH) yan tümceleri listesine bir işaretçi döndürür.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-104">Returns a pointer to a list of exception handling (EH) clauses that are defined for this intermediate language (IL).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc2ad-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="cc2ad-105">Syntax</span></span>  
  
```cpp
HRESULT GetEHClauses(  
   [in] ULONG32 cClauses,  
   [out] ULONG32 * pcClauses,  
   [out, size_is(cClauses), length_is(*pcClauses)] CorDebugEHClause clauses[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="cc2ad-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="cc2ad-106">Parameters</span></span>  
 `cClauses`  
 <span data-ttu-id="cc2ad-107">[in] Depolama kapasitesini `clauses` dizi.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-107">[in] The storage capacity of the `clauses` array.</span></span> <span data-ttu-id="cc2ad-108">Daha fazla bilgi için Açıklamalar bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-108">See the Remarks section for more information.</span></span>  
  
 `pcClauses`  
 <span data-ttu-id="cc2ad-109">[out] Hakkında bilgi yazılır yan tümceleri sayısı `clauses` dizi.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-109">[out] The number of clauses about which information is written to the `clauses` array.</span></span>  
  
 <span data-ttu-id="cc2ad-110">yan tümceleri</span><span class="sxs-lookup"><span data-stu-id="cc2ad-110">clauses</span></span>  
 <span data-ttu-id="cc2ad-111">[out] Bir dizi [CorDebugEHClause](../../../../docs/framework/unmanaged-api/debugging/cordebugehclause-structure.md) özel durum yan tümceleri bu IL için tanımlanan işleme hakkında bilgi içeren nesne.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-111">[out] An array of [CorDebugEHClause](../../../../docs/framework/unmanaged-api/debugging/cordebugehclause-structure.md) objects that contain information on exception handling clauses defined for this IL.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc2ad-112">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="cc2ad-112">Remarks</span></span>  
 <span data-ttu-id="cc2ad-113">Varsa `cClauses` 0'dır ve `pcClauses` olan olmayan**null**, `pcClauses` kullanılabilir özel durum yan tümceleri işleme sayısını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-113">If `cClauses` is 0 and `pcClauses` is non-**null**, `pcClauses` is set to the number of available exception handling clauses.</span></span> <span data-ttu-id="cc2ad-114">Varsa `cClauses` sıfır, değil depolama kapasitesini temsil `clauses` dizi.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-114">If `cClauses` is non-zero, it represents the storage capacity of the `clauses` array.</span></span> <span data-ttu-id="cc2ad-115">Yöntem döndüğünde `clauses` en fazla içeren `cClauses` öğeleri ve `pcClauses` gerçekte yazılan yan tümceleri sayısına ayarlayın `clauses` dizi.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-115">When the method returns, `clauses` contains a maximum of `cClauses` items, and `pcClauses` is set to the number of clauses actually written to the `clauses` array.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cc2ad-116">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="cc2ad-116">Requirements</span></span>  
 <span data-ttu-id="cc2ad-117">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cc2ad-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc2ad-118">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cc2ad-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cc2ad-119">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cc2ad-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cc2ad-120">**.NET framework sürümleri:**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc2ad-120">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc2ad-121">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="cc2ad-121">See Also</span></span>  
 [<span data-ttu-id="cc2ad-122">Icordebugılcode arabirimi</span><span class="sxs-lookup"><span data-stu-id="cc2ad-122">ICorDebugILCode Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md)  
 [<span data-ttu-id="cc2ad-123">CorDebugEHClause yapısı</span><span class="sxs-lookup"><span data-stu-id="cc2ad-123">CorDebugEHClause Structure</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugehclause-structure.md)  
 [<span data-ttu-id="cc2ad-124">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="cc2ad-124">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
