---
title: 39456 - TrackingRecordDropped
ms.date: 03/30/2017
ms.assetid: da13d5bc-1736-47a4-b3fd-064ca8040326
ms.openlocfilehash: d958b506e057bc0d59f954debdc9da6015bf5f1f
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96273092"
---
# <a name="39456---trackingrecorddropped"></a><span data-ttu-id="9a18b-102">39456 - TrackingRecordDropped</span><span class="sxs-lookup"><span data-stu-id="9a18b-102">39456 - TrackingRecordDropped</span></span>

## <a name="properties"></a><span data-ttu-id="9a18b-103">属性</span><span class="sxs-lookup"><span data-stu-id="9a18b-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="9a18b-104">ID</span><span class="sxs-lookup"><span data-stu-id="9a18b-104">ID</span></span>|<span data-ttu-id="9a18b-105">39456</span><span class="sxs-lookup"><span data-stu-id="9a18b-105">39456</span></span>|  
|<span data-ttu-id="9a18b-106">关键字</span><span class="sxs-lookup"><span data-stu-id="9a18b-106">Keywords</span></span>|<span data-ttu-id="9a18b-107">WFTracking</span><span class="sxs-lookup"><span data-stu-id="9a18b-107">WFTracking</span></span>|  
|<span data-ttu-id="9a18b-108">Level</span><span class="sxs-lookup"><span data-stu-id="9a18b-108">Level</span></span>|<span data-ttu-id="9a18b-109">警告</span><span class="sxs-lookup"><span data-stu-id="9a18b-109">Warning</span></span>|  
|<span data-ttu-id="9a18b-110">通道</span><span class="sxs-lookup"><span data-stu-id="9a18b-110">Channel</span></span>|<span data-ttu-id="9a18b-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="9a18b-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="9a18b-112">描述</span><span class="sxs-lookup"><span data-stu-id="9a18b-112">Description</span></span>  

 <span data-ttu-id="9a18b-113">指示一个跟踪记录已被丢弃，因为其大小超过 ETW 提供程序会话允许的最大大小。</span><span class="sxs-lookup"><span data-stu-id="9a18b-113">Indicates a tracking record has been dropped because its size exceeds maximum allowed by the ETW session provider.</span></span>  
  
## <a name="message"></a><span data-ttu-id="9a18b-114">消息</span><span class="sxs-lookup"><span data-stu-id="9a18b-114">Message</span></span>  

 <span data-ttu-id="9a18b-115">跟踪记录 %1 的大小超出了 ETW 会话对提供程序 %2 允许的最大值</span><span class="sxs-lookup"><span data-stu-id="9a18b-115">Size of tracking record %1 exceeds maximum allowed by the ETW session for provider %2</span></span>  
  
## <a name="details"></a><span data-ttu-id="9a18b-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="9a18b-116">Details</span></span>  
  
|<span data-ttu-id="9a18b-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="9a18b-117">Data Item Name</span></span>|<span data-ttu-id="9a18b-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="9a18b-118">Data Item Type</span></span>|<span data-ttu-id="9a18b-119">描述</span><span class="sxs-lookup"><span data-stu-id="9a18b-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="9a18b-120">异常</span><span class="sxs-lookup"><span data-stu-id="9a18b-120">Exception</span></span>|<span data-ttu-id="9a18b-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a18b-121">xs:string</span></span>|<span data-ttu-id="9a18b-122">异常的异常详细信息</span><span class="sxs-lookup"><span data-stu-id="9a18b-122">The exception details for the exception</span></span>|  
|<span data-ttu-id="9a18b-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="9a18b-123">AppDomain</span></span>|<span data-ttu-id="9a18b-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="9a18b-124">xs:string</span></span>|<span data-ttu-id="9a18b-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="9a18b-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
