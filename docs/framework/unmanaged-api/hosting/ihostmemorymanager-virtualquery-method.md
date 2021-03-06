---
title: IHostMemoryManager::VirtualQuery Yöntemi
ms.date: 03/30/2017
api_name:
- IHostMemoryManager.VirtualQuery
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostMemoryManager::VirtualQuery
helpviewer_keywords:
- IHostMemoryManager::VirtualQuery method [.NET Framework hosting]
- VirtualQuery method [.NET Framework hosting]
ms.assetid: 757af1e6-b9e8-49e7-b5db-342be3aa205f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 68a9d6ad7470ffaf1143a4a8e3134f20edb9e3c5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33439225"
---
# <a name="ihostmemorymanagervirtualquery-method"></a>IHostMemoryManager::VirtualQuery Yöntemi
Karşılık gelen Win32 işlevi için mantıksal bir kapsayıcı görevi görür. Win32 uygulaması `VirtualQuery` çağırma işleminin sanal adres alanındaki sayfaları bir dizi ilgili bilgileri alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
HRESULT VirtualQuery (  
    [in]  void*    lpAddress,  
    [out] void*    lpBuffer,  
    [in]  SIZE_T   dwLength,  
    [out] SIZE_T*  pResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `lpAddress`  
 [in] Sorgulanacak sanal bellek adresi için bir işaretçi.  
  
 `lpBuffer`  
 [out] Belirtilen bellek bölge hakkında bilgi içeren bir yapı için bir işaretçi.  
  
 `dwLength`  
 [in] Arabelleğin bayt cinsinden boyutu, `lpBuffer` işaret eder.  
  
 `pResult`  
 [out] Bilgi arabellek tarafından döndürülen bayt sayısı için bir işaretçi.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
|HRESULT|Açıklama|  
|-------------|-----------------|  
|S_OK|`VirtualQuery` başarıyla döndürüldü.|  
|HOST_E_CLRNOTAVAILABLE|Ortak dil çalışma zamanı (CLR) süreç içine yüklü değil veya CLR içinde yönetilen kod çalıştıramaz veya çağrı başarılı bir şekilde işlemek bir durumda.|  
|HOST_E_TIMEOUT|Arama zaman aşımına uğradı.|  
|HOST_E_NOT_OWNER|Arayan kilidi kendisine ait değil.|  
|HOST_E_ABANDONED|Bir olay engellenmiş iş parçacığı sırasında iptal edildi veya fiber üzerinde beklediği.|  
|E_FAIL|Bilinmeyen yıkıcı bir hata oluştu. Bir yöntem E_FAIL döndüğünde, CLR artık işlemi içinde kullanılamaz. Yöntemleri barındırma sonraki çağrılar HOST_E_CLRNOTAVAILABLE döndürür.|  
  
## <a name="remarks"></a>Açıklamalar  
 `VirtualQuery` bir dizi çağırma işleminin sanal adres alanındaki sayfaları hakkında bilgi sağlar. Bu uygulama değerini ayarlar `pResult` bayt sayısı parametre bilgileri arabellekte ve bir HRESULT değeri döndürür. Win32 `VirtualQuery` dönüş değeri işlevidir arabellek boyutu. Daha fazla bilgi için Windows platformu belgelerine bakın.  
  
> [!IMPORTANT]
>  İşletim sisteminin uyarlamasını `VirtualQuery` kilitlenme tabi değildir ve tamamlanıncaya kadar rastgele iş parçacığı içinde kullanıcı kodu askıya çalıştırabilirsiniz. Harika bu yöntem barındırılan bir sürümünü uygularken dikkatli olun.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Başlık:** MSCorEE.h  
  
 **Kitaplığı:** bir kaynak olarak MSCorEE.dll dahil  
  
 **.NET framework sürümleri:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IHostMemoryManager Arabirimi](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
