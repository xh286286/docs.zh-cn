---
title: Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt
ms.date: 03/30/2017
ms.assetid: 3e8fc825-9f22-47e7-9c16-d64ef291c932
ms.openlocfilehash: 9ad9dc9fd078f7ad4c0934c8bf9bb73feb935014
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96236645"
---
# <a name="microsofttransactionstransactionbridgevolatileparticipantindoubt"></a><span data-ttu-id="22417-102">Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt</span><span class="sxs-lookup"><span data-stu-id="22417-102">Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt</span></span>

<span data-ttu-id="22417-103">协议服务从无法识别的可变参与者接收到已准备或重播消息。</span><span class="sxs-lookup"><span data-stu-id="22417-103">The WS-AT protocol service received a Prepared or Replay message from an unrecognized volatile participant.</span></span> <span data-ttu-id="22417-104">已向参与者返回错误，声明事务的结果不确定。</span><span class="sxs-lookup"><span data-stu-id="22417-104">A fault was returned to the participant, declares that the transaction's outcome is in doubt.</span></span>  
  
## <a name="description"></a><span data-ttu-id="22417-105">描述</span><span class="sxs-lookup"><span data-stu-id="22417-105">Description</span></span>  

 <span data-ttu-id="22417-106">在本地事务管理器从它已经忘记的可变参与者接收到已准备或重播消息时进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="22417-106">Traced when the local Transaction Manager receives a Prepared or Replay message from a Volatile enlistment that it has already forgotten.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="22417-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="22417-107">Troubleshooting</span></span>  

 <span data-ttu-id="22417-108">调查来自可变参与者的最新消息的可能原因。</span><span class="sxs-lookup"><span data-stu-id="22417-108">Investigate potential causes of late messages coming from the Volatile participant.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22417-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22417-109">See also</span></span>

- [<span data-ttu-id="22417-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="22417-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="22417-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="22417-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="22417-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="22417-112">Administration and Diagnostics</span></span>](../index.md)
