---
title: 3502 - InferredOperationDescription
ms.date: 03/30/2017
ms.assetid: 6aebb614-3c72-4537-ba11-3cc7200ef1f1
ms.openlocfilehash: 05278067e3f86612ee4aafbe7d5eb66dc934cb85
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96242105"
---
# <a name="3502---inferredoperationdescription"></a><span data-ttu-id="e3501-102">3502 - InferredOperationDescription</span><span class="sxs-lookup"><span data-stu-id="e3501-102">3502 - InferredOperationDescription</span></span>

## <a name="properties"></a><span data-ttu-id="e3501-103">属性</span><span class="sxs-lookup"><span data-stu-id="e3501-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="e3501-104">ID</span><span class="sxs-lookup"><span data-stu-id="e3501-104">ID</span></span>|<span data-ttu-id="e3501-105">3502</span><span class="sxs-lookup"><span data-stu-id="e3501-105">3502</span></span>|  
|<span data-ttu-id="e3501-106">关键字</span><span class="sxs-lookup"><span data-stu-id="e3501-106">Keywords</span></span>|<span data-ttu-id="e3501-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="e3501-107">WFServices</span></span>|  
|<span data-ttu-id="e3501-108">Level</span><span class="sxs-lookup"><span data-stu-id="e3501-108">Level</span></span>|<span data-ttu-id="e3501-109">信息</span><span class="sxs-lookup"><span data-stu-id="e3501-109">Information</span></span>|  
|<span data-ttu-id="e3501-110">通道</span><span class="sxs-lookup"><span data-stu-id="e3501-110">Channel</span></span>|<span data-ttu-id="e3501-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="e3501-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="e3501-112">描述</span><span class="sxs-lookup"><span data-stu-id="e3501-112">Description</span></span>  

 <span data-ttu-id="e3501-113">指示已从 WorkflowService 中推断出 OperationDescription。</span><span class="sxs-lookup"><span data-stu-id="e3501-113">Indicates an OperationDescription has been inferred from WorkflowService.</span></span>  
  
## <a name="message"></a><span data-ttu-id="e3501-114">消息</span><span class="sxs-lookup"><span data-stu-id="e3501-114">Message</span></span>  

 <span data-ttu-id="e3501-115">已从 WorkflowService 中推断出协定“%2”中含有 Name='%1' 的 OperationDescription。</span><span class="sxs-lookup"><span data-stu-id="e3501-115">OperationDescription with Name='%1' in contract '%2' has been inferred from WorkflowService.</span></span> <span data-ttu-id="e3501-116">IsOneWay=%3。</span><span class="sxs-lookup"><span data-stu-id="e3501-116">IsOneWay=%3.</span></span>  
  
## <a name="details"></a><span data-ttu-id="e3501-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="e3501-117">Details</span></span>  
  
|<span data-ttu-id="e3501-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="e3501-118">Data Item Name</span></span>|<span data-ttu-id="e3501-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="e3501-119">Data Item Type</span></span>|<span data-ttu-id="e3501-120">描述</span><span class="sxs-lookup"><span data-stu-id="e3501-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="e3501-121">OperationName</span><span class="sxs-lookup"><span data-stu-id="e3501-121">OperationName</span></span>|<span data-ttu-id="e3501-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="e3501-122">xs:string</span></span>|<span data-ttu-id="e3501-123">操作的名称。</span><span class="sxs-lookup"><span data-stu-id="e3501-123">The name of the operation.</span></span>|  
|<span data-ttu-id="e3501-124">ContractName</span><span class="sxs-lookup"><span data-stu-id="e3501-124">ContractName</span></span>|<span data-ttu-id="e3501-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="e3501-125">xs:string</span></span>|<span data-ttu-id="e3501-126">协定的名称。</span><span class="sxs-lookup"><span data-stu-id="e3501-126">The name of the contract.</span></span>|  
|<span data-ttu-id="e3501-127">IsOneWay</span><span class="sxs-lookup"><span data-stu-id="e3501-127">IsOneWay</span></span>|<span data-ttu-id="e3501-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e3501-128">xs:string</span></span>|<span data-ttu-id="e3501-129">true 或 false 指示协定是否为单向。</span><span class="sxs-lookup"><span data-stu-id="e3501-129">True or False indicating if the contract is one-way.</span></span>|  
|<span data-ttu-id="e3501-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="e3501-130">AppDomain</span></span>|<span data-ttu-id="e3501-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="e3501-131">xs:string</span></span>|<span data-ttu-id="e3501-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="e3501-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
