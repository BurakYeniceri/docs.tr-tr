---
title: "API ağ geçidi düzeni karşı doğrudan istemci mikro hizmet iletişim"
description: "Kapsayıcılı .NET uygulamaları için .NET mikro mimarisi | API ağ geçidi düzeni karşı doğrudan istemci mikro hizmet iletişim"
keywords: "Docker, mikro, ASP.NET, kapsayıcı, API ağ geçidi"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: c8227ec47888c7cf361f34c4c85a09c0666f886e
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2017
---
# <a name="direct-client-to-microservice-communication-versus-the-api-gateway-pattern"></a><span data-ttu-id="cd618-104">API ağ geçidi düzeni karşı doğrudan istemci mikro hizmet iletişim</span><span class="sxs-lookup"><span data-stu-id="cd618-104">Direct client-to-microservice communication versus the API Gateway pattern</span></span>

<span data-ttu-id="cd618-105">Mikro mimarisinde her mikro hizmet (genellikle) fine‑grained uç noktalar kümesi sunar.</span><span class="sxs-lookup"><span data-stu-id="cd618-105">In a microservices architecture, each microservice exposes a set of (typically) fine‑grained endpoints.</span></span> <span data-ttu-id="cd618-106">Bu bölümde açıklandığı gibi bu olgu client‑to‑microservice iletişim etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-106">This fact can impact the client‑to‑microservice communication, as explained in this section.</span></span>

## <a name="direct-client-to-microservice-communication"></a><span data-ttu-id="cd618-107">Doğrudan istemci mikro hizmet iletişim</span><span class="sxs-lookup"><span data-stu-id="cd618-107">Direct client-to-microservice communication</span></span>

<span data-ttu-id="cd618-108">Bir doğrudan istemci mikro hizmet iletişim mimarisi kullanan olası bir yaklaşımdır.</span><span class="sxs-lookup"><span data-stu-id="cd618-108">A possible approach is to use a direct client-to-microservice communication architecture.</span></span> <span data-ttu-id="cd618-109">Bu yaklaşımda, bir istemci uygulaması mikro doğrudan bazıları için Şekil 4-12'de gösterildiği gibi isteğinde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-109">In this approach, a client app can make requests directly to some of the microservices, as shown in Figure 4-12.</span></span>

![](./media/image12.png)

<span data-ttu-id="cd618-110">**Şekil 4-12**.</span><span class="sxs-lookup"><span data-stu-id="cd618-110">**Figure 4-12**.</span></span> <span data-ttu-id="cd618-111">Bir doğrudan istemci mikro hizmet iletişim mimarisi kullanma</span><span class="sxs-lookup"><span data-stu-id="cd618-111">Using a direct client-to-microservice communication architecture</span></span>

<span data-ttu-id="cd618-112">Bu yaklaşım.</span><span class="sxs-lookup"><span data-stu-id="cd618-112">In this approach.</span></span> <span data-ttu-id="cd618-113">Her mikro hizmet bazen her mikro hizmet için farklı bir TCP bağlantı noktası ile ortak bir uç nokta vardır.</span><span class="sxs-lookup"><span data-stu-id="cd618-113">each microservice has a public endpoint, sometimes with a different TCP port for each microservice.</span></span> <span data-ttu-id="cd618-114">Belirli bir hizmet için bir URL örneği Azure aşağıdaki URL'de olabilir:</span><span class="sxs-lookup"><span data-stu-id="cd618-114">An example of a URL for a particular service could be the following URL in Azure:</span></span>

<span data-ttu-id="cd618-115"><http://eshoponcontainers.westus.cloudapp.Azure.com:88 /></span><span class="sxs-lookup"><span data-stu-id="cd618-115"><http://eshoponcontainers.westus.cloudapp.azure.com:88/></span></span>

