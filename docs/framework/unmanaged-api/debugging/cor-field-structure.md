---
title: "COR_FIELD Yapısı"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_FIELD
api_location: mscordbi.dll
api_type: COM
f1_keywords: COR_FIELD
helpviewer_keywords: COR_FIELD structure [.NET Framework debugging]
ms.assetid: c0822423-a9df-4961-950d-50dcc152f863
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 09a96a22a653688540bcc2ea3a03d86e242c10f5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="corfield-structure"></a><span data-ttu-id="2329d-102">COR_FIELD Yapısı</span><span class="sxs-lookup"><span data-stu-id="2329d-102">COR_FIELD Structure</span></span>
<span data-ttu-id="2329d-103">Bir nesne bir alanda hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2329d-103">Provides information about a field in an object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2329d-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2329d-104">Syntax</span></span>  
  
```  
typedef struct COR_FIELD{  
    mdFieldDef token;  
    ULONG32 offset;  
    COR_TYPEID id;  
    CorElementType fieldType;  
} COR_FIELD;  
```  
  
## <a name="members"></a><span data-ttu-id="2329d-105">Üyeler</span><span class="sxs-lookup"><span data-stu-id="2329d-105">Members</span></span>  
  
|<span data-ttu-id="2329d-106">Üye</span><span class="sxs-lookup"><span data-stu-id="2329d-106">Member</span></span>|<span data-ttu-id="2329d-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="2329d-107">Description</span></span>|  
|------------|-----------------|  
|`token`|<span data-ttu-id="2329d-108">Bir `mdFieldDef` alan bilgilerini almak için kullanılan belirteç.</span><span class="sxs-lookup"><span data-stu-id="2329d-108">An `mdFieldDef` token that can be used to get field information.</span></span>|  
|`offset`|<span data-ttu-id="2329d-109">Nesne yer alan verilere bayt uzaklığı.</span><span class="sxs-lookup"><span data-stu-id="2329d-109">The offset, in bytes, to the field data in the object.</span></span>|  
|`id`|<span data-ttu-id="2329d-110">A [cor_typeıd](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) bu alanın türünü tanımlayan bir değer.</span><span class="sxs-lookup"><span data-stu-id="2329d-110">A [COR_TYPEID](../../../../docs/framework/unmanaged-api/debugging/cor-typeid-structure.md) value that identifies the type of this field.</span></span>|  
|`fieldType`|<span data-ttu-id="2329d-111">Alan türünü belirten CorElementType numaralandırma değeri.</span><span class="sxs-lookup"><span data-stu-id="2329d-111">A CorElementType enumeration value that indicates the type of the field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2329d-112">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2329d-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2329d-113">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="2329d-113">Requirements</span></span>  
 <span data-ttu-id="2329d-114">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2329d-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2329d-115">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2329d-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2329d-116">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2329d-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2329d-117">**.NET framework sürümleri:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2329d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2329d-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="2329d-118">See Also</span></span>  
 [<span data-ttu-id="2329d-119">Hata Ayıklama Yapıları</span><span class="sxs-lookup"><span data-stu-id="2329d-119">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)  
 [<span data-ttu-id="2329d-120">Hata Ayıklama</span><span class="sxs-lookup"><span data-stu-id="2329d-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
