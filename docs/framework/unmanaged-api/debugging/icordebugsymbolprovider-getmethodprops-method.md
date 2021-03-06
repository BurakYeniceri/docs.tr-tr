---
title: ICorDebugSymbolProvider::GetMethodProps yöntemi
ms.date: 03/30/2017
ms.assetid: 8f836b80-b7a5-460b-bf76-5f0e45652aea
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: f52d20b9cb717d72d660bb19a0474c3e5b293ab4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422197"
---
# <a name="icordebugsymbolprovidergetmethodprops-method"></a>ICorDebugSymbolProvider::GetMethodProps yöntemi
Bu yönteme göreli sanal adres (RVA) verilen yöntemin meta veri simgesi ve kendi genel parametreleri hakkında bilgi gibi yöntemi özellikleri hakkında bilgi döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetMethodProps(  
   [in]  ULONG32 codeRva,  
   [out] mdToken *pMethodToken,  
   [out] ULONG32 *pcGenericParams,  
   [in]  ULONG32 cbSignature,  
   [out] ULONG32 *pcbSignature,  
   [out, size_is(cbSignature), length_is(*pcbSignature)] BYTE signature[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `codeRVA`  
 [in] Hakkında bilgi alınabilecek olduğu yönteminde göreli bir sanal adres.  
  
 `pMethodToken`  
 [out] Yöntemin meta veri simgesi için bir işaretçi.  
  
 `pcGenericParams`  
 [out] Bu yöntem ile ilgili genel parametreleri sayısı için bir işaretçi.  
  
 `cbSignature`  
 [in] Boyutunu `signature` dizi. Açıklamalar bölümüne bakın.  
  
 `pcbSignature`  
 [out] Döndürülen boyutu gösteren bir işaretçi `signature` dizi.  
  
 `signature`  
 [out] Tüm genel parametreler TypeSpec'te imzalarını tutan bir arabellek.  
  
## <a name="remarks"></a>Açıklamalar  
 Yöntemin gerekli boyutunu almak için `signature` dizisindeki, ayarlamak `cbSignature` bağımsız değişkeni 0 ve `signature` için **null**. Yöntem döndüğünde `pcbSignature` için gereken bayt sayısını içerecektir `signature` dizi.  
  
> [!NOTE]
>  Bu yöntem yalnızca .NET yerel ile kullanılabilir.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Başlık:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [GetTypeProps Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-gettypeprops-method.md)  
 [ICorDebugSymbolProvider Arabirimi](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [Hata Ayıklama Arabirimleri](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
