---
title: .NET derleme Platform SDK'si (Roslyn API)
description: ".NET kodu, nokta hataları anlamak ve bu hataları düzeltmek için .NET derleyici Platform (Roslyn API'ları olarak da bilinir) SDK kullanmayı öğrenin."
keywords: "roslyn, analyzer, kod düzeltme"
author: billwagner
ms.author: wiwagn
ms.date: 10/10/2017
ms.topic: conceptual
ms.prod: .net
ms.devlang: devlang-csharp
ms.custom: mvc
ms.openlocfilehash: 8bebb739805f28bdc192aef7678e762d0aa51016
ms.sourcegitcommit: bf8a3ba647252010bdce86dd914ac6c61b5ba89d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2018
---
# <a name="the-net-compiler-platform-sdk"></a><span data-ttu-id="dde2e-104">.NET derleme Platform SDK'si</span><span class="sxs-lookup"><span data-stu-id="dde2e-104">The .NET Compiler Platform SDK</span></span>

<span data-ttu-id="dde2e-105">Derleyicileri sözdizimi ve bu kodu semantiği doğrulamak uygulama kodunun ayrıntılı bir model oluşturma.</span><span class="sxs-lookup"><span data-stu-id="dde2e-105">Compilers build a detailed model of application code as they validate the syntax and semantics of that code.</span></span> <span data-ttu-id="dde2e-106">Kullanımı bu model kaynak kodunu yürütülebilir çıkışı oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="dde2e-106">The use this model to build the executable output from the source code.</span></span> <span data-ttu-id="dde2e-107">.NET derleme Platform SDK'sı bu modeline erişim sağlar.</span><span class="sxs-lookup"><span data-stu-id="dde2e-107">The .NET Compiler Platform SDK provides access to this model.</span></span> <span data-ttu-id="dde2e-108">Giderek, biz tümleşik geliştirme ortamı (IDE) özelliklerini kullanan yeniden düzenleme, IntelliSense, akıllı yeniden adlandır, "tüm başvuruları Bul" ve "Tanıma Git" gibi bizim üretkenliği artırmak için.</span><span class="sxs-lookup"><span data-stu-id="dde2e-108">Increasingly, we rely on integrated development environment (IDE) features such as IntelliSense, refactoring, intelligent rename, "Find all references," and "Go to definition" to increase our productivity.</span></span> <span data-ttu-id="dde2e-109">Kod çözümleme araçları bizim kod kalitesini ve uygulama yapısında yardımcı olmak için kod oluşturucuları geliştirmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-109">We rely on code analysis tools to improve our code quality, and code generators to aid in application construction.</span></span> <span data-ttu-id="dde2e-110">Bu araçları akıllı aldıkça, çok daha da fazla uygulama kodu işlemek gibi yalnızca derleyicileri oluşturduğunuz modelinin erişim.</span><span class="sxs-lookup"><span data-stu-id="dde2e-110">As these tools get smarter, they need access to more and more of the model that only compilers create as they process application code.</span></span> <span data-ttu-id="dde2e-111">Çekirdek Görev Roslyn API'leri budur: siyah kutuları açma ve araçları ve son kullanıcıların bilgi derleyicileri bol içinde paylaşmak izin vererek kodumuza hakkında sahip.</span><span class="sxs-lookup"><span data-stu-id="dde2e-111">This is the core mission of the Roslyn APIs: opening up the black boxes and allowing tools and end users to share in the wealth of information compilers have about our code.</span></span>
<span data-ttu-id="dde2e-112">Roslyn, aracılığıyla donuk kaynak kod içinde ve nesne kodu genişletme çevirmenler yerine derleyicileri platformları hale: araç ve uygulama kodu ilgili görevler için kullanabileceğiniz bir API.</span><span class="sxs-lookup"><span data-stu-id="dde2e-112">Instead of being opaque source-code-in and object-code-out translators, through Roslyn, compilers become platforms: APIs that you can use for code-related tasks in your tools and applications.</span></span>

