---
title: 204 - ClientParameterInspectorBeforeCallInvoked
ms.date: 03/30/2017
ms.assetid: 8253555a-9002-4565-8ede-33d7a33a895f
ms.openlocfilehash: a7db8c9fa87518c59969f3089ff033fa8c912577
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275783"
---
# <a name="204---clientparameterinspectorbeforecallinvoked"></a><span data-ttu-id="9d3d3-102">204 - ClientParameterInspectorBeforeCallInvoked</span><span class="sxs-lookup"><span data-stu-id="9d3d3-102">204 - ClientParameterInspectorBeforeCallInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="9d3d3-103">属性</span><span class="sxs-lookup"><span data-stu-id="9d3d3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9d3d3-104">ID</span><span class="sxs-lookup"><span data-stu-id="9d3d3-104">ID</span></span>|<span data-ttu-id="9d3d3-105">204</span><span class="sxs-lookup"><span data-stu-id="9d3d3-105">204</span></span>|  
|<span data-ttu-id="9d3d3-106">关键字</span><span class="sxs-lookup"><span data-stu-id="9d3d3-106">Keywords</span></span>|<span data-ttu-id="9d3d3-107">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="9d3d3-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="9d3d3-108">Level</span><span class="sxs-lookup"><span data-stu-id="9d3d3-108">Level</span></span>|<span data-ttu-id="9d3d3-109">信息</span><span class="sxs-lookup"><span data-stu-id="9d3d3-109">Information</span></span>|  
|<span data-ttu-id="9d3d3-110">通道</span><span class="sxs-lookup"><span data-stu-id="9d3d3-110">Channel</span></span>|<span data-ttu-id="9d3d3-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="9d3d3-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9d3d3-112">描述</span><span class="sxs-lookup"><span data-stu-id="9d3d3-112">Description</span></span>  

 <span data-ttu-id="9d3d3-113">服务模型在客户端参数检查器上调用 `BeforeCall` 方法之后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-113">This event is emitted after the Service Model has invoked the `BeforeCall` method on a client parameter inspector.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9d3d3-114">消息</span><span class="sxs-lookup"><span data-stu-id="9d3d3-114">Message</span></span>  

 <span data-ttu-id="9d3d3-115">调度程序对“%1”类型的 ClientParameterInspector 调用了“BeforeCall”。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-115">The Dispatcher invoked 'BeforeCall' on a ClientParameterInspector of type '%1'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="9d3d3-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="9d3d3-116">Details</span></span>  
  
|<span data-ttu-id="9d3d3-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9d3d3-117">Data Item Name</span></span>|<span data-ttu-id="9d3d3-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9d3d3-118">Data Item Type</span></span>|<span data-ttu-id="9d3d3-119">描述</span><span class="sxs-lookup"><span data-stu-id="9d3d3-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9d3d3-120">TypeName</span><span class="sxs-lookup"><span data-stu-id="9d3d3-120">TypeName</span></span>|`xs:string`|<span data-ttu-id="9d3d3-121">所调用检查器的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-121">The CLR FullName of the invoked inspector's type.</span></span>|  
|<span data-ttu-id="9d3d3-122">HostReference</span><span class="sxs-lookup"><span data-stu-id="9d3d3-122">HostReference</span></span>|`xs:string`|<span data-ttu-id="9d3d3-123">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-123">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="9d3d3-124">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-124">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="9d3d3-125">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-125">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="9d3d3-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9d3d3-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="9d3d3-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9d3d3-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
