---
title: 216 - MessageSentByTransport
ms.date: 03/30/2017
ms.assetid: 150c3167-4154-4225-8d94-57cc94341233
ms.openlocfilehash: b3e9e1a48951ad5a2e5e7820dc1828c20e310635
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96278903"
---
# <a name="216---messagesentbytransport"></a><span data-ttu-id="20678-102">216 - MessageSentByTransport</span><span class="sxs-lookup"><span data-stu-id="20678-102">216 - MessageSentByTransport</span></span>

## <a name="properties"></a><span data-ttu-id="20678-103">属性</span><span class="sxs-lookup"><span data-stu-id="20678-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="20678-104">ID</span><span class="sxs-lookup"><span data-stu-id="20678-104">ID</span></span>|<span data-ttu-id="20678-105">216</span><span class="sxs-lookup"><span data-stu-id="20678-105">216</span></span>|  
|<span data-ttu-id="20678-106">关键字</span><span class="sxs-lookup"><span data-stu-id="20678-106">Keywords</span></span>|<span data-ttu-id="20678-107">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="20678-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="20678-108">Level</span><span class="sxs-lookup"><span data-stu-id="20678-108">Level</span></span>|<span data-ttu-id="20678-109">信息</span><span class="sxs-lookup"><span data-stu-id="20678-109">Information</span></span>|  
|<span data-ttu-id="20678-110">通道</span><span class="sxs-lookup"><span data-stu-id="20678-110">Channel</span></span>|<span data-ttu-id="20678-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="20678-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="20678-112">描述</span><span class="sxs-lookup"><span data-stu-id="20678-112">Description</span></span>  

 <span data-ttu-id="20678-113">使用基于 TCP 的传输发送消息时发生此事件。</span><span class="sxs-lookup"><span data-stu-id="20678-113">This event occurs when a TCP-based transport sends a message.</span></span> <span data-ttu-id="20678-114">请注意，在传输级别上，单个操作可在客户端和服务之间交换多条消息。</span><span class="sxs-lookup"><span data-stu-id="20678-114">Note that at the transport level multiple messages can be exchanged between clients and services for a single operation.</span></span> <span data-ttu-id="20678-115">这可能是由于基础结构行为的特点，在此方面，安全性是一个很好的例子。</span><span class="sxs-lookup"><span data-stu-id="20678-115">This may be due to infrastructure behavior, security being a good example.</span></span> <span data-ttu-id="20678-116">因此，发出的 **MessageSentByTransport** 事件数因服务的绑定和其配置而异。</span><span class="sxs-lookup"><span data-stu-id="20678-116">Therefore, the number of **MessageSentByTransport** events that are emitted vary based on your service's binding and its configuration.</span></span>  
  
## <a name="message"></a><span data-ttu-id="20678-117">消息</span><span class="sxs-lookup"><span data-stu-id="20678-117">Message</span></span>  

 <span data-ttu-id="20678-118">传输向“%1”发送了一条消息。</span><span class="sxs-lookup"><span data-stu-id="20678-118">The transport sent a message to '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="20678-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="20678-119">Details</span></span>  
  
|<span data-ttu-id="20678-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="20678-120">Data Item Name</span></span>|<span data-ttu-id="20678-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="20678-121">Data Item Type</span></span>|<span data-ttu-id="20678-122">描述</span><span class="sxs-lookup"><span data-stu-id="20678-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="20678-123">目的地地址</span><span class="sxs-lookup"><span data-stu-id="20678-123">DestinationAddress</span></span>|`xs:string`|<span data-ttu-id="20678-124">将请求消息发送到的地址。</span><span class="sxs-lookup"><span data-stu-id="20678-124">The address that the request message was sent to.</span></span>|  
|<span data-ttu-id="20678-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="20678-125">HostReference</span></span>|<span data-ttu-id="20678-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="20678-126">xs:string</span></span>|<span data-ttu-id="20678-127">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="20678-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="20678-128">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="20678-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="20678-129">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="20678-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="20678-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="20678-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="20678-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="20678-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
