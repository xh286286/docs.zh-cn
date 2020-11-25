---
title: ICorDebugMDA::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetName
helpviewer_keywords:
- ICorDebugMDA::GetName method [.NET Framework debugging]
- GetName method, ICorDebugMDA interface [.NET Framework debugging]
ms.assetid: 885bf5e8-00b7-4cd7-9d8d-e720d47918c4
topic_type:
- apiref
ms.openlocfilehash: 516fcf8a97b92eac8dfff9eae34199caa97c2d2f
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710930"
---
# <a name="icordebugmdagetname-method"></a><span data-ttu-id="173c8-102">ICorDebugMDA::GetName 方法</span><span class="sxs-lookup"><span data-stu-id="173c8-102">ICorDebugMDA::GetName Method</span></span>

<span data-ttu-id="173c8-103">获取一个字符串，该字符串包含 [ICorDebugMDA](icordebugmda-interface.md)表示的托管调试助手 (MDA) 。</span><span class="sxs-lookup"><span data-stu-id="173c8-103">Gets a string containing the name of the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="173c8-104">语法</span><span class="sxs-lookup"><span data-stu-id="173c8-104">Syntax</span></span>  
  
```cpp  
HRESULT GetName (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="173c8-105">参数</span><span class="sxs-lookup"><span data-stu-id="173c8-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="173c8-106">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="173c8-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="173c8-107">弄指向名称长度的指针。</span><span class="sxs-lookup"><span data-stu-id="173c8-107">[out] A pointer to the length of the name.</span></span>  
  
 `szName`  
 <span data-ttu-id="173c8-108">弄要在其中存储名称的数组。</span><span class="sxs-lookup"><span data-stu-id="173c8-108">[out] An array in which to store the name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="173c8-109">注解</span><span class="sxs-lookup"><span data-stu-id="173c8-109">Remarks</span></span>  

 <span data-ttu-id="173c8-110">MDA 名称是唯一值。</span><span class="sxs-lookup"><span data-stu-id="173c8-110">MDA names are unique values.</span></span> <span data-ttu-id="173c8-111">`GetName`方法是获取 XML 流并基于该架构从流中提取名称的一种方便的性能方法。</span><span class="sxs-lookup"><span data-stu-id="173c8-111">The `GetName` method is a convenient performance alternative to getting the XML stream and extracting the name from the stream based on the schema.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="173c8-112">要求</span><span class="sxs-lookup"><span data-stu-id="173c8-112">Requirements</span></span>  

 <span data-ttu-id="173c8-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="173c8-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="173c8-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="173c8-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="173c8-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="173c8-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="173c8-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="173c8-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="173c8-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="173c8-117">See also</span></span>

- [<span data-ttu-id="173c8-118">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="173c8-118">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="173c8-119">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="173c8-119">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
