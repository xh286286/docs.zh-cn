---
title: 3550 - BufferOutOfOrderMessageNoInstance
ms.date: 03/30/2017
ms.assetid: 1299d294-99b8-430e-98b1-55f5f17002f3
ms.openlocfilehash: 61605d666911cce277bcebbb0a2f803e9a5dcfeb
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96261301"
---
# <a name="3550---bufferoutofordermessagenoinstance"></a><span data-ttu-id="7b9c9-102">3550 - BufferOutOfOrderMessageNoInstance</span><span class="sxs-lookup"><span data-stu-id="7b9c9-102">3550 - BufferOutOfOrderMessageNoInstance</span></span>

## <a name="properties"></a><span data-ttu-id="7b9c9-103">属性</span><span class="sxs-lookup"><span data-stu-id="7b9c9-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="7b9c9-104">ID</span><span class="sxs-lookup"><span data-stu-id="7b9c9-104">ID</span></span>|<span data-ttu-id="7b9c9-105">3550</span><span class="sxs-lookup"><span data-stu-id="7b9c9-105">3550</span></span>|  
|<span data-ttu-id="7b9c9-106">关键字</span><span class="sxs-lookup"><span data-stu-id="7b9c9-106">Keywords</span></span>|<span data-ttu-id="7b9c9-107">WFServices</span><span class="sxs-lookup"><span data-stu-id="7b9c9-107">WFServices</span></span>|  
|<span data-ttu-id="7b9c9-108">Level</span><span class="sxs-lookup"><span data-stu-id="7b9c9-108">Level</span></span>|<span data-ttu-id="7b9c9-109">信息</span><span class="sxs-lookup"><span data-stu-id="7b9c9-109">Information</span></span>|  
|<span data-ttu-id="7b9c9-110">通道</span><span class="sxs-lookup"><span data-stu-id="7b9c9-110">Channel</span></span>|<span data-ttu-id="7b9c9-111">Microsoft-Windows-应用程序服务器-应用程序/分析</span><span class="sxs-lookup"><span data-stu-id="7b9c9-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="7b9c9-112">描述</span><span class="sxs-lookup"><span data-stu-id="7b9c9-112">Description</span></span>  

 <span data-ttu-id="7b9c9-113">指示缓冲接收已失败。</span><span class="sxs-lookup"><span data-stu-id="7b9c9-113">Indicates a buffered receive has failed.</span></span> <span data-ttu-id="7b9c9-114">服务实例准备好处理此特定操作时，将再次尝试该操作。</span><span class="sxs-lookup"><span data-stu-id="7b9c9-114">The operation will be attempted again when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="message"></a><span data-ttu-id="7b9c9-115">消息</span><span class="sxs-lookup"><span data-stu-id="7b9c9-115">Message</span></span>  

 <span data-ttu-id="7b9c9-116">此时不能执行操作“%1”。</span><span class="sxs-lookup"><span data-stu-id="7b9c9-116">Operation '%1' cannot be performed at this time.</span></span> <span data-ttu-id="7b9c9-117">服务实例准备好处理此特定操作时，将进行另一个尝试。</span><span class="sxs-lookup"><span data-stu-id="7b9c9-117">Another attempt will be made when the service instance is ready to process this particular operation.</span></span>  
  
## <a name="details"></a><span data-ttu-id="7b9c9-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="7b9c9-118">Details</span></span>  
  
|<span data-ttu-id="7b9c9-119">数据项名称</span><span class="sxs-lookup"><span data-stu-id="7b9c9-119">Data Item Name</span></span>|<span data-ttu-id="7b9c9-120">数据项类型</span><span class="sxs-lookup"><span data-stu-id="7b9c9-120">Data Item Type</span></span>|<span data-ttu-id="7b9c9-121">描述</span><span class="sxs-lookup"><span data-stu-id="7b9c9-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="7b9c9-122">OperationName</span><span class="sxs-lookup"><span data-stu-id="7b9c9-122">OperationName</span></span>|<span data-ttu-id="7b9c9-123">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b9c9-123">xs:string</span></span>|<span data-ttu-id="7b9c9-124">操作的名称。</span><span class="sxs-lookup"><span data-stu-id="7b9c9-124">The name of the operation.</span></span>|  
|<span data-ttu-id="7b9c9-125">应用程序域</span><span class="sxs-lookup"><span data-stu-id="7b9c9-125">AppDomain</span></span>|<span data-ttu-id="7b9c9-126">xs:string</span><span class="sxs-lookup"><span data-stu-id="7b9c9-126">xs:string</span></span>|<span data-ttu-id="7b9c9-127">由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="7b9c9-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
