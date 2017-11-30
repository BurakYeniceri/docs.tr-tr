---
title: ICLRDataTarget::GetMachineType Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDataTarget.GetMachineType
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICLRDataTarget::GetMachineType
helpviewer_keywords:
- ICLRDataTarget::GetMachineType method [.NET Framework debugging]
- GetMachineType method [.NET Framework debugging]
ms.assetid: 5f1f9c61-3e3b-48b2-b111-a4395f7623a7
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8cd3a71d150011a1a5b9ad84c4687aac6346eb6f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="iclrdatatargetgetmachinetype-method"></a><span data-ttu-id="3177a-102">ICLRDataTarget::GetMachineType Metodu</span><span class="sxs-lookup"><span data-stu-id="3177a-102">ICLRDataTarget::GetMachineType Method</span></span>
<span data-ttu-id="3177a-103">Tanımlayıcı için hedef işlem kullanarak yönerge kümesi türünü alır.</span><span class="sxs-lookup"><span data-stu-id="3177a-103">Gets the identifier for the kind of instruction set that the target process is using.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3177a-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="3177a-104">Syntax</span></span>  
  
```  
HRESULT GetMachineType (  
    [out] ULONG32     *machineType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3177a-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="3177a-105">Parameters</span></span>  
 `machineType`  
 <span data-ttu-id="3177a-106">[out] Hedef işlem kümesi talimat belirten bir değer için bir işaretçi kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="3177a-106">[out] A pointer to a value that indicates the instruction set that the target process is using.</span></span> <span data-ttu-id="3177a-107">Döndürülen `machineType` WinNT.h üstbilgi dosyasında tanımlanan IMAGE_FILE_MACHINE sabitleri biridir.</span><span class="sxs-lookup"><span data-stu-id="3177a-107">The returned `machineType` is one of the IMAGE_FILE_MACHINE constants, which are defined in the WinNT.h header file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3177a-108">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="3177a-108">Requirements</span></span>  
 <span data-ttu-id="3177a-109">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3177a-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3177a-110">**Başlık:** ClrData.idl, ClrData.h</span><span class="sxs-lookup"><span data-stu-id="3177a-110">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="3177a-111">**Kitaplığı:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3177a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3177a-112">**.NET framework sürümleri:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3177a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3177a-113">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="3177a-113">See Also</span></span>  
 [<span data-ttu-id="3177a-114">Iclrdatatarget arabirimi</span><span class="sxs-lookup"><span data-stu-id="3177a-114">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
