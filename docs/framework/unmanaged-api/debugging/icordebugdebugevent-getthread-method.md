---
title: ICorDebugDebugEvent::GetThread Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 4f2e9a2c-8369-4a07-a881-ad5422626353
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 13b950545c2c8c8b54d24b932351d80280e1dac0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugdebugeventgetthread-method"></a><span data-ttu-id="17283-102">ICorDebugDebugEvent::GetThread Metodu</span><span class="sxs-lookup"><span data-stu-id="17283-102">ICorDebugDebugEvent::GetThread Method</span></span>
<span data-ttu-id="17283-103">Olayın oluştuğu iş parçacığı alır.</span><span class="sxs-lookup"><span data-stu-id="17283-103">Gets the thread on which the event occurred.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="17283-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="17283-104">Syntax</span></span>  
  
```  
HRESULT GetThread(  
        [out]ICorDebugThread **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="17283-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="17283-105">Parameters</span></span>  
 <span data-ttu-id="17283-106">ppThread</span><span class="sxs-lookup"><span data-stu-id="17283-106">ppThread</span></span>  
 <span data-ttu-id="17283-107">[out] Bir işaretçi adresine Icordebugthread nesnenin olayın oluştuğu iş parçacığı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="17283-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread on which the event occurred.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="17283-108">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="17283-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="17283-109">Bu yöntem yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="17283-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="17283-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="17283-110">Requirements</span></span>  
 <span data-ttu-id="17283-111">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="17283-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="17283-112">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="17283-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="17283-113">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="17283-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="17283-114">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="17283-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="17283-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="17283-115">See Also</span></span>  
 [<span data-ttu-id="17283-116">Icordebugdebugevent arabirimi</span><span class="sxs-lookup"><span data-stu-id="17283-116">ICorDebugDebugEvent Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md)  
 [<span data-ttu-id="17283-117">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="17283-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
