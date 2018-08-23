---
title: GetAssemblyIdentityFromFile İşlevi
ms.date: 03/30/2017
api_name:
- GetAssemblyIdentityFromFile
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- COM
f1_keywords:
- GetAssemblyIdentityFromFile
helpviewer_keywords:
- GetAssemblyIdentityFromFile function [.NET Framework fusion]
ms.assetid: 2c32da53-76c7-4048-84d0-d05207333004
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6dfb0b404413351761d269c800be19e75acfb41f
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42752292"
---
# <a name="getassemblyidentityfromfile-function"></a><span data-ttu-id="479dd-102">GetAssemblyIdentityFromFile İşlevi</span><span class="sxs-lookup"><span data-stu-id="479dd-102">GetAssemblyIdentityFromFile Function</span></span>
<span data-ttu-id="479dd-103">Bir işaretçi alır bir `IUnknown` belirtilen nesnesiyle `IID` belirtilen dosya yolunda derlemedeki.</span><span class="sxs-lookup"><span data-stu-id="479dd-103">Gets a pointer to an `IUnknown` object with the specified `IID` in the assembly at the specified file path.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="479dd-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="479dd-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyIdentityFromFile (  
    [in]  LPCWSTR   pwzFilePath,  
    [in]  REFIID    riid,  
    [out] IUnknown  **ppIdentity  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="479dd-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="479dd-105">Parameters</span></span>  
 `pwzFilePath`  
 <span data-ttu-id="479dd-106">[in] İstenen derleme için geçerli bir yol.</span><span class="sxs-lookup"><span data-stu-id="479dd-106">[in] A valid path to the requested assembly.</span></span>  
  
 `riid`  
 <span data-ttu-id="479dd-107">[in] `IID` Döndürülecek arabirimi.</span><span class="sxs-lookup"><span data-stu-id="479dd-107">[in] The `IID` of the interface to return.</span></span>  
  
 `ppIdentity`  
 <span data-ttu-id="479dd-108">[out] Döndürülen arabirim işaretçisi.</span><span class="sxs-lookup"><span data-stu-id="479dd-108">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="479dd-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="479dd-109">Requirements</span></span>  
 <span data-ttu-id="479dd-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="479dd-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="479dd-111">**Başlık:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="479dd-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="479dd-112">**.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="479dd-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="479dd-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="479dd-113">See Also</span></span>  
 [<span data-ttu-id="479dd-114">IUnknown</span><span class="sxs-lookup"><span data-stu-id="479dd-114">IUnknown</span></span>](/cpp/atl/iunknown)  
 [<span data-ttu-id="479dd-115">Fusion Genel Statik İşlevleri</span><span class="sxs-lookup"><span data-stu-id="479dd-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
