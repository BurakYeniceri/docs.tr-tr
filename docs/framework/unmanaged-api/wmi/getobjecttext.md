---
title: GetObjectText işlevi (yönetilmeyen API Başvurusu)
description: GetObjectText işlevi bir metin işleme bir nesnenin MOF sözdiziminde döndürür.
ms.date: 11/06/2017
api_name:
- GetObjectText
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetObjectText
helpviewer_keywords:
- GetObjectText function [.NET WMI and performance counters]
topic_type:
- Reference
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 24ba4b37cc8221df4e018d172996c0910ec07f7d
ms.sourcegitcommit: a1e35d4e94edab384a63406c0a5438306873031b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2018
ms.locfileid: "42752358"
---
# <a name="getobjecttext-function"></a>GetObjectText işlevi
Nesnenin değerinin metinsel bir işleme Yönetilen Nesne Biçimi (MOF) söz diziminde döndürür.

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
    
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT GetObjectText (
   [in] int                vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LONG                lFlags,
   [out] BSTR*              pstrObjectText
); 
```  

## <a name="parameters"></a>Parametreler

`vFunc`  
[in] Bu parametre kullanılmaz.

`ptr`  
[in] Bir işaretçi bir [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) örneği.

`lFlags`  
[in] Normalde 0. Varsa `WBEM_FLAG_NO_FLAVORS` (veya 0x1) belirtilirse, niteleyicileri yayma veya flavor bilgileri olmadan dahil edilir.

`pstrObjectText`   
[out] Bir işaretçi bir `null` girişi. Üzerinde iade, yeni ayrılan `BSTR` , içeren nesnenin MOF sözdizimi işleme.  

## <a name="return-value"></a>Dönüş değeri

Bu işlev tarafından döndürülen aşağıdaki değerleri tanımlanan *WbemCli.h* üst bilgi dosyası veya tanımlayabilirsiniz bunları sabitleri kodunuzda:

|Sabit  |Değer  |Açıklama  |
|---------|---------|---------|
|`WBEM_E_FAILED` | 0x80041001 | Genel bir hata oluştu. |
|`WBEM_E_INVALID_PARAMETER` | 0x80041008 | Bir parametre geçerli değil. |
|`WBEM_E_OUT_OF_MEMORY` | 0x80041006 | İşlemi tamamlamak yeterli bellek yok. |
|`WBEM_S_NO_ERROR` | 0 | İşlev çağrısı başarılı oldu.  |
  
## <a name="remarks"></a>Açıklamalar

Bu işlev bir çağrı sarılır [IWbemClassObject::GetObjectText](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext) yöntemi.

Döndürülen MOF metin nesnesine ilişkin tüm bilgileri, ancak orijinal nesneyi yeniden oluşturmaya yapabilmek MOF derleyicisi için yeterli bilgi içermiyor. Örneğin, yayılan niteleyicileri ya da üst sınıfı özellikleri dahil edilir.

Aşağıdaki algoritması, bir yöntemin parametre metin yeniden oluşturmak için kullanılır:

1. Parametre tanımlayıcı değerlerini sırasına göre yeniden sıralanmış.
1. Parametre olarak belirtilen `[in]` ve `[out]` tek bir parametre birleştirilir.
 
`pstrObjectText` bir işaretçi olmalıdır bir `null` işlev çağrıldığında; bu işaretçisi serbest çünkü yöntem çağrısından önce geçerli bir dizeye işaret etmelidir değil.

## <a name="requirements"></a>Gereksinimler  
**Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Başlık:** WMINet_Utils.idl  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
[WMI ve performans sayaçları (yönetilmeyen API Başvurusu)](index.md)
