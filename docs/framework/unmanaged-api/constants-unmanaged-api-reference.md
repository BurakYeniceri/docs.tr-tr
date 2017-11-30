---
title: "Sabitler (Yönetilmeyen API Başvurusu)"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
helpviewer_keywords:
- constants for unmanaged API [.NET Framework]
- native API reference [.NET Framework], constants
- unmanaged API reference [.NET Framework], constants
ms.assetid: 77526f65-b71c-4483-9d19-3a3751fd8a45
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 45e4d41c16695010dc452d2f22850d43f885974a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="constants-unmanaged-api-reference"></a><span data-ttu-id="1a188-102">Sabitler (Yönetilmeyen API Başvurusu)</span><span class="sxs-lookup"><span data-stu-id="1a188-102">Constants (Unmanaged API Reference)</span></span>
<span data-ttu-id="1a188-103">Bu konu, dil türü, dil satıcı ve CorSym.idl içinde tanımlanan belge türü sabitleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="1a188-103">This topic describes the language type, language vendor, and document type constants that are defined in CorSym.idl.</span></span>  
  
## <a name="language-type-constants"></a><span data-ttu-id="1a188-104">Dil türü sabitleri</span><span class="sxs-lookup"><span data-stu-id="1a188-104">Language Type Constants</span></span>  
 <span data-ttu-id="1a188-105">Aşağıdaki tabloda dil programlama dillerini belirleyin GUID'ler temsil türü sabitleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-105">The following table shows language type constants, which represent GUIDs that identify programming languages.</span></span>  
  
|<span data-ttu-id="1a188-106">Simgesi</span><span class="sxs-lookup"><span data-stu-id="1a188-106">Symbol</span></span>|<span data-ttu-id="1a188-107">Açıklama</span><span class="sxs-lookup"><span data-stu-id="1a188-107">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="1a188-108">CorSym_LanguageType_C</span><span class="sxs-lookup"><span data-stu-id="1a188-108">CorSym_LanguageType_C</span></span>|<span data-ttu-id="1a188-109">C dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-109">Indicates the C language.</span></span>|  
|<span data-ttu-id="1a188-110">CorSym_LanguageType_CPlusPlus</span><span class="sxs-lookup"><span data-stu-id="1a188-110">CorSym_LanguageType_CPlusPlus</span></span>|<span data-ttu-id="1a188-111">C++ dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a188-111">Indicates the C++ language.</span></span>|  
|<span data-ttu-id="1a188-112">CorSym_LanguageType_CSharp</span><span class="sxs-lookup"><span data-stu-id="1a188-112">CorSym_LanguageType_CSharp</span></span>|<span data-ttu-id="1a188-113">C# dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a188-113">Indicates the C# language.</span></span>|  
|<span data-ttu-id="1a188-114">CorSym_LanguageType_Basic</span><span class="sxs-lookup"><span data-stu-id="1a188-114">CorSym_LanguageType_Basic</span></span>|<span data-ttu-id="1a188-115">Temel dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-115">Indicates the Basic language.</span></span>|  
|<span data-ttu-id="1a188-116">CorSym_LanguageType_Java</span><span class="sxs-lookup"><span data-stu-id="1a188-116">CorSym_LanguageType_Java</span></span>|<span data-ttu-id="1a188-117">Java dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-117">Indicates the Java language.</span></span>|  
|<span data-ttu-id="1a188-118">CorSym_LanguageType_Cobol</span><span class="sxs-lookup"><span data-stu-id="1a188-118">CorSym_LanguageType_Cobol</span></span>|<span data-ttu-id="1a188-119">COBOL dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-119">Indicates the COBOL language.</span></span>|  
|<span data-ttu-id="1a188-120">CorSym_LanguageType_Pascal</span><span class="sxs-lookup"><span data-stu-id="1a188-120">CorSym_LanguageType_Pascal</span></span>|<span data-ttu-id="1a188-121">Pascal dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-121">Indicates the Pascal language.</span></span>|  
|<span data-ttu-id="1a188-122">CorSym_LanguageType_ILAssembly</span><span class="sxs-lookup"><span data-stu-id="1a188-122">CorSym_LanguageType_ILAssembly</span></span>|<span data-ttu-id="1a188-123">Microsoft Ara dili (MSIL) bütünleştirilmiş kodu gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-123">Indicates the Microsoft intermediate language (MSIL) assembly code.</span></span>|  
|<span data-ttu-id="1a188-124">CorSym_LanguageType_JScript</span><span class="sxs-lookup"><span data-stu-id="1a188-124">CorSym_LanguageType_JScript</span></span>|<span data-ttu-id="1a188-125">JScript dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-125">Indicates the JScript language.</span></span>|  
|<span data-ttu-id="1a188-126">CorSym_LanguageType_SMC</span><span class="sxs-lookup"><span data-stu-id="1a188-126">CorSym_LanguageType_SMC</span></span>|<span data-ttu-id="1a188-127">SMC dili gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-127">Indicates the SMC language.</span></span>|  
|<span data-ttu-id="1a188-128">CorSym_LanguageType_MCPlusPlus</span><span class="sxs-lookup"><span data-stu-id="1a188-128">CorSym_LanguageType_MCPlusPlus</span></span>|<span data-ttu-id="1a188-129">.NET Framework için etkin C++ dili belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a188-129">Indicates the C++ language enabled for the .NET Framework.</span></span>|  
  
