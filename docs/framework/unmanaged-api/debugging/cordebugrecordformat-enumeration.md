---
title: “Cor调试记录格式”枚举
ms.date: 03/30/2017
api_name:
- CorDebugRecordFormat
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: d680c1c0-16ab-4ccc-9444-39cf8e0e05ee
topic_type:
- apiref
ms.openlocfilehash: b3a22d7b32eb258263d373ae91b3fb7fbc9aae99
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696383"
---
# <a name="cordebugrecordformat-enumeration"></a><span data-ttu-id="7b6e2-102">“Cor调试记录格式”枚举</span><span class="sxs-lookup"><span data-stu-id="7b6e2-102">CorDebugRecordFormat Enumeration</span></span>

<span data-ttu-id="7b6e2-103">描述包含本机异常调试事件相关信息的字节数组的数据格式。</span><span class="sxs-lookup"><span data-stu-id="7b6e2-103">Describes the format of the data in a byte array that contains information about a native exception debug event.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b6e2-104">语法</span><span class="sxs-lookup"><span data-stu-id="7b6e2-104">Syntax</span></span>  
  
```cpp  
typedef enum CorDebugRecordFormat {  
    FORMAT_WINDOWS_EXCEPTIONRECORD32 = 1,  
    FORMAT_WINDOWS_EXCEPTIONRECORD64 = 2,  
} CorDebugRecordFormat;  
```  
  
## <a name="members"></a><span data-ttu-id="7b6e2-105">成员</span><span class="sxs-lookup"><span data-stu-id="7b6e2-105">Members</span></span>  
  
|<span data-ttu-id="7b6e2-106">成员</span><span class="sxs-lookup"><span data-stu-id="7b6e2-106">Member</span></span>|<span data-ttu-id="7b6e2-107">说明</span><span class="sxs-lookup"><span data-stu-id="7b6e2-107">Description</span></span>|  
|------------|-----------------|  
|`FORMAT_WINDOWS_EXCEPTIONRECORD32`|<span data-ttu-id="7b6e2-108">数据为 32 位 Windows 异常记录。</span><span class="sxs-lookup"><span data-stu-id="7b6e2-108">The data is a 32-bit Windows exception record.</span></span>|  
|`FORMAT_WINDOWS_EXCEPTIONRECORD64`|<span data-ttu-id="7b6e2-109">数据为 64 位 Windows 异常记录。</span><span class="sxs-lookup"><span data-stu-id="7b6e2-109">The data is a 64-bit Windows exception record.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7b6e2-110">注解</span><span class="sxs-lookup"><span data-stu-id="7b6e2-110">Remarks</span></span>  

 <span data-ttu-id="7b6e2-111">枚举的成员 `CorDebugRecordFormat` 将传递给 [DecodeEvent](icordebugprocess6-decodeevent-method.md) 方法，以便在其参数中指示字节数组的格式 `pRecord` 。</span><span class="sxs-lookup"><span data-stu-id="7b6e2-111">A member of the `CorDebugRecordFormat` enumeration is passed to the [DecodeEvent](icordebugprocess6-decodeevent-method.md) method to indicate the format of the byte array in its `pRecord` argument.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7b6e2-112">此枚举仅用于 .NET Native 调试方案。</span><span class="sxs-lookup"><span data-stu-id="7b6e2-112">This enumeration is intended for use in .NET Native debugging scenarios only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7b6e2-113">要求</span><span class="sxs-lookup"><span data-stu-id="7b6e2-113">Requirements</span></span>  

 <span data-ttu-id="7b6e2-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7b6e2-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b6e2-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="7b6e2-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="7b6e2-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="7b6e2-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="7b6e2-117">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b6e2-117">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b6e2-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b6e2-118">See also</span></span>

- [<span data-ttu-id="7b6e2-119">调试枚举</span><span class="sxs-lookup"><span data-stu-id="7b6e2-119">Debugging Enumerations</span></span>](debugging-enumerations.md)
