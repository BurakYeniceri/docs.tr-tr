---
title: "Bağlantıları yönetme"
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
- Internet, connections
- HTTP, classes for connecting
- requesting data from Internet, connections
- sending data, connections
- receiving data, connections
- ServicePoint class, about ServicePoint class
- response to Internet request, connections
- connections [.NET Framework], classes
- network resources, connections
- downloading Internet resources, connections
- ServicePointManager class, about ServicePointManager class
ms.assetid: 9b3d3de7-189f-4f7d-81ae-9c29c441aaaa
caps.latest.revision: "9"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: a4d0ca3b6aed1213405dc24f322b53a21dbd4fbe
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="managing-connections"></a><span data-ttu-id="1d322-102">Bağlantıları yönetme</span><span class="sxs-lookup"><span data-stu-id="1d322-102">Managing Connections</span></span>
<span data-ttu-id="1d322-103">Veri kaynaklarına bağlanmak için HTTP kullanan uygulamalar, .NET Framework'ün kullanabileceğiniz <xref:System.Net.ServicePoint> ve <xref:System.Net.ServicePointManager> sınıfları internet bağlantıları yönetmek ve bunları en uygun ölçek ve performans elde etmek amacıyla.</span><span class="sxs-lookup"><span data-stu-id="1d322-103">Applications that use HTTP to connect to data resources can use the .NET Framework's <xref:System.Net.ServicePoint> and <xref:System.Net.ServicePointManager> classes to manage connections to the Internet and to help them achieve optimum scale and performance.</span></span>  
  
 <span data-ttu-id="1d322-104">**ServicePoint** sınıfı, bir uygulama için uygulama bağlanabilir Internet kaynaklarına erişmek için bir uç nokta ile sağlar.</span><span class="sxs-lookup"><span data-stu-id="1d322-104">The **ServicePoint** class provides an application with an endpoint to which the application can connect to access Internet resources.</span></span> <span data-ttu-id="1d322-105">Her **ServicePoint** yardımcı performansını artırmak için bağlantıları arasında en iyi duruma getirme bilgilerini paylaşarak bir Internet sunucusu ile bağlantı iyileştirmek bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="1d322-105">Each **ServicePoint** contains information that helps optimize connections with an Internet server by sharing optimization information between connections to improve performance.</span></span>  
  
 <span data-ttu-id="1d322-106">Her **ServicePoint** bir Tekdüzen Kaynak Tanımlayıcısı (URI) tarafından tanımlanır ve düzeni tanımlayıcısı ve ana bilgisayar parçaları URI'sinin göre kategorilere ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="1d322-106">Each **ServicePoint** is identified by a Uniform Resource Identifier (URI) and is categorized according to the scheme identifier and host fragments of the URI.</span></span> <span data-ttu-id="1d322-107">Örneğin, aynı **ServicePoint** örneği aynı düzen tanımlayıcısı (http) ve ana bilgisayar olduğundan URI'ler http://www.contoso.com/index.htm ve http://www.contoso.com/news.htm?date=today isteklerine sağlamak parçaları (www.contoso.com).</span><span class="sxs-lookup"><span data-stu-id="1d322-107">For example, the same **ServicePoint** instance would provide requests to the URIs http://www.contoso.com/index.htm and http://www.contoso.com/news.htm?date=today since they have the same scheme identifier (http) and host fragments (www.contoso.com).</span></span> <span data-ttu-id="1d322-108">Uygulama zaten sunucu www.contoso.com kalıcı bir bağlantı varsa, iki bağlantı oluşturmak için gereken önleme hem istekleri almak için bu bağlantıyı kullanır.</span><span class="sxs-lookup"><span data-stu-id="1d322-108">If the application already has a persistent connection to the server www.contoso.com, it uses that connection to retrieve both requests, avoiding the need to create two connections.</span></span>  
  
 <span data-ttu-id="1d322-109">**ServicePointManager** oluşturma ve yok etme yöneten statik bir sınıftır **ServicePoint** örnekleri.</span><span class="sxs-lookup"><span data-stu-id="1d322-109">**ServicePointManager** is a static class that manages the creation and destruction of **ServicePoint** instances.</span></span> <span data-ttu-id="1d322-110">**ServicePointManager** oluşturur bir **ServicePoint** koleksiyonunda var olmayan bir Internet kaynağına uygulama isteğinde bulunduğunda **ServicePoint** örnekleri.</span><span class="sxs-lookup"><span data-stu-id="1d322-110">The **ServicePointManager** creates a **ServicePoint** when the application requests an Internet resource that is not in the collection of existing **ServicePoint** instances.</span></span> <span data-ttu-id="1d322-111">**ServicePoint** örnekleri kendi maksimum boşta kalma süresi aştığınızda veya sayısı yok varolan **ServicePoint** örnekleri üst sınırını aşıyor **ServicePoint**uygulama örneği.</span><span class="sxs-lookup"><span data-stu-id="1d322-111">**ServicePoint** instances are destroyed when they have exceeded their maximum idle time or when the number of existing **ServicePoint** instances exceeds the maximum number of **ServicePoint** instances for the application.</span></span> <span data-ttu-id="1d322-112">Varsayılan en fazla boşta kalma süresi ve en fazla sayısını kontrol edebilirsiniz **ServicePoint** ayarlayarak örnekleri <xref:System.Net.ServicePointManager.MaxServicePointIdleTime%2A> ve <xref:System.Net.ServicePointManager.MaxServicePoints%2A> özellikleri **ServicePointManager**.</span><span class="sxs-lookup"><span data-stu-id="1d322-112">You can control both the default maximum idle time and the maximum number of **ServicePoint** instances by setting the <xref:System.Net.ServicePointManager.MaxServicePointIdleTime%2A> and <xref:System.Net.ServicePointManager.MaxServicePoints%2A> properties on the **ServicePointManager**.</span></span>  
  
 <span data-ttu-id="1d322-113">İstemci ve sunucu arasındaki bağlantı sayısı üzerinde uygulama üretilen işi çarpıcı bir etkisi olabilir.</span><span class="sxs-lookup"><span data-stu-id="1d322-113">The number of connections between a client and server can have a dramatic impact on application throughput.</span></span> <span data-ttu-id="1d322-114">Varsayılan olarak, bir uygulama kullanarak <xref:System.Net.HttpWebRequest> sınıfı, belirli bir sunucuda iki kalıcı bağlantı maksimum kullanır, ancak bir uygulama başına temelinde en fazla bağlantı sayısını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1d322-114">By default, an application using the <xref:System.Net.HttpWebRequest> class uses a maximum of two persistent connections to a given server, but you can set the maximum number of connections on a per-application basis.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1d322-115">HTTP/1.1 belirtimini sunucu başına iki bağlantı uygulamaya bağlantı sayısını sınırlar.</span><span class="sxs-lookup"><span data-stu-id="1d322-115">The HTTP/1.1 specification limits the number of connections from an application to two connections per server.</span></span>  
  
 <span data-ttu-id="1d322-116">En yüksek bağlantı sayısını uygulamanın çalıştığı gerçek koşullara bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1d322-116">The optimum number of connections depends on the actual conditions in which the application runs.</span></span> <span data-ttu-id="1d322-117">Uygulama için kullanılabilir bağlantı sayısını artırmayı uygulama performansını etkileyebilir değil.</span><span class="sxs-lookup"><span data-stu-id="1d322-117">Increasing the number of connections available to the application may not affect application performance.</span></span> <span data-ttu-id="1d322-118">Daha fazla bağlantı etkisini belirlemek için bağlantı sayısı değişen sırasında performans testleri çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="1d322-118">To determine the impact of more connections, run performance tests while varying the number of connections.</span></span> <span data-ttu-id="1d322-119">Statik değiştirerek bir uygulamanın kullandığı bağlantı sayısını değiştirebilirsiniz <xref:System.Net.ServicePointManager.DefaultConnectionLimit%2A> özelliği **ServicePointManager** aşağıdaki kod örneğinde gösterildiği gibi uygulama başlatma sırasında sınıfı.</span><span class="sxs-lookup"><span data-stu-id="1d322-119">You can change the number of connections that an application uses by changing the static <xref:System.Net.ServicePointManager.DefaultConnectionLimit%2A> property on the **ServicePointManager** class at application initialization, as shown in the following code sample.</span></span>  
  
