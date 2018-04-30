---
title: 'Nasıl yapılır: Zaman Uyumsuz Bir Hizmet İşlemi Uygulama'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 4e5d2ea5-d8f8-4712-bd18-ea3c5461702c
caps.latest.revision: 14
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: fe823fc8b86dd20cfa344c9889eca9dff21514ec
ms.sourcegitcommit: 94d33cadc5ff81d2ac389bf5f26422c227832052
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/30/2018
---
# <a name="how-to-implement-an-asynchronous-service-operation"></a><span data-ttu-id="fe32f-102">Nasıl yapılır: Zaman Uyumsuz Bir Hizmet İşlemi Uygulama</span><span class="sxs-lookup"><span data-stu-id="fe32f-102">How to: Implement an Asynchronous Service Operation</span></span>
<span data-ttu-id="fe32f-103">İçinde [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] uygulamalar, bir hizmet işlemi uygulanabilir zaman uyumsuz veya zaman uyumlu olarak bunu nasıl istemciyi dikte olmadan.</span><span class="sxs-lookup"><span data-stu-id="fe32f-103">In [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] applications, a service operation can be implemented asynchronously or synchronously without dictating to the client how to call it.</span></span> <span data-ttu-id="fe32f-104">Örneğin, zaman uyumsuz hizmet işlemlerini zaman uyumlu çağırma ve zaman uyumlu hizmet işlemlerini zaman uyumsuz olarak çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="fe32f-104">For example, asynchronous service operations can be calling synchronously, and synchronous service operations can be called asynchronously.</span></span> <span data-ttu-id="fe32f-105">Bir istemci uygulamasında zaman uyumsuz bir işlem çağırma gösteren örnek için bkz: [nasıl yapılır: hizmet işlemlerini zaman uyumsuz çağrı](../../../docs/framework/wcf/feature-details/how-to-call-wcf-service-operations-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="fe32f-105">For an example that shows how to call an operation asynchronously in a client application, see [How to: Call Service Operations Asynchronously](../../../docs/framework/wcf/feature-details/how-to-call-wcf-service-operations-asynchronously.md).</span></span> <span data-ttu-id="fe32f-106">Zaman uyumlu ve zaman uyumsuz işlemler hakkında daha fazla bilgi için bkz: [Hizmet sözleşmeleri tasarlama](../../../docs/framework/wcf/designing-service-contracts.md) ve [zaman uyumlu ve zaman uyumsuz işlemleri](../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="fe32f-106">For more information about synchronous and asynchronous operations, see [Designing Service Contracts](../../../docs/framework/wcf/designing-service-contracts.md) and [Synchronous and Asynchronous Operations](../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md).</span></span> <span data-ttu-id="fe32f-107">Bu konuda bir zaman uyumsuz hizmet işlemi temel yapısını tanımlar, kod tam değil.</span><span class="sxs-lookup"><span data-stu-id="fe32f-107">This topic describes the basic structure of an asynchronous service operation, the code is not complete.</span></span> <span data-ttu-id="fe32f-108">Hem hizmet hem de istemci tarafında tam bir örnek için bkz: [zaman uyumsuz](http://msdn.microsoft.com/library/833db946-f511-4f64-a26f-2759a11217c7).</span><span class="sxs-lookup"><span data-stu-id="fe32f-108">For a complete example of both the service and client sides see [Asynchronous](http://msdn.microsoft.com/library/833db946-f511-4f64-a26f-2759a11217c7).</span></span>  
  
### <a name="implement-a-service-operation-asynchronously"></a><span data-ttu-id="fe32f-109">Zaman uyumsuz olarak bir hizmet işlemi uygulama</span><span class="sxs-lookup"><span data-stu-id="fe32f-109">Implement a service operation asynchronously</span></span>  
  
1.  <span data-ttu-id="fe32f-110">Hizmet sözleşmesini .NET zaman uyumsuz tasarım yönergelerine göre bir zaman uyumsuz yöntem çiftinin bildirin.</span><span class="sxs-lookup"><span data-stu-id="fe32f-110">In your service contract, declare an asynchronous method pair according to the .NET asynchronous design guidelines.</span></span> <span data-ttu-id="fe32f-111">`Begin` Yöntemi bir parametre, bir geri çağırma nesnesi ve bir durum nesnesi alır ve döndüren bir <xref:System.IAsyncResult?displayProperty=nameWithType> ve eşleşen bir `End` alır yöntemi bir <xref:System.IAsyncResult?displayProperty=nameWithType> ve dönüş değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fe32f-111">The `Begin` method takes a parameter, a callback object, and a state object, and returns a <xref:System.IAsyncResult?displayProperty=nameWithType> and a matching `End` method that takes a <xref:System.IAsyncResult?displayProperty=nameWithType> and returns the return value.</span></span> <span data-ttu-id="fe32f-112">Zaman uyumsuz çağrılar hakkında daha fazla bilgi için bkz: [zaman uyumsuz programlama tasarım desenleri](http://go.microsoft.com/fwlink/?LinkId=248221).</span><span class="sxs-lookup"><span data-stu-id="fe32f-112">For more information about asynchronous calls, see [Asynchronous Programming Design Patterns](http://go.microsoft.com/fwlink/?LinkId=248221).</span></span>  
  
2.  <span data-ttu-id="fe32f-113">İşareti `Begin` yöntemi ile zaman uyumsuz yöntem çiftinin <xref:System.ServiceModel.OperationContractAttribute?displayProperty=nameWithType> özniteliği ve ayarlayın <xref:System.ServiceModel.OperationContractAttribute.AsyncPattern%2A?displayProperty=nameWithType> özelliğine `true`.</span><span class="sxs-lookup"><span data-stu-id="fe32f-113">Mark the `Begin` method of the asynchronous method pair with the <xref:System.ServiceModel.OperationContractAttribute?displayProperty=nameWithType> attribute and set the <xref:System.ServiceModel.OperationContractAttribute.AsyncPattern%2A?displayProperty=nameWithType> property to `true`.</span></span> <span data-ttu-id="fe32f-114">Örneğin, aşağıdaki kodu, 1 ve 2. adımları gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="fe32f-114">For example, the following code performs steps 1 and 2.</span></span>  
  
     [!code-csharp[C_SyncAsyncClient#6](../../../samples/snippets/csharp/VS_Snippets_CFX/c_syncasyncclient/cs/services.cs#6)]
     [!code-vb[C_SyncAsyncClient#6](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_syncasyncclient/vb/services.vb#6)]  
  
3.  <span data-ttu-id="fe32f-115">Uygulama `Begin/End` zaman uyumsuz tasarım yönergelerine göre hizmet sınıfınızda yöntemi çifti.</span><span class="sxs-lookup"><span data-stu-id="fe32f-115">Implement the `Begin/End` method pair in your service class according to the asynchronous design guidelines.</span></span> <span data-ttu-id="fe32f-116">Örneğin, aşağıdaki kod örneği, bir dize yazılır hem de konsol uygulaması gösterir `Begin` ve `End` zaman uyumsuz hizmet işlemi ve dönüş değerini bölümlerini `End` işlemi istemciye döndürülen.</span><span class="sxs-lookup"><span data-stu-id="fe32f-116">For example, the following code example shows an implementation in which a string is written to the console in both the `Begin` and `End` portions of the asynchronous service operation, and the return value of the `End` operation is returned to the client.</span></span> <span data-ttu-id="fe32f-117">Tam kod örneği için örnek bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="fe32f-117">For the complete code example, see the Example section.</span></span>  
  
     [!code-csharp[C_SyncAsyncClient#3](../../../samples/snippets/csharp/VS_Snippets_CFX/c_syncasyncclient/cs/services.cs#3)]
     [!code-vb[C_SyncAsyncClient#3](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_syncasyncclient/vb/services.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="fe32f-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="fe32f-118">Example</span></span>  
 <span data-ttu-id="fe32f-119">Aşağıdaki kod örnekleri göster:</span><span class="sxs-lookup"><span data-stu-id="fe32f-119">The following code examples show:</span></span>  
  
1.  <span data-ttu-id="fe32f-120">Hizmet sözleşme arabirimi ile:</span><span class="sxs-lookup"><span data-stu-id="fe32f-120">A service contract interface with:</span></span>  
  
    1.  <span data-ttu-id="fe32f-121">Bir zaman uyumlu `SampleMethod` işlemi.</span><span class="sxs-lookup"><span data-stu-id="fe32f-121">A synchronous `SampleMethod` operation.</span></span>  
  
    2.  <span data-ttu-id="fe32f-122">Zaman uyumsuz bir `BeginSampleMethod` işlemi.</span><span class="sxs-lookup"><span data-stu-id="fe32f-122">An asynchronous `BeginSampleMethod` operation.</span></span>  
  
    3.  <span data-ttu-id="fe32f-123">Zaman uyumsuz bir `BeginServiceAsyncMethod` / `EndServiceAsyncMethod` işlemi çifti.</span><span class="sxs-lookup"><span data-stu-id="fe32f-123">An asynchronous `BeginServiceAsyncMethod`/`EndServiceAsyncMethod` operation pair.</span></span>  
  
2.  <span data-ttu-id="fe32f-124">Bir hizmet uygulamasını kullanarak bir <xref:System.IAsyncResult?displayProperty=nameWithType> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fe32f-124">A service implementation using a <xref:System.IAsyncResult?displayProperty=nameWithType> object.</span></span>  
  
 [!code-csharp[C_SyncAsyncClient#1](../../../samples/snippets/csharp/VS_Snippets_CFX/c_syncasyncclient/cs/services.cs#1)]
 [!code-vb[C_SyncAsyncClient#1](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_syncasyncclient/vb/services.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="fe32f-125">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="fe32f-125">See Also</span></span>  
 [<span data-ttu-id="fe32f-126">Hizmet Sözleşmeleri Tasarlama</span><span class="sxs-lookup"><span data-stu-id="fe32f-126">Designing Service Contracts</span></span>](../../../docs/framework/wcf/designing-service-contracts.md)  
 [<span data-ttu-id="fe32f-127">Zaman Uyumlu ve Zaman Uyumsuz İşlemler</span><span class="sxs-lookup"><span data-stu-id="fe32f-127">Synchronous and Asynchronous Operations</span></span>](../../../docs/framework/wcf/synchronous-and-asynchronous-operations.md)
