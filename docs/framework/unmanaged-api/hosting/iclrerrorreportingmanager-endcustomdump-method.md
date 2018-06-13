---
title: ICLRErrorReportingManager::EndCustomDump Yöntemi
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.EndCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::EndCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::EndCustomDump method [.NET Framework hosting]
- EndCustomDump method [.NET Framework hosting]
ms.assetid: 88a5da04-8729-4108-82c4-af206a7d483e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2e5e5a594743c5770d4b9f93d4b0949cce24592a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435725"
---
# <a name="iclrerrorreportingmanagerendcustomdump-method"></a><span data-ttu-id="34173-102">ICLRErrorReportingManager::EndCustomDump Yöntemi</span><span class="sxs-lookup"><span data-stu-id="34173-102">ICLRErrorReportingManager::EndCustomDump Method</span></span>
<span data-ttu-id="34173-103">Önceki bir çağrıda belirtilen özel yığın dökümü yapılandırmasını kaldırır [Iclrerrorreportingmanager::begincustomdump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="34173-103">Removes the custom stack dump configuration that was specified in an earlier call to the [ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34173-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="34173-104">Syntax</span></span>  
  
```  
HRESULT EndCustomDump ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="34173-105">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="34173-105">Return Value</span></span>  
  
|<span data-ttu-id="34173-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="34173-106">HRESULT</span></span>|<span data-ttu-id="34173-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="34173-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="34173-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="34173-108">S_OK</span></span>|<span data-ttu-id="34173-109">`EndCustomDump` başarıyla döndürüldü.</span><span class="sxs-lookup"><span data-stu-id="34173-109">`EndCustomDump` returned successfully.</span></span>|  
|<span data-ttu-id="34173-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="34173-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="34173-111">Ortak dil çalışma zamanı (CLR) süreç içine yüklü değil veya CLR içinde yönetilen kod çalıştıramaz veya çağrı başarılı bir şekilde işlemek bir durumda.</span><span class="sxs-lookup"><span data-stu-id="34173-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="34173-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="34173-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="34173-113">Arama zaman aşımına uğradı.</span><span class="sxs-lookup"><span data-stu-id="34173-113">The call timed out.</span></span>|  
|<span data-ttu-id="34173-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="34173-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="34173-115">Arayan kilidi kendisine ait değil.</span><span class="sxs-lookup"><span data-stu-id="34173-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="34173-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="34173-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="34173-117">Bir olay engellenmiş iş parçacığı sırasında iptal edildi veya fiber üzerinde beklediği.</span><span class="sxs-lookup"><span data-stu-id="34173-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="34173-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="34173-118">E_FAIL</span></span>|<span data-ttu-id="34173-119">Bilinmeyen yıkıcı bir hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="34173-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="34173-120">CLR, artık bir yöntem E_FAIL döndükten sonra işlemi içinde kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="34173-120">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="34173-121">Yöntemleri barındırma sonraki çağrılar HOST_E_CLRNOTAVAILABLE döndürür.</span><span class="sxs-lookup"><span data-stu-id="34173-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="34173-122">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="34173-122">Remarks</span></span>  
 <span data-ttu-id="34173-123">`EndCustomDump` Yöntemini temizler özel yığın dökümü yapılandırması için önceki bir çağrı tarafından ayarlanmış `BeginCustomDump` yöntemi ve herhangi bir ilişkili durum boşaltır.</span><span class="sxs-lookup"><span data-stu-id="34173-123">The `EndCustomDump` method clears the custom stack dump configuration set by an earlier call to the `BeginCustomDump` method and frees any associated state.</span></span> <span data-ttu-id="34173-124">Özel yığın dökümü tamamlandıktan sonra çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="34173-124">It should be called after the custom stack dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="34173-125">Çağrılacak hatası `EndCustomDump` bellek sızıntısı neden olur.</span><span class="sxs-lookup"><span data-stu-id="34173-125">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34173-126">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="34173-126">Requirements</span></span>  
 <span data-ttu-id="34173-127">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="34173-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34173-128">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="34173-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="34173-129">**Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="34173-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="34173-130">**.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34173-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34173-131">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="34173-131">See Also</span></span>  
 [<span data-ttu-id="34173-132">CustomDumpItem Yapısı</span><span class="sxs-lookup"><span data-stu-id="34173-132">CustomDumpItem Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md)  
 [<span data-ttu-id="34173-133">ECustomDumpFlavor Sabit Listesi</span><span class="sxs-lookup"><span data-stu-id="34173-133">ECustomDumpFlavor Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md)  
 [<span data-ttu-id="34173-134">ICLRErrorReportingManager Arabirimi</span><span class="sxs-lookup"><span data-stu-id="34173-134">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
