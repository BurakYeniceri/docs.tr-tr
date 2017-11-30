---
title: "EClrFailure Numaralandırması"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: EClrFailure
api_location: mscoree.dll
api_type: COM
f1_keywords: EClrFailure
helpviewer_keywords: EClrFailure enumeration [.NET Framework hosting]
ms.assetid: 37b95cce-9bfb-4ecf-a00b-33dcba782c67
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 94358fd0626fa17f1fd6d3c365aff79f89dde467
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="eclrfailure-enumeration"></a><span data-ttu-id="9ff91-102">EClrFailure Numaralandırması</span><span class="sxs-lookup"><span data-stu-id="9ff91-102">EClrFailure Enumeration</span></span>
<span data-ttu-id="9ff91-103">Bir ana bilgisayar ilkesi eylemleri ayarlayabilirsiniz hataları açıklar.</span><span class="sxs-lookup"><span data-stu-id="9ff91-103">Describes the set of failures for which a host can set policy actions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ff91-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="9ff91-104">Syntax</span></span>  
  
```  
typedef enum {  
    FAIL_NonCriticalResource,  
    FAIL_CriticalResource,  
    FAIL_FatalRuntime,  
    FAIL_OrphanedLock  
    FAIL_StackOverflow  
    FAIL_AccessViolation  
    FAIL_CodeContract  
} EClrFailure;  
```  
  
## <a name="members"></a><span data-ttu-id="9ff91-105">Üyeler</span><span class="sxs-lookup"><span data-stu-id="9ff91-105">Members</span></span>  
  
|<span data-ttu-id="9ff91-106">Üye</span><span class="sxs-lookup"><span data-stu-id="9ff91-106">Member</span></span>|<span data-ttu-id="9ff91-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="9ff91-107">Description</span></span>|  
|------------|-----------------|  
|`FAIL_NonCriticalResource`|<span data-ttu-id="9ff91-108">Kod kritik olmayan bir bölgede bir kaynak (örneğin, bir iş parçacığı, bir bellek bloğu veya kilit) tahsis girişimi sırasında hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="9ff91-108">A failure occurred during an attempt to allocate a resource (such as a thread, a block of memory, or a lock) in a non-critical region of code.</span></span>|  
|`FAIL_CriticalResource`|<span data-ttu-id="9ff91-109">Kod kritik bir bölgede bir kaynak (örneğin, bir iş parçacığı, bir bellek bloğu veya kilit) tahsis girişimi sırasında hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="9ff91-109">A failure occurred during an attempt to allocate a resource (such as a thread, a block of memory, or a lock) in a critical region of code.</span></span>|  
|`FAIL_FatalRuntime`|<span data-ttu-id="9ff91-110">Ortak dil çalışma zamanı (CLR) artık işleminde yönetilen kod çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="9ff91-110">The common language runtime (CLR) is no longer able to run managed code in the process.</span></span> <span data-ttu-id="9ff91-111">Henceforth, barındırma hiçbir işlev çağrıları HOST_E_CLRNOTAVAILABLE HRESULT değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9ff91-111">Henceforth, calls to any hosting functions return an HRESULT value of HOST_E_CLRNOTAVAILABLE.</span></span>|  
|`FAIL_OrphanedLock`|<span data-ttu-id="9ff91-112">Bir iş parçacığı döndürme bağlı bir kilidi serbest bırakmak başarısız oldu bir <xref:System.AppDomain> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9ff91-112">A thread has failed to release a lock upon returning from an <xref:System.AppDomain> object.</span></span> <span data-ttu-id="9ff91-113">Ana bilgisayar iptal etmek bir iş parçacığı neden bu hatanın ayarlanamıyor.</span><span class="sxs-lookup"><span data-stu-id="9ff91-113">The host cannot set this failure to cause a thread to abort.</span></span>|  
|`FAIL_StackOverflow`|<span data-ttu-id="9ff91-114">Bir yığın taşması oluştu.</span><span class="sxs-lookup"><span data-stu-id="9ff91-114">A stack overflow has occurred.</span></span>|  
|`FAIL_AccessViolation`|<span data-ttu-id="9ff91-115">Okuma veya yazma korumalı bellek için girişimde bulunuldu.</span><span class="sxs-lookup"><span data-stu-id="9ff91-115">An attempt was made to read or write protected memory.</span></span> <span data-ttu-id="9ff91-116">İçinde desteklenmez [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9ff91-116">Not supported in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>|  
|`FAIL_CodeContract`|<span data-ttu-id="9ff91-117">Kodu sözleşme hatası oluştu.</span><span class="sxs-lookup"><span data-stu-id="9ff91-117">A code contract failure occurred.</span></span> <span data-ttu-id="9ff91-118">Bkz: [kod sözleşmeleri](../../../../docs/framework/debug-trace-profile/code-contracts.md).</span><span class="sxs-lookup"><span data-stu-id="9ff91-118">See [Code Contracts](../../../../docs/framework/debug-trace-profile/code-contracts.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ff91-119">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="9ff91-119">Remarks</span></span>  
 <span data-ttu-id="9ff91-120">Bkz: [Iclrpolicymanager::setactiononfailure](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md) yöntemi listesini görmek için [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) değerleri konak hata koşulları için ilke eylemleri belirtmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9ff91-120">See the [ICLRPolicyManager::SetActionOnFailure](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md) method for a list of [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values the host can use to specify the policy actions for failure conditions.</span></span> <span data-ttu-id="9ff91-121">Kod kritik ve kritik olmayan bölgeleri hakkında daha fazla bilgi için bkz: [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="9ff91-121">For more information about critical and non-critical regions of code, see [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ff91-122">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="9ff91-122">Requirements</span></span>  
 <span data-ttu-id="9ff91-123">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9ff91-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ff91-124">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="9ff91-124">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9ff91-125">**Kitaplığı:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9ff91-125">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9ff91-126">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ff91-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ff91-127">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="9ff91-127">See Also</span></span>  
 [<span data-ttu-id="9ff91-128">Iclrpolicymanager arabirimi</span><span class="sxs-lookup"><span data-stu-id="9ff91-128">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [<span data-ttu-id="9ff91-129">SetActionOnFailure yöntemi</span><span class="sxs-lookup"><span data-stu-id="9ff91-129">SetActionOnFailure Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactiononfailure-method.md)  
 [<span data-ttu-id="9ff91-130">Ihostpolicymanager arabirimi</span><span class="sxs-lookup"><span data-stu-id="9ff91-130">IHostPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostpolicymanager-interface.md)  
 [<span data-ttu-id="9ff91-131">Barındırma numaralandırmaları</span><span class="sxs-lookup"><span data-stu-id="9ff91-131">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)