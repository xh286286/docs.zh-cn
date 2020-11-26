---
title: 3501 - InferredContractDescription
ms.date: 03/30/2017
ms.assetid: 21a70849-4fc0-41d2-b9a4-db5aa2acdf1a
ms.openlocfilehash: 88a04c0eb6d12876592702ad4dba3a17aa8da122
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96245284"
---
# <a name="3501---inferredcontractdescription"></a><span data-ttu-id="e4c46-102">3501 - InferredContractDescription</span><span class="sxs-lookup"><span data-stu-id="e4c46-102">3501 - InferredContractDescription</span></span>

## <a name="properties"></a><span data-ttu-id="e4c46-103">属性</span><span class="sxs-lookup"><span data-stu-id="e4c46-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e4c46-104">ID</span><span class="sxs-lookup"><span data-stu-id="e4c46-104">ID</span></span>|<span data-ttu-id="e4c46-105">3501</span><span class="sxs-lookup"><span data-stu-id="e4c46-105">3501</span></span>|  
|<span data-ttu-id="e4c46-106">关键字</span><span class="sxs-lookup"><span data-stu-id="e4c46-106">Keywords</span></span>|<span data-ttu-id="e4c46-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="e4c46-107">WFServices</span></span>|  
|<span data-ttu-id="e4c46-108">Level</span><span class="sxs-lookup"><span data-stu-id="e4c46-108">Level</span></span>|<span data-ttu-id="e4c46-109">信息</span><span class="sxs-lookup"><span data-stu-id="e4c46-109">Information</span></span>|  
|<span data-ttu-id="e4c46-110">通道</span><span class="sxs-lookup"><span data-stu-id="e4c46-110">Channel</span></span>|<span data-ttu-id="e4c46-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="e4c46-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e4c46-112">描述</span><span class="sxs-lookup"><span data-stu-id="e4c46-112">Description</span></span>  

 <span data-ttu-id="e4c46-113">指示已从 WorkflowService 中推断出 ContractDescription。</span><span class="sxs-lookup"><span data-stu-id="e4c46-113">Indicates a ContractDescription has been inferred from WorkflowService.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e4c46-114">消息</span><span class="sxs-lookup"><span data-stu-id="e4c46-114">Message</span></span>  

 <span data-ttu-id="e4c46-115">已从 WorkflowService 中推断出含有 Name 为“%1”和 Namespace 为“%2”的 ContractDescription。</span><span class="sxs-lookup"><span data-stu-id="e4c46-115">ContractDescription with Name='%1' and Namespace='%2' has been inferred from WorkflowService.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e4c46-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="e4c46-116">Details</span></span>  
  
|<span data-ttu-id="e4c46-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e4c46-117">Data Item Name</span></span>|<span data-ttu-id="e4c46-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e4c46-118">Data Item Type</span></span>|<span data-ttu-id="e4c46-119">描述</span><span class="sxs-lookup"><span data-stu-id="e4c46-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e4c46-120">“属性”</span><span class="sxs-lookup"><span data-stu-id="e4c46-120">Name</span></span>|<span data-ttu-id="e4c46-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4c46-121">xs:string</span></span>|<span data-ttu-id="e4c46-122">ContractDescription 的名称。</span><span class="sxs-lookup"><span data-stu-id="e4c46-122">The name of the ContractDescription.</span></span>|  
|<span data-ttu-id="e4c46-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="e4c46-123">Namespace</span></span>|<span data-ttu-id="e4c46-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4c46-124">xs:string</span></span>|<span data-ttu-id="e4c46-125">ContractDescription 的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e4c46-125">The namespace of the ContractDescription.</span></span>|  
|<span data-ttu-id="e4c46-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e4c46-126">AppDomain</span></span>|<span data-ttu-id="e4c46-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4c46-127">xs:string</span></span>|<span data-ttu-id="e4c46-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e4c46-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
