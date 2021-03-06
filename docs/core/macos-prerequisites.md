---
title: Mac üzerinde .NET Core için Önkoşullar
description: MacOS sürümleri ve geliştirme, dağıtma ve macOS makinelerinde .NET Core uygulamaları çalıştırmak için .NET Core bağımlılıklar desteklenmiyor.
author: guardrex
ms.author: mairaw
ms.date: 10/03/2018
ms.openlocfilehash: b5b3c6ea90a2cc4487e849af468d324b645834af
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48584084"
---
# <a name="prerequisites-for-net-core-on-macos"></a>MacOS üzerinde .NET Core için Önkoşullar

Bu makalede desteklenen macOS sürümleri ve geliştirme, dağıtma ve macOS makinelerinde .NET Core uygulamaları çalıştırmak için ihtiyacınız olan .NET Core bağımlılıkları gösterir. Desteklenen işletim sistemi sürümleri ve bağımlılıklarını izleyen bir Mac üzerinde .NET Core uygulamaları geliştirme üç yoldan uygulamak: aracılığıyla [komut satırı ile tercih ettiğiniz düzenleyiciyi](tutorials/using-with-xplat-cli.md), [Visual Studio Code](https://code.visualstudio.com/)ve [Mac için visual Studio](https://visualstudio.microsoft.com/vs/visual-studio-mac/).

## <a name="supported-macos-versions"></a>Desteklenen macOS sürümleri

# <a name="net-core-2xtabnetcore2x"></a>[.NET core 2.x](#tab/netcore2x)

.NET core 2.x, aşağıdaki macOS sürümlerinde desteklenir:

* macOS 10.12 "Sierra" ve sonraki sürümler

Bkz: [.NET Core 2.x desteklenen işletim sistemi sürümleri](https://github.com/dotnet/core/blob/master/release-notes/2.1/2.1-supported-os.md) .NET Core tam listesi için 2.x desteklenen işletim sistemleri, destek işletim sistemi sürümleri ve yaşam döngüsü ilkesi bağlantılar dışında.

# <a name="net-core-1xtabnetcore1x"></a>[.NET core 1.x](#tab/netcore1x)

.NET core 1.x macOS üzerinde aşağıdaki sürümleri desteklenir:

* macOS 10.12 "Sierra"
* macOS 10.11 "El Capitan"

Bkz: [.NET Core 1.x desteklenen işletim sistemi sürümleri](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0-supported-os.md) .NET Core tam listesi için 1.x desteklenen işletim sistemleri, destek işletim sistemi sürümleri ve yaşam döngüsü ilkesi bağlantılar dışında.

---

## <a name="net-core-dependencies"></a>.NET core bağımlılıkları

# <a name="net-core-2xtabnetcore2x"></a>[.NET core 2.x](#tab/netcore2x)

.NET Core SDK'sından yükleyip [.NET indirir](https://www.microsoft.com/net/download/core). Macos'ta yükleme ile ilgili sorunlar varsa, başvurun [bilinen sorunlar](https://github.com/dotnet/core/tree/master/release-notes/2.1) yüklü olan sürüm için konu.

# <a name="net-core-1xtabnetcore1x"></a>[.NET core 1.x](#tab/netcore1x)

**.NET core 1.x**

.NET core 1.x macOS üzerinde çalışırken OpenSSL gerektirir. OpenSSL almak için kolay bir yol kullanmaktır [Homebrew ("brew")](https://brew.sh/) macOS için Paket Yöneticisi. Yükledikten sonra *brew*, OpenSSL Terminal (komut) isteminde aşağıdaki komutları çalıştırarak yükleyin:

```console
brew update
brew install openssl
mkdir -p /usr/local/lib
ln -s /usr/local/opt/openssl/lib/libcrypto.1.0.0.dylib /usr/local/lib/
ln -s /usr/local/opt/openssl/lib/libssl.1.0.0.dylib /usr/local/lib/
```

.NET Core SDK'sından yükleyip [.NET indirir](https://www.microsoft.com/net/download/core). Macos'ta yükleme ile ilgili sorunlar varsa, başvurun [1.0.0 bilinen sorunlar](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.0-known-issues.md) ve [1.0.1 bilinen sorunlar](https://github.com/dotnet/core/blob/master/release-notes/1.0/1.0.1-known-issues.md) konuları.

---

## <a name="increase-the-maximum-open-file-limit-net-core-versions-before-net-core-sdk-202"></a>(.NET Core sürümleri .NET Core SDK'sı 2.0.2 önce) en fazla açık dosya sınırını artırın 

(Önce .NET Core SDK 2.0.2) daha eski .NET Core sürümlerinde varsayılan açık dosya sınırı macos'ta projeleri geri yükleme veya birim testleri çalıştırma gibi bazı .NET Core iş yükleri için yeterli olmayabilir.

Aşağıdaki adımları izleyerek bu sınırı artırabilirsiniz:

1. Bir metin düzenleyicisi kullanarak yeni bir dosya oluşturun _/Library/LaunchDaemons/limit.maxfiles.plist_, söz konusu içeriklerle dosyayı kaydedin:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN"
        "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
  <dict>
    <key>Label</key>
    <string>limit.maxfiles</string>
    <key>ProgramArguments</key>
    <array>
      <string>launchctl</string>
      <string>limit</string>
      <string>maxfiles</string>
      <string>2048</string>
      <string>4096</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
    <key>ServiceIPC</key>
    <false/>
  </dict>
</plist>
```

2. Bir terminal penceresinde aşağıdaki komutu çalıştırın:

```console
echo 'ulimit -n 2048' | sudo tee -a /etc/profile
```

3. Mac'iniz, bu ayarları uygulamak için yeniden başlatın.

## <a name="visual-studio-for-mac"></a>Mac için Visual Studio

.NET Core SDK'sını kullanarak .NET Core uygulamaları geliştirmek için herhangi bir düzenleyici kullanabilirsiniz. Ancak, bir tümleşik geliştirme ortamında bir Mac üzerinde .NET Core uygulamaları geliştirmek istiyorsanız, kullanabileceğiniz [Mac için Visual Studio](https://visualstudio.microsoft.com/vs/visual-studio-mac/). 

Mac için Visual Studio ile macOS üzerinde .NET core geliştirme gerektirir:

* MacOS işletim sisteminin desteklenen bir sürümü
* OpenSSL (.NET Core 1.x yalnızca; .NET Core 2.x kullandığı güvenlik hizmetleri yerel olarak macOS kullanılabilir)
* .NET core SDK'sı Mac için
* [Mac için Visual Studio](https://visualstudio.microsoft.com/vs/visual-studio-mac/)
