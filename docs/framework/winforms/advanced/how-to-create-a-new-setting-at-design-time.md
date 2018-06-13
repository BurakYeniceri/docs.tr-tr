---
title: 'Nasıl Yapılır: Tasarım Zamanında Yeni Ayar Oluşturma'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], design time
- application settings [Windows Forms], creating
ms.assetid: c5d60a66-6507-462f-a81f-e3bc0a804e16
ms.openlocfilehash: 618355948578bd8f15e8cf7bec6f599e3169b77a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33523773"
---
# <a name="how-to-create-a-new-setting-at-design-time"></a><span data-ttu-id="c8b3d-102">Nasıl Yapılır: Tasarım Zamanında Yeni Ayar Oluşturma</span><span class="sxs-lookup"><span data-stu-id="c8b3d-102">How To: Create a New Setting at Design Time</span></span>
<span data-ttu-id="c8b3d-103">Tasarım zamanında yeni bir ayar ayarları Tasarımcısını kullanarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-103">You can create a new setting at design time by using the Settings designer.</span></span> <span data-ttu-id="c8b3d-104">Ayarları Tasarımcısı yeni ayarları oluşturur ve bu ayarlar için özellikleri belirtin olanak tanıyan bir kılavuz stili arabirimidir.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-104">The Settings designer is a grid-style interface that allows you to create new settings and specify properties for those settings.</span></span> <span data-ttu-id="c8b3d-105">Ad, değer, türü ve yeni ayarlarınızı kapsamın belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-105">You must specify Name, Value, Type and Scope for your new settings.</span></span> <span data-ttu-id="c8b3d-106">Bir ayar oluşturulduktan sonra kodda erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-106">Once a setting is created, it is accessible in code.</span></span>  
  
### <a name="to-create-a-new-setting-at-design-time-in-c"></a><span data-ttu-id="c8b3d-107">C# tasarım zamanında yeni bir ayar oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="c8b3d-107">To create a new setting at design time in C#</span></span>  
  
1.  <span data-ttu-id="c8b3d-108">İçinde **Çözüm Gezgini**, genişletin **özellikleri** projenizin düğümü.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-108">In **Solution Explorer**, expand the **Properties** node of your project.</span></span>  
  
2.  <span data-ttu-id="c8b3d-109">Yeni bir ayar eklemek istediğiniz .settings dosyasını çift tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-109">Double-click the .settings file in which you want to add a new setting.</span></span> <span data-ttu-id="c8b3d-110">Bu dosya için varsayılan Settings.settings adıdır.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-110">The default name for this file is Settings.settings.</span></span>  
  
3.  <span data-ttu-id="c8b3d-111">Ayarları Tasarımcısı'nda adını, değeri, türü ve ayarınız kapsamın ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-111">In the Settings designer, set the Name, Value, Type, and Scope for your setting.</span></span> <span data-ttu-id="c8b3d-112">Her satırda tek bir ayar temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-112">Each row represents a single setting.</span></span>  
  
### <a name="to-create-a-new-setting-at-design-time-in-visual-basic"></a><span data-ttu-id="c8b3d-113">Visual Basic'te tasarım zamanında yeni bir ayar oluşturmak için</span><span class="sxs-lookup"><span data-stu-id="c8b3d-113">To create a new setting at design time in Visual Basic</span></span>  
  
1.  <span data-ttu-id="c8b3d-114">İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayın ve seçin **özellikleri**.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-114">In **Solution Explorer**, right-click your project node and choose **Properties**.</span></span>  
  
2.  <span data-ttu-id="c8b3d-115">İçinde **özellikleri** sayfasında, **ayarları** sekmesi.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-115">In the **Properties** page, select the **Settings** tab.</span></span>  
  
3.  <span data-ttu-id="c8b3d-116">Ayarları Tasarımcısı'nda adını, değeri, türü ve ayarınız kapsamın ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-116">In the Settings designer, set the Name, Value, Type, and Scope for your setting.</span></span> <span data-ttu-id="c8b3d-117">Her satırda tek bir ayar temsil eder.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-117">Each row represents a single setting.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8b3d-118">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="c8b3d-118">See Also</span></span>  
 [<span data-ttu-id="c8b3d-119">Uygulama Ayarları ve Kullanıcı Ayarlarını Kullanma</span><span class="sxs-lookup"><span data-stu-id="c8b3d-119">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)  
 [<span data-ttu-id="c8b3d-120">Uygulama Ayarlarına Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c8b3d-120">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)  
 [<span data-ttu-id="c8b3d-121">Nasıl yapılır: Tasarım Zamanında Mevcut Bir Ayarın Değerini Değiştirme</span><span class="sxs-lookup"><span data-stu-id="c8b3d-121">How To: Change the Value of an Existing Setting at Design Time</span></span>](../../../../docs/framework/winforms/advanced/how-to-change-the-value-of-an-existing-setting-at-design-time.md)
