---
title: ICorDebugMDA::GetXML 方法
ms.date: 03/30/2017
api_name:
- ICorDebugMDA.GetXML
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMDA::GetXML
helpviewer_keywords:
- ICorDebugMDA::GetXML method [.NET Framework debugging]
- GetXML method [.NET Framework debugging]
ms.assetid: 29746b24-3766-4255-8813-0426c45e73e5
topic_type:
- apiref
ms.openlocfilehash: 9a088c7e4e9c72c8247ccdd384bc724587210c37
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95710865"
---
# <a name="icordebugmdagetxml-method"></a><span data-ttu-id="1fae4-102">ICorDebugMDA::GetXML 方法</span><span class="sxs-lookup"><span data-stu-id="1fae4-102">ICorDebugMDA::GetXML Method</span></span>

<span data-ttu-id="1fae4-103">获取与托管调试助手关联的完整 XML 流 (MDA) 表示的 [ICorDebugMDA](icordebugmda-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="1fae4-103">Gets the full XML stream associated with the managed debugging assistant (MDA) represented by [ICorDebugMDA](icordebugmda-interface.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1fae4-104">语法</span><span class="sxs-lookup"><span data-stu-id="1fae4-104">Syntax</span></span>  
  
```cpp  
HRESULT GetXML (  
    [in] ULONG32   cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
        WCHAR      szName[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1fae4-105">参数</span><span class="sxs-lookup"><span data-stu-id="1fae4-105">Parameters</span></span>  

 `cchName`  
 <span data-ttu-id="1fae4-106">[in] `szName` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="1fae4-106">[in] The size of the `szName` array.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="1fae4-107">弄指向 XML 流长度的指针。</span><span class="sxs-lookup"><span data-stu-id="1fae4-107">[out] A pointer to the length of the XML stream.</span></span>  
  
 `szName`  
 <span data-ttu-id="1fae4-108">弄要在其中存储 XML 流的数组。</span><span class="sxs-lookup"><span data-stu-id="1fae4-108">[out] An array in which to store the XML stream.</span></span> <span data-ttu-id="1fae4-109">该数组可能为空。</span><span class="sxs-lookup"><span data-stu-id="1fae4-109">The array may be empty.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1fae4-110">注解</span><span class="sxs-lookup"><span data-stu-id="1fae4-110">Remarks</span></span>  

 <span data-ttu-id="1fae4-111">此 `GetXML` 方法可能会影响性能，具体取决于关联的 XML 流的大小。</span><span class="sxs-lookup"><span data-stu-id="1fae4-111">The `GetXML` method can potentially affect performance, depending on the size of the associated XML stream.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1fae4-112">要求</span><span class="sxs-lookup"><span data-stu-id="1fae4-112">Requirements</span></span>  

 <span data-ttu-id="1fae4-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1fae4-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1fae4-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="1fae4-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="1fae4-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="1fae4-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="1fae4-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1fae4-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1fae4-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1fae4-117">See also</span></span>

- [<span data-ttu-id="1fae4-118">ICorDebugMDA 接口</span><span class="sxs-lookup"><span data-stu-id="1fae4-118">ICorDebugMDA Interface</span></span>](icordebugmda-interface.md)
- [<span data-ttu-id="1fae4-119">使用托管调试助手诊断错误</span><span class="sxs-lookup"><span data-stu-id="1fae4-119">Diagnosing Errors with Managed Debugging Assistants</span></span>](../../debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
