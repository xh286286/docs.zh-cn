---
title: 'QualifierSet_Get 函数 (非托管 API 参考) '
description: QualifierSet_Get 函数获取命名限定符。
ms.date: 11/06/2017
api_name:
- QualifierSet_Get
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- QualifierSet_Get
helpviewer_keywords:
- QualifierSet_Get function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: fd096287b85b4a51a8cae85dddcca95cc1a8dbae
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721135"
---
# <a name="qualifierset_get-function"></a><span data-ttu-id="f0aef-103">QualifierSet_Get 函数</span><span class="sxs-lookup"><span data-stu-id="f0aef-103">QualifierSet_Get function</span></span>

<span data-ttu-id="f0aef-104">获取指定的命名限定符。</span><span class="sxs-lookup"><span data-stu-id="f0aef-104">Gets the specified named qualifier.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="f0aef-105">语法</span><span class="sxs-lookup"><span data-stu-id="f0aef-105">Syntax</span></span>  
  
```cpp  
HRESULT QualifierSet_Get (
   [in] int                  vFunc,
   [in] IWbemQualifierSet*   ptr,
   [in] LPCWSTR              wszName,
   [in] LONG                 lFlags,
   [out] VARIANT*            pVal,
   [out] LONG*               plFlavor
);
```  

## <a name="parameters"></a><span data-ttu-id="f0aef-106">参数</span><span class="sxs-lookup"><span data-stu-id="f0aef-106">Parameters</span></span>

<span data-ttu-id="f0aef-107">`vFunc` 中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="f0aef-107">`vFunc` [in] This parameter is unused.</span></span>

<span data-ttu-id="f0aef-108">`ptr` 中指向 [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="f0aef-108">`ptr` [in] A pointer to an [IWbemQualifierSet](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset) instance.</span></span>

<span data-ttu-id="f0aef-109">`wszName` 中请求其值的限定符的名称。</span><span class="sxs-lookup"><span data-stu-id="f0aef-109">`wszName` [in] The name of the qualifier whose value is requested.</span></span>

<span data-ttu-id="f0aef-110">`lFlags` 中保护.</span><span class="sxs-lookup"><span data-stu-id="f0aef-110">`lFlags` [in] Reserved.</span></span> <span data-ttu-id="f0aef-111">此参数必须为0。</span><span class="sxs-lookup"><span data-stu-id="f0aef-111">This parameter must be 0.</span></span>

<span data-ttu-id="f0aef-112">`pVal` 弄如果成功，则为限定符的正确类型和值。</span><span class="sxs-lookup"><span data-stu-id="f0aef-112">`pVal` [out] When successful, the correct type and value for the qualifier.</span></span> <span data-ttu-id="f0aef-113">如果函数失败，则 `VARIANT` `pVal` 不会修改指向的。</span><span class="sxs-lookup"><span data-stu-id="f0aef-113">If the function fails, the `VARIANT` pointed to by `pVal` is not modified.</span></span> <span data-ttu-id="f0aef-114">如果此参数为 `null` ，则忽略参数。</span><span class="sxs-lookup"><span data-stu-id="f0aef-114">If this parameter is `null`, the parameter is ignored.</span></span>

<span data-ttu-id="f0aef-115">`plFlavor` 弄一个指向 LONG 的指针，它接收所请求限定符的限定符风格位。</span><span class="sxs-lookup"><span data-stu-id="f0aef-115">`plFlavor` [out] A pointer to a LONG that receives the qualifier flavor bits for the requested qualifier.</span></span> <span data-ttu-id="f0aef-116">如果不需要口味信息，此参数可以为 `null` 。</span><span class="sxs-lookup"><span data-stu-id="f0aef-116">If flavor information is not desired, this parameter can be `null`.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0aef-117">返回值</span><span class="sxs-lookup"><span data-stu-id="f0aef-117">Return value</span></span>

<span data-ttu-id="f0aef-118">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="f0aef-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="f0aef-119">返回的常量</span><span class="sxs-lookup"><span data-stu-id="f0aef-119">Constant</span></span>  |<span data-ttu-id="f0aef-120">Value</span><span class="sxs-lookup"><span data-stu-id="f0aef-120">Value</span></span>  |<span data-ttu-id="f0aef-121">说明</span><span class="sxs-lookup"><span data-stu-id="f0aef-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="f0aef-122">0x80041008</span><span class="sxs-lookup"><span data-stu-id="f0aef-122">0x80041008</span></span> | <span data-ttu-id="f0aef-123">参数无效。</span><span class="sxs-lookup"><span data-stu-id="f0aef-123">A parameter is not valid.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="f0aef-124">0x80041002</span><span class="sxs-lookup"><span data-stu-id="f0aef-124">0x80041002</span></span> | <span data-ttu-id="f0aef-125">指定的限定符不存在。</span><span class="sxs-lookup"><span data-stu-id="f0aef-125">The specified qualifier does not exist.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="f0aef-126">0</span><span class="sxs-lookup"><span data-stu-id="f0aef-126">0</span></span> | <span data-ttu-id="f0aef-127">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="f0aef-127">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="f0aef-128">注解</span><span class="sxs-lookup"><span data-stu-id="f0aef-128">Remarks</span></span>

<span data-ttu-id="f0aef-129">此函数包装对 [IWbemQualifierSet：： Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-get) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="f0aef-129">This function wraps a call to the [IWbemQualifierSet::Get](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemqualifierset-get) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0aef-130">要求</span><span class="sxs-lookup"><span data-stu-id="f0aef-130">Requirements</span></span>  

 <span data-ttu-id="f0aef-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0aef-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0aef-132">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="f0aef-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="f0aef-133">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="f0aef-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0aef-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f0aef-134">See also</span></span>

- [<span data-ttu-id="f0aef-135">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="f0aef-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
