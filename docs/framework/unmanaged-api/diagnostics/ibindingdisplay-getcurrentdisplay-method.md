---
title: IBindingDisplay::GetCurrentDisplay 方法
ms.date: 03/30/2017
api_name:
- IBindingDisplay.GetCurrentDisplay
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IBindingDisplay::GetCurrentDisplay
helpviewer_keywords:
- IBindingDisplay::GetCurrentDisplay method [.NET Framework debugging]
- GetCurrentDisplay method [.NET Framework debugging]
ms.assetid: d28eeea4-c4e0-40d4-91de-198d98cfa13c
topic_type:
- apiref
ms.openlocfilehash: d52f089923d16f93345444c07ff8e0619644f2eb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95725144"
---
# <a name="ibindingdisplaygetcurrentdisplay-method"></a><span data-ttu-id="20f8b-102">IBindingDisplay::GetCurrentDisplay 方法</span><span class="sxs-lookup"><span data-stu-id="20f8b-102">IBindingDisplay::GetCurrentDisplay Method</span></span>

<span data-ttu-id="20f8b-103">返回当前绑定显示信息。</span><span class="sxs-lookup"><span data-stu-id="20f8b-103">Returns the current binding display information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20f8b-104">语法</span><span class="sxs-lookup"><span data-stu-id="20f8b-104">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentDisplay (  
    [out, retval] SAFEARRAY(struct BindingDisplayTabControl) *display  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="20f8b-105">参数</span><span class="sxs-lookup"><span data-stu-id="20f8b-105">Parameters</span></span>  

 `display`  
 <span data-ttu-id="20f8b-106">[out，retval]指向包含绑定显示信息的 safearray 的指针。</span><span class="sxs-lookup"><span data-stu-id="20f8b-106">[out, retval] A pointer to a safearray containing the binding display information.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="20f8b-107">注解</span><span class="sxs-lookup"><span data-stu-id="20f8b-107">Remarks</span></span>  

 <span data-ttu-id="20f8b-108">[IBindingDisplay：： InitializeForProcess](ibindingdisplay-initializeforprocess-method.md)方法之前必须已成功，并且调试器必须停止该程序。</span><span class="sxs-lookup"><span data-stu-id="20f8b-108">The [IBindingDisplay::InitializeForProcess](ibindingdisplay-initializeforprocess-method.md) method must have previously succeeded, and the program must be stopped by a debugger.</span></span>  
  
 <span data-ttu-id="20f8b-109">调用方必须使用 SafeArrayDestroy 释放返回的 `SAFEARRAY` 内存[SafeArrayDestroy](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy)。</span><span class="sxs-lookup"><span data-stu-id="20f8b-109">The caller must deallocate the returned `SAFEARRAY` memory by using [SafeArrayDestroy](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20f8b-110">要求</span><span class="sxs-lookup"><span data-stu-id="20f8b-110">Requirements</span></span>  

 <span data-ttu-id="20f8b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20f8b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20f8b-112">**标头：** BindingDisplay</span><span class="sxs-lookup"><span data-stu-id="20f8b-112">**Header:** BindingDisplay.h</span></span>  
  
 <span data-ttu-id="20f8b-113">**库：** BindingDisplay .idl</span><span class="sxs-lookup"><span data-stu-id="20f8b-113">**Library:** BindingDisplay.idl</span></span>  
  
 <span data-ttu-id="20f8b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20f8b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20f8b-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="20f8b-115">See also</span></span>

- [<span data-ttu-id="20f8b-116">IBindingDisplay 接口</span><span class="sxs-lookup"><span data-stu-id="20f8b-116">IBindingDisplay Interface</span></span>](ibindingdisplay-interface.md)
- [<span data-ttu-id="20f8b-117">InitializeForProcess 方法</span><span class="sxs-lookup"><span data-stu-id="20f8b-117">InitializeForProcess Method</span></span>](ibindingdisplay-initializeforprocess-method.md)
