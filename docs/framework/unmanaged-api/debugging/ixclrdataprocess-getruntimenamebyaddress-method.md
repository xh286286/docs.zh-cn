---
title: IXCLRDataProcess：： GetRuntimeNameByAddress 方法
ms.date: 4/27/2020
api.name:
- IXCLRDataProcess::GetRuntimeNameByAddress Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::GetRuntimeNameByAddress Method
helpviewer.keywords:
- IXCLRDataProcess::GetRuntimeNameByAddress Method [.NET Framework debugging]
topic_type:
- apiref
author: tommcdon
ms.author: tommcdon
ms.openlocfilehash: 6648bdafe6e5cdd402bcfa02a148c57f0f1e209e
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275564"
---
# <a name="ixclrdataprocessgetruntimenamebyaddress-method"></a><span data-ttu-id="65fd1-102">IXCLRDataProcess：： GetRuntimeNameByAddress 方法</span><span class="sxs-lookup"><span data-stu-id="65fd1-102">IXCLRDataProcess::GetRuntimeNameByAddress Method</span></span>

<span data-ttu-id="65fd1-103">获取给定地址的名称。</span><span class="sxs-lookup"><span data-stu-id="65fd1-103">Gets a name for the given address.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="65fd1-104">语法</span><span class="sxs-lookup"><span data-stu-id="65fd1-104">Syntax</span></span>

```cpp
HRESULT GetRuntimeNameByAddress(
    [in] CLRDATA_ADDRESS address,
    [in] ULONG32 flags,
    [in] ULONG32 bufLen,
    [out] ULONG32 *nameLen,
    [out, size_is(bufLen)] WCHAR nameBuf[],
    [out] CLRDATA_ADDRESS* displacement
);
```

## <a name="parameters"></a><span data-ttu-id="65fd1-105">参数</span><span class="sxs-lookup"><span data-stu-id="65fd1-105">Parameters</span></span>

`address`\
<span data-ttu-id="65fd1-106">中一个 `CLRDATA_ADDRESS` 表示代码地址的值。</span><span class="sxs-lookup"><span data-stu-id="65fd1-106">[in] A `CLRDATA_ADDRESS` value that represents a code address.</span></span>

`flags`\
<span data-ttu-id="65fd1-107">中设置为 "0"。</span><span class="sxs-lookup"><span data-stu-id="65fd1-107">[in] Set to '0'.</span></span>

`bufLen`\
<span data-ttu-id="65fd1-108">中缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="65fd1-108">[in] The length of the buffer.</span></span>

`namLen`\
<span data-ttu-id="65fd1-109">弄一个指针，指向返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="65fd1-109">[out] A pointer to the number of characters returned.</span></span>

`namBuf`\
<span data-ttu-id="65fd1-110">[out，size_is (`bufLen`) ] `bufLen` 存储运行时名称的长度的输入缓冲区。</span><span class="sxs-lookup"><span data-stu-id="65fd1-110">[out, size_is(`bufLen`)] The input buffer of length `bufLen` that stores the runtime name.</span></span>

`displacement`\
<span data-ttu-id="65fd1-111">弄 `CLRDATA_ADDRESS` 指向返回符号的代码偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="65fd1-111">[out] A `CLRDATA_ADDRESS` pointer to the code offset of the returned symbol.</span></span>

## <a name="remarks"></a><span data-ttu-id="65fd1-112">备注</span><span class="sxs-lookup"><span data-stu-id="65fd1-112">Remarks</span></span>

<span data-ttu-id="65fd1-113">提供的方法是接口的一部分 `IXCLRDataProcess` ，并且对应于虚拟方法表的第16个槽。</span><span class="sxs-lookup"><span data-stu-id="65fd1-113">The provided method is part of the `IXCLRDataProcess` interface and corresponds to the 16th slot of the virtual-method table.</span></span>

> [!NOTE]
> <span data-ttu-id="65fd1-114">如果缓冲区不够大，则此方法返回， `S_FALSE` 并将设置 `nameLen` 为所需的缓冲区长度。</span><span class="sxs-lookup"><span data-stu-id="65fd1-114">If the buffer is not large enough for the name, this method returns `S_FALSE` and sets `nameLen` to the required buffer length.</span></span>

## <a name="requirements"></a><span data-ttu-id="65fd1-115">要求</span><span class="sxs-lookup"><span data-stu-id="65fd1-115">Requirements</span></span>

<span data-ttu-id="65fd1-116">**平台：** 查看 [系统要求](../../get-started/system-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="65fd1-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md)</span></span>\
<span data-ttu-id="65fd1-117">**标头：** 内容</span><span class="sxs-lookup"><span data-stu-id="65fd1-117">**Header:** None\</span></span>
<span data-ttu-id="65fd1-118">**库：** 内容</span><span class="sxs-lookup"><span data-stu-id="65fd1-118">**Library:** None\</span></span>
<span data-ttu-id="65fd1-119">**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="65fd1-119">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="65fd1-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65fd1-120">See also</span></span>

- [<span data-ttu-id="65fd1-121">调试</span><span class="sxs-lookup"><span data-stu-id="65fd1-121">Debugging</span></span>](index.md)
- [<span data-ttu-id="65fd1-122">IXCLRDataProcess 接口</span><span class="sxs-lookup"><span data-stu-id="65fd1-122">IXCLRDataProcess Interface</span></span>](ixclrdataprocess-interface.md)
