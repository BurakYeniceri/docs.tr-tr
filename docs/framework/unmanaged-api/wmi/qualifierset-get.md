---
title: "QualifierSet_Get işlevi (yönetilmeyen API Başvurusu)"
description: "QualifierSet_Get işlevi bir adlandırılmış niteleyici alır."
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: QualifierSet_Get
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: QualifierSet_Get
helpviewer_keywords: QualifierSet_Get function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: aaf5de5b8e16ee2f96c7bc29dbb09f93298dd185
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2017
---
# <a name="qualifiersetget-function"></a><span data-ttu-id="91503-103">QualifierSet_Get işlevi</span><span class="sxs-lookup"><span data-stu-id="91503-103">QualifierSet_Get function</span></span>
<span data-ttu-id="91503-104">Belirtilen adlandırılmış niteleyici alır.</span><span class="sxs-lookup"><span data-stu-id="91503-104">Gets the specified named qualifier.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="91503-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="91503-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Get (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LPCWSTR              wszName,
   [in] LONG                 lFlags,
   [out] VARIANT*            pVal,
   [out] LONG*               plFlavor                 
); 
```  

## <a name="parameters"></a><span data-ttu-id="91503-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="91503-106">Parameters</span></span>

`vFunc`   
<span data-ttu-id="91503-107">[in] Bu parametre kullanılmıyor.</span><span class="sxs-lookup"><span data-stu-id="91503-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="91503-108">[in] Bir işaretçi bir [IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) örneği.</span><span class="sxs-lookup"><span data-stu-id="91503-108">[in] A pointer to an [IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) instance.</span></span>

`wszName`   
<span data-ttu-id="91503-109">[in] Değeri istenen Niteleyici adı.</span><span class="sxs-lookup"><span data-stu-id="91503-109">[in] The name of the qualifier whose value is requested.</span></span>

`lFlags`   
<span data-ttu-id="91503-110">[in] Ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="91503-110">[in] Reserved.</span></span> <span data-ttu-id="91503-111">Bu parametre 0 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="91503-111">This parameter must be 0.</span></span>

`pVal`   
<span data-ttu-id="91503-112">[out] Başarılı olduğunda, doğru türü ve değerine Niteleyici için.</span><span class="sxs-lookup"><span data-stu-id="91503-112">[out] When successful, the correct type and value for the qualifier.</span></span> <span data-ttu-id="91503-113">İşlev başarısız olursa, `VARIANT` gösterdiği `pVal` değiştirilmez.</span><span class="sxs-lookup"><span data-stu-id="91503-113">If the function fails, the `VARIANT` pointed to by `pVal` is not modified.</span></span> <span data-ttu-id="91503-114">Bu parametre ise `null`, parametre yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="91503-114">If this parameter is `null`, the parameter is ignored.</span></span>

`plFlavor`   
<span data-ttu-id="91503-115">[out] İstenen niteleyici niteleyici türü BITS alan uzun bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="91503-115">[out] A pointer to a LONG that receives the qualifier flavor bits for the requested qualifier.</span></span> <span data-ttu-id="91503-116">Özellik bilgileri değil istenirse, bu parametre olabilir `null`.</span><span class="sxs-lookup"><span data-stu-id="91503-116">If flavor information is not desired, this parameter can be `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="91503-117">Dönüş değeri</span><span class="sxs-lookup"><span data-stu-id="91503-117">Return value</span></span>

<span data-ttu-id="91503-118">Bu işlev tarafından döndürülen aşağıdaki değerleri tanımlanan *WbemCli.h* üstbilgi dosyası, veya tanımlayabilirsiniz bunları sabitleri kodunuzda:</span><span class="sxs-lookup"><span data-stu-id="91503-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="91503-119">Sabit</span><span class="sxs-lookup"><span data-stu-id="91503-119">Constant</span></span>  |<span data-ttu-id="91503-120">Değer</span><span class="sxs-lookup"><span data-stu-id="91503-120">Value</span></span>  |<span data-ttu-id="91503-121">Açıklama</span><span class="sxs-lookup"><span data-stu-id="91503-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="91503-122">0x80041008</span><span class="sxs-lookup"><span data-stu-id="91503-122">0x80041008</span></span> | <span data-ttu-id="91503-123">Parametre geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="91503-123">A parameter is not valid.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="91503-124">0x80041002</span><span class="sxs-lookup"><span data-stu-id="91503-124">0x80041002</span></span> | <span data-ttu-id="91503-125">Belirtilen niteleyicisi yok.</span><span class="sxs-lookup"><span data-stu-id="91503-125">The specified qualifier does not exist.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="91503-126">0</span><span class="sxs-lookup"><span data-stu-id="91503-126">0</span></span> | <span data-ttu-id="91503-127">İşlev çağrısı başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="91503-127">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="91503-128">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="91503-128">Remarks</span></span>

<span data-ttu-id="91503-129">Bu işlev çağrısı sarmalar [IWbemQualifierSet::Get](https://msdn.microsoft.com/library/aa391867(v=vs.85).aspx) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="91503-129">This function wraps a call to the [IWbemQualifierSet::Get](https://msdn.microsoft.com/library/aa391867(v=vs.85).aspx) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91503-130">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="91503-130">Requirements</span></span>  
 <span data-ttu-id="91503-131">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="91503-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91503-132">**Başlık:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="91503-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="91503-133">**.NET framework sürümleri:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="91503-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="91503-134">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="91503-134">See also</span></span>  
[<span data-ttu-id="91503-135">WMI ve performans sayaçları (yönetilmeyen API Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="91503-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
