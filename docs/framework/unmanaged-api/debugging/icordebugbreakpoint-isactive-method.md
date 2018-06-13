---
title: ICorDebugBreakpoint::IsActive Yöntemi
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::IsActive
helpviewer_keywords:
- ICorDebugBreakpoint::IsActive method [.NET Framework debugging]
- IsActive method, ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: 06e583d6-d88a-4ff5-bb95-5c48618a461c
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 61aece9dd506d6e4af8718e45cc772d120a7d579
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401667"
---
# <a name="icordebugbreakpointisactive-method"></a><span data-ttu-id="81b25-102">ICorDebugBreakpoint::IsActive Yöntemi</span><span class="sxs-lookup"><span data-stu-id="81b25-102">ICorDebugBreakpoint::IsActive Method</span></span>
<span data-ttu-id="81b25-103">Gösteren bir değer alır olup olmadığını bu `ICorDebugBreakpoint` etkindir.</span><span class="sxs-lookup"><span data-stu-id="81b25-103">Gets a value that indicates whether this `ICorDebugBreakpoint` is active.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81b25-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="81b25-104">Syntax</span></span>  
  
```  
HRESULT IsActive (  
    [out] BOOL *pbActive  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="81b25-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="81b25-105">Parameters</span></span>  
 `pbActive`  
 <span data-ttu-id="81b25-106">[out] `true` bu kesme noktası yoksa etkin, aksi takdirde `false`.</span><span class="sxs-lookup"><span data-stu-id="81b25-106">[out] `true` if this breakpoint is active; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81b25-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="81b25-107">Requirements</span></span>  
 <span data-ttu-id="81b25-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="81b25-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81b25-109">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="81b25-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="81b25-110">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="81b25-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="81b25-111">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81b25-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
