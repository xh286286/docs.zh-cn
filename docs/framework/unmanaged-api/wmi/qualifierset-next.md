---
title: 'QualifierSet_Next 函数 (非托管 API 参考) '
description: QualifierSet_Next 函数检索枚举中的下一个限定符。
ms.date: 11/06/2017
api_name:
- QualifierSet_Next
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Next
helpviewer_keywords:
- QualifierSet_Next function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: 54d79a3dc081e9cdcb42153b6f7aa457557e3399
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721122"
---
# <a name="qualifierset_next-function"></a><span data-ttu-id="a3293-103">QualifierSet_Next 函数</span><span class="sxs-lookup"><span data-stu-id="a3293-103">QualifierSet_Next function</span></span>

<span data-ttu-id="a3293-104">检索枚举中的下一个限定符，该枚举以调用 [QualifierSet_BeginEnumeration ](qualifierset-beginenumeration.md) 函数开始。</span><span class="sxs-lookup"><span data-stu-id="a3293-104">Retrieves the next qualifier in an enumeration that started with a call to the [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md) function.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="a3293-105">语法</span><span class="sxs-lookup"><span data-stu-id="a3293-105">Syntax</span></span>  
  
```cpp  
HRESULT QualifierSet_Next (
   [in] int                  vFunc,
   [in] IWbemQualifierSet*   ptr,
   [in] LONG                 lFlags,
   [out] BSTR*               pstrName,
   [out] VARIANT*            pVal,
   [out] LONG*               plFlavor
);
```  

## <a name="parameters"></a><span data-ttu-id="a3293-106">参数</span><span class="sxs-lookup"><span data-stu-id="a3293-106">Parameters</span></span>

<span data-ttu-id="a3293-107">`vFunc` 中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="a3293-107">`vFunc` [in] This parameter is unused.</span></span>

