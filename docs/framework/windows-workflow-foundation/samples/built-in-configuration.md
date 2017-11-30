---
title: "Yerleşik yapılandırma"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 34e85c9b-088d-4347-816c-0f77cb73ef2f
caps.latest.revision: "15"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 7dc11c19025393ffb1ce8e10cbfa637f38a867fd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="built-in-configuration"></a><span data-ttu-id="96624-102">Yerleşik yapılandırma</span><span class="sxs-lookup"><span data-stu-id="96624-102">Built-in Configuration</span></span>
<span data-ttu-id="96624-103">Bu örnek, kullanım ve SQL iş akışı örneği depolama yapılandırmasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96624-103">This sample demonstrates the use and configuration of the SQL workflow instance store.</span></span> <span data-ttu-id="96624-104">SQL iş akışı örneği deposuna bir SQL tabanlı bir örnek deposuna uygulamasıdır.</span><span class="sxs-lookup"><span data-stu-id="96624-104">The SQL workflow instance store is a SQL-based implementation of an instance store.</span></span> <span data-ttu-id="96624-105">Kaydetme ve yükleme durumu için ve SQL Server veya SQL Server Express veritabanından bir örnek sağlar.</span><span class="sxs-lookup"><span data-stu-id="96624-105">It allows an instance to save and load its state to and from a SQL Server or SQL Server Express database.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="96624-106">Örnekler, bilgisayarınızda yüklü.</span><span class="sxs-lookup"><span data-stu-id="96624-106">The samples may already be installed on your computer.</span></span> <span data-ttu-id="96624-107">Devam etmeden önce aşağıdaki (varsayılan) dizin denetleyin.</span><span class="sxs-lookup"><span data-stu-id="96624-107">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="96624-108">Bu dizin mevcut değilse (indirme) gidin tüm indirmek için [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri.</span><span class="sxs-lookup"><span data-stu-id="96624-108">If this directory does not exist, go to (download page) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="96624-109">Bu örnek aşağıdaki dizinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="96624-109">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Persistence\BuiltInConfiguration`  
  
## <a name="sample-details"></a><span data-ttu-id="96624-110">Örnek Ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="96624-110">Sample Details</span></span>  
 <span data-ttu-id="96624-111">Bu örnek bir sayım hizmeti uygulayan bir iş akışı oluşur.</span><span class="sxs-lookup"><span data-stu-id="96624-111">This sample consists of a workflow that implements a counting service.</span></span> <span data-ttu-id="96624-112">Hizmetin başlangıç yöntemi çağrıldıktan sonra hizmet 0 ile 59 arasında sayar.</span><span class="sxs-lookup"><span data-stu-id="96624-112">Once the service's start method is invoked, the service counts from 0 to 59.</span></span> <span data-ttu-id="96624-113">2 saniyede sayaç artırılır.</span><span class="sxs-lookup"><span data-stu-id="96624-113">The counter is incremented once every 2 seconds.</span></span> <span data-ttu-id="96624-114">Her sayısı sonra iş akışı devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="96624-114">After each count, the workflow persists.</span></span>  
  
 <span data-ttu-id="96624-115">Sayım iş akışını bir iş akışı hizmeti ana bilgisayar tarafından kendiliğinden barındırılır.</span><span class="sxs-lookup"><span data-stu-id="96624-115">The counting workflow is self-hosted by a workflow service host.</span></span> <span data-ttu-id="96624-116">Programın `Main` yöntemi sayım iş akışı barındıran iş akışı hizmeti ana bilgisayarı örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96624-116">The program's `Main` method creates an instance of the workflow service host that hosts the counting workflow.</span></span> <span data-ttu-id="96624-117">Sayım iş akışı altında ulaşılabilen uç noktaları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="96624-117">It defines the endpoints under which the counting workflow can be reached.</span></span> <span data-ttu-id="96624-118">Bundan sonra SQL iş akışı örneği deposunu yapılandırmak için kullanılan bir SQL iş akışı örneği deposu davranışı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="96624-118">After that, it defines a SQL workflow instance store behavior, which is used to configure the SQL workflow instance store.</span></span> <span data-ttu-id="96624-119">Ardından, program sayım iş akışının başlangıç yöntemini çağıran bir istemci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96624-119">Next, the program creates a client that calls the start method of the counting workflow.</span></span>  
  
 <span data-ttu-id="96624-120">Program başladıktan sonra sayaç sayım otomatik olarak başlar.</span><span class="sxs-lookup"><span data-stu-id="96624-120">Once the program is started, the counter automatically starts counting.</span></span> <span data-ttu-id="96624-121">Örneği yüklemek ve SQL iş akışı örneği deposunu yapılandırmak için birkaç saniye sürebilir unutmayın.</span><span class="sxs-lookup"><span data-stu-id="96624-121">Note that it might take a few seconds to load the instance and configure the SQL workflow instance store.</span></span> [!INCLUDE[crabout](../../../../includes/crabout-md.md)]<span data-ttu-id="96624-122">İş akışı örneği deposu bkz [SQL iş akışı örneği deposuna](../../../../docs/framework/windows-workflow-foundation/sql-workflow-instance-store.md).</span><span class="sxs-lookup"><span data-stu-id="96624-122"> the workflow instance store, see [SQL Workflow Instance Store](../../../../docs/framework/windows-workflow-foundation/sql-workflow-instance-store.md).</span></span>  
  
 <span data-ttu-id="96624-123">Örnek iki bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="96624-123">The sample consists of two parts:</span></span>  
  
