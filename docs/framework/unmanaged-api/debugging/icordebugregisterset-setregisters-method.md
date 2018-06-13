---
title: ICorDebugRegisterSet::SetRegisters Yöntemi
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.SetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::SetRegisters
helpviewer_keywords:
- SetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::SetRegisters method [.NET Framework debugging]
ms.assetid: ac6244b9-54ba-475f-b72a-abed6afc46ec
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d6f577302c9b75f3f6cbe3f7ca8d551c9186c397
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33420322"
---
# <a name="icordebugregistersetsetregisters-method"></a><span data-ttu-id="02866-102">ICorDebugRegisterSet::SetRegisters Yöntemi</span><span class="sxs-lookup"><span data-stu-id="02866-102">ICorDebugRegisterSet::SetRegisters Method</span></span>
<span data-ttu-id="02866-103">`SetRegisters` .NET Framework sürüm 2.0 uygulanmadı.</span><span class="sxs-lookup"><span data-stu-id="02866-103">`SetRegisters` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="02866-104">Bu yöntemi çağırmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="02866-104">Do not call this method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="02866-105">Üst düzey işlemleri gibi kullandığınız [Icordebugılframe::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) veya [Icordebugnativeframe::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md).</span><span class="sxs-lookup"><span data-stu-id="02866-105">Use the higher-level operations such as [ICorDebugILFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md) or [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="02866-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="02866-106">Syntax</span></span>  
  
```  
HRESULT SetRegisters (  
    [in] ULONG64   mask,  
    [in] ULONG32   regCount,  
    [in, size_is(regCount)] CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="02866-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="02866-107">Requirements</span></span>  
 <span data-ttu-id="02866-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="02866-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="02866-109">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="02866-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="02866-110">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="02866-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="02866-111">**.NET framework sürümleri:** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="02866-111">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02866-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="02866-112">See Also</span></span>  
 [<span data-ttu-id="02866-113">ICorDebugRegisterSet Arabirimi</span><span class="sxs-lookup"><span data-stu-id="02866-113">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)  
 [<span data-ttu-id="02866-114">ICorDebugRegisterSet2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="02866-114">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
