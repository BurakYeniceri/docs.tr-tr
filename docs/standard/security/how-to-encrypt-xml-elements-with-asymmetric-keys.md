---
title: "Nasıl yapılır: XML Öğelerini Asimetrik Anahtarlarla Şifreleme"
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
- cryptography [.NET Framework], asymmetric keys
- AES algorithm
- System.Security.Cryptography.RSACryptoServiceProvider class
- asymmetric keys [.NET Framework]
- System.Security.Cryptography.EncryptedXml class
- XML encryption
- key containers
- Advanced Encryption Standard algorithm
- Rijndael
- encryption [.NET Framework], asymmetric keys
ms.assetid: a164ba4f-e596-4bbe-a9ca-f214fe89ed48
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: bd8b63ab02527f66d30251f21a63e19ce4da50ed
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-encrypt-xml-elements-with-asymmetric-keys"></a><span data-ttu-id="619dc-102">Nasıl yapılır: XML Öğelerini Asimetrik Anahtarlarla Şifreleme</span><span class="sxs-lookup"><span data-stu-id="619dc-102">How to: Encrypt XML Elements with Asymmetric Keys</span></span>
<span data-ttu-id="619dc-103">Sınıflarda kullanabilirsiniz <xref:System.Security.Cryptography.Xml> bir XML belgesi içindeki bir öğe şifrelemek için ad alanı.</span><span class="sxs-lookup"><span data-stu-id="619dc-103">You can use the classes in the <xref:System.Security.Cryptography.Xml> namespace to encrypt an element within an XML document.</span></span>  <span data-ttu-id="619dc-104">XML şifrelemesi, exchange veya kolayca okunan veriler hakkında endişelenmeden şifrelenmiş XML verileri depolamak için standart bir yoludur.</span><span class="sxs-lookup"><span data-stu-id="619dc-104">XML Encryption is a standard way to exchange or store encrypted XML data, without worrying about the data being easily read.</span></span>  <span data-ttu-id="619dc-105">XML şifrelemesi için World Wide Web Konsorsiyumu (W3C) belirtimi http://www.w3.org/TR/xmldsig-core/ bulunan standart XML şifreleme hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="619dc-105">For more information about the XML Encryption standard, see the World Wide Web Consortium (W3C) specification for XML Encryption located at http://www.w3.org/TR/xmldsig-core/.</span></span>  
  
 <span data-ttu-id="619dc-106">XML şifrelemesi herhangi bir XML öğesi değiştirin veya ile belge için kullanabileceğiniz bir <`EncryptedData`> şifrelenmiş XML verileri içeren öğe.</span><span class="sxs-lookup"><span data-stu-id="619dc-106">You can use XML Encryption to replace any XML element or document with an <`EncryptedData`> element that contains the encrypted XML data.</span></span>  <span data-ttu-id="619dc-107"><`EncryptedData`> Öğesi anahtarları ve şifreleme sırasında kullanılan işlemler hakkında bilgi içeren alt öğeleri de içerebilir.</span><span class="sxs-lookup"><span data-stu-id="619dc-107">The <`EncryptedData`> element can also contain sub elements that include information about the keys and processes used during encryption.</span></span>  <span data-ttu-id="619dc-108">XML şifrelemesi şifrelenmiş birden çok öğe içeren bir belge ve birden çok kez şifrelenmesi için bir öğe olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="619dc-108">XML Encryption allows a document to contain multiple encrypted elements and allows an element to be encrypted multiple times.</span></span>  <span data-ttu-id="619dc-109">Bu yordamı kod örneğinde nasıl oluşturulacağını gösterir bir <`EncryptedData`> öğesi, daha sonra şifre çözme sırasında kullanabileceğiniz diğer alt öğelerini birlikte.</span><span class="sxs-lookup"><span data-stu-id="619dc-109">The code example in this procedure shows how to create an <`EncryptedData`> element along with several other sub elements that you can use later during decryption.</span></span>  
  
 <span data-ttu-id="619dc-110">Bu örnek iki anahtarlar kullanılarak bir XML öğesi şifreler.</span><span class="sxs-lookup"><span data-stu-id="619dc-110">This example encrypts an XML element using two keys.</span></span>  <span data-ttu-id="619dc-111">Bir RSA ortak/özel anahtar çifti oluşturur ve güvenli bir anahtar kapsayıcısı için anahtar çifti kaydeder.</span><span class="sxs-lookup"><span data-stu-id="619dc-111">It generates an RSA public/private key pair and saves the key pair to a secure key container.</span></span>  <span data-ttu-id="619dc-112">Bu örnek daha sonra Rijndael algoritması olarak da bilinir Gelişmiş Şifreleme Standardı (AES) algoritması kullanılarak ayrı oturum anahtarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="619dc-112">The example then creates a separate session key using the Advanced Encryption Standard (AES) algorithm, also called the Rijndael algorithm.</span></span>  <span data-ttu-id="619dc-113">Örnek XML belgesi şifrelemek için AES oturum anahtarı kullanır ve AES oturum anahtarı şifrelemek için RSA ortak anahtarı kullanır.</span><span class="sxs-lookup"><span data-stu-id="619dc-113">The example uses the AES session key to encrypt the XML document and then uses the RSA public key to encrypt the AES session key.</span></span>  <span data-ttu-id="619dc-114">Son olarak, örnek şifrelenmiş AES oturum anahtarı ve şifrelenmiş XML verileri XML belgesi içinde yeni bir kaydeder <`EncryptedData`> öğesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-114">Finally, the example saves the encrypted AES session key and the encrypted XML data to the XML document within a new <`EncryptedData`> element.</span></span>  
  
 <span data-ttu-id="619dc-115">XML öğesi şifresini çözmek için anahtar kapsayıcıdan RSA özel anahtarı almak, oturum anahtarının şifresini çözmek için kullanın ve sonra belgenin şifresini çözmek için oturum anahtarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="619dc-115">To decrypt the XML element, you retrieve the RSA private key from the key container, use it to decrypt the session key, and then use the session key to decrypt the document.</span></span>  <span data-ttu-id="619dc-116">Bu yordam kullanılarak şifrelenmiş bir XML öğesi şifresini hakkında daha fazla bilgi için bkz: [nasıl yapılır: XML öğelerini asimetrik anahtarlarla şifresini](../../../docs/standard/security/how-to-decrypt-xml-elements-with-asymmetric-keys.md).</span><span class="sxs-lookup"><span data-stu-id="619dc-116">For more information about how to decrypt an XML element that was encrypted using this procedure, see [How to: Decrypt XML Elements with Asymmetric Keys](../../../docs/standard/security/how-to-decrypt-xml-elements-with-asymmetric-keys.md).</span></span>  
  
 <span data-ttu-id="619dc-117">Bu örnek birden çok uygulama şifrelenmiş verileri paylaşmak gereken yeri veya burada çalıştırdığı zamanları arasında şifrelenmiş verileri kaydetmek bir uygulama gereken durumlar için uygundur.</span><span class="sxs-lookup"><span data-stu-id="619dc-117">This example is appropriate for situations where multiple applications need to share encrypted data or where an application needs to save encrypted data between the times that it runs.</span></span>  
  
