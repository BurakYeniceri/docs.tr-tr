---
title: "Nasıl yapılır: Dizelerin Geçerli E-Posta Biçiminde Olduğunu Doğrulama"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- regular expressions, examples
- user input, examples
- Regex.IsMatch method
- regular expressions [.NET Framework], examples
- examples [Visual Basic], strings
- IsValidEmail
- validation, e-mail strings
- input, checking
- strings [.NET Framework], examples [Visual Basic]
- e-mail [.NET Framework], validating
- IsMatch method
ms.assetid: 7536af08-4e86-4953-98a1-a8298623df92
caps.latest.revision: "30"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 03623cc4086981dc321aafe3020dcd571b74d9bc
ms.sourcegitcommit: 9c4b8d457ffb8d134c9d55c6d7682a0f22e2b9a8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2017
---
# <a name="how-to-verify-that-strings-are-in-valid-email-format"></a><span data-ttu-id="6527c-102">Nasıl yapılır: Dizelerin Geçerli E-Posta Biçiminde Olduğunu Doğrulama</span><span class="sxs-lookup"><span data-stu-id="6527c-102">How to: Verify that Strings Are in Valid Email Format</span></span>
<span data-ttu-id="6527c-103">Aşağıdaki örnek, bir dize geçerli e-posta biçiminde olduğunu doğrulamak için normal bir ifade kullanır.</span><span class="sxs-lookup"><span data-stu-id="6527c-103">The following example uses a regular expression to verify that a string is in valid email format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6527c-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="6527c-104">Example</span></span>  
 <span data-ttu-id="6527c-105">Örnek tanımlayan bir `IsValidEmail` döndürür yöntemi `true` dizesi geçerli bir eposta adresi içeriyorsa ve `false` desteklemez ancak başka bir eylemi alır.</span><span class="sxs-lookup"><span data-stu-id="6527c-105">The example defines an `IsValidEmail` method, which returns `true` if the string contains a valid email address and `false` if it does not, but takes no other action.</span></span>  
  
 <span data-ttu-id="6527c-106">E-posta adresi geçerli olduğunu doğrulamak için `IsValidEmail` yöntem çağrılarını <xref:System.Text.RegularExpressions.Regex.Replace%28System.String%2CSystem.String%2CSystem.Text.RegularExpressions.MatchEvaluator%29?displayProperty=nameWithType> yöntemiyle `(@)(.+)$` etki alanı adı e-posta adresinden ayırmak için normal ifade deseni.</span><span class="sxs-lookup"><span data-stu-id="6527c-106">To verify that the email address is valid, the `IsValidEmail` method calls the <xref:System.Text.RegularExpressions.Regex.Replace%28System.String%2CSystem.String%2CSystem.Text.RegularExpressions.MatchEvaluator%29?displayProperty=nameWithType> method with the `(@)(.+)$` regular expression pattern to separate the domain name from the email address.</span></span> <span data-ttu-id="6527c-107">Üçüncü parametre bir <xref:System.Text.RegularExpressions.MatchEvaluator> işler ve eşleşen metni değiştirir yöntemi temsil eden temsilci.</span><span class="sxs-lookup"><span data-stu-id="6527c-107">The third parameter is a <xref:System.Text.RegularExpressions.MatchEvaluator> delegate that represents the method that processes and replaces the matched text.</span></span> <span data-ttu-id="6527c-108">Normal ifade deseni şu şekilde yorumlanır.</span><span class="sxs-lookup"><span data-stu-id="6527c-108">The regular expression pattern is interpreted as follows.</span></span>  
  
