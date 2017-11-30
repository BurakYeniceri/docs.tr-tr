---
title: "JSON ve XML ile AJAX Hizmeti Örneği"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 8ea5860d-0c42-4ae9-941a-e07efdd8e29c
caps.latest.revision: "15"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: c0913a94f2fffd74890d7f996b2b103ed52f8d2f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="ajax-service-with-json-and-xml-sample"></a><span data-ttu-id="215d6-102">JSON ve XML ile AJAX Hizmeti Örneği</span><span class="sxs-lookup"><span data-stu-id="215d6-102">AJAX Service with JSON and XML Sample</span></span>
<span data-ttu-id="215d6-103">Bu örnek nasıl kullanılacağı ortaya [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] JavaScript nesne gösterimi (JSON) veya XML veri döndüren bir zaman uyumsuz JavaScript ve XML (AJAX) bir hizmet oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="215d6-103">This sample demonstrates how to use [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] to create an Asynchronous JavaScript and XML (AJAX) service that returns either JavaScript Object Notation (JSON) or XML data.</span></span> <span data-ttu-id="215d6-104">Bir AJAX hizmeti bir Web tarayıcısı istemciden JavaScript kodu kullanarak erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="215d6-104">You can access an AJAX service by using JavaScript code from a Web browser client.</span></span> <span data-ttu-id="215d6-105">Bu örnek derlemeler [temel AJAX hizmeti](../../../../docs/framework/wcf/samples/basic-ajax-service.md) örnek.</span><span class="sxs-lookup"><span data-stu-id="215d6-105">This sample builds on the [Basic AJAX Service](../../../../docs/framework/wcf/samples/basic-ajax-service.md) sample.</span></span>  
  
 <span data-ttu-id="215d6-106">Diğer AJAX örnekleri farklı olarak, bu örnek, ASP.NET AJAX kullanmaz ve <xref:System.Web.UI.ScriptManager> denetim.</span><span class="sxs-lookup"><span data-stu-id="215d6-106">Unlike the other AJAX samples, this sample does not use ASP.NET AJAX and the <xref:System.Web.UI.ScriptManager> control.</span></span> <span data-ttu-id="215d6-107">Bazı ek yapılandırma [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] AJAX Hizmetleri, JavaScript aracılığıyla herhangi bir HTML sayfadan erişilebilir ve bu senaryo burada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="215d6-107">With some additional configuration, [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] AJAX services can be accessed from any HTML page through JavaScript, and this scenario is shown here.</span></span> <span data-ttu-id="215d6-108">Kullanarak bir örnek için [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] ASP.NET AJAX ile bkz [AJAX örnekleri](http://msdn.microsoft.com/en-us/f3fa45b3-44d5-4926-8cc4-a13c30a3bf3e).</span><span class="sxs-lookup"><span data-stu-id="215d6-108">For an example of using [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] with ASP.NET AJAX, see [AJAX Samples](http://msdn.microsoft.com/en-us/f3fa45b3-44d5-4926-8cc4-a13c30a3bf3e).</span></span>  
  
 <span data-ttu-id="215d6-109">Bu örnek, JSON ve XML arasında bir işlem yanıt türünü geçiş gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="215d6-109">This sample shows how to switch the response type of an operation between JSON and XML.</span></span> <span data-ttu-id="215d6-110">Bu işlevsellik, olup hizmet ASP.NET AJAX veya bir HTML/JavaScript istemci sayfası tarafından erişilebilmesi için yapılandırılan bağımsız olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="215d6-110">This functionality is available regardless of whether the service is configured to be accessed by ASP.NET AJAX or by an HTML/JavaScript client page.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="215d6-111">Kurulum yordamı ve yapı yönergeleri Bu örnek için bu konunun sonunda yer alır.</span><span class="sxs-lookup"><span data-stu-id="215d6-111">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="215d6-112">ASP.NET AJAX istemcileri kullanımını etkinleştirmek için kullanın <xref:System.ServiceModel.Activation.WebServiceHostFactory> (değil <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>) .svc dosyasındaki.</span><span class="sxs-lookup"><span data-stu-id="215d6-112">To enable the use of non-ASP.NET AJAX clients, use <xref:System.ServiceModel.Activation.WebServiceHostFactory> (not <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>) in the .svc file.</span></span> <span data-ttu-id="215d6-113"><xref:System.ServiceModel.Activation.WebServiceHostFactory>ekler bir <xref:System.ServiceModel.Description.WebHttpEndpoint> hizmetine standart uç noktası.</span><span class="sxs-lookup"><span data-stu-id="215d6-113"><xref:System.ServiceModel.Activation.WebServiceHostFactory> adds a <xref:System.ServiceModel.Description.WebHttpEndpoint> standard endpoint to the service.</span></span> <span data-ttu-id="215d6-114">Uç nokta .svc dosyasıyla ilişkili boş bir adresindeki yapılandırılmıştır; Bu hizmet adresini işlemi adı dışında hiçbir ek sonekleri http://localhost/ServiceModelSamples/service.svc anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="215d6-114">The endpoint is configured at an empty address relative to the .svc file; this means that the address of the service is http://localhost/ServiceModelSamples/service.svc, with no additional suffixes other than the operation name.</span></span>  
  
```html  
<%@ServiceHost language="c#" Debug="true" Service="Microsoft.Samples.XmlAjaxService.CalculatorService" Factory="System.ServiceModel.Activation.WebServiceHostFactory" %>  
```  
  
 <span data-ttu-id="215d6-115">Web.config dosyasında aşağıdaki bölümde, uç nokta için ek yapılandırma değişiklikleri yapmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="215d6-115">The following section in Web.config can be used to make additional configuration changes to the endpoint.</span></span> <span data-ttu-id="215d6-116">Hiçbir ek değişikliklerin gerekli olup olmadığını kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="215d6-116">It can be removed if no extra changes are needed.</span></span>  
  
```xml  
<system.serviceModel>  
  <standardEndpoints>  
    <webHttpEndpoint>  
      <!-- Use this element to configure the endpoint -->  
      <standardEndpoint name="" />  
    </webHttpEndpoint>  
  </standardEndpoints>  
</system.serviceModel>  
```  
  
 <span data-ttu-id="215d6-117">Varsayılan verilerin biçimlendirilmesi için <xref:System.ServiceModel.Description.WebHttpEndpoint> , varsayılan veri biçimi sırasında XML'dir <xref:System.ServiceModel.Description.WebScriptEndpoint> JSON.</span><span class="sxs-lookup"><span data-stu-id="215d6-117">The default data format for <xref:System.ServiceModel.Description.WebHttpEndpoint> is XML, while the default data format for <xref:System.ServiceModel.Description.WebScriptEndpoint> is JSON.</span></span> <span data-ttu-id="215d6-118">Daha fazla bilgi için bkz: [ASP.NET olmadan WCF AJAX hizmetleri oluşturma](../../../../docs/framework/wcf/feature-details/creating-wcf-ajax-services-without-aspnet.md).</span><span class="sxs-lookup"><span data-stu-id="215d6-118">For more information, see [Creating WCF AJAX Services without ASP.NET](../../../../docs/framework/wcf/feature-details/creating-wcf-ajax-services-without-aspnet.md).</span></span>  
  
 <span data-ttu-id="215d6-119">Aşağıdaki örnek hizmetinde bir standarttır [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] hizmeti iki işlem ile.</span><span class="sxs-lookup"><span data-stu-id="215d6-119">The service in the following sample is a standard [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] service with two operations.</span></span> <span data-ttu-id="215d6-120">İki işlem gerektiren <xref:System.ServiceModel.Web.WebMessageBodyStyle.Wrapped> Gövde stili <xref:System.ServiceModel.Web.WebGetAttribute> veya <xref:System.ServiceModel.Web.WebInvokeAttribute> özel öznitelikleri `webHttp` davranışı ve şifrelemeyle JSON/XML veri biçimi anahtarı vardır.</span><span class="sxs-lookup"><span data-stu-id="215d6-120">Both operations require the <xref:System.ServiceModel.Web.WebMessageBodyStyle.Wrapped> body style on the <xref:System.ServiceModel.Web.WebGetAttribute> or <xref:System.ServiceModel.Web.WebInvokeAttribute> attributes, which is specific to the `webHttp` behavior and has no bearing on the JSON/XML data format switch.</span></span>  
  
```  
[OperationContract]  
[WebInvoke(ResponseFormat = WebMessageFormat.Xml, BodyStyle = WebMessageBodyStyle.Wrapped)]  
MathResult DoMathXml(double n1, double n2);  
```  
  
 <span data-ttu-id="215d6-121">İşlem yanıt biçimi varsayılan değer XML olarak belirtilen ayarını [ \<webHttp >](../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) davranışı.</span><span class="sxs-lookup"><span data-stu-id="215d6-121">The response format for the operation is specified as XML, which is the default setting for the [\<webHttp>](../../../../docs/framework/configure-apps/file-schema/wcf/webhttp.md) behavior.</span></span> <span data-ttu-id="215d6-122">Ancak, iyi açıkça bir yöntemdir yanıt biçimi belirtin.</span><span class="sxs-lookup"><span data-stu-id="215d6-122">However, it is good practice explicitly specify the response format.</span></span>  
  
 <span data-ttu-id="215d6-123">Başka bir işlem kullanır `WebInvokeAttribute` özniteliği ve XML yerine JSON yanıt için açıkça belirtir.</span><span class="sxs-lookup"><span data-stu-id="215d6-123">The other operation uses the `WebInvokeAttribute` attribute and explicitly specifies JSON instead of XML for the response.</span></span>  
  
```  
[OperationContract]  
[WebInvoke(ResponseFormat = WebMessageFormat.Json, BodyStyle = WebMessageBodyStyle.Wrapped)]  
MathResult DoMathJson(double n1, double n2);  
```  
  
 <span data-ttu-id="215d6-124">Her iki durumda da, karmaşık bir tür işlemler geri bildirdiğine dikkat edin `MathResult`, bir standart olduğu [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] veri sözleşme türü.</span><span class="sxs-lookup"><span data-stu-id="215d6-124">Note that in both cases the operations return a complex type, `MathResult`, which is a standard [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] data contract type.</span></span>  
  
 <span data-ttu-id="215d6-125">İstemci Web sayfası XmlAjaxClientPage.htm kullanıcı tıkladığında, önceki iki işlemlerden birini çağırır JavaScript kodu içeren **(dönüş JSON) hesaplamayı** veya **hesaplamayı (dönüş XML)**  sayfasında düğmeler.</span><span class="sxs-lookup"><span data-stu-id="215d6-125">The client Web page XmlAjaxClientPage.htm contains JavaScript code that invokes one of the preceding two operations when the user clicks the **Perform calculation (return JSON)** or **Perform calculation (return XML)** buttons on the page.</span></span> <span data-ttu-id="215d6-126">Hizmetini çağırmak için kodu JSON gövdesi oluşturur ve HTTP POST kullanarak gönderir.</span><span class="sxs-lookup"><span data-stu-id="215d6-126">The code to invoke the service constructs a JSON body and sends it using HTTP POST.</span></span> <span data-ttu-id="215d6-127">İstek el ile aksine, JavaScript'te oluşturulduğunda [temel AJAX hizmeti](../../../../docs/framework/wcf/samples/basic-ajax-service.md) örnek ve ASP.NET AJAX kullanılarak diğer örnekleri.</span><span class="sxs-lookup"><span data-stu-id="215d6-127">The request is created manually in JavaScript, unlike the [Basic AJAX Service](../../../../docs/framework/wcf/samples/basic-ajax-service.md) sample and the other samples using ASP.NET AJAX.</span></span>  
  
```  
// Create HTTP request  
var xmlHttp;  
// Request instantiation code omitted…  
// Result handler code omitted…  
  
// Build the operation URL  
var url = "service.svc/ajaxEndpoint/";  
url = url + operation;  
  
// Build the body of the JSON message  
var body = '{"n1":';  
body = body + document.getElementById("num1").value + ',"n2":';  
body = body + document.getElementById("num2").value + '}';  
  
// Send the HTTP request  
xmlHttp.open("POST", url, true);  
xmlHttp.setRequestHeader("Content-type", "application/json");  
xmlHttp.send(body);  
```  
  
 <span data-ttu-id="215d6-128">Hizmet yanıtladığında yanıt herhangi bir metin kutusuna sayfasında işlenmesi olmadan görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="215d6-128">When the service responds, the response is displayed without any further processing in a textbox on the page.</span></span> <span data-ttu-id="215d6-129">Bu tanıtım amacıyla kullanılan XML ve JSON veri biçimleri doğrudan gözlemlemek olanak tanımak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="215d6-129">This is implemented for demonstration purposes to allow you to directly observe the XML and JSON data formats used.</span></span>  
  
```  
// Create result handler   
xmlHttp.onreadystatechange=function(){  
     if(xmlHttp.readyState == 4){  
          document.getElementById("result").value = xmlHttp.responseText;  
     }  
}  
```  
  
> [!IMPORTANT]
>  <span data-ttu-id="215d6-130">Örnekler, makinenizde zaten yüklü olabilir.</span><span class="sxs-lookup"><span data-stu-id="215d6-130">The samples may already be installed on your machine.</span></span> <span data-ttu-id="215d6-131">Devam etmeden önce aşağıdaki (varsayılan) dizin denetleyin.</span><span class="sxs-lookup"><span data-stu-id="215d6-131">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="215d6-132">Bu dizin mevcut değilse, Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnek](http://go.microsoft.com/fwlink/?LinkId=150780) tüm indirmek için [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri.</span><span class="sxs-lookup"><span data-stu-id="215d6-132">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="215d6-133">Bu örnek aşağıdaki dizinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="215d6-133">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\AJAX\XmlAjaxService`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="215d6-134">Ayarlamak için derleme ve örnek çalıştırın</span><span class="sxs-lookup"><span data-stu-id="215d6-134">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="215d6-135">Gerçekleştirmiş emin olun [kerelik Kurulum prosedürü Windows Communication Foundation örnekleri için](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="215d6-135">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2.  <span data-ttu-id="215d6-136">Çözüm XmlAjaxService.sln açıklandığı gibi yapı [Windows Communication Foundation örnekleri derleme](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="215d6-136">Build the solution XmlAjaxService.sln as described in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
3.  <span data-ttu-id="215d6-137">İçin http://localhost/ServiceModelSamples/XmlAjaxClientPage.htm gidin (XmlAjaxClientPage.htm proje dizininden tarayıcıda aç değil).</span><span class="sxs-lookup"><span data-stu-id="215d6-137">Navigate to http://localhost/ServiceModelSamples/XmlAjaxClientPage.htm (do not open XmlAjaxClientPage.htm in the browser from the project directory).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="215d6-138">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="215d6-138">See Also</span></span>  
 [<span data-ttu-id="215d6-139">AJAX hizmeti kullanarak HTTP POST</span><span class="sxs-lookup"><span data-stu-id="215d6-139">AJAX Service Using HTTP POST</span></span>](../../../../docs/framework/wcf/samples/ajax-service-using-http-post.md)