## <a name="net-compiler-platform-sdk-concepts"></a><span data-ttu-id="dde2e-113">.NET derleme Platform SDK'sı kavramları</span><span class="sxs-lookup"><span data-stu-id="dde2e-113">.NET Compiler Platform SDK concepts</span></span>

<span data-ttu-id="dde2e-114">.NET derleme Platform SDK'sı odaklanmış kod araçları ve uygulamaları oluşturmak için girişe engel önemli ölçüde azaltır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-114">The .NET Compiler Platform SDK dramatically lowers the barrier to entry for creating code focused tools and applications.</span></span> <span data-ttu-id="dde2e-115">C# ve VB diller ve C# ve VB etki alanı belirli dillerde katıştırma meta programlama kodu oluşturma ve dönüştürme, etkileşimli kullanımı gibi alanlarda yenilik için birçok fırsatlar yaratır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-115">It creates many opportunities for innovation in areas such as meta-programming, code generation and transformation, interactive use of the C# and VB languages, and embedding of C# and VB in domain specific languages.</span></span>

<span data-ttu-id="dde2e-116">.NET derleme Platform SDK'sı oluşturmanıza olanak sağlayan ***çözümleyiciler*** ve ***kod düzeltmeleri*** bulmak ve kodlama hataları düzeltin.</span><span class="sxs-lookup"><span data-stu-id="dde2e-116">The .NET Compiler Platform SDK enables you to build ***analyzers*** and ***code fixes*** that find and correct coding mistakes.</span></span> <span data-ttu-id="dde2e-117">***Çözümleyiciler*** sözdizimi ve kod yapısını anlamak ve düzeltilmesi uygulamalar algılayabilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-117">***Analyzers*** understand the syntax and structure of code and detect practices that should be corrected.</span></span> <span data-ttu-id="dde2e-118">***Kod düzeltmeleri*** çözümleyicileri tarafından bulunan kodlama hataları ele almak için bir veya daha fazla önerilen düzeltmeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="dde2e-118">***Code fixes*** provide one or more suggested fixes for addressing coding mistakes found by analyzers.</span></span> <span data-ttu-id="dde2e-119">Genellikle, bir Çözümleyicisi ve ilişkili kodu düzeltmeleri tek bir projede birlikte paketlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-119">Typically, an analyzer and the associated code fixes are packaged together in a single project.</span></span> 

<span data-ttu-id="dde2e-120">Çözümleyicileri ve kod düzeltmeleri statik çözümleme kod anlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="dde2e-120">Analyzers and code fixes use static analysis to understand code.</span></span> <span data-ttu-id="dde2e-121">Bunlar kodu çalıştırmayın ve diğer sınama fayda sağlar.</span><span class="sxs-lookup"><span data-stu-id="dde2e-121">They do not run the code or provide other testing benefits.</span></span> <span data-ttu-id="dde2e-122">Bunlar Bununla birlikte, hatalar, unmaintanable kodu veya standart kılavuz doğrulama genellikle sağlama yöntemleri çıkışı işaret edebilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-122">They can, however, point out practices that often lead to bugs, unmaintanable code, or standard guideline validation.</span></span>

<span data-ttu-id="dde2e-123">.NET derleme Platform SDK'sı, tek bir inceleyin ve C# veya Visual Basic codebase anlamanıza olanak sağlayan API kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="dde2e-123">The .NET Compiler Platform SDK provides a single set of APIs that enable you to examine and understand a C# or Visual Basic codebase.</span></span> <span data-ttu-id="dde2e-124">Bu tek codebase kullanabileceğinizden çözümleyiciler yazabilir ve sözdizimsel ve anlamsal analiz API'leri .NET derleme Platform SDK tarafından sağlanan yararlanarak kodu daha kolay giderir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-124">Because you can use this single codebase, you can write analyzers and code fixes more easily by leveraging the syntactic and semantic analysis APIs provided by the .NET Compiler Platform SDK.</span></span> <span data-ttu-id="dde2e-125">Derleyici tarafından yapılan anaysis çoğaltılan büyük görevden serbest, proje veya kitaplık için ortak kodlama hataları bulma ve düzeltme daha odaklı görevini üzerinde odaklanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dde2e-125">Freed from the large task of replicating the anaysis done by the compiler, you can concentrate on the more focused task of finding and fixing common coding errors for your project or library.</span></span>

