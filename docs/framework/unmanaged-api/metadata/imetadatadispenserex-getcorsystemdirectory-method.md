---
title: IMetaDataDispenserEx::GetCORSystemDirectory Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataDispenserEx.GetCORSystemDirectory
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataDispenserEx::GetCORSystemDirectory
helpviewer_keywords:
- IMetaDataDispenserEx::GetCORSystemDirectory method [.NET Framework metadata]
- GetCORSystemDirectory method [.NET Framework metadata]
ms.assetid: d9e0f3b6-e106-4820-bada-5bfba34ce360
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: a876d6ffb8331ee52789d5c146db7615d352dc1b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatadispenserexgetcorsystemdirectory-method"></a><span data-ttu-id="fd324-102">IMetaDataDispenserEx::GetCORSystemDirectory Metodu</span><span class="sxs-lookup"><span data-stu-id="fd324-102">IMetaDataDispenserEx::GetCORSystemDirectory Method</span></span>
<span data-ttu-id="fd324-103">Geçerli ortak dil çalışma zamanı (CLR) tutan dizinin alır.</span><span class="sxs-lookup"><span data-stu-id="fd324-103">Gets the directory that holds the current common language runtime (CLR).</span></span> <span data-ttu-id="fd324-104">Bu yöntem yalnızca kullanım için işlem dışı hata ayıklayıcıları tarafından desteklenir.</span><span class="sxs-lookup"><span data-stu-id="fd324-104">This method is supported only for use by out-of-process debuggers.</span></span> <span data-ttu-id="fd324-105">Başka bir bileşen tarafından çağrılan olursa E_NOTIMPL döndürür.</span><span class="sxs-lookup"><span data-stu-id="fd324-105">If called from another component, it will return E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd324-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="fd324-106">Syntax</span></span>  
  
```  
HRESULT GetCORSystemDirectory (  
    [out] LPWSTR      szBuffer,   
    [in]  DWORD       cchBuffer,   
    [out] DWORD*      pchBuffer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fd324-107">Parametreler</span><span class="sxs-lookup"><span data-stu-id="fd324-107">Parameters</span></span>  
 `szBuffer`  
 <span data-ttu-id="fd324-108">[out] Dizin adı almak için bir arabellek.</span><span class="sxs-lookup"><span data-stu-id="fd324-108">[out] The buffer to receive the directory name.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="fd324-109">[in] Bayt olarak boyutu, `szBuffer`.</span><span class="sxs-lookup"><span data-stu-id="fd324-109">[in] The size, in bytes, of `szBuffer`.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="fd324-110">[out] Gerçekte döndürülen bayt sayısı `szBuffer`.</span><span class="sxs-lookup"><span data-stu-id="fd324-110">[out] The number of bytes actually returned in `szBuffer`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fd324-111">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="fd324-111">Requirements</span></span>  
 <span data-ttu-id="fd324-112">**Platform:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fd324-112">**Platform:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fd324-113">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="fd324-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fd324-114">**Kitaplığı:** MsCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="fd324-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fd324-115">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fd324-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd324-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="fd324-116">See Also</span></span>  
 [<span data-ttu-id="fd324-117">Imetadatadispenserex arabirimi</span><span class="sxs-lookup"><span data-stu-id="fd324-117">IMetaDataDispenserEx Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)  
 [<span data-ttu-id="fd324-118">Imetadatadispenser arabirimi</span><span class="sxs-lookup"><span data-stu-id="fd324-118">IMetaDataDispenser Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
