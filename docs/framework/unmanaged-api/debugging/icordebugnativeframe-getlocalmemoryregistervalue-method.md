---
title: ICorDebugNativeFrame::GetLocalMemoryRegisterValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetLocalMemoryRegisterValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetLocalMemoryRegisterValue
helpviewer_keywords:
- ICorDebugNativeFrame::GetLocalMemoryRegisterValue method [.NET Framework debugging]
- GetLocalMemoryRegisterValue method
ms.assetid: 33a19f6e-1029-4d53-af64-19591c6e58ee
topic_type:
- apiref
ms.openlocfilehash: 15485ac94ed9074baacc4fd2662a04bdcefcf1e7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709313"
---
# <a name="icordebugnativeframegetlocalmemoryregistervalue-method"></a><span data-ttu-id="f4651-102">ICorDebugNativeFrame::GetLocalMemoryRegisterValue 方法</span><span class="sxs-lookup"><span data-stu-id="f4651-102">ICorDebugNativeFrame::GetLocalMemoryRegisterValue Method</span></span>

<span data-ttu-id="f4651-103">获取参数或本地变量的值，在此本机帧中，将低字和高位字分别存储在指定的寄存器和内存位置。</span><span class="sxs-lookup"><span data-stu-id="f4651-103">Gets the value of an argument or local variable, of which the low word and high word are stored in the specified register and memory location, respectively, for this native frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4651-104">语法</span><span class="sxs-lookup"><span data-stu-id="f4651-104">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalMemoryRegisterValue (  
    [in] CORDB_ADDRESS      highWordAddress,  
    [in] CorDebugRegister   lowWordRegister,  
    [in] ULONG              cbSigBlob,  
    [in] PCCOR_SIGNATURE    pvSigBlob,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f4651-105">参数</span><span class="sxs-lookup"><span data-stu-id="f4651-105">Parameters</span></span>  

 `highWordAddress`  
 <span data-ttu-id="f4651-106">中一个 `CORDB_ADDRESS` 值，该值指定包含值高位字的内存位置。</span><span class="sxs-lookup"><span data-stu-id="f4651-106">[in] A `CORDB_ADDRESS` value that specifies the memory location containing the high word of the value.</span></span>  
  
 `lowWordRegister`  
 <span data-ttu-id="f4651-107">中"CorDebugRegister" 枚举的一个值，它指定包含值的低位字的寄存器。</span><span class="sxs-lookup"><span data-stu-id="f4651-107">[in] A value of the "CorDebugRegister" enumeration that specifies the register containing the low word of the value.</span></span>  
  
 `cbSigBlob`  
 <span data-ttu-id="f4651-108">中一个整数，指定参数引用的二进制元数据签名的大小 `pvSigBlob` 。</span><span class="sxs-lookup"><span data-stu-id="f4651-108">[in] An integer that specifies the size of the binary metadata signature which is referenced by the `pvSigBlob` parameter.</span></span>  
  
 `pvSigBlob`  
 <span data-ttu-id="f4651-109">中一个 `PCCOR_SIGNATURE` 值，该值指向值类型的二进制元数据签名。</span><span class="sxs-lookup"><span data-stu-id="f4651-109">[in] A `PCCOR_SIGNATURE` value that points to the binary metadata signature of the value's type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="f4651-110">弄一个指向 "ICorDebugValue" 对象地址的指针，该对象表示存储在指定寄存器和内存位置的检索到的值。</span><span class="sxs-lookup"><span data-stu-id="f4651-110">[out] A pointer to the address of an "ICorDebugValue" object representing the retrieved value that is stored in the specified register and memory location.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4651-111">要求</span><span class="sxs-lookup"><span data-stu-id="f4651-111">Requirements</span></span>  

 <span data-ttu-id="f4651-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f4651-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4651-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f4651-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f4651-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f4651-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f4651-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4651-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4651-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f4651-116">See also</span></span>
