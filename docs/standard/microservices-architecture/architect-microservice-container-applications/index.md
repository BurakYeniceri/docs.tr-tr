---
title: Tabanlı uygulamalar kapsayıcı ve mikro hizmet tasarlama
description: Kapsayıcılı .NET uygulamaları için .NET mikro hizmet mimarisi | Tabanlı uygulamalar kapsayıcı ve mikro hizmet tasarlama
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 05/26/2017
ms.openlocfilehash: f7933cc25a5fde13113d0c9c278e9bd1730d4f9d
ms.sourcegitcommit: 2eb5ca4956231c1a0efd34b6a9cab6153a5438af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/11/2018
ms.locfileid: "49085978"
---
# <a name="architecting-container--and-microservice-based-applications"></a>Kapsayıcı ve mikro hizmet tabanlı uygulama mimarileri oluşturma

*Mikro hizmetler, harika avantajlar sağlar ancak büyük yeni zorluklar da Yükselt. Mikro hizmet mimarisi desenleri, mikro hizmet tabanlı bir uygulama oluştururken, temel yapı taşları alır.*

Bu kılavuzda daha önce kapsayıcıları ve Docker hakkında temel kavramları öğrendiniz. Bu kapsayıcılar ile başlamak için ihtiyacınız olan en az bilgiyi oluştu. Bu mimari bölümdeki kavramları kapsayıcıları etkinleştiricilerden ve mikro hizmet için harika bir uygun olduğunda bile, bir mikro hizmet mimarisi ve birçok mimari için zorunlu olmasa da, kapsayıcıları çok uygulanabilir. Ancak, bu kılavuz hem kapsayıcıları zaten sunulan önemini nedeniyle kesişimi odaklanır.

Kurumsal uygulamalar genellikle birden çok hizmet yerine tek bir hizmet tabanlı uygulama, oluşan ve karmaşık olabilir. Bu gibi durumlarda, mikro hizmetler ve belirli etki alanı Odaklı Tasarım (DDD) desenleri ve kapsayıcı düzenleme kavramlarını gibi ek mimari yaklaşımlar anlamanız gerekir. Bu bölümde, kapsayıcılar, ancak her kapsayıcılı uygulamayı de yalnızca değil mikro hizmetler açıklanmaktadır unutmayın.

## <a name="container-design-principles"></a>Kapsayıcı tasarım ilkeleri

Kapsayıcı modelinde, bir kapsayıcı görüntü örneğinin tek bir işlem temsil eder. Bir kapsayıcı görüntüsü işlem sınır olarak tanımlayarak işlemin ölçeklendirmek için veya bu toplu iş için kullanılabilir temelleri oluşturabilirsiniz.

Bir kapsayıcı görüntüsü tasarlarken göreceğiniz bir [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/) Dockerfile içinde tanımı. Bu, kapsayıcıyı ömrünü ömürlerinin denetimleri işlem tanımlar. İşlem tamamlandığında, kapsayıcı ömrü sona erer. Kapsayıcılar web sunucuları gibi uzun süre çalışan işlemler temsil, ancak eski adıyla Azure uygulanmıştır toplu temsil kısa süreli işlemler de ister [WebJobs](https://docs.microsoft.com/azure/app-service-web/websites-webjobs-resources).

İşlem başarısız olursa, kapsayıcı sona erer ve orchestrator sürüyorsa. Orchestrator çalışan beş örneklerinin tutmak için yapılandırılmış ve biri başarısız olursa, orchestrator başarısız işlemi değiştirmek için başka bir kapsayıcı örneği oluşturur. Bir batch işinde parametrelerle işlemi başlatıldı. İşlem tamamlandığında, iş tamamlandığında. Bu kılavuz ayrıntısına gitme düzenleyicileri üzerinde daha sonra.

Birden çok işlem tek bir kapsayıcıda çalıştırmak istediğiniz bir senaryo bulabilirsiniz. Bu senaryo için kapsayıcı başına yalnızca bir giriş noktası olabileceği gerektiği gibi çok programları başlatır kapsayıcıdaki bir betik çalıştırabilir. Örneğin, kullanabileceğiniz [gözetmen](http://supervisord.org/) veya birden çok işlem tek bir kapsayıcı içinde başlatılmasını halletmeniz için benzer bir araç. Ancak, tutan kapsayıcı başına birden çok işlem mimarileri bulabilirsiniz olsa da, bu yaklaşımı yaygın değildir.


>[!div class="step-by-step"]
[Önceki](../net-core-net-framework-containers/official-net-docker-images.md)
[İleri](containerize-monolithic-applications.md)
