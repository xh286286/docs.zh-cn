---
title: ISymUnmanagedAsyncMethod::GetKickoffMethod 方法
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
ms.openlocfilehash: 2d4515087812b2b7c9303228ac5e5bbf34e8aa91
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707186"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="eb3d8-102">ISymUnmanagedAsyncMethod::GetKickoffMethod 方法</span><span class="sxs-lookup"><span data-stu-id="eb3d8-102">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>

<span data-ttu-id="eb3d8-103">请参阅 [DefineKickoffMethod 方法](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)。</span><span class="sxs-lookup"><span data-stu-id="eb3d8-103">See [DefineKickoffMethod Method](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb3d8-104">语法</span><span class="sxs-lookup"><span data-stu-id="eb3d8-104">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="eb3d8-105">参数</span><span class="sxs-lookup"><span data-stu-id="eb3d8-105">Parameters</span></span>  
  
|<span data-ttu-id="eb3d8-106">参数</span><span class="sxs-lookup"><span data-stu-id="eb3d8-106">Parameter</span></span>|<span data-ttu-id="eb3d8-107">说明</span><span class="sxs-lookup"><span data-stu-id="eb3d8-107">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="eb3d8-108">返回值</span><span class="sxs-lookup"><span data-stu-id="eb3d8-108">Return Value</span></span>  

 <span data-ttu-id="eb3d8-109">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="eb3d8-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eb3d8-110">要求</span><span class="sxs-lookup"><span data-stu-id="eb3d8-110">Requirements</span></span>  

 <span data-ttu-id="eb3d8-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="eb3d8-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb3d8-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb3d8-112">See also</span></span>

- [<span data-ttu-id="eb3d8-113">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="eb3d8-113">ISymUnmanagedAsyncMethod Interface</span></span>](isymunmanagedasyncmethod-interface.md)