<span data-ttu-id="cd618-116">URL kümede kullanılan yük dengeleyiciye eşleyen bir küme, temel bir üretim ortamında hangi sırayla isteklerini mikro arasında dağıtır.</span><span class="sxs-lookup"><span data-stu-id="cd618-116">In a production environment based on a cluster, that URL would map to the load balancer used in the cluster, which in turn distributes the requests across the microservices.</span></span> <span data-ttu-id="cd618-117">Üretim ortamlarında gibi uygulama teslim denetleyici (ADC) olabilir [Azure uygulama ağ geçidi](https://docs.microsoft.com/azure/application-gateway/application-gateway-introduction) , mikro ve Internet arasında.</span><span class="sxs-lookup"><span data-stu-id="cd618-117">In production environments, you could have an Application Delivery Controller (ADC) like [Azure Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-introduction) between your microservices and the Internet.</span></span> <span data-ttu-id="cd618-118">Bu, yalnızca Yük Dengeleme gerçekleştirir, ancak SSL sonlandırma sunarak hizmetlerinizi korur saydam bir katmanı görür.</span><span class="sxs-lookup"><span data-stu-id="cd618-118">This acts as a transparent tier that not only performs load balancing, but secures your services by offering SSL termination.</span></span> <span data-ttu-id="cd618-119">Bu CPU-yoğun SSL sonlandırma ve Azure uygulama ağ geçidi için yönlendirme diğer görevlerini boşaltarak konaklarınızın yükünü artırır.</span><span class="sxs-lookup"><span data-stu-id="cd618-119">This improves the load of your hosts by offloading CPU-intensive SSL termination and other routing duties to the Azure Application Gateway.</span></span> <span data-ttu-id="cd618-120">Herhangi bir durumda, bir yük dengeleyici ve ADC bir mantıksal uygulama mimarisi açısından bakıldığında görünmez.</span><span class="sxs-lookup"><span data-stu-id="cd618-120">In any case, a load balancer and ADC are transparent from a logical application architecture point of view.</span></span>

<span data-ttu-id="cd618-121">Bir doğrudan istemci mikro hizmet iletişim mimarisi özellikle istemci uygulaması bir ASP.NET MVC uygulaması gibi bir sunucu tarafı web uygulaması ise küçük mikro hizmet tabanlı bir uygulama için iyi yeterli olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-121">A direct client-to-microservice communication architecture could be good enough for a small microservice-based application, especially if the client app is a server-side web application like an ASP.NET MVC app.</span></span> <span data-ttu-id="cd618-122">Ancak, büyük ve karmaşık mikro hizmet tabanlı uygulamalar (örneğin, mikro hizmet türleri düzinelerce işlerken) derlerken ve özellikle istemci uygulamaları uzak mobil uygulamalar veya SPA web uygulamaları olduğunda bu yaklaşımı bazı sorunlar yüzler.</span><span class="sxs-lookup"><span data-stu-id="cd618-122">However, when you build large and complex microservice-based applications (for example, when handling dozens of microservice types), and especially when the client apps are remote mobile apps or SPA web applications, that approach faces a few issues.</span></span>

<span data-ttu-id="cd618-123">Mikro üzerinde temel büyük bir uygulama geliştirirken, aşağıdaki soruları göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="cd618-123">Consider the following questions when developing a large application based on microservices:</span></span>

-   <span data-ttu-id="cd618-124">*Nasıl istemci uygulamaları arka uç isteklerine sayısını en aza indirmek ve birden çok mikro chatty iletişimi azaltmak?*</span><span class="sxs-lookup"><span data-stu-id="cd618-124">*How can client apps minimize the number of requests to the backend and reduce chatty communication to multiple microservices?*</span></span>

<span data-ttu-id="cd618-125">Tek bir kullanıcı Arabirimi ekran oluşturmak için birden çok mikro etkileşim Internet üzerinden gidiş-dönüş sayısını artırır.</span><span class="sxs-lookup"><span data-stu-id="cd618-125">Interacting with multiple microservices to build a single UI screen increases the number of roundtrips across the Internet.</span></span> <span data-ttu-id="cd618-126">Bu gecikme süresi ve kullanıcı Arabirimi tarafında karmaşıklığını artırır.</span><span class="sxs-lookup"><span data-stu-id="cd618-126">This increases latency and complexity on the UI side.</span></span> <span data-ttu-id="cd618-127">İdeal olarak, yanıtları verimli bir şekilde sunucu tarafı toplanması gerektiğini — Bu paralel olarak birden çok veri parçalarını geri dönün ve hazır olduğunda hemen bazı kullanıcı Arabirimi verileri gösterebilir beri gecikmesini azaltır.</span><span class="sxs-lookup"><span data-stu-id="cd618-127">Ideally, responses should be efficiently aggregated in the server side—this reduces latency, since multiple pieces of data come back in parallel and some UI can show data as soon as it is ready.</span></span>

-   <span data-ttu-id="cd618-128">*Nasıl arası kesme sorunları yetkilendirme, veri dönüşümleri ve dinamik istek gönderme gibi işleyebilir?*</span><span class="sxs-lookup"><span data-stu-id="cd618-128">*How can you handle cross-cutting concerns such as authorization, data transformations, and dynamic request dispatching?*</span></span>

<span data-ttu-id="cd618-129">Güvenlik ve yetkilendirme her mikro hizmet üzerinde önemli geliştirme çaba gerektirebilir gibi güvenlik ve çapraz kesme sorunları uygulama.</span><span class="sxs-lookup"><span data-stu-id="cd618-129">Implementing security and cross-cutting concerns like security and authorization on every microservice can require significant development effort.</span></span> <span data-ttu-id="cd618-130">Dışarıdan kendilerine doğrudan erişimi kısıtlamak için ve bir API ağ geçidi gibi merkezi bir yerde bu arası kesme sorunları uygulamak için bu hizmetlerin Docker ana bilgisayar veya iç küme içinde sahip olası bir yaklaşımdır.</span><span class="sxs-lookup"><span data-stu-id="cd618-130">A possible approach is to have those services within the Docker host or internal cluster, in order to restrict direct access to them from the outside, and to implement those cross-cutting concerns in a centralized place, like an API Gateway.</span></span>

-   <span data-ttu-id="cd618-131">*İstemci uygulamaları Internet kolay protokoller kullanan Hizmetleri ile nasıl iletişim kurabilir?*</span><span class="sxs-lookup"><span data-stu-id="cd618-131">*How can client apps communicate with services that use non-Internet-friendly protocols?*</span></span>

<span data-ttu-id="cd618-132">(AMQP veya ikili protokolleri gibi) sunucu tarafında kullanılan protokoller istemci uygulamaları genellikle desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="cd618-132">Protocols used on the server side (like AMQP or binary protocols) are usually not supported in client apps.</span></span> <span data-ttu-id="cd618-133">Bu nedenle, istekleri HTTP/HTTPS gibi protokoller üzerinden gerçekleşen ve gerekir diğer protokoller için daha sonra çevrilmesi.</span><span class="sxs-lookup"><span data-stu-id="cd618-133">Therefore, requests must be performed through protocols like HTTP/HTTPS and translated to the other protocols afterwards.</span></span> <span data-ttu-id="cd618-134">A *man-in--middle* yaklaşım, bu durumda yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-134">A *man-in-the-middle* approach can help in this situation.</span></span>

-   <span data-ttu-id="cd618-135">*Nasıl özellikle mobil uygulamalar için yapılan bir cephesi Şekil?*</span><span class="sxs-lookup"><span data-stu-id="cd618-135">*How can you shape a façade especially made for mobile apps?*</span></span>

<span data-ttu-id="cd618-136">Birden çok mikro API için farklı istemci uygulamalarının ihtiyaçlarını iyi tasarlanmamış olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-136">The API of multiple microservices might not be well designed for the needs of different client applications.</span></span> <span data-ttu-id="cd618-137">Örneğin, bir mobil uygulama gereksinimlerini bir web uygulaması gereksinimlerini farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-137">For instance, the needs of a mobile app might be different than the needs of a web app.</span></span> <span data-ttu-id="cd618-138">Mobil uygulamalar için daha veri yanıtları daha etkili olması için en iyi duruma gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-138">For mobile apps, you might need to optimize even further so that data responses can be more efficient.</span></span> <span data-ttu-id="cd618-139">Birden çok mikro veri toplayarak ve tek bir veri kümesi döndüren ve bazı durumlarda mobil uygulama tarafından gerekli değildir yanıt herhangi bir veri ortadan bunu yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd618-139">You might do this by aggregating data from multiple microservices and returning a single set of data, and sometimes eliminating any data in the response that is not needed by the mobile app.</span></span> <span data-ttu-id="cd618-140">Ve tabi ki, bu verileri sıkıştırmak.</span><span class="sxs-lookup"><span data-stu-id="cd618-140">And, of course, you might compress that data.</span></span> <span data-ttu-id="cd618-141">Yeniden cephesi veya mobil uygulama ve mikro hizmetler arasında API bu senaryo için kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-141">Again, a façade or API in between the mobile app and the microservices can be convenient for this scenario.</span></span>

## <a name="using-an-api-gateway"></a><span data-ttu-id="cd618-142">Bir API ağ geçidi kullanma</span><span class="sxs-lookup"><span data-stu-id="cd618-142">Using an API Gateway</span></span>

<span data-ttu-id="cd618-143">Tasarım ve büyük veya karmaşık mikro hizmet tabanlı uygulamaları birden çok istemci uygulamaları oluşturmak, dikkate alınması gereken iyi bir yaklaşım olabilir bir [API ağ geçidi](http://microservices.io/patterns/apigateway.html).</span><span class="sxs-lookup"><span data-stu-id="cd618-143">When you design and build large or complex microservice-based applications with multiple client apps, a good approach to consider can be an [API Gateway](http://microservices.io/patterns/apigateway.html).</span></span> <span data-ttu-id="cd618-144">Bu, tek giriş noktası belirli mikro grupları sağlayan bir hizmettir.</span><span class="sxs-lookup"><span data-stu-id="cd618-144">This is a service that provides a single entry point for certain groups of microservices.</span></span> <span data-ttu-id="cd618-145">Aşağıdakine benzer [cephesi düzeni](https://en.wikipedia.org/wiki/Facade_pattern) object‑oriented tasarımdan ancak bu durumda, dağıtılmış bir sistemde bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="cd618-145">It is similar to the [Facade pattern](https://en.wikipedia.org/wiki/Facade_pattern) from object‑oriented design, but in this case, it is part of a distributed system.</span></span> <span data-ttu-id="cd618-146">API ağ geçidi düzeni bazen "arka uç ön uç için" olarak bilinen [(BFF)](http://samnewman.io/patterns/architectural/bff/) istemci uygulaması gereksinimlerini düşünmek sırasında oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="cd618-146">The API Gateway pattern is also sometimes known as the “backend for frontend” [(BFF)](http://samnewman.io/patterns/architectural/bff/) because you build it while thinking about the needs of the client app.</span></span>

<span data-ttu-id="cd618-147">Şekil 4-13 özel bir API ağ geçidi mikro hizmet tabanlı bir mimariye nasıl sığabilecek gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd618-147">Figure 4-13 shows how a custom API Gateway can fit into a microservice-based architecture.</span></span>
<span data-ttu-id="cd618-148">Bu diyagramda vurgulamak önemlidir, birden çok bakan tek özel API ağ geçidi hizmeti kullanarak ve farklı istemci uygulamaları.</span><span class="sxs-lookup"><span data-stu-id="cd618-148">It is important to highlight that in that diagram, you would be using a single custom API Gateway service facing multiple and different client apps.</span></span> <span data-ttu-id="cd618-149">Olgu API ağ geçidi hizmetinizi büyüyen gelişen ve için önemli bir risk olabilir istemci uygulamalardan birçok farklı gereksinimlerine göre.</span><span class="sxs-lookup"><span data-stu-id="cd618-149">That fact can be an important risk because your API Gateway service will be growing and evolving based on many different requirements from the client apps.</span></span> <span data-ttu-id="cd618-150">Sonuç olarak, bu farklı ihtiyaçları bloated olacak ve etkili bir şekilde bir tek yapılı uygulama veya tek yapılı hizmet oldukça benzer olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-150">Eventually, it will be bloated because of those different needs and effectively it could be pretty similar to a monolithic application or monolithic service.</span></span> <span data-ttu-id="cd618-151">Çok API ağ geçidi birden çok hizmet ya da birden çok daha küçük API ağ geçidi, form faktörünün türü, her bir örneği için bölmeniz önerilir nedeni budur.</span><span class="sxs-lookup"><span data-stu-id="cd618-151">That is why it is very much recommended to split the API Gateway in multiple services or multiple smaller API Gateways, one per form-factor type, for instance.</span></span>

![](./media/image13.png)

<span data-ttu-id="cd618-152">**Şekil 4-13**.</span><span class="sxs-lookup"><span data-stu-id="cd618-152">**Figure 4-13**.</span></span> <span data-ttu-id="cd618-153">Bir API ağ geçidi kullanılarak uygulanan özel bir Web API hizmet olarak</span><span class="sxs-lookup"><span data-stu-id="cd618-153">Using an API Gateway implemented as a custom Web API service</span></span>

<span data-ttu-id="cd618-154">Bu örnekte, bir kapsayıcı olarak çalışan özel bir Web API hizmeti olarak API ağ geçidi uygulanması.</span><span class="sxs-lookup"><span data-stu-id="cd618-154">In this example, the API Gateway would be implemented as a custom Web API service running as a container.</span></span>

<span data-ttu-id="cd618-155">Böylece her istemci uygulaması gereksinimleri için farklı bir cephesi sahip belirtildiği gibi birkaç API ağ geçidi uygulaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd618-155">As mentioned, you should implement several API Gateways so that you can have a different façade for the needs of each client app.</span></span> <span data-ttu-id="cd618-156">Her API ağ geçidi farklı bir sağlayabilir API uyarlanmış büyük olasılıkla bile istemci form faktörünü hangi underneath çağırır birden çok dahili mikro belirli bağdaştırıcı kodu uygulayarak göre her bir istemci uygulama için.</span><span class="sxs-lookup"><span data-stu-id="cd618-156">Each API Gateway can provide a different API tailored for each client app, possibly even based on the client form factor by implementing specific adapter code which underneath calls multiple internal microservices.</span></span>

<span data-ttu-id="cd618-157">Özel bir API ağ geçidi genellikle bir veri toplayıcısı olduğundan, kendisiyle dikkatli olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd618-157">Since a custom API Gateway is usually a data aggregator, you need to be careful with it.</span></span> <span data-ttu-id="cd618-158">Genellikle tek bir API uygulamanızın tüm iç mikro toplayarak ağ geçidi için iyi bir fikir değil.</span><span class="sxs-lookup"><span data-stu-id="cd618-158">Usually it isn't a good idea to have a single API Gateway aggregating all the internal microservices of your application.</span></span> <span data-ttu-id="cd618-159">Bulursa, bir tek yapılı toplayıcısı veya orchestrator olarak davranır ve tüm mikro eşleyerek mikro hizmet otonomisi ihlal ediyor.</span><span class="sxs-lookup"><span data-stu-id="cd618-159">If it does, it acts as a monolithic aggregator or orchestrator and violates microservice autonomy by coupling all the microservices.</span></span> <span data-ttu-id="cd618-160">Bu nedenle, API ağ geçitleri iş sınırları ve değil act bağlı olarak tüm uygulama için bir Toplayıcıya yinelenmeli.</span><span class="sxs-lookup"><span data-stu-id="cd618-160">Therefore, the API Gateways should be segregated based on business boundaries and not act as an aggregator for the whole application.</span></span>

<span data-ttu-id="cd618-161">Bazen ayrıntılı bir API ağ geçidi, bir mikro hizmet kendisi de ve bir etki alanı veya iş adı ve ilgili verileri bile sahip.</span><span class="sxs-lookup"><span data-stu-id="cd618-161">Sometimes a granular API Gateway can also be a microservice by itself, and even have a domain or business name and related data.</span></span> <span data-ttu-id="cd618-162">İş veya etki alanı tarafından dikte API ağ geçidi sınırları daha iyi bir tasarım almak için yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="cd618-162">Having the API Gateway’s boundaries dictated by the business or domain will help you to get a better design.</span></span>

<span data-ttu-id="cd618-163">Hassas bir API ağ geçidi kavramı bir UI birleşim hizmetine benzer olduğundan ayrıntı düzeyi API ağ geçidi katmanındaki mikro üzerinde göre daha gelişmiş bileşik UI uygulamalar için özellikle yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-163">Granularity in the API Gateway tier can be especially useful for more advanced composite UI applications based on microservices, because the concept of a fine-grained API Gateway is similar to a UI composition service.</span></span> <span data-ttu-id="cd618-164">Daha sonra bu konuda aşağıdakiler ele [bileşik kullanıcı Arabirimi oluşturma tabanlı mikro üzerinde](#creating-composite-ui-based-on-microservices-including-visual-ui-shape-and-layout-generated-by-multiple-microservices).</span><span class="sxs-lookup"><span data-stu-id="cd618-164">We discuss this later in the [Creating composite UI based on microservices](#creating-composite-ui-based-on-microservices-including-visual-ui-shape-and-layout-generated-by-multiple-microservices).</span></span>

<span data-ttu-id="cd618-165">Bu nedenle, birçok Orta ve büyük-ölçekli uygulamalar için özel olarak geliştirilmiş bir API ağ geçidi genellikle iyi bir yaklaşım kullanmaktır ancak tek tek yapılı toplayıcısı ya da benzersiz merkezi özel API ağ geçidi olarak değil.</span><span class="sxs-lookup"><span data-stu-id="cd618-165">Therefore, for many medium- and large-size applications, using a custom-built API Gateway is usually a good approach, but not as a single monolithic aggregator or unique central custom API Gateway.</span></span>

<span data-ttu-id="cd618-166">Başka bir yaklaşım gibi bir ürün kullanmaktır [Azure API Management](https://azure.microsoft.com/services/api-management/) Şekil 4-14'te gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="cd618-166">Another approach is to use a product like [Azure API Management](https://azure.microsoft.com/services/api-management/) as shown in Figure 4-14.</span></span> <span data-ttu-id="cd618-167">Bu yaklaşım yalnızca API ağ geçidi gereksinimlerinizi çözer, ancak, API'lerden Öngörüler toplama gibi özellikler sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd618-167">This approach not only solves your API Gateway needs, but provides features like gathering insights from your APIs.</span></span> <span data-ttu-id="cd618-168">API yönetim çözümünü kullanıyorsanız, bir API ağ geçidi yalnızca bir bu tam API yönetimi çözümü içinde bileşenidir.</span><span class="sxs-lookup"><span data-stu-id="cd618-168">If you are using an API management solution, an API Gateway is only a component within that full API management solution.</span></span>

![](./media/image14.png)

<span data-ttu-id="cd618-169">**Şekil 4-14**.</span><span class="sxs-lookup"><span data-stu-id="cd618-169">**Figure 4-14**.</span></span> <span data-ttu-id="cd618-170">API ağ geçidiniz için Azure API Management kullanma</span><span class="sxs-lookup"><span data-stu-id="cd618-170">Using Azure API Management for your API Gateway</span></span>

<span data-ttu-id="cd618-171">Bu tür bir API ağ geçidi "ince" olduğundan Azure API Management, tek bir API ağ geçidi olabilir olgu gibi bir ürün kullanarak kadar riskli olmadığı durumlarda, bu durumda, bir tek yapılı gelişmesi özel C# kod uygulamaz anlamına gelir Bileşen.</span><span class="sxs-lookup"><span data-stu-id="cd618-171">In this case, when using a product like Azure API Management, the fact that you might have a single API Gateway is not so risky because these kinds of API Gateways are "thinner", meaning that you don't implement custom C# code that could evolve towards a monolithic component.</span></span> 

<span data-ttu-id="cd618-172">Bu tür bir ürünün daha giriş iletişimi, burada, ayrıca iç mikro API'lerden filtre yanı sıra bu tek katmandaki yayımlanan API'ler yetkilendirme uygulamak için ters proxy gibi davranır.</span><span class="sxs-lookup"><span data-stu-id="cd618-172">This type of product acts more like a reverse proxy for ingress communication, where you can also filter the APIs from the internal microservices plus apply authorization to the published APIs in this single tier.</span></span>

<span data-ttu-id="cd618-173">Bir API Management sistem Yardım'dan kullanılabilir bilgiler Apı'lerinizi nasıl kullanılacağı konusunda bilgi edinmek ve nasıl performans gösterdiğini.</span><span class="sxs-lookup"><span data-stu-id="cd618-173">The insights available from an API Management system help you get an understanding of how your APIs are being used and how they are performing.</span></span> <span data-ttu-id="cd618-174">Gerçek zamanlı analiz raporları görüntülemenize izin vererek ve işinizin etkileyebilecek eğilimleri tanımlama bunu.</span><span class="sxs-lookup"><span data-stu-id="cd618-174">They do this by letting you view near real-time analytics reports and identifying trends that might impact your business.</span></span> <span data-ttu-id="cd618-175">Ayrıca, hakkında daha fazla çevrimiçi ve çevrimdışı analiz için istek ve yanıt etkinlik günlükleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-175">Plus, you can have logs about request and response activity for further online and offline analysis.</span></span>

<span data-ttu-id="cd618-176">Azure API Management ile bir anahtar, bir belirteç ve IP filtresini kullanarak Apı'lerinizi güvenliğini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd618-176">With Azure API Management, you can secure your APIs using a key, a token, and IP filtering.</span></span> <span data-ttu-id="cd618-177">Bu özellikler, esnek ve hassas kotaları zorlamak ve oran sınırları, Şekil ve ilkelerini kullanarak Apı'lerinizi davranışını değiştirmek ve yanıt önbelleğe alma ile performansı sağlar.</span><span class="sxs-lookup"><span data-stu-id="cd618-177">These features let you enforce flexible and fine-grained quotas and rate limits, modify the shape and behavior of your APIs using policies, and improve performance with response caching.</span></span>

<span data-ttu-id="cd618-178">Bu kılavuz ve başvuru örnek uygulaması (eShopOnContainers), biz mimarisi daha basit ve özel yapılan kapsayıcılı mimarisi için Azure API Management gibi PaaS ürünler kullanmadan düz kapsayıcılarında odaklanmak için kısıtlayan.</span><span class="sxs-lookup"><span data-stu-id="cd618-178">In this guide and the reference sample application (eShopOnContainers), we are limiting the architecture to a simpler and custom-made containerized architecture in order to focus on plain containers without using PaaS products like Azure API Management.</span></span> <span data-ttu-id="cd618-179">Ancak, Microsoft Azure'da dağıtılan büyük mikro hizmet tabanlı uygulamalar için gözden geçirmek ve Azure API Management temel olarak, API ağ geçitleri için benimsemek için öneririz.</span><span class="sxs-lookup"><span data-stu-id="cd618-179">But for large microservice-based applications that are deployed into Microsoft Azure, we encourage you to review and adopt Azure API Management as the base for your API Gateways.</span></span>

## <a name="drawbacks-of-the-api-gateway-pattern"></a><span data-ttu-id="cd618-180">API ağ geçidi düzeni eksileri</span><span class="sxs-lookup"><span data-stu-id="cd618-180">Drawbacks of the API Gateway pattern</span></span>

-   <span data-ttu-id="cd618-181">En önemli dezavantajı, bir API ağ geçidi uyguladığınızda, iç mikro ile bu katmanı Kuplaj olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="cd618-181">The most important drawback is that when you implement an API Gateway, you are coupling that tier with the internal microservices.</span></span> <span data-ttu-id="cd618-182">Bu gibi bağlantı uygulamanız için ciddi sorunlar getirebilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-182">Coupling like this might introduce serious difficulties for your application.</span></span> <span data-ttu-id="cd618-183">Bu olası güçlük "Yeni ESB" olarak kaldırmalıdır Vaster Clemens Azure Service Bus ekibine adresindeki Mimarı başvurur "[Mesajlaşma ve mikro](https://www.youtube.com/watch?v=rXi5CLjIQ9k)" GOTO 2016 oturumunda.</span><span class="sxs-lookup"><span data-stu-id="cd618-183">Clemens Vaster, architect at the Azure Service Bus team, refers to this potential difficulty as “the new ESB” in his "[Messaging and Microservices](https://www.youtube.com/watch?v=rXi5CLjIQ9k)" session at GOTO 2016.</span></span>

-   <span data-ttu-id="cd618-184">Mikro API ağ geçidi kullanarak bir ek olası tek hata noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd618-184">Using a microservices API Gateway creates an additional possible single point of failure.</span></span>

-   <span data-ttu-id="cd618-185">Bir API ağ geçidi artan yanıt süresi ek ağ çağrısı nedeniyle ortaya çıkarabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-185">An API Gateway can introduce increased response time due to the additional network call.</span></span> <span data-ttu-id="cd618-186">Ancak, bu ek çağrı genellikle, arabirim, bir istemcinin doğrudan iç mikro çağırma çok chatty olandan daha az etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="cd618-186">However, this extra call usually has less impact than having a client interface that is too chatty directly calling the internal microservices.</span></span>

-   <span data-ttu-id="cd618-187">Out düzgün ölçeklendirilmiş değil, API ağ geçidi bir ayak bağı olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-187">If not scaled out properly, the API Gateway can become a bottleneck.</span></span>

-   <span data-ttu-id="cd618-188">Özel mantık ve verileri toplama içeriyorsa, bir API ağ geçidi ek geliştirme maliyetini ve gelecekteki bakım gerektirir.</span><span class="sxs-lookup"><span data-stu-id="cd618-188">An API Gateway requires additional development cost and future maintenance if it includes custom logic and data aggregation.</span></span> <span data-ttu-id="cd618-189">Geliştiriciler API ağ geçidi her mikro 's uç noktalarını kullanıma sunmak için güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd618-189">Developers must update the API Gateway in order to expose each microservice’s endpoints.</span></span> <span data-ttu-id="cd618-190">Ayrıca, uygulama değişiklikleri iç mikro API ağ geçidi düzeyinde kod değişiklikleri neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-190">Moreover, implementation changes in the internal microservices might cause code changes at the API Gateway level.</span></span> <span data-ttu-id="cd618-191">Ancak, API ağ geçidi yalnızca güvenlik, günlüğe kaydetme ve sürüm oluşturma uygulama varsa (as Azure API Management kullanırken), bu ek geliştirme maliyet geçerli.</span><span class="sxs-lookup"><span data-stu-id="cd618-191">However, if the API Gateway is just applying security, logging, and versioning (as when using Azure API Management), this additional development cost might not apply.</span></span>

-   <span data-ttu-id="cd618-192">API ağ geçidi tek bir takım tarafından geliştirilen bir geliştirme performans sorunu olabilir.</span><span class="sxs-lookup"><span data-stu-id="cd618-192">If the API Gateway is developed by a single team, there can be a development bottleneck.</span></span> <span data-ttu-id="cd618-193">Birkaç fined düzey API farklı istemci ihtiyaçlarına yanıt veren ağ geçitleri için daha iyi bir yaklaşım neden olan başka bir neden de budur.</span><span class="sxs-lookup"><span data-stu-id="cd618-193">This is another reason why a better approach is to have several fined-grained API Gateways that respond to different client needs.</span></span> <span data-ttu-id="cd618-194">Ayrıca API ağ geçidi dahili olarak birden çok alanları veya iç mikro üzerinde çalışan farklı ekip tarafından sahip olunan Katmanlar kurabilmeleri.</span><span class="sxs-lookup"><span data-stu-id="cd618-194">You could also segregate the API Gateway internally into multiple areas or layers that are owned by the different teams working on the internal microservices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd618-195">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cd618-195">Additional resources</span></span>

-   <span data-ttu-id="cd618-196">**Charles Uludağ. Desen: API ağ geçidi / arka uç için ön uç**
    [*http://microservices.io/patterns/apigateway.html*](http://microservices.io/patterns/apigateway.html)</span><span class="sxs-lookup"><span data-stu-id="cd618-196">**Charles Richardson. Pattern: API Gateway / Backend for Front-End**
[*http://microservices.io/patterns/apigateway.html*](http://microservices.io/patterns/apigateway.html)</span></span>

-   <span data-ttu-id="cd618-197">**Azure API Management**
    [*https://azure.microsoft.com/services/api-management/*](https://azure.microsoft.com/services/api-management/)</span><span class="sxs-lookup"><span data-stu-id="cd618-197">**Azure API Management**
[*https://azure.microsoft.com/services/api-management/*](https://azure.microsoft.com/services/api-management/)</span></span>

-   <span data-ttu-id="cd618-198">**UDI Dahan. Birleşim hizmet odaklı**\\</span><span class="sxs-lookup"><span data-stu-id="cd618-198">**Udi Dahan. Service Oriented Composition**\\</span></span>
    [<span data-ttu-id="cd618-199">*http://udidahan.com/2014/07/30/Service-oriented-Composition-With-video/*</span><span class="sxs-lookup"><span data-stu-id="cd618-199">*http://udidahan.com/2014/07/30/service-oriented-composition-with-video/*</span></span>](http://udidahan.com/2014/07/30/service-oriented-composition-with-video/)

-   <span data-ttu-id="cd618-200">**Clemens Vasters. Mesajlaşma ve mikro GOTO 2016 adresindeki** (video) [ *https://www.youtube.com/watch?v=rXi5CLjIQ9k*](https://www.youtube.com/watch?v=rXi5CLjIQ9k)</span><span class="sxs-lookup"><span data-stu-id="cd618-200">**Clemens Vasters. Messaging and Microservices at GOTO 2016** (video) [*https://www.youtube.com/watch?v=rXi5CLjIQ9k*](https://www.youtube.com/watch?v=rXi5CLjIQ9k)</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="cd618-201">[Önceki] (tanımlamak-mikro hizmet-etki-model-boundaries.md) [sonraki] (iletişimi-içinde-mikro hizmet-architecture.md)</span><span class="sxs-lookup"><span data-stu-id="cd618-201">[Previous] (identify-microservice-domain-model-boundaries.md) [Next] (communication-in-microservice-architecture.md)</span></span>