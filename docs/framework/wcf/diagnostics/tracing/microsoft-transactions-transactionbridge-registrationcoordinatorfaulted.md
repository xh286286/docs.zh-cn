---
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted
ms.date: 03/30/2017
ms.assetid: 8193027e-9db2-4af9-a072-27300cd24330
ms.openlocfilehash: 5066501faf4c336e095910e7e2d8ba1186ba3386
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96251862"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfaulted"></a><span data-ttu-id="b16a0-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted</span><span class="sxs-lookup"><span data-stu-id="b16a0-102">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted</span></span>

<span data-ttu-id="b16a0-103">WS-AT 协议服务从其协调程序接收到错误作为对注册消息的响应。</span><span class="sxs-lookup"><span data-stu-id="b16a0-103">The WS-AT protocol service received a fault from its coordinator in response to a Register message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="b16a0-104">描述</span><span class="sxs-lookup"><span data-stu-id="b16a0-104">Description</span></span>  

 <span data-ttu-id="b16a0-105">在本地 TransactionManager 由于所返回的错误而无法向其上级 TransactionManager 注册时跟踪。</span><span class="sxs-lookup"><span data-stu-id="b16a0-105">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to a fault being returned.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="b16a0-106">疑难解答</span><span class="sxs-lookup"><span data-stu-id="b16a0-106">Troubleshooting</span></span>  

 <span data-ttu-id="b16a0-107">检查返回的错误的跟踪消息。</span><span class="sxs-lookup"><span data-stu-id="b16a0-107">Inspect the trace message for the fault returned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b16a0-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b16a0-108">See also</span></span>

- [<span data-ttu-id="b16a0-109">跟踪</span><span class="sxs-lookup"><span data-stu-id="b16a0-109">Tracing</span></span>](index.md)
- [<span data-ttu-id="b16a0-110">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="b16a0-110">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="b16a0-111">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="b16a0-111">Administration and Diagnostics</span></span>](../index.md)
