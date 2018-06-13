---
title: ICorDebugCode::GetAddress Metodu
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetAddress
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetAddress
helpviewer_keywords:
- GetAddress method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetAddress method [.NET Framework debugging]
ms.assetid: cc507cb0-df2e-49c2-b32e-0c3271a8df9a
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: e2de22729fd3d7a511c1105ebf810d0402bd73a9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402089"
---
# <a name="icordebugcodegetaddress-method"></a><span data-ttu-id="6a5a5-102">ICorDebugCode::GetAddress Metodu</span><span class="sxs-lookup"><span data-stu-id="6a5a5-102">ICorDebugCode::GetAddress Method</span></span>
<span data-ttu-id="6a5a5-103">Bu "ICorDebugCode" arabirimi temsil eden kod kesimi göreli sanal adres (RAV) alır.</span><span class="sxs-lookup"><span data-stu-id="6a5a5-103">Gets the relative virtual address (RVA) of the code segment that this "ICorDebugCode" interface represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6a5a5-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="6a5a5-104">Syntax</span></span>  
  
```  
HRESULT GetAddress (  
    [out] CORDB_ADDRESS *pStart  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6a5a5-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="6a5a5-105">Parameters</span></span>  
 `pStart`  
 <span data-ttu-id="6a5a5-106">[out] Kod kesimi RVA gösteren bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="6a5a5-106">[out] A pointer to the RVA of the code segment.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6a5a5-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="6a5a5-107">Requirements</span></span>  
 <span data-ttu-id="6a5a5-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="6a5a5-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6a5a5-109">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6a5a5-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6a5a5-110">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6a5a5-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6a5a5-111">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6a5a5-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6a5a5-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="6a5a5-112">See Also</span></span>  
 
