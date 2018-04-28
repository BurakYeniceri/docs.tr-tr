---
title: 'Nasıl yapılır: MaskedTextBox Denetimine Veri Bağlama'
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
- MaskedTextBox control [Windows Forms]
- data binding [Windows Forms], MaskedTextBox control [Windows Forms]
- MaskedTextBox control [Windows Forms], binding data
ms.assetid: 34b29f07-e8df-48d4-b08b-53fcca524708
caps.latest.revision: 12
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8adf445de4648c0a751a852f67a55ca9683e3469
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-bind-data-to-the-maskedtextbox-control"></a><span data-ttu-id="4fcd3-102">Nasıl yapılır: MaskedTextBox Denetimine Veri Bağlama</span><span class="sxs-lookup"><span data-stu-id="4fcd3-102">How to: Bind Data to the MaskedTextBox Control</span></span>
<span data-ttu-id="4fcd3-103">Veriye bağlayabilirsiniz bir <xref:System.Windows.Forms.MaskedTextBox> herhangi bir Windows Forms denetimi için gibi denetleme.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-103">You can bind data to a <xref:System.Windows.Forms.MaskedTextBox> control just as you can to any other Windows Forms control.</span></span> <span data-ttu-id="4fcd3-104">Ancak, veritabanındaki verilerinizin biçimini maskesi tanımı tarafından beklenen biçimde eşleşmiyorsa, verileri yeniden biçimlendirmek gerekir.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-104">However, if the format of your data in the database does not match the format expected by your mask definition, you will need to reformat the data.</span></span> <span data-ttu-id="4fcd3-105">Aşağıdaki yordamı kullanarak bunu yapmayı gösteren <xref:System.Windows.Forms.Binding.Format> ve <xref:System.Windows.Forms.Binding.Parse> olayları <xref:System.Windows.Forms.Binding> ayrı telefon numarasını görüntülemek ve tek düzenlenebilir bir alanı telefon uzantısı veritabanı alanları sınıfı.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-105">The following procedure demonstrates how to do this using the <xref:System.Windows.Forms.Binding.Format> and <xref:System.Windows.Forms.Binding.Parse> events of the <xref:System.Windows.Forms.Binding> class to display separate phone number and phone extension database fields as a single editable field.</span></span>  
  
 <span data-ttu-id="4fcd3-106">Aşağıdaki yordam, yüklü Northwind örnek veritabanı olan bir SQL Server veritabanına erişimi olmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-106">The following procedure requires that you have access to a SQL Server database with the Northwind sample database installed.</span></span>  
  
### <a name="to-bind-data-to-a-maskedtextbox-control"></a><span data-ttu-id="4fcd3-107">MaskedTextBox denetimine veri bağlama</span><span class="sxs-lookup"><span data-stu-id="4fcd3-107">To bind data to a MaskedTextBox control</span></span>  
  
1.  <span data-ttu-id="4fcd3-108">Yeni bir Windows Forms projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-108">Create a new Windows Forms project.</span></span>  
  
2.  <span data-ttu-id="4fcd3-109">İki <xref:System.Windows.Forms.TextBox> ; formunuza denetimler bunları `FirstName` ve `LastName`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-109">Drag two <xref:System.Windows.Forms.TextBox> controls onto your form; name them `FirstName` and `LastName`.</span></span>  
  
3.  <span data-ttu-id="4fcd3-110">Sürükleme bir <xref:System.Windows.Forms.MaskedTextBox> kontrol formunuza; adlandırın `PhoneMask`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-110">Drag a <xref:System.Windows.Forms.MaskedTextBox> control onto your form; name it `PhoneMask`.</span></span>  
  
4.  <span data-ttu-id="4fcd3-111">Ayarlama <xref:System.Windows.Forms.MaskedTextBox.Mask%2A> özelliği `PhoneMask` için `(000) 000-0000 x9999`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-111">Set the <xref:System.Windows.Forms.MaskedTextBox.Mask%2A> property of `PhoneMask` to `(000) 000-0000 x9999`.</span></span>  
  
