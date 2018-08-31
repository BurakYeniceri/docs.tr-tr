---
title: Temel Veri Sözleşmesi
ms.date: 03/30/2017
helpviewer_keywords:
- Data Contract
ms.assetid: b124e9e0-cb73-4ae0-b9c3-e6cdf5eced98
ms.openlocfilehash: a170423a5ae132c70710e22b5d61f57c46fdfc28
ms.sourcegitcommit: a368166a51e5204c0224fbf5e46476e3ed122817
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/31/2018
ms.locfileid: "43332085"
---
# <a name="basic-data-contract"></a><span data-ttu-id="ec10f-102">Temel Veri Sözleşmesi</span><span class="sxs-lookup"><span data-stu-id="ec10f-102">Basic Data Contract</span></span>
<span data-ttu-id="ec10f-103">Bu örnek, bir veri sözleşmesi uygulama gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ec10f-103">This sample demonstrates how to implement a data contract.</span></span> <span data-ttu-id="ec10f-104">Veri sözleşmeleri, yapılandırılmış veriler için ve hizmetlerden geçmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="ec10f-104">Data contracts allow you to pass structured data to and from services.</span></span> <span data-ttu-id="ec10f-105">Bu örnek dayanır [Başlarken](../../../../docs/framework/wcf/samples/getting-started-sample.md) ancak karmaşık sayılar yerine temel sayısal türleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="ec10f-105">This sample is based on the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) but uses complex numbers instead of basic numeric types.</span></span>  
  
 <span data-ttu-id="ec10f-106">Bu örnekte, Internet Information Services (IIS) tarafından barındırılan hizmet ve bir konsol uygulaması (.exe) istemcidir.</span><span class="sxs-lookup"><span data-stu-id="ec10f-106">In this sample, the service is hosted by Internet Information Services (IIS) and the client is a console application (.exe).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ec10f-107">Bu örnek için Kurulum yordamı ve derleme yönergelerini, bu konunun sonunda yer alır.</span><span class="sxs-lookup"><span data-stu-id="ec10f-107">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="ec10f-108">Aşağıdaki örnek kodda gösterildiği gibi bu hizmeti hizmet anlaşmasının karmaşık sayılar kullanır.</span><span class="sxs-lookup"><span data-stu-id="ec10f-108">The service contract for this service uses complex numbers, as shown in the following sample code.</span></span>  
  
```  
// Define a service contract.  
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public interface ICalculator  
{  
    [OperationContract]  
    ComplexNumber Add(ComplexNumber n1, ComplexNumber n2);  
    [OperationContract]  
    ComplexNumber Subtract(ComplexNumber n1, ComplexNumber n2);  
    [OperationContract]  
    ComplexNumber Multiply(ComplexNumber n1, ComplexNumber n2);  
    [OperationContract]  
    ComplexNumber Divide(ComplexNumber n1, ComplexNumber n2);  
}  
```  
  
 <span data-ttu-id="ec10f-109"><xref:System.Runtime.Serialization.DataContractAttribute> Ve <xref:System.Runtime.Serialization.DataMemberAttribute> öznitelikleri tanımına uygulanmadığını `ComplexNumber` aşağıdaki örnek kodda gösterildiği gibi sınıf hangi alanları kablo üzerinden istemci ile hizmet arasında geçirilebilir göstermek için sınıf.</span><span class="sxs-lookup"><span data-stu-id="ec10f-109">The <xref:System.Runtime.Serialization.DataContractAttribute> and <xref:System.Runtime.Serialization.DataMemberAttribute> attributes have been applied to the definition of the `ComplexNumber` class to indicate which fields of the class can be passed over the wire between the client and the service, as shown in the following sample code.</span></span>  
  
```  
[DataContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public class ComplexNumber  
{  
    [DataMember]  
    public double Real = 0.0D;  
    [DataMember]  
    public double Imaginary = 0.0D;  
  
    public ComplexNumber(double real, double imaginary)  
    {  
        this.Real = real;  
        this.Imaginary = imaginary;  
    }  
}  
```  
  
 <span data-ttu-id="ec10f-110">Hizmet uygulaması hesaplar ve kabul etme ve sayılarını döndüren uygun sonucu verir `ComplexNumber` türü.</span><span class="sxs-lookup"><span data-stu-id="ec10f-110">The service implementation calculates and returns the appropriate result, accepting and returning numbers of the `ComplexNumber` type.</span></span>  
  
