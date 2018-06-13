---
title: 'Nasıl yapılır: LINQ SQL komutlarını görüntüleme'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 1decb05e-37ad-4ed6-ab2f-071eb4c4f628
ms.openlocfilehash: 2be4096f03fe73f417b4b1871ebfc3b4f0f67206
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33359897"
---
# <a name="how-to-display-linq-to-sql-commands"></a><span data-ttu-id="7acf8-102">Nasıl yapılır: LINQ SQL komutlarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="7acf8-102">How to: Display LINQ to SQL Commands</span></span>
<span data-ttu-id="7acf8-103">Kullanım <xref:System.Data.Linq.DataContext.GetCommand%2A> SQL komutlarını ve diğer bilgileri görüntülemek için.</span><span class="sxs-lookup"><span data-stu-id="7acf8-103">Use <xref:System.Data.Linq.DataContext.GetCommand%2A> to display SQL commands and other information.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7acf8-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="7acf8-104">Example</span></span>  
 <span data-ttu-id="7acf8-105">Aşağıdaki örnekte, ardından oluşturulan SQL komutlarını, komut türü ve bağlantı türü, sorgu çıktısı konsol penceresinde görüntüler.</span><span class="sxs-lookup"><span data-stu-id="7acf8-105">In the following example, the console window displays the output from the query, followed by the SQL commands that are generated, the type of commands, and the type of connection.</span></span>  
  
 [!code-csharp[DLinqDebuggingSupport#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#3)]
 [!code-vb[DLinqDebuggingSupport#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#3)]  
  
 <span data-ttu-id="7acf8-106">Çıktı aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="7acf8-106">Output appears as follows:</span></span>  
  
```  
Customers from London:  
    Thomas Hardy  
    Victoria Ashworth  
    Elizabeth Brown  
    Ann Devon  
    Simon Crowther  
    Marie Bertrand  
    Hari Kumar  
    Dominique Perrier  
```  
  
```  
Command Text:  
SELECT [t0].[CustomerID], [t0].[CompanyName], [t0].[ContactName], [t0].[ContactT  
itle], [t0].[Address], [t0].[City], [t0].[Region], [t0].[PostalCode], [t0].[Coun  
try], [t0].[Phone], [t0].[Fax]  
FROM [dbo].[Customers] AS [t0]  
WHERE [t0].[City] = @p0  
  
Command Type: Text  
  
Connection: System.Data.SqlClient.SqlConnection  
```  
  
## <a name="see-also"></a><span data-ttu-id="7acf8-107">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="7acf8-107">See Also</span></span>  
 [<span data-ttu-id="7acf8-108">Hata Ayıklama Desteği</span><span class="sxs-lookup"><span data-stu-id="7acf8-108">Debugging Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/debugging-support.md)
