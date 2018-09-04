---
title: .NET Core yüklemeleri yönetme
description: Birden çok .NET Core SDK ve çalışma zamanı sürümleri ile yan yana yükleme stratejileri çalışma makinenizde yönetin.
author: leecow
ms.author: wiwagn
ms.date: 08/22/2018
ms.openlocfilehash: 06c3f43e7917efb8fd31898044d8f5d920c2cada
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/03/2018
ms.locfileid: "43485482"
---
# <a name="manage-net-core-installations"></a><span data-ttu-id="fb22e-103">.NET Core yüklemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="fb22e-103">Manage .NET Core installations</span></span>

<span data-ttu-id="fb22e-104">.NET core, hem oluşturma hem de .NET Core uygulamaları çalıştırmak için sürüm bağımlılık esneklik etkinleştirilmesi, yan yana birden çok sürümünü mevcut çalışma zamanını ve SDK sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb22e-104">.NET Core allows multiple versions of the SDK and Runtime to exist side-by-side, enabling version dependency flexibility for both building and running .NET Core applications.</span></span> <span data-ttu-id="fb22e-105">Bu yükleme ve otomatik sürüm sarma davranışları okunur eksisi ancak önemli avantajları sunar.</span><span class="sxs-lookup"><span data-stu-id="fb22e-105">These installation and automatic version roll-forward behaviors offer valuable benefits, but one pronounced drawback.</span></span> <span data-ttu-id="fb22e-106">.NET Core çalışma zamanı ve .NET Core SDK'sı güncelleştirme yüklü olarak, önceki sürümler disk üzerinde kalır.</span><span class="sxs-lookup"><span data-stu-id="fb22e-106">As updates of the .NET Core SDK or .NET Core Runtime are installed, previous versions remain on-disk.</span></span> <span data-ttu-id="fb22e-107">Birden çok yüklü sürümlerini zamanla disk kullanımını artırın.</span><span class="sxs-lookup"><span data-stu-id="fb22e-107">Multiple installed versions increase disk usage over time.</span></span> <span data-ttu-id="fb22e-108">50'den fazla .NET Core SDK'sı güncelleştirme yayımladık.</span><span class="sxs-lookup"><span data-stu-id="fb22e-108">More than 50 .NET Core SDK updates have been released.</span></span> <span data-ttu-id="fb22e-109">SDK ve çalışma zamanı kaldırılamadı, sisteminizde yüklü'nın birçok sürümü olabilir.</span><span class="sxs-lookup"><span data-stu-id="fb22e-109">There may be many versions of the SDK and Runtime installed on your system that could be removed.</span></span>

## <a name="safe-to-remove"></a><span data-ttu-id="fb22e-110">Kaldırmak için güvenli mi?</span><span class="sxs-lookup"><span data-stu-id="fb22e-110">Safe to remove?</span></span>

<span data-ttu-id="fb22e-111">[.NET Core sürüm seçimi](selection.md) davranışları ve .NET Core çalışma zamanı uyumluluğunu güncelleştirmeleri arasında önceki sürümlerini güvenli kaldırılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb22e-111">The [.NET Core version selection](selection.md) behaviors and the runtime compatibility of .NET Core across updates enables safe removal of previous versions.</span></span> <span data-ttu-id="fb22e-112">.NET core çalışma zamanı güncelleştirmeleri, bir ana sürüm 1.x ve 2.x'i gibi ' bant' içinde uyumludur.</span><span class="sxs-lookup"><span data-stu-id="fb22e-112">.NET Core runtime updates are compatible within a major version 'band' such as 1.x and 2.x.</span></span> <span data-ttu-id="fb22e-113">Ayrıca, .NET Core SDK'sının daha yeni sürümleri, genellikle, çalışma zamanı, hedef önceki sürümleri uyumlu bir şekilde uygulamalar oluşturmanızı yapılandırabilmeyi sürdürmeniz.</span><span class="sxs-lookup"><span data-stu-id="fb22e-113">Additionally, newer releases of the .NET Core SDK generally maintain the ability to build applications that target previous versions of the runtime in a compatible manner.</span></span>

<span data-ttu-id="fb22e-114">Genel olarak, yalnızca en son SDK'sı ve uygulamanız için gereken çalışma zamanları en son düzeltme eki sürümü gerekir.</span><span class="sxs-lookup"><span data-stu-id="fb22e-114">In general, you only need the latest SDK and latest patch version of the runtimes required for your application.</span></span> <span data-ttu-id="fb22e-115">Örnekleri burada project.json tabanlı uygulamaları sürdürmek tutulan daha eski SDK veya çalışma zamanı sürümleri içerir.</span><span class="sxs-lookup"><span data-stu-id="fb22e-115">Instances where retaining older SDK or Runtime versions include maintaining project.json-based applications.</span></span>  <span data-ttu-id="fb22e-116">Uygulamanızı önceki bir SDK'ları veya çalışma zamanları belirli nedenlerle olmadığı sürece, eski sürümleri güvenli bir şekilde kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb22e-116">Unless your application has specific reasons for earlier SDKs or runtimes, you may safely remove older versions.</span></span>

<span data-ttu-id="fb22e-117">.NET Core kaldırma yöntemleri platformdan platforma değişir ve .NET Core sürümleri arasında biraz değişti.</span><span class="sxs-lookup"><span data-stu-id="fb22e-117">The methods for removing .NET Core vary from platform to platform and have changed somewhat across .NET Core versions.</span></span> <span data-ttu-id="fb22e-118">Artık gerekli .NET Core sürümleri kaldırma hakkında daha fazla bilgi için bkz ['SDK ve .NET Core çalışma zamanı'nı kaldırmak nasıl'](remove-runtime-sdk-versions.md) içinde [.NET Core belgeleri](../index.md).</span><span class="sxs-lookup"><span data-stu-id="fb22e-118">For details on removing versions of .NET Core that are no longer needed, see ['How to remove the .NET Core Runtime and SDK'](remove-runtime-sdk-versions.md) in the [.NET Core documentation](../index.md).</span></span>