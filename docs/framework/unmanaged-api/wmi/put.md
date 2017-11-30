---
title: "PUT işlevi (yönetilmeyen API Başvurusu)"
description: "Put işlevi adlı bir özellik için yeni bir değer atar."
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: Put
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: Put
helpviewer_keywords: Put function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6c4ad979a3a662618ab62b52d63bda3dbb1e71b9
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2017
---
# <a name="put-function"></a><span data-ttu-id="50a10-103">PUT işlevi</span><span class="sxs-lookup"><span data-stu-id="50a10-103">Put function</span></span>
<span data-ttu-id="50a10-104">Adlandırılmış bir özelliği için yeni bir değer ayarlar.</span><span class="sxs-lookup"><span data-stu-id="50a10-104">Sets a named property to a new value.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a><span data-ttu-id="50a10-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="50a10-105">Syntax</span></span>  
  
```  
HRESULT Put (
   [in] int               vFunc, 
   [in] IWbemClassObject* ptr, 
   [in] LPCWSTR           wszName,
   [in] LONG              lFlags,
   [in] VARIANT*          pVal,
   [in] CIMTYPE           vtType
); 
```  

## <a name="parameters"></a><span data-ttu-id="50a10-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="50a10-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="50a10-107">[in] Bu parametre kullanılmıyor.</span><span class="sxs-lookup"><span data-stu-id="50a10-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="50a10-108">[in] Bir işaretçi bir [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) örneği.</span><span class="sxs-lookup"><span data-stu-id="50a10-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>

`wszName`  
<span data-ttu-id="50a10-109">[in] Özelliğin adı.</span><span class="sxs-lookup"><span data-stu-id="50a10-109">[in] The name of the property.</span></span> <span data-ttu-id="50a10-110">Bu parametre olamaz `null`.</span><span class="sxs-lookup"><span data-stu-id="50a10-110">This parameter cannot be `null`.</span></span>

`lFlags`  
<span data-ttu-id="50a10-111">[in] Ayrılmış.</span><span class="sxs-lookup"><span data-stu-id="50a10-111">[in] Reserved.</span></span> <span data-ttu-id="50a10-112">Bu parametre 0 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="50a10-112">This parameter must be 0.</span></span>

`pVal`   
<span data-ttu-id="50a10-113">[in] Geçerli bir işaretçi `VARIANT` yeni özellik değeri olur.</span><span class="sxs-lookup"><span data-stu-id="50a10-113">[in] A pointer to a valid `VARIANT` that becomes the new property value.</span></span> <span data-ttu-id="50a10-114">Varsa `pVal` olan `null` veya işaret eden bir `VARIANT` türü `VT_NULL`, özellik kümesine `null`.</span><span class="sxs-lookup"><span data-stu-id="50a10-114">If `pVal` is `null` or points to a `VARIANT` of type `VT_NULL`, the property is set to `null`.</span></span> 

