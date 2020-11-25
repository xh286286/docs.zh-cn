---
title: 'EndMethodEnumeration 函数 (非托管 API 参考) '
description: EndMethodEnumeration 函数终止方法枚举序列。
ms.date: 11/06/2017
api_name:
- EndMethodEnumeration
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- EndMethodEnumeration
helpviewer_keywords:
- EndMethodEnumeration function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: 82f50530967699427d8a00b1c9f518b639273626
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708057"
---
# <a name="endmethodenumeration-function"></a><span data-ttu-id="f8bdf-103">EndMethodEnumeration 函数</span><span class="sxs-lookup"><span data-stu-id="f8bdf-103">EndMethodEnumeration function</span></span>

<span data-ttu-id="f8bdf-104">终止使用对 [BeginMethodEnumeration 函数](beginmethodenumeration.md)的调用启动的枚举序列。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-104">Terminates an enumeration sequence started with a call to the [BeginMethodEnumeration function](beginmethodenumeration.md).</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="f8bdf-105">语法</span><span class="sxs-lookup"><span data-stu-id="f8bdf-105">Syntax</span></span>  
  
```cpp  
HRESULT EndMethodEnumeration (
   [in] int               vFunc,
   [in] IWbemClassObject* ptr
);
```  

## <a name="parameters"></a><span data-ttu-id="f8bdf-106">参数</span><span class="sxs-lookup"><span data-stu-id="f8bdf-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="f8bdf-107">中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="f8bdf-108">中指向 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8bdf-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f8bdf-109">Return value</span></span>

<span data-ttu-id="f8bdf-110">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="f8bdf-110">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="f8bdf-111">返回的常量</span><span class="sxs-lookup"><span data-stu-id="f8bdf-111">Constant</span></span>  |<span data-ttu-id="f8bdf-112">Value</span><span class="sxs-lookup"><span data-stu-id="f8bdf-112">Value</span></span>  |<span data-ttu-id="f8bdf-113">说明</span><span class="sxs-lookup"><span data-stu-id="f8bdf-113">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="f8bdf-114">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="f8bdf-114">0x8004101d</span></span> | <span data-ttu-id="f8bdf-115">发生了内部错误。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-115">An internal error occurred.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="f8bdf-116">0</span><span class="sxs-lookup"><span data-stu-id="f8bdf-116">0</span></span> | <span data-ttu-id="f8bdf-117">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-117">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="f8bdf-118">注解</span><span class="sxs-lookup"><span data-stu-id="f8bdf-118">Remarks</span></span>

<span data-ttu-id="f8bdf-119">此函数包装对 [IWbemClassObject：： EndMethodEnumeration](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endmethodenumeration) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-119">This function wraps a call to the [IWbemClassObject::EndMethodEnumeration](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endmethodenumeration) method.</span></span>

<span data-ttu-id="f8bdf-120">调用方使用 [BeginMethodEnumeration 函数](beginmethodenumeration.md)开始枚举序列，然后调用 [NextMethod 函数](nextmethod.md )，直到该方法返回 `WBEM_S_NO_MORE_DATA` 。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-120">The caller begins the enumeration sequence using [BeginMethodEnumeration function](beginmethodenumeration.md), and then calls the [NextMethod function](nextmethod.md )until the method  returns `WBEM_S_NO_MORE_DATA`.</span></span> <span data-ttu-id="f8bdf-121">调用方可以通过调用来完成序列 `EndMethodEnumeration` 。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-121">The caller optionally finishes the sequence by calling `EndMethodEnumeration`.</span></span> <span data-ttu-id="f8bdf-122">调用方可以在任何时间通过调用来提前终止枚举 `EndMethodEnumeration` 。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-122">The caller may terminate the enumeration early by calling `EndMethodEnumeration` at any time.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8bdf-123">要求</span><span class="sxs-lookup"><span data-stu-id="f8bdf-123">Requirements</span></span>  

 <span data-ttu-id="f8bdf-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f8bdf-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f8bdf-125">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="f8bdf-125">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="f8bdf-126">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f8bdf-126">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8bdf-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8bdf-127">See also</span></span>

- [<span data-ttu-id="f8bdf-128">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="f8bdf-128">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
