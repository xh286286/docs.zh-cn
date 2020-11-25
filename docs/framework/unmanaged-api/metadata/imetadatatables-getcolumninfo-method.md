---
title: IMetaDataTables::GetColumnInfo 方法
ms.date: 10/10/2019
api_name:
- IMetaDataTables.GetColumnInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataTables::GetColumnInfo
helpviewer_keywords:
- IMetaDataTables::GetColumnInfo method [.NET Framework metadata]
- GetColumnInfo method [.NET Framework metadata]
ms.assetid: 68c160ea-ae7d-4750-985d-a038b2c8e7d9
topic_type:
- apiref
ms.openlocfilehash: 227d9ab67ab3091508232be3018ca520a6b5dcc6
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95711047"
---
# <a name="imetadatatablesgetcolumninfo-method"></a><span data-ttu-id="c42c6-102">IMetaDataTables::GetColumnInfo 方法</span><span class="sxs-lookup"><span data-stu-id="c42c6-102">IMetaDataTables::GetColumnInfo Method</span></span>

<span data-ttu-id="c42c6-103">获取有关指定表中指定列的数据。</span><span class="sxs-lookup"><span data-stu-id="c42c6-103">Gets data about the specified column in the specified table.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c42c6-104">语法</span><span class="sxs-lookup"><span data-stu-id="c42c6-104">Syntax</span></span>  
  