### <a name="to-encrypt-an-xml-element-with-an-asymmetric-key"></a><span data-ttu-id="619dc-118">Bir XML öğesi bir asimetrik anahtar şifrelemek için</span><span class="sxs-lookup"><span data-stu-id="619dc-118">To encrypt an XML element with an asymmetric key</span></span>  
  
1.  <span data-ttu-id="619dc-119">Oluşturma bir <xref:System.Security.Cryptography.CspParameters> nesne ve anahtar kapsayıcı adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="619dc-119">Create a <xref:System.Security.Cryptography.CspParameters> object and specify the name of the key container.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#2](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#2)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#2)]  
  
2.  <span data-ttu-id="619dc-120">Bir simetrik anahtar kullanarak Oluştur <xref:System.Security.Cryptography.RSACryptoServiceProvider> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="619dc-120">Generate a symmetric key using the <xref:System.Security.Cryptography.RSACryptoServiceProvider> class.</span></span>  <span data-ttu-id="619dc-121">Geçirdiğiniz zaman anahtar için anahtar kapsayıcısını otomatik olarak kaydedilir <xref:System.Security.Cryptography.CspParameters> oluşturucusunun nesnesine <xref:System.Security.Cryptography.RSACryptoServiceProvider> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="619dc-121">The key is automatically saved to the key container when you pass the <xref:System.Security.Cryptography.CspParameters> object to the constructor of the <xref:System.Security.Cryptography.RSACryptoServiceProvider> class.</span></span>  <span data-ttu-id="619dc-122">Bu anahtar, AES oturum anahtarı şifrelemek için kullanılan ve daha sonra şifresini alınabilir.</span><span class="sxs-lookup"><span data-stu-id="619dc-122">This key will be used to encrypt the AES session key and can be retrieved later to decrypt it.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#3](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#3)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#3)]  
  
