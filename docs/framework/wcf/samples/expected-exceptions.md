---
title: Beklenen Özel Durumlar
ms.date: 03/30/2017
ms.assetid: 299a6987-ae6b-43c6-987f-12b034b583ae
ms.openlocfilehash: 6c4af62e0870cdd670c46ead169033ff72902fc0
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2018
ms.locfileid: "33805830"
---
# <a name="expected-exceptions"></a><span data-ttu-id="ee333-102">Beklenen Özel Durumlar</span><span class="sxs-lookup"><span data-stu-id="ee333-102">Expected Exceptions</span></span>
<span data-ttu-id="ee333-103">Bu örnek, bir türü belirlenmiş istemci kullanırken beklenen özel durumları yakalamak gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ee333-103">This sample demonstrates how to catch expected exceptions when using a typed client.</span></span> <span data-ttu-id="ee333-104">Bu örnek dayanır [Başlarken](../../../../docs/framework/wcf/samples/getting-started-sample.md) hesap makinesi hizmetinin uygular.</span><span class="sxs-lookup"><span data-stu-id="ee333-104">This sample is based on the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) that implements a calculator service.</span></span> <span data-ttu-id="ee333-105">Bu örnekte, istemci bir konsol uygulaması (.exe) ve Internet Information Services (IIS) tarafından barındırılan hizmetindeki.</span><span class="sxs-lookup"><span data-stu-id="ee333-105">In this sample, the client is a console application (.exe) and the service is hosted by Internet Information Services (IIS).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ee333-106">Kurulum yordamı ve yapı yönergeleri Bu örnek için bu konunun sonunda yer alır.</span><span class="sxs-lookup"><span data-stu-id="ee333-106">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="ee333-107">Bu örnek yakalama gösterir ve programları düzeltmek iki beklenen özel durum türleri işleme gerekir işlemek: `TimeoutException` ve `CommunicationException`.</span><span class="sxs-lookup"><span data-stu-id="ee333-107">This sample demonstrates catching and handling the two expected exception types that correct programs must handle: `TimeoutException` and `CommunicationException`.</span></span>  
  
 <span data-ttu-id="ee333-108">Windows Communication Foundation (WCF) istemci iletişimi yöntemlerden oluşturulan beklenen veya beklenmeyen özel durumlardır.</span><span class="sxs-lookup"><span data-stu-id="ee333-108">Exceptions that are thrown from communication methods on a Windows Communication Foundation (WCF) client are either expected or unexpected.</span></span> <span data-ttu-id="ee333-109">Beklenmeyen özel durumları içerecek yıkıcı hataları gibi `OutOfMemoryException` ve programlama hataları `ArgumentNullException` veya `InvalidOperationException`.</span><span class="sxs-lookup"><span data-stu-id="ee333-109">Unexpected exceptions include catastrophic failures like `OutOfMemoryException` and programming errors like `ArgumentNullException` or `InvalidOperationException`.</span></span> <span data-ttu-id="ee333-110">Genellikle beklenmeyen hataları, bu nedenle genellikle, bunları bir WCF istemci iletişim yönteminin çağrılırken catch değil işlemek için kullanışlı bir yolu yoktur.</span><span class="sxs-lookup"><span data-stu-id="ee333-110">Typically there is no useful way to handle unexpected errors, so typically you should not catch them when calling a WCF client communication method.</span></span>  
  
 <span data-ttu-id="ee333-111">Bir WCF istemcisi iletişimi yöntemlere özel durumlar dahil beklenen `TimeoutException`, `CommunicationException`, ve herhangi bir türetilmiş sınıf `CommunicationException`.</span><span class="sxs-lookup"><span data-stu-id="ee333-111">Expected exceptions from communication methods on a WCF client include `TimeoutException`, `CommunicationException`, and any derived class of `CommunicationException`.</span></span> <span data-ttu-id="ee333-112">Bunlar, WCF istemcisini durduruluyor ve bir iletişim hatası raporlama güvenli bir şekilde işlenebilir iletişimi sırasında bir sorun gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee333-112">These indicate a problem during communication that can be safely handled by aborting the WCF client and reporting a communication failure.</span></span> <span data-ttu-id="ee333-113">Herhangi bir uygulamada dış etkenler bu hataların neden olabileceğinden, doğru uygulamaları bu özel durumları yakalamak ve bunlar ortaya çıktığında kurtarın.</span><span class="sxs-lookup"><span data-stu-id="ee333-113">Because external factors can cause these errors in any application, correct applications must catch these exceptions and recover when they occur.</span></span>  
  
 <span data-ttu-id="ee333-114">Birkaç türetilmiş sınıfları vardır `CommunicationException` , bir istemci atabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee333-114">There are several derived classes of `CommunicationException` that a client can throw.</span></span> <span data-ttu-id="ee333-115">Bazı durumlarda, uygulamaların da özel işleme yapın, ancak diğer kişilerin olarak işlenmesine izin vermek için bunlardan bazıları catch bir `CommunicationException`.</span><span class="sxs-lookup"><span data-stu-id="ee333-115">In some cases, applications also catch some of these to do special handling, but let the others be handled as a `CommunicationException`.</span></span> <span data-ttu-id="ee333-116">Bu ayrıntılı özel durum türü ilk yakalama ve ardından Yakalama gerçekleştirilebilir `CommunicationException` bir sonraki catch yan tümcesinde.</span><span class="sxs-lookup"><span data-stu-id="ee333-116">This can be accomplished by catching the more specific exception type first and then catching `CommunicationException` in a later catch-clause.</span></span>  
  
 <span data-ttu-id="ee333-117">İstemci iletişim yöntemini çağıran kodu gerekir catch `TimeoutException` ve `CommunicationException`.</span><span class="sxs-lookup"><span data-stu-id="ee333-117">Code that calls a client communication method must catch the `TimeoutException` and `CommunicationException`.</span></span> <span data-ttu-id="ee333-118">Bu tür hataları işlemek için bir istemci iptal etmek ve iletişim hatası rapor yoludur.</span><span class="sxs-lookup"><span data-stu-id="ee333-118">One way to handle such errors is to abort the client and report the communication failure.</span></span>  
  
