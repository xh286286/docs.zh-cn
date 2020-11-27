---
title: 终结点
ms.date: 03/30/2017
ms.assetid: fe63370d-81a1-40f3-97c2-59cb357c78d2
ms.openlocfilehash: ceb4e4b41502b00d7bb21f1ecbd8249fccf1ce3b
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96288809"
---
# <a name="endpoint"></a><span data-ttu-id="9f90f-102">终结点</span><span class="sxs-lookup"><span data-stu-id="9f90f-102">Endpoint</span></span>

<span data-ttu-id="9f90f-103">终结点</span><span class="sxs-lookup"><span data-stu-id="9f90f-103">Endpoint</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f90f-104">语法</span><span class="sxs-lookup"><span data-stu-id="9f90f-104">Syntax</span></span>  
  
```csharp
class Endpoint  
{  
  string Address;  
  string AddressHeaders[];  
  string AddressIdentity;  
  sint32 AppDomainId;  
  Behavior Behaviors[];  
  Binding Binding;  
  string ContractName;  
  string CounterInstanceName;  
  string ListenUri;  
  string Name;  
  sint32 ProcessId;  
  Contract ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="9f90f-105">方法</span><span class="sxs-lookup"><span data-stu-id="9f90f-105">Methods</span></span>  

 <span data-ttu-id="9f90f-106">该终结点类定义以下方法。</span><span class="sxs-lookup"><span data-stu-id="9f90f-106">The Endpoint class defines the following method.</span></span>  
  
|<span data-ttu-id="9f90f-107">方法</span><span class="sxs-lookup"><span data-stu-id="9f90f-107">Method</span></span>|<span data-ttu-id="9f90f-108">描述</span><span class="sxs-lookup"><span data-stu-id="9f90f-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9f90f-109">GetOperationCounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="9f90f-109">GetOperationCounterInstanceName</span></span>](getoperationcounterinstancename.md)|<span data-ttu-id="9f90f-110">检索操作性能计数器实例名称</span><span class="sxs-lookup"><span data-stu-id="9f90f-110">Retrieves the operation performance counter instance name</span></span>|  
  
## <a name="properties"></a><span data-ttu-id="9f90f-111">属性</span><span class="sxs-lookup"><span data-stu-id="9f90f-111">Properties</span></span>  

 <span data-ttu-id="9f90f-112">该终结点类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="9f90f-112">The Endpoint class has the following properties:</span></span>  
  
### <a name="address"></a><span data-ttu-id="9f90f-113">地址</span><span class="sxs-lookup"><span data-stu-id="9f90f-113">Address</span></span>  

 <span data-ttu-id="9f90f-114">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f90f-114">Data type: string</span></span>  
  
 <span data-ttu-id="9f90f-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-116">一个包含终结点地址的 URI。</span><span class="sxs-lookup"><span data-stu-id="9f90f-116">A URI that contains the address of the endpoint.</span></span>  
  
### <a name="addressheaders"></a><span data-ttu-id="9f90f-117">AddressHeaders</span><span class="sxs-lookup"><span data-stu-id="9f90f-117">AddressHeaders</span></span>  

 <span data-ttu-id="9f90f-118">数据类型：String array</span><span class="sxs-lookup"><span data-stu-id="9f90f-118">Data type: string array</span></span>  
  
 <span data-ttu-id="9f90f-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-120">附加到此终结点的地址头的集合。</span><span class="sxs-lookup"><span data-stu-id="9f90f-120">The collection of address headers attached to this endpoint.</span></span>  
  
### <a name="addressidentity"></a><span data-ttu-id="9f90f-121">AddressIdentity</span><span class="sxs-lookup"><span data-stu-id="9f90f-121">AddressIdentity</span></span>  

 <span data-ttu-id="9f90f-122">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f90f-122">Data type: string</span></span>  
  
 <span data-ttu-id="9f90f-123">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-124">终结点的标识。</span><span class="sxs-lookup"><span data-stu-id="9f90f-124">The identity of the endpoint.</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="9f90f-125">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="9f90f-125">AppDomainId</span></span>  

 <span data-ttu-id="9f90f-126">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="9f90f-126">Data type: sint32</span></span>  
  
 <span data-ttu-id="9f90f-127">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-128">承载终结点的 AppDomain 的 AppDomain ID。</span><span class="sxs-lookup"><span data-stu-id="9f90f-128">The appdomain id of the appdomain that hosts the endpoint.</span></span>  
  
### <a name="behaviors"></a><span data-ttu-id="9f90f-129">行为</span><span class="sxs-lookup"><span data-stu-id="9f90f-129">Behaviors</span></span>  

 <span data-ttu-id="9f90f-130">数据类型：Behavior array</span><span class="sxs-lookup"><span data-stu-id="9f90f-130">Data type: Behavior array</span></span>  
  
 <span data-ttu-id="9f90f-131">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-132">此终结点所实现的行为的集合。</span><span class="sxs-lookup"><span data-stu-id="9f90f-132">The collection of behaviors implemented by this endpoint.</span></span>  
  
### <a name="binding"></a><span data-ttu-id="9f90f-133">绑定</span><span class="sxs-lookup"><span data-stu-id="9f90f-133">Binding</span></span>  

 <span data-ttu-id="9f90f-134">数据类型：绑定</span><span class="sxs-lookup"><span data-stu-id="9f90f-134">Data type: Binding</span></span>  
  
 <span data-ttu-id="9f90f-135">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-136">此终结点所使用的绑定。</span><span class="sxs-lookup"><span data-stu-id="9f90f-136">The binding used by this endpoint.</span></span>  
  
### <a name="contractname"></a><span data-ttu-id="9f90f-137">ContractName</span><span class="sxs-lookup"><span data-stu-id="9f90f-137">ContractName</span></span>  

 <span data-ttu-id="9f90f-138">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f90f-138">Data type: string</span></span>  
  
 <span data-ttu-id="9f90f-139">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-140">一个字符串，指定此终结点公开了哪个协定。</span><span class="sxs-lookup"><span data-stu-id="9f90f-140">A string that specifies which contract this endpoint is exposing.</span></span>  
  
### <a name="counterinstancename"></a><span data-ttu-id="9f90f-141">CounterInstanceName</span><span class="sxs-lookup"><span data-stu-id="9f90f-141">CounterInstanceName</span></span>  

 <span data-ttu-id="9f90f-142">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f90f-142">Data type: string</span></span>  
  
 <span data-ttu-id="9f90f-143">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-144">该终结点的性能计数器的实例名称。</span><span class="sxs-lookup"><span data-stu-id="9f90f-144">The name of the instance of performance counters of the endpoint.</span></span>  
  
### <a name="listenuri"></a><span data-ttu-id="9f90f-145">ListenUri</span><span class="sxs-lookup"><span data-stu-id="9f90f-145">ListenUri</span></span>  

 <span data-ttu-id="9f90f-146">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f90f-146">Data type: string</span></span>  
  
 <span data-ttu-id="9f90f-147">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-148">终结点在其上侦听的 Uri。</span><span class="sxs-lookup"><span data-stu-id="9f90f-148">The Uri the endpoint listens on.</span></span>  
  
### <a name="name"></a><span data-ttu-id="9f90f-149">“属性”</span><span class="sxs-lookup"><span data-stu-id="9f90f-149">Name</span></span>  

 <span data-ttu-id="9f90f-150">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="9f90f-150">Data type: string</span></span>  
  
 <span data-ttu-id="9f90f-151">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-151">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-152">此终结点的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="9f90f-152">The unique name of this endpoint.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="9f90f-153">ProcessId</span><span class="sxs-lookup"><span data-stu-id="9f90f-153">ProcessId</span></span>  

 <span data-ttu-id="9f90f-154">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="9f90f-154">Data type: sint32</span></span>  
  
 <span data-ttu-id="9f90f-155">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-156">承载该终结点的进程的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="9f90f-156">The process Id of the process that hosts the endpoint.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="9f90f-157">ref</span><span class="sxs-lookup"><span data-stu-id="9f90f-157">ref</span></span>  

 <span data-ttu-id="9f90f-158">数据类型：Contract</span><span class="sxs-lookup"><span data-stu-id="9f90f-158">Data type: Contract</span></span>  
  
 <span data-ttu-id="9f90f-159">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="9f90f-159">Access type: Read-only</span></span>  
  
 <span data-ttu-id="9f90f-160">此终结点公开的协定。</span><span class="sxs-lookup"><span data-stu-id="9f90f-160">The contract this endpoint is exposing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f90f-161">要求</span><span class="sxs-lookup"><span data-stu-id="9f90f-161">Requirements</span></span>  
  
|<span data-ttu-id="9f90f-162">MOF</span><span class="sxs-lookup"><span data-stu-id="9f90f-162">MOF</span></span>|<span data-ttu-id="9f90f-163">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="9f90f-163">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="9f90f-164">命名空间</span><span class="sxs-lookup"><span data-stu-id="9f90f-164">Namespace</span></span>|<span data-ttu-id="9f90f-165">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="9f90f-165">Defined in root\ServiceModel</span></span>|
