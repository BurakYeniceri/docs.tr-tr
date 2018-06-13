---
title: 'Hizmet: Saniye Başına Çağrı'
ms.date: 03/30/2017
ms.assetid: 6261d28d-d449-425a-b9fc-a4ee14079134
ms.openlocfilehash: c23456f49eb867d5b6f66b4386a83615d95e07da
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473934"
---
# <a name="service-calls-per-second"></a><span data-ttu-id="15e0f-102">Hizmet: Saniye Başına Çağrı</span><span class="sxs-lookup"><span data-stu-id="15e0f-102">Service: Calls Per Second</span></span>
<span data-ttu-id="15e0f-103">Sayaç adı: Saniye başına çağrı.</span><span class="sxs-lookup"><span data-stu-id="15e0f-103">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="15e0f-104">Açıklama</span><span class="sxs-lookup"><span data-stu-id="15e0f-104">Description</span></span>  
 <span data-ttu-id="15e0f-105">Bu ikinci hizmetinde yapılan çağrı sayısı.</span><span class="sxs-lookup"><span data-stu-id="15e0f-105">Number of calls to this service in a second.</span></span>  
  
 <span data-ttu-id="15e0f-106">Bu sayaç, performans sayacı türü [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), değeri, aşağıdaki formül kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="15e0f-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="15e0f-107">(1 - N 0 N) / ((D 1 -D 0) / F) burada (N) pay son örnekleme aralığı sırasında geçen çizgilerine sayısı payda (D) temsil son örnekleme aralığı sırasında gerçekleştirilen işlemler sayısını temsil eder ve F çizgilerine sıklığı.</span><span class="sxs-lookup"><span data-stu-id="15e0f-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) where the numerator (N) represents the number of operations performed during the last sample interval, the denominator (D) represents the number of ticks elapsed during the last sample interval, and F is the frequency of the ticks.</span></span>