```csharp   
try  
{  
    ...  
    double result = client.Add(value1, value2);  
    ...  
    client.Close();  
}  
catch (TimeoutException exception)  
{  
    Console.WriteLine("Got {0}", exception.GetType());  
    client.Abort();  
}  
catch (CommunicationException exception)  
{  
    Console.WriteLine("Got {0}", exception.GetType());  
    client.Abort();  
}  
```  
  
 <span data-ttu-id="ee333-119">Beklenen bir özel durum oluşursa, istemci olabilir veya daha sonra kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="ee333-119">If an expected exception occurs, the client may or may not be usable afterwards.</span></span> <span data-ttu-id="ee333-120">İstemci hala kullanılabilir olup olmadığını belirlemek için kontrol `State` özelliği `CommunicationState`. Açılır.</span><span class="sxs-lookup"><span data-stu-id="ee333-120">To determine if the client is still usable, check that the `State` property is `CommunicationState`.Opened.</span></span> <span data-ttu-id="ee333-121">Sonra hala açılırsa, hala kullanılabilir durumda değil.</span><span class="sxs-lookup"><span data-stu-id="ee333-121">If it is still opened, then it is still usable.</span></span> <span data-ttu-id="ee333-122">Aksi takdirde istemci iptal etmek ve tüm başvurularını serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="ee333-122">Otherwise you should abort the client and release all references to it.</span></span>  
  
