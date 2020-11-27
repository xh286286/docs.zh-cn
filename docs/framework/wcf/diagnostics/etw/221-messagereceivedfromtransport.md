---
title: 221 - MessageReceivedFromTransport
ms.date: 03/30/2017
ms.assetid: 4995f0d5-c182-4d97-981f-6951da6df1fb
ms.openlocfilehash: 47e871b70e3ef2419543b4710c2988736665cb46
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96263095"
---
# <a name="221---messagereceivedfromtransport"></a><span data-ttu-id="25fcd-102">221 - MessageReceivedFromTransport</span><span class="sxs-lookup"><span data-stu-id="25fcd-102">221 - MessageReceivedFromTransport</span></span>

## <a name="properties"></a><span data-ttu-id="25fcd-103">属性</span><span class="sxs-lookup"><span data-stu-id="25fcd-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="25fcd-104">ID</span><span class="sxs-lookup"><span data-stu-id="25fcd-104">ID</span></span>|<span data-ttu-id="25fcd-105">221</span><span class="sxs-lookup"><span data-stu-id="25fcd-105">221</span></span>|  
|<span data-ttu-id="25fcd-106">关键字</span><span class="sxs-lookup"><span data-stu-id="25fcd-106">Keywords</span></span>|<span data-ttu-id="25fcd-107">EndToEndMonitoring，疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="25fcd-107">EndToEndMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="25fcd-108">Level</span><span class="sxs-lookup"><span data-stu-id="25fcd-108">Level</span></span>|<span data-ttu-id="25fcd-109">信息</span><span class="sxs-lookup"><span data-stu-id="25fcd-109">Information</span></span>|  
|<span data-ttu-id="25fcd-110">通道</span><span class="sxs-lookup"><span data-stu-id="25fcd-110">Channel</span></span>|<span data-ttu-id="25fcd-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="25fcd-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="25fcd-112">描述</span><span class="sxs-lookup"><span data-stu-id="25fcd-112">Description</span></span>  

 <span data-ttu-id="25fcd-113">服务模型从传输中接收消息时将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="25fcd-113">This event is emitted when the Service Model receives a message from the transport.</span></span>  
  
## <a name="message"></a><span data-ttu-id="25fcd-114">消息</span><span class="sxs-lookup"><span data-stu-id="25fcd-114">Message</span></span>  

 <span data-ttu-id="25fcd-115">调度程序从传输收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="25fcd-115">The Dispatcher received a message from the transport.</span></span> <span data-ttu-id="25fcd-116">相关 ID 为“%1”。</span><span class="sxs-lookup"><span data-stu-id="25fcd-116">Correlation ID == '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="25fcd-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="25fcd-117">Details</span></span>  
  
|<span data-ttu-id="25fcd-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="25fcd-118">Data Item Name</span></span>|<span data-ttu-id="25fcd-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="25fcd-119">Data Item Type</span></span>|<span data-ttu-id="25fcd-120">描述</span><span class="sxs-lookup"><span data-stu-id="25fcd-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="25fcd-121">相关性 ID</span><span class="sxs-lookup"><span data-stu-id="25fcd-121">Correlation ID</span></span>|`xs:GUID`|<span data-ttu-id="25fcd-122">用于将服务或客户端的 `MessageSentToTransport` 事件与另一端的对应 `MessageReceivedFromTransport` 相关的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="25fcd-122">The activity ID used to correlate a `MessageSentToTransport` event from a service or client to its corresponding `MessageReceivedFromTransport` on the other end.</span></span>|  
|<span data-ttu-id="25fcd-123">HostReference</span><span class="sxs-lookup"><span data-stu-id="25fcd-123">HostReference</span></span>|`xs:string`|<span data-ttu-id="25fcd-124">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="25fcd-124">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="25fcd-125">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="25fcd-125">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="25fcd-126">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="25fcd-126">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="25fcd-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="25fcd-127">AppDomain</span></span>|`xs:string`|<span data-ttu-id="25fcd-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="25fcd-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