1.  <span data-ttu-id="96624-124">InstanceStore1 gösterir nasıl <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> C# kodu kullanarak yapılandırılır (Program.cs bakın).</span><span class="sxs-lookup"><span data-stu-id="96624-124">InstanceStore1 shows how <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> is configured using C# code (see Program.cs).</span></span>  
  
2.  <span data-ttu-id="96624-125">InstanceStore2 gösterir nasıl <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> XML kullanarak yapılandırılır (App.config bakın).</span><span class="sxs-lookup"><span data-stu-id="96624-125">InstanceStore2 shows how <xref:System.Activities.DurableInstancing.SqlWorkflowInstanceStore> is configured using XML (see App.config).</span></span>  
  
 <span data-ttu-id="96624-126">SQL iş akışı örneği deposuna davranışı yapılandırmak aşağıdaki ayarlar kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="96624-126">The following settings are available to configure the SQL Workflow Instance Store behavior:</span></span>  
  
-   <span data-ttu-id="96624-127">Ayarlama `HostLockRenewalPeriod`.</span><span class="sxs-lookup"><span data-stu-id="96624-127">Set the `HostLockRenewalPeriod`.</span></span> <span data-ttu-id="96624-128">Bu süre ile ana bilgisayar çalıştırılan örneklerinin sahipliği kilit yeniler aralığı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="96624-128">This time defines the interval with which the host renews the ownership lock of the instances it runs.</span></span> <span data-ttu-id="96624-129">Kilit bilgileri örnek deposunda saklanır.</span><span class="sxs-lookup"><span data-stu-id="96624-129">The lock information is stored in the Instance Store.</span></span> <span data-ttu-id="96624-130">Sahipliği iki tanımlı aralıklar için yenilendi değil, `HostLockRenewalPeriod`, örnek terk değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="96624-130">If the ownership is not renewed for two of the intervals defined in `HostLockRenewalPeriod`, the instance is considered abandoned.</span></span> <span data-ttu-id="96624-131">Başka bir <xref:System.ServiceModel.Activities.WorkflowServiceHost> aynı iş akışını çalıştıran ve aynı örnek depolama (ya da aynı bilgisayarda veya farklı bir bilgisayara) bağlı, bu örnek kurtarır.</span><span class="sxs-lookup"><span data-stu-id="96624-131">If another <xref:System.ServiceModel.Activities.WorkflowServiceHost> is running the same workflow and connected to the same instance store (either on the same computer or a different computer), it recovers that instance.</span></span> <span data-ttu-id="96624-132">(Bu örnek için kapsam dışına örneği kurtarma olur.)</span><span class="sxs-lookup"><span data-stu-id="96624-132">(Instance Recovery is out of scope for this sample.)</span></span>  
  