> [!CAUTION]
>  <span data-ttu-id="ee333-123">Bir oturum sahip istemciler genellikle artık özel durumdan sonra kullanılabilir ve bir oturum olmayan istemciler hala genellikle özel durumdan sonra kullanılabilir gözlemleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ee333-123">You may observe that clients that have a session are often no longer usable after an exception, and clients that do not have a session are often still usable after an exception.</span></span> <span data-ttu-id="ee333-124">Ancak, hiçbirini garanti, bunu istemci uygulamanız denetlemelidir özel durumdan sonra kullanmaya devam etmek denemek istiyorsanız `State` bir istemci özelliğini hala açık.</span><span class="sxs-lookup"><span data-stu-id="ee333-124">However, neither of these is guaranteed, so if you want to try to continue using the client after an exception your application should check the `State` property to verify the client is still opened.</span></span>  
  
 <span data-ttu-id="ee333-125">Örneği çalıştırdığınızda, özel durumlar ve işlem yanıtları istemci konsol penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ee333-125">When you run the sample, the operation responses and exceptions are displayed in the client console window.</span></span>  
  
 <span data-ttu-id="ee333-126">İki senaryo, istemci işlemini çalıştıran her hangi aranır `Add` arkasından `Divide`.</span><span class="sxs-lookup"><span data-stu-id="ee333-126">The client process runs two scenarios, each of which attempts to call `Add` followed by `Divide`.</span></span> <span data-ttu-id="ee333-127">İlk senaryoda, istemci iptal etme çağrısı yapmadan önce bir ağ sorunu taklit eder `Divide`.</span><span class="sxs-lookup"><span data-stu-id="ee333-127">The first scenario simulates a network issue by aborting the client before making the call to `Divide`.</span></span> <span data-ttu-id="ee333-128">İkinci senaryo, zaman aşımı tamamlanması için çok yöntemi ayarlayarak bir zaman aşımı koşulu neden olur.</span><span class="sxs-lookup"><span data-stu-id="ee333-128">The second scenario causes a timeout condition by setting the timeout too short for the method to complete.</span></span> <span data-ttu-id="ee333-129">İstemci işlemi beklenen çıktısı şöyledir:</span><span class="sxs-lookup"><span data-stu-id="ee333-129">The expected output from the client process is:</span></span>  
  
```  
Add(100,15.99) = 115.99  
Simulated network problem occurs...  
Got System.ServiceModel.CommunicationObjectAbortedException  
Add(100,15.99) = 115.99  
Set timeout too short for method to complete...  
Got System.TimeoutException  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ee333-130">Ayarlamak için derleme ve örnek çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ee333-130">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="ee333-131">Gerçekleştirmiş emin olun [kerelik Kurulum prosedürü Windows Communication Foundation örnekleri için](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ee333-131">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2.  <span data-ttu-id="ee333-132">Çözüm C# veya Visual Basic .NET sürümünü oluşturmak için'ndaki yönergeleri izleyin [Windows Communication Foundation örnekleri derleme](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ee333-132">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
3.  <span data-ttu-id="ee333-133">Tek veya çapraz makine yapılandırmada örneği çalıştırmak için'ndaki yönergeleri izleyin [Windows Communication Foundation örneklerini çalıştırma](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ee333-133">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ee333-134">Örnekler, makinenizde zaten yüklü olabilir.</span><span class="sxs-lookup"><span data-stu-id="ee333-134">The samples may already be installed on your machine.</span></span> <span data-ttu-id="ee333-135">Devam etmeden önce aşağıdaki (varsayılan) dizin denetleyin.</span><span class="sxs-lookup"><span data-stu-id="ee333-135">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="ee333-136">Bu dizin mevcut değilse, Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnek](http://go.microsoft.com/fwlink/?LinkId=150780) tüm Windows Communication Foundation (WCF) indirmek için ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri.</span><span class="sxs-lookup"><span data-stu-id="ee333-136">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ee333-137">Bu örnek aşağıdaki dizinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="ee333-137">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Client\ExpectedExceptions`  
  
## <a name="see-also"></a><span data-ttu-id="ee333-138">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ee333-138">See Also</span></span>
