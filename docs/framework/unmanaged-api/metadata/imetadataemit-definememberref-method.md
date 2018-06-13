---
title: IMetaDataEmit::DefineMemberRef Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineMemberRef
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineMemberRef
helpviewer_keywords:
- DefineMemberRef method [.NET Framework metadata]
- IMetaDataEmit::DefineMemberRef method [.NET Framework metadata]
ms.assetid: 21b5bcb8-ea75-4962-8acc-ad17584061e5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 881c0b1f755e750efcc74ca61a60bbd97bc5dba7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444470"
---
# <a name="imetadataemitdefinememberref-method"></a><span data-ttu-id="790c5-102">IMetaDataEmit::DefineMemberRef Yöntemi</span><span class="sxs-lookup"><span data-stu-id="790c5-102">IMetaDataEmit::DefineMemberRef Method</span></span>
<span data-ttu-id="790c5-103">Geçerli kapsam dışında bir modülün bir üyeye başvuru tanımlar ve bu başvuru tanımına bir belirteci alır.</span><span class="sxs-lookup"><span data-stu-id="790c5-103">Defines a reference to a member of a module outside the current scope, and gets a token to that reference definition.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="790c5-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="790c5-104">Syntax</span></span>  
  
```  
HRESULT DefineMemberRef (   
    [in]  mdToken           tkImport,   
    [in]  LPCWSTR           szName,   
    [in]  PCCOR_SIGNATURE   pvSigBlob,   
    [in]  ULONG             cbSigBlob,   
    [out] mdMemberRef       *pmr   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="790c5-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="790c5-105">Parameters</span></span>  
 `tkImport`  
 <span data-ttu-id="790c5-106">[in] Belirteç hedef üyenin sınıf veya arabirim için üye genel değilse; Genel üyesiyse `mdModuleRef` diğer bu dosya için belirteç.</span><span class="sxs-lookup"><span data-stu-id="790c5-106">[in] Token for the target member's class or interface, if the member is not global; if the member is global, the `mdModuleRef` token for that other file.</span></span>  
  
 `szName`  
 <span data-ttu-id="790c5-107">[in] Hedef üye adı.</span><span class="sxs-lookup"><span data-stu-id="790c5-107">[in] The name of the target member.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="790c5-108">[in] Hedef üye imzası.</span><span class="sxs-lookup"><span data-stu-id="790c5-108">[in] The signature of the target member.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="790c5-109">[in] Bayt sayısı `pvSigBlob`.</span><span class="sxs-lookup"><span data-stu-id="790c5-109">[in] The count of bytes in `pvSigBlob`.</span></span>  
  
 `pmr`  
 <span data-ttu-id="790c5-110">[out] `mdMemberRef` Atanan simgesi.</span><span class="sxs-lookup"><span data-stu-id="790c5-110">[out] The `mdMemberRef` token assigned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="790c5-111">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="790c5-111">Requirements</span></span>  
 <span data-ttu-id="790c5-112">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="790c5-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="790c5-113">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="790c5-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="790c5-114">**Kitaplığı:** MSCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="790c5-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="790c5-115">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="790c5-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="790c5-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="790c5-116">See Also</span></span>  
 [<span data-ttu-id="790c5-117">IMetaDataEmit Arabirimi</span><span class="sxs-lookup"><span data-stu-id="790c5-117">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="790c5-118">IMetaDataEmit2 Arabirimi</span><span class="sxs-lookup"><span data-stu-id="790c5-118">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