5.  <span data-ttu-id="4fcd3-112">Forma aşağıdaki ad alanını alır ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-112">Add the following namespace imports to the form.</span></span>  
  
    ```csharp  
    using System.Data.SqlClient;  
    ```  
  
    ```vb  
    Imports System.Data.SqlClient  
    ```  
  
6.  <span data-ttu-id="4fcd3-113">Forma sağ tıklayın ve seçin **görünümü kodu**.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-113">Right-click the form and choose **View Code**.</span></span> <span data-ttu-id="4fcd3-114">Bu kod, form sınıfınızda herhangi bir yere yerleştirin.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-114">Place this code anywhere in your form class.</span></span>  
  
    ```csharp  
    Binding currentBinding, phoneBinding;  
    DataSet employeesTable = new DataSet();  
    SqlConnection sc;  
    SqlDataAdapter dataConnect;  
  
    private void Form1_Load(object sender, EventArgs e)  
    {  
        DoMaskBinding();  
    }  
  
    private void DoMaskBinding()  
    {  
        try  
        {  
            sc = new SqlConnection("Data Source=CLIENTUE;Initial Catalog=NORTHWIND;Integrated Security=SSPI");  
            sc.Open();  
        }  
        catch (Exception ex)  
        {  
            MessageBox.Show(ex.Message);  
            return;  
        }  
  
        dataConnect = new SqlDataAdapter("SELECT * FROM Employees", sc);  
        dataConnect.Fill(employeesTable, "Employees");  
  
        // Now bind MaskedTextBox to appropriate field. Note that we must create the Binding objects  
        // before adding them to the control - otherwise, we won't get a Format event on the   
        // initial load.   
        try  
        {  
            currentBinding = new Binding("Text", employeesTable, "Employees.FirstName");  
            firstName.DataBindings.Add(currentBinding);  
  
            currentBinding = new Binding("Text", employeesTable, "Employees.LastName");  
            lastName.DataBindings.Add(currentBinding);  
  
            phoneBinding =new Binding("Text", employeesTable, "Employees.HomePhone");  
            // We must add the event handlers before we bind, or the Format event will not get called  
            // for the first record.  
            phoneBinding.Format += new ConvertEventHandler(phoneBinding_Format);  
            phoneBinding.Parse += new ConvertEventHandler(phoneBinding_Parse);  
            phoneMask.DataBindings.Add(phoneBinding);  
        }  
        catch (Exception ex)  
        {  
            MessageBox.Show(ex.Message);  
            return;  
        }  
    }  
    ```  
  
    ```vb  
    Dim WithEvents CurrentBinding, PhoneBinding As Binding  
    Dim EmployeesTable As New DataSet()  
    Dim sc As SqlConnection  
    Dim DataConnect As SqlDataAdapter  
  
    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load  
        DoMaskedBinding()  
    End Sub  
  
    Private Sub DoMaskedBinding()  
        Try  
            sc = New SqlConnection("Data Source=SERVERNAME;Initial Catalog=NORTHWIND;Integrated Security=SSPI")  
            sc.Open()  
        Catch ex As Exception  
            MessageBox.Show(ex.Message)  
            Exit Sub  
        End Try  
  
        DataConnect = New SqlDataAdapter("SELECT * FROM Employees", sc)  
        DataConnect.Fill(EmployeesTable, "Employees")  
  
        ' Now bind MaskedTextBox to appropriate field. Note that we must create the Binding objects  
        ' before adding them to the control - otherwise, we won't get a Format event on the   
        ' initial load.  
        Try  
            CurrentBinding = New Binding("Text", EmployeesTable, "Employees.FirstName")  
            firstName.DataBindings.Add(CurrentBinding)  
            CurrentBinding = New Binding("Text", EmployeesTable, "Employees.LastName")  
            lastName.DataBindings.Add(CurrentBinding)  
            PhoneBinding = New Binding("Text", EmployeesTable, "Employees.HomePhone")  
            PhoneMask.DataBindings.Add(PhoneBinding)  
        Catch ex As Exception  
            MessageBox.Show(ex.Message)  
            Application.Exit()  
        End Try  
    End Sub  
    ```  
  
