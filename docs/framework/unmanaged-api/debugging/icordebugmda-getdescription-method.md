---
title: ICorDebugMDA::GetDescription 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetDescription
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetDescription
helpviewer_keywords:
- GetDescription method [.NET Framework debugging]
- ICorDebugMDA::GetDescription method [.NET Framework debugging]
ms.assetid: 01d1b481-ca67-4712-8744-d342ec0df639
topic_type:
- apiref
ms.openlocfilehash: cb1e0f2bc597b48496dc362c9d7a364421c68a87
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95681842"
---
# <a name="icordebugmdagetdescription-method"></a><span data-ttu-id="0a491-102">ICorDebugMDA::GetDescription 方法</span><span class="sxs-lookup"><span data-stu-id="0a491-102">ICorDebugMDA::GetDescription Method</span></span>

<span data-ttu-id="0a491-103">获取一个字符串，该字符串包含由 [ICorDebugMDA](icordebugmda-interface.md)表示的托管调试助手 (MDA) 。</span><span class="sxs-lookup"><span data-stu-id="0a491-103">Gets a string containing the description of the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0a491-104">语法</span><span class="sxs-lookup"><span data-stu-id="0a491-104">Syntax</span></span>  
  
```cpp  
HRESULT GetDescription (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0a491-105">参数</span><span class="sxs-lookup"><span data-stu-id="0a491-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="0a491-106">中将存储说明的字符串缓冲区的大小。</span><span class="sxs-lookup"><span data-stu-id="0a491-106">[in] The size of the string buffer that will store the description.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="0a491-107">弄指向字符串缓冲区中返回的字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="0a491-107">[out] A pointer to the number of bytes returned in the string buffer.</span></span>  
  
 `szName`  
 <span data-ttu-id="0a491-108">弄包含 MDA 说明的字符串缓冲区。</span><span class="sxs-lookup"><span data-stu-id="0a491-108">[out] A string buffer containing the description of the MDA.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0a491-109">注解</span><span class="sxs-lookup"><span data-stu-id="0a491-109">Remarks</span></span>  

 <span data-ttu-id="0a491-110">字符串的长度可以为零。</span><span class="sxs-lookup"><span data-stu-id="0a491-110">The string can be zero in length.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0a491-111">要求</span><span class="sxs-lookup"><span data-stu-id="0a491-111">Requirements</span></span>  

 <span data-ttu-id="0a491-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0a491-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0a491-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0a491-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0a491-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0a491-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0a491-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0a491-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0a491-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0a491-116">See also</span></span>

- [<span data-ttu-id="0a491-117">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="0a491-117">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="0a491-118">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="0a491-118">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
