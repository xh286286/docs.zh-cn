---
title: CLRDataCreateInstance 函数
ms.date: 03/30/2017
api_name:
- CLRDataCreateInstance
api_location:
- mscordbi.dll
- mscordacwks.dll
api_type:
- COM
f1_keywords:
- CLRDataCreateInstance
helpviewer_keywords:
- CLRDataCreateInstance function [.NET Framework debugging]
ms.assetid: 440bad90-5a88-45e7-9157-4596801d8d19
topic_type:
- apiref
ms.openlocfilehash: 2ffc575cfcef1089a70ef3b6d38787a5b4c50443
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729819"
---
# <a name="clrdatacreateinstance-function"></a><span data-ttu-id="557ee-102">CLRDataCreateInstance 函数</span><span class="sxs-lookup"><span data-stu-id="557ee-102">CLRDataCreateInstance Function</span></span>

<span data-ttu-id="557ee-103">为指定的目标项创建接口对象。</span><span class="sxs-lookup"><span data-stu-id="557ee-103">Creates an interface object for the specified target item.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="557ee-104">语法</span><span class="sxs-lookup"><span data-stu-id="557ee-104">Syntax</span></span>  
  
```cpp  
HRESULT CLRDataCreateInstance (  
    [in]  REFIID           iid,
    [in]  ICLRDataTarget  *target,
    [out] void           **iface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="557ee-105">参数</span><span class="sxs-lookup"><span data-stu-id="557ee-105">Parameters</span></span>  

 `iid`  
 <span data-ttu-id="557ee-106">中要实例化的接口的标识符。</span><span class="sxs-lookup"><span data-stu-id="557ee-106">[in] The identifier of the interface to be instantiated.</span></span>  
  
 `target`  
 <span data-ttu-id="557ee-107">中一个指向用户实现的 [ICLRDataTarget](iclrdatatarget-interface.md) 对象的指针，该对象表示要为其创建 interface 对象的目标项。</span><span class="sxs-lookup"><span data-stu-id="557ee-107">[in] A pointer to a user-implemented [ICLRDataTarget](iclrdatatarget-interface.md) object that represents the target item for which to create the interface object.</span></span>  
  
 `iface`  
 <span data-ttu-id="557ee-108">弄指向返回的接口对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="557ee-108">[out] A pointer to the address of the returned interface object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="557ee-109">注解</span><span class="sxs-lookup"><span data-stu-id="557ee-109">Remarks</span></span>  

 <span data-ttu-id="557ee-110">`ICLRDataTarget`对象由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="557ee-110">The `ICLRDataTarget` object is implemented by the writer of the debugging application.</span></span> <span data-ttu-id="557ee-111">实现取决于所表示的目标项的类型。</span><span class="sxs-lookup"><span data-stu-id="557ee-111">The implementation depends on the type of target item being represented.</span></span> <span data-ttu-id="557ee-112">目标项可以是进程、内存转储、远程计算机，等等。</span><span class="sxs-lookup"><span data-stu-id="557ee-112">The target item may be a process, memory dump, remote machine, and so on.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="557ee-113">要求</span><span class="sxs-lookup"><span data-stu-id="557ee-113">Requirements</span></span>  

 <span data-ttu-id="557ee-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="557ee-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="557ee-115">**标头：** ClrData .idl</span><span class="sxs-lookup"><span data-stu-id="557ee-115">**Header:** ClrData.idl</span></span>  
  
 <span data-ttu-id="557ee-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="557ee-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="557ee-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="557ee-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="557ee-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="557ee-118">See also</span></span>

- [<span data-ttu-id="557ee-119">调试全局静态函数</span><span class="sxs-lookup"><span data-stu-id="557ee-119">Debugging Global Static Functions</span></span>](debugging-global-static-functions.md)
