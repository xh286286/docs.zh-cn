---
title: Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 54b677f7-03ad-40f2-9c5d-297a8ad9bf90
ms.openlocfilehash: bd6c9124e6346437e2bb35df620e00bad13b60f3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96258941"
---
# <a name="microsofttransactionstransactionbridgeparticipantstatemachinefinished"></a><span data-ttu-id="efa9d-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="efa9d-102">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span></span>

<span data-ttu-id="efa9d-103">参与者列入的状态机进入已完成状态。</span><span class="sxs-lookup"><span data-stu-id="efa9d-103">The state machine for a participant enlistment entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="efa9d-104">描述</span><span class="sxs-lookup"><span data-stu-id="efa9d-104">Description</span></span>  

 <span data-ttu-id="efa9d-105">从属参与者列入已完成 2pc 处理时跟踪。</span><span class="sxs-lookup"><span data-stu-id="efa9d-105">Traced when a subordinate participant enlistment has completed 2pc processing.</span></span> <span data-ttu-id="efa9d-106">列入的结果可以是“已提交”或“已中止”。</span><span class="sxs-lookup"><span data-stu-id="efa9d-106">The outcome for the enlistment can be Committed or Aborted.</span></span> <span data-ttu-id="efa9d-107">此外，还会跟踪是否有参与者在“准备”过程中投票“只读”。</span><span class="sxs-lookup"><span data-stu-id="efa9d-107">It is also traced if any participant votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="efa9d-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="efa9d-108">See also</span></span>

- [<span data-ttu-id="efa9d-109">跟踪</span><span class="sxs-lookup"><span data-stu-id="efa9d-109">Tracing</span></span>](index.md)
- [<span data-ttu-id="efa9d-110">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="efa9d-110">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="efa9d-111">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="efa9d-111">Administration and Diagnostics</span></span>](../index.md)
