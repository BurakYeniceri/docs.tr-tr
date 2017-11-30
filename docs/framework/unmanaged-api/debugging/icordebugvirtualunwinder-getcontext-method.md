---
title: "ICorDebugVirtualUnwinder::GetContext yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: fe502a76-3068-47e5-a0a0-85ccb72dfac3
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 45a914005e84d33b39d72fce96679e275b921d3c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvirtualunwindergetcontext-method"></a><span data-ttu-id="e331b-102">ICorDebugVirtualUnwinder::GetContext yöntemi</span><span class="sxs-lookup"><span data-stu-id="e331b-102">ICorDebugVirtualUnwinder::GetContext Method</span></span>
<span data-ttu-id="e331b-103">Bu unwinder geçerli bağlamını alır.</span><span class="sxs-lookup"><span data-stu-id="e331b-103">Gets the current context of this unwinder.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e331b-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e331b-104">Syntax</span></span>  
  
```  
HRESULT GetContext(  
   [in] ULONG32 contextFlags,  
   [in] ULONG32 cbContextBuf,  
   [out] ULONG32* contextSize,  
   [out, size_is(cbContextBuf)] BYTE contextBuf[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e331b-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="e331b-105">Parameters</span></span>  
 `contextFlags`  
 <span data-ttu-id="e331b-106">[in] Hangi kısımlarının (WinNT.h içinde tanımlanan) dönmek için bağlamı belirtmek bayraklar.</span><span class="sxs-lookup"><span data-stu-id="e331b-106">[in] Flags that specify which parts of the context to return (defined in WinNT.h).</span></span>  
  
 `cbContextBuf`  
 <span data-ttu-id="e331b-107">[in] Bayt sayısı `contextBuf`.</span><span class="sxs-lookup"><span data-stu-id="e331b-107">[in] The number of bytes in `contextBuf`.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="e331b-108">[out] Gerçekte yazılan bayt sayısı için bir işaretçi `contextBuf`.</span><span class="sxs-lookup"><span data-stu-id="e331b-108">[out] A pointer to the number of bytes actually written to `contextBuf`.</span></span>  
  
 `contextBuf`  
 <span data-ttu-id="e331b-109">[out] Bu unwinder geçerli içeriği içeren bir bayt dizisi.</span><span class="sxs-lookup"><span data-stu-id="e331b-109">[out] A byte array that contains the current context of this unwinder.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e331b-110">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="e331b-110">Return Value</span></span>  
 <span data-ttu-id="e331b-111">Tüm mscordbi tarafından alınan HRESULT değer başarısız önemli kabul edilir ve Icordebug dönmek API neden olacak `CORDBG_E_DATA_TARGET_ERROR`.</span><span class="sxs-lookup"><span data-stu-id="e331b-111">Any failing HRESULT value received by mscordbi is considered fatal and will cause ICorDebug APIs to return `CORDBG_E_DATA_TARGET_ERROR`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e331b-112">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="e331b-112">Remarks</span></span>  
 <span data-ttu-id="e331b-113">Başlangıç değerini ayarlamak `contextBuf` bağımsız değişkeni çağrılarak döndürülen bağlamı arabelleğinde [Icordebugstackwalk::getcontext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="e331b-113">You set the initial value of the `contextBuf` argument to the context buffer returned by calling the [ICorDebugStackWalk::GetContext](../../../../docs/framework/unmanaged-api/debugging/icordebugstackwalk-getcontext-method.md) method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e331b-114">Bu yöntem yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e331b-114">This method is available with .NET Native only.</span></span>  
  
 <span data-ttu-id="e331b-115">Unwinding may yalnızca geri yükleme bir alt yazmaçların geçici olmayan gibi yalnızca kaydeder olduğundan, bağlam tam kayıt durumu gerçek yöntem çağrısının aynı anda aynı olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="e331b-115">Because unwinding may only restore a subset of the registers, such as the non-volatile registers only, the context may not exactly match the register state at the time of the actual method call.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e331b-116">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e331b-116">Requirements</span></span>  
 <span data-ttu-id="e331b-117">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e331b-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e331b-118">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e331b-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e331b-119">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e331b-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e331b-120">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e331b-120">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e331b-121">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e331b-121">See Also</span></span>  
 [<span data-ttu-id="e331b-122">ICorDebugMemoryBuffer arabirimi</span><span class="sxs-lookup"><span data-stu-id="e331b-122">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)  
 [<span data-ttu-id="e331b-123">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="e331b-123">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)