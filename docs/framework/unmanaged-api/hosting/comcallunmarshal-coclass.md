---
title: ComCallUnmarshal Coclass’ı
ms.date: 03/30/2017
api_name:
- ComCallUnmarshal Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ComCallUnmarshal
helpviewer_keywords:
- ComCallUnmarshal coclass [.NET Framework hosting]
ms.assetid: 2adb5827-2268-4914-a1c6-f62b61880a45
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7884d53630ca13a30d7b4efd55d46684a9dd7d30
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427648"
---
# <a name="comcallunmarshal-coclass"></a><span data-ttu-id="a338e-102">ComCallUnmarshal Coclass’ı</span><span class="sxs-lookup"><span data-stu-id="a338e-102">ComCallUnmarshal Coclass</span></span>
<span data-ttu-id="a338e-103">Arabirim İşaretçileri hazırlama yönetmek için arabirim sağlar.</span><span class="sxs-lookup"><span data-stu-id="a338e-103">Provides interfaces for managing the marshaling of interface pointers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a338e-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a338e-104">Syntax</span></span>  
  
```  
coclass ComCallUnmarshal {  
    [default] interface IMarshal;  
};  
```  
  
## <a name="interfaces"></a><span data-ttu-id="a338e-105">Arabirimler</span><span class="sxs-lookup"><span data-stu-id="a338e-105">Interfaces</span></span>  
  
|<span data-ttu-id="a338e-106">Arabirim</span><span class="sxs-lookup"><span data-stu-id="a338e-106">Interface</span></span>|<span data-ttu-id="a338e-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="a338e-107">Description</span></span>|  
|---------------|-----------------|  
|`IMarshal`|<span data-ttu-id="a338e-108">Oluşturma, başlatma ve bir istemci işlemi proxy yönetme için yöntemleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="a338e-108">Provides methods for creating, initializing, and managing a proxy in a client process.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="a338e-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="a338e-109">Requirements</span></span>  
 <span data-ttu-id="a338e-110">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a338e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a338e-111">**Başlık:** MSCorEE.idl</span><span class="sxs-lookup"><span data-stu-id="a338e-111">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="a338e-112">**Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="a338e-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a338e-113">**.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a338e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a338e-114">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a338e-114">See Also</span></span>  
 [<span data-ttu-id="a338e-115">Barındırma Coclassları</span><span class="sxs-lookup"><span data-stu-id="a338e-115">Hosting Coclasses</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-coclasses.md)
