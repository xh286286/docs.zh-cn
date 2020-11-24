---
title: IMetaDataDispenserEx::OpenScopeOnITypeInfo 方法
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.OpenScopeOnITypeInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::OpenScopeOnITypeInfo
helpviewer_keywords:
- OpenScopeOnITypeInfo method [.NET Framework metadata]
- IMetaDataDispenserEx::OpenScopeOnITypeInfo method [.NET Framework metadata]
ms.assetid: 3480bbdb-c442-44a0-b7c6-333354503c52
topic_type:
- apiref
ms.openlocfilehash: 6056a64b354f69ce39692173da01892870fba9e1
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95682843"
---
# <a name="imetadatadispenserexopenscopeonitypeinfo-method"></a><span data-ttu-id="baf1b-102">IMetaDataDispenserEx::OpenScopeOnITypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="baf1b-102">IMetaDataDispenserEx::OpenScopeOnITypeInfo Method</span></span>

<span data-ttu-id="baf1b-103">未实现此方法。</span><span class="sxs-lookup"><span data-stu-id="baf1b-103">This method is not implemented.</span></span> <span data-ttu-id="baf1b-104">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="baf1b-104">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="baf1b-105">语法</span><span class="sxs-lookup"><span data-stu-id="baf1b-105">Syntax</span></span>  
  
```cpp  
HRESULT OpenScopeOnITypeInfo (  
    [in]  ITypeInfo   *pITI,  
    [in]  DWORD       dwOpenFlags,  
    [in]  REFIID      riid,  
    [out] IUnknown    **ppIUnk  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="baf1b-106">参数</span><span class="sxs-lookup"><span data-stu-id="baf1b-106">Parameters</span></span>  

 `pITI`  
 <span data-ttu-id="baf1b-107">中指向 [ITypeInfo](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo) 接口的指针，该接口提供要打开范围的类型信息。</span><span class="sxs-lookup"><span data-stu-id="baf1b-107">[in] Pointer to an [ITypeInfo](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo) interface that provides the type information on which to open the scope.</span></span>  
  
 `dwOpenFlags`  
 <span data-ttu-id="baf1b-108">中打开模式标志。</span><span class="sxs-lookup"><span data-stu-id="baf1b-108">[in] The open mode flags.</span></span>  
  
 `riid`  
 <span data-ttu-id="baf1b-109">中所需的接口。</span><span class="sxs-lookup"><span data-stu-id="baf1b-109">[in] The desired interface.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="baf1b-110">弄指向返回接口的指针的指针。</span><span class="sxs-lookup"><span data-stu-id="baf1b-110">[out] Pointer to a pointer to the returned interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="baf1b-111">要求</span><span class="sxs-lookup"><span data-stu-id="baf1b-111">Requirements</span></span>  

 <span data-ttu-id="baf1b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="baf1b-112">**Platform:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="baf1b-113">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="baf1b-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="baf1b-114">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="baf1b-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="baf1b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="baf1b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="baf1b-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="baf1b-116">See also</span></span>

- [<span data-ttu-id="baf1b-117">IMetaDataDispenserEx 接口</span><span class="sxs-lookup"><span data-stu-id="baf1b-117">IMetaDataDispenserEx Interface</span></span>](imetadatadispenserex-interface.md)
- [<span data-ttu-id="baf1b-118">IMetaDataDispenser 接口</span><span class="sxs-lookup"><span data-stu-id="baf1b-118">IMetaDataDispenser Interface</span></span>](imetadatadispenser-interface.md)
