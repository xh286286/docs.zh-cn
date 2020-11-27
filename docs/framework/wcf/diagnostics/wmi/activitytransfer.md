---
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: f1978881517fe5010ccc0f5192b21bd6688f063a
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96291110"
---
# <a name="activitytransfer"></a><span data-ttu-id="b30a8-102">ActivityTransfer</span><span class="sxs-lookup"><span data-stu-id="b30a8-102">ActivityTransfer</span></span>

<span data-ttu-id="b30a8-103">活动传输事件</span><span class="sxs-lookup"><span data-stu-id="b30a8-103">Activity Transfer Event</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b30a8-104">语法</span><span class="sxs-lookup"><span data-stu-id="b30a8-104">Syntax</span></span>  
  
```csharp
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="b30a8-105">方法</span><span class="sxs-lookup"><span data-stu-id="b30a8-105">Methods</span></span>  

 <span data-ttu-id="b30a8-106">ActivityTransfer 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="b30a8-106">The ActivityTransfer class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="b30a8-107">属性</span><span class="sxs-lookup"><span data-stu-id="b30a8-107">Properties</span></span>  

 <span data-ttu-id="b30a8-108">ActivityTransfer 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="b30a8-108">The ActivityTransfer class has the following properties:</span></span>  
  
### <a name="activityid"></a><span data-ttu-id="b30a8-109">ActivityID</span><span class="sxs-lookup"><span data-stu-id="b30a8-109">ActivityID</span></span>  
  
- <span data-ttu-id="b30a8-110">数据类型：object</span><span class="sxs-lookup"><span data-stu-id="b30a8-110">Data type: object</span></span>  
    <span data-ttu-id="b30a8-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b30a8-111">Access type: Read-only</span></span>  
  
- <span data-ttu-id="b30a8-112">活动 ID</span><span class="sxs-lookup"><span data-stu-id="b30a8-112">Activity ID</span></span>  
  
### <a name="relatedactivityid"></a><span data-ttu-id="b30a8-113">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="b30a8-113">RelatedActivityID</span></span>  
  
- <span data-ttu-id="b30a8-114">数据类型：object</span><span class="sxs-lookup"><span data-stu-id="b30a8-114">Data type: object</span></span>  
    <span data-ttu-id="b30a8-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="b30a8-115">Access type: Read-only</span></span>  
  
- <span data-ttu-id="b30a8-116">相关活动 ID</span><span class="sxs-lookup"><span data-stu-id="b30a8-116">Related Activity ID</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b30a8-117">要求</span><span class="sxs-lookup"><span data-stu-id="b30a8-117">Requirements</span></span>  
  
|<span data-ttu-id="b30a8-118">MOF</span><span class="sxs-lookup"><span data-stu-id="b30a8-118">MOF</span></span>|<span data-ttu-id="b30a8-119">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="b30a8-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="b30a8-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="b30a8-120">Namespace</span></span>|<span data-ttu-id="b30a8-121">已在 root\ServiceModel 中定义。</span><span class="sxs-lookup"><span data-stu-id="b30a8-121">Defined in root\ServiceModel.</span></span>|