<span data-ttu-id="dde2e-126">Daha küçük bir avantajı Çözümleyicileri ve kod düzeltmeleri daha küçüktür ve kendi yazdıysanız bunlar projesinde kodu anlamak için codebase daha Visual Studio'da yüklendiğinde çok az bellek kullanır ' dir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-126">A smaller benefit is that your analyzers and code fixes are smaller and use much less memory when loaded in Visual Studio than they would if you wrote your own codebase to understand the code in a project.</span></span> <span data-ttu-id="dde2e-127">Derleyici ve Visual Studio tarafından kullanılan aynı sınıflarını yararlanarak kendi statik çözümleme araçları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dde2e-127">By leveraging the same classes used by the compiler and Visual Studio, you can create your own static analysis tools.</span></span> <span data-ttu-id="dde2e-128">Bunun anlamı ekibinizin çözümleyiciler kullanabilirsiniz ve IDE'nin performansı belirgin bir etkisi olmadan kod giderir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-128">This means your team can use analyzers and code fixes without a noticeable impact on the IDE's performance.</span></span>

<span data-ttu-id="dde2e-129">Çözümleyicileri ve kod düzeltmeleri yazmak için üç ana senaryo vardır:</span><span class="sxs-lookup"><span data-stu-id="dde2e-129">There are three main scenarios for writing analyzers and code fixes:</span></span>

