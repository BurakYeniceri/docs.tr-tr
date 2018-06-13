---
title: 'Nasıl yapılır: yükleme ertelenmiş Kapat'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1b84b852-3cad-41a7-8077-149a70d50c8b
ms.openlocfilehash: 279317f10211271fad812068215b08a93e30fbdf
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358651"
---
# <a name="how-to-turn-off-deferred-loading"></a>Nasıl yapılır: yükleme ertelenmiş Kapat
Ayarlayarak yüklenirken ertelenmiş kapatabilirsiniz <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> için `false`. Daha fazla bilgi için bkz: [hemen yüklenirken karşı ertelenmiş](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md).  
  
> [!NOTE]
>  İzleme nesnesi devre dışı bırakıldığında dolaylı Ertelenen yükleme devre dışı bırakılır. Daha fazla bilgi için bkz: [nasıl yapılır: olarak bilgi almak Read-Only](../../../../../../docs/framework/data/adonet/sql/linq/how-to-retrieve-information-as-read-only.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek ayarlayarak yüklenirken ertelenmiş devre dışı bırakmak gösterilmiştir <xref:System.Data.Linq.DataContext.DeferredLoadingEnabled%2A> için `false`.  
  
 [!code-csharp[DLinqQuerying#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQuerying/cs/Program.cs#3)]
 [!code-vb[DLinqQuerying#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQuerying/vb/Module1.vb#3)]  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sorgu Kavramları](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)  
 [Veritabanını Sorgulama](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
