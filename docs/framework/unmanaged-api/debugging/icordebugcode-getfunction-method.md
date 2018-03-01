---
title: ICorDebugCode::GetFunction Metodu
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
- ICorDebugCode.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetFunction method [.NET Framework debugging]
ms.assetid: c568b737-fdb2-4816-accd-051f5ab760f1
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: d05d5d7172a43ebaa04155fb42c2711eaf1ac085
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugcodegetfunction-method"></a><span data-ttu-id="dab4f-102">ICorDebugCode::GetFunction Metodu</span><span class="sxs-lookup"><span data-stu-id="dab4f-102">ICorDebugCode::GetFunction Method</span></span>
<span data-ttu-id="dab4f-103">"Bu"Icordebugcode"ile ilişkili ICorDebugFunction" alır.</span><span class="sxs-lookup"><span data-stu-id="dab4f-103">Gets the "ICorDebugFunction" associated with this "ICorDebugCode".</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dab4f-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="dab4f-104">Syntax</span></span>  
  
```  
HRESULT GetFunction (  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dab4f-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="dab4f-105">Parameters</span></span>  
 `ppFunction`  
 <span data-ttu-id="dab4f-106">[out] İşlevin adresini gösteren bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="dab4f-106">[out] A pointer to the address of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dab4f-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="dab4f-107">Remarks</span></span>  
 <span data-ttu-id="dab4f-108">`ICorDebugCode`ve `ICorDebugFunction` bire bir ilişki korumak.</span><span class="sxs-lookup"><span data-stu-id="dab4f-108">`ICorDebugCode` and `ICorDebugFunction` maintain a one-to-one relationship.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dab4f-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="dab4f-109">Requirements</span></span>  
 <span data-ttu-id="dab4f-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dab4f-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dab4f-111">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="dab4f-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dab4f-112">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dab4f-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dab4f-113">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dab4f-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dab4f-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="dab4f-114">See Also</span></span>  
 
