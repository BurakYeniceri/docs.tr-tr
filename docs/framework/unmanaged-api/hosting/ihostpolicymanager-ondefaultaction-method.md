---
title: "IHostPolicyManager::OnDefaultAction Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostPolicyManager.OnDefaultAction
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostPolicyManager::OnDefaultAction
helpviewer_keywords:
- OnDefaultAction method [.NET Framework hosting]
- IHostPolicyManager::OnDefaultAction method [.NET Framework hosting]
ms.assetid: 071e73bd-4795-470f-9373-cfaef553b7f2
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ca5eb767c08733980c9156d04526594c62349624
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ihostpolicymanagerondefaultaction-method"></a><span data-ttu-id="26d86-102">IHostPolicyManager::OnDefaultAction Yöntemi</span><span class="sxs-lookup"><span data-stu-id="26d86-102">IHostPolicyManager::OnDefaultAction Method</span></span>
<span data-ttu-id="26d86-103">Ortak dil çalışma zamanı (CLR) için yapılan bir çağrı tarafından ayarlanan varsayılan eylem gerçekleştirmek üzere olan konak bildirir [Iclrpolicymanager::setdefaultaction](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md) yanıt olarak bir iş parçacığı iptal yöntemi veya <xref:System.AppDomain> kaldırın.</span><span class="sxs-lookup"><span data-stu-id="26d86-103">Notifies the host that the common language runtime (CLR) is about to take the default action that was set by a call to the [ICLRPolicyManager::SetDefaultAction](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setdefaultaction-method.md) method in response to a thread abort or <xref:System.AppDomain> unload.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="26d86-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="26d86-104">Syntax</span></span>  
  
```  
HRESULT OnDefaultAction (  
    [in] EClrOperation  operation,   
    [in] EPolicyAction  action  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="26d86-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="26d86-105">Parameters</span></span>  
 `operation`  
 <span data-ttu-id="26d86-106">[in] Aşağıdakilerden birini [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) CLR yanıt olay türünü belirten değer.</span><span class="sxs-lookup"><span data-stu-id="26d86-106">[in] One of the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) values, indicating the kind of event to which the CLR is responding.</span></span>  
  
 `action`  
 <span data-ttu-id="26d86-107">[in] Aşağıdakilerden birini [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) CLR olaya yanıt olarak alma eylemini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="26d86-107">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the action that the CLR is taking in response to the event.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="26d86-108">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="26d86-108">Return Value</span></span>  
  
|<span data-ttu-id="26d86-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="26d86-109">HRESULT</span></span>|<span data-ttu-id="26d86-110">Açıklama</span><span class="sxs-lookup"><span data-stu-id="26d86-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="26d86-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="26d86-111">S_OK</span></span>|<span data-ttu-id="26d86-112">`OnDefaultAction`başarıyla döndürüldü.</span><span class="sxs-lookup"><span data-stu-id="26d86-112">`OnDefaultAction` returned successfully.</span></span>|  
|<span data-ttu-id="26d86-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="26d86-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="26d86-114">CLR süreç içine yüklü değil veya CLR içinde yönetilen kod çalıştıramaz veya çağrısı bir durumda.</span><span class="sxs-lookup"><span data-stu-id="26d86-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call.</span></span> <span data-ttu-id="26d86-115">başarıyla</span><span class="sxs-lookup"><span data-stu-id="26d86-115">successfully</span></span>|  
|<span data-ttu-id="26d86-116">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="26d86-116">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="26d86-117">Arama zaman aşımına uğradı.</span><span class="sxs-lookup"><span data-stu-id="26d86-117">The call timed out.</span></span>|  
|<span data-ttu-id="26d86-118">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="26d86-118">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="26d86-119">Arayan kilidi kendisine ait değil.</span><span class="sxs-lookup"><span data-stu-id="26d86-119">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="26d86-120">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="26d86-120">HOST_E_ABANDONED</span></span>|<span data-ttu-id="26d86-121">Bir olay engellenmiş iş parçacığı sırasında iptal edildi veya fiber üzerinde beklediği.</span><span class="sxs-lookup"><span data-stu-id="26d86-121">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="26d86-122">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="26d86-122">E_FAIL</span></span>|<span data-ttu-id="26d86-123">Bilinmeyen yıkıcı bir hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="26d86-123">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="26d86-124">Bir yöntem E_FAIL döndüğünde, CLR artık işlemi içinde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="26d86-124">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="26d86-125">Yöntemleri barındırma sonraki çağrılar HOST_E_CLRNOTAVAILABLE döndürür.</span><span class="sxs-lookup"><span data-stu-id="26d86-125">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="26d86-126">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="26d86-126">Requirements</span></span>  
 <span data-ttu-id="26d86-127">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="26d86-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26d86-128">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="26d86-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="26d86-129">**Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="26d86-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="26d86-130">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26d86-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26d86-131">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="26d86-131">See Also</span></span>  
 [<span data-ttu-id="26d86-132">EClrOperation numaralandırması</span><span class="sxs-lookup"><span data-stu-id="26d86-132">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)  
 [<span data-ttu-id="26d86-133">EPolicyAction numaralandırması</span><span class="sxs-lookup"><span data-stu-id="26d86-133">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)  
 [<span data-ttu-id="26d86-134">Iclrpolicymanager arabirimi</span><span class="sxs-lookup"><span data-stu-id="26d86-134">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [<span data-ttu-id="26d86-135">Ihostpolicymanager arabirimi</span><span class="sxs-lookup"><span data-stu-id="26d86-135">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)