-   <span data-ttu-id="96624-133">Ayarlama `RunnableInstancesDetectionPeriod`.</span><span class="sxs-lookup"><span data-stu-id="96624-133">Set the `RunnableInstancesDetectionPeriod`.</span></span> <span data-ttu-id="96624-134">Bu süre içinde ana bilgisayar yoklama için aralığı tanımlar runnable duruma gelmiş örnekleri.</span><span class="sxs-lookup"><span data-stu-id="96624-134">This period defines the interval in which the host polls for instances that have become runnable.</span></span> <span data-ttu-id="96624-135">Örnekleri aşağıdaki olaylardan herhangi biri oluştuğunda runnable hale gelebilir:</span><span class="sxs-lookup"><span data-stu-id="96624-135">Instances may become runnable if any of the following events occur:</span></span>  
  
    -   <span data-ttu-id="96624-136">Dayanıklı bir süreölçer (<xref:System.Activities.Statements.Delay>) süresi dolar.</span><span class="sxs-lookup"><span data-stu-id="96624-136">A Durable Timer (<xref:System.Activities.Statements.Delay>) expires.</span></span>  
  
    -   <span data-ttu-id="96624-137">Başka bir ana bilgisayar isabetsiz kendi `HostLockRenewal` sinyal (örneğin, bir bilgisayar çökmesinden dolayı) ve örnek kurtarıldı.</span><span class="sxs-lookup"><span data-stu-id="96624-137">Another host misses its `HostLockRenewal` heartbeat (for example, due to a computer crash) and the instance is recovered.</span></span>  
  
-   <span data-ttu-id="96624-138">Ayarlama `InstanceCompletionAction`.</span><span class="sxs-lookup"><span data-stu-id="96624-138">Set the `InstanceCompletionAction`.</span></span> <span data-ttu-id="96624-139">Bu özellik, kümesine `DeleteNothing`, örnek deposuna tamamlandı tutar durumlarda; kümesine IF `DeleteAll`, örnekleri tamamlanmasından sonra mağaza'dan silinir.</span><span class="sxs-lookup"><span data-stu-id="96624-139">This property, if set to `DeleteNothing`, keeps completed instances in the Instance Store; if set to `DeleteAll`, instances are deleted from the store upon completion.</span></span> <span data-ttu-id="96624-140">Aşağıdakilere dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="96624-140">Note that</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="96624-141">Ana bilgisayar sayım tamamlanmadan önce ENTER tuşuna basarak sonlandırma iş akışı örneği tamamlanmaz.</span><span class="sxs-lookup"><span data-stu-id="96624-141">Terminating the host by pressing ENTER before the counting has completed does not complete the workflow instance.</span></span>  
  
