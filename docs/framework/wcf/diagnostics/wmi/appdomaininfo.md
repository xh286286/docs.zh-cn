---
title: AppDomainInfo
ms.date: 03/30/2017
ms.assetid: 6610b7d8-81eb-4bec-a543-9b72ad7b6f73
ms.openlocfilehash: c5c44f4d8f6d93443802d5e1950c4d850976c5b6
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96291123"
---
# <a name="appdomaininfo"></a><span data-ttu-id="6cb17-102">AppDomainInfo</span><span class="sxs-lookup"><span data-stu-id="6cb17-102">AppDomainInfo</span></span>

<span data-ttu-id="6cb17-103">应用程序域信息</span><span class="sxs-lookup"><span data-stu-id="6cb17-103">Application domain information</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cb17-104">语法</span><span class="sxs-lookup"><span data-stu-id="6cb17-104">Syntax</span></span>  
  
```csharp
class AppDomainInfo  
{  
  sint32 AppDomainId;  
  boolean IsDefault;  
  boolean LogMalformedMessages;  
  boolean LogMessagesAtServiceLevel;  
  boolean LogMessagesAtTransportLevel;  
  TraceListener MessageLoggingTraceListeners[];  
  string Name;  
  string PerformanceCounters;  
  sint32 ProcessId;  
  string ServiceConfigPath;  
  string TraceLevel;  
  TraceListener wmiTraceListeners[];  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="6cb17-105">方法</span><span class="sxs-lookup"><span data-stu-id="6cb17-105">Methods</span></span>  

 <span data-ttu-id="6cb17-106">AppDomainInfo 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="6cb17-106">The AppDomainInfo class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="6cb17-107">属性</span><span class="sxs-lookup"><span data-stu-id="6cb17-107">Properties</span></span>  

 <span data-ttu-id="6cb17-108">AppDomainInfo 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="6cb17-108">The AppDomainInfo class has the following properties:</span></span>  
  
### <a name="appdomainid"></a><span data-ttu-id="6cb17-109">AppDomainId</span><span class="sxs-lookup"><span data-stu-id="6cb17-109">AppDomainId</span></span>  

 <span data-ttu-id="6cb17-110">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="6cb17-110">Data type: sint32</span></span>  
  
 <span data-ttu-id="6cb17-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-112">Appdomain 的 ID。</span><span class="sxs-lookup"><span data-stu-id="6cb17-112">The Id of the appdomain.</span></span>  
  
### <a name="isdefault"></a><span data-ttu-id="6cb17-113">IsDefault</span><span class="sxs-lookup"><span data-stu-id="6cb17-113">IsDefault</span></span>  

 <span data-ttu-id="6cb17-114">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb17-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="6cb17-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-116">指示该 appdomain 是否为默认 appdomain。</span><span class="sxs-lookup"><span data-stu-id="6cb17-116">Indicates whether the appdomain is the default appdomain.</span></span>  
  
### <a name="logmalformedmessages"></a><span data-ttu-id="6cb17-117">LogMalformedMessages</span><span class="sxs-lookup"><span data-stu-id="6cb17-117">LogMalformedMessages</span></span>  

 <span data-ttu-id="6cb17-118">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb17-118">Data type: boolean</span></span>  
  
 <span data-ttu-id="6cb17-119">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="6cb17-119">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="6cb17-120">一个值，指定是否记录格式不正确的消息。</span><span class="sxs-lookup"><span data-stu-id="6cb17-120">A value that specifies whether malformed messages are logged.</span></span>  
  
### <a name="logmessagesatservicelevel"></a><span data-ttu-id="6cb17-121">LogMessagesAtServiceLevel</span><span class="sxs-lookup"><span data-stu-id="6cb17-121">LogMessagesAtServiceLevel</span></span>  

 <span data-ttu-id="6cb17-122">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb17-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="6cb17-123">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="6cb17-123">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="6cb17-124">一个值，指定是否在服务级别跟踪消息（在与加密和传输有关的转换之前）。</span><span class="sxs-lookup"><span data-stu-id="6cb17-124">A value that specifies whether messages are traced at the service level (before encryption and transport-related transforms).</span></span>  
  
### <a name="logmessagesattransportlevel"></a><span data-ttu-id="6cb17-125">LogMessagesAtTransportLevel</span><span class="sxs-lookup"><span data-stu-id="6cb17-125">LogMessagesAtTransportLevel</span></span>  

 <span data-ttu-id="6cb17-126">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="6cb17-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="6cb17-127">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="6cb17-127">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="6cb17-128">一个值，指定是否在传输级别跟踪消息。</span><span class="sxs-lookup"><span data-stu-id="6cb17-128">A value that specifies whether messages are traced at the transport level.</span></span>  
  
### <a name="messageloggingtracelisteners"></a><span data-ttu-id="6cb17-129">MessageLoggingTraceListeners</span><span class="sxs-lookup"><span data-stu-id="6cb17-129">MessageLoggingTraceListeners</span></span>  

 <span data-ttu-id="6cb17-130">数据类型：TraceListener 数组</span><span class="sxs-lookup"><span data-stu-id="6cb17-130">Data type: TraceListener array</span></span>  
  
 <span data-ttu-id="6cb17-131">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-132">侦听 System.Wmi.MessageLogging 跟踪源的集合跟踪侦听器。</span><span class="sxs-lookup"><span data-stu-id="6cb17-132">The collection trace listeners that listen to the System.Wmi.MessageLogging trace source.</span></span>  
  
### <a name="name"></a><span data-ttu-id="6cb17-133">“属性”</span><span class="sxs-lookup"><span data-stu-id="6cb17-133">Name</span></span>  

 <span data-ttu-id="6cb17-134">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="6cb17-134">Data type: string</span></span>  
  
 <span data-ttu-id="6cb17-135">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-136">Appdomain 的名称。</span><span class="sxs-lookup"><span data-stu-id="6cb17-136">The name of the appdomain.</span></span>  
  
### <a name="performancecounters"></a><span data-ttu-id="6cb17-137">PerformanceCounters</span><span class="sxs-lookup"><span data-stu-id="6cb17-137">PerformanceCounters</span></span>  

 <span data-ttu-id="6cb17-138">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="6cb17-138">Data type: string</span></span>  
  
 <span data-ttu-id="6cb17-139">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-140">Appdomain 中的活动性能计数器的范围。</span><span class="sxs-lookup"><span data-stu-id="6cb17-140">The scope of active performance counters in the appdomain.</span></span>  
  
### <a name="processid"></a><span data-ttu-id="6cb17-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="6cb17-141">ProcessId</span></span>  

 <span data-ttu-id="6cb17-142">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="6cb17-142">Data type: sint32</span></span>  
  
 <span data-ttu-id="6cb17-143">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-143">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-144">进程 ID。</span><span class="sxs-lookup"><span data-stu-id="6cb17-144">The process Id.</span></span>  
  
### <a name="serviceconfigpath"></a><span data-ttu-id="6cb17-145">ServiceConfigPath</span><span class="sxs-lookup"><span data-stu-id="6cb17-145">ServiceConfigPath</span></span>  

 <span data-ttu-id="6cb17-146">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="6cb17-146">Data type: string</span></span>  
  
 <span data-ttu-id="6cb17-147">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-147">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-148">服务配置的路径。</span><span class="sxs-lookup"><span data-stu-id="6cb17-148">The path to the configuration of the service.</span></span>  
  
### <a name="tracelevel"></a><span data-ttu-id="6cb17-149">TraceLevel</span><span class="sxs-lookup"><span data-stu-id="6cb17-149">TraceLevel</span></span>  

 <span data-ttu-id="6cb17-150">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="6cb17-150">Data type: string</span></span>  
  
 <span data-ttu-id="6cb17-151">访问类型：读/写</span><span class="sxs-lookup"><span data-stu-id="6cb17-151">Access type: Read/Write</span></span>  
  
 <span data-ttu-id="6cb17-152">System.Wmi 跟踪源的跟踪级别。</span><span class="sxs-lookup"><span data-stu-id="6cb17-152">The trace level of the System.Wmi trace source.</span></span>  
  
### <a name="servicemodeltracelisteners"></a><span data-ttu-id="6cb17-153">ServiceModelTraceListeners</span><span class="sxs-lookup"><span data-stu-id="6cb17-153">ServiceModelTraceListeners</span></span>  

 <span data-ttu-id="6cb17-154">数据类型：TraceListener 数组</span><span class="sxs-lookup"><span data-stu-id="6cb17-154">Data type: TraceListener array</span></span>  
  
 <span data-ttu-id="6cb17-155">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="6cb17-155">Access type: Read-only</span></span>  
  
 <span data-ttu-id="6cb17-156">一个来自 System.ServiceModel 跟踪源的侦听器的集合。</span><span class="sxs-lookup"><span data-stu-id="6cb17-156">A collection of listeners from the System.ServiceModel trace source.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6cb17-157">要求</span><span class="sxs-lookup"><span data-stu-id="6cb17-157">Requirements</span></span>  
  
|<span data-ttu-id="6cb17-158">MOF</span><span class="sxs-lookup"><span data-stu-id="6cb17-158">MOF</span></span>|<span data-ttu-id="6cb17-159">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="6cb17-159">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="6cb17-160">命名空间</span><span class="sxs-lookup"><span data-stu-id="6cb17-160">Namespace</span></span>|<span data-ttu-id="6cb17-161">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="6cb17-161">Defined in root\ServiceModel</span></span>|
