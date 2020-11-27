---
title: 1126 - InvokedMethodThrewException
ms.date: 03/30/2017
ms.assetid: 0d3cff1a-97e6-4b6c-be18-108c6881bfc0
ms.openlocfilehash: 7caaebe42f49a62fec61ba17a4d3fe3a538e2ab4
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96262835"
---
# <a name="1126---invokedmethodthrewexception"></a><span data-ttu-id="30c66-102">1126 - InvokedMethodThrewException</span><span class="sxs-lookup"><span data-stu-id="30c66-102">1126 - InvokedMethodThrewException</span></span>

## <a name="properties"></a><span data-ttu-id="30c66-103">属性</span><span class="sxs-lookup"><span data-stu-id="30c66-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="30c66-104">ID</span><span class="sxs-lookup"><span data-stu-id="30c66-104">ID</span></span>|<span data-ttu-id="30c66-105">1126</span><span class="sxs-lookup"><span data-stu-id="30c66-105">1126</span></span>|  
|<span data-ttu-id="30c66-106">关键字</span><span class="sxs-lookup"><span data-stu-id="30c66-106">Keywords</span></span>|<span data-ttu-id="30c66-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="30c66-107">WFRuntime</span></span>|  
|<span data-ttu-id="30c66-108">Level</span><span class="sxs-lookup"><span data-stu-id="30c66-108">Level</span></span>|<span data-ttu-id="30c66-109">信息</span><span class="sxs-lookup"><span data-stu-id="30c66-109">Information</span></span>|  
|<span data-ttu-id="30c66-110">通道</span><span class="sxs-lookup"><span data-stu-id="30c66-110">Channel</span></span>|<span data-ttu-id="30c66-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="30c66-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="30c66-112">描述</span><span class="sxs-lookup"><span data-stu-id="30c66-112">Description</span></span>  

 <span data-ttu-id="30c66-113">指示 InvokeMethod 活动调用的方法引发了异常。</span><span class="sxs-lookup"><span data-stu-id="30c66-113">Indicates an exception was thrown by the method called by the InvokeMethod activity.</span></span>  
  
## <a name="message"></a><span data-ttu-id="30c66-114">消息</span><span class="sxs-lookup"><span data-stu-id="30c66-114">Message</span></span>  

 <span data-ttu-id="30c66-115">在活动“%1”调用的方法中，引发了异常。</span><span class="sxs-lookup"><span data-stu-id="30c66-115">An exception was thrown in the method called by the activity '%1'.</span></span> <span data-ttu-id="30c66-116">%2</span><span class="sxs-lookup"><span data-stu-id="30c66-116">%2</span></span>  
  
## <a name="details"></a><span data-ttu-id="30c66-117">详细信息</span><span class="sxs-lookup"><span data-stu-id="30c66-117">Details</span></span>  
  
|<span data-ttu-id="30c66-118">数据项名称</span><span class="sxs-lookup"><span data-stu-id="30c66-118">Data Item Name</span></span>|<span data-ttu-id="30c66-119">数据项类型</span><span class="sxs-lookup"><span data-stu-id="30c66-119">Data Item Type</span></span>|<span data-ttu-id="30c66-120">描述</span><span class="sxs-lookup"><span data-stu-id="30c66-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="30c66-121">InvokeMethod</span><span class="sxs-lookup"><span data-stu-id="30c66-121">InvokeMethod</span></span>|<span data-ttu-id="30c66-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="30c66-122">xs:string</span></span>|<span data-ttu-id="30c66-123">InvokeMethod 活动的显示名称。</span><span class="sxs-lookup"><span data-stu-id="30c66-123">The display name of the InvokeMethod activity.</span></span>|  
|<span data-ttu-id="30c66-124">异常</span><span class="sxs-lookup"><span data-stu-id="30c66-124">Exception</span></span>|<span data-ttu-id="30c66-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="30c66-125">xs:string</span></span>|<span data-ttu-id="30c66-126">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="30c66-126">The exception details for the exception</span></span>|  
|<span data-ttu-id="30c66-127">应用程序域</span><span class="sxs-lookup"><span data-stu-id="30c66-127">AppDomain</span></span>|<span data-ttu-id="30c66-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="30c66-128">xs:string</span></span>|<span data-ttu-id="30c66-129">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="30c66-129">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
