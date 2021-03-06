---
title: .NET Core ve Visual Studio 2017'de C# ile bir Hello World uygulaması oluşturma
description: Visual Studio 2017 kullanarak C# ile basit bir .NET Core konsol uygulaması oluşturmayı öğrenin.
author: BillWagner
ms.author: wiwagn
ms.date: 09/13/2017
ms.custom: vs-dotnet
ms.openlocfilehash: 031c0a433391fbe4cdd40f6ce648f476787baf48
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46003028"
---
# <a name="build-a-c-hello-world-application-with-net-core-in-visual-studio-2017"></a>Visual Studio 2017'de .NET Core ile bir C# Merhaba Dünya uygulaması derleme

Bu konuda, derleme, hata ayıklama ve C# kullanarak Visual Studio 2017'de basit bir .NET Core konsol uygulaması yayımlama için adım adım bir giriş sağlar. Visual Studio 2017, .NET Core uygulamaları oluşturmaya yönelik tam özellikli bir geliştirme ortamı sağlar. Uygulama, platforma özel bağımlılıklar yok sürece, uygulama, .NET Core hedefleyen herhangi bir platformda çalışabilir ve .NET Core sahip herhangi bir sistemde yüklü.

## <a name="prerequisites"></a>Önkoşullar

[Visual Studio 2017](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs) yüklü ".NET Core çoklu platform geliştirme" iş yüküyle birlikte sağlanır. .NET Core 1.1 veya .NET Core 2.0 ile uygulamanızı geliştirebilirsiniz.

Daha fazla bilgi için [Windows üzerinde .NET Core önkoşulları](../../core/windows-prerequisites.md) konu.

## <a name="a-simple-hello-world-application"></a>Basit bir Hello World uygulaması

Basit bir "Hello World" konsol uygulaması oluşturarak başlayın. Aşağıdaki adımları uygulayın:

1. Visual Studio 2017'yi başlatın. Seçin **dosya** > **yeni** > **proje** menü çubuğundan. İçinde *yeni proje** iletişim kutusunda **Visual C#** düğümünü ve ardından **.NET Core** düğümü. Ardından **konsol uygulaması (.NET Core)** proje şablonu. İçinde **adı** metin kutusunda, "HelloWorld" yazın. Seçin **Tamam** düğmesi.

   ![Seçilen konsol uygulaması ile yeni proje iletişim kutusu](./media/with-visual-studio/newproject.png)
   
1. Visual Studio, projenizi oluşturmak için şablon kullanır. .NET Core için C# konsol uygulaması şablonu otomatik olarak bir sınıf tanımlar `Program`, tek bir yöntemi olan `Main`, alan bir <xref:System.String> bağımsız değişken olarak bir dizi. `Main` uygulama başlatıldığında otomatik olarak çalışma zamanı tarafından çağrılır yöntemi uygulama giriş noktası niteliğindedir. Uygulama başlatıldığında sağlanan komut satırı bağımsız değişkenleri kullanılabilir *args* dizisi.

   ![Visual Studio ve yeni HelloWorld proje](./media/with-visual-studio/devenv.png)

   Şablon, basit bir "Hello World" uygulaması oluşturur. Çağrı <xref:System.Console.WriteLine(System.String)?displayProperty=nameWithType> "Hello World!" sabit dizesini görüntülemek için yöntemi Konsol penceresinde. Seçerek **HelloWorld** düğme araç çubuğundaki yeşil ok ile programın hata ayıklama modunda çalıştırabilir. Bunu yaparsanız, kapatılmadan önce konsol penceresi yalnızca kısa bir zaman aralığı için görülebilir. Bu durum oluşur `Main` yöntemi sonlandırır ve uygulama aşağıdaki tek deyimde olan en kısa sürede sona `Main` yöntemini yürütür.

1. Konsol penceresinde kapatılmadan önce beklenecek Uygulanmanın için çağırdıktan hemen sonra aşağıdaki kodu ekleyin <xref:System.Console.WriteLine(System.String)?displayProperty=nameWithType> yöntemi:

   ```csharp
   Console.Write("Press any key to continue...");
   Console.ReadKey(true);
   ```
   Bu kod, herhangi bir tuşa basın ister ve daha sonra bir tuşa basıldığında kadar program duraklatılır.

