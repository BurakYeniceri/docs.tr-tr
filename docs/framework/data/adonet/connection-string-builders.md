---
title: "Bağlantı dizesi oluşturucular"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 8434b608-c4d3-43d3-8ae3-6d8c6b726759
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 836742264e44c4cb13f97a3528177080bd10c364
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="connection-string-builders"></a><span data-ttu-id="f5a4b-102">Bağlantı dizesi oluşturucular</span><span class="sxs-lookup"><span data-stu-id="f5a4b-102">Connection String Builders</span></span>
<span data-ttu-id="f5a4b-103">Önceki sürümlerinde [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)], derleme zamanı değerleri gerçekleşmediği, birleştirilmiş dizeyi içeren bağlantı dizeleri çalışma zamanında, yanlış bir anahtar sözcüğü oluşturulan böylece denetimi bir <xref:System.ArgumentException>.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-103">In earlier versions of [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)], compile-time checking of connection strings with concatenated string values did not occur, so that at run time, an incorrect keyword generated an <xref:System.ArgumentException>.</span></span> <span data-ttu-id="f5a4b-104">Her biri [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] veri sağlayıcıları geçerli bağlantı dizeleri zor el ile yapıldığında oluşturma yapılan bağlantı dizesi anahtar için farklı bir sözdizimi desteklenir.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-104">Each of the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] data providers supported different syntax for connection string keywords, which made constructing valid connection strings difficult if done manually.</span></span> <span data-ttu-id="f5a4b-105">Bu sorunu gidermek için [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)] 2.0 sunulan her yeni bağlantı dizesi oluşturucular [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] veri sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-105">To address this problem, [!INCLUDE[vstecado](../../../../includes/vstecado-md.md)] 2.0 introduced new connection string builders for each [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] data provider.</span></span> <span data-ttu-id="f5a4b-106">Her bir veri sağlayıcısı devralan bir kesin türü belirtilmiş bağlantı dizesi Oluşturucu sınıf içerir <xref:System.Data.Common.DbConnectionStringBuilder>.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-106">Each data provider includes a strongly typed connection string builder class that inherits from <xref:System.Data.Common.DbConnectionStringBuilder>.</span></span> <span data-ttu-id="f5a4b-107">Aşağıdaki tabloda [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] veri sağlayıcıları ve bunların ilişkili bir bağlantı dizesi Oluşturucu sınıfları.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-107">The following table lists the [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] data providers and their associated connection string builder classes.</span></span>  
  
|<span data-ttu-id="f5a4b-108">Sağlayıcı</span><span class="sxs-lookup"><span data-stu-id="f5a4b-108">Provider</span></span>|<span data-ttu-id="f5a4b-109">ConnectionStringBuilder sınıfı</span><span class="sxs-lookup"><span data-stu-id="f5a4b-109">ConnectionStringBuilder class</span></span>|  
|--------------|-----------------------------------|  
|<xref:System.Data.SqlClient>|<xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=nameWithType>|  
|<xref:System.Data.OleDb>|<xref:System.Data.OleDb.OleDbConnectionStringBuilder?displayProperty=nameWithType>|  
|<xref:System.Data.Odbc>|<xref:System.Data.Odbc.OdbcConnectionStringBuilder?displayProperty=nameWithType>|  
|<xref:System.Data.OracleClient>|<xref:System.Data.OracleClient.OracleConnectionStringBuilder?displayProperty=nameWithType>|  
  
