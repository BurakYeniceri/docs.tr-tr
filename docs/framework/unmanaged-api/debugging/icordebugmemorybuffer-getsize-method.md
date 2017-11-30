---
title: "ICorDebugMemoryBuffer::GetSize yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 9ffd5482-268e-4680-9fd1-bfb0b7d66450
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a21198c70512af703e106870d1bc3f7882d62fe9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmemorybuffergetsize-method"></a><span data-ttu-id="fd4f4-102">ICorDebugMemoryBuffer::GetSize yöntemi</span><span class="sxs-lookup"><span data-stu-id="fd4f4-102">ICorDebugMemoryBuffer::GetSize Method</span></span>
<span data-ttu-id="fd4f4-103">Bellek arabellek boyutunu bayt cinsinden alır.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-103">Gets the size of the memory buffer in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd4f4-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="fd4f4-104">Syntax</span></span>  
  
```  
HRESULT GetSize(  
   [out] ULONG32 *pcbBufferLength  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fd4f4-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="fd4f4-105">Parameters</span></span>  
 `pcbBufferLength`  
 <span data-ttu-id="fd4f4-106">[out] Bellek arabellek boyutu için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-106">[out] A pointer to the size of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fd4f4-107">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="fd4f4-107">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fd4f4-108">Bu yöntem yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-108">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd4f4-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="fd4f4-109">Requirements</span></span>  
 <span data-ttu-id="fd4f4-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fd4f4-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd4f4-111">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fd4f4-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fd4f4-112">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fd4f4-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fd4f4-113">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd4f4-113">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd4f4-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="fd4f4-114">See Also</span></span>  
 [<span data-ttu-id="fd4f4-115">ICorDebugMemoryBuffer arabirimi</span><span class="sxs-lookup"><span data-stu-id="fd4f4-115">ICorDebugMemoryBuffer Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md)  
 [<span data-ttu-id="fd4f4-116">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="fd4f4-116">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
