---
title: ICorDebugProcess6 Arabirimi
ms.date: 03/30/2017
ms.assetid: 34a10ac2-882c-4797-8369-f120e8e640c7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 103a37d7549d7ec18617b74c777506b3ad225a18
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33422870"
---
# <a name="icordebugprocess6-interface"></a>ICorDebugProcess6 Arabirimi
Mantıksal olarak yerel özel durum hata ayıklama olayları ve sanal modülü bölme kodlanmış yönetilen hata ayıklama olayları kod çözme gibi özellikleri etkinleştirmek için Icordebugprocess arabirimi genişletir.  
  
## <a name="methods"></a>Yöntemler  
  
|Yöntem|Açıklama|  
|------------|-----------------|  
|[DecodeEvent Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-decodeevent-method.md)|Özel olarak hazırlanmış yerel özel durum hata ayıklama olayları yükünde kapsüllenmiş yönetilen hata ayıklama olayları kodunu çözer.|  
|[EnableVirtualModuleSplitting Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-enablevirtualmodulesplitting-method.md)|Etkinleştirir veya sanal modülü bölme devre dışı bırakır.|  
|[GetCode Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getcode-method.md)|Yönetilen kodu hakkında bilgi belirli kod adresinde alır.|  
|[GetExportStepInfo Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-getexportstepinfo-method.md)|Yönetilen kod ilerleyebilirsiniz yardımcı olmak için dışarı çalışma zamanı işlevleri hakkında bilgi sağlar.|  
|[MarkDebuggerAttached Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-markdebuggerattached-method.md)|Debugee iç durumu değişir böylece <xref:System.Diagnostics.Debugger.IsAttached%2A?displayProperty=nameWithType> .NET Framework Sınıf Kitaplığı'nda yöntemi döndürür `true`.|  
|[ProcessStateChanged Yöntemi](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess6-processstatechanged-method.md)|Bildirir [Icordebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) işlemin çalıştığı.|  
  
## <a name="remarks"></a>Açıklamalar  
  
> [!NOTE]
>  Arabirimi yalnızca .NET yerel ile kullanılabilir. Çağrı girişimi `QueryInterface` bir arabirim işaretçisi almak için döndürür `E_NOINTERFACE` .NET yerel dışında Icordebug senaryoları için.  
  
## <a name="requirements"></a>Gereksinimler  
 **Platformlar:** bkz [sistem gereksinimleri](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Başlık:** CorDebug.idl, CorDebug.h  
  
 **Kitaplığı:** CorGuids.lib  
  
 **.NET framework sürümleri:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklama Arabirimleri](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [Hata Ayıklama](../../../../docs/framework/unmanaged-api/debugging/index.md)