3.  <span data-ttu-id="619dc-123">Oluşturma bir <xref:System.Xml.XmlDocument> diskten bir XML dosyası yüklenirken nesne.</span><span class="sxs-lookup"><span data-stu-id="619dc-123">Create an <xref:System.Xml.XmlDocument> object by loading an XML file from disk.</span></span>  <span data-ttu-id="619dc-124"><xref:System.Xml.XmlDocument> Nesne şifrelemek için XML öğesi içerir.</span><span class="sxs-lookup"><span data-stu-id="619dc-124">The <xref:System.Xml.XmlDocument> object contains the XML element to encrypt.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#4](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#4)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#4)]  
  
4.  <span data-ttu-id="619dc-125">Belirtilen öğe Bul <xref:System.Xml.XmlDocument> nesne ve yeni bir <xref:System.Xml.XmlElement> şifrelemek istediğiniz öğeyi temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="619dc-125">Find the specified element in the <xref:System.Xml.XmlDocument> object and create a new <xref:System.Xml.XmlElement> object to represent the element you want to encrypt.</span></span> <span data-ttu-id="619dc-126">Bu örnekte, `"creditcard"` öğesi şifrelenir.</span><span class="sxs-lookup"><span data-stu-id="619dc-126">In this example, the `"creditcard"` element is encrypted.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#5](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#5)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#5)]  
  
5.  <span data-ttu-id="619dc-127">Kullanarak bir yeni bir oturum anahtarı oluşturun <xref:System.Security.Cryptography.RijndaelManaged> sınıfı.</span><span class="sxs-lookup"><span data-stu-id="619dc-127">Create a new session key using the <xref:System.Security.Cryptography.RijndaelManaged> class.</span></span>  <span data-ttu-id="619dc-128">Bu anahtar XML öğesi şifrelemek ve ardından kendisini şifrelenir ve XML belgesinde yerleştirilir.</span><span class="sxs-lookup"><span data-stu-id="619dc-128">This key will encrypt the XML element, and then be encrypted itself and placed in the XML document.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#6](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#6)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#6)]  
  
6.  <span data-ttu-id="619dc-129">Yeni bir örneğini oluşturmak <xref:System.Security.Cryptography.Xml.EncryptedXml> sınıfı ve oturum anahtarı kullanarak belirtilen öğe şifrelemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="619dc-129">Create a new instance of the <xref:System.Security.Cryptography.Xml.EncryptedXml> class and use it to encrypt the specified element using the session key.</span></span>  <span data-ttu-id="619dc-130"><xref:System.Security.Cryptography.Xml.EncryptedXml.EncryptData%2A> Yöntem şifrelenmiş bir bayt dizisi şifrelenmiş öğesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="619dc-130">The <xref:System.Security.Cryptography.Xml.EncryptedXml.EncryptData%2A> method returns the encrypted element as an array of encrypted bytes.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#7](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#7)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#7)]  
  
