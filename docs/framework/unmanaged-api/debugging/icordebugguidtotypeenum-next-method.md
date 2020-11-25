---
title: ICorDebugGuidToTypeEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGuidToTypeEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGuidToTypeEnum::Next
helpviewer_keywords:
- ICorDebugGuidToTypeEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugGuidToTypeEnum interface [.NET Framework debugging]
ms.assetid: c9937666-8e18-484d-9fe0-b9ac95199530
topic_type:
- apiref
ms.openlocfilehash: 68f548705213da7d715ae569116abae0cd24129d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705652"
---
# <a name="icordebugguidtotypeenumnext-method"></a><span data-ttu-id="2c65b-102">ICorDebugGuidToTypeEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="2c65b-102">ICorDebugGuidToTypeEnum::Next Method</span></span>

<span data-ttu-id="2c65b-103">获取指定数量的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 实例，这些实例将 guid 映射到类型信息。</span><span class="sxs-lookup"><span data-stu-id="2c65b-103">Gets the specified number of [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) instances that map GUIDs to type information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c65b-104">语法</span><span class="sxs-lookup"><span data-stu-id="2c65b-104">Syntax</span></span>  
  
```cpp  
HRESULT Next(  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched] CorDebugGuidToTypeMapping values[  ],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2c65b-105">参数</span><span class="sxs-lookup"><span data-stu-id="2c65b-105">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="2c65b-106">中要检索的 GUID 到类型的映射对象的数量。</span><span class="sxs-lookup"><span data-stu-id="2c65b-106">[in] The number of GUID-to-type mapping objects to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="2c65b-107">弄指针的数组，其中每个都指向将 Windows 运行时 GUID 映射到其对应 ICorDebugType 对象的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="2c65b-107">[out] An array of pointers, each of which points to a [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) object that maps a Windows Runtime GUID to its corresponding ICorDebugType object.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="2c65b-108">弄一个指针，指向在中实际返回的 [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) 对象的数目 `values` 。</span><span class="sxs-lookup"><span data-stu-id="2c65b-108">[out] A pointer to the number of [CorDebugGuidToTypeMapping](cordebugguidtotypemapping-structure.md) objects actually returned in `values`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2c65b-109">备注</span><span class="sxs-lookup"><span data-stu-id="2c65b-109">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c65b-110">要求</span><span class="sxs-lookup"><span data-stu-id="2c65b-110">Requirements</span></span>  

 <span data-ttu-id="2c65b-111">**平台：** Windows 运行时</span><span class="sxs-lookup"><span data-stu-id="2c65b-111">**Platforms:** Windows Runtime</span></span>  
  
 <span data-ttu-id="2c65b-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="2c65b-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2c65b-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2c65b-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2c65b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2c65b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c65b-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c65b-115">See also</span></span>

- [<span data-ttu-id="2c65b-116">ICorDebugGuidToTypeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="2c65b-116">ICorDebugGuidToTypeEnum Interface</span></span>](icordebugguidtotypeenum-interface.md)
- [<span data-ttu-id="2c65b-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="2c65b-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
