---
title: IMetaDataImport2::GetPEKind 方法
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetPEKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetPEKind
helpviewer_keywords:
- GetPEKind method [.NET Framework metadata]
- IMetaDataImport2::GetPEKind method [.NET Framework metadata]
ms.assetid: d91c3d89-8022-4a4c-a2a2-a8af2c387507
topic_type:
- apiref
ms.openlocfilehash: d335beecc12e0c1c895e42888ad7172f78062ff7
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95702532"
---
# <a name="imetadataimport2getpekind-method"></a><span data-ttu-id="49232-102">IMetaDataImport2::GetPEKind 方法</span><span class="sxs-lookup"><span data-stu-id="49232-102">IMetaDataImport2::GetPEKind Method</span></span>

<span data-ttu-id="49232-103">获取一个值，该值标识可移植可执行文件中代码的性质 (PE) 文件（通常为 DLL 或 EXE 文件），该文件在当前的元数据范围内定义。</span><span class="sxs-lookup"><span data-stu-id="49232-103">Gets a value identifying the nature of the code in the portable executable (PE) file, typically a DLL or EXE file, that is defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49232-104">语法</span><span class="sxs-lookup"><span data-stu-id="49232-104">Syntax</span></span>  
  
```cpp  
HRESULT GetPEKind (  
   [out] DWORD *pdwPEKind,  
   [out] DWORD *pdwMachine  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="49232-105">参数</span><span class="sxs-lookup"><span data-stu-id="49232-105">Parameters</span></span>  

 `pdwPEKind`  
 <span data-ttu-id="49232-106">弄一个指针，指向描述 PE 文件的 [CorPEKind](corpekind-enumeration.md) 枚举的值。</span><span class="sxs-lookup"><span data-stu-id="49232-106">[out] A pointer to a value of the [CorPEKind](corpekind-enumeration.md) enumeration that describes the PE file.</span></span>  
  
 `pdwMachine`  
 <span data-ttu-id="49232-107">弄一个指针，指向用于标识计算机体系结构的值。</span><span class="sxs-lookup"><span data-stu-id="49232-107">[out] A pointer to a value that identifies the architecture of the machine.</span></span> <span data-ttu-id="49232-108">有关可能的值，请参阅下一节。</span><span class="sxs-lookup"><span data-stu-id="49232-108">See the next section for possible values.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="49232-109">注解</span><span class="sxs-lookup"><span data-stu-id="49232-109">Remarks</span></span>  

 <span data-ttu-id="49232-110">参数引用的值 `pdwMachine` 可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="49232-110">The value referenced by the `pdwMachine` parameter can be one of the following.</span></span>  
  
|<span data-ttu-id="49232-111">Value</span><span class="sxs-lookup"><span data-stu-id="49232-111">Value</span></span>|<span data-ttu-id="49232-112">计算机体系结构</span><span class="sxs-lookup"><span data-stu-id="49232-112">Machine architecture</span></span>|  
|-----------|--------------------------|  
|<span data-ttu-id="49232-113">IMAGE_FILE_MACHINE_I386</span><span class="sxs-lookup"><span data-stu-id="49232-113">IMAGE_FILE_MACHINE_I386</span></span><br /><br /> <span data-ttu-id="49232-114">0x014C</span><span class="sxs-lookup"><span data-stu-id="49232-114">0x014C</span></span>|<span data-ttu-id="49232-115">x86</span><span class="sxs-lookup"><span data-stu-id="49232-115">x86</span></span>|  
|<span data-ttu-id="49232-116">IMAGE_FILE_MACHINE_IA64</span><span class="sxs-lookup"><span data-stu-id="49232-116">IMAGE_FILE_MACHINE_IA64</span></span><br /><br /> <span data-ttu-id="49232-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="49232-117">0x0200</span></span>|<span data-ttu-id="49232-118">Intel IPF</span><span class="sxs-lookup"><span data-stu-id="49232-118">Intel IPF</span></span>|  
|<span data-ttu-id="49232-119">IMAGE_FILE_MACHINE_AMD64</span><span class="sxs-lookup"><span data-stu-id="49232-119">IMAGE_FILE_MACHINE_AMD64</span></span><br /><br /> <span data-ttu-id="49232-120">0x8664</span><span class="sxs-lookup"><span data-stu-id="49232-120">0x8664</span></span>|<span data-ttu-id="49232-121">X64</span><span class="sxs-lookup"><span data-stu-id="49232-121">x64</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="49232-122">要求</span><span class="sxs-lookup"><span data-stu-id="49232-122">Requirements</span></span>  

 <span data-ttu-id="49232-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="49232-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="49232-124">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="49232-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="49232-125">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="49232-125">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="49232-126">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="49232-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49232-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49232-127">See also</span></span>

- [<span data-ttu-id="49232-128">IMetaDataImport2 接口</span><span class="sxs-lookup"><span data-stu-id="49232-128">IMetaDataImport2 Interface</span></span>](imetadataimport2-interface.md)
- [<span data-ttu-id="49232-129">IMetaDataImport 接口</span><span class="sxs-lookup"><span data-stu-id="49232-129">IMetaDataImport Interface</span></span>](imetadataimport-interface.md)
- [<span data-ttu-id="49232-130">CorPEKind 枚举</span><span class="sxs-lookup"><span data-stu-id="49232-130">CorPEKind Enumeration</span></span>](corpekind-enumeration.md)
