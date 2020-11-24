---
title: IMetaDataEmit::SetPermissionSetProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.SetPermissionSetProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SetPermissionSetProps
helpviewer_keywords:
- SetPermissionSetProps method [.NET Framework metadata]
- IMetaDataEmit::SetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 8eaee971-40bf-45e2-a3d8-6e57674213b6
topic_type:
- apiref
ms.openlocfilehash: 4c3e0953d71020ba62ee4ab68aa9e21ea3f0f521
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95675030"
---
# <a name="imetadataemitsetpermissionsetprops-method"></a><span data-ttu-id="f2b76-102">IMetaDataEmit::SetPermissionSetProps 方法</span><span class="sxs-lookup"><span data-stu-id="f2b76-102">IMetaDataEmit::SetPermissionSetProps Method</span></span>

<span data-ttu-id="f2b76-103">设置或更新通过之前调用 [IMetaDataEmit：:D efinepermissionset](imetadataemit-definepermissionset-method.md)定义的权限集的元数据签名的功能。</span><span class="sxs-lookup"><span data-stu-id="f2b76-103">Sets or updates features of the metadata signature of a permission set defined by a prior call to [IMetaDataEmit::DefinePermissionSet](imetadataemit-definepermissionset-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2b76-104">语法</span><span class="sxs-lookup"><span data-stu-id="f2b76-104">Syntax</span></span>  
  
```cpp  
HRESULT SetPermissionSetProps (
    [in]  mdToken         tk,
    [in]  DWORD           dwAction,
    [in]  void const      *pvPermission,
    [in]  ULONG           cbPermission,
    [out] mdPermission    *ppm
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2b76-105">参数</span><span class="sxs-lookup"><span data-stu-id="f2b76-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="f2b76-106">中表示要修饰的对象的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="f2b76-106">[in] A metadata token that represents the object to be decorated.</span></span>  
  
 `dwAction`  
 <span data-ttu-id="f2b76-107">中一个 [CorDeclSecurity](cordeclsecurity-enumeration.md) 值，指定要使用的声明性安全类型。</span><span class="sxs-lookup"><span data-stu-id="f2b76-107">[in] A [CorDeclSecurity](cordeclsecurity-enumeration.md) value that specifies the type of declarative security to be used.</span></span>  
  
 `pvPermission`  
 <span data-ttu-id="f2b76-108">中权限 BLOB。</span><span class="sxs-lookup"><span data-stu-id="f2b76-108">[in] The permission BLOB.</span></span>  
  
 `cbPermission`  
 <span data-ttu-id="f2b76-109">中的大小（以字节为单位） `pvPermission` 。</span><span class="sxs-lookup"><span data-stu-id="f2b76-109">[in] The size, in bytes, of `pvPermission`.</span></span>  
  
 `ppm`  
 <span data-ttu-id="f2b76-110">弄 `mdPermission` 表示更新的权限的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="f2b76-110">[out] An `mdPermission` metadata token that represents the updated permissions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2b76-111">要求</span><span class="sxs-lookup"><span data-stu-id="f2b76-111">Requirements</span></span>  

 <span data-ttu-id="f2b76-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2b76-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2b76-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="f2b76-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f2b76-114">**库：** 用作 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="f2b76-114">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f2b76-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2b76-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f2b76-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2b76-116">See also</span></span>

- [<span data-ttu-id="f2b76-117">IMetaDataEmit 接口</span><span class="sxs-lookup"><span data-stu-id="f2b76-117">IMetaDataEmit Interface</span></span>](imetadataemit-interface.md)
- [<span data-ttu-id="f2b76-118">IMetaDataEmit2 接口</span><span class="sxs-lookup"><span data-stu-id="f2b76-118">IMetaDataEmit2 Interface</span></span>](imetadataemit2-interface.md)