7.  <span data-ttu-id="4fcd3-115">Olay işleyicileri ekleme <xref:System.Windows.Forms.Binding.Format> ve <xref:System.Windows.Forms.Binding.Parse> birleştirmek ve ayırmak için olayları `PhoneNumber` ve `Extension` bağlı alanlardan <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-115">Add event handlers for the <xref:System.Windows.Forms.Binding.Format> and <xref:System.Windows.Forms.Binding.Parse> events to combine and separate the `PhoneNumber` and `Extension` fields from the bound <xref:System.Data.DataSet>.</span></span>  
  
    ```csharp  
    private void phoneBinding_Format(Object sender, ConvertEventArgs e)  
    {  
        String ext;  
  
        DataRowView currentRow = (DataRowView)BindingContext[employeesTable, "Employees"].Current;  
        if (currentRow["Extension"] == null)   
        {  
            ext = "";  
        } else   
        {  
            ext = currentRow["Extension"].ToString();  
        }  
  
        e.Value = e.Value.ToString().Trim() + " x" + ext;  
    }  
  
    private void phoneBinding_Parse(Object sender, ConvertEventArgs e)  
    {  
        String phoneNumberAndExt = e.Value.ToString();  
  
        int extIndex = phoneNumberAndExt.IndexOf("x");  
        String ext = phoneNumberAndExt.Substring(extIndex).Trim();  
        String phoneNumber = phoneNumberAndExt.Substring(0, extIndex).Trim();  
  
        //Get the current binding object, and set the new extension manually.   
        DataRowView currentRow = (DataRowView)BindingContext[employeesTable, "Employees"].Current;  
        // Remove the "x" from the extension.  
        currentRow["Extension"] = ext.Substring(1);  
  
        //Return the phone number.  
        e.Value = phoneNumber;  
    }  
    ```  
  
    ```vb  
    Private Sub PhoneBinding_Format(ByVal sender As Object, ByVal e As ConvertEventArgs) Handles PhoneBinding.Format  
        Dim Ext As String  
  
        Dim CurrentRow As DataRowView = CType(Me.BindingContext(EmployeesTable, "Employees").Current, DataRowView)  
        If (CurrentRow("Extension") Is Nothing) Then  
            Ext = ""  
        Else  
            Ext = CurrentRow("Extension").ToString()  
        End If  
  
        e.Value = e.Value.ToString().Trim() & " x" & Ext  
    End Sub  
  
    Private Sub PhoneBinding_Parse(ByVal sender As Object, ByVal e As ConvertEventArgs) Handles PhoneBinding.Parse  
        Dim PhoneNumberAndExt As String = e.Value.ToString()  
  
        Dim ExtIndex As Integer = PhoneNumberAndExt.IndexOf("x")  
        Dim Ext As String = PhoneNumberAndExt.Substring(ExtIndex).Trim()  
        Dim PhoneNumber As String = PhoneNumberAndExt.Substring(0, ExtIndex).Trim()  
  
        ' Get the current binding object, and set the new extension manually.   
        Dim CurrentRow As DataRowView = CType(Me.BindingContext(EmployeesTable, "Employees").Current, DataRowView)  
        ' Remove the "x" from the extension.  
        CurrentRow("Extension") = CObj(Ext.Substring(1))  
  
        ' Return the phone number.  
        e.Value = PhoneNumber  
    End Sub  
    ```  
  