7.  <span data-ttu-id="619dc-131">Oluşturmak bir <xref:System.Security.Cryptography.Xml.EncryptedData> nesne ve şifrelenmiş XML öğesi URL tanıtıcısı ile doldurur.</span><span class="sxs-lookup"><span data-stu-id="619dc-131">Construct an <xref:System.Security.Cryptography.Xml.EncryptedData> object and populate it with the URL identifier of the encrypted XML element.</span></span>  <span data-ttu-id="619dc-132">Bu URL tanımlayıcı XML şifrelenmiş bir öğe içeriyor bilmeniz şifresi çözme bir taraf sağlar.</span><span class="sxs-lookup"><span data-stu-id="619dc-132">This URL identifier lets a decrypting party know that the XML contains an encrypted element.</span></span>  <span data-ttu-id="619dc-133">Kullanabileceğiniz <xref:System.Security.Cryptography.Xml.EncryptedXml.XmlEncElementUrl> alan URL tanımlayıcısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="619dc-133">You can use the <xref:System.Security.Cryptography.Xml.EncryptedXml.XmlEncElementUrl> field to specify the URL identifier.</span></span>  <span data-ttu-id="619dc-134">Düz metin XML öğesi yerine bir <`EncryptedData`> öğesi tarafından bu kapsüllenmiş <xref:System.Security.Cryptography.Xml.EncryptedData> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-134">The plaintext XML element will be replaced by an <`EncryptedData`> element encapsulated by this <xref:System.Security.Cryptography.Xml.EncryptedData> object.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#8](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#8)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#8)]  
  
8.  <span data-ttu-id="619dc-135">Oluşturma bir <xref:System.Security.Cryptography.Xml.EncryptionMethod> oturum anahtarı oluşturmak için kullanılan şifreleme algoritması URL tanıtıcısı başlatılmamış nesne.</span><span class="sxs-lookup"><span data-stu-id="619dc-135">Create an <xref:System.Security.Cryptography.Xml.EncryptionMethod> object that is initialized to the URL identifier of the cryptographic algorithm used to generate the session key.</span></span>  <span data-ttu-id="619dc-136">Geçirmek <xref:System.Security.Cryptography.Xml.EncryptionMethod> nesnesinin <xref:System.Security.Cryptography.Xml.EncryptedType.EncryptionMethod%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="619dc-136">Pass the <xref:System.Security.Cryptography.Xml.EncryptionMethod> object to the <xref:System.Security.Cryptography.Xml.EncryptedType.EncryptionMethod%2A> property.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#9](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#9)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#9](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#9)]  
  
9. <span data-ttu-id="619dc-137">Oluşturma bir <xref:System.Security.Cryptography.Xml.EncryptedKey> şifreli oturum anahtarı içeren nesne.</span><span class="sxs-lookup"><span data-stu-id="619dc-137">Create an <xref:System.Security.Cryptography.Xml.EncryptedKey> object to contain the encrypted session key.</span></span>  <span data-ttu-id="619dc-138">Oturum anahtarını şifrelemek, ekleyin <xref:System.Security.Cryptography.Xml.EncryptedKey> nesne ve bir oturum anahtarı adı ve anahtar tanımlayıcı URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="619dc-138">Encrypt the session key, add it to the <xref:System.Security.Cryptography.Xml.EncryptedKey> object, and enter a session key name and key identifier URL.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#10](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#10)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#10](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#10)]  
  
10. <span data-ttu-id="619dc-139">Yeni bir <xref:System.Security.Cryptography.Xml.DataReference> belirli oturum anahtarı için şifrelenmiş veriler eşlemeleri nesnesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-139">Create a new <xref:System.Security.Cryptography.Xml.DataReference> object that maps the encrypted data to a particular session key.</span></span>  <span data-ttu-id="619dc-140">Bu isteğe bağlı adım, bir XML belgesi birden fazla bölümü tek bir anahtarla şifrelenmiş kolayca belirtmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="619dc-140">This optional step allows you to easily specify that multiple parts of an XML document were encrypted by a single key.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#11](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#11)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#11](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#11)]  
  
