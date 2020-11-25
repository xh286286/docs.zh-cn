---
title: '克隆函数 (非托管 API 参考) '
description: Clone 函数返回一个新的对象，该对象是当前的完整副本。
ms.date: 11/06/2017
api_name:
- Clone
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- Clone
helpviewer_keywords:
- Clone function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: aecbf750b42626629dcb5aef369978a2e2bd002a
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708109"
---
# <a name="clone-function"></a><span data-ttu-id="a2f6a-103">Clone 函数</span><span class="sxs-lookup"><span data-stu-id="a2f6a-103">Clone function</span></span>

<span data-ttu-id="a2f6a-104">返回一个新对象，该对象是当前对象的完整克隆。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-104">Returns a new object that is a complete clone of the current object.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="a2f6a-105">语法</span><span class="sxs-lookup"><span data-stu-id="a2f6a-105">Syntax</span></span>  
  
```cpp  
HRESULT Clone (
   [in] int                  vFunc,
   [in] IWbemClassObject*    ptr,
   [out] IWbemClassObject**  ppCopy
);
```  

## <a name="parameters"></a><span data-ttu-id="a2f6a-106">参数</span><span class="sxs-lookup"><span data-stu-id="a2f6a-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="a2f6a-107">中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="a2f6a-108">中指向 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`ppCopy`  
<span data-ttu-id="a2f6a-109">弄一个新的对象，它是完全独立的 `ptr` 。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-109">[out] A new object that is a complete lone of `ptr`.</span></span> <span data-ttu-id="a2f6a-110">如果此参数接收当前对象的副本，则不能为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-110">This argument cannot be `null` if it receives the copy of the current object.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2f6a-111">返回值</span><span class="sxs-lookup"><span data-stu-id="a2f6a-111">Return value</span></span>

<span data-ttu-id="a2f6a-112">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="a2f6a-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="a2f6a-113">返回的常量</span><span class="sxs-lookup"><span data-stu-id="a2f6a-113">Constant</span></span>  |<span data-ttu-id="a2f6a-114">Value</span><span class="sxs-lookup"><span data-stu-id="a2f6a-114">Value</span></span>  |<span data-ttu-id="a2f6a-115">说明</span><span class="sxs-lookup"><span data-stu-id="a2f6a-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="a2f6a-116">0x80041001</span><span class="sxs-lookup"><span data-stu-id="a2f6a-116">0x80041001</span></span> | <span data-ttu-id="a2f6a-117">出现一般错误。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-117">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="a2f6a-118">0x80041008</span><span class="sxs-lookup"><span data-stu-id="a2f6a-118">0x80041008</span></span> | <span data-ttu-id="a2f6a-119">`null` 指定为一个参数，但在此用法中是非法的。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-119">`null` was specified as a parameter, and it is not legal in this usage.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="a2f6a-120">0x80041006</span><span class="sxs-lookup"><span data-stu-id="a2f6a-120">0x80041006</span></span> | <span data-ttu-id="a2f6a-121">没有足够的内存可用于克隆对象。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-121">Not enough memory is available to clone the object.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="a2f6a-122">0</span><span class="sxs-lookup"><span data-stu-id="a2f6a-122">0</span></span> | <span data-ttu-id="a2f6a-123">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-123">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="a2f6a-124">注解</span><span class="sxs-lookup"><span data-stu-id="a2f6a-124">Remarks</span></span>

<span data-ttu-id="a2f6a-125">此函数包装对 [IWbemClassObject：： Clone](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-125">This function wraps a call to the [IWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

<span data-ttu-id="a2f6a-126">克隆的对象是一个具有引用计数为1的 COM 对象。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-126">The cloned object is a COM object that has a reference count of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f6a-127">要求</span><span class="sxs-lookup"><span data-stu-id="a2f6a-127">Requirements</span></span>  

 <span data-ttu-id="a2f6a-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a2f6a-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a2f6a-129">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="a2f6a-129">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="a2f6a-130">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a2f6a-130">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a2f6a-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a2f6a-131">See also</span></span>

- [<span data-ttu-id="a2f6a-132">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="a2f6a-132">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