1. Menü çubuğunda, seçin **derleme** > **Çözümü Derle**. Bu, just-in-time (JIT) derleyici tarafından ikili koda dönüştürülür bir ara dile (IL) programınızı derler.

1. Programı çalıştırmayı seçerek tarafından **HelloWorld** araç çubuğundaki yeşil bir ok düğmesi.

   ![Devam etmek için herhangi bir tuşa Hello World tuşuna gösteren konsol penceresi](./media/with-visual-studio/helloworld1.png)

1. Konsol penceresini kapatmak için herhangi bir tuşa basın.

## <a name="enhancing-the-hello-world-application"></a>Hello World uygulaması geliştirme

Kullanıcıdan kendi ad ve tarih ve saat ile birlikte görüntülemek için uygulama geliştirin. Program sınama ve değiştirmek için aşağıdakileri yapın:

1. Aşağıdaki C# kodunu hemen izleyen açma ayracı sonra kod penceresinde girin `static void Main(string[] args)` satır ve ilk ayraç önce:

   [!code-csharp[GettingStarted#1](../../../samples/snippets/csharp/getting_started/with_visual_studio/helloworld.cs#1)]

   Bu kodu varolan değiştirir <xref:System.Console.WriteLine%2A?displayProperty=nameWithType>, <xref:System.Console.Write%2A?displayProperty=nameWithType>, ve <xref:System.Console.ReadKey%2A?displayProperty=nameWithType> deyimleri.

   ![Visual Studio Program c-sharp dosyası ile güncelleştirilmiş Main yöntemi](./media/with-visual-studio/codewindow.png)

   Bu kod, "Adınız ne?" görüntüler. Kullanıcı kadar bekler ve konsol penceresinde Enter tuşuna basın, bir dize girer. Bu dize adlı bir değişkende depoladığı `name`. Ayrıca bir değeri alır <xref:System.DateTime.Now?displayProperty=nameWithType> geçerli yerel saat içerir ve adlı bir değişkene atar özelliği `date`. Son olarak, bunu kullanan bir [ilişkilendirilmiş bir dizedir](../../csharp/language-reference/tokens/interpolated.md) bu değerleri konsol penceresinde görüntüler.

1. Program seçerek derleme **derleme** > **Çözümü Derle**.

1. Araç çubuğundaki yeşil oku seçerek, F5 tuşuna basarak veya seçerek Visual Studio'da hata ayıklama modunda programı çalıştırın **hata ayıklama** > **hata ayıklamayı Başlat** menü öğesi. Bir ad girmeniz ve Enter tuşuna basarak istemine yanıt.

   ![Konsol penceresi ile değiştirilmiş program çıktısı](./media/with-visual-studio/helloworld2.png)

1. Konsol penceresini kapatmak için herhangi bir tuşa basın.

Oluşturduğunuz ve uygulamanızı çalıştırın. Profesyonel uygulama geliştirmek için uygulamanız yayımlanmaya hazır hale getirmek için bazı ek adımlar uygulayın:

- Uygulamanızı hata ayıklama hakkında daha fazla bilgi için bkz: [Visual Studio 2017 ile C# Merhaba Dünya uygulamanızın hatalarını ayıklama](debugging-with-visual-studio.md).

- Geliştirme ve uygulamanızın dağıtılabilir bir sürümünü yayımlama hakkında daha fazla bilgi için bkz: [Visual Studio 2017 ile C# Merhaba Dünya uygulamanızı yayımlama](publishing-with-visual-studio.md).

## <a name="related-topics"></a>İlgili konular

Bir konsol uygulaması yerine bir sınıf kitaplığı ile .NET Core ve Visual Studio 2017'de oluşturabilirsiniz. Adım adım bir giriş için bkz. [C# ve Visual Studio 2017'de .NET Core ile bir sınıf kitaplığı oluşturma](library-with-visual-studio.md).

Mac, Linux ve Windows üzerinde .NET Core konsol uygulaması kullanarak da geliştirebilirsiniz [Visual Studio Code](https://code.visualstudio.com/), indirilebilir Kod Düzenleyicisi. Adım adım bir öğretici için bkz [Visual Studio Code ile çalışmaya başlama](with-visual-studio-code.md).
