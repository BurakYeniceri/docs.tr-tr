---
title: ISymUnmanagedDocument::GetSourceLength Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedDocument.GetSourceLength
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedDocument::GetSourceLength
helpviewer_keywords:
- GetSourceLength method [.NET Framework debugging]
- ISymUnmanagedDocument::GetSourceLength method [.NET Framework debugging]
ms.assetid: e087dbbb-f4fb-4fbe-8292-e4f1a14d0df2
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 61d9bd99a08f428993f38fb5b6889c9659607782
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanageddocumentgetsourcelength-method"></a><span data-ttu-id="566f5-102">ISymUnmanagedDocument::GetSourceLength Metodu</span><span class="sxs-lookup"><span data-stu-id="566f5-102">ISymUnmanagedDocument::GetSourceLength Method</span></span>
<span data-ttu-id="566f5-103">Katıştırılmış kaynak bayt cinsinden uzunluğu alır.</span><span class="sxs-lookup"><span data-stu-id="566f5-103">Gets the length, in bytes, of the embedded source.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="566f5-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="566f5-104">Syntax</span></span>  
  
```  
HRESULT GetSourceLength(  
    [out, retval]  ULONG32*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="566f5-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="566f5-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="566f5-106">[out] Bayt cinsinden uzunluğu katıştırılmış kaynak gösteren bir değişken için bir işaretçi.</span><span class="sxs-lookup"><span data-stu-id="566f5-106">[out] A pointer to a variable that indicates the length, in bytes, of the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="566f5-107">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="566f5-107">Return Value</span></span>  
 <span data-ttu-id="566f5-108">Yöntem başarılı olursa S_OK.</span><span class="sxs-lookup"><span data-stu-id="566f5-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="566f5-109">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="566f5-109">See Also</span></span>  
 [<span data-ttu-id="566f5-110">ISymUnmanagedDocument Arabirimi</span><span class="sxs-lookup"><span data-stu-id="566f5-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
