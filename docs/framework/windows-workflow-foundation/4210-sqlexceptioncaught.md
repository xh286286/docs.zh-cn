---
title: 4210 - SqlExceptionCaught
ms.date: 03/30/2017
ms.assetid: f0ce8af3-eb4c-48c8-b3d9-dd2f94b5574b
ms.openlocfilehash: 1dab44e3fb97d74a2146f5bf992225222bc93d50
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96280372"
---
# <a name="4210---sqlexceptioncaught"></a><span data-ttu-id="0b7cd-102">4210 - SqlExceptionCaught</span><span class="sxs-lookup"><span data-stu-id="0b7cd-102">4210 - SqlExceptionCaught</span></span>

## <a name="properties"></a><span data-ttu-id="0b7cd-103">属性</span><span class="sxs-lookup"><span data-stu-id="0b7cd-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="0b7cd-104">ID</span><span class="sxs-lookup"><span data-stu-id="0b7cd-104">ID</span></span>|<span data-ttu-id="0b7cd-105">4210</span><span class="sxs-lookup"><span data-stu-id="0b7cd-105">4210</span></span>|  
|<span data-ttu-id="0b7cd-106">关键字</span><span class="sxs-lookup"><span data-stu-id="0b7cd-106">Keywords</span></span>|<span data-ttu-id="0b7cd-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="0b7cd-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="0b7cd-108">Level</span><span class="sxs-lookup"><span data-stu-id="0b7cd-108">Level</span></span>|<span data-ttu-id="0b7cd-109">警告</span><span class="sxs-lookup"><span data-stu-id="0b7cd-109">Warning</span></span>|  
|<span data-ttu-id="0b7cd-110">通道</span><span class="sxs-lookup"><span data-stu-id="0b7cd-110">Channel</span></span>|<span data-ttu-id="0b7cd-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="0b7cd-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="0b7cd-112">描述</span><span class="sxs-lookup"><span data-stu-id="0b7cd-112">Description</span></span>  

 <span data-ttu-id="0b7cd-113">指示捕获了 SQL 异常。</span><span class="sxs-lookup"><span data-stu-id="0b7cd-113">Indicates a SQL exception was caught.</span></span>  
  
## <a name="message"></a><span data-ttu-id="0b7cd-114">消息</span><span class="sxs-lookup"><span data-stu-id="0b7cd-114">Message</span></span>  

 <span data-ttu-id="0b7cd-115">已捕获 SQL 异常编号为 %1 的消息 %2。</span><span class="sxs-lookup"><span data-stu-id="0b7cd-115">Caught SQL Exception number %1 message %2.</span></span>  
  
## <a name="details"></a><span data-ttu-id="0b7cd-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="0b7cd-116">Details</span></span>  
  
|<span data-ttu-id="0b7cd-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="0b7cd-117">Data Item Name</span></span>|<span data-ttu-id="0b7cd-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="0b7cd-118">Data Item Type</span></span>|<span data-ttu-id="0b7cd-119">描述</span><span class="sxs-lookup"><span data-stu-id="0b7cd-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="0b7cd-120">ErrorNumber</span><span class="sxs-lookup"><span data-stu-id="0b7cd-120">ErrorNumber</span></span>|<span data-ttu-id="0b7cd-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b7cd-121">xs:string</span></span>|<span data-ttu-id="0b7cd-122">SQL 错误号。</span><span class="sxs-lookup"><span data-stu-id="0b7cd-122">The SQL error number.</span></span>|  
|<span data-ttu-id="0b7cd-123">ExceptionMessage</span><span class="sxs-lookup"><span data-stu-id="0b7cd-123">ExceptionMessage</span></span>|<span data-ttu-id="0b7cd-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b7cd-124">xs:string</span></span>|<span data-ttu-id="0b7cd-125">来自 SQL 异常的消息。</span><span class="sxs-lookup"><span data-stu-id="0b7cd-125">The message from the SQL exception.</span></span>|  
|<span data-ttu-id="0b7cd-126">应用程序域</span><span class="sxs-lookup"><span data-stu-id="0b7cd-126">AppDomain</span></span>|<span data-ttu-id="0b7cd-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b7cd-127">xs:string</span></span>|<span data-ttu-id="0b7cd-128">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="0b7cd-128">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
