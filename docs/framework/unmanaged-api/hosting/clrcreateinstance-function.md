---
title: "CLRCreateInstance İşlevi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CLRCreateInstance
api_location:
- mscoree.dll
- mscoreei.dll
api_type: COM
f1_keywords: CLRCreateInstance
helpviewer_keywords: CLRCreateInstance function [.NET Framework hosting]
ms.assetid: 5de13327-96c6-4697-a89e-b8bf40717855
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f10fe48bc2b61a9de5d0703720629f31531c1ea1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="clrcreateinstance-function"></a>CLRCreateInstance İşlevi
Üç arabirimi birini sağlar: [Iclrmetahost](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md), [Iclrmetahostpolicy](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-interface.md), veya [Iclrdebugging](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-interface.md).  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT CLRCreateInstance(  
    [in]  REFCLSID  clsid,  
    [in]  REFIID     riid,  
    [out] LPVOID  * ppInterface  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `clsid`  
 [in] Üç sınıf tanımlayıcıları birini: CLSID_CLRMetaHost, CLSID_CLRMetaHostPolicy veya CLSID_CLRDebugging.  
  
 `riid`  
 [in] Üç arabirim tanımlayıcıları (IID'leri) birini: IID_ICLRMetaHost, IID_ICLRMetaHostPolicy veya IID_ICLRDebugging.  
  
 `ppInterface`  
 [out] Üç arabirimi birini: [Iclrmetahost](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-interface.md), [Iclrmetahostpolicy](../../../../docs/framework/unmanaged-api/hosting/iclrmetahostpolicy-interface.md), veya [Iclrdebugging](../../../../docs/framework/unmanaged-api/debugging/iclrdebugging-interface.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Bu yöntem aşağıdaki belirli HRESULTs yanı sıra HRESULT yöntem hatası olduğunu gösteren hatalar.  
  
|HRESULT|Açıklama|  
|-------------|-----------------|  
|S_OK|Yöntem başarıyla tamamlandı.|  
|E_POINTER|`ppInterface`null şeklindedir.|  
  
## <a name="remarks"></a>Açıklamalar  
 Aşağıdaki tablo için desteklenen birleşimlerin gösterir `clsid` ve `riid`.  
  
|`rclsid`|`riid`|  
|--------------|------------|  
|CLSID_CLRMetaHost|IID_ICLRMetaHost|  
|CLSID_CLRMetaHostPolicy|IID_ICLRMetaHostPolicy|  
|CLSID_CLRDebugging|IID_ICLRDebugging|  
  
 Aşağıdaki kodu nasıl kullanılacağını gösterir `CLRCreateInstance` tüm üç arabirimi almak için:  
  
```  
#include <metahost.h>  
#pragma comment(lib, "mscoree.lib")  
  
ICLRMetaHost       *pMetaHost       = NULL;  
ICLRMetaHostPolicy *pMetaHostPolicy = NULL;  
ICLRDebugging      *pCLRDebugging   = NULL;  
HRESULT hr;  
hr = CLRCreateInstance(CLSID_CLRMetaHost, IID_ICLRMetaHost,  
                    (LPVOID*)&pMetaHost);  
hr = CLRCreateInstance (CLSID_CLRMetaHostPolicy, IID_ICLRMetaHostPolicy,  
                    (LPVOID*)&pMetaHostPolicy);  
hr = CLRCreateInstance (CLSID_CLRDebugging, IID_ICLRDebugging,  
                    (LPVOID*)&pCLRDebugging);  
```  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Başlık:** MetaHost.h  
  
 **Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil  
  
 **.NET framework sürümleri:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Barındırma](../../../../docs/framework/unmanaged-api/hosting/index.md)
