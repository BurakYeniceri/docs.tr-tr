---
title: ICorDebugStepperEnum::Next Yöntemi
ms.date: 03/30/2017
api_name:
- ICorDebugStepperEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepperEnum::Next
helpviewer_keywords:
- Next method, ICorDebugStepperEnum interface [.NET Framework debugging]
- ICorDebugStepperEnum::Next method [.NET Framework debugging]
ms.assetid: d0ea0f30-e8d2-48b0-8477-e1a029ceb4dd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8bd62e4c5476aacf736f2ddfea008790861d931c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33419623"
---
# <a name="icordebugstepperenumnext-method"></a><span data-ttu-id="a3217-102">ICorDebugStepperEnum::Next Yöntemi</span><span class="sxs-lookup"><span data-stu-id="a3217-102">ICorDebugStepperEnum::Next Method</span></span>
<span data-ttu-id="a3217-103">ICorDebugStepper örnekleri belirtilen sayıda geçerli konumdan başlayarak numaralandırması alır.</span><span class="sxs-lookup"><span data-stu-id="a3217-103">Gets the specified number of ICorDebugStepper instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a3217-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a3217-104">Syntax</span></span>  
  
```  
HRESULT Next(  
    [in] ULONG  celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugStepper *steppers[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a3217-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="a3217-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="a3217-106">[in] Sayısı `ICorDebugStepper` alınacak örnekleri.</span><span class="sxs-lookup"><span data-stu-id="a3217-106">[in] The number of `ICorDebugStepper` instances to be retrieved.</span></span>  
  
 `steppers`  
 <span data-ttu-id="a3217-107">[out] Her biri işaret işaretçileri, bir dizi bir `ICorDebugStepper` nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a3217-107">[out] An array of pointers, each of which points to an `ICorDebugStepper` object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="a3217-108">[out] İşaretçi sayısına `ICorDebugStepper` gerçekte döndürülen örnek.</span><span class="sxs-lookup"><span data-stu-id="a3217-108">[out] Pointer to the number of `ICorDebugStepper` instances actually returned.</span></span> <span data-ttu-id="a3217-109">Bu değer null ise `celt` biridir.</span><span class="sxs-lookup"><span data-stu-id="a3217-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a3217-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="a3217-110">Requirements</span></span>  
 <span data-ttu-id="a3217-111">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a3217-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3217-112">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a3217-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a3217-113">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a3217-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a3217-114">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a3217-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
