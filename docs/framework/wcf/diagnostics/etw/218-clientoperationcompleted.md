---
title: 218 - ClientOperationCompleted
ms.date: 03/30/2017
ms.assetid: b069bced-7bb2-4e01-8227-e5dbda17af09
ms.openlocfilehash: d74aa77aff7b45b50f6891c999889011d9e03381
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96278851"
---
# <a name="218---clientoperationcompleted"></a><span data-ttu-id="f0aef-102">218 - ClientOperationCompleted</span><span class="sxs-lookup"><span data-stu-id="f0aef-102">218 - ClientOperationCompleted</span></span>

## <a name="properties"></a><span data-ttu-id="f0aef-103">属性</span><span class="sxs-lookup"><span data-stu-id="f0aef-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f0aef-104">ID</span><span class="sxs-lookup"><span data-stu-id="f0aef-104">ID</span></span>|<span data-ttu-id="f0aef-105">218</span><span class="sxs-lookup"><span data-stu-id="f0aef-105">218</span></span>|  
|<span data-ttu-id="f0aef-106">关键字</span><span class="sxs-lookup"><span data-stu-id="f0aef-106">Keywords</span></span>|<span data-ttu-id="f0aef-107">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f0aef-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="f0aef-108">Level</span><span class="sxs-lookup"><span data-stu-id="f0aef-108">Level</span></span>|<span data-ttu-id="f0aef-109">信息</span><span class="sxs-lookup"><span data-stu-id="f0aef-109">Information</span></span>|  
|<span data-ttu-id="f0aef-110">通道</span><span class="sxs-lookup"><span data-stu-id="f0aef-110">Channel</span></span>|<span data-ttu-id="f0aef-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="f0aef-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f0aef-112">描述</span><span class="sxs-lookup"><span data-stu-id="f0aef-112">Description</span></span>  

 <span data-ttu-id="f0aef-113">此事件恰好在操作完成之后由客户端发出。</span><span class="sxs-lookup"><span data-stu-id="f0aef-113">This event is emitted by clients just after an operation completes.</span></span> <span data-ttu-id="f0aef-114">对于单向操作，此事件恰好在成功发送消息之后发送。</span><span class="sxs-lookup"><span data-stu-id="f0aef-114">For one-way operations, this is just after the message is sent successfully.</span></span> <span data-ttu-id="f0aef-115">对于请求-响应操作，此事件在接收响应之后发送。</span><span class="sxs-lookup"><span data-stu-id="f0aef-115">For request-response operations this is after the response is received.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f0aef-116">消息</span><span class="sxs-lookup"><span data-stu-id="f0aef-116">Message</span></span>  

 <span data-ttu-id="f0aef-117">客户端已执行完与协定“%2”相关联的操作“%1”。</span><span class="sxs-lookup"><span data-stu-id="f0aef-117">The Client completed executing Action '%1' associated with the '%2' contract.</span></span> <span data-ttu-id="f0aef-118">消息已发送到“%3”。</span><span class="sxs-lookup"><span data-stu-id="f0aef-118">The message was sent to '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f0aef-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="f0aef-119">Details</span></span>  
  
|<span data-ttu-id="f0aef-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f0aef-120">Data Item Name</span></span>|<span data-ttu-id="f0aef-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f0aef-121">Data Item Type</span></span>|<span data-ttu-id="f0aef-122">说明</span><span class="sxs-lookup"><span data-stu-id="f0aef-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f0aef-123">操作</span><span class="sxs-lookup"><span data-stu-id="f0aef-123">Action</span></span>|<span data-ttu-id="f0aef-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="f0aef-124">xs:string</span></span>|<span data-ttu-id="f0aef-125">传出消息的 SOAP 操作标头。</span><span class="sxs-lookup"><span data-stu-id="f0aef-125">The SOAP action header of the outgoing message.</span></span>|  
|<span data-ttu-id="f0aef-126">协定名称</span><span class="sxs-lookup"><span data-stu-id="f0aef-126">Contract Name</span></span>|`xs:string`|<span data-ttu-id="f0aef-127">协定的名称。</span><span class="sxs-lookup"><span data-stu-id="f0aef-127">The name of the contract.</span></span> <span data-ttu-id="f0aef-128">示例：ICalculator。</span><span class="sxs-lookup"><span data-stu-id="f0aef-128">Example: ICalculator.</span></span>|  
|<span data-ttu-id="f0aef-129">目标</span><span class="sxs-lookup"><span data-stu-id="f0aef-129">Destination</span></span>|`xs:string`|<span data-ttu-id="f0aef-130">消息已发送到的服务终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="f0aef-130">The address of the service endpoint that the message was sent to.</span></span>|  
|<span data-ttu-id="f0aef-131">HostReference</span><span class="sxs-lookup"><span data-stu-id="f0aef-131">HostReference</span></span>|`xs:string`|<span data-ttu-id="f0aef-132">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="f0aef-132">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="f0aef-133">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="f0aef-133">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="f0aef-134">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="f0aef-134">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="f0aef-135">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f0aef-135">AppDomain</span></span>|`xs:string`|<span data-ttu-id="f0aef-136">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f0aef-136">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
