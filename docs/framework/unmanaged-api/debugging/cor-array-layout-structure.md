---
title: "COR_ARRAY_LAYOUT Yapısı"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_ARRAY_LAYOUT
api_location: mscordbi.dll
api_type: COM
f1_keywords: COR_ARRAY_LAYOUT
helpviewer_keywords: COR_DEBUG_IL_TO_NATIVE_MAP structure [.NET Framework debugging]
ms.assetid: aa20ac3d-6f60-4aa2-91c5-f3a86f82eba8
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 02ddd87cfaf16990ff487dfe27f30a2493cb9a01
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="corarraylayout-structure"></a><span data-ttu-id="8875e-102">COR_ARRAY_LAYOUT Yapısı</span><span class="sxs-lookup"><span data-stu-id="8875e-102">COR_ARRAY_LAYOUT Structure</span></span>
<span data-ttu-id="8875e-103">Bellekte bir dizi nesnesi düzen hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8875e-103">Provides information about the layout of an array object in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8875e-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8875e-104">Syntax</span></span>  
  
```  
typedef struct COR_ARRAY_LAYOUT {  
    COR_TYPEID componentID;  
    CorElementType componentType;  
    ULONG32 firstElementOffset;  
    ULONG32 elementSize;  
    ULONG32 countOffset;   
    ULONG32 rankSize;   
    ULONG32 numRanks;   
    ULONG32 rankOffset;   
} COR_ARRAY_LAYOUT;  
```  
  
## <a name="members"></a><span data-ttu-id="8875e-105">Üyeler</span><span class="sxs-lookup"><span data-stu-id="8875e-105">Members</span></span>  
  
|<span data-ttu-id="8875e-106">Üye</span><span class="sxs-lookup"><span data-stu-id="8875e-106">Member</span></span>|<span data-ttu-id="8875e-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="8875e-107">Description</span></span>|  
|------------|-----------------|  
|`componentID`|<span data-ttu-id="8875e-108">Dizinin içerdiği nesnelerin türü tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8875e-108">The identifier of the type of objects that the array contains.</span></span>|  
|`componentType`|<span data-ttu-id="8875e-109">Bileşen bir atık toplama başvuru, bir değer sınıfı ya da basit bir tür olup olmadığını belirten bir CorElementType numaralandırması değer.</span><span class="sxs-lookup"><span data-stu-id="8875e-109">A CorElementType enumeration value that indicates whether the component is a garbage collection reference, a value class, or a primitive.</span></span>|  
|`firstElementOffset`|<span data-ttu-id="8875e-110">Dizinin ilk öğe uzaklık.</span><span class="sxs-lookup"><span data-stu-id="8875e-110">The offset to the first element in the array.</span></span>|  
|`elementSize`|<span data-ttu-id="8875e-111">Her öğe boyutu.</span><span class="sxs-lookup"><span data-stu-id="8875e-111">The size of each element.</span></span>|  
|`countOffset`|<span data-ttu-id="8875e-112">Dizideki öğelerin sayısı uzaklık.</span><span class="sxs-lookup"><span data-stu-id="8875e-112">The offset to the number of elements in the array.</span></span>|  
|`rankSize`|<span data-ttu-id="8875e-113">Derecesini bayt cinsinden boyutu.</span><span class="sxs-lookup"><span data-stu-id="8875e-113">The size of the rank, in bytes.</span></span>|  
|`numRanks`|<span data-ttu-id="8875e-114">Dizideki sıralar sayısı.</span><span class="sxs-lookup"><span data-stu-id="8875e-114">The number of ranks in the array.</span></span>|  
|`rankOffset`|<span data-ttu-id="8875e-115">Hangi sıralar başlangıç uzaklığı.</span><span class="sxs-lookup"><span data-stu-id="8875e-115">The offset at which the ranks start.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8875e-116">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="8875e-116">Remarks</span></span>  
 <span data-ttu-id="8875e-117">`rankSize` Alan çok boyutlu bir dizi sırası boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8875e-117">The `rankSize` field specifies the size of a rank in a multi-dimensional array.</span></span> <span data-ttu-id="8875e-118">De tek boyutlu diziler doğru olur.</span><span class="sxs-lookup"><span data-stu-id="8875e-118">It is accurate for single-dimensional arrays as well.</span></span>  
  
 <span data-ttu-id="8875e-119">Değeri `numRanks` tek boyutlu bir dizi için 1'dir ve `N` çok boyutlu bir dizi için `N` boyutları.</span><span class="sxs-lookup"><span data-stu-id="8875e-119">The value of `numRanks` is 1 for a single-dimensional array and `N` for a multi-dimensional array of `N` dimensions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8875e-120">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="8875e-120">Requirements</span></span>  
 <span data-ttu-id="8875e-121">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8875e-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8875e-122">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8875e-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8875e-123">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8875e-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8875e-124">**.NET framework sürümleri:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8875e-124">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8875e-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="8875e-125">See Also</span></span>  
 [<span data-ttu-id="8875e-126">Hata ayıklama yapıları</span><span class="sxs-lookup"><span data-stu-id="8875e-126">Debugging Structures</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-structures.md)  
 [<span data-ttu-id="8875e-127">Hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="8875e-127">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)