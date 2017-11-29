---
title: "IMetaDataAssemblyImport::CloseEnum Yöntemi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataAssemblyImport.CloseEnum
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataAssemblyImport::CloseEnum
helpviewer_keywords:
- CloseEnum method, IMetaDataAssemblyImport interface [.NET Framework metadata]
- IMetaDataAssemblyImport::CloseEnum method [.NET Framework metadata]
ms.assetid: c9df4087-12b3-46d9-b075-9067dd7805df
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: a239ee69bdcb8c7558a28c7b04a02adbf358be09
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="imetadataassemblyimportcloseenum-method"></a><span data-ttu-id="8ab82-102">IMetaDataAssemblyImport::CloseEnum Yöntemi</span><span class="sxs-lookup"><span data-stu-id="8ab82-102">IMetaDataAssemblyImport::CloseEnum Method</span></span>
<span data-ttu-id="8ab82-103">Belirtilen numaralandırma örneğine başvuru serbest bırakır.</span><span class="sxs-lookup"><span data-stu-id="8ab82-103">Releases a reference to the specified enumeration instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ab82-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8ab82-104">Syntax</span></span>  
  
```  
void CloseEnum (  
    [in] HCORENUM     hEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8ab82-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="8ab82-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="8ab82-106">[in] Kapatılması numaralandırması örneği.</span><span class="sxs-lookup"><span data-stu-id="8ab82-106">[in] The enumeration instance to be closed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ab82-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="8ab82-107">Requirements</span></span>  
 <span data-ttu-id="8ab82-108">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8ab82-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ab82-109">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="8ab82-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8ab82-110">**Kitaplığı:** MsCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="8ab82-110">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8ab82-111">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8ab82-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8ab82-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="8ab82-112">See Also</span></span>  
 [<span data-ttu-id="8ab82-113">Imetadataassemblyımport arabirimi</span><span class="sxs-lookup"><span data-stu-id="8ab82-113">IMetaDataAssemblyImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
