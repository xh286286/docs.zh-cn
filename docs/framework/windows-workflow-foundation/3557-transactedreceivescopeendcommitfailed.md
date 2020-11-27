---
title: 3557 - TransactedReceiveScopeEndCommitFailed
ms.date: 03/30/2017
ms.assetid: 079f0188-8146-49ee-b6ae-a08f4e4d2b9b
ms.openlocfilehash: 4a4979047481687ef0d5c9d5891dec8f2826beed
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96263654"
---
# <a name="3557---transactedreceivescopeendcommitfailed"></a><span data-ttu-id="55723-102">3557 - TransactedReceiveScopeEndCommitFailed</span><span class="sxs-lookup"><span data-stu-id="55723-102">3557 - TransactedReceiveScopeEndCommitFailed</span></span>

## <a name="properties"></a><span data-ttu-id="55723-103">属性</span><span class="sxs-lookup"><span data-stu-id="55723-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="55723-104">ID</span><span class="sxs-lookup"><span data-stu-id="55723-104">ID</span></span>|<span data-ttu-id="55723-105">3557</span><span class="sxs-lookup"><span data-stu-id="55723-105">3557</span></span>|  
|<span data-ttu-id="55723-106">关键字</span><span class="sxs-lookup"><span data-stu-id="55723-106">Keywords</span></span>|<span data-ttu-id="55723-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="55723-107">WFServices</span></span>|  
|<span data-ttu-id="55723-108">Level</span><span class="sxs-lookup"><span data-stu-id="55723-108">Level</span></span>|<span data-ttu-id="55723-109">信息</span><span class="sxs-lookup"><span data-stu-id="55723-109">Information</span></span>|  
|<span data-ttu-id="55723-110">通道</span><span class="sxs-lookup"><span data-stu-id="55723-110">Channel</span></span>|<span data-ttu-id="55723-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="55723-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="55723-112">描述</span><span class="sxs-lookup"><span data-stu-id="55723-112">Description</span></span>  

 <span data-ttu-id="55723-113">指示对 CommittableTransaction 上的 EndCommit 的调用引发 TransactionException。</span><span class="sxs-lookup"><span data-stu-id="55723-113">Indicates the call to EndCommit on a CommittableTransaction threw a TransactionException.</span></span>  
  
## <a name="message"></a><span data-ttu-id="55723-114">消息</span><span class="sxs-lookup"><span data-stu-id="55723-114">Message</span></span>  

 <span data-ttu-id="55723-115">ID 为“%1”的 CommittableTransaction 上的 EndCommit 调用引发了具有以下消息的 TransactionException:“%2”。</span><span class="sxs-lookup"><span data-stu-id="55723-115">The call to EndCommit on the CommittableTransaction with id = '%1' threw a TransactionException with the following message: '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="55723-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="55723-116">Details</span></span>  
  
|<span data-ttu-id="55723-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="55723-117">Data Item Name</span></span>|<span data-ttu-id="55723-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="55723-118">Data Item Type</span></span>|<span data-ttu-id="55723-119">描述</span><span class="sxs-lookup"><span data-stu-id="55723-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="55723-120">TransactionId</span><span class="sxs-lookup"><span data-stu-id="55723-120">TransactionId</span></span>|<span data-ttu-id="55723-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="55723-121">xs:string</span></span>|<span data-ttu-id="55723-122">CommittableTransaction 的 ID。</span><span class="sxs-lookup"><span data-stu-id="55723-122">The id of the CommittableTransaction.</span></span>|  
|<span data-ttu-id="55723-123">异常</span><span class="sxs-lookup"><span data-stu-id="55723-123">Exception</span></span>|<span data-ttu-id="55723-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="55723-124">xs:string</span></span>|<span data-ttu-id="55723-125">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="55723-125">The exception details for the exception</span></span>|  
|<span data-ttu-id="55723-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="55723-126">AppDomain</span></span>|<span data-ttu-id="55723-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="55723-127">xs:string</span></span>|<span data-ttu-id="55723-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="55723-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
