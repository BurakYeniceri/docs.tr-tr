---
title: ICorDebugArrayValue::GetElementType Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugArrayValue.GetElementType
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugArrayValue::GetElementType
helpviewer_keywords:
- ICorDebugArrayValue::GetElementType method [.NET Framework debugging]
- GetElementType method [.NET Framework debugging]
ms.assetid: ed71961e-ae9b-4dfc-9554-06637696d697
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f225dd26376d511518900c38e13d74503004da17
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugarrayvaluegetelementtype-method"></a><span data-ttu-id="0f01d-102">ICorDebugArrayValue::GetElementType Metodu</span><span class="sxs-lookup"><span data-stu-id="0f01d-102">ICorDebugArrayValue::GetElementType Method</span></span>
<span data-ttu-id="0f01d-103">Dizideki öğeler basit türünü belirten bir değer alır.</span><span class="sxs-lookup"><span data-stu-id="0f01d-103">Gets a value that indicates the simple type of the elements in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f01d-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="0f01d-104">Syntax</span></span>  
  
```  
HRESULT GetElementType (  
    [out] CorElementType  *pType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0f01d-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="0f01d-105">Parameters</span></span>  
 `pType`  
 <span data-ttu-id="0f01d-106">[out] Türünü gösteren CorElementType numaralandırması değerini gösteren bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="0f01d-106">[out] A pointer to a value of the CorElementType enumeration that indicates the type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f01d-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="0f01d-107">Requirements</span></span>  
 <span data-ttu-id="0f01d-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0f01d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0f01d-109">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0f01d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0f01d-110">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0f01d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0f01d-111">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0f01d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
