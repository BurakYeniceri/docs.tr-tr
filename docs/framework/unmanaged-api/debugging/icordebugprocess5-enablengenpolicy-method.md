---
title: "ICorDebugProcess5::EnableNGENPolicy Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ICorDebugProcess5::EnableNGenPolicy
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess5::EnableNGENPolicy
helpviewer_keywords:
- ICorDebugProcess5::EnableNGENPolicy method [.NET Framework debugging]
- EnableNGENPolicy method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 3b8e15ca-3c72-4685-a937-da4c739cb9e9
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: dca0df7b0be643d53bb5b9a03bd3abbb186d69dd
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugprocess5enablengenpolicy-method"></a><span data-ttu-id="1ae4a-102">ICorDebugProcess5::EnableNGENPolicy Yöntemi</span><span class="sxs-lookup"><span data-stu-id="1ae4a-102">ICorDebugProcess5::EnableNGENPolicy Method</span></span>
<span data-ttu-id="1ae4a-103">Yönetilen hata ayıklayıcı altında çalışırken yerel görüntüler nasıl bir uygulamanın yüklediği belirleyen bir değer ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-103">Sets a value that determines how an application loads native images while running under a managed debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1ae4a-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="1ae4a-104">Syntax</span></span>  
  
```  
HRESULT EnableNGENPolicy(  
    [in] CorDebugNGENPolicy ePolicy  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1ae4a-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="1ae4a-105">Parameters</span></span>  
 `ePolicy`  
 <span data-ttu-id="1ae4a-106">[in] A [cordebugngenpolicy sabit](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md) nasıl yönetilen bir hata ayıklayıcı altında çalışırken yerel görüntüler bir uygulamanın yüklediği belirler sabiti.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-106">[in] A [CorDebugNGenPolicy](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md) constant that determines how an application loads native images while running under a managed debugger.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1ae4a-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="1ae4a-107">Remarks</span></span>  
 <span data-ttu-id="1ae4a-108">İlke başarılı bir şekilde ayarlanmışsa, yöntem `S_OK`.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-108">If the policy is set successfully, the method returns `S_OK`.</span></span> <span data-ttu-id="1ae4a-109">Varsa `ePolicy` tarafından tanımlanan Enum değerleri aralığı dışında [cordebugngenpolicy sabit](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md), yöntem döndürür `E_INVALIDARG` ve yöntem çağrısının etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-109">If `ePolicy` is outside the range of the enumerated values defined by [CorDebugNGenPolicy](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md), the method returns `E_INVALIDARG` and the method call has no effect.</span></span> <span data-ttu-id="1ae4a-110">Yerel Görüntü Oluşturucu (Ngen.exe) ilkesi güncelleştirilemiyor ise, yöntem `E_FAIL`.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-110">If the policy of the Native Image Generator (Ngen.exe) cannot be updated, the method returns `E_FAIL`.</span></span>  
  
 <span data-ttu-id="1ae4a-111">`ICorDebugProcess5::EnableNGenPolicy` Yöntemi, işlem kullanım ömrü süresince herhangi bir zamanda çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-111">The `ICorDebugProcess5::EnableNGenPolicy` method can be called at any time during the lifetime of the process.</span></span> <span data-ttu-id="1ae4a-112">İlke İlkesi ayarlandıktan sonra yüklü olan tüm modülleri için etkindir.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-112">The policy is in effect for any modules that are loaded after the policy is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1ae4a-113">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="1ae4a-113">Requirements</span></span>  
 <span data-ttu-id="1ae4a-114">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1ae4a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1ae4a-115">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1ae4a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1ae4a-116">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1ae4a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1ae4a-117">**.NET framework sürümleri:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1ae4a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1ae4a-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="1ae4a-118">See Also</span></span>  
 [<span data-ttu-id="1ae4a-119">ICorDebugProcess5 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="1ae4a-119">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)  
 [<span data-ttu-id="1ae4a-120">Hata Ayıklama Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="1ae4a-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="1ae4a-121">Hata Ayıklama</span><span class="sxs-lookup"><span data-stu-id="1ae4a-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
