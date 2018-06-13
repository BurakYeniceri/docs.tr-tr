---
title: ICorProfilerCallback::ClassUnloadFinished Yöntemi
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassUnloadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassUnloadFinished
helpviewer_keywords:
- ICorProfilerCallback::ClassUnloadFinished method [.NET Framework profiling]
- ClassUnloadFinished method [.NET Framework profiling]
ms.assetid: 55674b68-678a-4747-ae06-4e91519c7305
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: ebf72fe4f9fae5b3d791e6eed2e9421b9f4e3296
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450823"
---
# <a name="icorprofilercallbackclassunloadfinished-method"></a><span data-ttu-id="e8a91-102">ICorProfilerCallback::ClassUnloadFinished Yöntemi</span><span class="sxs-lookup"><span data-stu-id="e8a91-102">ICorProfilerCallback::ClassUnloadFinished Method</span></span>
<span data-ttu-id="e8a91-103">Profil Oluşturucu bir sınıf kaldırılması tamamlandığını bildirir.</span><span class="sxs-lookup"><span data-stu-id="e8a91-103">Notifies the profiler that a class has finished unloading.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8a91-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e8a91-104">Syntax</span></span>  
  
```  
HRESULT ClassUnloadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8a91-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="e8a91-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="e8a91-106">[in] Kaldırıldı sınıfı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e8a91-106">[in] Identifies the class that was unloaded.</span></span>  
  
 `hrStatus`  
 <span data-ttu-id="e8a91-107">[in] Sınıf başarıyla kaldırıldı olup olmadığını gösteren bir HRESULT.</span><span class="sxs-lookup"><span data-stu-id="e8a91-107">[in] An HRESULT that indicates whether the class was unloaded successfully.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e8a91-108">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="e8a91-108">Remarks</span></span>  
 <span data-ttu-id="e8a91-109">Sınıf kaldırılması, bazı bölümleri sonra devam edebilir `ClassUnloadFinished` geri çağırma.</span><span class="sxs-lookup"><span data-stu-id="e8a91-109">Some parts of unloading the class might continue after the `ClassUnloadFinished` callback.</span></span> <span data-ttu-id="e8a91-110">HRESULT hata içinde `hrStatus` hata gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8a91-110">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="e8a91-111">Ancak, bir başarı HRESULT içinde `hrStatus` yalnızca ilk sınıfı kaldırılması parçası başarılı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8a91-111">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the class has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8a91-112">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e8a91-112">Requirements</span></span>  
 <span data-ttu-id="e8a91-113">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8a91-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8a91-114">**Başlık:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e8a91-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e8a91-115">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8a91-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8a91-116">**.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8a91-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8a91-117">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e8a91-117">See Also</span></span>  
 [<span data-ttu-id="e8a91-118">ICorProfilerCallback Arabirimi</span><span class="sxs-lookup"><span data-stu-id="e8a91-118">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="e8a91-119">ClassUnloadStarted Yöntemi</span><span class="sxs-lookup"><span data-stu-id="e8a91-119">ClassUnloadStarted Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classunloadstarted-method.md)