-   <span data-ttu-id="96624-142">Ayarlama `InstanceLockedExceptionAction`.</span><span class="sxs-lookup"><span data-stu-id="96624-142">Set the `InstanceLockedExceptionAction`.</span></span> <span data-ttu-id="96624-143">Bu ayar, başka bir ana bilgisayar tarafından kilitlenmiş bir örneğini yükleme istiyorsa, bir ana ne tanımlar.</span><span class="sxs-lookup"><span data-stu-id="96624-143">This setting defines what a host should do if it wants to load an instance that is locked by another host.</span></span> <span data-ttu-id="96624-144">Aşağıdaki seçenekler mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="96624-144">The following options exist:</span></span>  
  
    -   <span data-ttu-id="96624-145">Varsa kümesine `NoRetry`: değil yükleme işlemini yeniden deneyin ve dönüş bir `InstanceLockedException` ana bilgisayara.</span><span class="sxs-lookup"><span data-stu-id="96624-145">If set to `NoRetry`: Do not retry the load and return an `InstanceLockedException` to the host.</span></span>  
  
    -   <span data-ttu-id="96624-146">Varsa kümesine `BasicRetry`: örneğini yükleme yeniden denemeye devam.</span><span class="sxs-lookup"><span data-stu-id="96624-146">If set to `BasicRetry`: Keep retrying to load the instance.</span></span> <span data-ttu-id="96624-147">Yeniden deneme işlemleri bir Basit doğrusal algoritması göre zamanlanmış (örneğin, 5 saniyede yeniden).</span><span class="sxs-lookup"><span data-stu-id="96624-147">The retries are scheduled according to a simple linear algorithm (for example, retry every 5 seconds).</span></span>  
  
    -   <span data-ttu-id="96624-148">Varsa kümesine `AggressiveRetry`: örneğini yükleme yeniden denemeye devam.</span><span class="sxs-lookup"><span data-stu-id="96624-148">If set to `AggressiveRetry`: Keep retrying to load the instance.</span></span> <span data-ttu-id="96624-149">Yeniden deneme işlemleri bir agresif üstel geri alma algoritma göre zamanlanır.</span><span class="sxs-lookup"><span data-stu-id="96624-149">The retries are scheduled according to an aggressive exponential back-off algorithm.</span></span>  
  
-   <span data-ttu-id="96624-150">Kodlama seçeneğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="96624-150">Set the Encoding option.</span></span> <span data-ttu-id="96624-151">Bu ayar, örneğin durumu SQL iş akışı örneği deposunda nasıl depolandığını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="96624-151">This setting defines how the instance state is stored in the SQL Workflow Instance Store.</span></span> <span data-ttu-id="96624-152">Aşağıdaki seçenekler mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="96624-152">The following options exist:</span></span>  
  
    -   <span data-ttu-id="96624-153">Örnek durum GZip sıkıştırma algoritması kullanılarak sıkıştırılmış.</span><span class="sxs-lookup"><span data-stu-id="96624-153">The instance state is compressed using the GZip compression algorithm.</span></span>  
  
    -   <span data-ttu-id="96624-154">Örnek durum sıkıştırılmış değil.</span><span class="sxs-lookup"><span data-stu-id="96624-154">The instance state is not compressed.</span></span>  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="96624-155">Bu örneği kullanmak için</span><span class="sxs-lookup"><span data-stu-id="96624-155">To use this sample</span></span>  
  
1.  <span data-ttu-id="96624-156">Açık bir [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] izinleri varsa bir yönetici olarak komut istemi.</span><span class="sxs-lookup"><span data-stu-id="96624-156">Open a [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] command prompt as an Administrator if permissions are available.</span></span>  
  
2.  <span data-ttu-id="96624-157">Örnek dizine (\WF\Basic\Persistence\BuiltInConfiguration\CS) gidin ve CreateInstanceStore.cmd çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="96624-157">Navigate to the sample directory (\WF\Basic\Persistence\BuiltInConfiguration\CS) and run CreateInstanceStore.cmd.</span></span>  
  
3.  <span data-ttu-id="96624-158">Yönetici ayrıcalıkları yoksa, Create SQL Server oturum açma.</span><span class="sxs-lookup"><span data-stu-id="96624-158">If Administrator privileges are not available, Create SQL Server login.</span></span> <span data-ttu-id="96624-159">Git `Security`, **oturumları**.</span><span class="sxs-lookup"><span data-stu-id="96624-159">Go to `Security`, **Logins**.</span></span> <span data-ttu-id="96624-160">Sağ **oturumları** ve yeni bir oturum oluşturun.</span><span class="sxs-lookup"><span data-stu-id="96624-160">Right-click **Logins** and create a new login.</span></span>  
  
