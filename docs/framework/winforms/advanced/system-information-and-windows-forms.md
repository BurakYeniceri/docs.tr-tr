---
title: Sistem Bilgileri ve Windows Forms
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- domain names [Windows Forms], retrieving
- SystemInformation class [Windows Forms]
- user names [Windows Forms], retrieving
- system information [Windows Forms]
ms.assetid: 30cf43a3-8cb2-4ff3-862b-6c34576616a8
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 685a62b885469a9cac8884cc045b67bac02bea80
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="system-information-and-windows-forms"></a><span data-ttu-id="4926e-102">Sistem Bilgileri ve Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4926e-102">System Information and Windows Forms</span></span>
<span data-ttu-id="4926e-103">Bazen, uygulama kodunuzda kararları için üzerinde çalıştığı bilgisayar hakkında bilgi toplamak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4926e-103">Sometimes it is necessary to gather information about the computer that your application is running on in order to make decisions in your code.</span></span> <span data-ttu-id="4926e-104">Örneğin, yalnızca belirli bir ağ etki alanına bağlı olduğunda geçerlidir bir işleve sahip olabilir; Bu durumda etki alanını belirlemek ve etki alanı mevcut değilse işlevi devre dışı bırakmak için bir yol gerekir.</span><span class="sxs-lookup"><span data-stu-id="4926e-104">For example, you might have a function that is only applicable when connected to a particular network domain; in this case you would need a way to determine the domain and disable the function if the domain is not present.</span></span>  
  
 <span data-ttu-id="4926e-105">Windows Forms uygulamaları kullanabileceğiniz <xref:System.Windows.Forms.SystemInformation> çalışma zamanında bir bilgisayar ile ilgili birkaç belirlemek için sınıf.</span><span class="sxs-lookup"><span data-stu-id="4926e-105">Windows Forms applications can use the <xref:System.Windows.Forms.SystemInformation> class to determine a number of things about a computer at run time.</span></span> <span data-ttu-id="4926e-106">Aşağıdaki örnek, kullanma gösterir <xref:System.Windows.Forms.SystemInformation> almak için sınıf <xref:System.Windows.Forms.SystemInformation.UserName%2A> ve <xref:System.Windows.Forms.SystemInformation.UserDomainName%2A>:</span><span class="sxs-lookup"><span data-stu-id="4926e-106">The following example demonstrates using the <xref:System.Windows.Forms.SystemInformation> class to retrieve the <xref:System.Windows.Forms.SystemInformation.UserName%2A> and <xref:System.Windows.Forms.SystemInformation.UserDomainName%2A>:</span></span>  
  
```vb  
Dim User As String = Windows.Forms.SystemInformation.UserName  
Dim Domain As String = Windows.Forms.SystemInformation.UserDomainName  
  
MessageBox.Show("Good morning " & User & ". You are connected to " _  
& Domain)  
```  
  
```csharp  
string User = SystemInformation.UserName;  
string Domain = SystemInformation.UserDomainName;  
  
MessageBox.Show("Good morning " + User + ". You are connected to " _  
+ Domain)  
```  
  
 <span data-ttu-id="4926e-107">Tüm üyeleri <xref:System.Windows.Forms.SystemInformation> sınıfı salt okunur; kullanıcının ayarlarını değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4926e-107">All members of the <xref:System.Windows.Forms.SystemInformation> class are read-only; you cannot modify a user's settings.</span></span> <span data-ttu-id="4926e-108">Sınıfı, 100'den üyeleri bilgi her şeyi bilgisayara bağlı monitör sayısını döndürme vardır (<xref:System.Windows.Forms.SystemInformation.MonitorCount%2A>) için Windows Gezgini'nde simgeler aralığını (<xref:System.Windows.Forms.SystemInformation.IconHorizontalSpacing%2A> ve <xref:System.Windows.Forms.SystemInformation.IconVerticalSpacing%2A>).</span><span class="sxs-lookup"><span data-stu-id="4926e-108">There are over 100 members of the class, returning information on everything from the number of monitors attached to the computer (<xref:System.Windows.Forms.SystemInformation.MonitorCount%2A>) to the spacing of icons in Windows Explorer (<xref:System.Windows.Forms.SystemInformation.IconHorizontalSpacing%2A> and <xref:System.Windows.Forms.SystemInformation.IconVerticalSpacing%2A>).</span></span>  
  
 <span data-ttu-id="4926e-109">Bazı daha kullanışlı üyelerinin <xref:System.Windows.Forms.SystemInformation> sınıfı dahil <xref:System.Windows.Forms.SystemInformation.ComputerName%2A>, <xref:System.Windows.Forms.SystemInformation.DbcsEnabled%2A>, <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A>, ve <xref:System.Windows.Forms.SystemInformation.TerminalServerSession%2A>.</span><span class="sxs-lookup"><span data-stu-id="4926e-109">Some of the more useful members of the <xref:System.Windows.Forms.SystemInformation> class include <xref:System.Windows.Forms.SystemInformation.ComputerName%2A>, <xref:System.Windows.Forms.SystemInformation.DbcsEnabled%2A>, <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A>, and <xref:System.Windows.Forms.SystemInformation.TerminalServerSession%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4926e-110">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4926e-110">See Also</span></span>  
 <xref:System.Windows.Forms.SystemInformation>  
 [<span data-ttu-id="4926e-111">Windows Forms'ta Güç Yönetimi</span><span class="sxs-lookup"><span data-stu-id="4926e-111">Power Management in Windows Forms</span></span>](../../../../docs/framework/winforms/advanced/power-management-in-windows-forms.md)