## <a name="connection-string-injection-attacks"></a><span data-ttu-id="f5a4b-110">Bağlantı dizesi ekleme saldırıları</span><span class="sxs-lookup"><span data-stu-id="f5a4b-110">Connection String Injection Attacks</span></span>  
 <span data-ttu-id="f5a4b-111">Dinamik dize birleştirme kullanıcı girişini temel alarak bağlantı dizelerini oluşturmak için kullanılan bağlantı dizesi ekleme saldırı ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-111">A connection string injection attack can occur when dynamic string concatenation is used to build connection strings that are based on user input.</span></span> <span data-ttu-id="f5a4b-112">Dize doğrulanmış ve kötü amaçlı metin veya değil kaçış karakterleri değilse, bir saldırganın olası hassas verileri veya sunucudaki diğer kaynakları erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-112">If the string is not validated and malicious text or characters not escaped, an attacker can potentially access sensitive data or other resources on the server.</span></span> <span data-ttu-id="f5a4b-113">Örneğin, bir saldırganın bir noktalı virgül sağladığını ve ek bir değer ekleyerek saldırısı.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-113">For example, an attacker could mount an attack by supplying a semicolon and appending an additional value.</span></span> <span data-ttu-id="f5a4b-114">Bağlantı dizesi "son bir WINS" algoritması kullanılarak ayrıştırılır ve tehlikeli giriş için meşru bir değer geçmesidir.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-114">The connection string is parsed by using a "last one wins" algorithm, and the hostile input is substituted for a legitimate value.</span></span>  
  
 <span data-ttu-id="f5a4b-115">Bağlantı dizesi Oluşturucu sınıfları konusunda güvenilir bilgiler ortadan kaldırmak ve sözdizimi hataları ve güvenlik açıklarına karşı korumak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-115">The connection string builder classes are designed to eliminate guesswork and protect against syntax errors and security vulnerabilities.</span></span> <span data-ttu-id="f5a4b-116">Bunlar, yöntemleri ve her veri sağlayıcısı tarafından izin verilen bilinen anahtar/değer çiftleri karşılık gelen özellikleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-116">They provide methods and properties corresponding to the known key/value pairs permitted by each data provider.</span></span> <span data-ttu-id="f5a4b-117">Her sınıf eş anlamlıları sabit koleksiyonu tutar ve iyi bilinen bir karşılık gelen anahtar ad bir eş anlamlı çevirebilir.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-117">Each class maintains a fixed collection of synonyms and can translate from a synonym to the corresponding well-known key name.</span></span> <span data-ttu-id="f5a4b-118">Denetimler için geçerli bir anahtar/değer çiftleri gerçekleştirilir ve geçersiz bir çiftinin bir özel durum oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-118">Checks are performed for valid key/value pairs and an invalid pair throws an exception.</span></span> <span data-ttu-id="f5a4b-119">Ayrıca, eklenen değerleri güvenli bir şekilde ele alınır.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-119">In addition, injected values are handled in a safe manner.</span></span>  
  
 <span data-ttu-id="f5a4b-120">Aşağıdaki örnekte gösterilmiştir nasıl <xref:System.Data.SqlClient.SqlConnectionStringBuilder> için eklenen ek değer işleme `Initial Catalog` ayarı.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-120">The following example demonstrates how the <xref:System.Data.SqlClient.SqlConnectionStringBuilder> handles an inserted extra value for the `Initial Catalog` setting.</span></span>  
  
```vb  
Dim builder As New System.Data.SqlClient.SqlConnectionStringBuilder  
builder("Data Source") = "(local)"  
builder("Integrated Security") = True  
builder("Initial Catalog") = "AdventureWorks;NewValue=Bad"  
Console.WriteLine(builder.ConnectionString)  
```  
  
```csharp  
System.Data.SqlClient.SqlConnectionStringBuilder builder =  
  new System.Data.SqlClient.SqlConnectionStringBuilder();  
builder["Data Source"] = "(local)";  
builder["integrated Security"] = true;  
builder["Initial Catalog"] = "AdventureWorks;NewValue=Bad";  
Console.WriteLine(builder.ConnectionString);  
```  
  
 <span data-ttu-id="f5a4b-121">Çıkış gösterir <xref:System.Data.SqlClient.SqlConnectionStringBuilder> bu doğru yeni bir anahtar/değer çifti olarak bağlantı dizesine ekleme yerine çift tırnak işaretleri ek değeri kaçış tarafından işlenen.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-121">The output shows that the <xref:System.Data.SqlClient.SqlConnectionStringBuilder> handled this correctly by escaping the extra value in double quotation marks instead of appending it to the connection string as a new key/value pair.</span></span>  
  
```  
data source=(local);Integrated Security=True;  
initial catalog="AdventureWorks;NewValue=Bad"  
```  
  