4.  <span data-ttu-id="96624-161">ACL kullanıcınız SQL rolüne ekleyin.</span><span class="sxs-lookup"><span data-stu-id="96624-161">Add your ACL user to SQL role.</span></span> <span data-ttu-id="96624-162">Açık **veritabanları**, **InstanceStore**, **güvenlik**.</span><span class="sxs-lookup"><span data-stu-id="96624-162">Open **Databases**, **InstanceStore**, **Security**.</span></span> <span data-ttu-id="96624-163">Sağ **kullanıcılar** seçip **yeni kullanıcılar**.</span><span class="sxs-lookup"><span data-stu-id="96624-163">Right-click **Users** and select **New users**.</span></span> <span data-ttu-id="96624-164">Ayarlama **oturum açma adı** önceki adımda oluşturduğunuz kullanıcı.</span><span class="sxs-lookup"><span data-stu-id="96624-164">Set the **Login name** to the user created in the previous step.</span></span> <span data-ttu-id="96624-165">Kullanıcı eklemek için veritabanı rolü üyeliği **System.Activities.DurableInstancing.InstanceStoreUsers** (ve diğerleri).</span><span class="sxs-lookup"><span data-stu-id="96624-165">Add the user to the Database role membership **System.Activities.DurableInstancing.InstanceStoreUsers** (and others).</span></span> <span data-ttu-id="96624-166">Kullanıcı zaten (örneğin, dbo kullanıcısı) bulunmayabilir unutmayın.</span><span class="sxs-lookup"><span data-stu-id="96624-166">Note that the user might exist already (for example, user dbo).</span></span>  
  
5.  <span data-ttu-id="96624-167">InstanceStore.sln dosyasında açma [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] ve CTRL + SHIFT + B tuşlarına basarak çözümü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="96624-167">Open the InstanceStore.sln file in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] and build the solution by pressing CTRL+SHIFT+B.</span></span>  
  
6.  <span data-ttu-id="96624-168">İçinde [!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)], örnek 's uygun bin\debug dizinine (\WF\Basic\Persistence\BuiltInConfiguration\cs\InstanceStore(1 or 2)\bin\debug) gidin, InstanceStore.exe sağ tıklatın ve seçin **yöneticiolarakçalıştır**.</span><span class="sxs-lookup"><span data-stu-id="96624-168">In [!INCLUDE[fileExplorer](../../../../includes/fileexplorer-md.md)], navigate to the sample’s appropriate bin\debug directory (\WF\Basic\Persistence\BuiltInConfiguration\cs\InstanceStore(1 or 2)\bin\debug), right click InstanceStore.exe and select **Run as administrator**.</span></span> <span data-ttu-id="96624-169">Bir kanal dinleyicisi açtığından Bu örnek yönetici ayrıcalıklarıyla çalıştırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="96624-169">This sample must be run with administrative privileges because it opens a channel listener.</span></span>  
  
7.  <span data-ttu-id="96624-170">Yerel SQL Server Express yüklemesi dışında bir veritabanında örnek deposuna oluşturduysanız, veritabanı bağlantı dizesi güncelleştirmeniz gerekir (`const string ConnectionString` InstanceStore1 projenin Program.cs içinde ve `connectionString` App.config özniteliği InstanceStore2 Proje) örnek ve örnek yeniden derleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="96624-170">If you created the instance store in a database other than a local installation of SQL Server Express you must update the database connection string (`const string ConnectionString` in Program.cs of the InstanceStore1 project, and the `connectionString` attribute in App.config of the InstanceStore2 project) in the sample and recompile the sample.</span></span>  
  
#### <a name="to-verify-the-sample-is-running-correctly"></a><span data-ttu-id="96624-171">Örnek doğrulamak için düzgün çalışıyor</span><span class="sxs-lookup"><span data-stu-id="96624-171">To verify the sample is running correctly</span></span>  
  
1.  <span data-ttu-id="96624-172">Örnek çalışırken, SQL Server Management Studio'yu başlatın.</span><span class="sxs-lookup"><span data-stu-id="96624-172">While the sample is running, start SQL Server Management Studio.</span></span>  
  
2.  <span data-ttu-id="96624-173">İçinde **Object Explorer**seçin **veritabanları**, **InstanceStore**, **tabloları**ve ardından  **System.Activities.DurableInstancing.InstanceTable**.</span><span class="sxs-lookup"><span data-stu-id="96624-173">In the **Object Explorer**, select **Databases**, **InstanceStore**, **Tables**, and then **System.Activities.DurableInstancing.InstanceTable**.</span></span>  
  
