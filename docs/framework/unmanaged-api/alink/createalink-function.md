---
title: CreateALink 函数
ms.date: 03/30/2017
api_name:
- CreateALink
api_location:
- alink.dll
api_type:
- DLLExport
f1_keywords:
- CreateALink
helpviewer_keywords:
- CreateALink function
- Alink API, CreateALink function
ms.assetid: fc73bcb9-6af6-44d8-bc39-2f4400325dae
topic_type:
- apiref
ms.openlocfilehash: 98c6ed4657dc69554a9fcca27145f65c621492f4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95683726"
---
# <a name="createalink-function"></a><span data-ttu-id="3e784-102">CreateALink 函数</span><span class="sxs-lookup"><span data-stu-id="3e784-102">CreateALink Function</span></span>

<span data-ttu-id="3e784-103">创建程序集链接器的实例，并设置指向指定接口的指针。</span><span class="sxs-lookup"><span data-stu-id="3e784-103">Creates an instance of the Assembly Linker and sets a pointer to the specified interface.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3e784-104">语法</span><span class="sxs-lookup"><span data-stu-id="3e784-104">Syntax</span></span>  
  
```cpp  
HRESULT CreateALink (  
   REFIID riid,  
   IUnknown **ppInterface  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3e784-105">参数</span><span class="sxs-lookup"><span data-stu-id="3e784-105">Parameters</span></span>  
  
|<span data-ttu-id="3e784-106">参数</span><span class="sxs-lookup"><span data-stu-id="3e784-106">Parameter</span></span>|<span data-ttu-id="3e784-107">说明</span><span class="sxs-lookup"><span data-stu-id="3e784-107">Description</span></span>|  
|---------------|-----------------|  
|`riid`|<span data-ttu-id="3e784-108">某个程序集链接器接口的物理名称。</span><span class="sxs-lookup"><span data-stu-id="3e784-108">The physical name of one of the Assembly Linker interfaces.</span></span>|  
|`ppInterface`|<span data-ttu-id="3e784-109">成功完成后的位置包含指向接口的指针 `riid` 。</span><span class="sxs-lookup"><span data-stu-id="3e784-109">The location that on successful completion contains a pointer to the `riid` interface.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3e784-110">要求</span><span class="sxs-lookup"><span data-stu-id="3e784-110">Requirements</span></span>  

 <span data-ttu-id="3e784-111">**库**： alink.dll</span><span class="sxs-lookup"><span data-stu-id="3e784-111">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e784-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3e784-112">See also</span></span>

- [<span data-ttu-id="3e784-113">Al.exe（程序集链接器）</span><span class="sxs-lookup"><span data-stu-id="3e784-113">Al.exe (Assembly Linker)</span></span>](../../tools/al-exe-assembly-linker.md)
