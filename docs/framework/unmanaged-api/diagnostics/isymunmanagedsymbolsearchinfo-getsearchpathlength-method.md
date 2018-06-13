---
title: ISymUnmanagedSymbolSearchInfo::GetSearchPathLength Metodu
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetSearchPathLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength
helpviewer_keywords:
- GetSearchPathLength method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength method [.NET Framework debugging]
ms.assetid: 274e73cf-8333-47ba-ac12-70214e2b0112
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3ad2167ab26eaa8164233ab9566854417f78df29
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427876"
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpathlength-method"></a><span data-ttu-id="5acdb-102">ISymUnmanagedSymbolSearchInfo::GetSearchPathLength Metodu</span><span class="sxs-lookup"><span data-stu-id="5acdb-102">ISymUnmanagedSymbolSearchInfo::GetSearchPathLength Method</span></span>
<span data-ttu-id="5acdb-103">Arama yolu uzunluğunu alır.</span><span class="sxs-lookup"><span data-stu-id="5acdb-103">Gets the search path length.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5acdb-104">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="5acdb-104">Syntax</span></span>  
  
```  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="5acdb-105">Parametreler</span><span class="sxs-lookup"><span data-stu-id="5acdb-105">Parameters</span></span>  
 `pcchPath`  
 <span data-ttu-id="5acdb-106">[out] Bir işaretçi bir `ULONG32` karakter arama yol uzunluğu içermesi gerekir arabellek boyutunu alır.</span><span class="sxs-lookup"><span data-stu-id="5acdb-106">[out] A pointer to a `ULONG32` that receives the size, in characters, of the buffer required to contain the search path length.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5acdb-107">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="5acdb-107">Return Value</span></span>  
 <span data-ttu-id="5acdb-108">Yöntem başarılı olursa S_OK; Aksi takdirde E_FAIL veya başka bir hata kodu.</span><span class="sxs-lookup"><span data-stu-id="5acdb-108">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5acdb-109">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="5acdb-109">Requirements</span></span>  
 <span data-ttu-id="5acdb-110">**Başlık:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="5acdb-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5acdb-111">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="5acdb-111">See Also</span></span>  
 [<span data-ttu-id="5acdb-112">ISymUnmanagedSymbolSearchInfo Arabirimi</span><span class="sxs-lookup"><span data-stu-id="5acdb-112">ISymUnmanagedSymbolSearchInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedsymbolsearchinfo-interface.md)
