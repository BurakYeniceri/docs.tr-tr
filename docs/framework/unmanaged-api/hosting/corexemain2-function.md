---
title: _CorExeMain2 İşlevi
ms.date: 03/30/2017
api_name:
- _CorExeMain2
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorExeMain2
helpviewer_keywords:
- _CorExeMain2 function [.NET Framework hosting]
ms.assetid: 72ea68b4-689f-4733-9416-9664b75e8892
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 573336b32040f44ff1b59fcbb75b59aa00976b5c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430185"
---
# <a name="corexemain2-function"></a>_CorExeMain2 İşlevi
Giriş noktası belirtilen bellekle eşlenen kodu yürütür. Bu işlev, işletim sistemi yükleyicisi tarafından çağrılır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
__int32 STDMETHODCALLTYPE _CorExeMain2 (  
   [in] PBYTE           pUnmappedPE,  
   [in] DWORD           cUnmappedPE,  
   [in] __in LPWSTR     pImageNameIn,  
   [in] __in LPWSTR     pLoadersFileName,  
   [in] __in LPWSTR     pCmdLine  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pUnmappedPE`  
 [in] Bellek eşlemeli kodu için bir işaretçi.  
  
 `cUnmappedPE`  
 [in] Öğe sayısını `pUnmappedPE` basılı tutabilirsiniz.  
  
 `pImageNameIn`  
 [in] Yürütülebilir görüntü adı için bir işaretçi.  
  
 `pLoadersFileName`  
 [in] Yükleyici dosyasının adı.  
  
 `pCmdLine`  
 [in] Komut satırı parametreleri, varsa.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Başlık:** Cor.h  
  
 **Kitaplığı:** bir kaynak olarak MsCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Meta Veri Genel Statik İşlevleri](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