1. [<span data-ttu-id="dde2e-130">*Kodlama standartları takım zorla*</span><span class="sxs-lookup"><span data-stu-id="dde2e-130">*Enforce team coding standards*</span></span>](#enforce-team-coding-standards)
1. [<span data-ttu-id="dde2e-131">*Kitaplık paketleriyle rehberlik sağlar*</span><span class="sxs-lookup"><span data-stu-id="dde2e-131">*Provide guidance with library packages*</span></span>](#provide-guidance-with-library-packages)
1. [<span data-ttu-id="dde2e-132">*Genel kodlama rehberlik sağlar*</span><span class="sxs-lookup"><span data-stu-id="dde2e-132">*Provide general coding guidance*</span></span>](#provide-general-coding-guidance)

## <a name="enforce-team-coding-standards"></a><span data-ttu-id="dde2e-133">Kodlama standartları takım zorla</span><span class="sxs-lookup"><span data-stu-id="dde2e-133">Enforce team coding standards</span></span>

<span data-ttu-id="dde2e-134">Birçok ekip kodlama kod incelemeleri diğer takım üyeleri ile aracılığıyla zorlanan standartları vardır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-134">Many teams have coding standards that are enforced through code reviews with other team members.</span></span> <span data-ttu-id="dde2e-135">Çözümleyicileri ve kod düzeltmeleri bu işlem çok daha verimli hale getirebilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-135">Analyzers and code fixes can make this process much more efficient.</span></span> <span data-ttu-id="dde2e-136">Bir geliştirici kendi iş başkalarıyla ekipte paylaşır kod incelemeleri meydana gelir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-136">Code reviews happen when a developer shares his work with others on the team.</span></span> <span data-ttu-id="dde2e-137">Daha yeni bir özellik açıklamaları almadan önce tamamlamak için gereken her zaman yatırım yapmış kullanıcılar.</span><span class="sxs-lookup"><span data-stu-id="dde2e-137">He will have invested all the time needed to complete a new feature before getting any comments.</span></span> <span data-ttu-id="dde2e-138">Müşterinizle ekibin yöntemler eşleşmeyen alışkanlıklarınıza eklenir ancak hafta gidin.</span><span class="sxs-lookup"><span data-stu-id="dde2e-138">Weeks may go by while he reinforces habits that don't match the team's practices.</span></span>

<span data-ttu-id="dde2e-139">Bir geliştirici kod yazar gibi çözümleyiciler çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="dde2e-139">Analyzers run as a developer writes code.</span></span> <span data-ttu-id="dde2e-140">Hüseyin, yönergeleri hemen teşvik eden anında geri bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-140">He gets immediate feedback that encourages following the guidance immediately.</span></span> <span data-ttu-id="dde2e-141">Cüneyt, kendisinin prototipi oluşturulurken başlar başlamaz uyumlu kod yazmaya alışkanlıklarınıza oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dde2e-141">He builds habits to write compliant code as soon as he begins prototyping.</span></span> <span data-ttu-id="dde2e-142">Özellik insanlar gözden geçirmek için hazır olduğunda, tüm standart Kılavuzu zorlandı.</span><span class="sxs-lookup"><span data-stu-id="dde2e-142">When the feature is ready for humans to review, all the standard guidance has been enforced.</span></span>

<span data-ttu-id="dde2e-143">Takımlar çözümleyiciler oluşturabilirsiniz ve görünüm yöntemler kodlama takım ihlal en sık kullanılan uygulamalar için kod giderir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-143">Teams can build analyzers and code fixes that look for the most common practices that violate team coding practices.</span></span> <span data-ttu-id="dde2e-144">Bu standartları zorlamak için her geliştiricinin makinesinde yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-144">These can be installed on each developer's machine to enforce the standards.</span></span>

## <a name="provide-guidance-with-library-packages"></a><span data-ttu-id="dde2e-145">Kitaplık paketleriyle rehberlik sağlar</span><span class="sxs-lookup"><span data-stu-id="dde2e-145">Provide guidance with library packages</span></span>

<span data-ttu-id="dde2e-146">Bol miktarda kitaplıkları NuGet üzerinde .NET geliştiricileri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-146">There are a wealth of libraries available for .NET developers on NuGet.</span></span>
<span data-ttu-id="dde2e-147">Bazı Microsoft bu geliyor, bazı üçüncü taraf şirketlerden ve diğer topluluk üyeleri ve gönüllüsü.</span><span class="sxs-lookup"><span data-stu-id="dde2e-147">Some of these come from Microsoft, some from third-party companies, and others from community members and volunteers.</span></span> <span data-ttu-id="dde2e-148">Geliştiricilerin bu kitaplıklarıyla başarılı olduğunda bu kitaplıklar daha fazla benimseme ve daha yüksek incelemeler alın.</span><span class="sxs-lookup"><span data-stu-id="dde2e-148">These libraries get more adoption and higher reviews when developers can succeed with those libraries.</span></span>

<span data-ttu-id="dde2e-149">Belge sağlamanın yanı sıra, Çözümleyicileri ve bulma ve hatalı yaygın kullanımları kitaplığınızın düzeltmek kod düzeltmeler sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-149">In addition to providing documentation, you can provide analyzers and code fixes that find and correct common mis-uses of your library.</span></span> <span data-ttu-id="dde2e-150">Bu hemen düzeltmeleri daha hızlı başarılı geliştiricilere yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="dde2e-150">These immediate corrections will help developers succeed more quickly.</span></span> 

<span data-ttu-id="dde2e-151">Çözümleyiciler paketleyebilirsiniz ve kitaplığınızı NuGet ile kod giderir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-151">You can package analyzers and code fixes with your library on NuGet.</span></span> <span data-ttu-id="dde2e-152">Bu senaryoda, NuGet paketini yükleyen her geliştiricinin Çözümleyicisi paketi de yüklenir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-152">In that scenario, every developer who installs your NuGet package will also install the analyzer package.</span></span> <span data-ttu-id="dde2e-153">Kitaplık kullanan tüm geliştiriciler hemen Kılavuzu, ekibinden anında geri bildirim hataları ve önerilen düzeltmeler biçiminde alır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-153">All developers using your library will immediately get guidance from your team in the form of immediate feedback on mistakes and suggested corrections.</span></span>

## <a name="provide-general-guidance"></a><span data-ttu-id="dde2e-154">Genel rehberlik sağlar</span><span class="sxs-lookup"><span data-stu-id="dde2e-154">Provide general guidance</span></span>

<span data-ttu-id="dde2e-155">.NET Geliştirici topluluğu iyi iş deneyimi desenleri ve en iyi kaçınılması desenleri buldu.</span><span class="sxs-lookup"><span data-stu-id="dde2e-155">The .NET developer community has discovered through experience patterns that work well and patterns that are best avoided.</span></span> <span data-ttu-id="dde2e-156">Birkaç topluluk üyeleri bu önerilen desenlerinin zorunlu çözümleyiciler oluşturdunuz.</span><span class="sxs-lookup"><span data-stu-id="dde2e-156">Several community members have created analyzers that enforce those recommended patterns.</span></span> <span data-ttu-id="dde2e-157">Size daha fazla bilgi edinin olarak da her zaman yeni fikirleri yer yoktur.</span><span class="sxs-lookup"><span data-stu-id="dde2e-157">As we learn more, there is always room for new ideas.</span></span>

<span data-ttu-id="dde2e-158">Bu çözümleyiciler karşıya yüklenebilir [Visual Studio Market'te](https://marketplace.visualstudio.com/vs) ve Visual Studio kullanarak geliştiriciler tarafından indirilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-158">These analyzers can be uploaded to the [Visual Studio Marketplace](https://marketplace.visualstudio.com/vs) and downloaded by developers using Visual Studio.</span></span> <span data-ttu-id="dde2e-159">Yeni gelenlere dili ve platformu için kendi .NET gezisine önceki üretken ve kabul edilen yöntemler hızlıca öğrenin.</span><span class="sxs-lookup"><span data-stu-id="dde2e-159">Newcomers to the language and the platform learn accepted practices quickly and become productive earlier in their .NET journey.</span></span> <span data-ttu-id="dde2e-160">Bunlar daha yaygın kullanılan hale topluluk bu yöntemler devralır.</span><span class="sxs-lookup"><span data-stu-id="dde2e-160">As these become more widely used, the community adopts these practices.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dde2e-161">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="dde2e-161">Next steps</span></span>

<span data-ttu-id="dde2e-162">.NET derleme Platform SDK kod oluşturma, çözümleme ve yeniden düzenleme için en son dil nesne modelleri içerir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-162">The .NET Compiler Platform SDK includes the latest language object models for code generation, analysis, and refactoring.</span></span> <span data-ttu-id="dde2e-163">Bu bölümde, .NET derleme Platform SDK'sı kavramsal genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="dde2e-163">This section provides a conceptual overview of the .NET Compiler Platform SDK.</span></span> <span data-ttu-id="dde2e-164">Daha ayrıntılı bilgi quickstarts, örnekler ve öğreticiler bölümlerde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="dde2e-164">Further details can be found in the quickstarts, samples and tutorials sections.</span></span>

<span data-ttu-id="dde2e-165">Aşağıdaki dört konulardaki .NET derleyici Platform SDK'sı kavramları hakkında daha fazla bilgi edinebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="dde2e-165">You can learn more about the concepts in the .NET Compiler Platform SDK in these four topics:</span></span>

 - [<span data-ttu-id="dde2e-166">Derleyici API modelini anlama</span><span class="sxs-lookup"><span data-stu-id="dde2e-166">Understand the compiler API model</span></span>](compiler-api-model.md)
 - [<span data-ttu-id="dde2e-167">Söz dizimi ile çalışma</span><span class="sxs-lookup"><span data-stu-id="dde2e-167">Work with syntax</span></span>](work-with-syntax.md)
 - [<span data-ttu-id="dde2e-168">Semantik ile çalışma</span><span class="sxs-lookup"><span data-stu-id="dde2e-168">Work with semantics</span></span>](work-with-semantics.md)
 - [<span data-ttu-id="dde2e-169">Bir çalışma alanı ile çalışma</span><span class="sxs-lookup"><span data-stu-id="dde2e-169">Work with a workspace</span></span>](work-with-workspace.md)

<!--

Turn this on as more of the conceptual content is in place:
- Try the [Quickstarts](quickstart/index.md) to create your first tutorial.
- Experiment with one of the [Tutorials](tutorials/index.md).
- Explore the [Samples](samples/index.md) to see some simple analyzers.
- Read the [Concepts](concepts/index.md) to understand the ideas behind analyzers and code fixes.

-->