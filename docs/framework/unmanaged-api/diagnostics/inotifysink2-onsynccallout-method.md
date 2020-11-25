---
title: INotifySink2::OnSyncCallOut 方法
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallOut
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallOut
helpviewer_keywords:
- INotifySink2::OnSyncCallOut method [.NET Framework debugging]
- OnSyncCallOut method [.NET Framework debugging]
ms.assetid: 97f15656-8677-4079-8553-a1d8603355d6
topic_type:
- apiref
ms.openlocfilehash: 00f6032f41caf54d7366de30a449f1ae76e8bbd0
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719978"
---
# <a name="inotifysink2onsynccallout-method"></a><span data-ttu-id="5218b-102">INotifySink2::OnSyncCallOut 方法</span><span class="sxs-lookup"><span data-stu-id="5218b-102">INotifySink2::OnSyncCallOut Method</span></span>

<span data-ttu-id="5218b-103">在调用时调用。</span><span class="sxs-lookup"><span data-stu-id="5218b-103">Gets invoked when a call is out.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5218b-104">语法</span><span class="sxs-lookup"><span data-stu-id="5218b-104">Syntax</span></span>  
  
```cpp  
HRESULT OnSyncCallOut  
(  
    [in]  CALL_ID  in_CallID,  
    [out, size_is(, *out_pBufferSize)] BYTE**  out_ppBuffer,  
    [out] DWORD*   out_pBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5218b-105">参数</span><span class="sxs-lookup"><span data-stu-id="5218b-105">Parameters</span></span>  

 `in_CallID`  
 <span data-ttu-id="5218b-106">中传出的调用的 ID。请参阅 [CALL_ID 结构](call-id-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="5218b-106">[in] ID of the call that is out. See [CALL_ID Structure](call-id-structure.md).</span></span>  
  
 `out_ppBuffer`  
 <span data-ttu-id="5218b-107">弄调用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="5218b-107">[out] Call buffer.</span></span>  
  
 `out_pBufferSize`  
 <span data-ttu-id="5218b-108">弄调用缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5218b-108">[out] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5218b-109">返回值</span><span class="sxs-lookup"><span data-stu-id="5218b-109">Return Value</span></span>  

 <span data-ttu-id="5218b-110">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="5218b-110">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5218b-111">要求</span><span class="sxs-lookup"><span data-stu-id="5218b-111">Requirements</span></span>  

 <span data-ttu-id="5218b-112">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="5218b-112">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5218b-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5218b-113">See also</span></span>

- [<span data-ttu-id="5218b-114">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="5218b-114">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="5218b-115">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="5218b-115">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="5218b-116">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="5218b-116">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
