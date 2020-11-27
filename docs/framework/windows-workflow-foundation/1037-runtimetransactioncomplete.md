---
title: 1037 - RuntimeTransactionComplete
ms.date: 03/30/2017
ms.assetid: 2c8c31e0-42a9-4f46-865b-2da9ab16a0ba
ms.openlocfilehash: ad05151a1497ea4b31e0fe33fe2983c1f145f224
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96294243"
---
# <a name="1037---runtimetransactioncomplete"></a><span data-ttu-id="ccd26-102">1037 - RuntimeTransactionComplete</span><span class="sxs-lookup"><span data-stu-id="ccd26-102">1037 - RuntimeTransactionComplete</span></span>

## <a name="properties"></a><span data-ttu-id="ccd26-103">属性</span><span class="sxs-lookup"><span data-stu-id="ccd26-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="ccd26-104">ID</span><span class="sxs-lookup"><span data-stu-id="ccd26-104">ID</span></span>|<span data-ttu-id="ccd26-105">1037</span><span class="sxs-lookup"><span data-stu-id="ccd26-105">1037</span></span>|  
|<span data-ttu-id="ccd26-106">关键字</span><span class="sxs-lookup"><span data-stu-id="ccd26-106">Keywords</span></span>|<span data-ttu-id="ccd26-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="ccd26-107">WFRuntime</span></span>|  
|<span data-ttu-id="ccd26-108">级别</span><span class="sxs-lookup"><span data-stu-id="ccd26-108">Level</span></span>|<span data-ttu-id="ccd26-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="ccd26-109">Verbose</span></span>|  
|<span data-ttu-id="ccd26-110">通道</span><span class="sxs-lookup"><span data-stu-id="ccd26-110">Channel</span></span>|<span data-ttu-id="ccd26-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="ccd26-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="ccd26-112">描述</span><span class="sxs-lookup"><span data-stu-id="ccd26-112">Description</span></span>  

 <span data-ttu-id="ccd26-113">指示运行时事务已完成。</span><span class="sxs-lookup"><span data-stu-id="ccd26-113">Indicates the runtime transaction has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="ccd26-114">消息</span><span class="sxs-lookup"><span data-stu-id="ccd26-114">Message</span></span>  

 <span data-ttu-id="ccd26-115">运行时事务已完成，状态为“%1”。</span><span class="sxs-lookup"><span data-stu-id="ccd26-115">The runtime transaction has completed with the state '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="ccd26-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="ccd26-116">Details</span></span>  
  
|<span data-ttu-id="ccd26-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="ccd26-117">Data Item Name</span></span>|<span data-ttu-id="ccd26-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="ccd26-118">Data Item Type</span></span>|<span data-ttu-id="ccd26-119">说明</span><span class="sxs-lookup"><span data-stu-id="ccd26-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="ccd26-120">状态</span><span class="sxs-lookup"><span data-stu-id="ccd26-120">State</span></span>|<span data-ttu-id="ccd26-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccd26-121">xs:string</span></span>|<span data-ttu-id="ccd26-122">事务的状态。</span><span class="sxs-lookup"><span data-stu-id="ccd26-122">The state of the transaction.</span></span>|  
|<span data-ttu-id="ccd26-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="ccd26-123">AppDomain</span></span>|<span data-ttu-id="ccd26-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="ccd26-124">xs:string</span></span>|<span data-ttu-id="ccd26-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="ccd26-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
