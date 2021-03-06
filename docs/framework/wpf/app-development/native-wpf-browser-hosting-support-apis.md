---
title: Destek API'leri Barındıran Yerel WPF Tarayıcısı
ms.date: 03/30/2017
f1_keywords:
- AutoGeneratedOrientationPage
helpviewer_keywords:
- browser hosting support [WPF]
- WPF browser hosting support APIs [WPF]
ms.assetid: 82c133a8-d760-45fb-a2b9-3a997537f1d4
ms.openlocfilehash: f542da55b6cde2d140e1f9f391e6b2f3d6fe172f
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43863741"
---
# <a name="native-wpf-browser-hosting-support-apis"></a>Destek API'leri Barındıran Yerel WPF Tarayıcısı
Barındırılmasını [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] uygulamalarının Web tarayıcılarında dışında WPF konağı kayıtlı olan etkin belge sunucusu (DocObject olarak da bilinir) barındırılması. [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] etkinleştirebilir doğrudan ve etkin bir belge ile tümleştirin. XBAP ve gevşek XAML belgeleri Mozilla tarayıcılarda barındırmak için [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] benzer bir barındırma ortamı sağlayan NPAPI eklentisi sağlar [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] etkin belge sunucusu olarak [!INCLUDE[TLA2#tla_ie](../../../../includes/tla2sharptla-ie-md.md)] yapar. Ancak, diğer tarayıcılarda XBAP'ler ve XAML barındırmak için pratik en kolay yolu belgeleri ve tek başına uygulamalar Internet Explorer Web tarayıcı denetimi. Web tarayıcı denetimi karmaşık etkin belge sunucusu barındırma ortamı sağlar, ancak özelleştirmek ve bu ortamda genişletmek ve geçerli etkin belgeyi nesne ile doğrudan iletişim kurmak kendi konak sağlar.  
  
 [!INCLUDE[TLA#tla_titlewinclient](../../../../includes/tlasharptla-titlewinclient-md.md)] Etkin belge sunucusu da dahil olmak üzere birkaç ortak barındırma arabirimleri uygulayan [IOleObject](https://go.microsoft.com/fwlink/?LinkId=162049), [IOleDocument](https://go.microsoft.com/fwlink/?LinkId=162050), [IOleInPlaceActiveObject](https://go.microsoft.com/fwlink/?LinkId=162051), [IPersistMoniker](https://go.microsoft.com/fwlink/?LinkId=162045), [IOleCommandTarget](https://go.microsoft.com/fwlink/?LinkId=162047). Web tarayıcı denetimi barındırıldığında, bu arabirimleri tarafından döndürülen nesne sorgularından olabilir [Iwebbrowser2::belge](https://go.microsoft.com/fwlink/?LinkId=162048) özelliği.  
  
## <a name="iolecommandtarget"></a>IOleCommandTarget  
 Etkin belge WPF sunucusunun [IOleCommandTarget](https://go.microsoft.com/fwlink/?LinkId=162047) standart OLE komut grubuyla (null komut grubu GUID) çok sayıda Gezinti ilgili ve tarayıcı özel komutları destekler. Ayrıca, CGID_PresentationHost adlı özel bir komut grubunu algılar. Şu anda, bu grup içinde tanımlanmış tek bir komut yoktur.  
  
```  
DEFINE_GUID(CGID_PresentationHost, 0xd0288c55, 0xd6, 0x4f5e, 0xa8, 0x51, 0x79, 0xde, 0xc5, 0x1b, 0x10, 0xec);  
enum PresentationHostCommands {   
   PHCMDID_TABINTO = 1   
};  
```  
  
 PHCMDID_TABINTO SHIFT tuşunun durumunu bağlı olarak, içeriği ilk veya son odaklanabilir öğesine odak geçiş bildirir.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [IEnumRAWINPUTDEVICE](../../../../docs/framework/wpf/app-development/ienumrawinputdevice.md)  
 [IWpfHostSupport](../../../../docs/framework/wpf/app-development/iwpfhostsupport.md)
