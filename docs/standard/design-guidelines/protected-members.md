---
title: "Korumalı üyeleri"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- members [.NET Framework], protected
- protected members
- classes [.NET Framework], unsealed
- classes [.NET Framework], protected members
- unsealed classes
- customizing class behavior
ms.assetid: aa0b58ee-3956-494d-ab48-471ae5db8740
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7c3aacd0f08641c01200f0b1791a78413a306590
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="protected-members"></a><span data-ttu-id="a9662-102">Korumalı üyeleri</span><span class="sxs-lookup"><span data-stu-id="a9662-102">Protected Members</span></span>
<span data-ttu-id="a9662-103">Korumalı üyeleri kendileri tarafından hiçbir genişletilebilirlik sağlamaz, ancak bunlar genişletilebilirlik sınıflara aracılığıyla daha güçlü yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9662-103">Protected members by themselves do not provide any extensibility, but they can make extensibility through subclassing more powerful.</span></span> <span data-ttu-id="a9662-104">Gelişmiş özelleştirme seçenekleri gereksiz yere ana ortak arabirimi karmaşıklaştırarak olmadan kullanıma sunmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9662-104">They can be used to expose advanced customization options without unnecessarily complicating the main public interface.</span></span>  
  
 <span data-ttu-id="a9662-105">Framework tasarımcıları "korumalı" adı yanlış bir fikir güvenlik verebilirsiniz çünkü korumalı üyeleriyle dikkatli olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9662-105">Framework designers need to be careful with protected members because the name "protected" can give a false sense of security.</span></span> <span data-ttu-id="a9662-106">Herhangi bir alt korumasız bir sınıf ve Korumalı Erişim üyeleri için bulabildiği ve bu nedenle aynı genel üyeler için kullanılan savunma kodlama uygulamalarını korumalı üyeleri için geçerli.</span><span class="sxs-lookup"><span data-stu-id="a9662-106">Anyone is able to subclass an unsealed class and access protected members, and so all the same defensive coding practices used for public members apply to protected members.</span></span>  
  
 <span data-ttu-id="a9662-107">**✓ DÜŞÜNÜN** kullanarak korumalı üyeler için Gelişmiş özelleştirme.</span><span class="sxs-lookup"><span data-stu-id="a9662-107">**✓ CONSIDER** using protected members for advanced customization.</span></span>  
  
 <span data-ttu-id="a9662-108">**✓ YAPMAK** korumalı üyeleri korumasız sınıflarında güvenlik, belgelerine ve uyumluluk analiz amacıyla genel olarak ele alın.</span><span class="sxs-lookup"><span data-stu-id="a9662-108">**✓ DO** treat protected members in unsealed classes as public for the purpose of security, documentation, and compatibility analysis.</span></span>  
  
 <span data-ttu-id="a9662-109">Herhangi bir sınıftan ve korumalı üyeleri erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9662-109">Anyone can inherit from a class and access the protected members.</span></span>  
  
 <span data-ttu-id="a9662-110">*Bölümleri © 2005, 2009 Microsoft Corporation. Tüm hakları saklıdır.*</span><span class="sxs-lookup"><span data-stu-id="a9662-110">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="a9662-111">*Pearson eğitim, Inc. şirketinin izni tarafından yeniden yazdırılmaları [Framework tasarım yönergeleri: kuralları, deyimleri ve yeniden kullanılabilir .NET kitaplıkları, 2 sürümü için desenleri](http://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina ve Brad Abrams tarafından 22 Eki 2008 tarafından yayımlanan Microsoft Windows geliştirme serisi bir parçası olarak Addison-Wesley Professional.*</span><span class="sxs-lookup"><span data-stu-id="a9662-111">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](http://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a9662-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="a9662-112">See Also</span></span>  
 [<span data-ttu-id="a9662-113">Framework tasarım yönergeleri</span><span class="sxs-lookup"><span data-stu-id="a9662-113">Framework Design Guidelines</span></span>](../../../docs/standard/design-guidelines/index.md)  
 [<span data-ttu-id="a9662-114">Genişletilebilirlik için tasarlama</span><span class="sxs-lookup"><span data-stu-id="a9662-114">Designing for Extensibility</span></span>](../../../docs/standard/design-guidelines/designing-for-extensibility.md)