|<span data-ttu-id="6527c-109">Desen</span><span class="sxs-lookup"><span data-stu-id="6527c-109">Pattern</span></span>|<span data-ttu-id="6527c-110">Açıklama</span><span class="sxs-lookup"><span data-stu-id="6527c-110">Description</span></span>|  
|-------------|-----------------|  
|`(@)`|<span data-ttu-id="6527c-111">Eşleşme @ karakteri.</span><span class="sxs-lookup"><span data-stu-id="6527c-111">Match the @ character.</span></span> <span data-ttu-id="6527c-112">Bu ilk yakalama grubudur.</span><span class="sxs-lookup"><span data-stu-id="6527c-112">This is the first capturing group.</span></span>|  
|`(.+)`|<span data-ttu-id="6527c-113">Herhangi bir karakterin bir veya birden çok tekrarı eşleşir.</span><span class="sxs-lookup"><span data-stu-id="6527c-113">Match one or more occurrences of any character.</span></span> <span data-ttu-id="6527c-114">Bu ikinci yakalama grubudur.</span><span class="sxs-lookup"><span data-stu-id="6527c-114">This is the second capturing group.</span></span>|  
|`$`|<span data-ttu-id="6527c-115">Son dizenin sonunda eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="6527c-115">End the match at the end of the string.</span></span>|  
  
 <span data-ttu-id="6527c-116">Etki alanı adı ile birlikte @ karakteri geçirilir `DomainMapper` kullanan yöntemi <xref:System.Globalization.IdnMapping> sınıfı Punycode US-ASCII karakter aralığı dışında olan Unicode karakterler çevir.</span><span class="sxs-lookup"><span data-stu-id="6527c-116">The domain name along with the @ character is passed to the `DomainMapper` method, which uses the <xref:System.Globalization.IdnMapping> class to translate Unicode characters that are outside the US-ASCII character range to Punycode.</span></span> <span data-ttu-id="6527c-117">Metodu ayrıca ayarlar `invalid` bayrağını `True` varsa <xref:System.Globalization.IdnMapping.GetAscii%2A?displayProperty=nameWithType> yöntemi, etki alanı adı geçersiz karakterler algılar.</span><span class="sxs-lookup"><span data-stu-id="6527c-117">The method also sets the `invalid` flag to `True` if the <xref:System.Globalization.IdnMapping.GetAscii%2A?displayProperty=nameWithType> method detects any invalid characters in the domain name.</span></span> <span data-ttu-id="6527c-118">Zayıf kod etki alanı adı öncesinde tarafından yöntemi döndürür @ simgesi `IsValidEmail` yöntemi.</span><span class="sxs-lookup"><span data-stu-id="6527c-118">The method returns the Punycode domain name preceded by the @ symbol to the `IsValidEmail` method.</span></span>  
  
 <span data-ttu-id="6527c-119">`IsValidEmail` Sonra yöntemi çağırır <xref:System.Text.RegularExpressions.Regex.IsMatch%28System.String%2CSystem.String%29?displayProperty=nameWithType> adresi bir normal ifade deseni uyduğunu doğrulamak için yöntem.</span><span class="sxs-lookup"><span data-stu-id="6527c-119">The `IsValidEmail` method then calls the <xref:System.Text.RegularExpressions.Regex.IsMatch%28System.String%2CSystem.String%29?displayProperty=nameWithType> method to verify that the address conforms to a regular expression pattern.</span></span>  
  
 <span data-ttu-id="6527c-120">Unutmayın `IsValidEmail` yöntemi e-posta adresini doğrulamak için kimlik doğrulaması gerçekleştirmez.</span><span class="sxs-lookup"><span data-stu-id="6527c-120">Note that the `IsValidEmail` method does not perform authentication to validate the email address.</span></span> <span data-ttu-id="6527c-121">Yalnızca kendi biçiminde bir e-posta adresi için geçerli olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="6527c-121">It merely determines whether its format is valid for an email address.</span></span> <span data-ttu-id="6527c-122">Ayrıca, `IsValidEmail` yöntemi en üst düzey etki alanı adı geçerli bir etki alanı adları adresinde listelenmiş olduğunu doğrulamaz [IANA kök bölgesi veritabanı](https://www.iana.org/domains/root/db), bir arama işlemi duyar.</span><span class="sxs-lookup"><span data-stu-id="6527c-122">In addition, the `IsValidEmail` method does not verify that the top-level domain name is a valid domain name listed at the [IANA Root Zone Database](https://www.iana.org/domains/root/db), which would require a look-up operation.</span></span> <span data-ttu-id="6527c-123">Bunun yerine, normal ifade yalnızca üst düzey etki alanı adı ve yirmi dört iki ASCII karakterler, alfasayısal ilk ve son karakterler ve geriye kalan karakterler alfasayısal veya tire ile arasında oluşan olduğunu doğrular (-).</span><span class="sxs-lookup"><span data-stu-id="6527c-123">Instead, the regular expression merely verifies that the top-level domain name consists of between two and twenty-four ASCII characters, with alphanumeric first and last characters and the remaining characters being either alphanumeric or a hyphen (-).</span></span>  
  
 [!code-csharp[RegularExpressions.Examples.Email#7](../../../samples/snippets/csharp/VS_Snippets_CLR/RegularExpressions.Examples.Email/cs/example4.cs#7)]
 [!code-vb[RegularExpressions.Examples.Email#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR/RegularExpressions.Examples.Email/vb/example4.vb#7)]  
  
 <span data-ttu-id="6527c-124">Bu örnekte, normal ifade deseni ``^(?(")(".+?(?<!\\)"@)|(([0-9a-z]((\.(?!\.))|[-!#\$%&'\*\+/=\?\^`{}|~\w])*)(?<=[0-9a-z])@))(?([)([(\d{1,3}.){3}\d{1,3}])|(([0-9a-z][-0-9a-z]*[0-9a-z]*.)+[a-z0-9][-a-z0-9]{0,22}[a-z0-9]))$`\` aşağıdaki tabloda gösterildiği gibi yorumlanır.</span><span class="sxs-lookup"><span data-stu-id="6527c-124">In this example, the regular expression pattern ``^(?(")(".+?(?<!\\)"@)|(([0-9a-z]((\.(?!\.))|[-!#\$%&'\*\+/=\?\^`{}|~\w])*)(?<=[0-9a-z])@))(?([)([(\d{1,3}.){3}\d{1,3}])|(([0-9a-z][-0-9a-z]*[0-9a-z]*.)+[a-z0-9][-a-z0-9]{0,22}[a-z0-9]))$`\` is interpreted as shown in the following table.</span></span> <span data-ttu-id="6527c-125">Normal ifade kullanarak derlenir Not <xref:System.Text.RegularExpressions.RegexOptions.IgnoreCase?displayProperty=nameWithType> bayrağı.</span><span class="sxs-lookup"><span data-stu-id="6527c-125">Note that the regular expression is compiled using the <xref:System.Text.RegularExpressions.RegexOptions.IgnoreCase?displayProperty=nameWithType> flag.</span></span>  
  
|<span data-ttu-id="6527c-126">Desen</span><span class="sxs-lookup"><span data-stu-id="6527c-126">Pattern</span></span>|<span data-ttu-id="6527c-127">Açıklama</span><span class="sxs-lookup"><span data-stu-id="6527c-127">Description</span></span>|  
|-------------|-----------------|  
|`^`|<span data-ttu-id="6527c-128">Eşleşme dizenin başında başlar.</span><span class="sxs-lookup"><span data-stu-id="6527c-128">Begin the match at the start of the string.</span></span>|  
|`(?(")`|<span data-ttu-id="6527c-129">İlk karakteri bir tırnak işareti olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="6527c-129">Determine whether the first character is a quotation mark.</span></span> <span data-ttu-id="6527c-130">`(?(")`bir değişim yapısıyla başlangıcıdır.</span><span class="sxs-lookup"><span data-stu-id="6527c-130">`(?(")` is the beginning of an alternation construct.</span></span>|  
|`(?("")("".+?(?<!\\)""@)`|<span data-ttu-id="6527c-131">İlk karakteri bir tırnak işareti ise, en az bir oluşumu bir bitiş tırnak işareti herhangi bir karakterin ardından bir başlangıç tırnağından eşleşmesi.</span><span class="sxs-lookup"><span data-stu-id="6527c-131">If the first character is a quotation mark, match a beginning quotation mark followed by at least one occurrence of any character, followed by an ending quotation mark.</span></span> <span data-ttu-id="6527c-132">Bitiş tırnağından ters eğik çizgi karakteriyle gelmemelidir (\\).</span><span class="sxs-lookup"><span data-stu-id="6527c-132">The ending quotation mark must not be preceded by a backslash character (\\).</span></span> <span data-ttu-id="6527c-133">`(?<!`Sıfır Genişlik negatif geriye ilerleme onaylama başlangıcıdır.</span><span class="sxs-lookup"><span data-stu-id="6527c-133">`(?<!` is the beginning of a zero-width negative lookbehind assertion.</span></span> <span data-ttu-id="6527c-134">Dize duymanıza neden bir at işareti (@).</span><span class="sxs-lookup"><span data-stu-id="6527c-134">The string should conclude with an at sign (@).</span></span>|  
|`&#124;(([0-9a-z]`|<span data-ttu-id="6527c-135">İlk karakteri bir tırnak işareti yoksa, alfasayısal bir karakter gelen eşleşen bir-z veya A-Z (karşılaştırma büyük/küçük harfe duyarsız) veya sayısal bir karakterle 0 ile 9 arasında.</span><span class="sxs-lookup"><span data-stu-id="6527c-135">If the first character is not a quotation mark, match any alphabetic character from a to z or A to Z (the comparison is case insensitive), or any numeric character from 0 to 9.</span></span>|  
|`(\.(?!\.))`|<span data-ttu-id="6527c-136">Sonraki karakteri bir nokta ise, aynı.</span><span class="sxs-lookup"><span data-stu-id="6527c-136">If the next character is a period, match it.</span></span> <span data-ttu-id="6527c-137">Bir süre değilse, devam sonraki karaktere bakın ve eşleşme devam edin.</span><span class="sxs-lookup"><span data-stu-id="6527c-137">If it is not a period, look ahead to the next character and continue the match.</span></span> <span data-ttu-id="6527c-138">`(?!\.)`bir e-posta adresi yerel bölümünde görünmesini art arda iki nokta engelleyen bir sıfır Genişlik negatif ileri yönlü onayı ifade eder.</span><span class="sxs-lookup"><span data-stu-id="6527c-138">`(?!\.)` is a zero-width negative lookahead assertion that prevents two consecutive periods from appearing in the local part of an email address.</span></span>|  
|``&#124;[-!#\$%&'\*\+/=\?\^`{}\&#124;~\w]``|<span data-ttu-id="6527c-139">Sonraki karakteri bir süre değilse, herhangi bir sözcük karakteri veya şu karakterlerden birini eşleşen:-! #$%'*+=?^'{} &#124; ~.</span><span class="sxs-lookup"><span data-stu-id="6527c-139">If the next character is not a period, match any word character or one of the following characters: -!#$%'*+=?^\`{}&#124;~.</span></span>|  
|``((\.(?!\.))&#124;[-!#\$%'\*\+/=\?\^`{}\&#124;~\w])*``|<span data-ttu-id="6527c-140">(Süre olmayan veya karakter sayısını biri tarafından izlenen bir dönemi) değişim deseni sıfır veya daha çok kez aynı.</span><span class="sxs-lookup"><span data-stu-id="6527c-140">Match the alternation pattern (a period followed by a non-period, or one of a number of characters) zero or more times.</span></span>|  
|`@`|<span data-ttu-id="6527c-141">Eşleşme @ karakteri.</span><span class="sxs-lookup"><span data-stu-id="6527c-141">Match the @ character.</span></span>|  
|`(?<=[0-9a-z])`|<span data-ttu-id="6527c-142">Karakter önceyse eşleşme devam A ile Z, A'dan Z'ye veya 0-9 arası karakterdir.</span><span class="sxs-lookup"><span data-stu-id="6527c-142">Continue the match if the character that precedes the @ character is A through Z, a through z, or 0 through 9.</span></span> <span data-ttu-id="6527c-143">`(?<=[0-9a-z])` Yapı Sıfır Genişlik pozitif geriye ilerleme onaylama tanımlar.</span><span class="sxs-lookup"><span data-stu-id="6527c-143">The `(?<=[0-9a-z])` construct defines a zero-width positive lookbehind assertion.</span></span>|  
|`(?(\[)`|<span data-ttu-id="6527c-144">@ İzleyen karakterin ayraç olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="6527c-144">Check whether the character that follows @ is an opening bracket.</span></span>|  
|`(\[(\d{1,3}\.){3}\d{1,3}\])`|<span data-ttu-id="6527c-145">Bir açma ayracı ise, ardından bir IP adresi (virgülle ayrılmış her kümesiyle bir ile üç basamak dört ayarlar) ve bir kapanış ayracı ayraç eşleşmesi.</span><span class="sxs-lookup"><span data-stu-id="6527c-145">If it is an opening bracket, match the opening bracket followed by an IP address (four sets of one to three digits, with each set separated by a period) and a closing bracket.</span></span>|  
|`&#124;(([0-9a-z][-0-9a-z]*[0-9a-z]*\.)+`|<span data-ttu-id="6527c-146">@ İzleyen karakterin eşleşen bir alfasayısal karakter, A-z, bir değerle bir açılış ayracı değilse, a-z veya 0-9, bir tire sıfır veya daha çok tekrarı tarafından izlenen ve ardından sıfır veya bir alfasayısal bir karakterle değeri, A-Z, a-z veya 0-9 , ardından bir noktayla.</span><span class="sxs-lookup"><span data-stu-id="6527c-146">If the character that follows @ is not an opening bracket, match one alphanumeric character with a value of A-Z, a-z, or 0-9, followed by zero or more occurrences of a hyphen, followed by zero or one alphanumeric character with a value of A-Z, a-z, or 0-9, followed by a period.</span></span> <span data-ttu-id="6527c-147">Bu desen bir veya daha çok sayıda Tekrarlanmış ve ardından üst düzey etki alanı adı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6527c-147">This pattern can be repeated one or more times, and must be followed by the top-level domain name.</span></span>|  
|`[a-z0-9][\-a-z0-9]{0,22}[a-z0-9]))`|<span data-ttu-id="6527c-148">Üst düzey etki alanı ad başlamalı ve bitmelidir alfasayısal bir karakterle (a-z, A-Z ve 0-9).</span><span class="sxs-lookup"><span data-stu-id="6527c-148">The top-level domain name must begin and end with an alphanumeric character (a-z, A-Z, and 0-9).</span></span> <span data-ttu-id="6527c-149">Ayrıca sıfır ya da olan 22 ASCII karakterleri içerebilir alfasayısal veya kısa çizgi.</span><span class="sxs-lookup"><span data-stu-id="6527c-149">It can also include from zero to 22 ASCII characters that are either alphanumeric or hyphens.</span></span>|  
|`$`|<span data-ttu-id="6527c-150">Son dizenin sonunda eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="6527c-150">End the match at the end of the string.</span></span>|  
  
> [!NOTE]
>  <span data-ttu-id="6527c-151">Kullanabileceğiniz bir e-posta adresini doğrulamak için normal bir ifade kullanmak yerine, <xref:System.Net.Mail.MailAddress?displayProperty=nameWithType> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="6527c-151">Instead of using a regular expression to validate an email address, you can use the <xref:System.Net.Mail.MailAddress?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="6527c-152">Geçişi e-posta adresine bir e-posta adresi geçerli olup olmadığını belirlemek için <xref:System.Net.Mail.MailAddress.%23ctor%28System.String%29?displayProperty=nameWithType> sınıfı oluşturucusu.</span><span class="sxs-lookup"><span data-stu-id="6527c-152">To determine whether an email address is valid, pass the email address to the <xref:System.Net.Mail.MailAddress.%23ctor%28System.String%29?displayProperty=nameWithType> class constructor.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="6527c-153">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="6527c-153">Compiling the Code</span></span>  
 <span data-ttu-id="6527c-154">`IsValidEmail` Ve `DomainMapper` yöntemleri normal ifade yardımcı program yöntemleri kitaplıkta dahil edilebilir ya da bunlar özel statik veya örnek uygulama sınıfı yöntemleri olarak dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="6527c-154">The `IsValidEmail` and `DomainMapper` methods can be included in a library of regular expression utility methods, or they can be included as private static or instance methods in the application class.</span></span>  
  
 <span data-ttu-id="6527c-155">Normal ifade kitaplığa eklemek için ya da kopyalayın ve Visual Studio sınıf kitaplığı projeye kodu yapıştırın veya kopyalayıp bir metin dosyasına yapıştırın ve aşağıdaki gibi bir komutla komut satırından derleme (varsayılarak kaynak kodunun adı  RegexUtilities.cs veya RegexUtilities.vb dosyadır:</span><span class="sxs-lookup"><span data-stu-id="6527c-155">To include them in a regular expression library, either copy and paste the code into a Visual Studio Class Library project, or copy and paste it into a text file and compile it from the command line with a command like the following (assuming that the name of the source code file is RegexUtilities.cs or RegexUtilities.vb:</span></span>  
  
```csharp  
csc /t:library RegexUtilities.cs  
```  
  
```vb  
vbc /t:library RegexUtilities.vb  
```  
  
 <span data-ttu-id="6527c-156">Aynı zamanda <xref:System.Text.RegularExpressions.Regex.CompileToAssembly%2A?displayProperty=nameWithType> yöntemi bir normal ifade kitaplığa normal ifade.</span><span class="sxs-lookup"><span data-stu-id="6527c-156">You can also use the <xref:System.Text.RegularExpressions.Regex.CompileToAssembly%2A?displayProperty=nameWithType> method to include this regular expression in a regular expression library.</span></span>  
  
 <span data-ttu-id="6527c-157">Bunlar bir normal ifade kitaplığında kullanılıyorsa, aşağıdaki gibi kod çağırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6527c-157">If they are used in a regular expression library, you can call them by using code such as the following:</span></span>  
  
 [!code-csharp[RegularExpressions.Examples.Email#8](../../../samples/snippets/csharp/VS_Snippets_CLR/RegularExpressions.Examples.Email/cs/example4.cs#8)]
 [!code-vb[RegularExpressions.Examples.Email#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/RegularExpressions.Examples.Email/vb/example4.vb#8)]  
  
 <span data-ttu-id="6527c-158">E-posta doğrulama normal ifade içeren RegexUtilities.dll adlı bir sınıf kitaplığı oluşturduğunuz varsayıldığında, bu örnekte, aşağıdaki iki yoldan biriyle hazırlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6527c-158">Assuming you've created a class library named RegexUtilities.dll that includes your email validation regular expression, you can compile this example in either of the following ways:</span></span>  
  
-   <span data-ttu-id="6527c-159">Görsel bir konsol uygulaması oluşturma ve projenize RegexUtilities.dll bir başvuru ekleyerek Studio'da.</span><span class="sxs-lookup"><span data-stu-id="6527c-159">In Visual Studio, by creating a Console Application and adding a reference to RegexUtilities.dll to your project.</span></span>  
  
-   <span data-ttu-id="6527c-160">Komut satırından kopyalayarak ve kaynak kodunu metin dosyasında kopyalayıp yapıştırarak ve aşağıdaki gibi bir komutu ile derleme (kaynak kodu dosyasının adını Example.cs veya Example.vb olduğu varsayılarak:</span><span class="sxs-lookup"><span data-stu-id="6527c-160">From the command line, by copying and pasting the source code into a text file and compiling it with a command like the following (assuming that the name of the source code file is Example.cs or Example.vb:</span></span>  
  
    ```csharp  
    csc Example.cs /r:RegexUtilities.dll  
    ```  
  
    ```vb  
    vbc Example.vb /r:RegexUtilities.dll  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="6527c-161">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="6527c-161">See Also</span></span>  
 [<span data-ttu-id="6527c-162">.NET framework normal ifadeleri</span><span class="sxs-lookup"><span data-stu-id="6527c-162">.NET Framework Regular Expressions</span></span>](../../../docs/standard/base-types/regular-expressions.md)