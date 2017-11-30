---
title: ICorDebugFunction3::GetActiveReJitRequestILCode Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: ICorDebugFunction3.GetActiveReJitRequestILCode
api_location: mscordbi.dll
api_type: COM
ms.assetid: 88584574-ade5-45b2-9778-489ed5c4dd7f
topic_type: apiref
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6459297a2a04728ca87801bfc8484acec384a45c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugfunction3getactiverejitrequestilcode-method"></a><span data-ttu-id="0fd8a-102">ICorDebugFunction3::GetActiveReJitRequestILCode Metodu</span><span class="sxs-lookup"><span data-stu-id="0fd8a-102">ICorDebugFunction3::GetActiveReJitRequestILCode Method</span></span>
<span data-ttu-id="0fd8a-103">[.NET Framework 4.5.2 ve sonraki sürümlerinde desteklenen]</span><span class="sxs-lookup"><span data-stu-id="0fd8a-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="0fd8a-104">Bir arabirim işaretçisi alır bir [Icordebugılcode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) etkin bir ReJIT istek IL içerir.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-104">Gets an interface pointer to an [ICorDebugILCode](../../../../docs/framework/unmanaged-api/debugging/icordebugilcode-interface.md) that contains the IL from an active ReJIT request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fd8a-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0fd8a-105">Syntax</span></span>  
  
```cpp
HRESULT GetActiveReJitRequestILCode(  
   ICorDebugILCode **ppReJitedILCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0fd8a-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="0fd8a-106">Parameters</span></span>  
 `ppReJitedILCode`  
 <span data-ttu-id="0fd8a-107">IL için bir işaretçi bir etkin ReJIT istek.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-107">A pointer to the IL from an active ReJIT request.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0fd8a-108">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="0fd8a-108">Remarks</span></span>  
 <span data-ttu-id="0fd8a-109">Yöntemi bu tarafından temsil edilen varsa `ICorDebugFunction3` nesne sahip etkin bir ReJIT isteği `ppReJitedILCode` kendi IL bir işaretçi döndürür.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-109">If the method represented by this `ICorDebugFunction3` object has an active ReJIT request, `ppReJitedILCode` returns a pointer to its IL.</span></span> <span data-ttu-id="0fd8a-110">Ortak bir durumda ise hiçbir etkin isteği olup olmadığını `ppReJitedILCode` olan **null**.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-110">If there is no active request, which is a common case, then `ppReJitedILCode` is **null**.</span></span>  
  
 <span data-ttu-id="0fd8a-111">Yürütme yalnızca döndürür sonra ReJIT isteği etkin hale [Icorprofilercallback4::getrejıtparameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) yöntem çağrısı.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-111">A ReJIT request becomes active just after execution returns from the [ICorProfilerCallback4::GetReJITParameters](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback4-getrejitparameters-method.md) method call.</span></span> <span data-ttu-id="0fd8a-112">Bu henüz JIT derlenmiş olmayabilir ve iş parçacığı hala kodu özgün sürümünde yürütme.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-112">It may not yet be JIT-compiled, and threads may still be executing in the original version of the code.</span></span> <span data-ttu-id="0fd8a-113">Profil Oluşturucu'nın arama sırasında ReJIT isteği devre dışı olduğu [Icorprofilerınfo4::requestrevert](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-requestrevert-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-113">A ReJIT request becomes inactive during the profiler's call to the [ICorProfilerInfo4::RequestRevert](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo4-requestrevert-method.md) method.</span></span> <span data-ttu-id="0fd8a-114">IL bile dönüştürüldükten sonra bir iş parçacığı JIT yeniden derlenmesi (ReJIT) kodda hala yürütülüyor.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-114">Even after the IL is reverted, a thread can still be executing in the JIT-recompiled (ReJIT) code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fd8a-115">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="0fd8a-115">Requirements</span></span>  
 <span data-ttu-id="0fd8a-116">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0fd8a-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0fd8a-117">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0fd8a-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0fd8a-118">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0fd8a-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0fd8a-119">**.NET framework sürümleri:**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0fd8a-119">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fd8a-120">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="0fd8a-120">See Also</span></span>  
 [<span data-ttu-id="0fd8a-121">Icordebugfunction3 arabirimi</span><span class="sxs-lookup"><span data-stu-id="0fd8a-121">ICorDebugFunction3 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugfunction3-interface.md)  
 [<span data-ttu-id="0fd8a-122">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="0fd8a-122">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="0fd8a-123">ReJIT: Nasıl yapılır Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="0fd8a-123">ReJIT: A How-To Guide</span></span>](http://blogs.msdn.com/b/davbr/archive/2011/10/12/rejit-a-how-to-guide.aspx)