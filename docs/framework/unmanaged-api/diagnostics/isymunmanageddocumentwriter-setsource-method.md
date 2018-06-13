---
title: ISymUnmanagedDocumentWriter::SetSource Yöntemi
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocumentWriter.SetSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocumentWriter::SetSource
helpviewer_keywords:
- ISymUnmanagedDocumentWriter::SetSource method [.NET Framework debugging]
- SetSource method [.NET Framework debugging]
ms.assetid: ea5b9d9f-ff06-4bd3-8de5-6435343aba59
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f25f66d7092c50247e24051280eaa7b714297c20
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33424423"
---
# <a name="isymunmanageddocumentwritersetsource-method"></a><span data-ttu-id="199a9-102">ISymUnmanagedDocumentWriter::SetSource Yöntemi</span><span class="sxs-lookup"><span data-stu-id="199a9-102">ISymUnmanagedDocumentWriter::SetSource Method</span></span>
<span data-ttu-id="199a9-103">Yazılmakta bir belgeyi katıştırılmış kaynağı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="199a9-103">Sets embedded source for a document that is being written.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="199a9-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="199a9-104">Syntax</span></span>  
  
```  
HRESULT SetSource(  
    [in]  ULONG32  sourceSize,  
    [in, size_is(sourceSize)] BYTE  source[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="199a9-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="199a9-105">Parameters</span></span>  
 `sourceSize`  
 <span data-ttu-id="199a9-106">[in] A `ULONG32` boyutunu içeren `source` arabellek.</span><span class="sxs-lookup"><span data-stu-id="199a9-106">[in] A `ULONG32` that contains the size of the `source` buffer.</span></span>  
  
 `source`  
 <span data-ttu-id="199a9-107">[in] Katıştırılmış kaynak depolayan bir arabellek.</span><span class="sxs-lookup"><span data-stu-id="199a9-107">[in] The buffer that stores the embedded source.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="199a9-108">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="199a9-108">Return Value</span></span>  
 <span data-ttu-id="199a9-109">Yöntem başarılı olursa S_OK; Aksi takdirde E_FAIL veya başka bir hata kodu.</span><span class="sxs-lookup"><span data-stu-id="199a9-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="199a9-110">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="199a9-110">Requirements</span></span>  
 <span data-ttu-id="199a9-111">**Başlık:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="199a9-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="199a9-112">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="199a9-112">See Also</span></span>  
 [<span data-ttu-id="199a9-113">ISymUnmanagedDocumentWriter Arabirimi</span><span class="sxs-lookup"><span data-stu-id="199a9-113">ISymUnmanagedDocumentWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocumentwriter-interface.md)
