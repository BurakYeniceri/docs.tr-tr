---
title: "Hizmet: Saniye Başına Çağrı"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6261d28d-d449-425a-b9fc-a4ee14079134
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 7a1fd0b3fdbb07a975c23decf0ab389f09033699
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2017
---
# <a name="service-calls-per-second"></a><span data-ttu-id="cb03a-102">Hizmet: Saniye Başına Çağrı</span><span class="sxs-lookup"><span data-stu-id="cb03a-102">Service: Calls Per Second</span></span>
<span data-ttu-id="cb03a-103">Sayaç adı: Saniye başına çağrı.</span><span class="sxs-lookup"><span data-stu-id="cb03a-103">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="cb03a-104">Açıklama</span><span class="sxs-lookup"><span data-stu-id="cb03a-104">Description</span></span>  
 <span data-ttu-id="cb03a-105">Bu ikinci hizmetinde yapılan çağrı sayısı.</span><span class="sxs-lookup"><span data-stu-id="cb03a-105">Number of calls to this service in a second.</span></span>  
  
 <span data-ttu-id="cb03a-106">Bu sayaç, performans sayacı türü [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), değeri, aşağıdaki formül kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="cb03a-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="cb03a-107">(1 - N 0 N) / ((D 1 -D 0) / F) burada (N) pay son örnekleme aralığı sırasında geçen çizgilerine sayısı payda (D) temsil son örnekleme aralığı sırasında gerçekleştirilen işlemler sayısını temsil eder ve F çizgilerine sıklığı.</span><span class="sxs-lookup"><span data-stu-id="cb03a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F) where the numerator (N) represents the number of operations performed during the last sample interval, the denominator (D) represents the number of ticks elapsed during the last sample interval, and F is the frequency of the ticks.</span></span>
