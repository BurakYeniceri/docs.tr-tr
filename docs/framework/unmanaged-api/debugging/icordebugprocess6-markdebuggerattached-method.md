---
title: "ICorDebugProcess6::MarkDebuggerAttached Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: bf94f090-5265-4112-8e57-5b4e20e070d0
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f6d219e298e04157ea0670681c7550bd920bd284
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugprocess6markdebuggerattached-method"></a><span data-ttu-id="62fc8-102">ICorDebugProcess6::MarkDebuggerAttached Yöntemi</span><span class="sxs-lookup"><span data-stu-id="62fc8-102">ICorDebugProcess6::MarkDebuggerAttached Method</span></span>
<span data-ttu-id="62fc8-103">Debugee iç durumu değişir böylece <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> .NET Framework Sınıf Kitaplığı'nda yöntemi döndürür `true`.</span><span class="sxs-lookup"><span data-stu-id="62fc8-103">Changes the internal state of the debugee so that the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method in the .NET Framework Class Library returns `true`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="62fc8-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="62fc8-104">Syntax</span></span>  
  
```  
HRESULT MarkDebuggerAttached(  
    BOOL fIsAttached  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="62fc8-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="62fc8-105">Parameters</span></span>  
 `fIsAttached`  
 <span data-ttu-id="62fc8-106">`true`varsa <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> yöntemi belirten bir hata ayıklayıcısı bağlı olduğu; `false` Aksi takdirde.</span><span class="sxs-lookup"><span data-stu-id="62fc8-106">`true` if the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method should indicate that a debugger is attached; `false` otherwise.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="62fc8-107">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="62fc8-107">Return Value</span></span>  
 <span data-ttu-id="62fc8-108">Yöntemi aşağıdaki tabloda listelenen değerleri döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="62fc8-108">The method can return the values listed in the following table.</span></span>  
  
|<span data-ttu-id="62fc8-109">Dönüş değeri</span><span class="sxs-lookup"><span data-stu-id="62fc8-109">Return value</span></span>|<span data-ttu-id="62fc8-110">Açıklama</span><span class="sxs-lookup"><span data-stu-id="62fc8-110">Description</span></span>|  
|------------------|-----------------|  
|`S_OK`|<span data-ttu-id="62fc8-111">Ayıklayıcı başarıyla güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="62fc8-111">The debuggee was successfully updated.</span></span>|  
|`CORDBG_E_MODULE_NOT_LOADED`|<span data-ttu-id="62fc8-112">İçeren derlemenin <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> yöntemi yüklü değil veya eksik meta verileri gibi diğer bazı hata kabul görünür duruma engelliyor.</span><span class="sxs-lookup"><span data-stu-id="62fc8-112">The assembly that contains the <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> method is not loaded, or some other error, such as missing metadata, is preventing it from being recognized.</span></span><br /><br /> <span data-ttu-id="62fc8-113">Bu, ortak ve zararsız hatasıdır.</span><span class="sxs-lookup"><span data-stu-id="62fc8-113">This error is common and benign.</span></span> <span data-ttu-id="62fc8-114">Ek derlemeler yüklediğinizde yöntemi yeniden çağırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="62fc8-114">You should call the method again when additional assemblies load.</span></span>|  
|<span data-ttu-id="62fc8-115">Diğer başarısız `HRESULT` değerleri.</span><span class="sxs-lookup"><span data-stu-id="62fc8-115">Other failing `HRESULT` values.</span></span>|<span data-ttu-id="62fc8-116">Diğer değerleri büyük olasılıkla hatalı davranan hata ayıklayıcı veya derleyici bileşenleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="62fc8-116">Other values likely indicate misbehaving debugger or compiler components.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="62fc8-117">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="62fc8-117">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="62fc8-118">Bu yöntem yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="62fc8-118">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="62fc8-119">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="62fc8-119">Requirements</span></span>  
 <span data-ttu-id="62fc8-120">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="62fc8-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="62fc8-121">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="62fc8-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="62fc8-122">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="62fc8-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="62fc8-123">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="62fc8-123">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62fc8-124">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="62fc8-124">See Also</span></span>  
 [<span data-ttu-id="62fc8-125">Icordebugprocess6 arabirimi</span><span class="sxs-lookup"><span data-stu-id="62fc8-125">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)  
 [<span data-ttu-id="62fc8-126">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="62fc8-126">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)