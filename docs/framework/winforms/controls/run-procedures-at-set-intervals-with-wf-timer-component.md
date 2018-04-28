---
title: 'Nasıl yapılır: Windows Forms Süreölçer Bileşeni ile Belirlenen Aralıklarda Yordamları Çalıştırma'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-winforms
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], timers
- timers [Windows Forms], event intervals
- initialization [Windows Forms], Timer components
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], initializing
- procedures [Windows Forms], specific time intervals
ms.assetid: 8025247a-2de4-4d86-b8ab-a8cb8aeab2ea
caps.latest.revision: 20
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: b0b25f2ea86e58b7fe644f84412d1923fa761b82
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2018
---
# <a name="how-to-run-procedures-at-set-intervals-with-the-windows-forms-timer-component"></a><span data-ttu-id="cb9b0-102">Nasıl yapılır: Windows Forms Süreölçer Bileşeni ile Belirlenen Aralıklarda Yordamları Çalıştırma</span><span class="sxs-lookup"><span data-stu-id="cb9b0-102">How to: Run Procedures at Set Intervals with the Windows Forms Timer Component</span></span>
<span data-ttu-id="cb9b0-103">Bazen belirli zaman aralıklarında bir döngü sona erdi veya ayarlanmış bir zaman aralığından geçtiğinde çalıştıran kadar çalıştıran bir yordam oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-103">You might sometimes want to create a procedure that runs at specific time intervals until a loop has finished or that runs when a set time interval has elapsed.</span></span> <span data-ttu-id="cb9b0-104"><xref:System.Windows.Forms.Timer> Bileşen bu tür bir yordam olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-104">The <xref:System.Windows.Forms.Timer> component makes such a procedure possible.</span></span>  
  
 <span data-ttu-id="cb9b0-105">Bu bileşen, bir Windows Forms ortamı için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-105">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="cb9b0-106">Bir sunucu ortamı için uygun bir süreölçer gerekirse bkz [sunucu tabanlı zamanlayıcılar giriş](http://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span><span class="sxs-lookup"><span data-stu-id="cb9b0-106">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](http://msdn.microsoft.com/library/adc0bc0a-a519-4812-bafc-fb9d1a5801fc).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="cb9b0-107">Bazı sınırlamalar vardır kullanırken <xref:System.Windows.Forms.Timer> bileşeni.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-107">There are some limitations when using the <xref:System.Windows.Forms.Timer> component.</span></span> <span data-ttu-id="cb9b0-108">Daha fazla bilgi için bkz: [Windows Forms süreölçer bileşeninin aralık özelliği sınırlamaları](../../../../docs/framework/winforms/controls/limitations-of-the-timer-component-interval-property.md).</span><span class="sxs-lookup"><span data-stu-id="cb9b0-108">For more information, see [Limitations of the Windows Forms Timer Component's Interval Property](../../../../docs/framework/winforms/controls/limitations-of-the-timer-component-interval-property.md).</span></span>  
  
### <a name="to-run-a-procedure-at-set-intervals-with-the-timer-component"></a><span data-ttu-id="cb9b0-109">Süreölçer bileşeni ile belirlenen aralıklarda bir yordamı çalıştırmak için</span><span class="sxs-lookup"><span data-stu-id="cb9b0-109">To run a procedure at set intervals with the Timer component</span></span>  
  
1.  <span data-ttu-id="cb9b0-110">Ekleme bir <xref:System.Windows.Forms.Timer> formunuza.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-110">Add a <xref:System.Windows.Forms.Timer> to your form.</span></span> <span data-ttu-id="cb9b0-111">Bu program aracılığıyla yapmak nasıl bir çizimi için aşağıdaki örnek bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-111">See the following Example section for an illustration of how to do this programmatically.</span></span> <span data-ttu-id="cb9b0-112">Visual Studio bileşenleri bir forma ekleme desteği de vardır.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-112">Visual Studio also has support for adding components to a form.</span></span> <span data-ttu-id="cb9b0-113">Ayrıca bkz. [nasıl yapılır: ekleme denetimleri olmadan bir kullanıcı arabirimine Windows Forms](http://msdn.microsoft.com/library/becyw7bz\(v=vs.110\)).</span><span class="sxs-lookup"><span data-stu-id="cb9b0-113">Also see [How to: Add Controls Without a User Interface to Windows Forms](http://msdn.microsoft.com/library/becyw7bz\(v=vs.110\)).</span></span>  
  
2.  <span data-ttu-id="cb9b0-114">Ayarlama <xref:System.Windows.Forms.Timer.Interval%2A> Zamanlayıcı için özelliği (milisaniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="cb9b0-114">Set the <xref:System.Windows.Forms.Timer.Interval%2A> property (in milliseconds) for the timer.</span></span> <span data-ttu-id="cb9b0-115">Bu özellik, yordamı tekrar çalıştırmadan önce ne kadar süre geçer belirler.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-115">This property determines how much time will pass before the procedure is run again.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="cb9b0-116">Daha sık süreölçer olayı oluşur, daha fazla işlemci zamanı olaya yanıt olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-116">The more often a timer event occurs, the more processor time is used in responding to the event.</span></span> <span data-ttu-id="cb9b0-117">Bu genel performansını yavaşlatabilir.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-117">This can slow down overall performance.</span></span> <span data-ttu-id="cb9b0-118">Gereksinim duyduğunuz daha küçük bir aralık ayarlı değil.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-118">Do not set a smaller interval than you need.</span></span>  
  
3.  <span data-ttu-id="cb9b0-119">Uygun kodu yazmak <xref:System.Windows.Forms.Timer.Tick> olay işleyicisi.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-119">Write appropriate code in the <xref:System.Windows.Forms.Timer.Tick> event handler.</span></span> <span data-ttu-id="cb9b0-120">Bu durumda yazma kodu, belirtilen aralıkta çalıştıracak <xref:System.Windows.Forms.Timer.Interval%2A> özelliği.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-120">The code you write in this event will run at the interval specified in the <xref:System.Windows.Forms.Timer.Interval%2A> property.</span></span>  
  
4.  <span data-ttu-id="cb9b0-121">Ayarlama <xref:System.Windows.Forms.Timer.Enabled%2A> özelliğine `true` süreölçeri başlatmak için.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-121">Set the <xref:System.Windows.Forms.Timer.Enabled%2A> property to `true` to start the timer.</span></span> <span data-ttu-id="cb9b0-122"><xref:System.Windows.Forms.Timer.Tick> Olay başlayacak gerçekleşmesi belirlenen aralıkta yordamınız çalışıyor.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-122">The <xref:System.Windows.Forms.Timer.Tick> event will begin to occur, running your procedure at the set interval.</span></span>  
  
5.  <span data-ttu-id="cb9b0-123">Uygun sırada ayarlamak <xref:System.Windows.Forms.Timer.Enabled%2A> özelliğine `false` yeniden çalışmasını yordamı durdurmak için.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-123">At the appropriate time, set the <xref:System.Windows.Forms.Timer.Enabled%2A> property to `false` to stop the procedure from running again.</span></span> <span data-ttu-id="cb9b0-124">Aralığı ayarını `0` durdurmak Zamanlayıcı neden olmaz.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-124">Setting the interval to `0` does not cause the timer to stop.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb9b0-125">Örnek</span><span class="sxs-lookup"><span data-stu-id="cb9b0-125">Example</span></span>  
 <span data-ttu-id="cb9b0-126">Bu ilk örnek kod bir saniyelik artışlarla günün saatini izler.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-126">This first code example tracks the time of day in one-second increments.</span></span> <span data-ttu-id="cb9b0-127">Kullandığı bir <xref:System.Windows.Forms.Button>, <xref:System.Windows.Forms.Label>ve bir <xref:System.Windows.Forms.Timer> bir form üzerinde bileşen.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-127">It uses a <xref:System.Windows.Forms.Button>, a <xref:System.Windows.Forms.Label>, and a <xref:System.Windows.Forms.Timer> component on a form.</span></span> <span data-ttu-id="cb9b0-128"><xref:System.Windows.Forms.Timer.Interval%2A> Özelliği 1000 (bir saniye eşit) olarak ayarlanmış.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-128">The <xref:System.Windows.Forms.Timer.Interval%2A> property is set to 1000 (equal to one second).</span></span> <span data-ttu-id="cb9b0-129">İçinde <xref:System.Windows.Forms.Timer.Tick> olay, etiketin resim yazısı geçerli saate ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-129">In the <xref:System.Windows.Forms.Timer.Tick> event, the label's caption is set to the current time.</span></span> <span data-ttu-id="cb9b0-130">Düğme tıklatıldığında <xref:System.Windows.Forms.Timer.Enabled%2A> özelliği ayarlanmış `false`, etiketin resim yazısı güncelleştirme gelen zamanlayıcı durduruluyor.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-130">When the button is clicked, the <xref:System.Windows.Forms.Timer.Enabled%2A> property is set to `false`, stopping the timer from updating the label's caption.</span></span> <span data-ttu-id="cb9b0-131">Aşağıdaki kod örneğinde bir formla sahip olmasını gerektiren bir <xref:System.Windows.Forms.Button> adlı Denetim `Button1`, <xref:System.Windows.Forms.Timer> adlı Denetim `Timer1`ve bir <xref:System.Windows.Forms.Label> adlı Denetim `Label1`.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-131">The following code example requires that you have a form with a <xref:System.Windows.Forms.Button> control named `Button1`, a <xref:System.Windows.Forms.Timer> control named `Timer1`, and a <xref:System.Windows.Forms.Label> control named `Label1`.</span></span>  
  
```vb  
Private Sub InitializeTimer()  
   ' Run this procedure in an appropriate event.  
   ' Set to 1 second.  
   Timer1.Interval = 1000  
   ' Enable timer.  
   Timer1.Enabled = True  
   Button1.Text = "Enabled"  
End Sub  
x  
Private Sub Timer1_Tick(ByVal Sender As Object, ByVal e As EventArgs) Handles Timer1.Tick  
' Set the caption to the current time.  
   Label1.Text = DateTime.Now  
End Sub  
  
Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
      If Button1.Text = "Stop" Then  
         Button1.Text = "Start"  
         Timer1.Enabled = False  
      Else  
         Button1.Text = "Stop"  
         Timer1.Enabled = True  
      End If  
End Sub  
```  
  
```csharp  
private void InitializeTimer()  
{  
    // Call this procedure when the application starts.  
    // Set to 1 second.  
    Timer1.Interval = 1000;  
    Timer1.Tick += new EventHandler(Timer1_Tick);  
  
    // Enable timer.  
    Timer1.Enabled = true;  
  
    Button1.Text = "Stop";  
    Button1.Click += new EventHandler(Button1_Click);  
}  
  
private void Timer1_Tick(object Sender, EventArgs e)     
{  
   // Set the caption to the current time.  
   Label1.Text = DateTime.Now.ToString();  
}  
  
private void Button1_Click(object sender, EventArgs e)  
{  
  if ( Button1.Text == "Stop" )  
  {  
    Button1.Text = "Start";  
    Timer1.Enabled = false;  
  }  
  else  
  {  
    Button1.Text = "Stop";  
    Timer1.Enabled = true;  
  }  
}  
```  
  
```cpp  
private:  
   void InitializeTimer()  
   {  
      // Run this procedure in an appropriate event.  
      // Set to 1 second.  
      timer1->Interval = 1000;  
      // Enable timer.  
      timer1->Enabled = true;  
      this->timer1->Tick += gcnew System::EventHandler(this,    
                               &Form1::timer1_Tick);  
  
      button1->Text = S"Stop";  
      this->button1->Click += gcnew System::EventHandler(this,   
                               &Form1::button1_Click);  
   }  
  
   void timer1_Tick(System::Object ^ sender,  
      System::EventArgs ^ e)  
   {  
      // Set the caption to the current time.  
      label1->Text = DateTime::Now.ToString();  
   }  
  
   void button1_Click(System::Object ^ sender,  
      System::EventArgs ^ e)  
   {  
      if ( button1->Text == "Stop" )  
      {  
         button1->Text = "Start";  
         timer1->Enabled = false;  
      }  
      else  
      {  
         button1->Text = "Stop";  
         timer1->Enabled = true;  
      }  
   }  
```  
  
## <a name="example"></a><span data-ttu-id="cb9b0-132">Örnek</span><span class="sxs-lookup"><span data-stu-id="cb9b0-132">Example</span></span>  
 <span data-ttu-id="cb9b0-133">Döngü tamamlanana kadar bu ikinci kod örneği bir yordam her 600 milisaniye çalışır.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-133">This second code example runs a procedure every 600 milliseconds until a loop has finished.</span></span> <span data-ttu-id="cb9b0-134">Aşağıdaki kod örneğinde bir formla sahip olmasını gerektiren bir <xref:System.Windows.Forms.Button> adlı Denetim `Button1`, <xref:System.Windows.Forms.Timer> adlı Denetim `Timer1`ve bir <xref:System.Windows.Forms.Label> adlı Denetim `Label1`.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-134">The following code example requires that you have a form with a <xref:System.Windows.Forms.Button> control named `Button1`, a <xref:System.Windows.Forms.Timer> control named `Timer1`, and a <xref:System.Windows.Forms.Label> control named `Label1`.</span></span>  
  
```vb  
' This variable will be the loop counter.  
Private counter As Integer  
  
Private Sub InitializeTimer()  
   ' Run this procedure in an appropriate event.  
   counter = 0  
   Timer1.Interval = 600  
   Timer1.Enabled = True  
End Sub  
  
Private Sub Timer1_Tick(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer1.Tick  
   If counter => 10 Then  
      ' Exit loop code.  
      Timer1.Enabled = False  
      counter = 0  
   Else  
      ' Run your procedure here.  
      ' Increment counter.  
      counter = counter + 1  
      Label1.Text = "Procedures Run: " & counter.ToString  
   End If  
End Sub  
```  
  
```csharp  
// This variable will be the loop counter.  
private int counter;  
  
private void InitializeTimer()  
{  
   // Run this procedure in an appropriate event.  
   counter = 0;  
   timer1.Interval = 600;  
   timer1.Enabled = true;  
   // Hook up timer's tick event handler.  
   this.timer1.Tick += new System.EventHandler(this.timer1_Tick);  
}  
  
private void timer1_Tick(object sender, System.EventArgs e)     
{  
   if (counter >= 10)   
   {  
      // Exit loop code.  
      timer1.Enabled = false;  
      counter = 0;  
   }  
   else  
   {  
      // Run your procedure here.  
      // Increment counter.  
      counter = counter + 1;  
      label1.Text = "Procedures Run: " + counter.ToString();  
      }  
}  
```  
  
```cpp  
private:  
   int counter;  
  
   void InitializeTimer()  
   {  
      // Run this procedure in an appropriate event.  
      counter = 0;  
      timer1->Interval = 600;  
      timer1->Enabled = true;  
      // Hook up timer's tick event handler.  
      this->timer1->Tick += gcnew System::EventHandler(this, &Form1::timer1_Tick);  
   }  
  
   void timer1_Tick(System::Object ^ sender,  
      System::EventArgs ^ e)  
   {  
      if (counter >= 10)   
      {  
         // Exit loop code.  
         timer1->Enabled = false;  
         counter = 0;  
      }  
      else  
      {  
         // Run your procedure here.  
         // Increment counter.  
         counter = counter + 1;  
         label1->Text = String::Concat("Procedures Run: ",  
            counter.ToString());  
      }  
   }  
```  
  
## <a name="see-also"></a><span data-ttu-id="cb9b0-135">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="cb9b0-135">See Also</span></span>  
 <xref:System.Windows.Forms.Timer>  
 [<span data-ttu-id="cb9b0-136">Süreölçer Bileşeni</span><span class="sxs-lookup"><span data-stu-id="cb9b0-136">Timer Component</span></span>](../../../../docs/framework/winforms/controls/timer-component-windows-forms.md)  
 [<span data-ttu-id="cb9b0-137">Süreölçer Bileşenine Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="cb9b0-137">Timer Component Overview</span></span>](../../../../docs/framework/winforms/controls/timer-component-overview-windows-forms.md)
