---
title: 302 - 出现用户定义的警告
ms.date: 03/30/2017
ms.assetid: 8d1f0bf1-0151-45e6-be92-573d397b54de
ms.openlocfilehash: b942b2e9716713371b8679fc9df9b9634dfc7283
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96243438"
---
# <a name="302---userdefinedwarningoccurred"></a><span data-ttu-id="57222-102">302 - 出现用户定义的警告</span><span class="sxs-lookup"><span data-stu-id="57222-102">302 - UserDefinedWarningOccurred</span></span>

## <a name="properties"></a><span data-ttu-id="57222-103">属性</span><span class="sxs-lookup"><span data-stu-id="57222-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="57222-104">ID</span><span class="sxs-lookup"><span data-stu-id="57222-104">ID</span></span>|<span data-ttu-id="57222-105">302</span><span class="sxs-lookup"><span data-stu-id="57222-105">302</span></span>|  
|<span data-ttu-id="57222-106">关键字</span><span class="sxs-lookup"><span data-stu-id="57222-106">Keywords</span></span>|<span data-ttu-id="57222-107">疑难解答，HealthMonitoring，UserEvents，ServiceModel，EndToEndMonitoring</span><span class="sxs-lookup"><span data-stu-id="57222-107">Troubleshooting, HealthMonitoring, UserEvents, ServiceModel, EndToEndMonitoring</span></span>|  
|<span data-ttu-id="57222-108">Level</span><span class="sxs-lookup"><span data-stu-id="57222-108">Level</span></span>|<span data-ttu-id="57222-109">警告</span><span class="sxs-lookup"><span data-stu-id="57222-109">Warning</span></span>|  
|<span data-ttu-id="57222-110">通道</span><span class="sxs-lookup"><span data-stu-id="57222-110">Channel</span></span>|<span data-ttu-id="57222-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="57222-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="57222-112">描述</span><span class="sxs-lookup"><span data-stu-id="57222-112">Description</span></span>  

 <span data-ttu-id="57222-113">此事件从用户代码发出。</span><span class="sxs-lookup"><span data-stu-id="57222-113">This event is emitted from user code.</span></span> <span data-ttu-id="57222-114">当开发人员的服务中出现自定义的警告事件时，开发人员可以发出此事件。</span><span class="sxs-lookup"><span data-stu-id="57222-114">Developers can emit this event when a custom-defined warning event occurs in their service.</span></span> <span data-ttu-id="57222-115">可以使用 <xref:System.Diagnostics.Eventing> API 完成此操作。</span><span class="sxs-lookup"><span data-stu-id="57222-115">This can be done using the <xref:System.Diagnostics.Eventing> APIs.</span></span> <span data-ttu-id="57222-116">此外，还提供了一个 WCF 示例，该示例包装 API 并演示如何正确发出此事件。</span><span class="sxs-lookup"><span data-stu-id="57222-116">Additionally, there is a WCF sample that wraps that API and demonstrates how to properly emit this event.</span></span>  
  
## <a name="message"></a><span data-ttu-id="57222-117">消息</span><span class="sxs-lookup"><span data-stu-id="57222-117">Message</span></span>  

 <span data-ttu-id="57222-118">Name“%1”、Reference“%2”、Payload: %3</span><span class="sxs-lookup"><span data-stu-id="57222-118">Name:'%1', Reference:'%2', Payload:%3</span></span>  
  
## <a name="details"></a><span data-ttu-id="57222-119">详细信息</span><span class="sxs-lookup"><span data-stu-id="57222-119">Details</span></span>  
  
|<span data-ttu-id="57222-120">数据项名称</span><span class="sxs-lookup"><span data-stu-id="57222-120">Data Item Name</span></span>|<span data-ttu-id="57222-121">数据项类型</span><span class="sxs-lookup"><span data-stu-id="57222-121">Data Item Type</span></span>|<span data-ttu-id="57222-122">描述</span><span class="sxs-lookup"><span data-stu-id="57222-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="57222-123">“属性”</span><span class="sxs-lookup"><span data-stu-id="57222-123">Name</span></span>|`xs:string`|<span data-ttu-id="57222-124">事件的用户定义名称。</span><span class="sxs-lookup"><span data-stu-id="57222-124">The user-defined name of the event.</span></span>|  
|<span data-ttu-id="57222-125">HostReference</span><span class="sxs-lookup"><span data-stu-id="57222-125">HostReference</span></span>|`xs:string`|<span data-ttu-id="57222-126">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="57222-126">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="57222-127">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="57222-127">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="57222-128">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="57222-128">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="57222-129">有效负载</span><span class="sxs-lookup"><span data-stu-id="57222-129">Payload</span></span>|`xs:string`|<span data-ttu-id="57222-130">事件的用户定义负载。</span><span class="sxs-lookup"><span data-stu-id="57222-130">The user-defined payload of the event.</span></span>|