11. <span data-ttu-id="619dc-141">Şifrelenmiş anahtar ekler <xref:System.Security.Cryptography.Xml.EncryptedData> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-141">Add the encrypted key to the <xref:System.Security.Cryptography.Xml.EncryptedData> object.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#12](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#12)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#12](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#12)]  
  
12. <span data-ttu-id="619dc-142">Yeni bir <xref:System.Security.Cryptography.Xml.KeyInfo> nesne RSA anahtar adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="619dc-142">Create a new <xref:System.Security.Cryptography.Xml.KeyInfo> object to specify the name of the RSA key.</span></span>  <span data-ttu-id="619dc-143">Ekleyin <xref:System.Security.Cryptography.Xml.EncryptedData> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-143">Add it to the <xref:System.Security.Cryptography.Xml.EncryptedData> object.</span></span> <span data-ttu-id="619dc-144">Bu, oturum anahtarının şifresini çözme sırasında kullanmak için doğru asimetrik anahtar tanımlamak şifresi çözme taraf yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="619dc-144">This helps the decrypting party identify the correct asymmetric key to use when decrypting the session key.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#13](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#13)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#13](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#13)]  
  
13. <span data-ttu-id="619dc-145">Şifreli öğe verileri eklediğinizde <xref:System.Security.Cryptography.Xml.EncryptedData> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-145">Add the encrypted element data to the <xref:System.Security.Cryptography.Xml.EncryptedData> object.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#14](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#14)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#14](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#14)]  
  
14. <span data-ttu-id="619dc-146">Özgün öğeyi değiştirin <xref:System.Xml.XmlDocument> nesnesi ile <xref:System.Security.Cryptography.Xml.EncryptedData> öğesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-146">Replace the element from the original <xref:System.Xml.XmlDocument> object with the <xref:System.Security.Cryptography.Xml.EncryptedData> element.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#15](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#15)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#15](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#15)]  
  
