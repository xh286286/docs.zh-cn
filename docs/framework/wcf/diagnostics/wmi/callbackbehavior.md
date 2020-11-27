---
title: CallbackBehavior
ms.date: 03/30/2017
ms.assetid: 42acd302-2b62-4849-a2d1-a03084343ecd
ms.openlocfilehash: cec9005a099247671dbebaacc0b242ca8d7a0144
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96269643"
---
# <a name="callbackbehavior"></a><span data-ttu-id="d74a1-102">CallbackBehavior</span><span class="sxs-lookup"><span data-stu-id="d74a1-102">CallbackBehavior</span></span>

<span data-ttu-id="d74a1-103">CallbackBehavior</span><span class="sxs-lookup"><span data-stu-id="d74a1-103">CallbackBehavior</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d74a1-104">语法</span><span class="sxs-lookup"><span data-stu-id="d74a1-104">Syntax</span></span>  
  
```csharp
class CallbackBehavior : Behavior  
{  
  boolean AutomaticSessionShutdown;  
  string ConcurrencyMode;  
  boolean IgnoreExtensionDataObject;  
  boolean IncludeExceptionDetailInFaults;  
  boolean MaxItemsInObjectGraph;  
  boolean UseSynchronizationContext;  
  boolean ValidateMustUnderstand;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="d74a1-105">方法</span><span class="sxs-lookup"><span data-stu-id="d74a1-105">Methods</span></span>  

 <span data-ttu-id="d74a1-106">CallbackBehavior 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="d74a1-106">The CallbackBehavior class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="d74a1-107">属性</span><span class="sxs-lookup"><span data-stu-id="d74a1-107">Properties</span></span>  

 <span data-ttu-id="d74a1-108">CallbackBehavior 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="d74a1-108">The CallbackBehavior class has the following properties:</span></span>  
  
### <a name="automaticsessionshutdown"></a><span data-ttu-id="d74a1-109">AutomaticSessionShutdown</span><span class="sxs-lookup"><span data-stu-id="d74a1-109">AutomaticSessionShutdown</span></span>  

 <span data-ttu-id="d74a1-110">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d74a1-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="d74a1-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-112">如果为 true，则会话在服务关闭双工会话时自动关闭。</span><span class="sxs-lookup"><span data-stu-id="d74a1-112">When true, the session is automatically closed when a service closes a duplex session.</span></span>  
  
### <a name="concurrencymode"></a><span data-ttu-id="d74a1-113">ConcurrencyMode</span><span class="sxs-lookup"><span data-stu-id="d74a1-113">ConcurrencyMode</span></span>  

 <span data-ttu-id="d74a1-114">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="d74a1-114">Data type: string</span></span>  
<span data-ttu-id="d74a1-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-116">指定服务是支持一个线程、多个线程还是支持可重入调用。</span><span class="sxs-lookup"><span data-stu-id="d74a1-116">Specifies whether the service supports one thread, multiple threads, or reentrant calls.</span></span>  
  
### <a name="ignoreextensiondataobject"></a><span data-ttu-id="d74a1-117">IgnoreExtensionDataObject</span><span class="sxs-lookup"><span data-stu-id="d74a1-117">IgnoreExtensionDataObject</span></span>  

 <span data-ttu-id="d74a1-118">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d74a1-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="d74a1-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-120">一个值，指定是否将未知序列化数据发送到网络上。</span><span class="sxs-lookup"><span data-stu-id="d74a1-120">A value that specifies whether to send unknown serialization data onto the wire.</span></span>  
  
### <a name="includeexceptiondetailinfaults"></a><span data-ttu-id="d74a1-121">IncludeExceptionDetailInFaults</span><span class="sxs-lookup"><span data-stu-id="d74a1-121">IncludeExceptionDetailInFaults</span></span>  

 <span data-ttu-id="d74a1-122">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d74a1-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="d74a1-123">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-124">如果启用，则回调异常的详细信息被附加到服务所返回的错误中。</span><span class="sxs-lookup"><span data-stu-id="d74a1-124">When enabled, details about exceptions on the callback are attached to the faults returned to the service.</span></span>  
  
### <a name="maxitemsinobjectgraph"></a><span data-ttu-id="d74a1-125">MaxItemsInObjectGraph</span><span class="sxs-lookup"><span data-stu-id="d74a1-125">MaxItemsInObjectGraph</span></span>  

 <span data-ttu-id="d74a1-126">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d74a1-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="d74a1-127">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-128">序列化对象中允许的最大项数。</span><span class="sxs-lookup"><span data-stu-id="d74a1-128">The maximum number of items allowed in a serialized object.</span></span>  
  
### <a name="usesynchronizationcontext"></a><span data-ttu-id="d74a1-129">UseSynchronizationContext</span><span class="sxs-lookup"><span data-stu-id="d74a1-129">UseSynchronizationContext</span></span>  

 <span data-ttu-id="d74a1-130">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d74a1-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="d74a1-131">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-132">指定是否使用当前同步上下文来选择执行的线程。</span><span class="sxs-lookup"><span data-stu-id="d74a1-132">Specifies whether to use the current synchronization context to choose the thread of execution.</span></span>  
  
### <a name="validatemustunderstand"></a><span data-ttu-id="d74a1-133">ValidateMustUnderstand</span><span class="sxs-lookup"><span data-stu-id="d74a1-133">ValidateMustUnderstand</span></span>  

 <span data-ttu-id="d74a1-134">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="d74a1-134">Data type: boolean</span></span>  
  
 <span data-ttu-id="d74a1-135">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="d74a1-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="d74a1-136">指定系统或应用程序是否强制执行 SOAP MustUnderstand 标头处理。</span><span class="sxs-lookup"><span data-stu-id="d74a1-136">Specifies whether the system or the application enforces SOAP MustUnderstand header processing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d74a1-137">要求</span><span class="sxs-lookup"><span data-stu-id="d74a1-137">Requirements</span></span>  
  
|<span data-ttu-id="d74a1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d74a1-138">MOF</span></span>|<span data-ttu-id="d74a1-139">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="d74a1-139">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="d74a1-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="d74a1-140">Namespace</span></span>|<span data-ttu-id="d74a1-141">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="d74a1-141">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d74a1-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d74a1-142">See also</span></span>

- <xref:System.ServiceModel.CallbackBehaviorAttribute>
