---
title: 'GetCurrentApartmentType 函数 (非托管 API 参考) '
description: GetCurrentApartmentType 函数检索要在其中执行调用方的单元的类型。
ms.date: 11/06/2017
api_name:
- GetCurrentApartmentType
api_location:
- WMINet_Utils.dll
api_type:
- DLLExport
f1_keywords:
- GetCurrentApartmentType
helpviewer_keywords:
- GetCurrentApartmentType function [.NET WMI and performance counters]
topic_type:
- Reference
ms.openlocfilehash: 0832867d86b7dda80e037846d9aa66c1d37f87be
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726192"
---
# <a name="getcurrentapartmenttype-function"></a><span data-ttu-id="d014f-103">GetCurrentApartmentType 函数</span><span class="sxs-lookup"><span data-stu-id="d014f-103">GetCurrentApartmentType function</span></span>

<span data-ttu-id="d014f-104">检索调用方执行操作所在的单元类型。</span><span class="sxs-lookup"><span data-stu-id="d014f-104">Retrieves the type of apartment in which the caller is executing.</span></span>
  
[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="d014f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d014f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCurrentApartmentType (
   [in] int                   vFunc,
   [in] IComThreadingInfo*    ptr,
   [out] APTTYPE*             aptType
);
```  

## <a name="parameters"></a><span data-ttu-id="d014f-106">参数</span><span class="sxs-lookup"><span data-stu-id="d014f-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="d014f-107">中此参数未使用。</span><span class="sxs-lookup"><span data-stu-id="d014f-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="d014f-108">中指向 [IComThreadingInfo](/windows/desktop/api/objidlbase/nn-objidlbase-icomthreadinginfo) 实例的指针。</span><span class="sxs-lookup"><span data-stu-id="d014f-108">[in] A pointer to an [IComThreadingInfo](/windows/desktop/api/objidlbase/nn-objidlbase-icomthreadinginfo) instance.</span></span>

`aptType`  
<span data-ttu-id="d014f-109">弄指向 [APTTYPE](/windows/win32/api/objidlbase/ne-objidlbase-apttype) 枚举值的指针，该枚举值指示调用方的单元。</span><span class="sxs-lookup"><span data-stu-id="d014f-109">[out] A pointer to an [APTTYPE](/windows/win32/api/objidlbase/ne-objidlbase-apttype) enumeration value that indicates the caller's apartment.</span></span>

## <a name="return-value"></a><span data-ttu-id="d014f-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d014f-110">Return value</span></span>

|<span data-ttu-id="d014f-111">返回的常量</span><span class="sxs-lookup"><span data-stu-id="d014f-111">Constant</span></span>  |<span data-ttu-id="d014f-112">Value</span><span class="sxs-lookup"><span data-stu-id="d014f-112">Value</span></span>  |<span data-ttu-id="d014f-113">说明</span><span class="sxs-lookup"><span data-stu-id="d014f-113">Description</span></span>  |
|---------|---------|---------|
| `S_OK` | <span data-ttu-id="d014f-114">0</span><span class="sxs-lookup"><span data-stu-id="d014f-114">0</span></span> | <span data-ttu-id="d014f-115">函数已成功完成。</span><span class="sxs-lookup"><span data-stu-id="d014f-115">The function completed successfully.</span></span> |
| `E_FAIL` | <span data-ttu-id="d014f-116">0x80000008</span><span class="sxs-lookup"><span data-stu-id="d014f-116">0x80000008</span></span> | <span data-ttu-id="d014f-117">调用方不在单元中执行。</span><span class="sxs-lookup"><span data-stu-id="d014f-117">The caller is not executing in an apartment.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="d014f-118">注解</span><span class="sxs-lookup"><span data-stu-id="d014f-118">Remarks</span></span>

<span data-ttu-id="d014f-119">此函数包装对 [IComThreadingInfo：： GetCurrentApartmentType](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="d014f-119">This function wraps a call to the [IComThreadingInfo::GetCurrentApartmentType](/windows/desktop/api/objidlbase/nf-objidlbase-icomthreadinginfo-getcurrentapartmenttype) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d014f-120">要求</span><span class="sxs-lookup"><span data-stu-id="d014f-120">Requirements</span></span>  

 <span data-ttu-id="d014f-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d014f-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d014f-122">**标头：** WMINet_Utils .idl</span><span class="sxs-lookup"><span data-stu-id="d014f-122">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="d014f-123">**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d014f-123">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d014f-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d014f-124">See also</span></span>

- [<span data-ttu-id="d014f-125">WMI 和性能计数器（非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="d014f-125">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
