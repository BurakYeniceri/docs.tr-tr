---
title: IMetaDataValidate::ValidatorInit Yöntemi
ms.date: 03/30/2017
api_name:
- IMetaDataValidate.ValidatorInit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataValidate::ValidatorInit
helpviewer_keywords:
- IMetaDataValidate::ValidatorInit method [.NET Framework metadata]
- ValidatorInit method [.NET Framework metadata]
ms.assetid: 6bafd75a-e2d0-4aea-aed1-074374d5dff6
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 053c94bc540b130510f155506b6fad32f032a475
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33449552"
---
# <a name="imetadatavalidatevalidatorinit-method"></a><span data-ttu-id="e65d9-102">IMetaDataValidate::ValidatorInit Yöntemi</span><span class="sxs-lookup"><span data-stu-id="e65d9-102">IMetaDataValidate::ValidatorInit Method</span></span>
<span data-ttu-id="e65d9-103">Modül türü geçerli meta veri kapsamda belirtir ve doğrulama hataları için belirtilen geri çağırma yöntemi kaydeden bir bayrak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e65d9-103">Sets a flag that specifies the type of the module in the current metadata scope, and registers the specified callback method for validation errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e65d9-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e65d9-104">Syntax</span></span>  
  
```  
HRESULT ValidatorInit (  
   [in] DWORD       dwModuleType,  
   [in] IUnknown    *pUnk  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e65d9-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="e65d9-105">Parameters</span></span>  
 `dwModule`  
 <span data-ttu-id="e65d9-106">[in] Değerini [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) modül türü geçerli meta veri kapsamda belirtir numaralandırması.</span><span class="sxs-lookup"><span data-stu-id="e65d9-106">[in] A value of the [CorValidatorModuleType](../../../../docs/framework/unmanaged-api/metadata/corvalidatormoduletype-enumeration.md) enumeration that specifies the type of the module in the current metadata scope.</span></span>  
  
 `pUnk`  
 <span data-ttu-id="e65d9-107">[in] Bir işaretçi bir <<!--zzxref:IUnknown --> `IUnknown`> Doğrulama hataları için işlevi geri görevi gören örneği.</span><span class="sxs-lookup"><span data-stu-id="e65d9-107">[in] A pointer to an <<!--zzxref:IUnknown --> `IUnknown`> instance that serves as a function callback for validation errors.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e65d9-108">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="e65d9-108">Requirements</span></span>  
 <span data-ttu-id="e65d9-109">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e65d9-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e65d9-110">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e65d9-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e65d9-111">**Kitaplığı:** MsCorEE.dll kaynak olarak kullanılır</span><span class="sxs-lookup"><span data-stu-id="e65d9-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e65d9-112">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e65d9-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e65d9-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="e65d9-113">See Also</span></span>  
 [<span data-ttu-id="e65d9-114">IMetaDataValidate Arabirimi</span><span class="sxs-lookup"><span data-stu-id="e65d9-114">IMetaDataValidate Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatavalidate-interface.md)
