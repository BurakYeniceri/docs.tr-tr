---
title: "Bağlantı sınıfı"
ms.date: 05/01/2017
ms.prod: .net-framework
ms.technology: 
ms.topic: reference
topic_type: apiref
api_name: System.Net.Connection
api_location: System.dll
api_type: Assembly
ms.assetid: 6f0b8902-f31c-4ab9-a8c9-de43228995ec
author: guardrex
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 02303a584aca738718d3e69a0071b40690fa055a
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="connection-class"></a><span data-ttu-id="01a8f-102">Bağlantı sınıfı</span><span class="sxs-lookup"><span data-stu-id="01a8f-102">Connection Class</span></span>

<span data-ttu-id="01a8f-103">`Connection` Sınıfı ayrıştırıyor sunucu yanıtlarının, sıra isteklerini ve ardışık düzen isteği.</span><span class="sxs-lookup"><span data-stu-id="01a8f-103">The `Connection` class parses server responses, queue requests, and pipeline requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="01a8f-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="01a8f-104">Syntax</span></span>
  
```csharp  
internal class Connection : PooledStream
```

> [!WARNING]
> <span data-ttu-id="01a8f-105">`Connection` Sınıfı, iç ve kodunuzda doğrudan kullanılmak üzere yüksetlmesi.</span><span class="sxs-lookup"><span data-stu-id="01a8f-105">The `Connection` class is internal and not meant to be used directly in your code.</span></span>
> 
> <span data-ttu-id="01a8f-106">Microsoft hiçbir koşulda bir üretim uygulamasında bu sınıf kullanımını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="01a8f-106">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a8f-107">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="01a8f-107">Requirements</span></span>

<span data-ttu-id="01a8f-108">**Namespace:**<xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="01a8f-108">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="01a8f-109">**Derleme:** sisteminde (System.dll)</span><span class="sxs-lookup"><span data-stu-id="01a8f-109">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="01a8f-110">**.NET framework sürümleri:** 2.0 sürümünden itibaren kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="01a8f-110">**.NET Framework versions:** Available since 2.0.</span></span>
