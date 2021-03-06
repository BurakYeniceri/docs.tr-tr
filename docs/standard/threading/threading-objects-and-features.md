---
title: İş parçacığı nesneleri ve özellikleri
ms.date: 10/01/2018
ms.technology: dotnet-standard
helpviewer_keywords:
- threading [.NET Framework], features
- managed threading
ms.assetid: 239b2e8d-581b-4ca3-992b-0e8525b9321c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1ba47ece16c74555b58780733e14de9833718c33
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2018
ms.locfileid: "48873313"
---
# <a name="threading-objects-and-features"></a>İş parçacığı nesneleri ve özellikleri

İle birlikte <xref:System.Threading.Thread?displayProperty=nameWithType> .NET sağlar sınıfını yardımcı sınıfları sayısı çok iş parçacıklı uygulamalar geliştirin. Aşağıdaki makaleler bu sınıflara genel bakış sunar:

|Başlık|Açıklama|  
|-----------|-----------------|  
|[Yönetilen iş parçacığı havuzu](the-managed-thread-pool.md)|Açıklar <xref:System.Threading.ThreadPool?displayProperty=nameWithType> .NET tarafından yönetilen çalışan iş parçacığı havuzu sağlar sınıfını.|  
|[Süreölçerler](timers.md)|Çok iş parçacıklı bir ortamda kullanılabilir .NET zamanlayıcılar açıklar.|
|[Eşitleme temellerine genel bakış](overview-of-synchronization-primitives.md)|Bir paylaşılan kaynağa veya denetimi iş parçacığı etkileşim erişimi eşitlemek için kullanılan türleri açıklanmaktadır.|
|[EventWaitHandle, AutoResetEvent, CountdownEvent, ManualResetEvent](eventwaithandle-autoresetevent-countdownevent-manualresetevent.md)|Sinyal ve sinyalleri için bekleyen iş parçacığı etkinlikleri eşitlemek için kullanılan yönetilen bir olay bekleme tanıtıcıları açıklar.|
|[Karşılıklı dışlamalar](mutexes.md)|Açıklar <xref:System.Threading.Mutex?displayProperty=nameWithType>, paylaşılan bir kaynağa özel erişim verir.|
|[Birbirine kenetlenmiş işlemler](interlocked-operations.md)|Açıklar <xref:System.Threading.Interlocked?displayProperty=nameWithType> birden çok iş parçacığı tarafından paylaşılan değişkenleri için atomik işlemler sağlar sınıfını.|
|[Okuyucu-Yazıcı Kilitleri](reader-writer-locks.md)|Açıklar <xref:System.Threading.ReaderWriterLockSlim?displayProperty=nameWithType> tek yazıcı/birden çok okuyucu paylaşılan bir kaynağa erişim sağlayan sınıf.|
|[Semaphore ve SemaphoreSlim](semaphore-and-semaphoreslim.md)|Açıklar <xref:System.Threading.Semaphore?displayProperty=nameWithType> sınıfını, paylaşılan bir kaynağa erişmek için iş parçacığı sayısı veya bir kaynak havuzu eşzamanlı olarak sınırlar.|
|[Engel](barrier.md)|Açıklar <xref:System.Threading.Barrier?displayProperty=nameWithType> aşamalı işlemlerinde koordinasyon iş parçacıklarının engeli desenini uygulayan sınıf.|
|[SpinLock](spinlock.md)|Açıklar <xref:System.Threading.SpinLock?displayProperty=nameWithType> hafif bir yapısı için alternatif <xref:System.Threading.Monitor?displayProperty=nameWithType> belirli alt düzey kilitleme senaryoları için sınıf.|
|[SpinWait](spinwait.md)|Açıklar <xref:System.Threading.SpinWait?displayProperty=nameWithType> yapısı, döndürme tabanlı bekleme için destek sağlar.|

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Threading.Monitor?displayProperty=nameWithType>
- <xref:System.Threading.WaitHandle?displayProperty=nameWithType>
- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Parallel?displayProperty=nameWithType>
- <xref:System.Threading.Tasks.Task?displayProperty=nameWithType>
- [İş parçacığı kullanma ve iş parçacığı oluşturma](using-threads-and-threading.md)
- [Zaman Uyumsuz Dosya G/Ç](../io/asynchronous-file-i-o.md)
- [Paralel Programlama](../parallel-programming/index.md)
- [Görev Paralel Kitaplığı (TPL)](../parallel-programming/task-parallel-library-tpl.md)
