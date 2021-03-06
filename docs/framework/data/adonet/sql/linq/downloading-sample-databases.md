---
title: Örnek veritabanları için ADO.NET kod örnekleri edinin
description: SQL Server ve yönetim araçlarının yanı sıra ADO.NET belgeler, kod örnekleri kullanılan örnek veritabanları indirme
ms.date: 10/18/2018
ms.assetid: ef9d69a1-9461-43fe-94bb-7c836754bcb5
ms.openlocfilehash: 9779300288135cb9332a028d547ce55a07e89471
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50188397"
---
# <a name="get-the-sample-databases-for-adonet-code-samples"></a>Örnek veritabanları için ADO.NET kod örnekleri edinin

Örnekler ve izlenecek yollar, bir dizi [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] örnek veritabanları ve SQL Server Express belgeleri kullanın. Microsoft bu ürünlerin ücretsiz olarak indirebilirsiniz.

## <a name="get-the-northwind-sample-database"></a>Northwind örnek veritabanını almak

Northwind örnek veritabanıyla kurulan Microsoft Download Center'daki şu sayfadan yükleyin:

[Northwind ve Pubs örnek veritabanları](https://go.microsoft.com/fwlink?linkid=64296)

Dosya indirdi sonra veritabanları ve komut dosyalarını ayıklamak için dosyaya çift tıklayın. Varsayılan olarak, dosyaların klasöründe yüklü `<drive>:\SQL Server 2000 Sample Databases`.

Northwind veritabanı kullanabilmeniz için SQL Server örneği üzerinde veritabanı kullanarak oluşturmanız gerekebilir [SQL Server Management Studio](#get_ssms) veya çalıştırmak için benzer bir araç `instnwnd.sql` yükleme klasöründe betik dosyası.

## <a name="get-the-adventureworks-sample-database"></a>AdventureWorks örnek veritabanını almak

AdventureWorks örnek veritabanını aşağıdaki GitHub deposundan indirin:

[AdventureWorks örnek veritabanları](https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks)

Bir veritabanı yedeğinin indirdikten sonra (\*.bak) dosyaları, SQL Server örneğine SQL Server Management Studio (SSMS) kullanarak yedeklemeyi geri yükleme. Bkz: [alma SQL Server Management Studio'yu](#get_ssms).

## <a name="get_sql"></a> SQL Server Express edinin

SQL Server Express, SQL Server, uygulamaları yeniden dağıtabilirsiniz, ücretsiz, giriş düzeyi bir sürümüdür. SQL Server Express'i aşağıdaki sayfadan indirebilirsiniz:
  
[SQL Server Express sürümleri](https://www.microsoft.com/sql-server/sql-server-editions-express)

Kullanıyorsanız [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), SQL Server Express LocalDB, Professional ve üzeri sürümleri yanı sıra ücretsiz Community sürümü bulunur.  

## <a name="get_ssms"></a> SQL Server Management Studio'yu edinin
Görüntülemek veya karşıdan yüklediğiniz bir veritabanı değiştirmek istiyorsanız, SQL Server Management Studio (SSMS) kullanabilirsiniz. SSMS aşağıdaki sayfasından indirin:

[SQL Server Management Studio'yu (SSMS) indirin](/sql/ssms/download-sql-server-management-studio-ssms) 

Ayrıca, görüntüleyin ve Visual Studio tümleşik geliştirme ortamı (IDE) veritabanlarında yönetin. İçinde [Visual Studio](https://www.visualstudio.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017), veritabanından bağlanma **SQL Server Nesne Gezgini**, ya da veritabanında veri bağlantısı oluşturma **Sunucu Gezgini**. Bu Gezgini bölmeden açın **görünümü** menüsü.
  
## <a name="see-also"></a>Ayrıca bkz.

- [Başlarken](../../../../../../docs/framework/data/adonet/sql/linq/getting-started.md)
