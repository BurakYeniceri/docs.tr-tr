---
title: "Nasıl yapılır: FTP dizin içeriğiyle listesi"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 130c64c9-7b7f-4672-9b3b-d946bd2616c5
caps.latest.revision: "5"
author: mcleblanc
ms.author: markl
manager: markl
ms.workload: dotnet
ms.openlocfilehash: b3c0a5090709999ee5ab17e857bb5334d6982954
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-list-directory-contents-with-ftp"></a>Nasıl yapılır: FTP dizin içeriğiyle listesi
Bu örnek, FTP sunucusunda dizin içeriğini listesinde gösterilmiştir.  
  
## <a name="example"></a>Örnek  
  
```csharp  
using System;  
using System.IO;  
using System.Net;  
using System.Text;  
  
namespace Examples.System.Net  
{  
    public class WebRequestGetExample  
    {  
        public static void Main ()  
        {  
            // Get the object used to communicate with the server.  
            FtpWebRequest request = (FtpWebRequest)WebRequest.Create("ftp://www.contoso.com/");  
            request.Method = WebRequestMethods.Ftp.ListDirectoryDetails;  
  
            // This example assumes the FTP site uses anonymous logon.  
            request.Credentials = new NetworkCredential ("anonymous","janeDoe@contoso.com");  
  
            FtpWebResponse response = (FtpWebResponse)request.GetResponse();  
  
            Stream responseStream = response.GetResponseStream();  
            StreamReader reader = new StreamReader(responseStream);  
            Console.WriteLine(reader.ReadToEnd());  
  
            Console.WriteLine("Directory List Complete, status {0}", response.StatusDescription);  
  
            reader.Close();  
            response.Close();  
        }  
    }  
}  
```  
  
## <a name="compiling-the-code"></a>Kod Derleniyor  
 Bu örnek gerektirir:  
  
-   Başvurular **System.Net** ad alanı.  
  
## <a name="robust-programming"></a>Güçlü Programlama  
  
## <a name="net-framework-security"></a>.NET Framework Güvenliği
