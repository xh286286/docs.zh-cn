---
title: IMetaDataImport::GetPermissionSetProps 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetPermissionSetProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetPermissionSetProps
helpviewer_keywords:
- GetPermissionSetProps method [.NET Framework metadata]
- IMetaDataImport::GetPermissionSetProps method [.NET Framework metadata]
ms.assetid: 9855f0e4-12c0-4d3d-ab5d-d6bc52d25eae
topic_type:
- apiref
ms.openlocfilehash: 89c45c049ebadf9e1f16bef8d2626b4e2a17fb70
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729247"
---
# <a name="imetadataimportgetpermissionsetprops-method"></a><span data-ttu-id="048d3-102">IMetaDataImport::GetPermissionSetProps 方法</span><span class="sxs-lookup"><span data-stu-id="048d3-102">IMetaDataImport::GetPermissionSetProps Method</span></span>

<span data-ttu-id="048d3-103">获取与指定的权限标记所表示的关联的元数据 <xref:System.Security.PermissionSet?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="048d3-103">Gets the metadata associated with the <xref:System.Security.PermissionSet?displayProperty=nameWithType> represented by the specified Permission token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="048d3-104">语法</span><span class="sxs-lookup"><span data-stu-id="048d3-104">Syntax</span></span>  
  
```cpp  
HRESULT GetPermissionSetProps (  
   [in]  mdPermission      pm,  
   [out] DWORD             *pdwAction,
   [out] void const        **ppvPermission,
   [out] ULONG             *pcbPermission  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="048d3-105">参数</span><span class="sxs-lookup"><span data-stu-id="048d3-105">Parameters</span></span>  

 `pm`  
 <span data-ttu-id="048d3-106">中权限元数据标记，它表示要获取其元数据属性的权限集。</span><span class="sxs-lookup"><span data-stu-id="048d3-106">[in] The Permission metadata token that represents the permission set to get the metadata properties for.</span></span>  
  
 `pdwAction`  
 <span data-ttu-id="048d3-107">弄指向权限集的指针。</span><span class="sxs-lookup"><span data-stu-id="048d3-107">[out] A pointer to the permission set.</span></span>  
  
 `ppvPermission`  
 <span data-ttu-id="048d3-108">弄指向权限集的二进制元数据签名的指针。</span><span class="sxs-lookup"><span data-stu-id="048d3-108">[out] A pointer to the binary metadata signature of the permission set.</span></span>  
  
 `pcbPermission`  
 <span data-ttu-id="048d3-109">弄的大小（以字节为单位） `ppvPermission` 。</span><span class="sxs-lookup"><span data-stu-id="048d3-109">[out] The size in bytes of `ppvPermission`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="048d3-110">要求</span><span class="sxs-lookup"><span data-stu-id="048d3-110">Requirements</span></span>  

 <span data-ttu-id="048d3-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="048d3-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="048d3-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="048d3-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="048d3-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="048d3-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="048d3-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="048d3-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="048d3-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="048d3-115">See also</span></span>

- <xref:System.Security.PermissionSet>
- [<span data-ttu-id="048d3-116">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="048d3-116">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="048d3-117">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="048d3-117">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
