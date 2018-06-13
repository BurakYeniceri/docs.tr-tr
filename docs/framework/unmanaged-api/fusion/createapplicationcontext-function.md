---
title: CreateApplicationContext İşlevi
ms.date: 03/30/2017
api_name:
- CreateApplicationContext
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateApplicationContext
helpviewer_keywords:
- CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 80012d030d0ea51ab3d150a7fd346b78e29dbde5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430106"
---
# <a name="createapplicationcontext-function"></a><span data-ttu-id="ef1b4-102">CreateApplicationContext İşlevi</span><span class="sxs-lookup"><span data-stu-id="ef1b4-102">CreateApplicationContext Function</span></span>
<span data-ttu-id="ef1b4-103">Bu işlev .NET Framework altyapısını destekler ve doğrudan kodunuzdan kullanılmaya yönelik değildir.</span><span class="sxs-lookup"><span data-stu-id="ef1b4-103">This function supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ef1b4-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ef1b4-104">Syntax</span></span>  
  
```  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ef1b4-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="ef1b4-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="ef1b4-106">[in] Bir kolay ad için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="ef1b4-106">[in] A pointer to a friendly name.</span></span>  
  
 `ppCtx`  
 <span data-ttu-id="ef1b4-107">[out] Uygulama bağlamı için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="ef1b4-107">[out] A pointer to an application context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ef1b4-108">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="ef1b4-108">Requirements</span></span>  
 <span data-ttu-id="ef1b4-109">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ef1b4-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ef1b4-110">**Başlık:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="ef1b4-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="ef1b4-111">**Kitaplığı:** bir kaynak olarak Fusion.dll dahil</span><span class="sxs-lookup"><span data-stu-id="ef1b4-111">**Library:** Included as a resource in Fusion.dll</span></span>  
  
 <span data-ttu-id="ef1b4-112">**.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef1b4-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef1b4-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ef1b4-113">See Also</span></span>  
 [<span data-ttu-id="ef1b4-114">IAssemblyCache Arabirimi</span><span class="sxs-lookup"><span data-stu-id="ef1b4-114">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)  
 [<span data-ttu-id="ef1b4-115">Fusion Genel Statik İşlevleri</span><span class="sxs-lookup"><span data-stu-id="ef1b4-115">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)  
 [<span data-ttu-id="ef1b4-116">Genel Derleme Önbelleği</span><span class="sxs-lookup"><span data-stu-id="ef1b4-116">Global Assembly Cache</span></span>](../../../../docs/framework/app-domains/gac.md)
