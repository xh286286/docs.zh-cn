---
title: 4201 - EndSqlCommandExecute
ms.date: 03/30/2017
ms.assetid: ae0dbc15-f98c-4096-a8d9-fbe4dc36f1cd
ms.openlocfilehash: 0d6326889077e36ad49aa6267ae7285849c6818d
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275861"
---
# <a name="4201---endsqlcommandexecute"></a><span data-ttu-id="d11b1-102">4201 - EndSqlCommandExecute</span><span class="sxs-lookup"><span data-stu-id="d11b1-102">4201 - EndSqlCommandExecute</span></span>

## <a name="properties"></a><span data-ttu-id="d11b1-103">属性</span><span class="sxs-lookup"><span data-stu-id="d11b1-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d11b1-104">ID</span><span class="sxs-lookup"><span data-stu-id="d11b1-104">ID</span></span>|<span data-ttu-id="d11b1-105">4201</span><span class="sxs-lookup"><span data-stu-id="d11b1-105">4201</span></span>|  
|<span data-ttu-id="d11b1-106">关键字</span><span class="sxs-lookup"><span data-stu-id="d11b1-106">Keywords</span></span>|<span data-ttu-id="d11b1-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="d11b1-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="d11b1-108">级别</span><span class="sxs-lookup"><span data-stu-id="d11b1-108">Level</span></span>|<span data-ttu-id="d11b1-109">“详细”</span><span class="sxs-lookup"><span data-stu-id="d11b1-109">Verbose</span></span>|  
|<span data-ttu-id="d11b1-110">通道</span><span class="sxs-lookup"><span data-stu-id="d11b1-110">Channel</span></span>|<span data-ttu-id="d11b1-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="d11b1-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d11b1-112">描述</span><span class="sxs-lookup"><span data-stu-id="d11b1-112">Description</span></span>  

 <span data-ttu-id="d11b1-113">指示 SQL 命令已完成执行。</span><span class="sxs-lookup"><span data-stu-id="d11b1-113">Indicates a SQL command has finished executing.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d11b1-114">消息</span><span class="sxs-lookup"><span data-stu-id="d11b1-114">Message</span></span>  

 <span data-ttu-id="d11b1-115">结束 SQL 命令执行: %1</span><span class="sxs-lookup"><span data-stu-id="d11b1-115">End SQL command execution: %1</span></span>  
  
## <a name="details"></a><span data-ttu-id="d11b1-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="d11b1-116">Details</span></span>  
  
|<span data-ttu-id="d11b1-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="d11b1-117">Data Item Name</span></span>|<span data-ttu-id="d11b1-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="d11b1-118">Data Item Type</span></span>|<span data-ttu-id="d11b1-119">描述</span><span class="sxs-lookup"><span data-stu-id="d11b1-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d11b1-120">SqlCommand</span><span class="sxs-lookup"><span data-stu-id="d11b1-120">SqlCommand</span></span>|<span data-ttu-id="d11b1-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="d11b1-121">xs:string</span></span>|<span data-ttu-id="d11b1-122">已执行的 SQL 命令。</span><span class="sxs-lookup"><span data-stu-id="d11b1-122">The SQL command that was executed.</span></span>|  
|<span data-ttu-id="d11b1-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="d11b1-123">AppDomain</span></span>|<span data-ttu-id="d11b1-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="d11b1-124">xs:string</span></span>|<span data-ttu-id="d11b1-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="d11b1-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
