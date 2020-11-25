---
title: 'WritePropertyValue 函数 (非托管 API 参考) '
description: WritePropertyValue 函数将字节写入属性。
ms.date: 11/06/2017
api_name:
- WritePropertyValue
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- WritePropertyValue
helpviewer_keywords:
- WritePropertyValue function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: e225516b06c477dc1a24cf721bc3e1ade9076b75
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729403"
---
# <a name="writepropertyvalue-function"></a><span data-ttu-id="2bd54-103">WritePropertyValue 函数</span><span class="sxs-lookup"><span data-stu-id="2bd54-103">WritePropertyValue function</span></span>

<span data-ttu-id="2bd54-104">将指定数量的字节写入由属性句柄标识的属性。</span><span class="sxs-lookup"><span data-stu-id="2bd54-104">Writes a specified number of bytes to a property identified by a property handle.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="2bd54-105">语法</span><span class="sxs-lookup"><span data-stu-id="2bd54-105">Syntax</span></span>  
  
```cpp  
HRESULT WritePropertyValue (
   [in] int                  vFunc,
   [in] IWbemObjectAccess*   ptr,
   [in] long                 lHandle,
   [in] long                 lNumBytes,
   [in] byte*                aData
);
```  

## <a name="parameters"></a><span data-ttu-id="2bd54-106">参数</span><span class="sxs-lookup"><span data-stu-id="2bd54-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="2bd54-107">中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="2bd54-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="2bd54-108">中指向 [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="2bd54-108">[in] A pointer to an [IWbemObjectAccess](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess) instance.</span></span>

`lHandle`  
<span data-ttu-id="2bd54-109">中一个整数，其中包含用于标识此属性的句柄。</span><span class="sxs-lookup"><span data-stu-id="2bd54-109">[in] An integer that contains the handle that identifies this property.</span></span> <span data-ttu-id="2bd54-110">可以通过调用 [GetPropertyHandle](getpropertyhandle.md) 函数来检索句柄。</span><span class="sxs-lookup"><span data-stu-id="2bd54-110">The handle can be retrieved by calling the [GetPropertyHandle](getpropertyhandle.md) function.</span></span>

`lNumBytes`  
<span data-ttu-id="2bd54-111">中要写入属性的字节数。</span><span class="sxs-lookup"><span data-stu-id="2bd54-111">[in] The number of bytes being written to the property.</span></span> <span data-ttu-id="2bd54-112">有关详细信息，请参阅 " [备注](#remarks) " 部分。</span><span class="sxs-lookup"><span data-stu-id="2bd54-112">See the [Remarks](#remarks) section for more information.</span></span>

<span data-ttu-id="2bd54-113">`pHandle` 弄指向包含数据的字节数组的指针。</span><span class="sxs-lookup"><span data-stu-id="2bd54-113">`pHandle` [out] A pointer to the byte array that contains the data.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bd54-114">返回值</span><span class="sxs-lookup"><span data-stu-id="2bd54-114">Return value</span></span>

<span data-ttu-id="2bd54-115">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="2bd54-115">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="2bd54-116">返回的常量</span><span class="sxs-lookup"><span data-stu-id="2bd54-116">Constant</span></span>  |<span data-ttu-id="2bd54-117">Value</span><span class="sxs-lookup"><span data-stu-id="2bd54-117">Value</span></span>  |<span data-ttu-id="2bd54-118">说明</span><span class="sxs-lookup"><span data-stu-id="2bd54-118">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="2bd54-119">0x80041008</span><span class="sxs-lookup"><span data-stu-id="2bd54-119">0x80041008</span></span> | <span data-ttu-id="2bd54-120">参数无效。</span><span class="sxs-lookup"><span data-stu-id="2bd54-120">A parameter is not valid.</span></span> |
|`WBEM_E_TYPE_MISMATCH` | <span data-ttu-id="2bd54-121">0x80041005</span><span class="sxs-lookup"><span data-stu-id="2bd54-121">0x80041005</span></span> | <span data-ttu-id="2bd54-122">出现类型不匹配。</span><span class="sxs-lookup"><span data-stu-id="2bd54-122">A type mismatch occurred.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="2bd54-123">0</span><span class="sxs-lookup"><span data-stu-id="2bd54-123">0</span></span> | <span data-ttu-id="2bd54-124">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="2bd54-124">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="2bd54-125">注解</span><span class="sxs-lookup"><span data-stu-id="2bd54-125">Remarks</span></span>

<span data-ttu-id="2bd54-126">此函数包装对 [IWbemClassObject：： WritePropertyValue](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="2bd54-126">This function wraps a call to the [IWbemClassObject::WritePropertyValue](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue) method.</span></span>

<span data-ttu-id="2bd54-127">使用此函数可设置字符串和所有其他非 `DWORD` 数据或非 `QWORD` 数据。</span><span class="sxs-lookup"><span data-stu-id="2bd54-127">Use this function to set string and all other non-`DWORD` or non-`QWORD` data.</span></span>

<span data-ttu-id="2bd54-128">对于非字符串属性值， `lNumBytes` 必须是指定的属性类型的正确数据大小。</span><span class="sxs-lookup"><span data-stu-id="2bd54-128">For nonstring property values, `lNumBytes` must be the correct data size of the property type specified.</span></span> <span data-ttu-id="2bd54-129">对于字符串属性值， `lNumBytes` 必须为指定字符串的长度（以字节为单位），并且字符串本身的长度必须为偶数（以字节为单位），后跟 null 终止字符。</span><span class="sxs-lookup"><span data-stu-id="2bd54-129">For string property values, `lNumBytes` must be the length of the specified string in bytes, and the string itself must be of an even length in bytes and be followed with a null-termination character.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd54-130">要求</span><span class="sxs-lookup"><span data-stu-id="2bd54-130">Requirements</span></span>  

<span data-ttu-id="2bd54-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2bd54-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2bd54-132">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="2bd54-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="2bd54-133">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="2bd54-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2bd54-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2bd54-134">See also</span></span>

- [<span data-ttu-id="2bd54-135">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="2bd54-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
