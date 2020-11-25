---
title: IMetaDataImport::GetPinvokeMap 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport.GetPinvokeMap
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetPinvokeMap
helpviewer_keywords:
- IMetaDataImport::GetPinvokeMap method [.NET Framework metadata]
- GetPinvokeMap method [.NET Framework metadata]
ms.assetid: b8685c1e-b80c-4198-8eb3-748d6f48a99e
topic_type:
- apiref
ms.openlocfilehash: c34215f48190e60bd1a851f31b8b23f09491f4e1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95729234"
---
# <a name="imetadataimportgetpinvokemap-method"></a><span data-ttu-id="79c15-102">IMetaDataImport::GetPinvokeMap 方法</span><span class="sxs-lookup"><span data-stu-id="79c15-102">IMetaDataImport::GetPinvokeMap Method</span></span>

<span data-ttu-id="79c15-103">获取用于表示 PInvoke 调用的目标程序集的 ModuleRef 标记。</span><span class="sxs-lookup"><span data-stu-id="79c15-103">Gets a ModuleRef token to represent the target assembly of a PInvoke call.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79c15-104">语法</span><span class="sxs-lookup"><span data-stu-id="79c15-104">Syntax</span></span>  
  
```cpp  
HRESULT GetPinvokeMap (  
   [in]  mdToken       tk,  
   [out] DWORD         *pdwMappingFlags,  
   [out] LPWSTR        szImportName,  
   [in]  ULONG         cchImportName,  
   [out] ULONG         *pchImportName,  
   [out] mdModuleRef   *pmrImportDLL  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79c15-105">参数</span><span class="sxs-lookup"><span data-stu-id="79c15-105">Parameters</span></span>  

 `tk`  
 <span data-ttu-id="79c15-106">中要为其获取 PInvoke 映射元数据的 FieldDef 或 MethodDef 标记。</span><span class="sxs-lookup"><span data-stu-id="79c15-106">[in] A FieldDef or MethodDef token to get the PInvoke mapping metadata for.</span></span>  
  
 `pdwMappingFlags`  
 <span data-ttu-id="79c15-107">弄一个指针，指向用于映射的标志。</span><span class="sxs-lookup"><span data-stu-id="79c15-107">[out] A pointer to flags used for mapping.</span></span> <span data-ttu-id="79c15-108">此值是 [CorPinvokeMap](corpinvokemap-enumeration.md) 枚举中的位掩码。</span><span class="sxs-lookup"><span data-stu-id="79c15-108">This value is a bitmask from the [CorPinvokeMap](corpinvokemap-enumeration.md) enumeration.</span></span>  
  
 `szImportName`  
 <span data-ttu-id="79c15-109">弄非托管目标 DLL 的名称。</span><span class="sxs-lookup"><span data-stu-id="79c15-109">[out] The name of the unmanaged target DLL.</span></span>  
  
 `cchImportName`  
 <span data-ttu-id="79c15-110">中的大小（以宽字符为大小） `szImportName` 。</span><span class="sxs-lookup"><span data-stu-id="79c15-110">[in] The size in wide characters of `szImportName`.</span></span>  
  
 `pchImportName`  
 <span data-ttu-id="79c15-111">弄返回的宽字符数 `szImportName` 。</span><span class="sxs-lookup"><span data-stu-id="79c15-111">[out] The number of wide characters returned in `szImportName`.</span></span>  
  
 `pmrImportDLL`  
 <span data-ttu-id="79c15-112">弄一个指针，指向表示非托管目标对象库的 ModuleRef 标记。</span><span class="sxs-lookup"><span data-stu-id="79c15-112">[out] A pointer to a ModuleRef token that represents the unmanaged target object library.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79c15-113">要求</span><span class="sxs-lookup"><span data-stu-id="79c15-113">Requirements</span></span>  

 <span data-ttu-id="79c15-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79c15-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79c15-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="79c15-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="79c15-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="79c15-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="79c15-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79c15-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79c15-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="79c15-118">See also</span></span>

- [<span data-ttu-id="79c15-119">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="79c15-119">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="79c15-120">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="79c15-120">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
