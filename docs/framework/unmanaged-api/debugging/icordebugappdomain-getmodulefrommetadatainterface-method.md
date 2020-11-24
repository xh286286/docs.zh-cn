---
title: ICorDebugAppDomain::GetModuleFromMetaDataInterface 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetModuleFromMetaDataInterface
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetModuleFromMetaDataInterface
helpviewer_keywords:
- ICorDebugAppDomain::GetModuleFromMetaDatainterface method [.NET Framework debugging]
- GetModuleFromMetaDatainterface method [.NET Framework debugging]
ms.assetid: f35225b3-5dda-4d5a-913d-b3373e9ab81e
topic_type:
- apiref
ms.openlocfilehash: 5dede67412711736d269386a20446cf45fab1619
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95672196"
---
# <a name="icordebugappdomaingetmodulefrommetadatainterface-method"></a><span data-ttu-id="da3d0-102">ICorDebugAppDomain::GetModuleFromMetaDataInterface 方法</span><span class="sxs-lookup"><span data-stu-id="da3d0-102">ICorDebugAppDomain::GetModuleFromMetaDataInterface Method</span></span>

<span data-ttu-id="da3d0-103">获取与给定的元数据接口相对应的模块。</span><span class="sxs-lookup"><span data-stu-id="da3d0-103">Gets the module that corresponds to the given metadata interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da3d0-104">语法</span><span class="sxs-lookup"><span data-stu-id="da3d0-104">Syntax</span></span>  
  
```cpp  
HRESULT GetModuleFromMetaDataInterface (  
    [in] IUnknown           *pIMetaData,  
    [out] ICorDebugModule  **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="da3d0-105">参数</span><span class="sxs-lookup"><span data-stu-id="da3d0-105">Parameters</span></span>  

 `pIMetaData`  
 <span data-ttu-id="da3d0-106">中指向对象的指针，该对象为 [元数据接口](../metadata/metadata-interfaces.md)之一。</span><span class="sxs-lookup"><span data-stu-id="da3d0-106">[in] A pointer to an object that is one of the [Metadata interfaces](../metadata/metadata-interfaces.md).</span></span>  
  
 `ppModule`  
 <span data-ttu-id="da3d0-107">弄指向 ICorDebugModule 对象的地址的指针，该对象表示与给定的元数据接口相对应的模块。</span><span class="sxs-lookup"><span data-stu-id="da3d0-107">[out] A pointer to the address of an ICorDebugModule object that represents the module corresponding to the given metadata interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da3d0-108">要求</span><span class="sxs-lookup"><span data-stu-id="da3d0-108">Requirements</span></span>  

 <span data-ttu-id="da3d0-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="da3d0-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da3d0-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="da3d0-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="da3d0-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="da3d0-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="da3d0-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da3d0-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
