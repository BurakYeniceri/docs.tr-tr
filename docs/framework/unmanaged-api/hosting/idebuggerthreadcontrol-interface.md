---
title: IDebuggerThreadControl Arabirimi
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IDebuggerThreadControl
helpviewer_keywords:
- IDebuggerThreadControl interface [.NET Framework hosting]
ms.assetid: 0a270c42-a7d1-45f1-a64d-fa3e84d14532
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 619a28d2382aa9cc3130a3130c07fa1e283119e4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437921"
---
# <a name="idebuggerthreadcontrol-interface"></a><span data-ttu-id="136cc-102">IDebuggerThreadControl Arabirimi</span><span class="sxs-lookup"><span data-stu-id="136cc-102">IDebuggerThreadControl Interface</span></span>
<span data-ttu-id="136cc-103">Engelleme hakkında konak bildirme ve hata ayıklama Hizmetleri tarafından iş parçacıklarının kaldırma için yöntemleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="136cc-103">Provides methods for notifying the host about the blocking and unblocking of threads by the debugging services.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="136cc-104">Yöntemler</span><span class="sxs-lookup"><span data-stu-id="136cc-104">Methods</span></span>  
  
|<span data-ttu-id="136cc-105">Yöntem</span><span class="sxs-lookup"><span data-stu-id="136cc-105">Method</span></span>|<span data-ttu-id="136cc-106">Açıklama</span><span class="sxs-lookup"><span data-stu-id="136cc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="136cc-107">ThreadIsBlockingForDebugger Yöntemi</span><span class="sxs-lookup"><span data-stu-id="136cc-107">ThreadIsBlockingForDebugger Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-threadisblockingfordebugger-method.md)|<span data-ttu-id="136cc-108">Bu geri çağırma gönderme iş parçacığı hakkındadır konak bildirir hata ayıklama Hizmetleri blokta için.</span><span class="sxs-lookup"><span data-stu-id="136cc-108">Notifies the host that the thread that is sending this callback is about to block within the debugging services.</span></span>|  
|[<span data-ttu-id="136cc-109">ReleaseAllRuntimeThreads Yöntemi</span><span class="sxs-lookup"><span data-stu-id="136cc-109">ReleaseAllRuntimeThreads Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-releaseallruntimethreads-method.md)|<span data-ttu-id="136cc-110">Ana bilgisayar hata ayıklama hizmetleri hakkında engellenmiş durumda olan tüm iş parçacıklarının yayın olduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="136cc-110">Notifies the host that the debugging services are about to release all threads that are blocked.</span></span>|  
|[<span data-ttu-id="136cc-111">StartBlockingForDebugger Yöntemi</span><span class="sxs-lookup"><span data-stu-id="136cc-111">StartBlockingForDebugger Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-startblockingfordebugger-method.md)|<span data-ttu-id="136cc-112">Ana bilgisayar hata ayıklama hizmetleri hakkında tüm iş parçacıklarının engelleme başlangıç olduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="136cc-112">Notifies the host that the debugging services are about to start blocking all threads.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="136cc-113">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="136cc-113">Requirements</span></span>  
 <span data-ttu-id="136cc-114">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="136cc-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="136cc-115">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="136cc-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="136cc-116">**Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="136cc-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="136cc-117">**.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="136cc-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="136cc-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="136cc-118">See Also</span></span>  
 [<span data-ttu-id="136cc-119">Barındırma Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="136cc-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
