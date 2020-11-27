---
title: 4206 - UnlockInstanceException
ms.date: 03/30/2017
ms.assetid: 5a46dc5f-d517-4135-8905-25a42f01206b
ms.openlocfilehash: 48182d7c5fe8f29842a17f28c0ea296f93b31089
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96251251"
---
# <a name="4206---unlockinstanceexception"></a><span data-ttu-id="40704-102">4206 - UnlockInstanceException</span><span class="sxs-lookup"><span data-stu-id="40704-102">4206 - UnlockInstanceException</span></span>

## <a name="properties"></a><span data-ttu-id="40704-103">属性</span><span class="sxs-lookup"><span data-stu-id="40704-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="40704-104">ID</span><span class="sxs-lookup"><span data-stu-id="40704-104">ID</span></span>|<span data-ttu-id="40704-105">4206</span><span class="sxs-lookup"><span data-stu-id="40704-105">4206</span></span>|  
|<span data-ttu-id="40704-106">关键字</span><span class="sxs-lookup"><span data-stu-id="40704-106">Keywords</span></span>|<span data-ttu-id="40704-107">WFInstanceStore</span><span class="sxs-lookup"><span data-stu-id="40704-107">WFInstanceStore</span></span>|  
|<span data-ttu-id="40704-108">Level</span><span class="sxs-lookup"><span data-stu-id="40704-108">Level</span></span>|<span data-ttu-id="40704-109">错误</span><span class="sxs-lookup"><span data-stu-id="40704-109">Error</span></span>|  
|<span data-ttu-id="40704-110">通道</span><span class="sxs-lookup"><span data-stu-id="40704-110">Channel</span></span>|<span data-ttu-id="40704-111">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="40704-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="40704-112">描述</span><span class="sxs-lookup"><span data-stu-id="40704-112">Description</span></span>  

 <span data-ttu-id="40704-113">指示在尝试解锁某一实例时遇到了异常。</span><span class="sxs-lookup"><span data-stu-id="40704-113">Indicates an exception was encountered while trying to unlock an instance.</span></span>  
  
## <a name="message"></a><span data-ttu-id="40704-114">消息</span><span class="sxs-lookup"><span data-stu-id="40704-114">Message</span></span>  

 <span data-ttu-id="40704-115">尝试解除实例锁定时遇到异常 %1。</span><span class="sxs-lookup"><span data-stu-id="40704-115">Encountered exception %1 while attempting to unlock instance.</span></span>  
  
## <a name="details"></a><span data-ttu-id="40704-116">详细信息</span><span class="sxs-lookup"><span data-stu-id="40704-116">Details</span></span>  
  
|<span data-ttu-id="40704-117">数据项名称</span><span class="sxs-lookup"><span data-stu-id="40704-117">Data Item Name</span></span>|<span data-ttu-id="40704-118">数据项类型</span><span class="sxs-lookup"><span data-stu-id="40704-118">Data Item Type</span></span>|<span data-ttu-id="40704-119">描述</span><span class="sxs-lookup"><span data-stu-id="40704-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="40704-120">ExceptionMessage</span><span class="sxs-lookup"><span data-stu-id="40704-120">ExceptionMessage</span></span>|<span data-ttu-id="40704-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="40704-121">xs:string</span></span>|<span data-ttu-id="40704-122">来自 SQL 异常的消息。</span><span class="sxs-lookup"><span data-stu-id="40704-122">The message from the SQL exception.</span></span>|  
|<span data-ttu-id="40704-123">应用程序域</span><span class="sxs-lookup"><span data-stu-id="40704-123">AppDomain</span></span>|<span data-ttu-id="40704-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="40704-124">xs:string</span></span>|<span data-ttu-id="40704-125">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="40704-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
