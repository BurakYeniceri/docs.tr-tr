---
title: IMetaDataImport::GetPropertyProps Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.GetPropertyProps
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::GetPropertyProps
helpviewer_keywords:
- GetPropertyProps method [.NET Framework metadata]
- IMetaDataImport::GetPropertyProps method [.NET Framework metadata]
ms.assetid: dc0ff3e6-7e7d-4f6c-948d-52b28f5cb78c
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: fc3a1ce1d07bda50b2b578e7d20870324d60edc0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportgetpropertyprops-method"></a><span data-ttu-id="d55de-102">IMetaDataImport::GetPropertyProps Metodu</span><span class="sxs-lookup"><span data-stu-id="d55de-102">IMetaDataImport::GetPropertyProps Method</span></span>
<span data-ttu-id="d55de-103">Belirtilen belirteç tarafından temsil edilen bir özellik için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="d55de-103">Gets the metadata for the property represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d55de-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d55de-104">Syntax</span></span>  
  
```  
HRESULT GetPropertyProps (  
   [in]  mdProperty        prop,  
   [out] mdTypeDef         *pClass,   
   [out] LPCWSTR           szProperty,   
   [in]  ULONG             cchProperty,   
   [out] ULONG             *pchProperty,   
   [out] DWORD             *pdwPropFlags,   
   [out] PCCOR_SIGNATURE   *ppvSig,   
   [out] ULONG             *pbSig,   
   [out] DWORD             *pdwCPlusTypeFlag,   
   [out] UVCP_CONSTANT     *ppDefaultValue,  
   [out] ULONG             *pcchDefaultValue,  
   [out] mdMethodDef       *pmdSetter,   
   [out] mdMethodDef       *pmdGetter,   
   [out] mdMethodDef       rmdOtherMethod[],  
   [in]  ULONG             cMax,   
   [out] ULONG             *pcOtherMethod   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d55de-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="d55de-105">Parameters</span></span>  
 `prop`  
 <span data-ttu-id="d55de-106">[in] Özellik için meta verileri döndürmek için temsil eden bir belirteci.</span><span class="sxs-lookup"><span data-stu-id="d55de-106">[in] A token that represents the property to return metadata for.</span></span>  
  
 `pClass`  
 <span data-ttu-id="d55de-107">[out] Özellik uygulayan türünü temsil eden TypeDef belirteci için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="d55de-107">[out] A pointer to the TypeDef token that represents the type that implements the property.</span></span>  
  
 `szProperty`  
 <span data-ttu-id="d55de-108">[out] Özellik adı tutacak bir arabellek.</span><span class="sxs-lookup"><span data-stu-id="d55de-108">[out] A buffer to hold the property name.</span></span>  
  
 `cchProperty`  
 <span data-ttu-id="d55de-109">[in] Geniş karakter cinsinden boyutu `szProperty`.</span><span class="sxs-lookup"><span data-stu-id="d55de-109">[in] The size in wide characters of `szProperty`.</span></span>  
  
 `pchProperty`  
 <span data-ttu-id="d55de-110">[out] Döndürülen geniş karakter sayısını `szProperty`.</span><span class="sxs-lookup"><span data-stu-id="d55de-110">[out] The number of wide characters returned in `szProperty`.</span></span>  
  
 `pdwPropFlags`  
 <span data-ttu-id="d55de-111">[out] Özelliğine uygulanan herhangi bir öznitelik bayrağı için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="d55de-111">[out] A pointer to any attribute flags applied to the property.</span></span> <span data-ttu-id="d55de-112">Bu değer gelen bir bit maskesi olan [CorPropertyAttr](../../../../docs/framework/unmanaged-api/metadata/corpropertyattr-enumeration.md) numaralandırması.</span><span class="sxs-lookup"><span data-stu-id="d55de-112">This value is a bitmask from the [CorPropertyAttr](../../../../docs/framework/unmanaged-api/metadata/corpropertyattr-enumeration.md) enumeration.</span></span>  
  
 `ppvSig`  
 <span data-ttu-id="d55de-113">[out] Meta veri imza özelliği için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="d55de-113">[out] A pointer to the metadata signature of the property.</span></span>  
  
 `pbSig`  
 <span data-ttu-id="d55de-114">[out] Döndürülen bayt sayısı `ppvSig`.</span><span class="sxs-lookup"><span data-stu-id="d55de-114">[out] The number of bytes returned in `ppvSig`.</span></span>  
  
 `pdwCPlusTypeFlag`  
 <span data-ttu-id="d55de-115">[out] Özelliğin varsayılan değeri sabiti türünü belirleyen bir bayrak.</span><span class="sxs-lookup"><span data-stu-id="d55de-115">[out] A flag specifying the type of the constant that is the default value of the property.</span></span> <span data-ttu-id="d55de-116">CorElementType numaralandırması değerdir.</span><span class="sxs-lookup"><span data-stu-id="d55de-116">This value is from the CorElementType enumeration.</span></span>  
  
 `ppDefaultValue`  
 <span data-ttu-id="d55de-117">[out] Bu özellik için varsayılan değer depolamak bayt gösteren bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="d55de-117">[out] A pointer to the bytes that store the default value for this property.</span></span>  
  
 `pcchDefaultValue`  
 <span data-ttu-id="d55de-118">[out] Geniş karakter cinsinden boyutu `ppDefaultValue`, `pdwCPlusTypeFlag` olan ELEMENT_TYPE_STRING; Aksi takdirde, bu değer ilgili değildir.</span><span class="sxs-lookup"><span data-stu-id="d55de-118">[out] The size in wide characters of `ppDefaultValue`, if `pdwCPlusTypeFlag` is ELEMENT_TYPE_STRING; otherwise, this value is not relevant.</span></span> <span data-ttu-id="d55de-119">Bu durumda, uzunluğu `ppDefaultValue` tarafından belirtilen türden olayla `pdwCPlusTypeFlag`.</span><span class="sxs-lookup"><span data-stu-id="d55de-119">In that case, the length of `ppDefaultValue` is inferred from the type that is specified by `pdwCPlusTypeFlag`.</span></span>  
  
 `pmdSetter`  
 <span data-ttu-id="d55de-120">[out] Özelliği için set erişimcisi yöntemi temsil eden MethodDef belirteci için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="d55de-120">[out] A pointer to the MethodDef token that represents the set accessor method for the property.</span></span>  
  
 `pmdGetter`  
 <span data-ttu-id="d55de-121">[out] Özellik get erişimcisi yöntemi temsil eden MethodDef belirteci için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="d55de-121">[out] A pointer to the MethodDef token that represents the get accessor method for the property.</span></span>  
  
 `rmdOtherMethod`  
 <span data-ttu-id="d55de-122">[out] Özellik ile ilişkilendirilmiş diğer yöntemleri gösteren MethodDef belirteçleri dizisi.</span><span class="sxs-lookup"><span data-stu-id="d55de-122">[out] An array of MethodDef tokens that represent other methods associated with the property.</span></span>  
  
 `cMax`  
 <span data-ttu-id="d55de-123">[in] En büyük boyutunu `rmdOtherMethod` dizi.</span><span class="sxs-lookup"><span data-stu-id="d55de-123">[in] The maximum size of the `rmdOtherMethod` array.</span></span> <span data-ttu-id="d55de-124">Tüm yöntemleri tutabilecek kadar büyük bir dizi belirtmezseniz, bunlar uyarmadan atlanır.</span><span class="sxs-lookup"><span data-stu-id="d55de-124">If you do not provide an array large enough to hold all the methods, they are skipped without warning.</span></span>  
  
 `pcOtherMethod`  
 <span data-ttu-id="d55de-125">[out] Döndürülen MethodDef belirteçleri sayısı `rmdOtherMethod`.</span><span class="sxs-lookup"><span data-stu-id="d55de-125">[out] The number of MethodDef tokens returned in `rmdOtherMethod`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d55de-126">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="d55de-126">Requirements</span></span>  
 <span data-ttu-id="d55de-127">**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d55de-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d55de-128">**Başlık:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="d55de-128">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d55de-129">**Kitaplığı:** bir kaynak olarak MsCorEE.dll dahil</span><span class="sxs-lookup"><span data-stu-id="d55de-129">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d55de-130">**.NET framework sürümleri:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d55de-130">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d55de-131">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="d55de-131">See Also</span></span>  
 [<span data-ttu-id="d55de-132">Imetadataımport arabirimi</span><span class="sxs-lookup"><span data-stu-id="d55de-132">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="d55de-133">Imetadataımport2 arabirimi</span><span class="sxs-lookup"><span data-stu-id="d55de-133">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)