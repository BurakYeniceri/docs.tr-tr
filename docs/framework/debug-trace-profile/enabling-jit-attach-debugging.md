---
title: JIT-Ekleme Hata Ayıklamayı Etkinleştirme
ms.date: 03/30/2017
helpviewer_keywords:
- JIT-attach debugging
- debugging [.NET Framework], JIT-attach debugging
ms.assetid: f91fc5f7-de5a-4f23-b6ac-f450e63c662e
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b92592500f0babf29891710cedf1228b0ddcb0e4
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45970740"
---
# <a name="enabling-jit-attach-debugging"></a>JIT-Ekleme Hata Ayıklamayı Etkinleştirme
JIT-ekleme hata ayıklamayı hatalarla ya da belirli yöntemler ve işlevlere tarafından tetiklenebilir bir hata ayıklayıcı bir işlemine iliştirme açıklamak için kullanılan ifade var.  
  
 JIT-ekleme hata ayıklamayı aşağıdaki hata koşulları altında kullanılır:  
  
-   İşlenmeyen özel durumları (yerel ve yönetilen kod).  
  
-   <xref:System.Environment.FailFast%2A?displayProperty=nameWithType> yöntem veya [RaiseFailFastException](https://go.microsoft.com/fwlink/?LinkId=182107) işlevi (Windows 7 ailesi).  
  
-   Önemli hatalarla çalışma zamanı.  
  
 JIT-ekleme hata ayıklamayı aşağıdaki yöntemleri ve işlevleri yapılan çağrılar tarafından ayrıca başlatılır:  
  
-   <xref:System.Diagnostics.Debugger.Launch%2A?displayProperty=nameWithType> yöntem.  
  
-   <xref:System.Diagnostics.Debugger.Break%2A?displayProperty=nameWithType> yöntem.  
  
-   [DebugBreak](https://go.microsoft.com/fwlink/?LinkId=182106) işlevi (Win32).  
  
 Önce [!INCLUDE[net_v40_long](../../../includes/net-v40-long-md.md)], .NET Framework sağlanan yerel ve yönetilen hata ayıklayıcıları davranışını denetlemek için ayrı bir kayıt defteri anahtarları. İle başlayarak [!INCLUDE[net_v40_short](../../../includes/net-v40-short-md.md)], denetim bir tek bir kayıt defteri anahtarı altında birleştirilir: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\Current Version\AeDebug. Bu anahtarı ayarlayabilirsiniz değerleri bir hata ayıklayıcı çağrılan, ve olup bu durumda, kullanıcı etkileşimi gerektiren bir iletişim kutusu çağrılır olup olmadığını belirler. Bu kayıt defteri anahtarı ayarlama hakkında daha fazla bilgi için bkz: [otomatik hata ayıklama yapılandırma](https://go.microsoft.com/fwlink/?LinkId=181767).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklama, İzleme ve Profil Oluşturma](../../../docs/framework/debug-trace-profile/index.md)  
 [Görüntüde Hata Ayıklamayı Kolaylaştırma](../../../docs/framework/debug-trace-profile/making-an-image-easier-to-debug.md)  
 [Profil oluşturmayı etkinleştirme](https://msdn.microsoft.com/library/3b669676-f0e0-4ebf-8674-68986dd2020d)
