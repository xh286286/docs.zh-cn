---
title: DeliveryRequirementsAttribute
ms.date: 03/30/2017
ms.assetid: 40c5435c-a325-4cf8-9dd0-d6e24b4a56a3
ms.openlocfilehash: a70a4ba40b569acc7893b21d796194224dc4ee78
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96274044"
---
# <a name="deliveryrequirementsattribute"></a><span data-ttu-id="d9343-102">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="d9343-102">DeliveryRequirementsAttribute</span></span>

<span data-ttu-id="d9343-103">DeliveryRequirementsAttribute</span><span class="sxs-lookup"><span data-stu-id="d9343-103">DeliveryRequirementsAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d9343-104">语法</span><span class="sxs-lookup"><span data-stu-id="d9343-104">Syntax</span></span>  
  
```csharp
class DeliveryRequirementsAttribute : Behavior  
{  
  string QueuedDeliveryRequirements;  
  boolean RequireOrderedDelivery;  
  string TargetContract;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="d9343-105">方法</span><span class="sxs-lookup"><span data-stu-id="d9343-105">Methods</span></span>  

 <span data-ttu-id="d9343-106">DeliveryRequirementsAttribute 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="d9343-106">The DeliveryRequirementsAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="d9343-107">属性</span><span class="sxs-lookup"><span data-stu-id="d9343-107">Properties</span></span>  

 <span data-ttu-id="d9343-108">DeliveryRequirementsAttribute 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="d9343-108">The DeliveryRequirementsAttribute class has the following properties:</span></span>  
  
### <a name="queueddeliveryrequirements"></a><span data-ttu-id="d9343-109">QueuedDeliveryRequirements</span><span class="sxs-lookup"><span data-stu-id="d9343-109">QueuedDeliveryRequirements</span></span>  

 <span data-ttu-id="d9343-110">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d9343-110">Data type: string</span></span>  
  
 <span data-ttu-id="d9343-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d9343-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d9343-112">指定服务的绑定是否支持协定。</span><span class="sxs-lookup"><span data-stu-id="d9343-112">Specifies whether the binding for a service supports contracts.</span></span>  
  
### <a name="requireordereddelivery"></a><span data-ttu-id="d9343-113">RequireOrderedDelivery</span><span class="sxs-lookup"><span data-stu-id="d9343-113">RequireOrderedDelivery</span></span>  

 <span data-ttu-id="d9343-114">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d9343-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="d9343-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d9343-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d9343-116">指定绑定是否支持已排序消息。</span><span class="sxs-lookup"><span data-stu-id="d9343-116">Specifies whether the binding supports ordered messages.</span></span>  
  
### <a name="targetcontract"></a><span data-ttu-id="d9343-117">TargetContract</span><span class="sxs-lookup"><span data-stu-id="d9343-117">TargetContract</span></span>  

 <span data-ttu-id="d9343-118">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d9343-118">Data type: string</span></span>  
  
 <span data-ttu-id="d9343-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d9343-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d9343-120">该类应用到的协定。</span><span class="sxs-lookup"><span data-stu-id="d9343-120">The contract to which it applies.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9343-121">要求</span><span class="sxs-lookup"><span data-stu-id="d9343-121">Requirements</span></span>  
  
|<span data-ttu-id="d9343-122">MOF</span><span class="sxs-lookup"><span data-stu-id="d9343-122">MOF</span></span>|<span data-ttu-id="d9343-123">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="d9343-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="d9343-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9343-124">Namespace</span></span>|<span data-ttu-id="d9343-125">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="d9343-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d9343-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9343-126">See also</span></span>

- <xref:System.ServiceModel.DeliveryRequirementsAttribute>
