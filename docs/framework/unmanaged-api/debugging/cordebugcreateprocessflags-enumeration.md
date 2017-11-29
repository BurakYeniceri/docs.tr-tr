---
title: "CorDebugCreateProcessFlags Numaralandırması"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugCreateProcessFlags
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugCreateProcessFlags
helpviewer_keywords: CorDebugCreateProcessFlags enumeration [.NET Framework debugging]
ms.assetid: e709acce-6a17-4346-b38a-467dba567358
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 35503a89077b05d622ccc3f8e5cf1bb7d95ea9e0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="21ac5-102">CorDebugCreateProcessFlags Numaralandırması</span><span class="sxs-lookup"><span data-stu-id="21ac5-102">CorDebugCreateProcessFlags Enumeration</span></span>
<span data-ttu-id="21ac5-103">Çağrıda kullanılan ek hata ayıklama seçenekleri sunar [Icordebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="21ac5-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="21ac5-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="21ac5-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="21ac5-105">Üyeler</span><span class="sxs-lookup"><span data-stu-id="21ac5-105">Members</span></span>  
  
|<span data-ttu-id="21ac5-106">Üye</span><span class="sxs-lookup"><span data-stu-id="21ac5-106">Member</span></span>|<span data-ttu-id="21ac5-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="21ac5-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="21ac5-108">Hiçbir özel seçeneklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="21ac5-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="21ac5-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="21ac5-109">Requirements</span></span>  
 <span data-ttu-id="21ac5-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="21ac5-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="21ac5-111">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="21ac5-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="21ac5-112">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="21ac5-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="21ac5-113">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="21ac5-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="21ac5-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="21ac5-114">See Also</span></span>  
 [<span data-ttu-id="21ac5-115">Hata ayıklama numaralandırmaları</span><span class="sxs-lookup"><span data-stu-id="21ac5-115">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
