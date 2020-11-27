---
title: 212 - ParameterInspectorBeforeCallInvoked
ms.date: 03/30/2017
ms.assetid: 063fc8d2-ceac-4c18-8368-de84f2c78035
ms.openlocfilehash: 28c2aca4555d2e4ff498e450deae55ad6a87743c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96279033"
---
# <a name="212---parameterinspectorbeforecallinvoked"></a><span data-ttu-id="f661b-102">212 - ParameterInspectorBeforeCallInvoked</span><span class="sxs-lookup"><span data-stu-id="f661b-102">212 - ParameterInspectorBeforeCallInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="f661b-103">属性</span><span class="sxs-lookup"><span data-stu-id="f661b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="f661b-104">ID</span><span class="sxs-lookup"><span data-stu-id="f661b-104">ID</span></span>|<span data-ttu-id="f661b-105">212</span><span class="sxs-lookup"><span data-stu-id="f661b-105">212</span></span>|  
|<span data-ttu-id="f661b-106">关键字</span><span class="sxs-lookup"><span data-stu-id="f661b-106">Keywords</span></span>|<span data-ttu-id="f661b-107">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="f661b-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="f661b-108">Level</span><span class="sxs-lookup"><span data-stu-id="f661b-108">Level</span></span>|<span data-ttu-id="f661b-109">信息</span><span class="sxs-lookup"><span data-stu-id="f661b-109">Information</span></span>|  
|<span data-ttu-id="f661b-110">通道</span><span class="sxs-lookup"><span data-stu-id="f661b-110">Channel</span></span>|<span data-ttu-id="f661b-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="f661b-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="f661b-112">描述</span><span class="sxs-lookup"><span data-stu-id="f661b-112">Description</span></span>  

 <span data-ttu-id="f661b-113">服务模型对 `BeforeCall` 调用 `ParameterInspector` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="f661b-113">This event is emitted after the Service Model has invoked the `BeforeCall` method on a `ParameterInspector`.</span></span>  
  
## <a name="message"></a><span data-ttu-id="f661b-114">消息</span><span class="sxs-lookup"><span data-stu-id="f661b-114">Message</span></span>  

 <span data-ttu-id="f661b-115">调度程序对“%1”类型的 ParameterInspector 调用了“BeforeCall”。</span><span class="sxs-lookup"><span data-stu-id="f661b-115">The Dispatcher invoked 'BeforeCall' on a ParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="f661b-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="f661b-116">Details</span></span>  
  
|<span data-ttu-id="f661b-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="f661b-117">Data Item Name</span></span>|<span data-ttu-id="f661b-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="f661b-118">Data Item Type</span></span>|<span data-ttu-id="f661b-119">描述</span><span class="sxs-lookup"><span data-stu-id="f661b-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="f661b-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="f661b-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="f661b-121">所调用检查器的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="f661b-121">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="f661b-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="f661b-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="f661b-123">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="f661b-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="f661b-124">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="f661b-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="f661b-125">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="f661b-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="f661b-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="f661b-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="f661b-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f661b-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
