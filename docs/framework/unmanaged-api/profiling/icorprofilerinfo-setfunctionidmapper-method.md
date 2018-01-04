---
title: "ICorProfilerInfo::SetFunctionIDMapper Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.SetFunctionIDMapper
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::SetFunctionIDMapper
helpviewer_keywords:
- ICorProfilerInfo::SetFunctionIDMapper method [.NET Framework profiling]
- SetFunctionIDMapper method [.NET Framework profiling]
ms.assetid: 1a6e5dae-d366-4497-9c02-7b5b1f43f9ec
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 11f89b8d6697a2abf5a2787f0f4f10436e0a0212
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilerinfosetfunctionidmapper-method"></a><span data-ttu-id="c3e44-102">ICorProfilerInfo::SetFunctionIDMapper Yöntemi</span><span class="sxs-lookup"><span data-stu-id="c3e44-102">ICorProfilerInfo::SetFunctionIDMapper Method</span></span>
<span data-ttu-id="c3e44-103">Eşlenecek adlı profil oluşturucu uygulanan işlevini belirten `FunctionID` değerleri profil oluşturucu için 's geçirilen alternatif değerler için giriş/çıkış kancaları işlev.</span><span class="sxs-lookup"><span data-stu-id="c3e44-103">Specifies the profiler-implemented function that will be called to map `FunctionID` values to alternative values, which are passed to the profiler's function entry/exit hooks.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3e44-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="c3e44-104">Syntax</span></span>  
  
```  
HRESULT SetFunctionIDMapper (  
    [in] FunctionIDMapper *pFunc);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c3e44-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="c3e44-105">Parameters</span></span>  
 `pFunc`  
 <span data-ttu-id="c3e44-106">[in] Bir işaretçi [Functionıdmapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) eşlemek için adlı uygulama `FunctionID` alternatif değerlerine değerleri.</span><span class="sxs-lookup"><span data-stu-id="c3e44-106">[in] A pointer to the [FunctionIDMapper](../../../../docs/framework/unmanaged-api/profiling/functionidmapper-function.md) implementation that will be called to map the `FunctionID` values to their alternative values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c3e44-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="c3e44-107">Remarks</span></span>  
 <span data-ttu-id="c3e44-108">Alternatifleri için `FunctionID` değerleri için Profil Oluşturucu'nın işlevi giriş/çıkış kancaları geçirilecektir ([FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md), [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md), ve [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)) tarafından belirtilen [Icorprofilerınfo2::setenterleavefunctionhooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="c3e44-108">The alternatives for the `FunctionID` values will be passed to the profiler's function entry/exit hooks ([FunctionEnter2](../../../../docs/framework/unmanaged-api/profiling/functionenter2-function.md), [FunctionLeave2](../../../../docs/framework/unmanaged-api/profiling/functionleave2-function.md), and [FunctionTailcall2](../../../../docs/framework/unmanaged-api/profiling/functiontailcall2-function.md)) that are specified by the [ICorProfilerInfo2::SetEnterLeaveFunctionHooks2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-setenterleavefunctionhooks2-method.md) method.</span></span>  
  
 <span data-ttu-id="c3e44-109">`FunctionIDMapper` Yalnızca bir kez ayarlanabilir ve onu ayarladığınız önerilir [Icorprofilercallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) geri çağırma.</span><span class="sxs-lookup"><span data-stu-id="c3e44-109">The `FunctionIDMapper` can be set only once and it is recommended that you set it in the [ICorProfilerCallback::Initialize](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-initialize-method.md) callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c3e44-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="c3e44-110">Requirements</span></span>  
 <span data-ttu-id="c3e44-111">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c3e44-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c3e44-112">**Başlık:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="c3e44-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="c3e44-113">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c3e44-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c3e44-114">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c3e44-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3e44-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c3e44-115">See Also</span></span>  
 [<span data-ttu-id="c3e44-116">ICorProfilerInfo Arabirimi</span><span class="sxs-lookup"><span data-stu-id="c3e44-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