8.  <span data-ttu-id="4fcd3-116">İki eklemek <xref:System.Windows.Forms.Button> formu denetimleri.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-116">Add two <xref:System.Windows.Forms.Button> controls to the form.</span></span> <span data-ttu-id="4fcd3-117">Bunları `previousButton` ve `nextButton`.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-117">Name them `previousButton` and `nextButton`.</span></span> <span data-ttu-id="4fcd3-118">Her düğme eklemek için çift bir <xref:System.Windows.Forms.Control.Click> olay işleyicisi ve aşağıdaki kod örneğinde gösterildiği gibi olay işleyicileri doldurun.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-118">Double-click each button to add a <xref:System.Windows.Forms.Control.Click> event handler, and fill in the event handlers as shown in the following code example.</span></span>  
  
    ```csharp  
    private void previousButton_Click(object sender, EventArgs e)  
    {  
        BindingContext[employeesTable, "Employees"].Position = BindingContext[employeesTable, "Employees"].Position - 1;  
    }  
  
    private void nextButton_Click(object sender, EventArgs e)  
    {  
        BindingContext[employeesTable, "Employees"].Position = BindingContext[employeesTable, "Employees"].Position + 1;  
    }  
    ```  
  
    ```vb  
    Private Sub PreviousButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles PreviousButton.Click  
        Me.BindingContext(EmployeesTable, "Employees").Position = Me.BindingContext(EmployeesTable, "Employees").Position - 1  
    End Sub  
  
    Private Sub NextButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles NextButton.Click  
        Me.BindingContext(EmployeesTable, "Employees").Position = Me.BindingContext(EmployeesTable, "Employees").Position + 1  
    End Sub  
    ```  
  
9. <span data-ttu-id="4fcd3-119">Örnek çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-119">Run the sample.</span></span> <span data-ttu-id="4fcd3-120">Verileri düzenleyip kullanabileceğiniz **önceki** ve **sonraki** için verilerin düzgün bir şekilde kalıcı olduğunu görmek için düğmeler <xref:System.Data.DataSet>.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-120">Edit the data, and use the **Previous** and **Next** buttons to see that the data is properly persisted to the <xref:System.Data.DataSet>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4fcd3-121">Örnek</span><span class="sxs-lookup"><span data-stu-id="4fcd3-121">Example</span></span>  
 <span data-ttu-id="4fcd3-122">Aşağıdaki kod örneğinde, önceki yordamda tamamlanmasını sonucu listeleme tam kodudur.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-122">The following code example is the full code listing that results from completing the previous procedure.</span></span>  
  
 [!code-cpp[MaskedTextBoxData#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/MaskedTextBoxData/cpp/form1.cpp#1)]
 [!code-csharp[MaskedTextBoxData#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/MaskedTextBoxData/CS/form1.cs#1)]
 [!code-vb[MaskedTextBoxData#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/MaskedTextBoxData/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="4fcd3-123">Kod Derleniyor</span><span class="sxs-lookup"><span data-stu-id="4fcd3-123">Compiling the Code</span></span>  
  
-   <span data-ttu-id="4fcd3-124">Visual C# veya Visual Basic projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-124">Create a Visual C# or Visual Basic project.</span></span>  
  
-   <span data-ttu-id="4fcd3-125">Ekleme <xref:System.Windows.Forms.TextBox> ve <xref:System.Windows.Forms.MaskedTextBox> önceki yordamda açıklandığı gibi formuna denetler.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-125">Add the <xref:System.Windows.Forms.TextBox> and <xref:System.Windows.Forms.MaskedTextBox> controls to the form, as described in the previous procedure.</span></span>  
  
-   <span data-ttu-id="4fcd3-126">Projenin varsayılan form için kaynak kodu dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-126">Open the source code file for the project's default form.</span></span>  
  
-   <span data-ttu-id="4fcd3-127">Bu dosya kaynak kodunda önceki "Kod" bölümünde listelenen kod ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-127">Replace the source code in this file with the code listed in the previous "Code" section.</span></span>  
  
-   <span data-ttu-id="4fcd3-128">Uygulamayı derleyin.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-128">Compile the application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4fcd3-129">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4fcd3-129">See Also</span></span>  
 [<span data-ttu-id="4fcd3-130">İzlenecek Yol: MaskedTextBox Denetimiyle Çalışma</span><span class="sxs-lookup"><span data-stu-id="4fcd3-130">Walkthrough: Working with the MaskedTextBox Control</span></span>](../../../../docs/framework/winforms/controls/walkthrough-working-with-the-maskedtextbox-control.md)
