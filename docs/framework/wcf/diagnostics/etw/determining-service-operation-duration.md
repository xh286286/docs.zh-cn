---
title: 确定服务操作持续时间
ms.date: 03/30/2017
ms.assetid: e8a93a2c-2c20-48b3-8986-57e90e9aa908
ms.openlocfilehash: 2607efe0d469f1235ee3d43d62f5e9781681668d
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96254826"
---
# <a name="determining-service-operation-duration"></a><span data-ttu-id="7f7d6-102">确定服务操作持续时间</span><span class="sxs-lookup"><span data-stu-id="7f7d6-102">Determining service operation duration</span></span>

<span data-ttu-id="7f7d6-103">如果在 Windows Communication Foundation (WCF) 应用程序中启用了分析跟踪，则可以通过检查事件日志轻松确定服务操作的执行持续时间。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-103">If analytic tracing is enabled in a Windows Communication Foundation (WCF) application, the duration of execution for a service operation can easily be determined by examining the event log.</span></span>  <span data-ttu-id="7f7d6-104">本主题演示如何确定完成服务操作所需的时间量。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-104">This topic demonstrates how to determine the amount of time a service operation takes to complete.</span></span>  
  
### <a name="determining-service-operation-execution-duration"></a><span data-ttu-id="7f7d6-105">确定服务操作执行持续时间</span><span class="sxs-lookup"><span data-stu-id="7f7d6-105">Determining service operation execution duration</span></span>  
  
1. <span data-ttu-id="7f7d6-106">通过单击 " **开始**"、" **运行**" 和 "输入" 打开事件查看器 `eventvwr.exe` 。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-106">Open Event Viewer by clicking **Start**, **Run**, and entering `eventvwr.exe`.</span></span>  
  
2. <span data-ttu-id="7f7d6-107">如果尚未启用分析跟踪，请展开 " **应用程序和服务日志**"、" **Microsoft**"、" **Windows**"、" **应用程序服务器应用程序**"。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-107">If you haven’t enabled analytic tracing, expand **Applications and Services Logs**, **Microsoft**, **Windows**, **Application Server-Applications**.</span></span> <span data-ttu-id="7f7d6-108">选择 " **查看**"、" **显示分析和调试日志**"。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-108">Select **View**, **Show Analytic and Debug Logs**.</span></span> <span data-ttu-id="7f7d6-109">右键单击 " **分析** "，然后选择 " **启用日志**"。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-109">Right-click **Analytic** and select **Enable Log**.</span></span> <span data-ttu-id="7f7d6-110">保持事件查看器打开，以便在服务操作运行后可以查看跟踪。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-110">Leave Event Viewer open so that traces can be viewed after the service operation is run.</span></span>  
  
3. <span data-ttu-id="7f7d6-111">接下来，打开一个包含服务项目的 WCF 应用程序以及与该服务交互的客户端项目。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-111">Next, open a WCF application that includes a service project and a client project that interacts with that service.</span></span>  <span data-ttu-id="7f7d6-112">可以按照 [入门教程](../../getting-started-tutorial.md)创建此类应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-112">You can create such an application by following the [Getting Started Tutorial](../../getting-started-tutorial.md).</span></span>  <span data-ttu-id="7f7d6-113">如果已安装 WCF 示例，则可以打开 " [入门](../../samples/getting-started-sample.md)"，其中包含本教程中创建的已完成项目。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-113">If you have the WCF samples installed, you can open the [Getting Started](../../samples/getting-started-sample.md), which contains the completed project created in the tutorial.</span></span>  
  
4. <span data-ttu-id="7f7d6-114">按 **F5** 执行服务器应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-114">Execute the server application by pressing **F5**.</span></span> <span data-ttu-id="7f7d6-115">右键单击 **客户端** 项目，然后选择 " **调试**"、" **启动新实例**" 来执行客户端应用程序。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-115">Execute the client application by right-clicking on the **Client** project and selecting **Debug**, **Start New Instance**.</span></span>  
  
5. <span data-ttu-id="7f7d6-116">在事件查看器中，刷新分析日志，然后按事件 ID 对事件排序。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-116">In Event Viewer, refresh the Analytic log and sort the events by Event ID.</span></span>  <span data-ttu-id="7f7d6-117">查找事件 ID 为 [214-OperationCompleted](214-operationcompleted.md)的事件。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-117">Look for events with Event ID [214 - OperationCompleted](214-operationcompleted.md).</span></span>  <span data-ttu-id="7f7d6-118">这些事件将显示已完成的操作以及操作的持续时间。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-118">These events will show which operations have completed, and what the duration of the operation was.</span></span>  <span data-ttu-id="7f7d6-119">下面的事件显示 Add 操作的持续时间。</span><span class="sxs-lookup"><span data-stu-id="7f7d6-119">The following event shows the duration of an Add operation.</span></span>  
  
    ```output  
    An OperationInvoker completed the call to the 'Add' method.  The method call duration was '3' ms.  
    ```
