---
title: 301 - UserDefinedErrorOccurred
ms.date: 03/30/2017
ms.assetid: a0285d1c-550f-4c14-9c36-a96e97f1c4e4
ms.openlocfilehash: 2c3ff1905a1d17413211246f5b3cc156bcbb7320
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96243451"
---
# <a name="301---userdefinederroroccurred"></a><span data-ttu-id="07a4e-102">301 - UserDefinedErrorOccurred</span><span class="sxs-lookup"><span data-stu-id="07a4e-102">301 - UserDefinedErrorOccurred</span></span>

## <a name="properties"></a><span data-ttu-id="07a4e-103">属性</span><span class="sxs-lookup"><span data-stu-id="07a4e-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="07a4e-104">ID</span><span class="sxs-lookup"><span data-stu-id="07a4e-104">ID</span></span>|<span data-ttu-id="07a4e-105">301</span><span class="sxs-lookup"><span data-stu-id="07a4e-105">301</span></span>|  
|<span data-ttu-id="07a4e-106">关键字</span><span class="sxs-lookup"><span data-stu-id="07a4e-106">Keywords</span></span>|<span data-ttu-id="07a4e-107">疑难解答，HealthMonitoring，UserEvents，ServiceModel，EndToEndMonitoring</span><span class="sxs-lookup"><span data-stu-id="07a4e-107">Troubleshooting, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span></span>|  
|<span data-ttu-id="07a4e-108">Level</span><span class="sxs-lookup"><span data-stu-id="07a4e-108">Level</span></span>|<span data-ttu-id="07a4e-109">错误</span><span class="sxs-lookup"><span data-stu-id="07a4e-109">Error</span></span>|  
|<span data-ttu-id="07a4e-110">通道</span><span class="sxs-lookup"><span data-stu-id="07a4e-110">Channel</span></span>|<span data-ttu-id="07a4e-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="07a4e-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="07a4e-112">描述</span><span class="sxs-lookup"><span data-stu-id="07a4e-112">Description</span></span>  

 <span data-ttu-id="07a4e-113">此事件从用户代码发出。</span><span class="sxs-lookup"><span data-stu-id="07a4e-113">This event is emitted from user code.</span></span> <span data-ttu-id="07a4e-114">当开发人员的服务中出现自定义错误时，开发人员可以发出此事件。</span><span class="sxs-lookup"><span data-stu-id="07a4e-114">Developers can emit this event when a custom-defined error occurs in their service.</span></span> <span data-ttu-id="07a4e-115">可以使用 <xref:System.Diagnostics.Eventing> API 完成此操作。</span><span class="sxs-lookup"><span data-stu-id="07a4e-115">This can be done using the <xref:System.Diagnostics.Eventing> APIs.</span></span> <span data-ttu-id="07a4e-116">此外，还提供了一个 WCF 示例，该示例包装 API 并演示如何正确发出此事件。</span><span class="sxs-lookup"><span data-stu-id="07a4e-116">Additionally, there is a WCF sample that wraps that API and demonstrates how to properly emit this event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="07a4e-117">消息</span><span class="sxs-lookup"><span data-stu-id="07a4e-117">Message</span></span>  

 <span data-ttu-id="07a4e-118">Name“%1”、Reference“%2”、Payload: %3</span><span class="sxs-lookup"><span data-stu-id="07a4e-118">Name:'%1', Reference:'%2', Payload:%3</span></span>  
  
## <a name="details"></a><span data-ttu-id="07a4e-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="07a4e-119">Details</span></span>  
  
|<span data-ttu-id="07a4e-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="07a4e-120">Data Item Name</span></span>|<span data-ttu-id="07a4e-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="07a4e-121">Data Item Type</span></span>|<span data-ttu-id="07a4e-122">描述</span><span class="sxs-lookup"><span data-stu-id="07a4e-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="07a4e-123">“属性”</span><span class="sxs-lookup"><span data-stu-id="07a4e-123">Name</span></span>|`xs:string`|<span data-ttu-id="07a4e-124">事件的用户定义名称。</span><span class="sxs-lookup"><span data-stu-id="07a4e-124">The user-defined name of the event.</span></span>|  
|<span data-ttu-id="07a4e-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="07a4e-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="07a4e-126">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="07a4e-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="07a4e-127">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="07a4e-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="07a4e-128">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="07a4e-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="07a4e-129">有效负载</span><span class="sxs-lookup"><span data-stu-id="07a4e-129">Payload</span></span>|`xs:string`|<span data-ttu-id="07a4e-130">事件的用户定义负载。</span><span class="sxs-lookup"><span data-stu-id="07a4e-130">The user-defined payload of the event.</span></span>|
