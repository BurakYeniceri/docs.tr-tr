---
title: "Nasıl yapılır: sorgu için bir klasör (LINQ) (Visual Basic) kümesi bayt toplam sayısı"
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: bfe85ed2-44dc-4ef1-aac7-241622b80a69
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: b200581f4876400727c63e86e3ccf4a44c67914b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-query-for-the-total-number-of-bytes-in-a-set-of-folders-linq-visual-basic"></a><span data-ttu-id="dc24a-102">Nasıl yapılır: sorgu için bir klasör (LINQ) (Visual Basic) kümesi bayt toplam sayısı</span><span class="sxs-lookup"><span data-stu-id="dc24a-102">How to: Query for the Total Number of Bytes in a Set of Folders (LINQ) (Visual Basic)</span></span>
<span data-ttu-id="dc24a-103">Bu örnek belirtilen bir klasördeki tüm dosyaları ve onun tüm alt klasörleri tarafından kullanılan bayt toplam sayısını almak üzere nasıl gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc24a-103">This example shows how to retrieve the total number of bytes used by all the files in a specified folder and all its subfolders.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc24a-104">Örnek</span><span class="sxs-lookup"><span data-stu-id="dc24a-104">Example</span></span>  
 <span data-ttu-id="dc24a-105"><xref:System.Linq.Enumerable.Sum%2A> Yöntemi, seçilen tüm öğelerin değerini ekler `select` yan tümcesi.</span><span class="sxs-lookup"><span data-stu-id="dc24a-105">The <xref:System.Linq.Enumerable.Sum%2A> method adds the values of all the items selected in the `select` clause.</span></span> <span data-ttu-id="dc24a-106">Belirtilen dizin ağacındaki en büyük veya en küçük dosya çağırarak almak için bu sorguyu kolayca değiştirebilirsiniz <xref:System.Linq.Enumerable.Min%2A> veya <xref:System.Linq.Enumerable.Max%2A> yöntemi yerine <xref:System.Linq.Enumerable.Sum%2A>.</span><span class="sxs-lookup"><span data-stu-id="dc24a-106">You can easily modify this query to retrieve the biggest or smallest file in the specified directory tree by calling the <xref:System.Linq.Enumerable.Min%2A> or <xref:System.Linq.Enumerable.Max%2A> method instead of <xref:System.Linq.Enumerable.Sum%2A>.</span></span>  
  
