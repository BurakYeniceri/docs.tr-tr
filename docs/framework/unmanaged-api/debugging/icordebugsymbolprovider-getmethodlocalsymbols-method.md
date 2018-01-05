---
title: "ICorDebugSymbolProvider::GetMethodLocalSymbols yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 8b989e38-e779-49d1-9e90-f1f920484b08
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c07151c4cdd43df17025deff4af37a0156ecaf78
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugsymbolprovidergetmethodlocalsymbols-method"></a><span data-ttu-id="8d438-102">ICorDebugSymbolProvider::GetMethodLocalSymbols yöntemi</span><span class="sxs-lookup"><span data-stu-id="8d438-102">ICorDebugSymbolProvider::GetMethodLocalSymbols Method</span></span>
<span data-ttu-id="8d438-103">Bu yöntemin göreli sanal adres (RVA) verilen bir yöntemin yerel simgelerini alır.</span><span class="sxs-lookup"><span data-stu-id="8d438-103">Gets a method's local symbols given the relative virtual address (RVA) of that method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d438-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8d438-104">Syntax</span></span>  
  
```  
HRESULT GetMethodLocalSymbols(  
   [in] ULONG32 nativeRVA,  
   [in] ULONG32 cRequestedSymbols,  
   [out] ULONG32 *pcFetchedSymbols,  
   [out, size_is(cRequestedSymbols), length_is(*pcFetchedSymbols)] ICorDebugVariableSymbol *pSymbols[]  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8d438-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="8d438-105">Parameters</span></span>  
 `nativeRVA`  
 <span data-ttu-id="8d438-106">[in] Yerel göreli sanal adresi yöntemi.</span><span class="sxs-lookup"><span data-stu-id="8d438-106">[in] The native relative virtual address of the method.</span></span>  
  
 `cRequestedSymbols`  
 <span data-ttu-id="8d438-107">[in] İstenen yerel semboller sayısı.</span><span class="sxs-lookup"><span data-stu-id="8d438-107">[in] The number of local symbols requested.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="8d438-108">[out] Sembol yöntemi tarafından alınan sayısını gösteren bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="8d438-108">[out] A pointer to the number of symbols retrieved by the method.</span></span>  
  
 `pcFetchedSymbols`  
 <span data-ttu-id="8d438-109">[out] Bir işaretçi bir [ICorDebugVariableSymbol](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md) yöntemin yerel semboller içeren bir dizi.</span><span class="sxs-lookup"><span data-stu-id="8d438-109">[out] A pointer to an [ICorDebugVariableSymbol](../../../../docs/framework/unmanaged-api/debugging/icordebugvariablesymbol-interface.md) array that contains the method's local symbols.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8d438-110">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="8d438-110">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8d438-111">Bu yöntem yalnızca .NET yerel ile kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8d438-111">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8d438-112">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="8d438-112">Requirements</span></span>  
 <span data-ttu-id="8d438-113">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8d438-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8d438-114">**Başlık:** CorDebug.idl, CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8d438-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8d438-115">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8d438-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8d438-116">**.NET framework sürümleri:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8d438-116">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8d438-117">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="8d438-117">See Also</span></span>  
 [<span data-ttu-id="8d438-118">GetMethodParameterSymbols Yöntemi</span><span class="sxs-lookup"><span data-stu-id="8d438-118">GetMethodParameterSymbols Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-getmethodparametersymbols-method.md)  
 [<span data-ttu-id="8d438-119">ICorDebugSymbolProvider Arabirimi</span><span class="sxs-lookup"><span data-stu-id="8d438-119">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="8d438-120">Hata Ayıklama Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="8d438-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
