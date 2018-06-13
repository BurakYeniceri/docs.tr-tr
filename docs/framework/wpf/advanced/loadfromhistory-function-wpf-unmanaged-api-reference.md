---
title: LoadFromHistory işlevi (WPF yönetilmeyen API Başvurusu)
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- LoadFromHistory
api_location:
- PresentationHost_v0400.dll
ms.assetid: d037c062-a911-4949-b251-ccd3e48b1d17
ms.openlocfilehash: 19674b45af84e1e6a6ca169f7b6654c6e3847416
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33544670"
---
# <a name="loadfromhistory-function-wpf-unmanaged-api-reference"></a><span data-ttu-id="12ae1-102">LoadFromHistory işlevi (WPF yönetilmeyen API Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="12ae1-102">LoadFromHistory Function (WPF Unmanaged API Reference)</span></span>
<span data-ttu-id="12ae1-103">Bu API Windows Presentation Foundation (WPF) altyapısını destekler ve doğrudan kodunuzdan kullanılmaya yönelik değildir.</span><span class="sxs-lookup"><span data-stu-id="12ae1-103">This API supports the Windows Presentation Foundation (WPF) infrastructure and is not intended to be used directly from your code.</span></span>  
  
 <span data-ttu-id="12ae1-104">Windows Presentation Foundation (WPF) altyapısı tarafından windows yönetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12ae1-104">Used by the Windows Presentation Foundation (WPF) infrastructure for windows management.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12ae1-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="12ae1-105">Syntax</span></span>  
  
```cpp  
HRESULT LoadFromHistory_export(  
        IStream* pHistoryStream,   
        IBindCtx* pBindCtx  
)  
```  
  
#### <a name="parameters"></a><span data-ttu-id="12ae1-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="12ae1-106">Parameters</span></span>  
 <span data-ttu-id="12ae1-107">pHistoryStream</span><span class="sxs-lookup"><span data-stu-id="12ae1-107">pHistoryStream</span></span>  
 <span data-ttu-id="12ae1-108">Bir işaretçi bir akışa geçmiş bilgileri.</span><span class="sxs-lookup"><span data-stu-id="12ae1-108">A pointer to a stream of history information.</span></span>  
  
 <span data-ttu-id="12ae1-109">pBindCtx</span><span class="sxs-lookup"><span data-stu-id="12ae1-109">pBindCtx</span></span>  
 <span data-ttu-id="12ae1-110">Bir bağlama bağlamı için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="12ae1-110">A pointer to a bind context.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12ae1-111">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="12ae1-111">Requirements</span></span>  
 <span data-ttu-id="12ae1-112">**Platformlar:** bkz [.NET Framework sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12ae1-112">**Platforms:** See [.NET Framework System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12ae1-113">**DLL:**</span><span class="sxs-lookup"><span data-stu-id="12ae1-113">**DLL:**</span></span>  
  
 <span data-ttu-id="12ae1-114">.NET Framework 3.0 ve 3.5: PresentationHostDLL.dll</span><span class="sxs-lookup"><span data-stu-id="12ae1-114">In the .NET Framework 3.0 and 3.5: PresentationHostDLL.dll</span></span>  
  
 <span data-ttu-id="12ae1-115">.NET Framework 4 ve üzeri: PresentationHost_v0400.dll</span><span class="sxs-lookup"><span data-stu-id="12ae1-115">In the .NET Framework 4 and later: PresentationHost_v0400.dll</span></span>  
  
 <span data-ttu-id="12ae1-116">**.NET framework sürüm:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="12ae1-116">**.NET Framework Version:** [!INCLUDE[net_current_v30plus](../../../../includes/net-current-v30plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12ae1-117">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="12ae1-117">See Also</span></span>  
 [<span data-ttu-id="12ae1-118">WPF Yönetilmeyen API Başvurusu</span><span class="sxs-lookup"><span data-stu-id="12ae1-118">WPF Unmanaged API Reference</span></span>](../../../../docs/framework/wpf/advanced/wpf-unmanaged-api-reference.md)
