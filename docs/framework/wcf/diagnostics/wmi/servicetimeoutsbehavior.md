---
title: ServiceTimeoutsBehavior
ms.date: 03/30/2017
ms.assetid: 4412525d-a3cc-4eae-b3e8-a50ce766d09d
ms.openlocfilehash: 867219130fc853f3ba2c1c2f807b1651f6480f13
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96273966"
---
# <a name="servicetimeoutsbehavior"></a><span data-ttu-id="548fd-102">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="548fd-102">ServiceTimeoutsBehavior</span></span>

<span data-ttu-id="548fd-103">ServiceTimeoutsBehavior</span><span class="sxs-lookup"><span data-stu-id="548fd-103">ServiceTimeoutsBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="548fd-104">语法</span><span class="sxs-lookup"><span data-stu-id="548fd-104">Syntax</span></span>  
  
```csharp
class ServiceTimeoutsBehavior : Behavior  
{  
  datetime TransactionTimeout;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="548fd-105">方法</span><span class="sxs-lookup"><span data-stu-id="548fd-105">Methods</span></span>  

 <span data-ttu-id="548fd-106">ServiceTimeoutsBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="548fd-106">The ServiceTimeoutsBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="548fd-107">属性</span><span class="sxs-lookup"><span data-stu-id="548fd-107">Properties</span></span>  

 <span data-ttu-id="548fd-108">ServiceTimeoutsBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="548fd-108">The ServiceTimeoutsBehavior class has the following property:</span></span>  
  
### <a name="transactiontimeout"></a><span data-ttu-id="548fd-109">TransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="548fd-109">TransactionTimeout</span></span>  

 <span data-ttu-id="548fd-110">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="548fd-110">Data type: datetime</span></span>  
  
 <span data-ttu-id="548fd-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="548fd-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="548fd-112">事务必须在此期间完成的时间段。</span><span class="sxs-lookup"><span data-stu-id="548fd-112">The period within which a transaction must complete.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="548fd-113">要求</span><span class="sxs-lookup"><span data-stu-id="548fd-113">Requirements</span></span>  
  
|<span data-ttu-id="548fd-114">MOF</span><span class="sxs-lookup"><span data-stu-id="548fd-114">MOF</span></span>|<span data-ttu-id="548fd-115">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="548fd-115">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="548fd-116">命名空间</span><span class="sxs-lookup"><span data-stu-id="548fd-116">Namespace</span></span>|<span data-ttu-id="548fd-117">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="548fd-117">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="548fd-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="548fd-118">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
