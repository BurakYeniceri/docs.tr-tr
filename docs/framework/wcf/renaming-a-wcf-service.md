---
title: Bir WCF Hizmetini Yeniden Adlandırma
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 14235a65-b1c5-409d-b6cc-a979acd54bbd
caps.latest.revision: ''
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: f2ab3d780f85131fc7adf24c5f420bd5fe643d9e
ms.sourcegitcommit: c883637b41ee028786edceece4fa872939d2e64c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/26/2018
---
# <a name="renaming-a-wcf-service"></a><span data-ttu-id="d1130-102">Bir WCF Hizmetini Yeniden Adlandırma</span><span class="sxs-lookup"><span data-stu-id="d1130-102">Renaming a WCF Service</span></span>
<span data-ttu-id="d1130-103">Bu konu, nasıl adlandırabilirsiniz açıklar bir [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] hizmet.</span><span class="sxs-lookup"><span data-stu-id="d1130-103">This topic describes how you can rename a [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] service.</span></span>  
  
## <a name="renaming-a-wcf-service"></a><span data-ttu-id="d1130-104">Bir WCF Hizmetini Yeniden Adlandırma</span><span class="sxs-lookup"><span data-stu-id="d1130-104">Renaming a WCF Service</span></span>  
 <span data-ttu-id="d1130-105">Bir hizmet olarak yeniden adlandırmak için aşağıdaki adımları izleyerek bir [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] şablonu</span><span class="sxs-lookup"><span data-stu-id="d1130-105">Perform the following steps to rename a service in a [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] template,</span></span>  
  
-   <span data-ttu-id="d1130-106">Hizmet uygulayan sınıf adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d1130-106">Change the name of the class that implements the service.</span></span>  
  
-   <span data-ttu-id="d1130-107">Hizmet yapılandırma dosyasında hizmetin adı aşağıdaki örnekte gösterildiği gibi seçtiğiniz yeni bir adla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d1130-107">In the configuration file of the service, change the name of the service to the new name you have chosen, as indicated in the following example.</span></span> <span data-ttu-id="d1130-108">Yapılandırma dosyası, barındırma modelinize bağlı olarak app.config veya web.config dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="d1130-108">The configuration file can be either app.config or web.config file depending on your hosting model.</span></span>  
  
```xml  
<system.servicemodel>  
   <services>  
      <service name="WcfService.NewName">  
      </service>  
   </services>  
</system.servicemodel>  
```  
  
-   <span data-ttu-id="d1130-109">Hizmetinizi webhosted ise, bir \*.svc dosyası kullanır.</span><span class="sxs-lookup"><span data-stu-id="d1130-109">If your service is webhosted, it uses an \*.svc file.</span></span> <span data-ttu-id="d1130-110">Svc dosyasını açın ve aşağıdaki örnekte gösterildiği gibi hizmet adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d1130-110">Open the svc file and modify the name of your service as indicated in the following example.</span></span> <span data-ttu-id="d1130-111">Svc dosya olduğundan bu adımı kendini barındıran uygulamalar için gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="d1130-111">This step is not necessary for self-hosted applications, as there is no svc file.</span></span>  
  
```  
<%@ ServiceHost Service="WcfService.NewName">  
```  
  
## <a name="renaming-a-wcf-service-contract"></a><span data-ttu-id="d1130-112">WCF hizmet sözleşmesini yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="d1130-112">Renaming a WCF Service Contract</span></span>  
  
-   <span data-ttu-id="d1130-113">Hizmet sözleşmesi yeniden adlandırmak için aşağıdaki adımları gerçekleştirin,</span><span class="sxs-lookup"><span data-stu-id="d1130-113">Perform the following steps to rename the service contract,</span></span>  
  
-   <span data-ttu-id="d1130-114">Hizmet sözleşmesi adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d1130-114">Change the name of the service contract.</span></span>  
  
-   <span data-ttu-id="d1130-115">Hizmet yapılandırma dosyasında aşağıdaki örnekte gösterildiği gibi hizmet sözleşmesi adı seçtiğiniz yeni bir adla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d1130-115">In the configuration file of the service, change the name of the service contract to the new name you have chosen, as indicated in the following example.</span></span> <span data-ttu-id="d1130-116">Yapılandırma dosyası, barındırma modelinize bağlı olarak app.config veya web.config dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="d1130-116">The configuration file can be either app.config or web.config file depending on your hosting model.</span></span>  
  
```xml  
<system.servicemodel>  
   <services>  
      <service>  
         <endpoint contract="WcfService.NewContractName" />  
      </service>  
   </services>  
</system.servicemodel>  
```
