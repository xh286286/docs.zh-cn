---
title: 206 - ErrorHandlerInvoked
ms.date: 03/30/2017
ms.assetid: 97340f4d-4e09-4e42-a17a-982b3868dbcf
ms.openlocfilehash: 99415733624752217d32f6f026a419b2b32bfa7b
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96244608"
---
# <a name="206---errorhandlerinvoked"></a><span data-ttu-id="04d78-102">206 - ErrorHandlerInvoked</span><span class="sxs-lookup"><span data-stu-id="04d78-102">206 - ErrorHandlerInvoked</span></span>

## <a name="properties"></a><span data-ttu-id="04d78-103">属性</span><span class="sxs-lookup"><span data-stu-id="04d78-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="04d78-104">ID</span><span class="sxs-lookup"><span data-stu-id="04d78-104">ID</span></span>|<span data-ttu-id="04d78-105">206</span><span class="sxs-lookup"><span data-stu-id="04d78-105">206</span></span>|  
|<span data-ttu-id="04d78-106">关键字</span><span class="sxs-lookup"><span data-stu-id="04d78-106">Keywords</span></span>|<span data-ttu-id="04d78-107">疑难解答，ServiceModel</span><span class="sxs-lookup"><span data-stu-id="04d78-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="04d78-108">Level</span><span class="sxs-lookup"><span data-stu-id="04d78-108">Level</span></span>|<span data-ttu-id="04d78-109">信息</span><span class="sxs-lookup"><span data-stu-id="04d78-109">Information</span></span>|  
|<span data-ttu-id="04d78-110">通道</span><span class="sxs-lookup"><span data-stu-id="04d78-110">Channel</span></span>|<span data-ttu-id="04d78-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="04d78-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="04d78-112">描述</span><span class="sxs-lookup"><span data-stu-id="04d78-112">Description</span></span>  

 <span data-ttu-id="04d78-113">当 `ErrorHandler` 有机会处理在服务操作中发生的异常后，将发出此事件。</span><span class="sxs-lookup"><span data-stu-id="04d78-113">This event is emitted after an `ErrorHandler` has had an opportunity to handle an exception that occurred in a service operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="04d78-114">消息</span><span class="sxs-lookup"><span data-stu-id="04d78-114">Message</span></span>  

 <span data-ttu-id="04d78-115">调度程序调用了类型为 "%1" 且类型为 "%3" 的 ErrorHandler 的类型为 "%1" 的。</span><span class="sxs-lookup"><span data-stu-id="04d78-115">The Dispatcher invoked an ErrorHandler of type '%1' with an exception of type '%3'.</span></span> <span data-ttu-id="04d78-116">ErrorHandled 为“%2”。</span><span class="sxs-lookup"><span data-stu-id="04d78-116">ErrorHandled == '%2'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="04d78-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="04d78-117">Details</span></span>  
  
|<span data-ttu-id="04d78-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="04d78-118">Data Item Name</span></span>|<span data-ttu-id="04d78-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="04d78-119">Data Item Type</span></span>|<span data-ttu-id="04d78-120">描述</span><span class="sxs-lookup"><span data-stu-id="04d78-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="04d78-121">TypeName</span><span class="sxs-lookup"><span data-stu-id="04d78-121">TypeName</span></span>|`xs:string`|<span data-ttu-id="04d78-122">所调用 `ErrorHandler` 的类型的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="04d78-122">The CLR FullName of the type of the invoked `ErrorHandler`.</span></span>|  
|<span data-ttu-id="04d78-123">已处理</span><span class="sxs-lookup"><span data-stu-id="04d78-123">Handled</span></span>|`xs:unsignedByte`|<span data-ttu-id="04d78-124">如果错误处理程序已处理错误，则为 `true`；否则为 `false`。</span><span class="sxs-lookup"><span data-stu-id="04d78-124">`true` if the error handler handled the error, otherwise `false`.</span></span>|  
|<span data-ttu-id="04d78-125">ExceptionTypeName</span><span class="sxs-lookup"><span data-stu-id="04d78-125">ExceptionTypeName</span></span>|`xs:string`|<span data-ttu-id="04d78-126">待处理异常的 CLR FullName。</span><span class="sxs-lookup"><span data-stu-id="04d78-126">The CLR FullName of the exception that was being handled.</span></span>|  
|<span data-ttu-id="04d78-127">HostReference</span><span class="sxs-lookup"><span data-stu-id="04d78-127">HostReference</span></span>|`xs:string`|<span data-ttu-id="04d78-128">对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。</span><span class="sxs-lookup"><span data-stu-id="04d78-128">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="04d78-129">其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。</span><span class="sxs-lookup"><span data-stu-id="04d78-129">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="04d78-130">示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。</span><span class="sxs-lookup"><span data-stu-id="04d78-130">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="04d78-131">应用程序域</span><span class="sxs-lookup"><span data-stu-id="04d78-131">AppDomain</span></span>|`xs:string`|<span data-ttu-id="04d78-132">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="04d78-132">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