15. <span data-ttu-id="619dc-147">Kaydet <xref:System.Xml.XmlDocument> nesnesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-147">Save the <xref:System.Xml.XmlDocument> object.</span></span>  
  
     [!code-csharp[HowToEncryptXMLElementAsymmetric#16](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#16)]
     [!code-vb[HowToEncryptXMLElementAsymmetric#16](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#16)]  
  
## <a name="example"></a><span data-ttu-id="619dc-148">Örnek</span><span class="sxs-lookup"><span data-stu-id="619dc-148">Example</span></span>  
 <span data-ttu-id="619dc-149">Bu örnek, bir dosya adlı varsayar `"test.xml"` derlenmiş programın aynı dizinde bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="619dc-149">This example assumes that a file named `"test.xml"` exists in the same directory as the compiled program.</span></span>  <span data-ttu-id="619dc-150">Ayrıca varsayılmaktadır `"test.xml"` içeren bir `"creditcard"` öğesi.</span><span class="sxs-lookup"><span data-stu-id="619dc-150">It also assumes that `"test.xml"` contains a `"creditcard"` element.</span></span>  <span data-ttu-id="619dc-151">Aşağıdaki XML adlı bir dosyaya yerleştirebilirsiniz `test.xml` ve bu örnek ile kullanın.</span><span class="sxs-lookup"><span data-stu-id="619dc-151">You can place the following XML into a file called `test.xml` and use it with this example.</span></span>  
  
```xml  
<root>  
    <creditcard>  
        <number>19834209</number>  
        <expiry>02/02/2002</expiry>  
    </creditcard>  
</root>  
```  
  
 [!code-csharp[HowToEncryptXMLElementAsymmetric#1](../../../samples/snippets/csharp/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/cs/sample.cs#1)]
 [!code-vb[HowToEncryptXMLElementAsymmetric#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/HowToEncryptXMLElementAsymmetric/vb/sample.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="619dc-152">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="619dc-152">Compiling the Code</span></span>  
  
-   <span data-ttu-id="619dc-153">Bu örneği derlemek için bir başvuru eklemeniz gerekir `System.Security.dll`.</span><span class="sxs-lookup"><span data-stu-id="619dc-153">To compile this example, you need to include a reference to `System.Security.dll`.</span></span>  
  
-   <span data-ttu-id="619dc-154">Şu ad alanlarından içerir: <xref:System.Xml>, <xref:System.Security.Cryptography>, ve <xref:System.Security.Cryptography.Xml>.</span><span class="sxs-lookup"><span data-stu-id="619dc-154">Include the following namespaces: <xref:System.Xml>, <xref:System.Security.Cryptography>, and <xref:System.Security.Cryptography.Xml>.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="619dc-155">.NET Framework Güvenliği</span><span class="sxs-lookup"><span data-stu-id="619dc-155">.NET Framework Security</span></span>  
 <span data-ttu-id="619dc-156">Düz metin olarak hiçbir zaman bir simetrik şifreleme anahtarı depolamak veya düz metin olarak makineler arasında bir simetrik anahtar aktarın.</span><span class="sxs-lookup"><span data-stu-id="619dc-156">Never store a symmetric cryptographic key in plaintext or transfer a symmetric key between machines in plaintext.</span></span>  <span data-ttu-id="619dc-157">Buna ek olarak, hiçbir zaman depolamak veya asimetrik anahtar çifti düz metin olarak özel anahtarı aktarın.</span><span class="sxs-lookup"><span data-stu-id="619dc-157">Additionally, never store or transfer the private key of an asymmetric key pair in plaintext.</span></span>  <span data-ttu-id="619dc-158">Simetrik ve asimetrik şifreleme anahtarları hakkında daha fazla bilgi için bkz: [şifreleme ve şifre çözme için anahtarlar oluşturma](../../../docs/standard/security/generating-keys-for-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="619dc-158">For more information about symmetric and asymmetric cryptographic keys, see [Generating Keys for Encryption and Decryption](../../../docs/standard/security/generating-keys-for-encryption-and-decryption.md).</span></span>  
  
 <span data-ttu-id="619dc-159">Hiç kaynak kodunuza doğrudan bir anahtar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="619dc-159">Never embed a key directly into your source code.</span></span>  <span data-ttu-id="619dc-160">Katıştırılmış anahtarları kullanarak bir derlemeye ait kolayca da okunabilir [Ildasm.exe (IL ayrıştırıcı)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md) veya Not Defteri gibi bir metin düzenleyicisinde derleme açarak.</span><span class="sxs-lookup"><span data-stu-id="619dc-160">Embedded keys can be easily read from an assembly using the [Ildasm.exe (IL Disassembler)](../../../docs/framework/tools/ildasm-exe-il-disassembler.md) or by opening the assembly in a text editor such as Notepad.</span></span>  
  
 <span data-ttu-id="619dc-161">İşiniz bittiğinde şifreleme anahtarını kullanarak temizleyin, bellekten her bayt sıfır olarak ayarlayarak veya çağırarak <xref:System.Security.Cryptography.SymmetricAlgorithm.Clear%2A> yönetilen şifreleme sınıfının yöntemi.</span><span class="sxs-lookup"><span data-stu-id="619dc-161">When you are done using a cryptographic key, clear it from memory by setting each byte to zero or by calling the <xref:System.Security.Cryptography.SymmetricAlgorithm.Clear%2A> method of the managed cryptography class.</span></span>  <span data-ttu-id="619dc-162">Şifreleme anahtarları bazen bellekten bir hata ayıklayıcı tarafından okunabilir veya bellek konumuna disk belleği, bir sabit diskten okuma diske.</span><span class="sxs-lookup"><span data-stu-id="619dc-162">Cryptographic keys can sometimes be read from memory by a debugger or read from a hard drive if the memory location is paged to disk.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="619dc-163">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="619dc-163">See Also</span></span>  
 <xref:System.Security.Cryptography.Xml>  
 [<span data-ttu-id="619dc-164">Nasıl yapılır: XML öğelerini asimetrik anahtarlarla şifresini çözme</span><span class="sxs-lookup"><span data-stu-id="619dc-164">How to: Decrypt XML Elements with Asymmetric Keys</span></span>](../../../docs/standard/security/how-to-decrypt-xml-elements-with-asymmetric-keys.md)