```cpp  
HRESULT GetColumnInfo (
    [in]  ULONG        ixTbl,  
    [in]  ULONG        ixCol,  
    [out] ULONG        *poCol,  
    [out] ULONG        *pcbCol,  
    [out] ULONG        *pType,  
    [out] const char   **ppName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c42c6-105">参数</span><span class="sxs-lookup"><span data-stu-id="c42c6-105">Parameters</span></span>

=======

 `ixTbl`  
 <span data-ttu-id="c42c6-106">中所需表的索引。</span><span class="sxs-lookup"><span data-stu-id="c42c6-106">[in] The index of the desired table.</span></span>  
  
 `ixCol`  
 <span data-ttu-id="c42c6-107">中所需列的索引。</span><span class="sxs-lookup"><span data-stu-id="c42c6-107">[in] The index of the desired column.</span></span>  
  
 `poCol`  
 <span data-ttu-id="c42c6-108">弄指向行中列的偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="c42c6-108">[out] A pointer to the offset of the column in the row.</span></span>  
  
 `pcbCol`  
 <span data-ttu-id="c42c6-109">弄一个指针，指向列的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="c42c6-109">[out] A pointer to the size, in bytes, of the column.</span></span>  
  
 `pType`  
 <span data-ttu-id="c42c6-110">弄一个指针，指向列中值的类型。</span><span class="sxs-lookup"><span data-stu-id="c42c6-110">[out] A pointer to the type of the values in the column.</span></span>  
  
 `ppName`  
 <span data-ttu-id="c42c6-111">弄指向列名的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="c42c6-111">[out] A pointer to a pointer to the column name.</span></span>  

## <a name="remarks"></a><span data-ttu-id="c42c6-112">注解</span><span class="sxs-lookup"><span data-stu-id="c42c6-112">Remarks</span></span>

<span data-ttu-id="c42c6-113">返回的列类型位于值的范围内：</span><span class="sxs-lookup"><span data-stu-id="c42c6-113">The returned column type falls within a range of values:</span></span>

| <span data-ttu-id="c42c6-114">pType</span><span class="sxs-lookup"><span data-stu-id="c42c6-114">pType</span></span>                    | <span data-ttu-id="c42c6-115">说明</span><span class="sxs-lookup"><span data-stu-id="c42c6-115">Description</span></span>   | <span data-ttu-id="c42c6-116">Helper 函数</span><span class="sxs-lookup"><span data-stu-id="c42c6-116">Helper function</span></span>                   |
|--------------------------|---------------|-----------------------------------|
| <span data-ttu-id="c42c6-117">`0`..`iRidMax`</span><span class="sxs-lookup"><span data-stu-id="c42c6-117">`0`..`iRidMax`</span></span><br><span data-ttu-id="c42c6-118"> (0. 63) </span><span class="sxs-lookup"><span data-stu-id="c42c6-118">(0..63)</span></span>   | <span data-ttu-id="c42c6-119">去掉</span><span class="sxs-lookup"><span data-stu-id="c42c6-119">Rid</span></span>           | <span data-ttu-id="c42c6-120">**IsRidType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-120">**IsRidType**</span></span><br><span data-ttu-id="c42c6-121">**IsRidOrToken**</span><span class="sxs-lookup"><span data-stu-id="c42c6-121">**IsRidOrToken**</span></span> |
| <span data-ttu-id="c42c6-122">`iCodedToken`..`iCodedTokenMax`</span><span class="sxs-lookup"><span data-stu-id="c42c6-122">`iCodedToken`..`iCodedTokenMax`</span></span><br><span data-ttu-id="c42c6-123"> (64.. 95) </span><span class="sxs-lookup"><span data-stu-id="c42c6-123">(64..95)</span></span> | <span data-ttu-id="c42c6-124">编码标记</span><span class="sxs-lookup"><span data-stu-id="c42c6-124">Coded token</span></span> | <span data-ttu-id="c42c6-125">**IsCodedTokenType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-125">**IsCodedTokenType**</span></span> <br><span data-ttu-id="c42c6-126">**IsRidOrToken**</span><span class="sxs-lookup"><span data-stu-id="c42c6-126">**IsRidOrToken**</span></span> |
| <span data-ttu-id="c42c6-127">`iSHORT` (96) </span><span class="sxs-lookup"><span data-stu-id="c42c6-127">`iSHORT` (96)</span></span>            | <span data-ttu-id="c42c6-128">Int16</span><span class="sxs-lookup"><span data-stu-id="c42c6-128">Int16</span></span>         | <span data-ttu-id="c42c6-129">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-129">**IsFixedType**</span></span>                   |
| <span data-ttu-id="c42c6-130">`iUSHORT` (97) </span><span class="sxs-lookup"><span data-stu-id="c42c6-130">`iUSHORT` (97)</span></span>           | <span data-ttu-id="c42c6-131">UInt16</span><span class="sxs-lookup"><span data-stu-id="c42c6-131">UInt16</span></span>        | <span data-ttu-id="c42c6-132">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-132">**IsFixedType**</span></span>                   |
| <span data-ttu-id="c42c6-133">`iLONG` (98) </span><span class="sxs-lookup"><span data-stu-id="c42c6-133">`iLONG` (98)</span></span>             | <span data-ttu-id="c42c6-134">Int32</span><span class="sxs-lookup"><span data-stu-id="c42c6-134">Int32</span></span>         | <span data-ttu-id="c42c6-135">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-135">**IsFixedType**</span></span>                   |
| <span data-ttu-id="c42c6-136">`iULONG` (99) </span><span class="sxs-lookup"><span data-stu-id="c42c6-136">`iULONG` (99)</span></span>            | <span data-ttu-id="c42c6-137">UInt32</span><span class="sxs-lookup"><span data-stu-id="c42c6-137">UInt32</span></span>        | <span data-ttu-id="c42c6-138">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-138">**IsFixedType**</span></span>                   |
| <span data-ttu-id="c42c6-139">`iBYTE` (100) </span><span class="sxs-lookup"><span data-stu-id="c42c6-139">`iBYTE` (100)</span></span>            | <span data-ttu-id="c42c6-140">Byte</span><span class="sxs-lookup"><span data-stu-id="c42c6-140">Byte</span></span>          | <span data-ttu-id="c42c6-141">**IsFixedType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-141">**IsFixedType**</span></span>                   |
| <span data-ttu-id="c42c6-142">`iSTRING` (101) </span><span class="sxs-lookup"><span data-stu-id="c42c6-142">`iSTRING` (101)</span></span>          | <span data-ttu-id="c42c6-143">String</span><span class="sxs-lookup"><span data-stu-id="c42c6-143">String</span></span>        | <span data-ttu-id="c42c6-144">**IsHeapType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-144">**IsHeapType**</span></span>                    |
| <span data-ttu-id="c42c6-145">`iGUID` (102) </span><span class="sxs-lookup"><span data-stu-id="c42c6-145">`iGUID` (102)</span></span>            | <span data-ttu-id="c42c6-146">GUID</span><span class="sxs-lookup"><span data-stu-id="c42c6-146">Guid</span></span>          | <span data-ttu-id="c42c6-147">**IsHeapType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-147">**IsHeapType**</span></span>                    |
| <span data-ttu-id="c42c6-148">`iBLOB` (103) </span><span class="sxs-lookup"><span data-stu-id="c42c6-148">`iBLOB` (103)</span></span>            | <span data-ttu-id="c42c6-149">Blob</span><span class="sxs-lookup"><span data-stu-id="c42c6-149">Blob</span></span>          | <span data-ttu-id="c42c6-150">**IsHeapType**</span><span class="sxs-lookup"><span data-stu-id="c42c6-150">**IsHeapType**</span></span>                    |

<span data-ttu-id="c42c6-151">存储在 *堆* 中的值 (即， `IsHeapType == true` 可以使用读取) ：</span><span class="sxs-lookup"><span data-stu-id="c42c6-151">Values that are stored in the *heap* (that is, `IsHeapType == true`) can be read using:</span></span>

- <span data-ttu-id="c42c6-152">`iSTRING`： **IMetadataTables. GetString**</span><span class="sxs-lookup"><span data-stu-id="c42c6-152">`iSTRING`: **IMetadataTables.GetString**</span></span>
- <span data-ttu-id="c42c6-153">`iGUID`： **IMetadataTables. GetGUID**</span><span class="sxs-lookup"><span data-stu-id="c42c6-153">`iGUID`: **IMetadataTables.GetGUID**</span></span>
- <span data-ttu-id="c42c6-154">`iBLOB`： **IMetadataTables. GetBlob**</span><span class="sxs-lookup"><span data-stu-id="c42c6-154">`iBLOB`: **IMetadataTables.GetBlob**</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c42c6-155">若要使用上表中定义的常量，请包含 `#define _DEFINE_META_DATA_META_CONSTANTS` *cor* 头文件提供的指令。</span><span class="sxs-lookup"><span data-stu-id="c42c6-155">To use the constants defined in the table above, include the directive `#define _DEFINE_META_DATA_META_CONSTANTS` provided by the *cor.h* header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c42c6-156">要求</span><span class="sxs-lookup"><span data-stu-id="c42c6-156">Requirements</span></span>  

 <span data-ttu-id="c42c6-157">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c42c6-157">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c42c6-158">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="c42c6-158">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c42c6-159">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="c42c6-159">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c42c6-160">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c42c6-160">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c42c6-161">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c42c6-161">See also</span></span>

- [<span data-ttu-id="c42c6-162">IMetaDataTables 接口</span><span class="sxs-lookup"><span data-stu-id="c42c6-162">IMetaDataTables Interface</span></span>](imetadatatables-interface.md)
- [<span data-ttu-id="c42c6-163">IMetaDataTables2 接口</span><span class="sxs-lookup"><span data-stu-id="c42c6-163">IMetaDataTables2 Interface</span></span>](imetadatatables2-interface.md)