`vtType`  
<span data-ttu-id="50a10-115">[in] Türü `VARIANT` gösterdiği `pVal`.</span><span class="sxs-lookup"><span data-stu-id="50a10-115">[in] The type of `VARIANT` pointed to by `pVal`.</span></span> <span data-ttu-id="50a10-116">Bkz: [açıklamalar](#remarks) daha fazla bilgi için bölüm.</span><span class="sxs-lookup"><span data-stu-id="50a10-116">See the [Remarks](#remarks) section for more information.</span></span>
 

## <a name="return-value"></a><span data-ttu-id="50a10-117">Dönüş değeri</span><span class="sxs-lookup"><span data-stu-id="50a10-117">Return value</span></span>

<span data-ttu-id="50a10-118">Bu işlev tarafından döndürülen aşağıdaki değerleri tanımlanan *WbemCli.h* üstbilgi dosyası, veya tanımlayabilirsiniz bunları sabitleri kodunuzda:</span><span class="sxs-lookup"><span data-stu-id="50a10-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="50a10-119">Sabit</span><span class="sxs-lookup"><span data-stu-id="50a10-119">Constant</span></span>  |<span data-ttu-id="50a10-120">Değer</span><span class="sxs-lookup"><span data-stu-id="50a10-120">Value</span></span>  |<span data-ttu-id="50a10-121">Açıklama</span><span class="sxs-lookup"><span data-stu-id="50a10-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_FAILED` | <span data-ttu-id="50a10-122">0x80041001</span><span class="sxs-lookup"><span data-stu-id="50a10-122">0x80041001</span></span> | <span data-ttu-id="50a10-123">Genel bir hata oluştu.</span><span class="sxs-lookup"><span data-stu-id="50a10-123">There has been a general failure.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="50a10-124">0x80041008</span><span class="sxs-lookup"><span data-stu-id="50a10-124">0x80041008</span></span> | <span data-ttu-id="50a10-125">Bir veya daha fazla parametre geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="50a10-125">One or more parameters are not valid.</span></span> |
|`WBEM_E_INVALID_PROPERTY_TYPE` | <span data-ttu-id="50a10-126">0x8004102a</span><span class="sxs-lookup"><span data-stu-id="50a10-126">0x8004102a</span></span> | <span data-ttu-id="50a10-127">Özellik türü tanınmıyor.</span><span class="sxs-lookup"><span data-stu-id="50a10-127">The property type is not recognized.</span></span> <span data-ttu-id="50a10-128">Bu değer, sınıf zaten varsa sınıf örnekleri oluşturulurken döndürülür.</span><span class="sxs-lookup"><span data-stu-id="50a10-128">This value is returned when creating class instances if the class already exists.</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="50a10-129">0x80041006</span><span class="sxs-lookup"><span data-stu-id="50a10-129">0x80041006</span></span> | <span data-ttu-id="50a10-130">İşlemi tamamlamak yeterli bellek yok.</span><span class="sxs-lookup"><span data-stu-id="50a10-130">Not enough memory is available to complete the operation.</span></span> |
| `WBEM_E_TYPE_MISMATCH` | <span data-ttu-id="50a10-131">0x80041005</span><span class="sxs-lookup"><span data-stu-id="50a10-131">0x80041005</span></span> | <span data-ttu-id="50a10-132">İçin örnekleri: belirten `pVal` işaret eden bir `VARIANT` özelliği için yanlış bir türde.</span><span class="sxs-lookup"><span data-stu-id="50a10-132">For instances: Indicates that `pVal` points to a `VARIANT` of an incorrect type for the property.</span></span> <br/> <span data-ttu-id="50a10-133">Sınıf tanımları için: üst sınıfta bir özellik zaten var ve yeni COM türü eski COM türünden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="50a10-133">For class definitions: The property already exists in the parent class, and the new COM type is different from the old COM type.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="50a10-134">0</span><span class="sxs-lookup"><span data-stu-id="50a10-134">0</span></span> | <span data-ttu-id="50a10-135">İşlev çağrısı başarısız oldu.</span><span class="sxs-lookup"><span data-stu-id="50a10-135">The function call was successful.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="50a10-136">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="50a10-136">Remarks</span></span>

<span data-ttu-id="50a10-137">Bu işlev çağrısı sarmalar [IWbemClassObject::Put](https://msdn.microsoft.com/library/aa391455(v=vs.85).aspx) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="50a10-137">This function wraps a call to the [IWbemClassObject::Put](https://msdn.microsoft.com/library/aa391455(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="50a10-138">Bu işlev her zaman geçerli özellik değeri ile yeni bir tane üzerine yazar.</span><span class="sxs-lookup"><span data-stu-id="50a10-138">This function always overwrites the current property value with a new one.</span></span> <span data-ttu-id="50a10-139">Varsa [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) işaret eden bir sınıf tanımına `Put` oluşturur veya özellik değeri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="50a10-139">If the [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) points to a class definition, `Put` creates or updates the property value.</span></span> <span data-ttu-id="50a10-140">Zaman [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) işaret eden bir CIM örneğine `Put` özellik değeri yalnızca; güncelleştirir `Put` bir özellik değeri oluşturulamıyor.</span><span class="sxs-lookup"><span data-stu-id="50a10-140">When [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) points to a CIM instance, `Put` updates the property value only; `Put` cannot create a property value.</span></span>

<span data-ttu-id="50a10-141">`__CLASS` Sistem özelliği olduğunda yalnızca yazılabilir sınıfı oluşturma sırasında bunu boş bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="50a10-141">The `__CLASS` system property is only writable during class creation, when it may not be left blank.</span></span> <span data-ttu-id="50a10-142">Diğer tüm sistem özellikleri salt okunurdur.</span><span class="sxs-lookup"><span data-stu-id="50a10-142">All other system properties are read-only.</span></span>

<span data-ttu-id="50a10-143">Kullanıcı özellikleri başlayamaz veya bitemez bir alt çizgi ("_") adlarla oluşturulamıyor.</span><span class="sxs-lookup"><span data-stu-id="50a10-143">A user cannot create properties with names that begin or end with an underscore ("_").</span></span> <span data-ttu-id="50a10-144">Bu, sistem sınıfları ve özellikleri için ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="50a10-144">This is reserved for system classes and properties.</span></span>

<span data-ttu-id="50a10-145">Özelliği ayarlarsanız `Put` üst sınıfında exists işlevi, özellik türü üst sınıf türü eşleşmiyor sürece özelliğinin varsayılan değeri değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="50a10-145">If the property set by the `Put` function exists in the parent class, the default value of the property is changed unless the property type does not match the parent class type.</span></span> <span data-ttu-id="50a10-146">Özelliği yok ve tür uyuşmazlığı değilse ceated özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="50a10-146">If the property does not exist and it is not a type mismatch, the property is ceated.</span></span>

<span data-ttu-id="50a10-147">Kullanım `vtType` yalnızca yeni özellikleri bir CIM sınıfı tanımında oluşturulurken parametre ve `pVal` olan `null` veya işaret eden bir `VARIANT` türü `VT_NULL`.</span><span class="sxs-lookup"><span data-stu-id="50a10-147">Use the `vtType` parameter only when creating new properties in a CIM class definition and `pVal` is `null` or points to a `VARIANT` of type `VT_NULL`.</span></span> <span data-ttu-id="50a10-148">Bu durumda, `vType` parametresi özelliği CIM türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="50a10-148">In this case, the `vType` parameter specifies the CIM type of the property.</span></span> <span data-ttu-id="50a10-149">Diğer her durumda `vtType` 0 olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="50a10-149">In every other case, `vtType` must be 0.</span></span> <span data-ttu-id="50a10-150">`vtType`temel alınan nesnede bir örneğiyse 0 olmalıdır (olsa bile `Val` olan `null`) çünkü özelliğinin türü sabittir ve değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="50a10-150">`vtType` must also be 0 if the underlying object is an instance (even if `Val` is `null`) because the type of the property is fixed and cannot be changed.</span></span>   

## <a name="example"></a><span data-ttu-id="50a10-151">Örnek</span><span class="sxs-lookup"><span data-stu-id="50a10-151">Example</span></span>

<span data-ttu-id="50a10-152">Bir örnek için bkz: [IWbemClassObject::Put](https://msdn.microsoft.com/library/aa391455(v=vs.85).aspx) yöntemi.</span><span class="sxs-lookup"><span data-stu-id="50a10-152">For an example, see the [IWbemClassObject::Put](https://msdn.microsoft.com/library/aa391455(v=vs.85).aspx) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50a10-153">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="50a10-153">Requirements</span></span>  
 <span data-ttu-id="50a10-154">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50a10-154">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50a10-155">**Başlık:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="50a10-155">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="50a10-156">**.NET framework sürümleri:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="50a10-156">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50a10-157">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="50a10-157">See also</span></span>  
[<span data-ttu-id="50a10-158">WMI ve performans sayaçları (yönetilmeyen API Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="50a10-158">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)