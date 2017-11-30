---
title: COR_PRF_CODEGEN_FLAGS Sabit Listesi
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_CODEGEN_FLAGS
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_CODEGEN_FLAGS
helpviewer_keywords: COR_PRF_CODEGEN_FLAGS enumeration [.NET Framework profiling]
ms.assetid: 3e184022-0247-4824-a23d-6b29593d8d01
topic_type: apiref
caps.latest.revision: "6"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c2c97510077fefd730827ac00326d267fd1c62ef
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="corprfcodegenflags-enumeration"></a><span data-ttu-id="3c19c-102">COR_PRF_CODEGEN_FLAGS Sabit Listesi</span><span class="sxs-lookup"><span data-stu-id="3c19c-102">COR_PRF_CODEGEN_FLAGS Enumeration</span></span>
<span data-ttu-id="3c19c-103">İle ayarlayabilirsiniz kod oluşturma bayrakları tanımlar [Icorprofilerfunctioncontrol::setcodegenflags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="3c19c-103">Defines the code generation flags that can be set with the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c19c-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3c19c-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_CODEGEN_DISABLE_INLINING =          0x0001,  
    COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS = 0x0002,  
} COR_PRF_CODEGEN_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="3c19c-105">Üyeler</span><span class="sxs-lookup"><span data-stu-id="3c19c-105">Members</span></span>  
  
|<span data-ttu-id="3c19c-106">Üye</span><span class="sxs-lookup"><span data-stu-id="3c19c-106">Member</span></span>|<span data-ttu-id="3c19c-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="3c19c-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_CODEGEN_DISABLE_INLINING`|<span data-ttu-id="3c19c-108">Hiçbir işlevler bu işlevin gövdesi içermesinden olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3c19c-108">No functions will be inlined into this function’s body.</span></span> <span data-ttu-id="3c19c-109">Ancak, işlevi kendi arayanlar içermesinden olabilir.</span><span class="sxs-lookup"><span data-stu-id="3c19c-109">However, the function itself may be inlined into its callers.</span></span>|  
|`COR_PRF_CODEGEN_DISABLE_ALL_OPTIMIZATIONS`|<span data-ttu-id="3c19c-110">Tüm iyileştirmeler bu işlevin gövdesi için devre dışı bırakılacak.</span><span class="sxs-lookup"><span data-stu-id="3c19c-110">All optimizations will be disabled for this function’s body.</span></span> <span data-ttu-id="3c19c-111">Ancak, işlevi hala kendi arayanlar içermesinden olabilir.</span><span class="sxs-lookup"><span data-stu-id="3c19c-111">However, the function itself may still be inlined into its callers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3c19c-112">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="3c19c-112">Remarks</span></span>  
 <span data-ttu-id="3c19c-113">`COR_PRF_CODEGEN_FLAGS` Numaralandırması tarafından kullanılan [Icorprofilerfunctioncontrol::setcodegenflags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) JIT yeniden derlenmesi işlevi için kod oluşturmanın denetlemek profil oluşturucu etkinleştirmek için yöntemi.</span><span class="sxs-lookup"><span data-stu-id="3c19c-113">The `COR_PRF_CODEGEN_FLAGS` enumeration is used by the [ICorProfilerFunctionControl::SetCodegenFlags](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctioncontrol-setcodegenflags-method.md) method to enable the profiler to control the code generation for the JIT-recompiled function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c19c-114">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="3c19c-114">Requirements</span></span>  
 <span data-ttu-id="3c19c-115">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3c19c-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c19c-116">**Başlık:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3c19c-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3c19c-117">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c19c-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c19c-118">**.NET framework sürümleri:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c19c-118">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c19c-119">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="3c19c-119">See Also</span></span>  
 [<span data-ttu-id="3c19c-120">Profil oluşturma numaralandırmaları</span><span class="sxs-lookup"><span data-stu-id="3c19c-120">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)