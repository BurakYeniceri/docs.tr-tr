---
title: IEnumDefinitionIdentity Arabirimi
ms.date: 03/30/2017
api_name:
- IEnumDefinitionIdentity
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IEnumDefinitionIdentity
helpviewer_keywords:
- IEnumDefinitionIdentity interface [.NET Framework fusion]
ms.assetid: 8263e75d-251b-4abc-8a1a-c62884142232
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 34186ee8825c0981ec095cf855c76ff5f800907d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432360"
---
# <a name="ienumdefinitionidentity-interface"></a><span data-ttu-id="859f8-102">IEnumDefinitionIdentity Arabirimi</span><span class="sxs-lookup"><span data-stu-id="859f8-102">IEnumDefinitionIdentity Interface</span></span>
<span data-ttu-id="859f8-103">Koleksiyonu için Numaralandırıcı görevi gören `IDefinitionIdentity` nesneleri.</span><span class="sxs-lookup"><span data-stu-id="859f8-103">Serves as the enumerator for a collection of `IDefinitionIdentity` objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="859f8-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="859f8-104">Syntax</span></span>  
  
```  
IEnumDefinitionIdentity : IUnknown {  
  
    HRESULT Clone (  
        [out] IEnumDefinitionIdentity **ppIEnumDefinitionIdentity  
    );  
  
    HRESULT Next (  
        [in]  ULONG               celt,  
        [out, length_is(celt), size_is(*pceltWritten)]  
              IDefinitionIdentity *rgpIDefinitionIdentity[],  
        [out] ULONG               *pceltWritten  
    );  
  
    HRESULT Reset ();  
  
    HRESULT Skip (  
        [in] ULONG celt  
    );  
  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="859f8-105">Yöntemler</span><span class="sxs-lookup"><span data-stu-id="859f8-105">Methods</span></span>  
  
|<span data-ttu-id="859f8-106">Yöntem</span><span class="sxs-lookup"><span data-stu-id="859f8-106">Method</span></span>|<span data-ttu-id="859f8-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="859f8-107">Description</span></span>|  
|------------|-----------------|  
|`IEnumDefinitionIdentity::Clone`|<span data-ttu-id="859f8-108">Arabirim işaretçisi yeni bir alır `IEnumDefinitionIdentity` bu aynı üyeleri içeren nesne `IEnumDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="859f8-108">Gets an interface pointer to a new `IEnumDefinitionIdentity` object that contains the same members as this `IEnumDefinitionIdentity`.</span></span>|  
|`IEnumDefinitionIdentity::Next`|<span data-ttu-id="859f8-109">Belirtilen sayıda alır `IDefinitionIdentity` geçerli konumdan başlayarak nesneleri.</span><span class="sxs-lookup"><span data-stu-id="859f8-109">Gets the specified number of `IDefinitionIdentity` objects, starting at the current position.</span></span>|  
|`IEnumDefinitionIdentity::Reset`|<span data-ttu-id="859f8-110">Yönerge işaretçisi başlangıcına bu taşır `IEnumDefinitionIdentity`.</span><span class="sxs-lookup"><span data-stu-id="859f8-110">Moves the instruction pointer to the beginning of this `IEnumDefinitionIdentity`.</span></span>|  
|`IEnumDefinitionIdentity::Skip`|<span data-ttu-id="859f8-111">Öğeler, geçerli konumdan başlayarak belirtilen sayıda tarafından yönerge işaretçisi İleri taşınır.</span><span class="sxs-lookup"><span data-stu-id="859f8-111">Moves the instruction pointer forward by the specified number of elements, starting at the current position.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="859f8-112">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="859f8-112">Requirements</span></span>  
 <span data-ttu-id="859f8-113">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="859f8-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="859f8-114">**Başlık:** Isolation.h</span><span class="sxs-lookup"><span data-stu-id="859f8-114">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="859f8-115">**.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="859f8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="859f8-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="859f8-116">See Also</span></span>  
 [<span data-ttu-id="859f8-117">Fusion Arabirimleri</span><span class="sxs-lookup"><span data-stu-id="859f8-117">Fusion Interfaces</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-interfaces.md)  
 [<span data-ttu-id="859f8-118">IDefinitionIdentity Arabirimi</span><span class="sxs-lookup"><span data-stu-id="859f8-118">IDefinitionIdentity Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/idefinitionidentity-interface.md)
