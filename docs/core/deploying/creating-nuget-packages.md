---
title: Çapraz Platform araçları ile bir NuGet paketi oluşturma
description: Bir NuGet paketi 'dotnet pack' komutuyla oluşturmayı öğrenin.
author: cartermp
ms.author: mairaw
ms.date: 06/20/2016
ms.technology: dotnet-cli
ms.openlocfilehash: 6be94c2e2cef443f69b2d6df7c2d490cb1fb629d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33219462"
---
# <a name="how-to-create-a-nuget-package-with-cross-platform-tools"></a><span data-ttu-id="8405d-103">Çapraz Platform araçları ile bir NuGet paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8405d-103">How to Create a NuGet Package with Cross Platform Tools</span></span>

> [!NOTE]
> <span data-ttu-id="8405d-104">UNIX kullanarak komut satırı örnekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8405d-104">The following shows command-line samples using Unix.</span></span>  <span data-ttu-id="8405d-105">`dotnet pack` Aşağıda gösterildiği gibi komutu Windows'da aynı şekilde çalışır.</span><span class="sxs-lookup"><span data-stu-id="8405d-105">The `dotnet pack` command as shown here works the same way on Windows.</span></span>

<span data-ttu-id="8405d-106">.NET Core 1.0 için kitaplıkları NuGet paketleri olarak dağıtılmış beklenir.</span><span class="sxs-lookup"><span data-stu-id="8405d-106">For .NET Core 1.0, libraries are expected to be distributed as NuGet packages.</span></span>  <span data-ttu-id="8405d-107">Aslında nasıl tüm .NET standart kitaplıkları dağıtılmış tüketilen ve budur.</span><span class="sxs-lookup"><span data-stu-id="8405d-107">This is in fact how all of the .NET Standard libraries are distributed and consumed.</span></span>  <span data-ttu-id="8405d-108">Bu en kolay gerçekleştirilir `dotnet pack` komutu.</span><span class="sxs-lookup"><span data-stu-id="8405d-108">This is most easily done with the `dotnet pack` command.</span></span>

<span data-ttu-id="8405d-109">Yalnızca NuGet dağıtmak istediğiniz bir harika yeni kitaplık yazdığınız düşünün.</span><span class="sxs-lookup"><span data-stu-id="8405d-109">Imagine that you just wrote an awesome new library that you would like to distribute over NuGet.</span></span>  <span data-ttu-id="8405d-110">Bir NuGet paketi ile tam olarak bunu yapmak için platformu araçları çapraz oluşturabilirsiniz!</span><span class="sxs-lookup"><span data-stu-id="8405d-110">You can create a NuGet package with cross platform tools to do exactly that!</span></span>  <span data-ttu-id="8405d-111">Aşağıdaki örnek adlı bir kitaplık varsayar **SuperAwesomeLibrary** hangi hedefleri `netstandard1.0`.</span><span class="sxs-lookup"><span data-stu-id="8405d-111">The following example assumes a library called **SuperAwesomeLibrary** which targets `netstandard1.0`.</span></span>

<span data-ttu-id="8405d-112">Geçişli bağımlılıkları varsa; diğer bir deyişle, başka bir projeye bağlıdır bir proje çözümünüzle birlikte paketlerini geri yüklemek emin olmak ihtiyacınız vardır `dotnet restore` bir NuGet paketi oluşturmadan önce komutu.</span><span class="sxs-lookup"><span data-stu-id="8405d-112">If you have transitive dependencies; that is, a project which depends on another project, you'll need to make sure to restore packages for your entire solution with the `dotnet restore` command before creating a NuGet package.</span></span>  <span data-ttu-id="8405d-113">Bunu yapmazsanız neden olur `dotnet pack` düzgün çalışmasını komutu.</span><span class="sxs-lookup"><span data-stu-id="8405d-113">Failing to do so will result in the `dotnet pack` command to not work properly.</span></span>

[!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]


<span data-ttu-id="8405d-114">Olduktan paketler geri yüklenir, bir kitaplık nerede yaşıyor dizinine gidin:</span><span class="sxs-lookup"><span data-stu-id="8405d-114">After ensuring packages are restored, you can navigate to the directory where a library lives:</span></span>

`$ cd src/SuperAwesomeLibrary`

<span data-ttu-id="8405d-115">Yalnızca tek bir komut komut satırından sonra:</span><span class="sxs-lookup"><span data-stu-id="8405d-115">Then it's just a single command from the command line:</span></span>
    
`$ dotnet pack`

<span data-ttu-id="8405d-116">`/bin/Debug` Klasörü şimdi şuna benzeyebilir:</span><span class="sxs-lookup"><span data-stu-id="8405d-116">Your `/bin/Debug` folder will now look like this:</span></span>

```
$ ls bin/Debug

netstandard1.0/
SuperAwesomeLibrary.1.0.0.nupkg
SuperAwesomeLibrary.1.0.0.symbols.nupkg
```

<span data-ttu-id="8405d-117">Bu hata ayıklaması işleyebilen bir paket oluşturur unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8405d-117">Note that this will produce a package which is capable of being debugged.</span></span>  <span data-ttu-id="8405d-118">Bir NuGet paketi yayın ikililerini oluşturmak istiyorsanız, tüm yapmanız gereken ekleyin `-c` / `--configuration` geçin ve kullanmak `release` bağımsız değişkeni olarak.</span><span class="sxs-lookup"><span data-stu-id="8405d-118">If you want to build a NuGet package with release binaries, all you need to do is add the `-c`/`--configuration` switch and use `release` as the argument.</span></span>

`$ dotnet pack --configuration release`

<span data-ttu-id="8405d-119">`/bin` Klasörü şimdi sahip olacak bir `release` NuGet paketinizle yayın ikili dosyaları içeren klasör:</span><span class="sxs-lookup"><span data-stu-id="8405d-119">Your `/bin` folder will now have a `release` folder containing your NuGet package with release binaries:</span></span>

```
$ ls bin/release

netstandard1.0/
SuperAwesomeLibrary.1.0.0.nupkg
SuperAwesomeLibrary.1.0.0.symbols.nupkg
```

<span data-ttu-id="8405d-120">Ve şimdi bir NuGet paketi yayımlamak için gerekli dosyaları!</span><span class="sxs-lookup"><span data-stu-id="8405d-120">And now you have the necessary files to publish a NuGet package!</span></span>

## <a name="dont-confuse-dotnet-pack-with-dotnet-publish"></a><span data-ttu-id="8405d-121">Karıştırmayın `dotnet pack` ile `dotnet publish`</span><span class="sxs-lookup"><span data-stu-id="8405d-121">Don't confuse `dotnet pack` with `dotnet publish`</span></span>

<span data-ttu-id="8405d-122">Herhangi bir noktada olduğunu dikkate almak önemlidir `dotnet publish` komut söz konusu.</span><span class="sxs-lookup"><span data-stu-id="8405d-122">It is important to note that at no point is the `dotnet publish` command involved.</span></span>  <span data-ttu-id="8405d-123">`dotnet publish` Komuttur dağıtılmış ve NuGet üzerinden tüketilen bir NuGet paketi oluşturma değil aynı gruptaki -, bağımlılıklarının tümü ile uygulamaları dağıtmak için.</span><span class="sxs-lookup"><span data-stu-id="8405d-123">The `dotnet publish` command is for deploying applications with all of their dependencies in the same bundle -  not for generating a NuGet package to be distributed and consumed via NuGet.</span></span>
