---
title: 211 - ParameterInspectorAfterCallInvoked
ms.date: 03/30/2017
ms.assetid: c0e21297-10b8-4456-a0e1-e019145cd5ac
ms.openlocfilehash: 7027b6557520a9ccb587f8d383d3598571da5838
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96279059"
---
# <a name="211---parameterinspectoraftercallinvoked"></a><span data-ttu-id="215d1-102">211 - ParameterInspectorAfterCallInvoked</span><span class="sxs-lookup"><span data-stu-id="215d1-102">211 - ParameterInspectorAfterCallInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="215d1-103">属性</span><span class="sxs-lookup"><span data-stu-id="215d1-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="215d1-104">ID</span><span class="sxs-lookup"><span data-stu-id="215d1-104">ID</span></span>|<span data-ttu-id="215d1-105">211</span><span class="sxs-lookup"><span data-stu-id="215d1-105">211</span></span>|  
|<span data-ttu-id="215d1-106">关键字</span><span class="sxs-lookup"><span data-stu-id="215d1-106">Keywords</span></span>|<span data-ttu-id="215d1-107">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="215d1-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="215d1-108">Level</span><span class="sxs-lookup"><span data-stu-id="215d1-108">Level</span></span>|<span data-ttu-id="215d1-109">信息</span><span class="sxs-lookup"><span data-stu-id="215d1-109">Information</span></span>|  
|<span data-ttu-id="215d1-110">通道</span><span class="sxs-lookup"><span data-stu-id="215d1-110">Channel</span></span>|<span data-ttu-id="215d1-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="215d1-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="215d1-112">描述</span><span class="sxs-lookup"><span data-stu-id="215d1-112">Description</span></span>  

 <span data-ttu-id="215d1-113">服务模型对 `AfterCall` 调用 `ParameterInspector` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="215d1-113">This event is emitted after the Service Model has invoked the `AfterCall` method on a `ParameterInspector`.</span></span>  
  
## <a name="message"></a><span data-ttu-id="215d1-114">消息</span><span class="sxs-lookup"><span data-stu-id="215d1-114">Message</span></span>  

 <span data-ttu-id="215d1-115">调度程序对“%1”类型的 ParameterInspector 调用了“AfterCall”。</span><span class="sxs-lookup"><span data-stu-id="215d1-115">The Dispatcher invoked 'AfterCall' on a ParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="215d1-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="215d1-116">Details</span></span>  
  
|<span data-ttu-id="215d1-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="215d1-117">Data Item Name</span></span>|<span data-ttu-id="215d1-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="215d1-118">Data Item Type</span></span>|<span data-ttu-id="215d1-119">描述</span><span class="sxs-lookup"><span data-stu-id="215d1-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="215d1-120">类型名称</span><span class="sxs-lookup"><span data-stu-id="215d1-120">Type Name</span></span>|`xs:string`|<span data-ttu-id="215d1-121">所调用 `ParameterInspector` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="215d1-121">The CLR FullName of the type of the invoked `ParameterInspector`.</span></span>|  
|<span data-ttu-id="215d1-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="215d1-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="215d1-123">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="215d1-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="215d1-124">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="215d1-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="215d1-125">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="215d1-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="215d1-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="215d1-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="215d1-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="215d1-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
