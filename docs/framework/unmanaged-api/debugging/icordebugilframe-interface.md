---
title: "Icordebugılframe Interface1"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugILFrame
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugILFrame
helpviewer_keywords: ICorDebugILFrame interface [.NET Framework debugging]
ms.assetid: d5cf5056-da4d-4629-914d-afe42a5393df
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d8d370fa971f698eb694127c72ff96499b85143d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugilframe-interface1"></a><span data-ttu-id="cbcf4-102">Icordebugılframe Interface1</span><span class="sxs-lookup"><span data-stu-id="cbcf4-102">ICorDebugILFrame Interface1</span></span>
<span data-ttu-id="cbcf4-103">Yığın çerçevesi Microsoft Ara dili (MSIL) kodunun temsil eder.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-103">Represents a stack frame of Microsoft intermediate language (MSIL) code.</span></span> <span data-ttu-id="cbcf4-104">Bu arabirim Icordebugframe arabirimi sınıfıdır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-104">This interface is a subclass of the ICorDebugFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cbcf4-105">Yöntemler</span><span class="sxs-lookup"><span data-stu-id="cbcf4-105">Methods</span></span>  
  
|<span data-ttu-id="cbcf4-106">Yöntem</span><span class="sxs-lookup"><span data-stu-id="cbcf4-106">Method</span></span>|<span data-ttu-id="cbcf4-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="cbcf4-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cbcf4-108">Cansetıp yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-108">CanSetIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-cansetip-method.md)|<span data-ttu-id="cbcf4-109">Yönerge işaretçisi belirtilen uzaklık konuma ayarlamak güvenli olup olmadığını belirten bir değer alır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-109">Gets a value that indicates whether it is safe to set the instruction pointer to the specified offset location.</span></span>|  
|[<span data-ttu-id="cbcf4-110">EnumerateArguments yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-110">EnumerateArguments Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratearguments-method.md)|<span data-ttu-id="cbcf4-111">Bir numaralandırıcı Bu çerçevede bağımsız değişkenleri alır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-111">Gets an enumerator for the arguments in this frame.</span></span>|  
|[<span data-ttu-id="cbcf4-112">EnumerateLocalVariables yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-112">EnumerateLocalVariables Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-enumeratelocalvariables-method.md)|<span data-ttu-id="cbcf4-113">Bir numaralandırıcı yerel değişkenler için bu çerçevede alır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-113">Gets an enumerator for the local variables in this frame.</span></span>|  
|[<span data-ttu-id="cbcf4-114">GetArgument yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-114">GetArgument Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getargument-method.md)|<span data-ttu-id="cbcf4-115">Belirtilen bağımsız değişkenin değeri bu MSIL yığın çerçevesinde alır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-115">Gets the value of the specified argument in this MSIL stack frame.</span></span>|  
|[<span data-ttu-id="cbcf4-116">Getıp yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-116">GetIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getip-method.md)|<span data-ttu-id="cbcf4-117">Yönerge işaretçisi değerini ve nasıl yönerge işaretçisi değerini edinilen açıklayan Bitsel bir birleşimi değeri alır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-117">Gets the value of the instruction pointer and a bitwise combination value that describes how the value of the instruction pointer was obtained.</span></span>|  
|[<span data-ttu-id="cbcf4-118">GetLocalVariable yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-118">GetLocalVariable Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getlocalvariable-method.md)|<span data-ttu-id="cbcf4-119">Bu MSIL yığın çerçevesinde belirtilen yerel değişkenin değerini alır.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-119">Gets the value of the specified local variable in this MSIL stack frame.</span></span>|  
|[<span data-ttu-id="cbcf4-120">GetStackDepth yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-120">GetStackDepth Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getstackdepth-method.md)|<span data-ttu-id="cbcf4-121">Henüz uygulanmadı.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-121">Not implemented.</span></span>|  
|[<span data-ttu-id="cbcf4-122">GetStackValue yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-122">GetStackValue Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-getstackvalue-method.md)|<span data-ttu-id="cbcf4-123">Henüz uygulanmadı.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-123">Not implemented.</span></span>|  
|[<span data-ttu-id="cbcf4-124">SetIP yöntemi</span><span class="sxs-lookup"><span data-stu-id="cbcf4-124">SetIP Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugilframe-setip-method.md)|<span data-ttu-id="cbcf4-125">Yönerge işaretçisi MSIL kodda belirtilen uzaklık konumuna ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-125">Sets the instruction pointer to the specified offset location in the MSIL code.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cbcf4-126">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="cbcf4-126">Remarks</span></span>  
 <span data-ttu-id="cbcf4-127">`ICorDebugILFrame` Özel Icordebugframe arabirimi bir arabirimdir.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-127">The `ICorDebugILFrame` interface is a specialized ICorDebugFrame interface.</span></span> <span data-ttu-id="cbcf4-128">Kullanıldığı MSIL kod çerçeveleri için veya tam zamanında (JIT) için çerçeveler derlenmiş.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-128">It is used either for MSIL code frames or for just-in-time (JIT) compiled frames.</span></span> <span data-ttu-id="cbcf4-129">JIT derlenmiş çerçeveleri her ikisini de uygulamak `ICorDebugILFrame` arabirimi ve Icordebugnativeframe arabirimi.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-129">The JIT-compiled frames implement both the `ICorDebugILFrame` interface and the ICorDebugNativeFrame interface.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cbcf4-130">Bu arabirim, makineler arası veya çapraz işlem uzaktan çağrılan desteklemez.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-130">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cbcf4-131">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="cbcf4-131">Requirements</span></span>  
 <span data-ttu-id="cbcf4-132">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="cbcf4-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cbcf4-133">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cbcf4-133">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cbcf4-134">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cbcf4-134">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cbcf4-135">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cbcf4-135">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cbcf4-136">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="cbcf4-136">See Also</span></span>  
 [<span data-ttu-id="cbcf4-137">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="cbcf4-137">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
