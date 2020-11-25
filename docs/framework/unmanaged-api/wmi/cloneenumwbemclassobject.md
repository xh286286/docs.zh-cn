---
title: 'CloneEnumWbemClassObject 函数 (非托管 API 参考) '
description: CloneEnumWbemClassObject 函数生成枚举器的逻辑副本。
ms.date: 11/06/2017
api_name:
- CloneEnumWbemClassObject
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- CloneEnumWbemClassObject
helpviewer_keywords:
- CloneEnumWbemClassObject function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: fa8a7f436c018e3e083be452d300eb21e17f93f3
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95708122"
---
# <a name="cloneenumwbemclassobject-function"></a><span data-ttu-id="384e3-103">CloneEnumWbemClassObject 函数</span><span class="sxs-lookup"><span data-stu-id="384e3-103">CloneEnumWbemClassObject function</span></span>

<span data-ttu-id="384e3-104">制作枚举器的逻辑副本，并保留其在枚举中的当前位置。</span><span class="sxs-lookup"><span data-stu-id="384e3-104">Makes a logical copy of an enumerator, retaining its current position in an enumeration.</span></span>

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]

## <a name="syntax"></a><span data-ttu-id="384e3-105">语法</span><span class="sxs-lookup"><span data-stu-id="384e3-105">Syntax</span></span>

```cpp
HRESULT CloneEnumWbemClassObject (
   [out] IEnumWbemClassObject**  ppEnum,
   [in] DWORD                    authLevel,
   [in] DWORD                    impLevel,
   [in] IEnumWbemClassObject*    pCurrentEnumWbemClassObject,
   [in] BSTR                     strUser,
   [in] BSTR                     strPassword,
   [in BSTR]                     strAuthority
);
```

## <a name="parameters"></a><span data-ttu-id="384e3-106">参数</span><span class="sxs-lookup"><span data-stu-id="384e3-106">Parameters</span></span>

`ppEnum`\
<span data-ttu-id="384e3-107">弄接收指向新 [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject)的指针。</span><span class="sxs-lookup"><span data-stu-id="384e3-107">[out] Receives a pointer to a new [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject).</span></span>

`authLevel`\
<span data-ttu-id="384e3-108">中授权级别。</span><span class="sxs-lookup"><span data-stu-id="384e3-108">[in] The authorization level.</span></span>

`impLevel`\
<span data-ttu-id="384e3-109">中模拟级别。</span><span class="sxs-lookup"><span data-stu-id="384e3-109">[in] The impersonation level.</span></span>

