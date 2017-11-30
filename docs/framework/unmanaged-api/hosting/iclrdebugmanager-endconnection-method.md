---
title: "ICLRDebugManager::EndConnection Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDebugManager.EndConnection
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRDebugManager::EndConnection
helpviewer_keywords:
- ICLRDebugManager::EndConnection method [.NET Framework hosting]
- EndConnection method [.NET Framework hosting]
ms.assetid: 89dc7363-2f29-4eb2-8f23-fccdda6a76a6
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 114f2217d22fc270b03d271db4acc44f0edbcca8
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="iclrdebugmanagerendconnection-method"></a><span data-ttu-id="d3f34-102">ICLRDebugManager::EndConnection Yöntemi</span><span class="sxs-lookup"><span data-stu-id="d3f34-102">ICLRDebugManager::EndConnection Method</span></span>
<span data-ttu-id="d3f34-103">Görevlerin bir listesi ve bir tanımlayıcı ve bir kolay ad arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d3f34-103">Removes the association between a list of tasks and an identifier and a friendly name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3f34-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d3f34-104">Syntax</span></span>  
  
```  
HRESULT EndConnection (  
    [in] CONNID dwConnectionId  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d3f34-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="d3f34-105">Parameters</span></span>  
 `dwConnectionId`  
 <span data-ttu-id="d3f34-106">[in] Bağlantı ve ortak dil çalışma zamanı (CLR) görevler ilişkili listesi ana bilgisayara özgü tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d3f34-106">[in] The host-specific identifier for the connection and the associated list of common language runtime (CLR) tasks.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d3f34-107">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="d3f34-107">Return Value</span></span>  
  
|<span data-ttu-id="d3f34-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d3f34-108">HRESULT</span></span>|<span data-ttu-id="d3f34-109">Açıklama</span><span class="sxs-lookup"><span data-stu-id="d3f34-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d3f34-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3f34-110">S_OK</span></span>|<span data-ttu-id="d3f34-111">`EndConnection`başarıyla döndürüldü.</span><span class="sxs-lookup"><span data-stu-id="d3f34-111">`EndConnection` returned successfully.</span></span>|  
|<span data-ttu-id="d3f34-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d3f34-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d3f34-113">CLR süreç içine yüklü değil veya CLR içinde yönetilen kod çalıştıramaz veya çağrı başarılı bir şekilde işlemek bir durumda.</span><span class="sxs-lookup"><span data-stu-id="d3f34-113">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d3f34-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d3f34-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d3f34-115">Arama zaman aşımına uğradı.</span><span class="sxs-lookup"><span data-stu-id="d3f34-115">The call timed out.</span></span>|  
|<span data-ttu-id="d3f34-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d3f34-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d3f34-117">Arayan kilidi kendisine ait değil.</span><span class="sxs-lookup"><span data-stu-id="d3f34-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d3f34-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d3f34-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d3f34-119">Bir olay engellenmiş iş parçacığı sırasında iptal edildi veya fiber üzerinde beklediği.</span><span class="sxs-lookup"><span data-stu-id="d3f34-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d3f34-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d3f34-120">E_FAIL</span></span>|<span data-ttu-id="d3f34-121">Bilinmeyen yıkıcı bir hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="d3f34-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d3f34-122">CLR, artık bir yöntem E_FAIL döndükten sonra işlemi içinde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="d3f34-122">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d3f34-123">Yöntemleri barındırma sonraki çağrılar HOST_E_CLRNOTAVAILABLE döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3f34-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d3f34-124">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d3f34-124">E_INVALIDARG</span></span>|<span data-ttu-id="d3f34-125">[BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) kullanarak hiçbir zaman çağrıldı `dwConnectionId`, veya `dwConnectionId` sıfır oluştu.</span><span class="sxs-lookup"><span data-stu-id="d3f34-125">[BeginConnection](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md) was never called using `dwConnectionId`, or `dwConnectionId` was zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d3f34-126">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="d3f34-126">Remarks</span></span>  
 <span data-ttu-id="d3f34-127">[Iclrdebugmanager](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md) üç yöntem sunar `BeginConnection`, [SetConnectionTasks](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setconnectiontasks-method.md), ve `EndConnection`, görev listeleri tanımlayıcıları ve kolay adlar ile ilişkilendirme.</span><span class="sxs-lookup"><span data-stu-id="d3f34-127">[ICLRDebugManager](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md) provides three methods, `BeginConnection`, [SetConnectionTasks](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setconnectiontasks-method.md), and `EndConnection`, for associating task lists with identifiers and friendly names.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="d3f34-128">Bu üç yöntem, her bir dizi görevi için belirli bir sırayla çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d3f34-128">These three methods must be called in a specific order for each set of tasks.</span></span> <span data-ttu-id="d3f34-129">`BeginConnection`Yeni bir bağlantı kurmak için önce çağrılır.</span><span class="sxs-lookup"><span data-stu-id="d3f34-129">`BeginConnection` is called first to establish a new connection.</span></span> <span data-ttu-id="d3f34-130">`SetConnectionTasks`ardından bu bağlantı ile ilişkili görevleri kümesi sağlamak için çağrılır.</span><span class="sxs-lookup"><span data-stu-id="d3f34-130">`SetConnectionTasks` is called next to provide the set of tasks to be associated with that connection.</span></span> <span data-ttu-id="d3f34-131">`EndConnection`Görev listesi ve tanımlayıcısı ve kolay ad arasındaki ilişkiyi kaldırmak için son çağrılır. Ancak, çağrıları farklı bağlantılar için iç içe.</span><span class="sxs-lookup"><span data-stu-id="d3f34-131">`EndConnection` is called last to remove the association between the task list and the identifier and friendly name.However, calls for different connections can be nested.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d3f34-132">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="d3f34-132">Requirements</span></span>  
 <span data-ttu-id="d3f34-133">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3f34-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3f34-134">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d3f34-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d3f34-135">**Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="d3f34-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d3f34-136">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3f34-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3f34-137">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d3f34-137">See Also</span></span>  
 [<span data-ttu-id="d3f34-138">Iclrcontrol arabirimi</span><span class="sxs-lookup"><span data-stu-id="d3f34-138">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="d3f34-139">Iclrdebugmanager arabirimi</span><span class="sxs-lookup"><span data-stu-id="d3f34-139">ICLRDebugManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-interface.md)  
 [<span data-ttu-id="d3f34-140">BeginConnection yöntemi</span><span class="sxs-lookup"><span data-stu-id="d3f34-140">BeginConnection Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-beginconnection-method.md)  
 [<span data-ttu-id="d3f34-141">SetConnectionTasks yöntemi</span><span class="sxs-lookup"><span data-stu-id="d3f34-141">SetConnectionTasks Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrdebugmanager-setconnectiontasks-method.md)  
 [<span data-ttu-id="d3f34-142">Ihostcontrol arabirimi</span><span class="sxs-lookup"><span data-stu-id="d3f34-142">IHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostcontrol-interface.md)