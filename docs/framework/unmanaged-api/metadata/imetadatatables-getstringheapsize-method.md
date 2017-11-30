---
title: IMetaDataTables::GetStringHeapSize Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataTables.GetStringHeapSize
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataTables::GetStringHeapSize
helpviewer_keywords:
- IMetaDataTables::GetStringHeapSize method [.NET Framework metadata]
- GetStringHeapSize method [.NET Framework metadata]
ms.assetid: ed8f6335-81f5-4c09-81a9-2a909fc530c9
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: a0e664192ac39dd12085346738dbc283a11d3381
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatatablesgetstringheapsize-method"></a><span data-ttu-id="dccb4-102">IMetaDataTables::GetStringHeapSize Metodu</span><span class="sxs-lookup"><span data-stu-id="dccb4-102">IMetaDataTables::GetStringHeapSize Method</span></span>
<span data-ttu-id="dccb4-103">Dize yığın bayt cinsinden boyutu alır.</span><span class="sxs-lookup"><span data-stu-id="dccb4-103">Gets the size, in bytes, of the string heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dccb4-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="dccb4-104">Syntax</span></span>  
  
```  
HRESULT GetStringHeapSize (  
    [out] ULONG   *pcbStrings  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dccb4-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="dccb4-105">Parameters</span></span>  
 `pcbStrings`  
 <span data-ttu-id="dccb4-106">[out] Bir işaretçi bayt dizesi yığın boyutu.</span><span class="sxs-lookup"><span data-stu-id="dccb4-106">[out] A pointer to the size, in bytes, of the string heap.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dccb4-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="dccb4-107">Requirements</span></span>  
 <span data-ttu-id="dccb4-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dccb4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dccb4-109">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="dccb4-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="dccb4-110">**Kitaplığı:** MsCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="dccb4-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="dccb4-111">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dccb4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dccb4-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="dccb4-112">See Also</span></span>  
 [<span data-ttu-id="dccb4-113">Imetadatatables arabirimi</span><span class="sxs-lookup"><span data-stu-id="dccb4-113">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="dccb4-114">Imetadatatables2 arabirimi</span><span class="sxs-lookup"><span data-stu-id="dccb4-114">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
