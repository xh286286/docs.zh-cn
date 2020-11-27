---
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 6e20556541b1aa48e7dfc6a8cde97e1bc477457e
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96273940"
---
# <a name="servicetoendpointassociation"></a><span data-ttu-id="9f744-102">ServiceToEndpointAssociation</span><span class="sxs-lookup"><span data-stu-id="9f744-102">ServiceToEndpointAssociation</span></span>

<span data-ttu-id="9f744-103">将服务映射到终结点。</span><span class="sxs-lookup"><span data-stu-id="9f744-103">Maps a service to an endpoint.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f744-104">语法</span><span class="sxs-lookup"><span data-stu-id="9f744-104">Syntax</span></span>  
  
```csharp
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="9f744-105">方法</span><span class="sxs-lookup"><span data-stu-id="9f744-105">Methods</span></span>  

 <span data-ttu-id="9f744-106">ServiceToEndpointAssociation 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="9f744-106">The ServiceToEndpointAssociation class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="9f744-107">属性</span><span class="sxs-lookup"><span data-stu-id="9f744-107">Properties</span></span>  

 <span data-ttu-id="9f744-108">ServiceToEndpointAssociation 类有以下属性：</span><span class="sxs-lookup"><span data-stu-id="9f744-108">The ServiceToEndpointAssociation class has the following properties:</span></span>  
  
### <a name="ref"></a><span data-ttu-id="9f744-109">ref</span><span class="sxs-lookup"><span data-stu-id="9f744-109">ref</span></span>  

 <span data-ttu-id="9f744-110">数据类型：Service</span><span class="sxs-lookup"><span data-stu-id="9f744-110">Data type: Service</span></span>  
  
 <span data-ttu-id="9f744-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f744-111">Access type: Read-only</span></span>  
<span data-ttu-id="9f744-112">限定符：键</span><span class="sxs-lookup"><span data-stu-id="9f744-112">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="9f744-113">与终结点关联的服务。</span><span class="sxs-lookup"><span data-stu-id="9f744-113">The service associated with the endpoint.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="9f744-114">ref</span><span class="sxs-lookup"><span data-stu-id="9f744-114">ref</span></span>  

 <span data-ttu-id="9f744-115">数据类型：Endpoint</span><span class="sxs-lookup"><span data-stu-id="9f744-115">Data type: Endpoint</span></span>  
  
 <span data-ttu-id="9f744-116">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f744-116">Access type: Read-only</span></span>  
<span data-ttu-id="9f744-117">限定符：键</span><span class="sxs-lookup"><span data-stu-id="9f744-117">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="9f744-118">与服务关联的终结点。</span><span class="sxs-lookup"><span data-stu-id="9f744-118">The endpoint associated with the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f744-119">要求</span><span class="sxs-lookup"><span data-stu-id="9f744-119">Requirements</span></span>  
  
|<span data-ttu-id="9f744-120">MOF</span><span class="sxs-lookup"><span data-stu-id="9f744-120">MOF</span></span>|<span data-ttu-id="9f744-121">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="9f744-121">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="9f744-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="9f744-122">Namespace</span></span>|<span data-ttu-id="9f744-123">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="9f744-123">Defined in root\ServiceModel</span></span>|
