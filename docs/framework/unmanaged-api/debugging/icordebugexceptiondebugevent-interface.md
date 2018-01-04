---
title: ICorDebugExceptionDebugEvent Arabirimi
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: f9ba60d8-b54d-417e-bb3e-fde4b41ca44c
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 97bbd9374b8a3f938f42b8ddd001049a2e7a324c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugexceptiondebugevent-interface"></a><span data-ttu-id="39ccd-102">ICorDebugExceptionDebugEvent Arabirimi</span><span class="sxs-lookup"><span data-stu-id="39ccd-102">ICorDebugExceptionDebugEvent Interface</span></span>
<span data-ttu-id="39ccd-103">Genişletir [Icordebugdebugevent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) özel durum olayları desteklemek için arabirim.</span><span class="sxs-lookup"><span data-stu-id="39ccd-103">Extends the [ICorDebugDebugEvent](../../../../docs/framework/unmanaged-api/debugging/icordebugdebugevent-interface.md) interface to support exception events.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="39ccd-104">Yöntemler</span><span class="sxs-lookup"><span data-stu-id="39ccd-104">Methods</span></span>  
  
|<span data-ttu-id="39ccd-105">Yöntem</span><span class="sxs-lookup"><span data-stu-id="39ccd-105">Method</span></span>|<span data-ttu-id="39ccd-106">Açıklama</span><span class="sxs-lookup"><span data-stu-id="39ccd-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="39ccd-107">GetFlags Yöntemi</span><span class="sxs-lookup"><span data-stu-id="39ccd-107">GetFlags Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getflags-method.md)|<span data-ttu-id="39ccd-108">Bir özel durum olup olmadığını gösteren bayrağı alır geçirilebilir.</span><span class="sxs-lookup"><span data-stu-id="39ccd-108">Gets a flag that indicates whether the exception is can be intercepted.</span></span>|  
|[<span data-ttu-id="39ccd-109">GetNativeIP Yöntemi</span><span class="sxs-lookup"><span data-stu-id="39ccd-109">GetNativeIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getnativeip-method.md)|<span data-ttu-id="39ccd-110">Yerel arabirim işaretçisi için bu özel durum hata ayıklama olayı alır.</span><span class="sxs-lookup"><span data-stu-id="39ccd-110">Gets the native interface pointer for this exception debug event.</span></span>|  
|[<span data-ttu-id="39ccd-111">GetStackPointer Yöntemi</span><span class="sxs-lookup"><span data-stu-id="39ccd-111">GetStackPointer Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptiondebugevent-getstackpointer-method.md)|<span data-ttu-id="39ccd-112">Yığın işaretçisi için bu özel durum hata ayıklama olayı alır.</span><span class="sxs-lookup"><span data-stu-id="39ccd-112">Gets the stack pointer for this exception debug event.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="39ccd-113">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="39ccd-113">Remarks</span></span>  
 <span data-ttu-id="39ccd-114">`ICorDebugExceptionDebugEvent` Arabirimi, aşağıdaki olay türlerine göre uygulanır:</span><span class="sxs-lookup"><span data-stu-id="39ccd-114">The `ICorDebugExceptionDebugEvent` interface is implemented by the following event types:</span></span>  
  
-   [<span data-ttu-id="39ccd-115">MANAGED_EXCEPTION_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="39ccd-115">MANAGED_EXCEPTION_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="39ccd-116">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span><span class="sxs-lookup"><span data-stu-id="39ccd-116">MANAGED_EXCEPTION_USER_FIRST_CHANCE</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="39ccd-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span><span class="sxs-lookup"><span data-stu-id="39ccd-117">MANAGED_EXCEPTION_CATCH_HANDLER_FOUND</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
-   [<span data-ttu-id="39ccd-118">MANAGED_EXCEPTION_UNHANDLED</span><span class="sxs-lookup"><span data-stu-id="39ccd-118">MANAGED_EXCEPTION_UNHANDLED</span></span>](../../../../docs/framework/unmanaged-api/debugging/cordebugrecordformat-enumeration.md)  
  
> [!NOTE]
>  <span data-ttu-id="39ccd-119">Arabirimi yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="39ccd-119">The interface is available with .NET Native only.</span></span> <span data-ttu-id="39ccd-120">Çağrı girişimi `QueryInterface` bir arabirim işaretçisi almak için döndürür `E_NOINTERFACE` .NET yerel dışında Icordebug senaryoları için.</span><span class="sxs-lookup"><span data-stu-id="39ccd-120">Attempting to call `QueryInterface` to retrieve an interface pointer returns `E_NOINTERFACE` for ICorDebug scenarios outside of .NET Native.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="39ccd-121">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="39ccd-121">Requirements</span></span>  
 <span data-ttu-id="39ccd-122">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="39ccd-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="39ccd-123">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="39ccd-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="39ccd-124">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="39ccd-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="39ccd-125">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="39ccd-125">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="39ccd-126">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="39ccd-126">See Also</span></span>  
 [<span data-ttu-id="39ccd-127">Hata Ayıklama Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="39ccd-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="39ccd-128">Hata Ayıklama</span><span class="sxs-lookup"><span data-stu-id="39ccd-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