## <a name="building-connection-strings-from-configuration-files"></a><span data-ttu-id="f5a4b-122">Yapı bağlantı dizeleri yapılandırma dosyaları</span><span class="sxs-lookup"><span data-stu-id="f5a4b-122">Building Connection Strings from Configuration Files</span></span>  
 <span data-ttu-id="f5a4b-123">Belirli öğeleri, bir bağlantı dizesi önceden biliniyorsa, bunlar bir yapılandırma dosyasında depolanabilir ve tam bağlantı dizesi oluşturmak için çalışma zamanında alınan.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-123">If certain elements of a connection string are known beforehand, they can be stored in a configuration file and retrieved at run time to construct a complete connection string.</span></span> <span data-ttu-id="f5a4b-124">Örneğin, veritabanının adı önceden bilinen, ancak sunucu adını değil olabilir.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-124">For example, the name of the database might be known in advance, but not the name of the server.</span></span> <span data-ttu-id="f5a4b-125">Veya diğer değerleri bağlantı dizesi Ekle mümkün olmaksızın çalışma zamanında bir adı ve parola sağlamak için bir kullanıcı isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-125">Or you might want a user to supply a name and password at run time without being able to inject other values into the connection string.</span></span>  
  
 <span data-ttu-id="f5a4b-126">Bir bağlantı dizesi oluşturucusu için aşırı yüklü oluşturucular birini alır bir <xref:System.String> bağımsız değişken olarak, hangi kullanıcı girişten sonra tamamlanabilir bir kısmi bağlantı dizesi sağlayabilirsiniz olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-126">One of the overloaded constructors for a connection string builder takes a <xref:System.String> as an argument, which enables you to supply a partial connection string that can then be completed from user input.</span></span> <span data-ttu-id="f5a4b-127">Kısmi bağlantı dizesini yapılandırma dosyasında depolanır ve çalışma zamanında alınır.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-127">The partial connection string can be stored in a configuration file and retrieved at run time.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5a4b-128"><xref:System.Configuration> Ad alanı kullanan yapılandırma dosyaları için programlı erişim sağlayan <xref:System.Web.Configuration.WebConfigurationManager> Web uygulamaları için ve <xref:System.Configuration.ConfigurationManager> Windows uygulamaları için.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-128">The <xref:System.Configuration> namespace allows programmatic access to configuration files that use the <xref:System.Web.Configuration.WebConfigurationManager> for Web applications and the <xref:System.Configuration.ConfigurationManager> for Windows applications.</span></span> <span data-ttu-id="f5a4b-129">Bağlantı dizeleri ve yapılandırma dosyaları ile çalışma hakkında daha fazla bilgi için bkz: [bağlantı dizeleri ve yapılandırma dosyalarını](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="f5a4b-129">For more information about working with connection strings and configuration files, see [Connection Strings and Configuration Files](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md).</span></span>  
  
### <a name="example"></a><span data-ttu-id="f5a4b-130">Örnek</span><span class="sxs-lookup"><span data-stu-id="f5a4b-130">Example</span></span>  
 <span data-ttu-id="f5a4b-131">Bu örnek bir yapılandırma dosyasından bir kısmi bağlantı dizesi alma ve ayarlayarak Tamamlanıyor gösterir <xref:System.Data.SqlClient.SqlConnectionStringBuilder.DataSource%2A>, <xref:System.Data.SqlClient.SqlConnectionStringBuilder.UserID%2A>, ve <xref:System.Data.SqlClient.SqlConnectionStringBuilder.Password%2A> özelliklerini <xref:System.Data.SqlClient.SqlConnectionStringBuilder>.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-131">This example demonstrates retrieving a partial connection string from a configuration file and completing it by setting the <xref:System.Data.SqlClient.SqlConnectionStringBuilder.DataSource%2A>, <xref:System.Data.SqlClient.SqlConnectionStringBuilder.UserID%2A>, and <xref:System.Data.SqlClient.SqlConnectionStringBuilder.Password%2A> properties of the <xref:System.Data.SqlClient.SqlConnectionStringBuilder>.</span></span> <span data-ttu-id="f5a4b-132">Yapılandırma dosyası şu şekilde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-132">The configuration file is defined as follows.</span></span>  
  
```xml  
<connectionStrings>  
  <clear/>  
  <add name="partialConnectString"   
    connectionString="Initial Catalog=Northwind;"  
    providerName="System.Data.SqlClient" />  
</connectionStrings>  
```  
  
> [!NOTE]
>  <span data-ttu-id="f5a4b-133">Bir başvuru ayarlamalısınız `System.Configuration.dll` projenizdeki çalıştırmak için kod.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-133">You must set a reference to the `System.Configuration.dll` in your project for the code to run.</span></span>  
  
 [!code-csharp[DataWorks SqlConnectionStringBuilder.UserNamePwd#1](../../../../samples/snippets/csharp/VS_Snippets_ADO.NET/DataWorks SqlConnectionStringBuilder.UserNamePwd/CS/source.cs#1)]
 [!code-vb[DataWorks SqlConnectionStringBuilder.UserNamePwd#1](../../../../samples/snippets/visualbasic/VS_Snippets_ADO.NET/DataWorks SqlConnectionStringBuilder.UserNamePwd/VB/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="f5a4b-134">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="f5a4b-134">See Also</span></span>  
 [<span data-ttu-id="f5a4b-135">Bağlantı dizeleri</span><span class="sxs-lookup"><span data-stu-id="f5a4b-135">Connection Strings</span></span>](../../../../docs/framework/data/adonet/connection-strings.md)  
 [<span data-ttu-id="f5a4b-136">Gizlilik ve veri güvenliği</span><span class="sxs-lookup"><span data-stu-id="f5a4b-136">Privacy and Data Security</span></span>](../../../../docs/framework/data/adonet/privacy-and-data-security.md)  
 [<span data-ttu-id="f5a4b-137">ADO.NET yönetilen sağlayıcıları ve veri kümesi Geliştirici Merkezi</span><span class="sxs-lookup"><span data-stu-id="f5a4b-137">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)