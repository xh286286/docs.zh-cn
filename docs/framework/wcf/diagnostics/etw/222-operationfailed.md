---
title: 222 - OperationFailed
ms.date: 03/30/2017
ms.assetid: 6b530ded-8f20-4d78-8bfe-1875276df6ba
ms.openlocfilehash: 64b41ee78e943ca16eaa791133454ec62ccf6ed8
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96263082"
---
# <a name="222---operationfailed"></a><span data-ttu-id="fae05-102">222 - OperationFailed</span><span class="sxs-lookup"><span data-stu-id="fae05-102">222 - OperationFailed</span></span>

## <a name="properties"></a><span data-ttu-id="fae05-103">属性</span><span class="sxs-lookup"><span data-stu-id="fae05-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="fae05-104">ID</span><span class="sxs-lookup"><span data-stu-id="fae05-104">ID</span></span>|<span data-ttu-id="fae05-105">222</span><span class="sxs-lookup"><span data-stu-id="fae05-105">222</span></span>|  
|<span data-ttu-id="fae05-106">关键字</span><span class="sxs-lookup"><span data-stu-id="fae05-106">Keywords</span></span>|<span data-ttu-id="fae05-107">EndToEndMonitoring、HealthMonitoring、疑难解答、ServiceModel</span><span class="sxs-lookup"><span data-stu-id="fae05-107">EndToEndMonitoring, HealthMonitoring, Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="fae05-108">Level</span><span class="sxs-lookup"><span data-stu-id="fae05-108">Level</span></span>|<span data-ttu-id="fae05-109">警告</span><span class="sxs-lookup"><span data-stu-id="fae05-109">Warning</span></span>|  
|<span data-ttu-id="fae05-110">通道</span><span class="sxs-lookup"><span data-stu-id="fae05-110">Channel</span></span>|<span data-ttu-id="fae05-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="fae05-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="fae05-112">描述</span><span class="sxs-lookup"><span data-stu-id="fae05-112">Description</span></span>  

 <span data-ttu-id="fae05-113">如果服务模型的默认 `OperationInvoker` 在调用其方法时遇到异常，则会发出此事件。</span><span class="sxs-lookup"><span data-stu-id="fae05-113">This event is emitted when the Service Model's default `OperationInvoker` has encountered an exception while invoking its method.</span></span> <span data-ttu-id="fae05-114">请注意，派生自 `FaultException` 的异常会导致不发出此事件。</span><span class="sxs-lookup"><span data-stu-id="fae05-114">Note that exceptions that derive from `FaultException` cause this event to not be emitted.</span></span>  
  
## <a name="message"></a><span data-ttu-id="fae05-115">消息</span><span class="sxs-lookup"><span data-stu-id="fae05-115">Message</span></span>  

 <span data-ttu-id="fae05-116">“%1”方法在由 OperationInvoker 调用时引发了未经处理的异常。</span><span class="sxs-lookup"><span data-stu-id="fae05-116">The '%1' method threw an unhandled exception when invoked by the OperationInvoker.</span></span> <span data-ttu-id="fae05-117">该方法调用持续了“%2”毫秒。</span><span class="sxs-lookup"><span data-stu-id="fae05-117">The method call duration was '%2' ms.</span></span>  
  
## <a name="details"></a><span data-ttu-id="fae05-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="fae05-118">Details</span></span>  
  
|<span data-ttu-id="fae05-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="fae05-119">Data Item Name</span></span>|<span data-ttu-id="fae05-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="fae05-120">Data Item Type</span></span>|<span data-ttu-id="fae05-121">描述</span><span class="sxs-lookup"><span data-stu-id="fae05-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="fae05-122">方法名</span><span class="sxs-lookup"><span data-stu-id="fae05-122">Method Name</span></span>|`xs:string`|<span data-ttu-id="fae05-123">由 `OperationInvoker` 调用的方法的 CLR 名称。</span><span class="sxs-lookup"><span data-stu-id="fae05-123">The CLR name of the method that was invoked by the `OperationInvoker`.</span></span>|  
|<span data-ttu-id="fae05-124">持续时间</span><span class="sxs-lookup"><span data-stu-id="fae05-124">Duration</span></span>|`xs:long`|<span data-ttu-id="fae05-125">`OperationInvoker` 调用方法所花费的时间（以毫秒为单位）。</span><span class="sxs-lookup"><span data-stu-id="fae05-125">The time, in milliseconds, that it took the `OperationInvoker` to invoke the method.</span></span>|  
|<span data-ttu-id="fae05-126">HostReference</span><span class="sxs-lookup"><span data-stu-id="fae05-126">HostReference</span></span>|`xs:string`|<span data-ttu-id="fae05-127">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="fae05-127">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="fae05-128">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="fae05-128">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="fae05-129">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="fae05-129">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="fae05-130">应用程序域</span><span class="sxs-lookup"><span data-stu-id="fae05-130">AppDomain</span></span>|`xs:string`|<span data-ttu-id="fae05-131">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="fae05-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