```vb  
Module QueryTotalBytes  
    Sub Main()  
  
        ' Change the drive\path if necessary.  
        Dim root As String = "C:\Program Files\Microsoft Visual Studio 9.0\VB"  
  
        'Take a snapshot of the folder contents.  
        ' This method assumes that the application has discovery permissions  
        ' for all folders under the specified path.  
        Dim fileList = My.Computer.FileSystem.GetFiles _  
                  (root, FileIO.SearchOption.SearchAllSubDirectories, "*.*")  
  
        Dim fileQuery = From file In fileList _  
                        Select GetFileLength(file)  
  
        ' Force execution and cache the results to avoid multiple trips to the file system.  
        Dim fileLengths = fileQuery.ToArray()  
  
        ' Find the largest file  
        Dim maxSize = Aggregate aFile In fileLengths Into Max()  
  
        ' Find the total number of bytes  
        Dim totalBytes = Aggregate aFile In fileLengths Into Sum()  
  
        Console.WriteLine("The largest file is " & maxSize & " bytes")  
        Console.WriteLine("There are " & totalBytes & " total bytes in " & _  
                          fileList.Count & " files under " & root)  
  
        ' Keep the console window open in debug mode  
        Console.WriteLine("Press any key to exit.")  
        Console.ReadKey()  
    End Sub  
  
    ' This method is used to catch the possible exception  
    ' that can be raised when accessing the FileInfo.Length property.  
    Function GetFileLength(ByVal filename As String) As Long  
        Dim retval As Long  
        Try  
            Dim fi As New System.IO.FileInfo(filename)  
            retval = fi.Length  
        Catch ex As System.IO.FileNotFoundException  
            ' If a file is no longer present,  
            ' just return zero bytes.   
            retval = 0  
        End Try  
  
        Return retval  
    End Function  
End Module  
```  
  
 <span data-ttu-id="dc24a-107">Yalnızca belirtilen dizin ağacında bayt sayısını varsa, daha verimli bir veri kaynağı olarak liste koleksiyonu oluşturma için ek yükü doğurur LINQ Sorgu oluşturmadan bunu yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc24a-107">If you only have to count the number of bytes in a specified directory tree, you can do this more efficiently without creating a LINQ query, which incurs the overhead of creating the list collection as a data source.</span></span> <span data-ttu-id="dc24a-108">LINQ yaklaşım yararlılığı sorguyu daha karmaşık hale geldiğinde veya birden çok sorgu aynı veri kaynağına karşı çalıştırmak sahip olduğunuzda artırır.</span><span class="sxs-lookup"><span data-stu-id="dc24a-108">The usefulness of the LINQ approach increases as the query becomes more complex, or when you have to run multiple queries against the same data source.</span></span>  
  
 <span data-ttu-id="dc24a-109">Sorgu dosyası uzunluğu almak için ayrı bir yöntem için çağırır.</span><span class="sxs-lookup"><span data-stu-id="dc24a-109">The query calls out to a separate method to obtain the file length.</span></span> <span data-ttu-id="dc24a-110">Sonra başka bir iş parçacığında dosya silinirse, gerçekleştirilecektir olası özel kullanmak için bunu yapar <xref:System.IO.FileInfo> nesne çağrısında oluşturulduğu `GetFiles`.</span><span class="sxs-lookup"><span data-stu-id="dc24a-110">It does this in order to consume the possible exception that will be raised if the file was deleted on another thread after the <xref:System.IO.FileInfo> object was created in the call to `GetFiles`.</span></span> <span data-ttu-id="dc24a-111">Olsa bile <xref:System.IO.FileInfo> nesnesi zaten oluşturulmuş, özel durumu oluşabilir çünkü bir <xref:System.IO.FileInfo> nesne Yenile deneyecek kendi <xref:System.IO.FileInfo.Length%2A> özelliği erişildiğinde ilk kez en son uzunluğundaki özellik.</span><span class="sxs-lookup"><span data-stu-id="dc24a-111">Even though the <xref:System.IO.FileInfo> object has already been created, the exception can occur because a <xref:System.IO.FileInfo> object will try to refresh its <xref:System.IO.FileInfo.Length%2A> property with the most current length the first time the property is accessed.</span></span> <span data-ttu-id="dc24a-112">Try-catch bloğunda sorgu dışında bu işlemi koyarak kodu yan etkileri neden olan sorguları işlemlerinde önleme kuralı izler.</span><span class="sxs-lookup"><span data-stu-id="dc24a-112">By putting this operation in a try-catch block outside the query, the code follows the rule of avoiding operations in queries that can cause side-effects.</span></span> <span data-ttu-id="dc24a-113">Bir uygulama bilinmeyen bir durumda sol değil emin olmak için özel durumlar kullandığında genel olarak, çok dikkatli olunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc24a-113">In general, great care must be taken when you consume exceptions to make sure that an application is not left in an unknown state.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="dc24a-114">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="dc24a-114">Compiling the Code</span></span>  
 <span data-ttu-id="dc24a-115">.NET Framework sürüm 3.5 veya daha yüksek System.Core.dll başvuru hedefleyen bir proje oluşturun ve bir `Imports` System.Linq ad alanı bildirimi.</span><span class="sxs-lookup"><span data-stu-id="dc24a-115">Create a project that targets the .NET Framework version 3.5 or higher with a reference to System.Core.dll and a   `Imports` statement for the System.Linq namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc24a-116">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="dc24a-116">See Also</span></span>  
 [<span data-ttu-id="dc24a-117">LINQ to nesneler (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dc24a-117">LINQ to Objects (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md)  
 [<span data-ttu-id="dc24a-118">LINQ ve dosya dizinleri (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dc24a-118">LINQ and File Directories (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-and-file-directories.md)