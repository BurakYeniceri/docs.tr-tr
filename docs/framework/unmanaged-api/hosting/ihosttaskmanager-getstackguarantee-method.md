---
title: IHostTaskManager::GetStackGuarantee Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostTaskManager.GetStackGuarantee
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostTaskManager::GetStackGuarantee
helpviewer_keywords:
- GetStackGuarantee method [.NET Framework hosting]
- IHostTaskManager::GetStackGuarantee method [.NET Framework hosting]
ms.assetid: 8176d732-c25c-4520-811d-e3310f339947
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: a2e4829083715fad8d77c1b5a2c303a07d5684ac
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="ihosttaskmanagergetstackguarantee-method"></a><span data-ttu-id="5252d-102">IHostTaskManager::GetStackGuarantee Metodu</span><span class="sxs-lookup"><span data-stu-id="5252d-102">IHostTaskManager::GetStackGuarantee Method</span></span>
<span data-ttu-id="5252d-103">Yığın işlemi tamamlandıktan sonra kullanılabilir olması garanti yığın alanı, ancak bir işlemin kapanmadan önce miktarını alır.</span><span class="sxs-lookup"><span data-stu-id="5252d-103">Gets the amount of stack space that is guaranteed to be available after a stack operation completes, but before the closing of a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5252d-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="5252d-104">Syntax</span></span>  
  
```  
HRESULT GetStackGuarantee(  
    [out] ULONG *pGuarantee  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5252d-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="5252d-105">Parameters</span></span>  
 `pGuarantee`  
 <span data-ttu-id="5252d-106">[out] Kullanılabilir bayt sayısı için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="5252d-106">[out] A pointer to the number of bytes that are available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5252d-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="5252d-107">Requirements</span></span>  
 <span data-ttu-id="5252d-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5252d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5252d-109">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="5252d-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="5252d-110">**Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="5252d-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="5252d-111">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5252d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5252d-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5252d-112">See Also</span></span>  
 [<span data-ttu-id="5252d-113">IHostTaskManager Arabirimi</span><span class="sxs-lookup"><span data-stu-id="5252d-113">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
