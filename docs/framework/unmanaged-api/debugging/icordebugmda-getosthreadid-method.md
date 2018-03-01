---
title: ICorDebugMDA::GetOSThreadId Metodu
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
- ICorDebugMDA.GetOSThreadId
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetOSThreadId
helpviewer_keywords:
- ICorDebugMDA::GetOSThreadId method [.NET Framework debugging]
- GetOSThreadId method [.NET Framework debugging]
ms.assetid: 7ca7c364-ade4-4219-b434-9f6ae2359be6
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: baec0852e75593c8c3731b9b912d618bf83045c9
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugmdagetosthreadid-method"></a><span data-ttu-id="c445d-102">ICorDebugMDA::GetOSThreadId Metodu</span><span class="sxs-lookup"><span data-stu-id="c445d-102">ICorDebugMDA::GetOSThreadId Method</span></span>
<span data-ttu-id="c445d-103">Yönetilen hata ayıklama Yardımcısı (MDA) bağlı temsil ettiği işletim sistemi (OS) iş parçacığı tanımlayıcısını alır [Icordebugmda](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md) yürütüyor.</span><span class="sxs-lookup"><span data-stu-id="c445d-103">Gets the operating system (OS) thread identifier upon which the managed debugging assistant (MDA) represented by [ICorDebugMDA](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md) is executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c445d-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="c445d-104">Syntax</span></span>  
  
```  
HRESULT GetOSThreadId (  
    [out] DWORD    *pOsTid  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c445d-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="c445d-105">Parameters</span></span>  
 `pOsTid`  
 <span data-ttu-id="c445d-106">[out] İşletim sistemi iş parçacığı tanımlayıcısı için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="c445d-106">[out] A pointer to the OS thread identifier.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c445d-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="c445d-107">Remarks</span></span>  
 <span data-ttu-id="c445d-108">İşletim sistemi iş parçacığı bir Icordebugthread yerine bir MDA yerel iş parçacığı veya yönetilen kod henüz girilmemiş yönetilen bir iş parçacığı tetiklenir durumlar için izin vermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c445d-108">The OS thread is used instead of an ICorDebugThread to allow for situations in which an MDA is fired either on a native thread or on a managed thread that has not yet entered managed code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c445d-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="c445d-109">Requirements</span></span>  
 <span data-ttu-id="c445d-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c445d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c445d-111">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c445d-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c445d-112">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c445d-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c445d-113">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c445d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c445d-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c445d-114">See Also</span></span>  
 [<span data-ttu-id="c445d-115">ICorDebugMDA Arabirimi</span><span class="sxs-lookup"><span data-stu-id="c445d-115">ICorDebugMDA Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmda-interface.md)  
 [<span data-ttu-id="c445d-116">Yönetilen Hata Ayıklama Yardımcıları ile Hataları Tanılama</span><span class="sxs-lookup"><span data-stu-id="c445d-116">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
