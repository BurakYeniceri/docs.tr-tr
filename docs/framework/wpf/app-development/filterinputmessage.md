---
title: FilterInputMessage
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- raw input [WPF]
- FilterInputMessage method [WPF]
ms.assetid: 4d74c6cf-7d1d-49ff-96c1-231340ce54f5
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 6b3a0e58c7485d46f004db7ea52215be60340b68
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2017
---
# <a name="filterinputmessage"></a><span data-ttu-id="4ed9e-102">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="4ed9e-102">FilterInputMessage</span></span>
<span data-ttu-id="4ed9e-103">E_NOTIMPL sürece bir ileti alındığında PresentationHost.exe tarafından çağrılır.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-103">Called by PresentationHost.exe whenever a message is received unless E_NOTIMPL is returned.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ed9e-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="4ed9e-104">Syntax</span></span>  
  
```  
HRESULT FilterInputMessage( [in] MSG* pMsg ) ;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4ed9e-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="4ed9e-105">Parameters</span></span>  
 `pMsg`  
  
 <span data-ttu-id="4ed9e-106">[in] Ham giriş alma penceresine WM_INPUT iletisi gönderdi.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-106">[in] The WM_INPUT message sent to the window that is getting raw input.</span></span>  
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4ed9e-107">Özellik Değeri/Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="4ed9e-107">Property Value/Return Value</span></span>  
 <span data-ttu-id="4ed9e-108">HRESULT:</span><span class="sxs-lookup"><span data-stu-id="4ed9e-108">HRESULT:</span></span>  
  
 <span data-ttu-id="4ed9e-109">S_OK - filtre iletiyi işlemedi ve başka bir işleme ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-109">S_OK - The filter did not process the message and further processing may occur.</span></span>  
  
 <span data-ttu-id="4ed9e-110">S_FALSE - filtre bu ileti işleme ve başka işlem olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-110">S_FALSE - The filter processed this message and no further processing should occur.</span></span>  
  
 <span data-ttu-id="4ed9e-111">Bu değeri döndürülürse, E_NOTIMPL – [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md) yeniden çağrılmaz.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-111">E_NOTIMPL – If this value is returned, [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md) is not called again.</span></span> <span data-ttu-id="4ed9e-112">Bu yalnızca özel ilerleme sağlanmasıyla ilgilenen bir konak uygulamasından döndürülen ve hata kullanıcı arabirimlerinin PresentationHost.exe değil ilgileniyor ham giriş iletilerini PresentationHost.exe iletilen.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-112">This might be returned from a host application that is only interested in providing custom progress and error user interfaces to PresentationHost.exe is not interested in being forwarded raw input messages from PresentationHost.exe.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4ed9e-113">Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="4ed9e-113">Remarks</span></span>  
 <span data-ttu-id="4ed9e-114">PresentationHost.exe klavye, fare ve Uzaktan denetimler de dahil olmak üzere çeşitli ham giriş aygıtlarının hedefidir.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-114">PresentationHost.exe is the target of various raw input devices, including keyboard, mice, and remote controls.</span></span> <span data-ttu-id="4ed9e-115">Bazı durumlarda, ana bilgisayar uygulamasını davranışını PresentationHost.exe tarafından tüketilen giriş bağımlıdır.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-115">Sometimes, behavior in the host application is dependent on input that would otherwise be consumed by PresentationHost.exe.</span></span> <span data-ttu-id="4ed9e-116">Örneğin, bir ana bilgisayar uygulaması belirli kullanıcı arabirimi öğeleri kullanılıp kullanılmayacağını belirlemek için belirli giriş iletilerinin alınmasına bağlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-116">For example, a host application may depend on receiving certain input messages to determine whether or not to display specific user interface elements.</span></span>  
  
 <span data-ttu-id="4ed9e-117">Ana bilgisayar uygulamasının bu davranışların sağlamak için gerekli giriş iletilerini almasına izin vermek için PresentationHost.exe barındırılan uygulama için uygun ham giriş iletilerini çağırarak iletir [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md).</span><span class="sxs-lookup"><span data-stu-id="4ed9e-117">To allow the host application to receive the necessary input messages to provide these behaviors, PresentationHost.exe forwards appropriate raw input messages to the hosted application by calling [FilterInputMessage](../../../../docs/framework/wpf/app-development/filterinputmessage.md).</span></span>  
  
 <span data-ttu-id="4ed9e-118">Barındırılan uygulama tarafından döndürülen ham giriş aygıtları (İnsan Arabirimi aygıtları) kümesi ile kaydederek ham giriş iletilerini alır [GetRawInputDevices](../../../../docs/framework/wpf/app-development/getrawinputdevices.md).</span><span class="sxs-lookup"><span data-stu-id="4ed9e-118">The hosted application receives raw input messages by registering with the set of raw input devices (Human Interface Devices) returned by [GetRawInputDevices](../../../../docs/framework/wpf/app-development/getrawinputdevices.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ed9e-119">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="4ed9e-119">See Also</span></span>  
 [<span data-ttu-id="4ed9e-120">WM_INPUT Bildirimi</span><span class="sxs-lookup"><span data-stu-id="4ed9e-120">WM_INPUT Notification</span></span>](http://msdn.microsoft.com/library/default.asp?url=/library/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputmessages/wm_input.asp)
