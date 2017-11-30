---
title: ISymUnmanagedReader2::GetMethodByVersionPreRemap Metodu
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedReader2.GetMethodByVersionPreRemap
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedReader2::GetMethodByVersionPreRemap
helpviewer_keywords:
- GetMethodByVersionPreRemap method [.NET Framework debugging]
- ISymUnmanagedReader2::GetMethodByVersionPreRemap method [.NET Framework debugging]
ms.assetid: 0d144ed4-bdb0-4cac-960c-cb90f4dca173
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 69a203424320a176cd285c23d98111e71709042a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedreader2getmethodbyversionpreremap-method"></a><span data-ttu-id="7a74f-102">ISymUnmanagedReader2::GetMethodByVersionPreRemap Metodu</span><span class="sxs-lookup"><span data-stu-id="7a74f-102">ISymUnmanagedReader2::GetMethodByVersionPreRemap Method</span></span>
<span data-ttu-id="7a74f-103">Bir simge okuyucu yöntemi, verilen bir yöntem belirteci ve Düzenle ve devam et sürüm numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="7a74f-103">Gets a symbol reader method, given a method token and an edit-and-continue version number.</span></span> <span data-ttu-id="7a74f-104">Sürüm numaraları 1'den başlar ve yöntemi Düzenle ve devam et bir işlemin sonucunda her değiştirildiğinde artırılır.</span><span class="sxs-lookup"><span data-stu-id="7a74f-104">Version numbers start at 1 and are incremented each time the method is changed as a result of an edit-and-continue operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7a74f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7a74f-105">Syntax</span></span>  
  
```  
HRESULT GetMethodByVersionPreRemap(  
    [in]  mdMethodDef token,  
    [in]  int version,  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7a74f-106">Parametreler</span><span class="sxs-lookup"><span data-stu-id="7a74f-106">Parameters</span></span>  
 `token`  
 <span data-ttu-id="7a74f-107">[in] Yöntem meta veri simgesi.</span><span class="sxs-lookup"><span data-stu-id="7a74f-107">[in] The method metadata token.</span></span>  
  
 `version`  
 <span data-ttu-id="7a74f-108">[in] Yöntem sürümü.</span><span class="sxs-lookup"><span data-stu-id="7a74f-108">[in] The method version.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="7a74f-109">[out] Bir işaretçi döndürülen [Isymunmanagedmethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) arabirimi.</span><span class="sxs-lookup"><span data-stu-id="7a74f-109">[out] A pointer to the returned [ISymUnmanagedMethod](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7a74f-110">Dönüş Değeri</span><span class="sxs-lookup"><span data-stu-id="7a74f-110">Return Value</span></span>  
 <span data-ttu-id="7a74f-111">Yöntem başarılı olursa S_OK; Aksi takdirde E_FAIL veya başka bir hata kodu.</span><span class="sxs-lookup"><span data-stu-id="7a74f-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7a74f-112">Gereksinimler</span><span class="sxs-lookup"><span data-stu-id="7a74f-112">Requirements</span></span>  
 <span data-ttu-id="7a74f-113">**Başlık:** CorSym.idl.</span><span class="sxs-lookup"><span data-stu-id="7a74f-113">**Header:** CorSym.idl.</span></span> <span data-ttu-id="7a74f-114">CorSym.h</span><span class="sxs-lookup"><span data-stu-id="7a74f-114">CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7a74f-115">Ayrıca Bkz.</span><span class="sxs-lookup"><span data-stu-id="7a74f-115">See Also</span></span>  
 [<span data-ttu-id="7a74f-116">Isymunmanagedreader2 arabirimi</span><span class="sxs-lookup"><span data-stu-id="7a74f-116">ISymUnmanagedReader2 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedreader2-interface.md)