```  
// This is the service class that implements the service contract.  
public class CalculatorService : ICalculator  
{  
    public ComplexNumber Add(ComplexNumber n1, ComplexNumber n2)  
    {  
        return new ComplexNumber(n1.Real + n2.Real, n1.Imaginary +  
                                                      n2.Imaginary);  
    }  
  
    public ComplexNumber Subtract(ComplexNumber n1, ComplexNumber n2)  
    {  
        return new ComplexNumber(n1.Real - n2.Real, n1.Imaginary -   
                                                     n2.Imaginary);  
    }  
    public ComplexNumber Multiply(ComplexNumber n1, ComplexNumber n2)  
    {  
        double real1 = n1.Real * n2.Real;  
        double imaginary1 = n1.Real * n2.Imaginary;  
        double imaginary2 = n2.Real * n1.Imaginary;  
        double real2 = n1.Imaginary * n2.Imaginary * -1;  
        return new ComplexNumber(real1 + real2, imaginary1 +   
                                                 imaginary2);  
    }  
  
    public ComplexNumber Divide(ComplexNumber n1, ComplexNumber n2)  
    {  
         ComplexNumber conjugate =   
              new ComplexNumber(n2.Real, -1*n2.Imaginary);  
         ComplexNumber numerator = Multiply(n1, conjugate);  
         ComplexNumber denominator = Multiply(n2, conjugate);  
         return new ComplexNumber(numerator.Real / denominator.Real,  
                                               numerator.Imaginary);  
    }  
}  
```  
  
 <span data-ttu-id="ec10f-111">İstemci uygulaması, karmaşık sayılar da kullanır.</span><span class="sxs-lookup"><span data-stu-id="ec10f-111">The client implementation also uses complex numbers.</span></span> <span data-ttu-id="ec10f-112">Hizmet sözleşmesi hem veri anlaşması tarafından üretilen kaynak dosyası generatedClient.cs tanımlanan [ServiceModel meta veri yardımcı Programracı (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) hizmeti meta veriler.</span><span class="sxs-lookup"><span data-stu-id="ec10f-112">Both the service contract and the data contract are defined in the source file generatedClient.cs, which is generated by the [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) from service metadata.</span></span>  
  
```  
// Create a client.  
DataContractCalculatorClient client = new DataContractCalculatorClient();  
// Call the Add service operation.  
ComplexNumber value1 = new ComplexNumber();   
value1.Real = 1;   
value1.Imaginary = 2;  
ComplexNumber value2 = new ComplexNumber();   
value2.Real = 3;  
value2.Imaginary = 4;  
ComplexNumber result = proxy.Add(value1, value2);  
Console.WriteLine("Add({0} + {1}i, {2} + {3}i) = {4} + {5}i",  
      value1.Real, value1.Imaginary, value2.Real, value2.Imaginary,   
      result.Real, result.Imaginary);   
    …  
}  
```  
  
 <span data-ttu-id="ec10f-113">Örneği çalıştırdığında istek ve yanıtların işlemin istemci konsol penceresinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ec10f-113">When you run the sample, the requests and responses of the operation are displayed in the client console window.</span></span> <span data-ttu-id="ec10f-114">İstemci bilgisayarı için istemci penceresinde ENTER tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="ec10f-114">Press ENTER in the client window to shut down the client.</span></span>  
  
```  
Add(1 + 2i, 3 + 4i) = 4 + 6i  
Subtract(1 + 2i, 3 + 4i) = -2 + -2i  
Multiply(2 + 3i, 4 + 7i) = -13 + 26i  
Divide(3 + 7i, 5 + -2i) = 0.0344827586206897 + 41i  
  
Press <ENTER> to terminate client.  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ec10f-115">Ayarlamak için derleme ve örneği çalıştırma</span><span class="sxs-lookup"><span data-stu-id="ec10f-115">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="ec10f-116">Gerçekleştirdiğinizden emin olmak [Windows Communication Foundation örnekleri için bir kerelik Kurulum yordamı](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ec10f-116">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2.  <span data-ttu-id="ec10f-117">Çözüm C# veya Visual Basic .NET sürümünü oluşturmak için yönergeleri izleyin. [Windows Communication Foundation örnekleri derleme](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ec10f-117">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
3.  <span data-ttu-id="ec10f-118">Tek veya çapraz makine yapılandırmasında örneği çalıştırmak için yönergeleri izleyin. [Windows Communication Foundation örneklerini çalıştırma](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ec10f-118">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ec10f-119">Örnekler, makinenizde zaten yüklü.</span><span class="sxs-lookup"><span data-stu-id="ec10f-119">The samples may already be installed on your machine.</span></span> <span data-ttu-id="ec10f-120">Devam etmeden önce şu (varsayılan) dizin denetleyin.</span><span class="sxs-lookup"><span data-stu-id="ec10f-120">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="ec10f-121">Bu dizin mevcut değilse Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnekleri](https://go.microsoft.com/fwlink/?LinkId=150780) tüm Windows Communication Foundation (WCF) indirmek için ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri.</span><span class="sxs-lookup"><span data-stu-id="ec10f-121">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ec10f-122">Bu örnek, şu dizinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="ec10f-122">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Contract\Data\Basic`  
  
## <a name="see-also"></a><span data-ttu-id="ec10f-123">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="ec10f-123">See Also</span></span>
