---
title: 'Nasıl yapılır: Uygulama Etki Alanını Boşaltma'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Unload method
- application domains, unloading
- unloading application domains
ms.assetid: f356116d-e415-4f7c-a332-6e6a60227192
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8b4cbdff72167cfc063254cf5370d22fb729b0a
ms.sourcegitcommit: 9bd8f213b50f0e1a73e03bd1e840c917fbd6d20a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50088578"
---
# <a name="how-to-unload-an-application-domain"></a>Nasıl yapılır: Uygulama Etki Alanını Boşaltma
Uygulama etki alanı kullanarak tamamladığınızda kullanarak kaldırma <xref:System.AppDomain.Unload%2A?displayProperty=nameWithType> yöntemi. **Kaldırma** yöntemi düzgün bir şekilde belirtilen uygulama etki alanı kapatır. Kaldırma işlemi sırasında hiçbir yeni iş parçacığı uygulama etki alanı erişebilir ve tüm uygulama etki alanına özgü veri yapıları serbest.  
  
 Uygulama etki alanına yüklenen derlemelerin kaldırılır ve artık kullanılamaz. Uygulama etki alanındaki bir derleme etki alanından bağımsız ise, derleme için veri işlem kapatılana kadar bellekte kalır. Tüm işlemi kapatma dışındaki bir etki alanından bağımsız derleme kaldırmak için bir mekanizma yoktur. Burada, bir uygulama etki alanını boşaltma isteği çalışmıyor ve sonuçlanır durumlar vardır bir <xref:System.CannotUnloadAppDomainException>.  
  
 Aşağıdaki örnekte adlı yeni bir uygulama etki alanı oluşturur `MyDomain`bazı bilgileri konsola yazdırır ve ardından uygulama etki alanını kaldırır. Kodu daha sonra konsola bellekten uygulama etki alanının kolay adını yazdırmak çalışır olduğunu unutmayın. Bu eylem, programın sonunda try/catch deyimleri tarafından işlenen özel durum oluşturur.  
  
## <a name="example"></a>Örnek  
 [!code-cpp[System.AppDomain.Load#3](../../../samples/snippets/cpp/VS_Snippets_CLR_System/system.appdomain.load/cpp/source3.cpp#3)]
 [!code-csharp[System.AppDomain.Load#3](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.appdomain.load/cs/source3.cs#3)]
 [!code-vb[System.AppDomain.Load#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.appdomain.load/vb/source3.vb#3)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
- [Uygulama etki alanlarıyla programlama](application-domains.md#programming-with-application-domains)  
- [Nasıl yapılır: Uygulama Etki Alanı Oluşturma](../../../docs/framework/app-domains/how-to-create-an-application-domain.md)  
- [Uygulama Etki Alanlarını Kullanma](../../../docs/framework/app-domains/use.md)
