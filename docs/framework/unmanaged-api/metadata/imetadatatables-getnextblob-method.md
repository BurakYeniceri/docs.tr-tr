---
title: IMetaDataTables::GetNextBlob Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataTables.GetNextBlob
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataTables::GetNextBlob
helpviewer_keywords:
- IMetaDataTables::GetNextBlob method [.NET Framework metadata]
- GetNextBlob method [.NET Framework metadata]
ms.assetid: 017c8ab4-4c09-4754-9935-5b0b49cabecb
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 151fdf06f6203eabf2fc3e37bd30399b52394124
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="imetadatatablesgetnextblob-method"></a><span data-ttu-id="622d2-102">IMetaDataTables::GetNextBlob Metodu</span><span class="sxs-lookup"><span data-stu-id="622d2-102">IMetaDataTables::GetNextBlob Method</span></span>
<span data-ttu-id="622d2-103">Tabloda sonraki ikili büyük nesne (BLOB) dizinini alır.</span><span class="sxs-lookup"><span data-stu-id="622d2-103">Gets the index of the next binary large object (BLOB) in the table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="622d2-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="622d2-104">Syntax</span></span>  
  
```  
HRESULT GetNextBlob (  
    [in]  ULONG   ixBlob,  
    [out] ULONG   *pNext  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="622d2-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="622d2-105">Parameters</span></span>  
 `ixBlob`  
 <span data-ttu-id="622d2-106">[in] BLOB'ları sütundan döndürülen dizini.</span><span class="sxs-lookup"><span data-stu-id="622d2-106">[in] The index, as returned from a column of BLOBs.</span></span>  
  
 `pNext`  
 <span data-ttu-id="622d2-107">[out] Sonraki BLOB dizini için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="622d2-107">[out] A pointer to the index of the next BLOB.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="622d2-108">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="622d2-108">Requirements</span></span>  
 <span data-ttu-id="622d2-109">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="622d2-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="622d2-110">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="622d2-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="622d2-111">**Kitaplığı:** MsCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="622d2-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="622d2-112">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="622d2-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="622d2-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="622d2-113">See Also</span></span>  
 [<span data-ttu-id="622d2-114">Imetadatatables arabirimi</span><span class="sxs-lookup"><span data-stu-id="622d2-114">IMetaDataTables Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables-interface.md)  
 [<span data-ttu-id="622d2-115">Imetadatatables2 arabirimi</span><span class="sxs-lookup"><span data-stu-id="622d2-115">IMetaDataTables2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatatables2-interface.md)