## <a name="language-vendor-constants"></a><span data-ttu-id="1a188-130">Dil satıcı sabitleri</span><span class="sxs-lookup"><span data-stu-id="1a188-130">Language Vendor Constants</span></span>  
 <span data-ttu-id="1a188-131">Aşağıdaki tabloda dil programlama dili satıcıları tanımlamak GUID'ler temsil eden satıcı sabitleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-131">The following table shows language vendor constants, which represent GUIDs that identify programming language vendors.</span></span>  
  
|<span data-ttu-id="1a188-132">Simgesi</span><span class="sxs-lookup"><span data-stu-id="1a188-132">Symbol</span></span>|<span data-ttu-id="1a188-133">Açıklama</span><span class="sxs-lookup"><span data-stu-id="1a188-133">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="1a188-134">CorSym_LanguageVendor_Microsoft</span><span class="sxs-lookup"><span data-stu-id="1a188-134">CorSym_LanguageVendor_Microsoft</span></span>|<span data-ttu-id="1a188-135">Microsoft gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-135">Indicates Microsoft.</span></span>|  
  
## <a name="document-type-constants"></a><span data-ttu-id="1a188-136">Belge türü sabitleri</span><span class="sxs-lookup"><span data-stu-id="1a188-136">Document Type Constants</span></span>  
 <span data-ttu-id="1a188-137">Aşağıdaki tabloda belge belge türlerini tanımlamak GUID'ler temsil türü sabitleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-137">The following table shows document type constants, which represent GUIDs that identify document types.</span></span>  
  
|<span data-ttu-id="1a188-138">Simgesi</span><span class="sxs-lookup"><span data-stu-id="1a188-138">Symbol</span></span>|<span data-ttu-id="1a188-139">Açıklama</span><span class="sxs-lookup"><span data-stu-id="1a188-139">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="1a188-140">CorSym_DocumentType_Text</span><span class="sxs-lookup"><span data-stu-id="1a188-140">CorSym_DocumentType_Text</span></span>|<span data-ttu-id="1a188-141">Bir metin belgesi gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-141">Indicates a text document.</span></span>|  
|<span data-ttu-id="1a188-142">CorSym_DocumentType_MC</span><span class="sxs-lookup"><span data-stu-id="1a188-142">CorSym_DocumentType_MC</span></span>|<span data-ttu-id="1a188-143">Bir metin dışı belge gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a188-143">Indicates a non-text document.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="1a188-144">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="1a188-144">See Also</span></span>  
 [<span data-ttu-id="1a188-145">Yönetilmeyen API Başvurusu</span><span class="sxs-lookup"><span data-stu-id="1a188-145">Unmanaged API Reference</span></span>](../../../docs/framework/unmanaged-api/index.md)