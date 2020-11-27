---
title: 4202 - StartSqlCommandExecute
ms.date: 03/30/2017
ms.assetid: 4559f64f-c824-4075-9e7e-4710bf30f805
ms.openlocfilehash: d3f27c6ed28efe9d099dcedfc676b839ae9b1dee
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275835"
---
# <a name="4202---startsqlcommandexecute"></a><span data-ttu-id="753b3-102">4202 - StartSqlCommandExecute</span><span class="sxs-lookup"><span data-stu-id="753b3-102">4202 - StartSqlCommandExecute</span></span>

## <a name="properties"></a><span data-ttu-id="753b3-103">属性</span><span class="sxs-lookup"><span data-stu-id="753b3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="753b3-104">ID</span><span class="sxs-lookup"><span data-stu-id="753b3-104">ID</span></span>|<span data-ttu-id="753b3-105">4202</span><span class="sxs-lookup"><span data-stu-id="753b3-105">4202</span></span>|  
|<span data-ttu-id="753b3-106">关键字</span><span class="sxs-lookup"><span data-stu-id="753b3-106">Keywords</span></span>|<span data-ttu-id="753b3-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="753b3-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="753b3-108">级别</span><span class="sxs-lookup"><span data-stu-id="753b3-108">Level</span></span>|<span data-ttu-id="753b3-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="753b3-109">Verbose</span></span>|  
|<span data-ttu-id="753b3-110">通道</span><span class="sxs-lookup"><span data-stu-id="753b3-110">Channel</span></span>|<span data-ttu-id="753b3-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="753b3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="753b3-112">描述</span><span class="sxs-lookup"><span data-stu-id="753b3-112">Description</span></span>  

 <span data-ttu-id="753b3-113">指示 SQL 命令正在执行。</span><span class="sxs-lookup"><span data-stu-id="753b3-113">Indicates a SQL command is being executed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="753b3-114">消息</span><span class="sxs-lookup"><span data-stu-id="753b3-114">Message</span></span>  

 <span data-ttu-id="753b3-115">正在开始 SQL 命令执行: %1</span><span class="sxs-lookup"><span data-stu-id="753b3-115">Starting SQL command execution: %1</span></span>  
  
## <a name="details"></a><span data-ttu-id="753b3-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="753b3-116">Details</span></span>  
  
|<span data-ttu-id="753b3-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="753b3-117">Data Item Name</span></span>|<span data-ttu-id="753b3-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="753b3-118">Data Item Type</span></span>|<span data-ttu-id="753b3-119">描述</span><span class="sxs-lookup"><span data-stu-id="753b3-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="753b3-120">SqlCommand</span><span class="sxs-lookup"><span data-stu-id="753b3-120">SqlCommand</span></span>|<span data-ttu-id="753b3-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b3-121">xs:string</span></span>|<span data-ttu-id="753b3-122">已执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="753b3-122">The SQL command that was executed.</span></span>|  
|<span data-ttu-id="753b3-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="753b3-123">AppDomain</span></span>|<span data-ttu-id="753b3-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="753b3-124">xs:string</span></span>|<span data-ttu-id="753b3-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="753b3-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
