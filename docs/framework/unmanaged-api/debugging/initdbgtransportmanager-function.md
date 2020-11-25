---
title: InitDbgTransportManager 函数
ms.date: 03/30/2017
api_name:
- InitDbgTransportManager
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- InitDbgTransportManager
helpviewer_keywords:
- remote debugging API [Silverlight]
- InitDbgTransportManager function
- Silverlight, remote debugging
ms.assetid: a30102ff-c52e-48c9-b3a9-aa14286a42b2
topic_type:
- apiref
ms.openlocfilehash: a5b4783eadb8045733b9ebd6d10c4e31f7829498
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95716676"
---
# <a name="initdbgtransportmanager-function"></a><span data-ttu-id="f5a92-102">InitDbgTransportManager 函数</span><span class="sxs-lookup"><span data-stu-id="f5a92-102">InitDbgTransportManager Function</span></span>

<span data-ttu-id="f5a92-103">初始化传输管理器以连接到进程和运行时枚举的远程目标。</span><span class="sxs-lookup"><span data-stu-id="f5a92-103">Initializes the transport manager to connect to a remote target for process and runtime enumeration.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5a92-104">语法</span><span class="sxs-lookup"><span data-stu-id="f5a92-104">Syntax</span></span>  
  
```cpp  
HRESULT InitDbgTransportManager ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="f5a92-105">返回值</span><span class="sxs-lookup"><span data-stu-id="f5a92-105">Return Value</span></span>  

 <span data-ttu-id="f5a92-106">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5a92-106">S_OK</span></span>  
 <span data-ttu-id="f5a92-107">成功。</span><span class="sxs-lookup"><span data-stu-id="f5a92-107">Success.</span></span>  
  
 <span data-ttu-id="f5a92-108">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="f5a92-108">E_OUTOFMEMORY</span></span>  
 <span data-ttu-id="f5a92-109">该函数不能为传输管理器分配内存。</span><span class="sxs-lookup"><span data-stu-id="f5a92-109">The function was unable to allocate memory for a transport manager.</span></span>  
  
 <span data-ttu-id="f5a92-110">E_FAIL（或其他 E_ 返回代码）</span><span class="sxs-lookup"><span data-stu-id="f5a92-110">E_FAIL (or other E_ return codes)</span></span>  
 <span data-ttu-id="f5a92-111">其他故障。</span><span class="sxs-lookup"><span data-stu-id="f5a92-111">Other failures.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5a92-112">要求</span><span class="sxs-lookup"><span data-stu-id="f5a92-112">Requirements</span></span>  

 <span data-ttu-id="f5a92-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f5a92-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5a92-114">**标头：** CoreClrRemoteDebuggingInterfaces</span><span class="sxs-lookup"><span data-stu-id="f5a92-114">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="f5a92-115">**库：** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="f5a92-115">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="f5a92-116">**.NET Framework 版本：** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="f5a92-116">**.NET Framework Versions:** 3.5 SP1</span></span>
