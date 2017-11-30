---
title: "Nasıl Yapılır: Dosya Aramak için Arka Plan İş Parçacığı Kullanma"
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
- Multithreaded Windows Forms Control sample [Windows Forms]
- custom controls [Windows Forms], multithreading
- threading [Windows Forms], custom controls
- custom controls [Windows Forms], samples
ms.assetid: 7fe3956f-5b8f-4f78-8aae-c9eb0b28f13a
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 9f23a99418d585f43348cd155bc65a3c3e73742b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-use-a-background-thread-to-search-for-files"></a><span data-ttu-id="f7f29-102">Nasıl Yapılır: Dosya Aramak için Arka Plan İş Parçacığı Kullanma</span><span class="sxs-lookup"><span data-stu-id="f7f29-102">How to: Use a Background Thread to Search for Files</span></span>
<span data-ttu-id="f7f29-103"><xref:System.ComponentModel.BackgroundWorker> Bileşeni değiştirir ve işlevlerini ekler <xref:System.Threading> ad alanı; ancak, <xref:System.Threading> ad alanı tutulur geriye dönük uyumluluk ve gelecekte kullanım için seçerseniz.</span><span class="sxs-lookup"><span data-stu-id="f7f29-103">The <xref:System.ComponentModel.BackgroundWorker> component replaces and adds functionality to the <xref:System.Threading> namespace; however, the <xref:System.Threading> namespace is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="f7f29-104">Daha fazla bilgi için bkz: [BackgroundWorker bileşenine genel bakış](../../../../docs/framework/winforms/controls/backgroundworker-component-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f7f29-104">For more information, see [BackgroundWorker Component Overview](../../../../docs/framework/winforms/controls/backgroundworker-component-overview.md).</span></span>  
  
 <span data-ttu-id="f7f29-105">Windows Forms kendiliğinden boş iş parçacıklı olan yerel Win32 windows tabanlı olduğundan Windows Forms tek iş parçacıklı (STA) modeli kullanır.</span><span class="sxs-lookup"><span data-stu-id="f7f29-105">Windows Forms uses the single-threaded apartment (STA) model because Windows Forms is based on native Win32 windows that are inherently apartment-threaded.</span></span> <span data-ttu-id="f7f29-106">STA modeli bir pencere hiçbir iş parçacığı üzerinde oluşturulabilir ancak oluşturulduktan sonra iş parçacığı geçemezsiniz, ve ona tüm işlev çağrıları kendi oluşturma iş parçacığı üzerinde gerçekleşmesi anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-106">The STA model implies that a window can be created on any thread, but it cannot switch threads once created, and all function calls to it must occur on its creation thread.</span></span> <span data-ttu-id="f7f29-107">Windows Forms dışında .NET Framework sınıfları boş iş parçacığı modelini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f7f29-107">Outside Windows Forms, classes in the .NET Framework use the free threading model.</span></span> <span data-ttu-id="f7f29-108">.NET Framework iş parçacığı oluşturma hakkında daha fazla bilgi için bkz: [parçacıkları](../../../../docs/standard/threading/index.md).</span><span class="sxs-lookup"><span data-stu-id="f7f29-108">For information about threading in the .NET Framework, see [Threading](../../../../docs/standard/threading/index.md).</span></span>  
  
 <span data-ttu-id="f7f29-109">Denetimin oluşturma iş parçacığı dışında öğesinden çağrılması gereken denetim üzerinde herhangi bir yöntem için (üzerinde yürütülen) sıralanması gerekir, STA modeli gerektiriyor denetimin oluşturma iş parçacığı.</span><span class="sxs-lookup"><span data-stu-id="f7f29-109">The STA model requires that any methods on a control that need to be called from outside the control's creation thread must be marshaled to (executed on) the control's creation thread.</span></span> <span data-ttu-id="f7f29-110">Taban sınıfı <xref:System.Windows.Forms.Control> çeşitli yöntemler sağlar (<xref:System.Windows.Forms.Control.Invoke%2A>, <xref:System.Windows.Forms.Control.BeginInvoke%2A>, ve <xref:System.Windows.Forms.Control.EndInvoke%2A>) bu amaç için.</span><span class="sxs-lookup"><span data-stu-id="f7f29-110">The base class <xref:System.Windows.Forms.Control> provides several methods (<xref:System.Windows.Forms.Control.Invoke%2A>, <xref:System.Windows.Forms.Control.BeginInvoke%2A>, and <xref:System.Windows.Forms.Control.EndInvoke%2A>) for this purpose.</span></span> <span data-ttu-id="f7f29-111"><xref:System.Windows.Forms.Control.Invoke%2A>zaman uyumlu yöntemi çağrılar; <xref:System.Windows.Forms.Control.BeginInvoke%2A> zaman uyumsuz yöntem çağrısı yapmaz.</span><span class="sxs-lookup"><span data-stu-id="f7f29-111"><xref:System.Windows.Forms.Control.Invoke%2A> makes synchronous method calls; <xref:System.Windows.Forms.Control.BeginInvoke%2A> makes asynchronous method calls.</span></span>  
  
 <span data-ttu-id="f7f29-112">Kullanırsanız, çoklu iş parçacığı kullanımı yoğun bir kaynak hesaplama bir arka plan iş parçacığı üzerinde çalışırken yoğun bir kaynak görevler için denetim kullanıcı arabirimi yanıt verebilir durumda kalabilir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-112">If you use multithreading in your control for resource-intensive tasks, the user interface can remain responsive while a resource-intensive computation executes on a background thread.</span></span>  
  
 <span data-ttu-id="f7f29-113">Aşağıdaki örnek (`DirectorySearcher`) belirtilen arama dizesine uyan dosyaları için bir arka plan iş parçacığı özyinelemeli olarak aramak bir dizin kullanır ve ardından arama sonucu içeren bir liste kutusu doldurur birden çok iş parçacıklı bir Windows Forms denetimini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-113">The following sample (`DirectorySearcher`) shows a multithreaded Windows Forms control that uses a background thread to recursively search a directory for files matching a specified search string and then populates a list box with the search result.</span></span> <span data-ttu-id="f7f29-114">Örnek tarafından gösterilen anahtar kavramları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="f7f29-114">The key concepts illustrated by the sample are as follows:</span></span>  
  
-   <span data-ttu-id="f7f29-115">`DirectorySearcher`arama yapmak için yeni bir iş parçacığı başlatır.</span><span class="sxs-lookup"><span data-stu-id="f7f29-115">`DirectorySearcher` starts a new thread to perform the search.</span></span> <span data-ttu-id="f7f29-116">İş parçacığı yürütür `ThreadProcedure` sırayla yardımcı çağıran yöntemi `RecurseDirectory` gerçek arama yapmak ve liste kutusunu doldurmak için yöntemi.</span><span class="sxs-lookup"><span data-stu-id="f7f29-116">The thread executes the `ThreadProcedure` method that in turn calls the helper `RecurseDirectory` method to do the actual search and to populate the list box.</span></span> <span data-ttu-id="f7f29-117">Ancak, liste kutusunu doldurma iş parçacıkları arası çağrı, sonraki iki madde işaretli öğeleri açıklandığı gibi'gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-117">However, populating the list box requires a cross-thread call, as explained in the next two bulleted items.</span></span>  
  
-   <span data-ttu-id="f7f29-118">`DirectorySearcher`tanımlar `AddFiles` dosyaları için bir liste kutusu; ekleme yöntemi ancak `RecurseDirectory` doğrudan çağrılamaz `AddFiles` çünkü `AddFiles` yalnızca oluşturulan STA parçacığında yürütebilir `DirectorySearcher`.</span><span class="sxs-lookup"><span data-stu-id="f7f29-118">`DirectorySearcher` defines the `AddFiles` method to add files to a list box; however, `RecurseDirectory` cannot directly invoke `AddFiles` because `AddFiles` can execute only in the STA thread that created `DirectorySearcher`.</span></span>  
  
-   <span data-ttu-id="f7f29-119">Tek yolu `RecurseDirectory` çağırabilirsiniz `AddFiles` iş parçacıkları arası çağrı — diğer bir deyişle, göre çağırma <xref:System.Windows.Forms.Control.Invoke%2A> veya <xref:System.Windows.Forms.Control.BeginInvoke%2A> sıralamakta `AddFiles` oluşturma iş parçacığı için `DirectorySearcher`.</span><span class="sxs-lookup"><span data-stu-id="f7f29-119">The only way `RecurseDirectory` can call `AddFiles` is through a cross-thread call — that is, by calling <xref:System.Windows.Forms.Control.Invoke%2A> or <xref:System.Windows.Forms.Control.BeginInvoke%2A> to marshal `AddFiles` to the creation thread of `DirectorySearcher`.</span></span> <span data-ttu-id="f7f29-120">`RecurseDirectory`kullanan <xref:System.Windows.Forms.Control.BeginInvoke%2A> böylece çağrısı zaman uyumsuz olarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-120">`RecurseDirectory` uses <xref:System.Windows.Forms.Control.BeginInvoke%2A> so that the call can be made asynchronously.</span></span>  
  
-   <span data-ttu-id="f7f29-121">Bir yöntem hazırlama bir işlev işaretçisi veya geri çağırma denk gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-121">Marshaling a method requires the equivalent of a function pointer or callback.</span></span> <span data-ttu-id="f7f29-122">Bu, .NET Framework'teki temsilcileri kullanılarak gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-122">This is accomplished using delegates in the .NET Framework.</span></span> <span data-ttu-id="f7f29-123"><xref:System.Windows.Forms.Control.BeginInvoke%2A>bağımsız değişken olarak bir temsilciyi alır.</span><span class="sxs-lookup"><span data-stu-id="f7f29-123"><xref:System.Windows.Forms.Control.BeginInvoke%2A> takes a delegate as an argument.</span></span> <span data-ttu-id="f7f29-124">`DirectorySearcher`Bu nedenle bir temsilci tanımlar (`FileListDelegate`), bağlar `AddFiles` örneğine `FileListDelegate` kendi oluşturucusu ve bu temsilci örneği için geçişleri <xref:System.Windows.Forms.Control.BeginInvoke%2A>.</span><span class="sxs-lookup"><span data-stu-id="f7f29-124">`DirectorySearcher` therefore defines a delegate (`FileListDelegate`), binds `AddFiles` to an instance of `FileListDelegate` in its constructor, and passes this delegate instance to <xref:System.Windows.Forms.Control.BeginInvoke%2A>.</span></span> <span data-ttu-id="f7f29-125">`DirectorySearcher`Ayrıca arama tamamlandığında, sıralanmış olduğundan bir olayı temsilci tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f7f29-125">`DirectorySearcher` also defines an event delegate that is marshaled when the search is completed.</span></span>  
  
```vb  
Option Strict  
Option Explicit  
  
Imports System  
Imports System.IO  
Imports System.Threading  
Imports System.Windows.Forms  
  
Namespace Microsoft.Samples.DirectorySearcher  
   ' <summary>  
   '      This class is a Windows Forms control that implements a simple directory searcher.  
   '      You provide, through code, a search string and it will search directories on  
   '      a background thread, populating its list box with matches.  
   ' </summary>  
   Public Class DirectorySearcher  
      Inherits Control  
      ' Define a special delegate that handles marshaling  
      ' lists of file names from the background directory search  
      ' thread to the thread that contains the list box.  
      Delegate Sub FileListDelegate(files() As String, startIndex As Integer, count As Integer)  
  
      Private _listBox As ListBox  
      Private _searchCriteria As String  
      Private _searching As Boolean  
      Private _deferSearch As Boolean  
      Private _searchThread As Thread  
      Private _fileListDelegate As FileListDelegate  
      Private _onSearchComplete As EventHandler  
  
      Public Sub New()  
         _listBox = New ListBox()  
         _listBox.Dock = DockStyle.Fill  
  
         Controls.Add(_listBox)  
  
         _fileListDelegate = New FileListDelegate(AddressOf AddFiles)  
         _onSearchComplete = New EventHandler(AddressOf OnSearchComplete)  
      End Sub  
  
      Public Property SearchCriteria() As String  
         Get  
            Return _searchCriteria  
         End Get  
         Set  
            ' If currently searching, abort  
            ' the search and restart it after  
            ' setting the new criteria.  
            '  
            Dim wasSearching As Boolean = Searching  
  
            If wasSearching Then  
               StopSearch()  
            End If  
  
            _listBox.Items.Clear()  
            _searchCriteria = value  
  
            If wasSearching Then  
               BeginSearch()  
            End If  
         End Set  
      End Property  
  
      Public ReadOnly Property Searching() As Boolean  
         Get  
            Return _searching  
         End Get  
      End Property  
  
      Public Event SearchComplete As EventHandler  
  
      ' <summary>  
      ' This method is called from the background thread.  It is called through  
      ' a BeginInvoke call so that it is always marshaled to the thread that  
      ' owns the list box control.  
      ' </summary>  
      ' <param name="files"></param>  
      ' <param name="startIndex"></param>  
      ' <param name="count"></param>  
      Private Sub AddFiles(files() As String, startIndex As Integer, count As Integer)  
         While count > 0  
            count -= 1  
            _listBox.Items.Add(files((startIndex + count)))  
         End While  
      End Sub  
  
      Public Sub BeginSearch()  
         ' Create the search thread, which   
         ' will begin the search.  
         ' If already searching, do nothing.  
         '  
         If Searching Then  
            Return  
         End If  
  
         ' Start the search if the handle has  
         ' been created. Otherwise, defer it until the  
         ' handle has been created.  
         If IsHandleCreated Then  
            _searchThread = New Thread(New ThreadStart(AddressOf ThreadProcedure))  
            _searching = True  
            _searchThread.Start()  
         Else  
            _deferSearch = True  
         End If  
      End Sub  
  
      Protected Overrides Sub OnHandleDestroyed(e As EventArgs)  
         ' If the handle is being destroyed and you are not  
         ' recreating it, then abort the search.  
         If Not RecreatingHandle Then  
            StopSearch()  
         End If  
         MyBase.OnHandleDestroyed(e)  
      End Sub  
  
      Protected Overrides Sub OnHandleCreated(e As EventArgs)  
         MyBase.OnHandleCreated(e)  
         If _deferSearch Then  
            _deferSearch = False  
            BeginSearch()  
         End If  
      End Sub  
  
      ' <summary>  
      ' This method is called by the background thread when it has  
      ' finished the search.  
      ' </summary>  
      ' <param name="sender"></param>  
      ' <param name="e"></param>  
      Private Sub OnSearchComplete(sender As Object, e As EventArgs)  
         RaiseEvent SearchComplete(sender, e)  
      End Sub  
  
      Public Sub StopSearch()  
         If Not _searching Then  
            Return  
         End If  
  
         If _searchThread.IsAlive Then  
            _searchThread.Abort()  
            _searchThread.Join()  
         End If  
  
         _searchThread = Nothing  
         _searching = False  
      End Sub  
  
      ' <summary>  
      ' Recurses the given path, adding all files on that path to   
      ' the list box. After it finishes with the files, it  
      ' calls itself once for each directory on the path.  
      ' </summary>  
      ' <param name="searchPath"></param>  
      Private Sub RecurseDirectory(searchPath As String)  
         ' Split searchPath into a directory and a wildcard specification.  
         '  
         Dim directoryPath As String = Path.GetDirectoryName(searchPath)  
         Dim search As String = Path.GetFileName(searchPath)  
  
         ' If a directory or search criteria are not specified, then return.  
         '  
         If directoryPath Is Nothing Or search Is Nothing Then  
            Return  
         End If  
  
         Dim files() As String  
  
         ' File systems like NTFS that have  
         ' access permissions might result in exceptions  
         ' when looking into directories without permission.  
         ' Catch those exceptions and return.  
         Try  
            files = Directory.GetFiles(directoryPath, search)  
         Catch e As UnauthorizedAccessException  
            Return  
         Catch e As DirectoryNotFoundException  
            Return  
         End Try  
  
         ' Perform a BeginInvoke call to the list box  
         ' in order to marshal to the correct thread. It is not  
         ' very efficient to perform this marshal once for every  
         ' file, so batch up multiple file calls into one  
         ' marshal invocation.  
         Dim startingIndex As Integer = 0  
         While startingIndex < files.Length  
            ' Batch up 20 files at once, unless at the  
            ' end.  
            '  
            Dim count As Integer = 20  
            If count + startingIndex >= files.Length Then  
               count = files.Length - startingIndex  
            End If  
            ' Begin the cross-thread call. Because you are passing  
            ' immutable objects into this invoke method, you do not have to  
            ' wait for it to finish. If these were complex objects, you would  
            ' have to either create new instances of them or   
            ' wait for the thread to process this invoke before modifying  
            ' the objects.  
            Dim r As IAsyncResult = BeginInvoke(_fileListDelegate, New Object() {files, startingIndex, count})  
            startingIndex += count  
         End While  
         ' Now that you have finished the files in this directory, recurse  
         ' for each subdirectory.  
         Dim directories As String() = Directory.GetDirectories(directoryPath)  
         Dim d As String  
         For Each d In  directories  
            RecurseDirectory(Path.Combine(d, search))  
         Next d  
      End Sub  
  
      '/ <summary>  
      '/ This is the actual thread procedure. This method runs in a background  
      '/ thread to scan directories. When finished, it simply exits.  
      '/ </summary>  
      Private Sub ThreadProcedure()  
         ' Get the search string. Individual   
         ' field assigns are atomic in .NET, so you do not  
         ' need to use any thread synchronization to grab  
         ' the string value here.  
         Try  
            Dim localSearch As String = SearchCriteria  
  
            ' Now, search the file system.  
            '  
            RecurseDirectory(localSearch)  
         Finally  
            ' You are done with the search, so update.  
            '  
            _searching = False  
  
            ' Raise an event that notifies the user that  
            ' the search has terminated.    
            ' You do not have to do this through a marshaled call, but  
            ' marshaling is recommended for the following reason:  
            ' Users of this control do not know that it is  
            ' multithreaded, so they expect its events to   
            ' come back on the same thread as the control.  
            BeginInvoke(_onSearchComplete, New Object() {Me, EventArgs.Empty})  
         End Try  
      End Sub  
   End Class  
End Namespace  
```  
  
```csharp  
namespace Microsoft.Samples.DirectorySearcher  
{  
   using System;  
   using System.IO;  
   using System.Threading;  
   using System.Windows.Forms;  
  
   /// <summary>  
   ///      This class is a Windows Forms control that implements a simple directory searcher.  
   ///      You provide, through code, a search string and it will search directories on  
   ///      a background thread, populating its list box with matches.  
   /// </summary>  
   public class DirectorySearcher : Control  
   {  
      // Define a special delegate that handles marshaling  
      // lists of file names from the background directory search  
      // thread to the thread that contains the list box.  
      private delegate void FileListDelegate(string[] files, int startIndex, int count);  
  
      private ListBox listBox;  
      private string  searchCriteria;  
      private bool searching;  
      private bool deferSearch;  
      private Thread searchThread;  
      private FileListDelegate fileListDelegate;  
      private EventHandler onSearchComplete;  
  
      public DirectorySearcher()  
      {  
         listBox = new ListBox();  
         listBox.Dock = DockStyle.Fill;  
  
         Controls.Add(listBox);  
  
         fileListDelegate = new FileListDelegate(AddFiles);  
         onSearchComplete = new EventHandler(OnSearchComplete);  
      }  
  
      public string SearchCriteria   
      {  
         get   
         {  
            return searchCriteria;  
         }  
         set   
         {  
            // If currently searching, abort  
            // the search and restart it after  
            // setting the new criteria.  
            //  
            bool wasSearching = Searching;  
  
            if (wasSearching)  
            {  
               StopSearch();  
            }  
  
            listBox.Items.Clear();  
            searchCriteria = value;  
  
            if (wasSearching)  
            {  
               BeginSearch();  
            }  
         }  
      }  
  
      public bool Searching   
      {  
         get   
         {  
            return searching;  
         }  
      }  
  
      public event EventHandler SearchComplete;  
  
      /// <summary>  
      /// This method is called from the background thread. It is called through  
      /// a BeginInvoke call so that it is always marshaled to the thread that  
      /// owns the list box control.  
      /// </summary>  
      /// <param name="files"></param>  
      /// <param name="startIndex"></param>  
      /// <param name="count"></param>  
      private void AddFiles(string[] files, int startIndex, int count)  
      {  
         while(count-- > 0)  
         {  
            listBox.Items.Add(files[startIndex + count]);  
         }  
      }  
  
      public void BeginSearch()   
      {  
         // Create the search thread, which   
         // will begin the search.  
         // If already searching, do nothing.  
         //  
         if (Searching)  
         {  
            return;  
         }  
  
         // Start the search if the handle has  
         // been created. Otherwise, defer it until the  
         // handle has been created.  
         if (IsHandleCreated)  
         {  
            searchThread = new Thread(new ThreadStart(ThreadProcedure));  
            searching = true;  
            searchThread.Start();  
         }  
         else  
         {  
            deferSearch = true;  
         }  
      }  
  
      protected override void OnHandleDestroyed(EventArgs e)  
      {  
         // If the handle is being destroyed and you are not  
         // recreating it, then abort the search.  
         if (!RecreatingHandle)  
         {  
            StopSearch();  
         }  
         base.OnHandleDestroyed(e);  
      }  
  
      protected override void OnHandleCreated(EventArgs e)   
      {  
         base.OnHandleCreated(e);  
         if (deferSearch)  
         {  
            deferSearch = false;  
            BeginSearch();  
         }  
      }  
  
      /// <summary>  
      /// This method is called by the background thread when it has finished  
      /// the search.  
      /// </summary>  
      /// <param name="sender"></param>  
      /// <param name="e"></param>  
      private void OnSearchComplete(object sender, EventArgs e)  
      {  
         if (SearchComplete != null)  
         {  
            SearchComplete(sender, e);  
         }  
      }  
  
      public void StopSearch()  
      {  
         if (!searching)  
         {  
            return;  
         }  
  
         if (searchThread.IsAlive)  
         {  
            searchThread.Abort();  
            searchThread.Join();  
         }  
  
         searchThread = null;  
         searching = false;  
      }  
  
      /// <summary>  
      /// Recurses the given path, adding all files on that path to   
      /// the list box. After it finishes with the files, it  
      /// calls itself once for each directory on the path.  
      /// </summary>  
      /// <param name="searchPath"></param>  
      private void RecurseDirectory(string searchPath)  
      {  
         // Split searchPath into a directory and a wildcard specification.  
         //  
         string directory = Path.GetDirectoryName(searchPath);  
         string search = Path.GetFileName(searchPath);  
  
         // If a directory or search criteria are not specified, then return.  
         //  
         if (directory == null || search == null)  
         {  
            return;  
         }  
  
         string[] files;  
  
         // File systems like NTFS that have  
         // access permissions might result in exceptions  
         // when looking into directories without permission.  
         // Catch those exceptions and return.  
         try   
         {  
            files = Directory.GetFiles(directory, search);  
         }  
         catch(UnauthorizedAccessException)  
         {  
            return;  
         }  
         catch(DirectoryNotFoundException)  
         {  
            return;  
         }  
  
         // Perform a BeginInvoke call to the list box  
         // in order to marshal to the correct thread. It is not  
         // very efficient to perform this marshal once for every  
         // file, so batch up multiple file calls into one  
         // marshal invocation.  
         int startingIndex = 0;  
  
         while(startingIndex < files.Length)  
         {  
            // Batch up 20 files at once, unless at the  
            // end.  
            //  
            int count = 20;  
            if (count + startingIndex >= files.Length)  
            {  
               count = files.Length - startingIndex;  
            }  
  
            // Begin the cross-thread call. Because you are passing  
            // immutable objects into this invoke method, you do not have to  
            // wait for it to finish. If these were complex objects, you would  
            // have to either create new instances of them or   
            // wait for the thread to process this invoke before modifying  
            // the objects.  
            IAsyncResult r = BeginInvoke(fileListDelegate, new object[] {files, startingIndex, count});  
            startingIndex += count;  
         }  
  
         // Now that you have finished the files in this directory, recurse for  
         // each subdirectory.  
         string[] directories = Directory.GetDirectories(directory);  
         foreach(string d in directories)  
         {  
            RecurseDirectory(Path.Combine(d, search));  
         }  
      }  
  
      /// <summary>  
      /// This is the actual thread procedure. This method runs in a background  
      /// thread to scan directories. When finished, it simply exits.  
      /// </summary>  
      private void ThreadProcedure()  
      {  
         // Get the search string. Individual   
         // field assigns are atomic in .NET, so you do not  
         // need to use any thread synchronization to grab  
         // the string value here.  
         try   
         {  
            string localSearch = SearchCriteria;  
  
            // Now, search the file system.  
            //  
            RecurseDirectory(localSearch);  
         }  
         finally  
         {  
            // You are done with the search, so update.  
            //  
            searching = false;  
  
            // Raise an event that notifies the user that  
            // the search has terminated.    
            // You do not have to do this through a marshaled call, but  
            // marshaling is recommended for the following reason:  
            // Users of this control do not know that it is  
            // multithreaded, so they expect its events to   
            // come back on the same thread as the control.  
            BeginInvoke(onSearchComplete, new object[] {this, EventArgs.Empty});  
         }  
      }  
   }  
}  
```  
  
## <a name="using-the-multithreaded-control-on-a-form"></a><span data-ttu-id="f7f29-126">Bir Form üzerinde birden çok iş parçacıklı Denetimi'ni kullanma</span><span class="sxs-lookup"><span data-stu-id="f7f29-126">Using the Multithreaded Control on a Form</span></span>  
 <span data-ttu-id="f7f29-127">Aşağıdaki örnekte gösterildiği nasıl birden çok iş parçacıklı `DirectorySearcher` denetimi bir form üzerinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f7f29-127">The following example shows how the multithreaded `DirectorySearcher` control can be used on a form.</span></span>  
  
```vb  
Option Explicit  
Option Strict  
  
Imports Microsoft.Samples.DirectorySearcher  
Imports System  
Imports System.Drawing  
Imports System.Collections  
Imports System.ComponentModel  
Imports System.Windows.Forms  
Imports System.Data  
  
Namespace SampleUsage  
  
   ' <summary>  
   '      Summary description for Form1.  
   ' </summary>  
   Public Class Form1  
      Inherits System.Windows.Forms.Form  
      Private WithEvents directorySearcher As DirectorySearcher  
      Private searchText As System.Windows.Forms.TextBox  
      Private searchLabel As System.Windows.Forms.Label  
      Private WithEvents searchButton As System.Windows.Forms.Button  
  
      Public Sub New()  
         '  
         ' Required for Windows Forms designer support.  
         '  
         InitializeComponent()  
         '  
         ' Add any constructor code after InitializeComponent call here.  
         '  
      End Sub  
  
      #Region "Windows Form Designer generated code"  
      ' <summary>  
      '      Required method for designer support. Do not modify  
      '      the contents of this method with the code editor.  
      ' </summary>  
      Private Sub InitializeComponent()  
         Me.directorySearcher = New Microsoft.Samples.DirectorySearcher.DirectorySearcher()  
         Me.searchButton = New System.Windows.Forms.Button()  
         Me.searchText = New System.Windows.Forms.TextBox()  
         Me.searchLabel = New System.Windows.Forms.Label()  
         Me.directorySearcher.Anchor = System.Windows.Forms.AnchorStyles.Top Or System.Windows.Forms.AnchorStyles.Bottom Or System.Windows.Forms.AnchorStyles.Left Or System.Windows.Forms.AnchorStyles.Right  
         Me.directorySearcher.Location = New System.Drawing.Point(8, 72)  
         Me.directorySearcher.SearchCriteria = Nothing  
         Me.directorySearcher.Size = New System.Drawing.Size(271, 173)  
         Me.directorySearcher.TabIndex = 2  
         Me.searchButton.Location = New System.Drawing.Point(8, 16)  
         Me.searchButton.Size = New System.Drawing.Size(88, 40)  
         Me.searchButton.TabIndex = 0  
         Me.searchButton.Text = "&Search"  
         Me.searchText.Anchor = System.Windows.Forms.AnchorStyles.Top Or System.Windows.Forms.AnchorStyles.Left Or System.Windows.Forms.AnchorStyles.Right  
         Me.searchText.Location = New System.Drawing.Point(104, 24)  
         Me.searchText.Size = New System.Drawing.Size(175, 20)  
         Me.searchText.TabIndex = 1  
         Me.searchText.Text = "c:\*.cs"  
         Me.searchLabel.ForeColor = System.Drawing.Color.Red  
         Me.searchLabel.Location = New System.Drawing.Point(104, 48)  
         Me.searchLabel.Size = New System.Drawing.Size(176, 16)  
         Me.searchLabel.TabIndex = 3  
         Me.ClientSize = New System.Drawing.Size(291, 264)  
         Me.Controls.AddRange(New System.Windows.Forms.Control() {Me.searchLabel, Me.directorySearcher, Me.searchText, Me.searchButton})  
         Me.Text = "Search Directories"  
      End Sub  
      #End Region  
  
      ' <summary>  
      '    The main entry point for the application.  
      ' </summary>  
      <STAThread()> _  
      Shared Sub Main()  
         Application.Run(New Form1())  
      End Sub  
  
      Private Sub searchButton_Click(sender As Object, e As System.EventArgs) Handles searchButton.Click  
         directorySearcher.SearchCriteria = searchText.Text  
         searchLabel.Text = "Searching..."  
         directorySearcher.BeginSearch()  
      End Sub  
  
      Private Sub directorySearcher_SearchComplete(sender As Object, e As System.EventArgs) Handles directorySearcher.SearchComplete  
         searchLabel.Text = String.Empty  
      End Sub  
   End Class  
End Namespace  
```  
  
```csharp  
namespace SampleUsage  
{  
   using Microsoft.Samples.DirectorySearcher;  
   using System;  
   using System.Drawing;  
   using System.Collections;  
   using System.ComponentModel;  
   using System.Windows.Forms;  
   using System.Data;  
  
   /// <summary>  
   ///      Summary description for Form1.  
   /// </summary>  
   public class Form1 : System.Windows.Forms.Form  
   {  
      private DirectorySearcher directorySearcher;  
      private System.Windows.Forms.TextBox searchText;  
      private System.Windows.Forms.Label searchLabel;  
      private System.Windows.Forms.Button searchButton;  
  
      public Form1()  
      {  
         //  
         // Required for Windows Forms designer support.  
         //  
         InitializeComponent();  
  
         //  
         // Add any constructor code after InitializeComponent call here.  
         //  
      }  
  
      #region Windows Form Designer generated code  
      /// <summary>  
      ///      Required method for designer support. Do not modify  
      ///      the contents of this method with the code editor.  
      /// </summary>  
      private void InitializeComponent()  
      {  
         this.directorySearcher = new Microsoft.Samples.DirectorySearcher.DirectorySearcher();  
         this.searchButton = new System.Windows.Forms.Button();  
         this.searchText = new System.Windows.Forms.TextBox();  
         this.searchLabel = new System.Windows.Forms.Label();  
         this.directorySearcher.Anchor = (((System.Windows.Forms.AnchorStyles.Top | System.Windows.Forms.AnchorStyles.Bottom)   
            | System.Windows.Forms.AnchorStyles.Left)   
            | System.Windows.Forms.AnchorStyles.Right);  
         this.directorySearcher.Location = new System.Drawing.Point(8, 72);  
         this.directorySearcher.SearchCriteria = null;  
         this.directorySearcher.Size = new System.Drawing.Size(271, 173);  
         this.directorySearcher.TabIndex = 2;  
         this.directorySearcher.SearchComplete += new System.EventHandler(this.directorySearcher_SearchComplete);  
         this.searchButton.Location = new System.Drawing.Point(8, 16);  
         this.searchButton.Size = new System.Drawing.Size(88, 40);  
         this.searchButton.TabIndex = 0;  
         this.searchButton.Text = "&Search";  
         this.searchButton.Click += new System.EventHandler(this.searchButton_Click);  
         this.searchText.Anchor = ((System.Windows.Forms.AnchorStyles.Top | System.Windows.Forms.AnchorStyles.Left)   
            | System.Windows.Forms.AnchorStyles.Right);  
         this.searchText.Location = new System.Drawing.Point(104, 24);  
         this.searchText.Size = new System.Drawing.Size(175, 20);  
         this.searchText.TabIndex = 1;  
         this.searchText.Text = "c:\\*.cs";  
         this.searchLabel.ForeColor = System.Drawing.Color.Red;  
         this.searchLabel.Location = new System.Drawing.Point(104, 48);  
         this.searchLabel.Size = new System.Drawing.Size(176, 16);  
         this.searchLabel.TabIndex = 3;  
         this.ClientSize = new System.Drawing.Size(291, 264);  
         this.Controls.AddRange(new System.Windows.Forms.Control[] {this.searchLabel,  
                                                        this.directorySearcher,  
                                                        this.searchText,  
                                                        this.searchButton});  
         this.Text = "Search Directories";  
  
      }  
      #endregion  
  
      /// <summary>  
      ///    The main entry point for the application.  
      /// </summary>  
      [STAThread]  
      static void Main()   
      {  
         Application.Run(new Form1());  
      }  
  
      private void searchButton_Click(object sender, System.EventArgs e)  
      {  
         directorySearcher.SearchCriteria = searchText.Text;  
         searchLabel.Text = "Searching...";  
         directorySearcher.BeginSearch();  
      }  
  
      private void directorySearcher_SearchComplete(object sender, System.EventArgs e)  
      {  
         searchLabel.Text = string.Empty;  
      }  
   }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="f7f29-128">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="f7f29-128">See Also</span></span>  
 <xref:System.ComponentModel.BackgroundWorker>  
 [<span data-ttu-id="f7f29-129">Özel Windows Forms denetimleri .NET Framework ile geliştirme</span><span class="sxs-lookup"><span data-stu-id="f7f29-129">Developing Custom Windows Forms Controls with the .NET Framework</span></span>](../../../../docs/framework/winforms/controls/developing-custom-windows-forms-controls.md)  
 [<span data-ttu-id="f7f29-130">Olay tabanlı zaman uyumsuz desene genel bakış</span><span class="sxs-lookup"><span data-stu-id="f7f29-130">Event-based Asynchronous Pattern Overview</span></span>](../../../../docs/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview.md)