3.  <span data-ttu-id="96624-174">Sağ tıklayın **InstanceTable** seçip **ilk 1000 satırı Seç**.</span><span class="sxs-lookup"><span data-stu-id="96624-174">Right click **InstanceTable** and select **Select Top 1000 Rows**.</span></span>  
  
4.  <span data-ttu-id="96624-175">Yeni bir giriş ve, olup olmadığına bakın **kilitleme sona erme** 5 saniyede değiştirir (görev çubuğunu tıklatın **yürütme** sorgu yenilemek için düğmesini).</span><span class="sxs-lookup"><span data-stu-id="96624-175">Observe that there is a new entry and that the **Lock Expiration** changes every 5 seconds, (click the taskbar’s **Execute** button to refresh the query).</span></span> <span data-ttu-id="96624-176">Bu ayar bir sonucu olduğundan **konak kilit yenileme süresini** 5.</span><span class="sxs-lookup"><span data-stu-id="96624-176">This is a consequence of setting the **Host Lock Renewal Period** to 5.</span></span>  
  
5.  <span data-ttu-id="96624-177">Sayım tamamlandıktan sonra örnek tablosunda girişi kaldırılır inceleyin.</span><span class="sxs-lookup"><span data-stu-id="96624-177">Observe after the counting completes, that the entry in the instance table is removed.</span></span> <span data-ttu-id="96624-178">Bu ayar bir sonucu olduğundan **örneği tamamlama eylem** için **DeleteAll**.</span><span class="sxs-lookup"><span data-stu-id="96624-178">This is a consequence of setting **Instance Completion Action** to **DeleteAll**.</span></span>  
  
6.  <span data-ttu-id="96624-179">İş akışı ana sonlandırmak ve görüntülendiğini için ENTER tuşuna basın **LockOwnersTable** silinir.</span><span class="sxs-lookup"><span data-stu-id="96624-179">Press ENTER to terminate the workflow host application and observe that the **LockOwnersTable** is deleted.</span></span>  
  
#### <a name="to-uninstall-the-sample"></a><span data-ttu-id="96624-180">Örnek kaldırmak için</span><span class="sxs-lookup"><span data-stu-id="96624-180">To uninstall the sample</span></span>  
  
1.  <span data-ttu-id="96624-181">RemoveInstanceStore.cmd örnek dizininde (\WF\Basic\Persistence\BuiltInConfiguration) çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="96624-181">Run RemoveInstanceStore.cmd in the sample directory (\WF\Basic\Persistence\BuiltInConfiguration).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="96624-182">Örnekler, bilgisayarınızda yüklü.</span><span class="sxs-lookup"><span data-stu-id="96624-182">The samples may already be installed on your computer.</span></span> <span data-ttu-id="96624-183">Devam etmeden önce aşağıdaki (varsayılan) dizin denetleyin.</span><span class="sxs-lookup"><span data-stu-id="96624-183">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="96624-184">Bu dizin mevcut değilse, Git [Windows Communication Foundation (WCF) ve .NET Framework 4 için Windows Workflow Foundation (WF) örnek](http://go.microsoft.com/fwlink/?LinkId=150780) tüm indirmek için [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] ve [!INCLUDE[wf1](../../../../includes/wf1-md.md)] örnekleri.</span><span class="sxs-lookup"><span data-stu-id="96624-184">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="96624-185">Bu örnek aşağıdaki dizinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="96624-185">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Persistence\BuiltInConfiguration`  
  
## <a name="see-also"></a><span data-ttu-id="96624-186">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="96624-186">See Also</span></span>  
 [<span data-ttu-id="96624-187">AppFabric barındırma ve kalıcılığı örnekleri</span><span class="sxs-lookup"><span data-stu-id="96624-187">AppFabric Hosting and Persistence Samples</span></span>](http://go.microsoft.com/fwlink/?LinkId=193961)