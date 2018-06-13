---
title: ICorProfilerThreadEnum::GetCount Metodu
ms.date: 03/30/2017
api_name:
- ICorProfilerThreadEnum.GetCount
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerThreadEnum::GetCount
helpviewer_keywords:
- ICorProfilerThreadEnum::GetCount method [.NET Framework profiling]
- GetCount method, ICorProfilerThreadEnum interface [.NET Framework profiling]
ms.assetid: d6dbdc4a-6115-455d-a3f3-704a81d3646b
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 2b803c83b905df47b3957e07c0d64e7ce6f6d303
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33455484"
---
# <a name="icorprofilerthreadenumgetcount-method"></a><span data-ttu-id="e88c1-102">ICorProfilerThreadEnum::GetCount Metodu</span><span class="sxs-lookup"><span data-stu-id="e88c1-102">ICorProfilerThreadEnum::GetCount Method</span></span>
<span data-ttu-id="e88c1-103">Uygulama tarafından kullanılan iş parçacığı sayısını alır.</span><span class="sxs-lookup"><span data-stu-id="e88c1-103">Gets the number of threads that are used by the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e88c1-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e88c1-104">Syntax</span></span>  
  
```  
HRESULT GetCount (    [out] ULONG * pcelt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e88c1-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="e88c1-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="e88c1-106">[out] Uygulama tarafından kullanılan iş parçacıklarının sayısı.</span><span class="sxs-lookup"><span data-stu-id="e88c1-106">[out] The number of threads used by the application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e88c1-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e88c1-107">Requirements</span></span>  
 <span data-ttu-id="e88c1-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e88c1-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e88c1-109">**Başlık:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e88c1-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e88c1-110">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e88c1-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e88c1-111">**.NET framework sürümleri:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e88c1-111">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e88c1-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e88c1-112">See Also</span></span>  
 [<span data-ttu-id="e88c1-113">ICorProfilerThreadEnum Arabirimi</span><span class="sxs-lookup"><span data-stu-id="e88c1-113">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)  
 [<span data-ttu-id="e88c1-114">Profil Oluşturma Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="e88c1-114">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
