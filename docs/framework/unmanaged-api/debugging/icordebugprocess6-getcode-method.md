---
title: ICorDebugProcess6::GetCode Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: faa538c2-60c9-4064-b996-1b4c24ebd751
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c69ce290a486960978ddaf87203328df4f392b48
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugprocess6getcode-method"></a><span data-ttu-id="5b2f1-102">ICorDebugProcess6::GetCode Metodu</span><span class="sxs-lookup"><span data-stu-id="5b2f1-102">ICorDebugProcess6::GetCode Method</span></span>
<span data-ttu-id="5b2f1-103">Yönetilen kodu hakkında bilgi belirli kod adresinde alır.</span><span class="sxs-lookup"><span data-stu-id="5b2f1-103">Gets information about the managed code at a particular code address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5b2f1-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="5b2f1-104">Syntax</span></span>  
  
```  
HRESULT GetCode(  
    [in] CORDB_ADDRESS codeAddress,   
    [out] ICorDebugCode **ppCode);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5b2f1-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="5b2f1-105">Parameters</span></span>  
 `codeAddress`  
 <span data-ttu-id="5b2f1-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) yönetilen kod kesimi başlangıç adresini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="5b2f1-106">[in] A [CORDB_ADDRESS](../../../../docs/framework/unmanaged-api/common-data-types-unmanaged-api-reference.md) value that specifies the starting address of the managed code segment.</span></span>  
  
 `ppCode`  
 <span data-ttu-id="5b2f1-107">[out] Yönetilen kod kesimini temsil eder "ICorDebugCode" nesneyi adresini gösteren bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="5b2f1-107">[out] A pointer to the address of an "ICorDebugCode" object that represents a segment of managed code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5b2f1-108">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="5b2f1-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5b2f1-109">Bu yöntem yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5b2f1-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5b2f1-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="5b2f1-110">Requirements</span></span>  
 <span data-ttu-id="5b2f1-111">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="5b2f1-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5b2f1-112">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5b2f1-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5b2f1-113">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5b2f1-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5b2f1-114">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5b2f1-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5b2f1-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5b2f1-115">See Also</span></span>  
 [<span data-ttu-id="5b2f1-116">Icordebugprocess6 arabirimi</span><span class="sxs-lookup"><span data-stu-id="5b2f1-116">ICorDebugProcess6 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-interface.md)  
 [<span data-ttu-id="5b2f1-117">Hata ayıklama arabirimleri</span><span class="sxs-lookup"><span data-stu-id="5b2f1-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)