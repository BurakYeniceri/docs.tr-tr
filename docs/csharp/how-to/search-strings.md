---
title: "Nasıl yapılır: arama dizeleri (C# Kılavuzu)"
ms.date: 02/21/2018
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
helpviewer_keywords:
- searching strings [C#]
- strings [C#], searching with String methods
- strings [C#], searching with regular expressions
ms.assetid: fb1d9a6d-598d-4a35-bd5f-b86012edcb2b
ms.author: wiwagn
ms.openlocfilehash: 60d31a3d6d694c04d0c93b96816928e2ccbd3fba
ms.sourcegitcommit: d95a91d685565f4d95c8773b558752864a6a3d7e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2018
---
# <a name="how-to-search-strings"></a><span data-ttu-id="84ba2-102">Nasıl yapılır: dizeleri arama</span><span class="sxs-lookup"><span data-stu-id="84ba2-102">How to: search strings</span></span>

<span data-ttu-id="84ba2-103">Dizelerdeki metni aramak için iki ana stratejileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="84ba2-103">You can use two main strategies to search for text in strings.</span></span> <span data-ttu-id="84ba2-104">Yöntemlerinin <xref:System.String> belirli bir metni sınıfı arayın.</span><span class="sxs-lookup"><span data-stu-id="84ba2-104">Methods of the <xref:System.String> class search for specific text.</span></span> <span data-ttu-id="84ba2-105">Normal ifadeler metin düzenleri arayın.</span><span class="sxs-lookup"><span data-stu-id="84ba2-105">Regular expressions search for patterns in text.</span></span>

[!INCLUDE[interactive-note](~/includes/csharp-interactive-note.md)]

<span data-ttu-id="84ba2-106">[Dize](../language-reference/keywords/string.md) türü olan bir diğer ad için <xref:System.String?displayProperty=nameWithType> sınıfı, çeşitli dize içeriğini aramak için kullanışlı yöntemler sağlar.</span><span class="sxs-lookup"><span data-stu-id="84ba2-106">The [string](../language-reference/keywords/string.md) type, which is an alias for the <xref:System.String?displayProperty=nameWithType> class, provides a number of useful methods for searching the contents of a string.</span></span> <span data-ttu-id="84ba2-107">Bunlar arasında olan <xref:System.String.Contains%2A>, <xref:System.String.StartsWith%2A>, <xref:System.String.EndsWith%2A>, <xref:System.String.IndexOf%2A>, <xref:System.String.LastIndexOf%2A>.</span><span class="sxs-lookup"><span data-stu-id="84ba2-107">Among them are <xref:System.String.Contains%2A>, <xref:System.String.StartsWith%2A>, <xref:System.String.EndsWith%2A>, <xref:System.String.IndexOf%2A>, <xref:System.String.LastIndexOf%2A>.</span></span> <span data-ttu-id="84ba2-108"><xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType> Sınıfı metin kalıpları aramak için zengin bir sözlüğünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="84ba2-108">The <xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType> class provides a rich vocabulary to search for patterns in text.</span></span> <span data-ttu-id="84ba2-109">Bu makalede, bu teknikler ve gereksinimleriniz için en iyi yöntem seçme öğrenin.</span><span class="sxs-lookup"><span data-stu-id="84ba2-109">In this article, you learn these techniques and how to choose the best method for your needs.</span></span>

## <a name="does-a-string-contain-text"></a><span data-ttu-id="84ba2-110">Bir dize metin içeriyor mu?</span><span class="sxs-lookup"><span data-stu-id="84ba2-110">Does a string contain text?</span></span>

<span data-ttu-id="84ba2-111"><xref:System.String.Contains%2A?displayProperty=nameWithType>, <xref:System.String.StartsWith%2A?displayProperty=nameWithType> Ve <xref:System.String.EndsWith%2A?displayProperty=nameWithType> yöntemleri arama belirli bir metin dizesi.</span><span class="sxs-lookup"><span data-stu-id="84ba2-111">The <xref:System.String.Contains%2A?displayProperty=nameWithType>, <xref:System.String.StartsWith%2A?displayProperty=nameWithType> and <xref:System.String.EndsWith%2A?displayProperty=nameWithType> methods search a string for specific text.</span></span> <span data-ttu-id="84ba2-112">Aşağıdaki örnek, her biri bu yöntemleri ve büyük küçük harfe duyarlı arama kullanan bir değişim gösterir:</span><span class="sxs-lookup"><span data-stu-id="84ba2-112">The following example shows each of these methods and a variation that uses a case insensitive search:</span></span>

[!code-csharp-interactive[search strings using methods](../../../samples/snippets/csharp/how-to/strings/SearchStrings.cs#1)]

<span data-ttu-id="84ba2-113">Önceki örnekte, bu yöntemleri kullanarak için önemli olan bir nokta gösterir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-113">The preceding example demonstrates an important point for using these methods.</span></span> <span data-ttu-id="84ba2-114">Aramalar **büyük küçük harfe duyarlı** varsayılan olarak.</span><span class="sxs-lookup"><span data-stu-id="84ba2-114">Searches are **case-sensitive** by default.</span></span> <span data-ttu-id="84ba2-115">Kullandığınız <xref:System.StringComparison.CurrentCultureIgnoreCase?displayProperty=nameWithType> enum değeri büyük küçük harfe duyarlı arama belirtin.</span><span class="sxs-lookup"><span data-stu-id="84ba2-115">You use the <xref:System.StringComparison.CurrentCultureIgnoreCase?displayProperty=nameWithType> enum value to specify a case insensitive search.</span></span>

## <a name="where-does-the-sought-text-occur-in-a-string"></a><span data-ttu-id="84ba2-116">Aranan metin dizesi içinde gerçekleştiği?</span><span class="sxs-lookup"><span data-stu-id="84ba2-116">Where does the sought text occur in a string?</span></span>

<span data-ttu-id="84ba2-117"><xref:System.String.IndexOf%2A> Ve <xref:System.String.LastIndexOf%2A> yöntemleri de arama metni dizelerinde için.</span><span class="sxs-lookup"><span data-stu-id="84ba2-117">The <xref:System.String.IndexOf%2A> and <xref:System.String.LastIndexOf%2A> methods also search for text in strings.</span></span> <span data-ttu-id="84ba2-118">Bu yöntemler Aranan metin konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="84ba2-118">These methods return the location of the text being sought.</span></span> <span data-ttu-id="84ba2-119">Döndürmeleri metin varsa bulunamadıysa, `-1`.</span><span class="sxs-lookup"><span data-stu-id="84ba2-119">If the text isn't found, they return `-1`.</span></span> <span data-ttu-id="84ba2-120">Aşağıdaki örnekte "yöntemleri" sözcüğü ilk ve son geçtiği için bir arama gösterir ve metin arasında görüntüler.</span><span class="sxs-lookup"><span data-stu-id="84ba2-120">The following example shows a search for the first and last occurrence of the word "methods" and displays the text in between.</span></span>
  
[!code-csharp-interactive[search strings for indices](../../../samples/snippets/csharp/how-to/strings/SearchStrings.cs#2)]

## <a name="finding-specific-text-using-regular-expressions"></a><span data-ttu-id="84ba2-121">Normal ifadeler kullanarak belirli bir metin bulma</span><span class="sxs-lookup"><span data-stu-id="84ba2-121">Finding specific text using regular expressions</span></span>

<span data-ttu-id="84ba2-122"><xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType> Sınıfı, dizeleri aramak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-122">The <xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType> class can be used to search strings.</span></span> <span data-ttu-id="84ba2-123">Bu aramalar basit karmaşıklığı karmaşık metin kalıplarını için değişebilir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-123">These searches can range in complexity from simple to complicated text patterns.</span></span>

<span data-ttu-id="84ba2-124">Aşağıdaki kod örneğinde "" veya bir tümcedeki durumu yok "," sözcüğü arar.</span><span class="sxs-lookup"><span data-stu-id="84ba2-124">The following code example searches for the word "the" or "their" in a sentence, ignoring case.</span></span> <span data-ttu-id="84ba2-125">Statik yöntemi <xref:System.Text.RegularExpressions.Regex.IsMatch%2A?displayProperty=nameWithType> arama gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-125">The static method <xref:System.Text.RegularExpressions.Regex.IsMatch%2A?displayProperty=nameWithType> performs the search.</span></span> <span data-ttu-id="84ba2-126">Bu dizeyi arama ve arama deseni verin.</span><span class="sxs-lookup"><span data-stu-id="84ba2-126">You give it the string to search and a search pattern.</span></span> <span data-ttu-id="84ba2-127">Bu durumda, üçüncü bağımsız değişken büyük küçük harf duyarsız arama belirtir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-127">In this case, a third argument specifies case-insensitive search.</span></span> <span data-ttu-id="84ba2-128">Daha fazla bilgi için bkz. <xref:System.Text.RegularExpressions.RegexOptions?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="84ba2-128">For more information, see <xref:System.Text.RegularExpressions.RegexOptions?displayProperty=nameWithType>.</span></span>  

<span data-ttu-id="84ba2-129">Arama deseni arama metni tanımlar.</span><span class="sxs-lookup"><span data-stu-id="84ba2-129">The search pattern describes the text you search for.</span></span> <span data-ttu-id="84ba2-130">Aşağıdaki tabloda her öğeye arama deseni açıklar.</span><span class="sxs-lookup"><span data-stu-id="84ba2-130">The following table describes each element of the search pattern.</span></span> <span data-ttu-id="84ba2-131">(Aşağıdaki tabloda tek kullanan `\` hangi konulmalıdır olarak `\\` C# dizesinde).</span><span class="sxs-lookup"><span data-stu-id="84ba2-131">(The table below uses the single `\` which must be escaped as `\\` in a C# string).</span></span>

| <span data-ttu-id="84ba2-132">deseni</span><span class="sxs-lookup"><span data-stu-id="84ba2-132">pattern</span></span>  | <span data-ttu-id="84ba2-133">Açıklama</span><span class="sxs-lookup"><span data-stu-id="84ba2-133">Meaning</span></span>     |
| -------- |-------------|
| <span data-ttu-id="84ba2-134">,</span><span class="sxs-lookup"><span data-stu-id="84ba2-134">the</span></span>      | <span data-ttu-id="84ba2-135">metinle eşleşen ""</span><span class="sxs-lookup"><span data-stu-id="84ba2-135">match the text "the"</span></span> |
| <span data-ttu-id="84ba2-136">(EIR)?</span><span class="sxs-lookup"><span data-stu-id="84ba2-136">(eir)?</span></span>   | <span data-ttu-id="84ba2-137">0 veya 1 geçişi "EIR" ile eşleşmesi</span><span class="sxs-lookup"><span data-stu-id="84ba2-137">match 0 or 1 occurence of "eir"</span></span> |
| <span data-ttu-id="84ba2-138">\s</span><span class="sxs-lookup"><span data-stu-id="84ba2-138">\s</span></span>       | <span data-ttu-id="84ba2-139">boşluk karakteri eşleştirmek</span><span class="sxs-lookup"><span data-stu-id="84ba2-139">match a whitespace character</span></span>    |
  
[!code-csharp-interactive[Search using regular expressions](../../../samples/snippets/csharp/how-to/strings/SearchStrings.cs#3)]
  
> [!TIP]
> <span data-ttu-id="84ba2-140">`string` Yöntemleridir genellikle daha iyi seçimler tam bir dize ararken.</span><span class="sxs-lookup"><span data-stu-id="84ba2-140">The `string` methods are usually better choices when you are searching for an exact string.</span></span> <span data-ttu-id="84ba2-141">Normal ifadeler daha iyi bir kaynak dizesi bazı düzeni için ne zaman aradığınız var.</span><span class="sxs-lookup"><span data-stu-id="84ba2-141">Regular expressions are better when you are searching for some pattern is a source string.</span></span>

## <a name="does-a-string-follow-a-pattern"></a><span data-ttu-id="84ba2-142">Bir dizeyi bir desenle takip ediyor mu?</span><span class="sxs-lookup"><span data-stu-id="84ba2-142">Does a string follow a pattern?</span></span>

<span data-ttu-id="84ba2-143">Aşağıdaki kod, bir dizideki her dizesinin biçimi doğrulamak için normal ifadeler kullanır.</span><span class="sxs-lookup"><span data-stu-id="84ba2-143">The following code uses regular expressions to validate the format of each string in an array.</span></span> <span data-ttu-id="84ba2-144">Doğrulama her dize basamak üç grup çizgilerle ayrılır bir telefon numarası form sahip olmasını gerektirir, ilk iki grupları üç rakam ve dört basamak üçüncü grubunu içerir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-144">The validation requires that each string have the form of a telephone number in which three groups of digits are separated by dashes, the first two groups contain three digits, and the third group contains four digits.</span></span> <span data-ttu-id="84ba2-145">Normal ifade arama deseni kullanır `^\\d{3}-\\d{3}-\\d{4}$`.</span><span class="sxs-lookup"><span data-stu-id="84ba2-145">The search pattern uses the regular expression `^\\d{3}-\\d{3}-\\d{4}$`.</span></span> <span data-ttu-id="84ba2-146">Daha fazla bilgi için bkz: [normal ifade dili - hızlı başvuru](../../standard/base-types/regular-expression-language-quick-reference.md).</span><span class="sxs-lookup"><span data-stu-id="84ba2-146">For more information, see [Regular Expression Language - Quick Reference](../../standard/base-types/regular-expression-language-quick-reference.md).</span></span>

| <span data-ttu-id="84ba2-147">deseni</span><span class="sxs-lookup"><span data-stu-id="84ba2-147">pattern</span></span>  | <span data-ttu-id="84ba2-148">Açıklama</span><span class="sxs-lookup"><span data-stu-id="84ba2-148">Meaning</span></span>                             |
| -------- |-------------------------------------|
| ^        | <span data-ttu-id="84ba2-149">Dize başlangıcı ile eşleşir</span><span class="sxs-lookup"><span data-stu-id="84ba2-149">matches the beginning of the string</span></span> |
| <span data-ttu-id="84ba2-150">\d{3}</span><span class="sxs-lookup"><span data-stu-id="84ba2-150">\d{3}</span></span>    | <span data-ttu-id="84ba2-151">tam olarak 3 basamak karakterle eşleşir</span><span class="sxs-lookup"><span data-stu-id="84ba2-151">matches exactly 3 digit characters</span></span>  |
| -        | <span data-ttu-id="84ba2-152">eşleşen '-' karakteri</span><span class="sxs-lookup"><span data-stu-id="84ba2-152">matches the '-' character</span></span>           |
| <span data-ttu-id="84ba2-153">\d{3}</span><span class="sxs-lookup"><span data-stu-id="84ba2-153">\d{3}</span></span>    | <span data-ttu-id="84ba2-154">tam olarak 3 basamak karakterle eşleşir</span><span class="sxs-lookup"><span data-stu-id="84ba2-154">matches exactly 3 digit characters</span></span>  |
| -        | <span data-ttu-id="84ba2-155">eşleşen '-' karakteri</span><span class="sxs-lookup"><span data-stu-id="84ba2-155">matches the '-' character</span></span>           |
| <span data-ttu-id="84ba2-156">\d{4}</span><span class="sxs-lookup"><span data-stu-id="84ba2-156">\d{4}</span></span>    | <span data-ttu-id="84ba2-157">tam olarak 4 basamaklı karakterle eşleşir</span><span class="sxs-lookup"><span data-stu-id="84ba2-157">matches exactly 4 digit characters</span></span>  |
| $        | <span data-ttu-id="84ba2-158">Dize sonu ile eşleşir</span><span class="sxs-lookup"><span data-stu-id="84ba2-158">matches the end of the string</span></span>       |


[!code-csharp-interactive[csProgGuideStrings#4](../../../samples/snippets/csharp/how-to/strings/SearchStrings.cs#4)]

<span data-ttu-id="84ba2-159">Bu tek arama deseni birçok geçerli dizeler eşleştirir.</span><span class="sxs-lookup"><span data-stu-id="84ba2-159">This single search pattern matches many valid strings.</span></span> <span data-ttu-id="84ba2-160">Normal ifadeler için arama yapın ya da tek bir metin dizesi yerine bir desen karşı doğrulamak daha uygundur.</span><span class="sxs-lookup"><span data-stu-id="84ba2-160">Regular expressions are better to search for or validate against a pattern, rather than a single text string.</span></span>

<span data-ttu-id="84ba2-161">Kodda bakarak bu örnekleri deneyebilirsiniz bizim [GitHub deposunu](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings).</span><span class="sxs-lookup"><span data-stu-id="84ba2-161">You can try these samples by looking at the code in our [GitHub repository](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings).</span></span> <span data-ttu-id="84ba2-162">Veya örnekleri indirebilirsiniz [zip dosyası olarak](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings.zip).</span><span class="sxs-lookup"><span data-stu-id="84ba2-162">Or you can download the samples [as a zip file](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/how-to/strings.zip).</span></span>

## <a name="see-also"></a><span data-ttu-id="84ba2-163">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="84ba2-163">See Also</span></span>  

 [<span data-ttu-id="84ba2-164">C# Programlama Kılavuzu</span><span class="sxs-lookup"><span data-stu-id="84ba2-164">C# Programming Guide</span></span>](../programming-guide/index.md)  
 [<span data-ttu-id="84ba2-165">Dizeler</span><span class="sxs-lookup"><span data-stu-id="84ba2-165">Strings</span></span>](../programming-guide/strings/index.md)  
 <span data-ttu-id="84ba2-166">[LINQ ve dizeler](../programming-guide/concepts/linq/linq-and-strings.md) </span><span class="sxs-lookup"><span data-stu-id="84ba2-166">[LINQ and Strings](../programming-guide/concepts/linq/linq-and-strings.md) </span></span>  
 <span data-ttu-id="84ba2-167"><xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="84ba2-167"><xref:System.Text.RegularExpressions.Regex?displayProperty=nameWithType></span></span>     
 <span data-ttu-id="84ba2-168">[.NET framework normal ifadeleri](../../standard/base-types/regular-expressions.md) </span><span class="sxs-lookup"><span data-stu-id="84ba2-168">[.NET Framework Regular Expressions](../../standard/base-types/regular-expressions.md) </span></span>  
 <span data-ttu-id="84ba2-169">[Normal ifade dili - hızlı başvuru](../../standard/base-types/regular-expression-language-quick-reference.md) </span><span class="sxs-lookup"><span data-stu-id="84ba2-169">[Regular Expression Language - Quick Reference](../../standard/base-types/regular-expression-language-quick-reference.md) </span></span>  
 [<span data-ttu-id="84ba2-170">.NET dizeleri kullanmak için en iyi uygulamalar</span><span class="sxs-lookup"><span data-stu-id="84ba2-170">Best practices for using strings in .NET</span></span>](../../standard/base-types/best-practices-strings.md)  