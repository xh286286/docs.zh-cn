---
title: 'InheritsFrom 函数 (非托管 API 参考) '
description: InheritsFrom 函数确定类或实例是否从特定的父类派生。
ms.date: 11/06/2017
api_name:
- InheritsFrom
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- InheritsFrom
helpviewer_keywords:
- InheritsFrom function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: 3cfe3388dc808335e6d3daaf7ec949108e95f52e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726782"
---
# <a name="inheritsfrom-function"></a><span data-ttu-id="5c223-103">InheritsFrom 函数</span><span class="sxs-lookup"><span data-stu-id="5c223-103">InheritsFrom function</span></span>

<span data-ttu-id="5c223-104">确定当前类或实例是否派生自指定的父类。</span><span class="sxs-lookup"><span data-stu-id="5c223-104">Determines whether the current class or instance derives from a specified parent class.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="5c223-105">语法</span><span class="sxs-lookup"><span data-stu-id="5c223-105">Syntax</span></span>  
  
```cpp
HRESULT InheritsFrom (
   [in] int               vFunc,
   [in] IWbemClassObject* ptr,
   [in] LPCWSTR           wszAncestor
);
```  

## <a name="parameters"></a><span data-ttu-id="5c223-106">参数</span><span class="sxs-lookup"><span data-stu-id="5c223-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="5c223-107">中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="5c223-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="5c223-108">中指向 [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="5c223-108">[in] A pointer to an [IWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject) instance.</span></span>

`wszAncestor`  
<span data-ttu-id="5c223-109">中类的名称。</span><span class="sxs-lookup"><span data-stu-id="5c223-109">[in] The name of the class.</span></span> <span data-ttu-id="5c223-110">`wszAncestor` 必须指向有效的 `LPCWSTR` 。</span><span class="sxs-lookup"><span data-stu-id="5c223-110">`wszAncestor` must point to a valid `LPCWSTR`.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c223-111">返回值</span><span class="sxs-lookup"><span data-stu-id="5c223-111">Return value</span></span>

<span data-ttu-id="5c223-112">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="5c223-112">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="5c223-113">返回的常量</span><span class="sxs-lookup"><span data-stu-id="5c223-113">Constant</span></span>  |<span data-ttu-id="5c223-114">Value</span><span class="sxs-lookup"><span data-stu-id="5c223-114">Value</span></span>  |<span data-ttu-id="5c223-115">说明</span><span class="sxs-lookup"><span data-stu-id="5c223-115">Description</span></span>  |
|---------|---------|---------|
| `WBEM_S_NO_ERROR` | <span data-ttu-id="5c223-116">0</span><span class="sxs-lookup"><span data-stu-id="5c223-116">0</span></span> | <span data-ttu-id="5c223-117">当前对象继承自 `wszAncestor` 。</span><span class="sxs-lookup"><span data-stu-id="5c223-117">The current object inherits from `wszAncestor`.</span></span>  |
| `WBEM_S_FALSE` | <span data-ttu-id="5c223-118">1</span><span class="sxs-lookup"><span data-stu-id="5c223-118">1</span></span> | <span data-ttu-id="5c223-119">当前的对象不是从继承的 `wszAncestor` 。</span><span class="sxs-lookup"><span data-stu-id="5c223-119">The current object does not inherit from `wszAncestor`.</span></span> |
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="5c223-120">0x80041008</span><span class="sxs-lookup"><span data-stu-id="5c223-120">0x80041008</span></span> | <span data-ttu-id="5c223-121">`wszAncestor` 为 `null`。</span><span class="sxs-lookup"><span data-stu-id="5c223-121">`wszAncestor` is `null`.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="5c223-122">注解</span><span class="sxs-lookup"><span data-stu-id="5c223-122">Remarks</span></span>

<span data-ttu-id="5c223-123">此函数包装对 [IWbemClassObject：： InheritsFrom](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-inheritsfrom) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="5c223-123">This function wraps a call to the [IWbemClassObject::InheritsFrom](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-inheritsfrom) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c223-124">要求</span><span class="sxs-lookup"><span data-stu-id="5c223-124">Requirements</span></span>  

 <span data-ttu-id="5c223-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5c223-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5c223-126">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="5c223-126">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="5c223-127">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="5c223-127">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c223-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c223-128">See also</span></span>

- [<span data-ttu-id="5c223-129">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="5c223-129">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