<span data-ttu-id="a3293-108">`ptr` 中指向 [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="a3293-108">`ptr` [in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

<span data-ttu-id="a3293-109">`lFlags` 中保护.</span><span class="sxs-lookup"><span data-stu-id="a3293-109">`lFlags` [in] Reserved.</span></span> <span data-ttu-id="a3293-110">此参数必须为0。</span><span class="sxs-lookup"><span data-stu-id="a3293-110">This parameter must be 0.</span></span>

<span data-ttu-id="a3293-111">`pstrName` 弄限定符的名称。</span><span class="sxs-lookup"><span data-stu-id="a3293-111">`pstrName` [out] The name of the qualifier.</span></span> <span data-ttu-id="a3293-112">如果为 `null` ，则忽略此参数; 否则，将 `pstrName` 不会指向有效 `BSTR` 或内存泄漏。</span><span class="sxs-lookup"><span data-stu-id="a3293-112">If `null`, this parameter is ignored; otherwise, `pstrName` should not point to a valid `BSTR` or a memory leak occurs.</span></span> <span data-ttu-id="a3293-113">如果不为 null，则当函数返回时，它将始终分配一个新的 `BSTR` `WBEM_S_NO_ERROR` 。</span><span class="sxs-lookup"><span data-stu-id="a3293-113">If not null, the function always allocates a new `BSTR` when it returns `WBEM_S_NO_ERROR`.</span></span>

<span data-ttu-id="a3293-114">`pVal` 弄如果成功，则为限定符的值。</span><span class="sxs-lookup"><span data-stu-id="a3293-114">`pVal` [out] When successful, the value for the qualifier.</span></span> <span data-ttu-id="a3293-115">如果函数失败，则 `VARIANT` `pVal` 不会修改指向的。</span><span class="sxs-lookup"><span data-stu-id="a3293-115">If the function fails, the `VARIANT` pointed to by `pVal` is not modified.</span></span> <span data-ttu-id="a3293-116">如果此参数为 `null` ，则忽略参数。</span><span class="sxs-lookup"><span data-stu-id="a3293-116">If this parameter is `null`, the parameter is ignored.</span></span>

<span data-ttu-id="a3293-117">`plFlavor` 弄指向接收限定符风格的长时间的指针。</span><span class="sxs-lookup"><span data-stu-id="a3293-117">`plFlavor` [out] A pointer to a LONG that receives the qualifier flavor.</span></span> <span data-ttu-id="a3293-118">如果不需要口味信息，此参数可以为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="a3293-118">If flavor information is not desired, this parameter can be `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3293-119">返回值</span><span class="sxs-lookup"><span data-stu-id="a3293-119">Return value</span></span>

<span data-ttu-id="a3293-120">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="a3293-120">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="a3293-121">返回的常量</span><span class="sxs-lookup"><span data-stu-id="a3293-121">Constant</span></span>  |<span data-ttu-id="a3293-122">Value</span><span class="sxs-lookup"><span data-stu-id="a3293-122">Value</span></span>  |<span data-ttu-id="a3293-123">说明</span><span class="sxs-lookup"><span data-stu-id="a3293-123">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="a3293-124">0x80041008</span><span class="sxs-lookup"><span data-stu-id="a3293-124">0x80041008</span></span> | <span data-ttu-id="a3293-125">参数无效。</span><span class="sxs-lookup"><span data-stu-id="a3293-125">A parameter is not valid.</span></span> |
|`WBEM_E_UNEXPECTED` | <span data-ttu-id="a3293-126">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="a3293-126">0x8004101d</span></span> | <span data-ttu-id="a3293-127">调用方没有调用 [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="a3293-127">The caller did not call [QualifierSet_BeginEnumeration](qualifierset-beginenumeration.md).</span></span> |
|`WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="a3293-128">0x80041006</span><span class="sxs-lookup"><span data-stu-id="a3293-128">0x80041006</span></span> | <span data-ttu-id="a3293-129">没有足够的内存可用于开始新的枚举。</span><span class="sxs-lookup"><span data-stu-id="a3293-129">Not enough memory is available to begin a new enumeration.</span></span> |
| `WBEM_S_NO_MORE_DATA` | <span data-ttu-id="a3293-130">0x40005</span><span class="sxs-lookup"><span data-stu-id="a3293-130">0x40005</span></span> | <span data-ttu-id="a3293-131">枚举中没有剩余限定符。</span><span class="sxs-lookup"><span data-stu-id="a3293-131">No more qualifiers are left in the enumeration.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="a3293-132">0</span><span class="sxs-lookup"><span data-stu-id="a3293-132">0</span></span> | <span data-ttu-id="a3293-133">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="a3293-133">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="a3293-134">注解</span><span class="sxs-lookup"><span data-stu-id="a3293-134">Remarks</span></span>

<span data-ttu-id="a3293-135">此函数包装对 [IWbemQualifierSet：： Next](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-next) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="a3293-135">This function wraps a call to the [IWbemQualifierSet::Next](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-next) method.</span></span>

<span data-ttu-id="a3293-136">`QualifierSet_Next`重复调用函数以枚举所有限定符，直到函数返回 `WBEM_S_NO_MORE_DATA` 。</span><span class="sxs-lookup"><span data-stu-id="a3293-136">You call the `QualifierSet_Next` function repeatedly to enumerate all the qualifiers until the function return `WBEM_S_NO_MORE_DATA`.</span></span> <span data-ttu-id="a3293-137">若要提前终止枚举，请调用 [QualifierSet_EndEnumeration](qualifierset-endenumeration.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="a3293-137">To terminate the enumeration early, call the [QualifierSet_EndEnumeration](qualifierset-endenumeration.md) function.</span></span>

<span data-ttu-id="a3293-138">枚举过程中返回的限定符的顺序是不确定的。</span><span class="sxs-lookup"><span data-stu-id="a3293-138">The order of the qualifiers returned during the enumeration is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3293-139">要求</span><span class="sxs-lookup"><span data-stu-id="a3293-139">Requirements</span></span>  

 <span data-ttu-id="a3293-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a3293-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a3293-141">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="a3293-141">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="a3293-142">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="a3293-142">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a3293-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a3293-143">See also</span></span>

- [<span data-ttu-id="a3293-144">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="a3293-144">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
