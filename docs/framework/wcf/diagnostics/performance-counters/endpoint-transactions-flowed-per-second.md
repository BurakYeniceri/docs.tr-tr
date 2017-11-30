---
title: "Uç noktası: Saniyede Akışı Yapılan İşlem"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0f370ff1-a913-450b-bccb-c279ad165b3d
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: dc0764c689db15a256ad8384c10010c33b6a99f3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="endpoint-transactions-flowed-per-second"></a><span data-ttu-id="30bd8-102">Uç noktası: Saniyede Akışı Yapılan İşlem</span><span class="sxs-lookup"><span data-stu-id="30bd8-102">Endpoint: Transactions Flowed Per Second</span></span>
<span data-ttu-id="30bd8-103">Sayaç adı: Saniyede akışı yapılan işlemler.</span><span class="sxs-lookup"><span data-stu-id="30bd8-103">Counter Name: Transactions Flowed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="30bd8-104">Açıklama</span><span class="sxs-lookup"><span data-stu-id="30bd8-104">Description</span></span>  
 <span data-ttu-id="30bd8-105">İşlem sayısı Bu uç noktada işlemleri için bir saniyede akışı yapılan işlem.</span><span class="sxs-lookup"><span data-stu-id="30bd8-105">Number of transactions flowed to operations at this endpoint in a second.</span></span> <span data-ttu-id="30bd8-106">Bu sayaç, bir işlem kimliği uç noktasına gönderilen bir ileti bulunur dilediğiniz zaman artırılır.</span><span class="sxs-lookup"><span data-stu-id="30bd8-106">This counter is incremented any time a transaction ID is present in a message sent to the endpoint.</span></span>  
  
 <span data-ttu-id="30bd8-107">Bu sayaç, performans sayacı türü [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), değeri, aşağıdaki formül kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="30bd8-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="30bd8-108">(1 - N 0 N) / ((D 1 - D 0) / F)</span><span class="sxs-lookup"><span data-stu-id="30bd8-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>