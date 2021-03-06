---
title: Veri sağlayıcıları (WCF Veri Hizmetleri) Hizmetleri
ms.date: 03/30/2017
helpviewer_keywords:
- WCF Data Services, providers
ms.assetid: a0160b1b-3d9c-4cc8-8391-cb0986a60a41
ms.openlocfilehash: 7be6578f0b237f986bcb68a3ace10ba04cf06474
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33358885"
---
# <a name="data-services-providers-wcf-data-services"></a>Veri sağlayıcıları (WCF Veri Hizmetleri) Hizmetleri
[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] veri olarak sunmaya yönelik birden çok sağlayıcı modellerini destekleyen bir [!INCLUDE[ssODataFull](../../../../includes/ssodatafull-md.md)] akış. Bu konu en iyi seçmenize olanak sağlamak için bilgi sağlamaktadır [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] veri kaynağı için sağlayıcı.  
  
## <a name="data-source-providers"></a>Veri kaynağı sağlayıcıları  
 [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] Veri Hizmeti veri modelini tanımlamak için aşağıdaki sağlayıcılarını destekler.  
  
|Sağlayıcı|Açıklama|  
|--------------|-----------------|  
|Entity Framework sağlayıcısı|Bu sağlayıcı ADO.NET Entity Framework ilişkisel veri eşleyen bir veri modeli tanımlayarak veri hizmeti ile ilişkisel veri kullanmanızı sağlamak için kullanır. Veri kaynağı SQL Server veya başka bir veri kaynağını Entity Framework'ün üçüncü taraf sağlayıcı desteğiyle olabilir. Bir SQL Server veritabanı gibi bir ilişkisel veri kaynağı varsa, Entity Framework sağlayıcısı kullanmanız gerekir. Daha fazla bilgi için bkz: [Entity Framework sağlayıcısı](../../../../docs/framework/data/wcf/entity-framework-provider-wcf-data-services.md).|  
|Yansıma sağlayıcısı|Örnekleri olarak verilebilen var olan veri sınıfları dayalı bir veri modeli tanımlamanıza olanak sağlamak için bu sağlayıcıyı yansıma kullanan <xref:System.Linq.IQueryable%601> arabirimi. Güncelleştirmeleri uygulayarak etkin <xref:System.Data.Services.IUpdatable> arabirimi. LINQ-SQL tarafından oluşturulan veya türü belirtilmiş bir veri kümesi tarafından tanımlanan gibi çalışma zamanında tanımlanan statik veri sınıfları sahip olduğunda bu sağlayıcı kullanmanız gerekir. Daha fazla bilgi için bkz: [yansıma sağlayıcısı](../../../../docs/framework/data/wcf/reflection-provider-wcf-data-services.md).|  
|Özel veri hizmet sağlayıcıları|[!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] geç bağlama veri türlerine bağlı bir veri modeli dinamik olarak tanımlamanızı sağlayan sağlayıcıları kümesi içerir. Uygulama tasarlandığında yararlanılmasını veri bilinmiyor veya Entity Framework veya yansıma Sağlayıcı yeterli olmadığında bu arabirimleri uygulamanız gerekir. Daha fazla bilgi için bkz: [özel veri hizmeti sağlayıcıları](../../../../docs/framework/data/wcf/custom-data-service-providers-wcf-data-services.md).|  
  
## <a name="other-data-service-providers"></a>Diğer veri hizmeti sağlayıcıları  
 [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)] diğer sağlayıcılardan biri kullanılarak tanımlanmış bir veri kaynağı performansını geliştirir aşağıdaki ek veri hizmeti sağlayıcısı sahiptir.  
  
|Sağlayıcı|Açıklama|  
|--------------|-----------------|  
|Akış sağlayıcısı|Bu sağlayıcı kullanarak ikili büyük nesne veri türlerini kullanıma sağlar [!INCLUDE[ssAstoria](../../../../includes/ssastoria-md.md)]. Bir akış sağlayıcı uygulama tarafından oluşturulan <xref:System.Data.Services.Providers.IDataServiceStreamProvider> arabirimi. Bu sağlayıcı ile birlikte herhangi bir veri kaynağı sağlayıcısına uygulanabilir. Daha fazla bilgi için bkz: [Akış sağlayıcısı](../../../../docs/framework/data/wcf/streaming-provider-wcf-data-services.md).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [WCF Veri Hizmetlerini Tanımlama](../../../../docs/framework/data/wcf/defining-wcf-data-services.md)  
 [Veri Hizmeti Yapılandırma](../../../../docs/framework/data/wcf/configuring-the-data-service-wcf-data-services.md)  
 [Veri Hizmeti Barındırma](../../../../docs/framework/data/wcf/hosting-the-data-service-wcf-data-services.md)
