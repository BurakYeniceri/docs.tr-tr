---
title: "Nasıl yapılır: bir uygulama için varsayılan zaman tabanlı önbellek İlkesi ayarlama"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- time-based cache policies
- cache [.NET Framework], time-based policies
- default time-based cache policy
ms.assetid: 6bfce066-a2e7-4add-a05e-85c12ec9f07f
caps.latest.revision: "9"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: 1d5166090a0682b71f74565e666c96ddadb7c6c1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-set-the-default-time-based-cache-policy-for-an-application"></a><span data-ttu-id="7a832-102">Nasıl yapılır: bir uygulama için varsayılan zaman tabanlı önbellek İlkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a832-102">How to: Set the Default Time-Based Cache Policy for an Application</span></span>
<span data-ttu-id="7a832-103">Önbelleğe alınan kaynakla gönderilen üstbilgiler ve 13 ve RFC 2616, adresinde 14 bölümlerde tanımlanan önbellek davranışını tarafından tanımlanan önbellek davranışını sağlamak bir uygulamanın varsayılan zamana dayalı önbellek İlkesi sağlayan [http://www.ietf.org](http://www.ietf.org/). Çoğu uygulama için uygun önbellek davranış budur.</span><span class="sxs-lookup"><span data-stu-id="7a832-103">The default time-based cache policy allows an application to have its cache behavior defined by the headers sent with the cached resource and the cache behavior defined in sections 13 and 14 of RFC 2616, available at [http://www.ietf.org](http://www.ietf.org/). This is the appropriate cache behavior for most applications.</span></span>  
  
### <a name="to-set-the-default-automatic-policy-for-an-application"></a><span data-ttu-id="7a832-104">Bir uygulama için varsayılan otomatik ilkesini ayarlamak için</span><span class="sxs-lookup"><span data-stu-id="7a832-104">To set the default automatic policy for an application</span></span>  
  
1.  <span data-ttu-id="7a832-105">Varsayılan zaman tabanlı ilke nesnesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a832-105">Create a default time-based policy object.</span></span>  
  
2.  <span data-ttu-id="7a832-106">Uygulama etki alanı için varsayılan olarak ilkesi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7a832-106">Set the policy object as the default for the application domain.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7a832-107">Örnek</span><span class="sxs-lookup"><span data-stu-id="7a832-107">Example</span></span>  
 <span data-ttu-id="7a832-108">Bu bölümdeki iki örnekleri aynı ilkeler üretir.</span><span class="sxs-lookup"><span data-stu-id="7a832-108">The two examples in this section produce identical policies.</span></span>  
  
 <span data-ttu-id="7a832-109">Aşağıdaki örnekte, varsayılan zaman tabanlı bir ilke oluşturulur ve uygulama etki alanı için varsayılan olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a832-109">The following example creates a default time-based policy and sets it as the default for the application domain.</span></span>  
  
```csharp  
public static void SetDefaultTimeBasedPolicy ()  
{  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy ();  
    HttpWebRequest.DefaultCachePolicy = policy ;  
}  
```  
  
```vb  
Public Shared Sub SetDefaultTimeBasedPolicy ()  
    Dim policy = New HttpRequestCachePolicy ()  
    HttpWebRequest.DefaultCachePolicy = policy  
End Sub  
```  
  
 <span data-ttu-id="7a832-110">Varsayılan zamana dayalı önbellek İlkesi kullanarak da oluşturabilirsiniz <xref:System.Net.Cache.RequestCachePolicy> sınıfı aşağıdaki örnekte gösterildiği gibi:</span><span class="sxs-lookup"><span data-stu-id="7a832-110">You can also create the default time-based cache policy using the <xref:System.Net.Cache.RequestCachePolicy> class as shown in the following example:</span></span>  
  
```csharp  
public static void SetDefaultTimeBasedPolicy2()  
{  
    RequestCachePolicy policy = new RequestCachePolicy ();  
    HttpWebRequest.DefaultCachePolicy = policy ;  
}  
```  
  
```vb  
Public Shared Sub SetDefaultTimeBasedPolicy2()  
    Dim policy As New RequestCachePolicy()  
    HttpWebRequest.DefaultCachePolicy = policy  
End Sub  
```  
  
## <a name="see-also"></a><span data-ttu-id="7a832-111">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="7a832-111">See Also</span></span>  
 [<span data-ttu-id="7a832-112">Ağ Uygulamaları için Önbellek Yönetimi</span><span class="sxs-lookup"><span data-stu-id="7a832-112">Cache Management for Network Applications</span></span>](../../../docs/framework/network-programming/cache-management-for-network-applications.md)  
 [<span data-ttu-id="7a832-113">Önbellek İlkesi</span><span class="sxs-lookup"><span data-stu-id="7a832-113">Cache Policy</span></span>](../../../docs/framework/network-programming/cache-policy.md)  
 [<span data-ttu-id="7a832-114">Konum Temelli Önbellek İlkeleri</span><span class="sxs-lookup"><span data-stu-id="7a832-114">Location-Based Cache Policies</span></span>](../../../docs/framework/network-programming/location-based-cache-policies.md)  
 [<span data-ttu-id="7a832-115">Saat Temelli Önbellek İlkeleri</span><span class="sxs-lookup"><span data-stu-id="7a832-115">Time-Based Cache Policies</span></span>](../../../docs/framework/network-programming/time-based-cache-policies.md)  
 [<span data-ttu-id="7a832-116">\<requestCaching > öğesi (ağ ayarları)</span><span class="sxs-lookup"><span data-stu-id="7a832-116">\<requestCaching> Element (Network Settings)</span></span>](../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)
