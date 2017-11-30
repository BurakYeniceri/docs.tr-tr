---
title: "VerifyClientKey işlevi (yönetilmeyen API Başvurusu)"
description: "Doğru güvenlik istemci anahtara sahip VerifyClientKey işlevi sağlar."
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: VerifyClientKey
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: VerifyClientKey
helpviewer_keywords: VerifyClientKey function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: cce10e3dd5536a85b4dee62cc7f6e9e8e73929cb
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2017
---
# <a name="verifyclientkey-function"></a><span data-ttu-id="8fff6-103">VerifyClientKey işlevi</span><span class="sxs-lookup"><span data-stu-id="8fff6-103">VerifyClientKey function</span></span>
<span data-ttu-id="8fff6-104">İstemci anahtar doğru güvenlik sahip olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="8fff6-104">Ensures that the client key has the correct security.</span></span>  
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="8fff6-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8fff6-105">Syntax</span></span>  
  
```  
LONG VerifyClientKey(); 
```  

## <a name="return-value"></a><span data-ttu-id="8fff6-106">Dönüş değeri</span><span class="sxs-lookup"><span data-stu-id="8fff6-106">Return value</span></span>

<span data-ttu-id="8fff6-107">İşlev başarılı olursa, dönüş değeri olan `ERROR_SUCCESS` (0).</span><span class="sxs-lookup"><span data-stu-id="8fff6-107">If the function succeeds, the return value is `ERROR_SUCCESS` (0).</span></span>

<span data-ttu-id="8fff6-108">İşlev başarısız olursa, dönüş değeri tanımlanan bir sıfır olmayan bir hata kodu *Winerror.h'de*.</span><span class="sxs-lookup"><span data-stu-id="8fff6-108">If the function fails, the return value is a non-zero error code defined in *WinError.h*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fff6-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="8fff6-109">Requirements</span></span>  
 <span data-ttu-id="8fff6-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8fff6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8fff6-111">**Başlık:** WMINet_Utils.def</span><span class="sxs-lookup"><span data-stu-id="8fff6-111">**Header:** WMINet_Utils.def</span></span>  
  
 <span data-ttu-id="8fff6-112">**.NET framework sürümleri:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="8fff6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fff6-113">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="8fff6-113">See also</span></span>  
[<span data-ttu-id="8fff6-114">WMI ve performans sayaçları (yönetilmeyen API Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="8fff6-114">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)