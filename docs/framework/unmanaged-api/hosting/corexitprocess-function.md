---
title: CorExitProcess İşlevi
ms.date: 03/30/2017
api_name:
- CorExitProcess
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- CorExitProcess
helpviewer_keywords:
- CorExitProcess function [.NET Framework hosting]
ms.assetid: a5cab4c6-990e-47f3-8798-cf422b791015
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d3e7f3208d7ac84645fa4c7ad7e0b71f6a0d3d3d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429335"
---
# <a name="corexitprocess-function"></a><span data-ttu-id="198ba-102">CorExitProcess İşlevi</span><span class="sxs-lookup"><span data-stu-id="198ba-102">CorExitProcess Function</span></span>
<span data-ttu-id="198ba-103">Geçerli yönetilmeyen işlemi kapatır.</span><span class="sxs-lookup"><span data-stu-id="198ba-103">Shuts down the current unmanaged process.</span></span>  
  
 <span data-ttu-id="198ba-104">Bu işlev kaldırılmamıştır [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="198ba-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="198ba-105">Kullanım [Iclrmetahost::exitprocess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) yöntemi yerine.</span><span class="sxs-lookup"><span data-stu-id="198ba-105">Use the [ICLRMetaHost::ExitProcess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="198ba-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="198ba-106">Syntax</span></span>  
  
```  
void STDMETHODCALLTYPE CorExitProcess (   
  int  exitCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="198ba-107">Parametreler</span><span class="sxs-lookup"><span data-stu-id="198ba-107">Parameters</span></span>  
 `exitCode`  
 <span data-ttu-id="198ba-108">İşlem çıkış kodu belirten bir tamsayı.</span><span class="sxs-lookup"><span data-stu-id="198ba-108">An integer that specifies the process exit code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="198ba-109">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="198ba-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="198ba-110">İle başlayarak [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` işleminde, yalnızca, eski API bağlı çalışma zamanı başlatılan her çalışma zamanı çıkar.</span><span class="sxs-lookup"><span data-stu-id="198ba-110">Beginning with the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` exits every started runtime in the process, not just the runtime to which the legacy APIs have been bound.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="198ba-111">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="198ba-111">Requirements</span></span>  
 <span data-ttu-id="198ba-112">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="198ba-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="198ba-113">**Başlık:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="198ba-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="198ba-114">**Kitaplığı:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="198ba-114">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="198ba-115">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="198ba-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="198ba-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="198ba-116">See Also</span></span>  
 [<span data-ttu-id="198ba-117">Kullanım Dışı CLR Barındırma İşlevleri</span><span class="sxs-lookup"><span data-stu-id="198ba-117">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
