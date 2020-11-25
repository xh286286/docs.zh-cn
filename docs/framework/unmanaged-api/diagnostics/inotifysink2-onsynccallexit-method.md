---
title: INotifySink2::OnSyncCallExit 方法
ms.date: 03/30/2017
api_name:
- INotifySink2.OnSyncCallExit
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2::OnSyncCallExit
helpviewer_keywords:
- INotifySink2::OnSyncCallExit method [.NET Framework debugging]
- OnSyncCallExit method [.NET Framework debugging]
ms.assetid: d9d7600e-a8f5-443a-96de-67d26e130f2d
topic_type:
- apiref
ms.openlocfilehash: 9049cd42e9c10cdcff62b005094b56c9df9ce975
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95719991"
---
# <a name="inotifysink2onsynccallexit-method"></a><span data-ttu-id="4b42d-102">INotifySink2::OnSyncCallExit 方法</span><span class="sxs-lookup"><span data-stu-id="4b42d-102">INotifySink2::OnSyncCallExit Method</span></span>

<span data-ttu-id="4b42d-103">在退出调用时调用。</span><span class="sxs-lookup"><span data-stu-id="4b42d-103">Gets invoked when exiting a call.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b42d-104">语法</span><span class="sxs-lookup"><span data-stu-id="4b42d-104">Syntax</span></span>  
  
```cpp  
HRESULT OnSyncCallExit  
(  
    [in]  CALL_ID   in_CallID,  
    [out, size_is(, *out_pBufferSize)] BYTE**  out_ppBuffer,  
    [out] DWORD*    out_pBufferSize  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b42d-105">参数</span><span class="sxs-lookup"><span data-stu-id="4b42d-105">Parameters</span></span>  

 `in_CallID`  
 <span data-ttu-id="4b42d-106">中正在退出的调用的 ID。</span><span class="sxs-lookup"><span data-stu-id="4b42d-106">[in] ID of the call being exited.</span></span> <span data-ttu-id="4b42d-107">请参阅 [CALL_ID 结构](call-id-structure.md)。</span><span class="sxs-lookup"><span data-stu-id="4b42d-107">See [CALL_ID Structure](call-id-structure.md).</span></span>  
  
 `out_ppBuffer`  
 <span data-ttu-id="4b42d-108">弄调用缓冲区。</span><span class="sxs-lookup"><span data-stu-id="4b42d-108">[out] Call buffer.</span></span>  
  
 `out_pBufferSize`  
 <span data-ttu-id="4b42d-109">弄调用缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="4b42d-109">[out] Size of the call buffer, in bytes.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4b42d-110">返回值</span><span class="sxs-lookup"><span data-stu-id="4b42d-110">Return Value</span></span>  

 <span data-ttu-id="4b42d-111">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="4b42d-111">S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b42d-112">要求</span><span class="sxs-lookup"><span data-stu-id="4b42d-112">Requirements</span></span>  

 <span data-ttu-id="4b42d-113">**标头：** ProtocolNotify2 .idl</span><span class="sxs-lookup"><span data-stu-id="4b42d-113">**Header:** ProtocolNotify2.idl</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b42d-114">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b42d-114">See also</span></span>

- [<span data-ttu-id="4b42d-115">INotifySink2 接口</span><span class="sxs-lookup"><span data-stu-id="4b42d-115">INotifySink2 Interface</span></span>](inotifysink2-interface.md)
- [<span data-ttu-id="4b42d-116">INotifySource2 接口</span><span class="sxs-lookup"><span data-stu-id="4b42d-116">INotifySource2 Interface</span></span>](inotifysource2-interface.md)
- [<span data-ttu-id="4b42d-117">INotifyConnection2 接口</span><span class="sxs-lookup"><span data-stu-id="4b42d-117">INotifyConnection2 Interface</span></span>](inotifyconnection2-interface.md)
