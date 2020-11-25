---
title: ICLRDataTarget::GetTLSValue 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.GetTLSValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::GetTLSValue
helpviewer_keywords:
- GetTLSValue method [.NET Framework debugging]
- ICLRDataTarget::GetTLSValue method [.NET Framework debugging]
ms.assetid: 0d8a7730-edc9-4728-898f-41b219cf5a28
topic_type:
- apiref
ms.openlocfilehash: f6066774961b3fba2c466e156296907efc2e53df
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95703390"
---
# <a name="iclrdatatargetgettlsvalue-method"></a><span data-ttu-id="fc00b-102">ICLRDataTarget::GetTLSValue 方法</span><span class="sxs-lookup"><span data-stu-id="fc00b-102">ICLRDataTarget::GetTLSValue Method</span></span>

<span data-ttu-id="fc00b-103">从线程本地存储区中获取一个值，该值在目标进程中指定线程 (TLS) 。</span><span class="sxs-lookup"><span data-stu-id="fc00b-103">Gets a value from the thread local storage (TLS) of the specified thread in the target process.</span></span> <span data-ttu-id="fc00b-104">此方法由公共语言运行时 (CLR) 数据访问服务调用。</span><span class="sxs-lookup"><span data-stu-id="fc00b-104">This method is called by the common language runtime (CLR) data access services.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fc00b-105">语法</span><span class="sxs-lookup"><span data-stu-id="fc00b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetTLSValue (  
    [in] ULONG32            threadID,  
    [in] ULONG32            index,  
    [out] CLRDATA_ADDRESS   *value  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fc00b-106">参数</span><span class="sxs-lookup"><span data-stu-id="fc00b-106">Parameters</span></span>  

 `threadID`  
 <span data-ttu-id="fc00b-107">中目标进程中的线程的操作系统标识符。</span><span class="sxs-lookup"><span data-stu-id="fc00b-107">[in] The operating system identifier of a thread in the target process.</span></span>  
  
 `index`  
 <span data-ttu-id="fc00b-108">中位置的索引。</span><span class="sxs-lookup"><span data-stu-id="fc00b-108">[in] The index of the location.</span></span> <span data-ttu-id="fc00b-109">此值必须是指定线程的本地存储区中的有效索引。</span><span class="sxs-lookup"><span data-stu-id="fc00b-109">This value must be a valid index in the local store of the specified thread.</span></span>  
  
 `value`  
 <span data-ttu-id="fc00b-110">弄一个指向 `CLRDATA_ADDRESS` 值的指针，该值指定从给定的 TLS 位置返回的值。</span><span class="sxs-lookup"><span data-stu-id="fc00b-110">[out] A pointer to a `CLRDATA_ADDRESS` value that specifies the value returned from the given TLS location.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="fc00b-111">注解</span><span class="sxs-lookup"><span data-stu-id="fc00b-111">Remarks</span></span>  

 <span data-ttu-id="fc00b-112">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="fc00b-112">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fc00b-113">要求</span><span class="sxs-lookup"><span data-stu-id="fc00b-113">Requirements</span></span>  

 <span data-ttu-id="fc00b-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fc00b-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc00b-115">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="fc00b-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="fc00b-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fc00b-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fc00b-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fc00b-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc00b-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fc00b-118">See also</span></span>

- [<span data-ttu-id="fc00b-119">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="fc00b-119">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
