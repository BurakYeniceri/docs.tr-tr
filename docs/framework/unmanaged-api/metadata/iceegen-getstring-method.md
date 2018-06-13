---
title: ICeeGen::GetString Metodu
ms.date: 03/30/2017
api_name:
- ICeeGen.GetString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetString
helpviewer_keywords:
- ICeeGen::GetString method [.NET Framework metadata]
- GetString method, ICeeGen interface [.NET Framework metadata]
ms.assetid: 7cc22562-128c-440a-9147-55ff20f173d7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f7ac5ef95ca3705b11cfda51d7fd1aca7400abc4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443079"
---
# <a name="iceegengetstring-method"></a><span data-ttu-id="43c37-102">ICeeGen::GetString Metodu</span><span class="sxs-lookup"><span data-stu-id="43c37-102">ICeeGen::GetString Method</span></span>
<span data-ttu-id="43c37-103">Belirtilen göreli sanal adresinde depolanan dizesini alır.</span><span class="sxs-lookup"><span data-stu-id="43c37-103">Gets the string stored at the specified relative virtual address.</span></span>  
  
 <span data-ttu-id="43c37-104">Bu yöntem artık kullanılmıyor ve kullanılmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="43c37-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="43c37-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="43c37-105">Syntax</span></span>  
  
```  
HRESULT GetString (  
    [in]  ULONG      RVA,   
    [out] LPWSTR     *lpString  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="43c37-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="43c37-106">Parameters</span></span>  
 `RVA`  
 <span data-ttu-id="43c37-107">[in] Döndürülecek dizesinin göreli sanal adres.</span><span class="sxs-lookup"><span data-stu-id="43c37-107">[in] The relative virtual address of the string to return.</span></span>  
  
 `lpString`  
 <span data-ttu-id="43c37-108">[out] Döndürülen dize.</span><span class="sxs-lookup"><span data-stu-id="43c37-108">[out] The returned string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="43c37-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="43c37-109">Requirements</span></span>  
 <span data-ttu-id="43c37-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="43c37-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43c37-111">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="43c37-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="43c37-112">**Kitaplığı:** MsCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="43c37-112">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="43c37-113">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43c37-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43c37-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="43c37-114">See Also</span></span>  
 [<span data-ttu-id="43c37-115">ICeeGen Arabirimi</span><span class="sxs-lookup"><span data-stu-id="43c37-115">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