```csharp  
// Set the maximum number of connections per server to 4.  
ServicePointManager.DefaultConnectionLimit = 4;  
```  
  
```vb  
' Set the maximum number of connections per server to 4.  
ServicePointManager.DefaultConnectionLimit = 4  
```  
  
 <span data-ttu-id="1d322-120">Değiştirme **ServicePointManager.DefaultConnectionLimit** özelliği daha önce başlatılmış etkilemez **ServicePoint** örnekleri.</span><span class="sxs-lookup"><span data-stu-id="1d322-120">Changing the **ServicePointManager.DefaultConnectionLimit** property does not affect previously initialized **ServicePoint** instances.</span></span> <span data-ttu-id="1d322-121">Aşağıdaki kod, var olan üzerinde bağlantı sınırı değiştirme gösterir **ServicePoint** depolanan değerine sunucu http://www.contoso.com için `newLimit`.</span><span class="sxs-lookup"><span data-stu-id="1d322-121">The following code demonstrates changing the connection limit on an existing **ServicePoint** for the server http://www.contoso.com to the value stored in `newLimit`.</span></span>  
  
```csharp  
Uri uri = new Uri("http://www.contoso.com/");  
ServicePoint sp = ServicePointManager.FindServicePoint(uri);  
sp.ConnectionLimit = newLimit;  
```  
  
```vb  
Dim uri As New Uri("http://www.contoso.com/")  
Dim sp As ServicePoint = ServicePointManager.FindServicePoint(uri)  
sp.ConnectionLimit = newLimit  
```  
  
## <a name="see-also"></a><span data-ttu-id="1d322-122">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="1d322-122">See Also</span></span>  
 [<span data-ttu-id="1d322-123">Bağlantı Gruplandırma</span><span class="sxs-lookup"><span data-stu-id="1d322-123">Connection Grouping</span></span>](../../../docs/framework/network-programming/connection-grouping.md)  
 [<span data-ttu-id="1d322-124">Uygulama Protokolleri Kullanma</span><span class="sxs-lookup"><span data-stu-id="1d322-124">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)
