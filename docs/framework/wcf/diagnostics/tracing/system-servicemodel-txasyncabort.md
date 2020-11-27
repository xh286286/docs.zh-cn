---
title: System.ServiceModel.TxAsyncAbort
ms.date: 03/30/2017
ms.assetid: bce47ff2-abd0-4b58-8667-ebf1ef3580b8
ms.openlocfilehash: fd21428279a68cd8480b6ff0617bb2a70033a40d
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96269946"
---
# <a name="systemservicemodeltxasyncabort"></a><span data-ttu-id="32378-102">System.ServiceModel.TxAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="32378-102">System.ServiceModel.TxAsyncAbort</span></span>

<span data-ttu-id="32378-103">指定的事务被异步中止。</span><span class="sxs-lookup"><span data-stu-id="32378-103">The specified transaction was asynchronously aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="32378-104">描述</span><span class="sxs-lookup"><span data-stu-id="32378-104">Description</span></span>  

 <span data-ttu-id="32378-105">由于另一名参与者赞成中止，发生超时，或事务的参与者内部出现另一错误，因此当前事务被中止。</span><span class="sxs-lookup"><span data-stu-id="32378-105">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="32378-106">疑难解答</span><span class="sxs-lookup"><span data-stu-id="32378-106">Troubleshooting</span></span>  

 <span data-ttu-id="32378-107">如果该中止是意料之外的，请检查所有系统日志，以便确定发生该中止的真正原因。</span><span class="sxs-lookup"><span data-stu-id="32378-107">Check all system logs if this abort is unexpected to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32378-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="32378-108">See also</span></span>

- [<span data-ttu-id="32378-109">跟踪</span><span class="sxs-lookup"><span data-stu-id="32378-109">Tracing</span></span>](index.md)
- [<span data-ttu-id="32378-110">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="32378-110">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="32378-111">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="32378-111">Administration and Diagnostics</span></span>](../index.md)
