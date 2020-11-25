---
title: ICorDebugEval::CreateValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.CreateValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::CreateValue
helpviewer_keywords:
- ICorDebugEval::CreateValue method [.NET Framework debugging]
- CreateValue method [.NET Framework debugging]
ms.assetid: 9a1c0b47-6f10-4fcb-844a-4ab2d7990140
topic_type:
- apiref
ms.openlocfilehash: 41db6ac00d8646651d0e8433d076c37af6020071
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95696149"
---
# <a name="icordebugevalcreatevalue-method"></a><span data-ttu-id="939ec-102">ICorDebugEval::CreateValue 方法</span><span class="sxs-lookup"><span data-stu-id="939ec-102">ICorDebugEval::CreateValue Method</span></span>

<span data-ttu-id="939ec-103">创建指定类型的值，其初始值为零或 null。</span><span class="sxs-lookup"><span data-stu-id="939ec-103">Creates a value of the specified type, with an initial value of zero or null.</span></span>  
  
 <span data-ttu-id="939ec-104">此方法在 .NET Framework 版本2.0 中已过时。</span><span class="sxs-lookup"><span data-stu-id="939ec-104">This method is obsolete in the .NET Framework version 2.0.</span></span> <span data-ttu-id="939ec-105">改 [为使用 ICorDebugEval2：： CreateValueForType](icordebugeval2-createvaluefortype-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="939ec-105">Use [ICorDebugEval2::CreateValueForType](icordebugeval2-createvaluefortype-method.md) instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="939ec-106">语法</span><span class="sxs-lookup"><span data-stu-id="939ec-106">Syntax</span></span>  
  
```cpp  
HRESULT CreateValue (  
    [in] CorElementType     elementType,  
    [in] ICorDebugClass     *pElementClass,  
    [out] ICorDebugValue    **ppValue  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="939ec-107">参数</span><span class="sxs-lookup"><span data-stu-id="939ec-107">Parameters</span></span>  

 `elementType`  
 <span data-ttu-id="939ec-108">中 [CorElementType](../metadata/corelementtype-enumeration.md) 枚举的一个值，该值指定值的类型。</span><span class="sxs-lookup"><span data-stu-id="939ec-108">[in] A value of the [CorElementType](../metadata/corelementtype-enumeration.md) enumeration that specifies the type of the value.</span></span>  
  
 `pElementClass`  
 <span data-ttu-id="939ec-109">中指向 [ICorDebugClass](icordebugclass-interface.md) 对象的指针，该对象指定值的类（如果该类型不是基元类型）。</span><span class="sxs-lookup"><span data-stu-id="939ec-109">[in] Pointer to an [ICorDebugClass](icordebugclass-interface.md) object that specifies the class of the value, if the type is not a primitive type.</span></span>  
  
 `ppValue`  
 <span data-ttu-id="939ec-110">弄指向表示值的 "ICorDebugValue" 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="939ec-110">[out] Pointer to the address of an "ICorDebugValue" object that represents the value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="939ec-111">注解</span><span class="sxs-lookup"><span data-stu-id="939ec-111">Remarks</span></span>  

 <span data-ttu-id="939ec-112">`CreateValue` 创建 `ICorDebugValue` 给定类型的对象，其唯一目的是在函数计算中使用它。</span><span class="sxs-lookup"><span data-stu-id="939ec-112">`CreateValue` creates an `ICorDebugValue` object of the given type for the sole purpose of using it in a function evaluation.</span></span> <span data-ttu-id="939ec-113">此值对象可用于将用户常数作为参数传递。</span><span class="sxs-lookup"><span data-stu-id="939ec-113">This value object can be used to pass user constants as parameters.</span></span>  
  
 <span data-ttu-id="939ec-114">如果值的类型为基元类型，则其初始值为零或 null。</span><span class="sxs-lookup"><span data-stu-id="939ec-114">If the type of the value is a primitive type, its initial value is zero or null.</span></span> <span data-ttu-id="939ec-115">使用 [ICorDebugGenericValue：： SetValue](icordebuggenericvalue-setvalue-method.md) 设置基元类型的值。</span><span class="sxs-lookup"><span data-stu-id="939ec-115">Use [ICorDebugGenericValue::SetValue](icordebuggenericvalue-setvalue-method.md) to set the value of a primitive type.</span></span>  
  
 <span data-ttu-id="939ec-116">如果 ELEMENT_TYPE_CLASS 的值 `elementType` ，则将获取 `ppValue`) 表示 null 对象引用的 "ICorDebugReferenceValue" (。</span><span class="sxs-lookup"><span data-stu-id="939ec-116">If the value of `elementType` is ELEMENT_TYPE_CLASS, you get an "ICorDebugReferenceValue" (returned in `ppValue`) representing the null object reference.</span></span> <span data-ttu-id="939ec-117">您可以使用此对象将 null 传递给具有对象引用参数的函数求值。</span><span class="sxs-lookup"><span data-stu-id="939ec-117">You can use this object to pass null to a function evaluation that has object reference parameters.</span></span> <span data-ttu-id="939ec-118">不能将设置 `ICorDebugValue` 为任何内容; 它始终保留为 null。</span><span class="sxs-lookup"><span data-stu-id="939ec-118">You cannot set the `ICorDebugValue` to anything; it always remains null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="939ec-119">要求</span><span class="sxs-lookup"><span data-stu-id="939ec-119">Requirements</span></span>  

 <span data-ttu-id="939ec-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="939ec-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="939ec-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="939ec-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="939ec-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="939ec-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="939ec-123">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="939ec-123">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="939ec-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="939ec-124">See also</span></span>

- [<span data-ttu-id="939ec-125">CreateValueForType 方法</span><span class="sxs-lookup"><span data-stu-id="939ec-125">CreateValueForType Method</span></span>](icordebugeval2-createvaluefortype-method.md)
- [<span data-ttu-id="939ec-126">ICorDebugEval 接口</span><span class="sxs-lookup"><span data-stu-id="939ec-126">ICorDebugEval Interface</span></span>](icordebugeval-interface.md)