`pCurrentEnumWbemClassObject`\
<span data-ttu-id="384e3-110">弄指向要克隆的 [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="384e3-110">[out] A pointer to the [IEnumWbemClassObject](/windows/desktop/api/wbemcli/nn-wbemcli-ienumwbemclassobject) instance to be cloned.</span></span>

`strUser`\
<span data-ttu-id="384e3-111">中用户名。</span><span class="sxs-lookup"><span data-stu-id="384e3-111">[in] The user name.</span></span> <span data-ttu-id="384e3-112">有关详细信息，请参阅 [ConnectServerWmi](connectserverwmi.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="384e3-112">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

`strPassword`\
<span data-ttu-id="384e3-113">中密码。</span><span class="sxs-lookup"><span data-stu-id="384e3-113">[in] The password.</span></span> <span data-ttu-id="384e3-114">有关详细信息，请参阅 [ConnectServerWmi](connectserverwmi.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="384e3-114">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

`strAuthority`\
<span data-ttu-id="384e3-115">中用户的域名。</span><span class="sxs-lookup"><span data-stu-id="384e3-115">[in] The domain name of the user.</span></span> <span data-ttu-id="384e3-116">有关详细信息，请参阅 [ConnectServerWmi](connectserverwmi.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="384e3-116">See the [ConnectServerWmi](connectserverwmi.md) function for more information.</span></span>

## <a name="return-value"></a><span data-ttu-id="384e3-117">返回值</span><span class="sxs-lookup"><span data-stu-id="384e3-117">Return value</span></span>

<span data-ttu-id="384e3-118">此函数返回的以下值是在 *WbemCli* 头文件中定义的，也可以在代码中将它们定义为常量：</span><span class="sxs-lookup"><span data-stu-id="384e3-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="384e3-119">返回的常量</span><span class="sxs-lookup"><span data-stu-id="384e3-119">Constant</span></span>  |<span data-ttu-id="384e3-120">Value</span><span class="sxs-lookup"><span data-stu-id="384e3-120">Value</span></span>  |<span data-ttu-id="384e3-121">说明</span><span class="sxs-lookup"><span data-stu-id="384e3-121">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_FAILED` | <span data-ttu-id="384e3-122">0x80041001</span><span class="sxs-lookup"><span data-stu-id="384e3-122">0x80041001</span></span> | <span data-ttu-id="384e3-123">出现一般错误。</span><span class="sxs-lookup"><span data-stu-id="384e3-123">There has been a general failure.</span></span> |
| `WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="384e3-124">0x80041008</span><span class="sxs-lookup"><span data-stu-id="384e3-124">0x80041008</span></span> | <span data-ttu-id="384e3-125">参数无效。</span><span class="sxs-lookup"><span data-stu-id="384e3-125">A parameter is invalid.</span></span> |
| `WBEM_E_OUT_OF_MEMORY` | <span data-ttu-id="384e3-126">0x80041006</span><span class="sxs-lookup"><span data-stu-id="384e3-126">0x80041006</span></span> | <span data-ttu-id="384e3-127">没有足够的可用内存来完成该操作。</span><span class="sxs-lookup"><span data-stu-id="384e3-127">Not enough memory is available complete the operation.</span></span> |
| `WBEM_E_TRANSPORT_FAILURE` | <span data-ttu-id="384e3-128">0x80041015</span><span class="sxs-lookup"><span data-stu-id="384e3-128">0x80041015</span></span> | <span data-ttu-id="384e3-129">远程过程调用 (RPC) 当前进程和 WMI 之间的链接已失败。</span><span class="sxs-lookup"><span data-stu-id="384e3-129">The remote procedure call (RPC) link between the current process and WMI has failed.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="384e3-130">0</span><span class="sxs-lookup"><span data-stu-id="384e3-130">0</span></span> | <span data-ttu-id="384e3-131">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="384e3-131">The function call was successful.</span></span>  |

## <a name="remarks"></a><span data-ttu-id="384e3-132">注解</span><span class="sxs-lookup"><span data-stu-id="384e3-132">Remarks</span></span>

<span data-ttu-id="384e3-133">此函数包装对 [IEnumWbemClassObject：： Clone](/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="384e3-133">This function wraps a call to the [IEnumWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone) method.</span></span>

<span data-ttu-id="384e3-134">此方法仅进行 "最大努力" 复制。</span><span class="sxs-lookup"><span data-stu-id="384e3-134">This method makes only a "best effort" copy.</span></span> <span data-ttu-id="384e3-135">由于很多 CIM 对象的动态性质，新枚举器可能不会枚举与源枚举器相同的一组对象。</span><span class="sxs-lookup"><span data-stu-id="384e3-135">Due to the dynamic nature of many CIM objects, it is possible that the new enumerator does not enumerate the same set of objects as the source enumerator.</span></span>

<span data-ttu-id="384e3-136">如果函数调用失败，可以通过调用 [GetErrorInfo](geterrorinfo.md) 函数获取其他错误信息。</span><span class="sxs-lookup"><span data-stu-id="384e3-136">If the function call fails, you can obtain additional error information by calling the [GetErrorInfo](geterrorinfo.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="384e3-137">示例</span><span class="sxs-lookup"><span data-stu-id="384e3-137">Example</span></span>

<span data-ttu-id="384e3-138">有关示例，请参阅 [IEnumWbemClassObject：： Clone](/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone) 方法。</span><span class="sxs-lookup"><span data-stu-id="384e3-138">For an example, see the [IEnumWbemClassObject::Clone](/windows/desktop/api/wbemcli/nf-wbemcli-ienumwbemclassobject-clone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="384e3-139">要求</span><span class="sxs-lookup"><span data-stu-id="384e3-139">Requirements</span></span>

 <span data-ttu-id="384e3-140">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="384e3-140">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

 <span data-ttu-id="384e3-141">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="384e3-141">**Header:** WMINet_Utils.idl</span></span>

 <span data-ttu-id="384e3-142">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="384e3-142">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="384e3-143">另请参阅</span><span class="sxs-lookup"><span data-stu-id="384e3-143">See also</span></span>

- [<span data-ttu-id="384e3-144">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="384e3-144">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
