---
title: "ECustomDumpFlavor Numaralandırması"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ECustomDumpFlavor
api_location: mscoree.dll
api_type: COM
f1_keywords: ECustomDumpFlavor
helpviewer_keywords: ECustomDumpFlavor enumeration [.NET Framework hosting]
ms.assetid: b39b3320-fac7-41f1-9a03-ab6fb0cd89c7
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2a7317a3a12acef2a16deebab9a1e1b10205ebf6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="ecustomdumpflavor-enumeration"></a><span data-ttu-id="67585-102">ECustomDumpFlavor Numaralandırması</span><span class="sxs-lookup"><span data-stu-id="67585-102">ECustomDumpFlavor Enumeration</span></span>
<span data-ttu-id="67585-103">Hata raporlama yapılırken bir öbek içinde bir özel alt dahil edilecek maddeleri dökümü belirtmek değerlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="67585-103">Contains values that indicate which items to include in a custom subset of a heap dump when reporting errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="67585-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="67585-104">Syntax</span></span>  
  
```  
typedef enum {  
    DUMP_FLAVOR_Mini            = 1,  
    DUMP_FLAVOR_NonHeapCLRState = 2  
} ECustomDumpFlavor;  
```  
  
## <a name="members"></a><span data-ttu-id="67585-105">Üyeler</span><span class="sxs-lookup"><span data-stu-id="67585-105">Members</span></span>  
  
|<span data-ttu-id="67585-106">Üye</span><span class="sxs-lookup"><span data-stu-id="67585-106">Member</span></span>|<span data-ttu-id="67585-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="67585-107">Description</span></span>|  
|------------|-----------------|  
|`DUMP_FLAVOR_Mini`|<span data-ttu-id="67585-108">Özel yığın dökümü ve bir mini döküm Başlat tarafından belirtilen ek verileri dahil belirtir [Customdumpıtem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) örnekleri aynı yönteme geçirilen.</span><span class="sxs-lookup"><span data-stu-id="67585-108">Specifies that the custom heap dump should start as a minidump and include extra data specified by any [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) instances passed to the same method.</span></span>|  
|`DUMP_FLAVOR_NonHeapCLRState`|<span data-ttu-id="67585-109">Özel yığın dökümü dinamik olarak ayrılmamış tüm çalışma zamanı durumu verileri toplamanız gereken belirtir.</span><span class="sxs-lookup"><span data-stu-id="67585-109">Specifies that the custom heap dump should gather all run-time state data that was not dynamically allocated.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="67585-110">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="67585-110">Remarks</span></span>  
 <span data-ttu-id="67585-111">Türünde bir parametre `ECustomDumpFlavor` geçirilir [Iclrerrorreportingmanager::begincustomdump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="67585-111">A parameter of type `ECustomDumpFlavor` is passed to the [ICLRErrorReportingManager::BeginCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="67585-112">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="67585-112">Requirements</span></span>  
 <span data-ttu-id="67585-113">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="67585-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="67585-114">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="67585-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="67585-115">**Kitaplığı:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="67585-115">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="67585-116">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="67585-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67585-117">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="67585-117">See Also</span></span>  
 [<span data-ttu-id="67585-118">Ecustomdumpıtemkind numaralandırması</span><span class="sxs-lookup"><span data-stu-id="67585-118">ECustomDumpItemKind Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpitemkind-enumeration.md)  
 [<span data-ttu-id="67585-119">Iclrerrorreportingmanager arabirimi</span><span class="sxs-lookup"><span data-stu-id="67585-119">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)  
 [<span data-ttu-id="67585-120">Barındırma numaralandırmaları</span><span class="sxs-lookup"><span data-stu-id="67585-120">Hosting Enumerations</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
