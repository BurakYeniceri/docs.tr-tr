---
title: "Nasıl yapılır: String.Split (C# Kılavuzu) kullanarak dizeleri ayrıştırma"
description: "String.Split sınırlayıcıları kümesinden bölünmüş bir dizeler dizisi döndürür. Dizeleri ayrıştırma kolay bir yoludur."
ms.date: 01/03/2018
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- splitting strings [C#]
- Split method [C#]
- strings [C#], splitting
- parse strings
ms.assetid: 729c2923-4169-41c6-9c90-ef176c1e2953
author: BillWagner
ms.author: wiwagn
ms.custom: mvc
ms.openlocfilehash: fc1032f2cdf6706ec933323643dbf6ecff3e9f6f
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/17/2018
---
# <a name="how-to-parse-strings-using-stringsplit-c-guide"></a><span data-ttu-id="4f518-104">Nasıl yapılır: String.Split (C# Kılavuzu) kullanarak dizeleri ayrıştırma</span><span class="sxs-lookup"><span data-stu-id="4f518-104">How to: Parse Strings Using String.Split (C# Guide)</span></span>

<span data-ttu-id="4f518-105"><xref:System.String.Split%2A?displayProperty=nameWithType> Yöntemi, bir veya daha fazla ayırıcıları temel giriş dizesi bölerek alt dizeler dizisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f518-105">The <xref:System.String.Split%2A?displayProperty=nameWithType> method creates an array of substrings by splitting the input string based on one or more delimiters.</span></span> <span data-ttu-id="4f518-106">Bir dize word sınırlarındaki ayırmak için genellikle en kolay yoludur.</span><span class="sxs-lookup"><span data-stu-id="4f518-106">It is often the easiest way to separate a string on word boundaries.</span></span> <span data-ttu-id="4f518-107">Ayrıca, dizeleri diğer özel karakterler veya dizeleri bölme için de kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f518-107">It is also used to split strings on other specific characters or strings.</span></span>

<span data-ttu-id="4f518-108">Aşağıdaki kodu her sözcüğün dizelerden oluşan bir dizi ortak bir deyim ayıran.</span><span class="sxs-lookup"><span data-stu-id="4f518-108">The following code splits a common phrase into an array of strings for each word.</span></span>
<span data-ttu-id="4f518-109">Kendiniz tuşlarına basarak deneyin *çalıştırmak* düğmesi.</span><span class="sxs-lookup"><span data-stu-id="4f518-109">Try it yourself by pressing the *Run* button.</span></span>

[!code-csharp-interactive[split strings on word boundaries](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#1)]

<span data-ttu-id="4f518-110">Her bir ayırıcı karakter örneğini döndürülen dizideki bir değer oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4f518-110">Every instance of a separator character produces a value in the returned array.</span></span> <span data-ttu-id="4f518-111">Ardışık ayırıcı karakter boş dize verilen dizi değer olarak üretir.</span><span class="sxs-lookup"><span data-stu-id="4f518-111">Consecutive separator characters produce the empty string as a value in the returned array.</span></span>  <span data-ttu-id="4f518-112">Bu alan bir ayırıcı olarak kullanan aşağıdaki örnekte görebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4f518-112">You can see this in the following example, which uses space as a separator:</span></span>

[!code-csharp-interactive[split strings with repeated separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#2)]

<span data-ttu-id="4f518-113">Bu davranış biçimleri için tablo verileri temsil eden virgülle ayrılmış değerler (CSV) dosyaları gibi kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="4f518-113">This behavior makes it easier for formats like comma separated values (CSV) files representing tabular data.</span></span> <span data-ttu-id="4f518-114">Ardışık virgül boş bir sütunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4f518-114">Consecutive commas represent a blank column.</span></span>

<span data-ttu-id="4f518-115">İsteğe bağlı bir geçirebilirsiniz <xref:System.StringSplitOptions.RemoveEmptyEntries?displayProperty=fullName> herhangi boş dizeler döndürülen dizideki dışlamak için parametre.</span><span class="sxs-lookup"><span data-stu-id="4f518-115">You can pass an optional <xref:System.StringSplitOptions.RemoveEmptyEntries?displayProperty=fullName> parameter to exclude any empty strings in the returned array.</span></span> <span data-ttu-id="4f518-116">Döndürülen koleksiyon daha karmaşık işlenmesi için kullandığınız [LINQ](../programming-guide/concepts/linq/index.md) Sonuç dizisini denetlemek için.</span><span class="sxs-lookup"><span data-stu-id="4f518-116">For more complicated processing of the returned collection, you can use [LINQ](../programming-guide/concepts/linq/index.md) to manipulate the result sequence.</span></span>    

<span data-ttu-id="4f518-117"><xref:System.String.Split%2A?displayProperty=nameWithType>birden çok ayırıcı karakter kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f518-117"><xref:System.String.Split%2A?displayProperty=nameWithType> can use multiple separator characters.</span></span> <span data-ttu-id="4f518-118">Aşağıdaki örnek, boşluk, virgül, nokta, iki nokta üst üste ve sekmeler, tüm bu karakterler için ayırma içeren bir dizi geçirilen kullanır <xref:System.String.Split%2A>.</span><span class="sxs-lookup"><span data-stu-id="4f518-118">The following example uses spaces, commas, periods, colons, and tabs, all passed in an array containing these separating characters, to <xref:System.String.Split%2A>.</span></span>  <span data-ttu-id="4f518-119">Kod alt döngü her sözcüklerin döndürülen dizideki görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4f518-119">The loop at the bottom of the code displays each of the words in the returned array.</span></span>  

[!code-csharp-interactive[split strings using multiple separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#3)]

<span data-ttu-id="4f518-120">Tüm ayırıcı ardışık örnekleri çıkış dizisi boş dizesinde üretir:</span><span class="sxs-lookup"><span data-stu-id="4f518-120">Consecutive instances of any separator produce the empty string in the output array:</span></span>

[!code-csharp-interactive[split strings using multiple consecutive separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#4)]

<span data-ttu-id="4f518-121"><xref:System.String.Split%2A?displayProperty=nameWithType>dizeler (tek karakter yerine hedef dizesini ayrıştırmak için ayırıcı olarak davranmak karakter sıraları) dizisi alabilir.</span><span class="sxs-lookup"><span data-stu-id="4f518-121"><xref:System.String.Split%2A?displayProperty=nameWithType> can take an array of strings (character sequences that act as separators for parsing the target string, instead of single characters).</span></span>  
  
[!code-csharp-interactive[split strings using strings as separators](../../../samples/snippets/csharp/how-to/strings/ParseStringsUsingSplit.cs#5)]

<span data-ttu-id="4f518-122">Kodda bakarak bu örnekleri deneyebilirsiniz bizim [GitHub deposunu](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings)</span><span class="sxs-lookup"><span data-stu-id="4f518-122">You can try these samples by looking at the code in our [GitHub repository](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings)</span></span>

## <a name="see-also"></a><span data-ttu-id="4f518-123">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4f518-123">See Also</span></span>  
 [<span data-ttu-id="4f518-124">C# Programlama Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="4f518-124">C# Programming Guide</span></span>](../programming-guide/index.md)  
 [<span data-ttu-id="4f518-125">Dizeler</span><span class="sxs-lookup"><span data-stu-id="4f518-125">Strings</span></span>](../programming-guide/strings/index.md)  
 [<span data-ttu-id="4f518-126">.NET framework normal ifadeleri</span><span class="sxs-lookup"><span data-stu-id="4f518-126">.NET Framework Regular Expressions</span></span>](https://msdn.microsoft.com/library/hs600312)