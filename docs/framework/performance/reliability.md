---
title: 可靠性
description: 了解 .NET 中的可靠性。 防范在 .NET 中执行的主机上的异步异常，如 SQL Server。
ms.date: 03/30/2017
helpviewer_keywords:
- SQL Server [.NET Framework]
- managed code, reliability
- reliability [.NET Framework]
- writing reliable code
- code, reliability
ms.assetid: 294aa306-0afe-4cbe-b397-86ba9f1860f8
ms.openlocfilehash: 00af439a12476addbe564ecf81152a1bc435d637
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96245596"
---
# <a name="reliability"></a><span data-ttu-id="d646a-104">可靠性</span><span class="sxs-lookup"><span data-stu-id="d646a-104">Reliability</span></span>

<span data-ttu-id="d646a-105">在服务器环境（如 SQL Server）中执行的代码防止发生异步异常，这一点非常重要。</span><span class="sxs-lookup"><span data-stu-id="d646a-105">It is important that code executing in server environments such as SQL Server protect against asynchronous exceptions.</span></span> <span data-ttu-id="d646a-106">文本所讨论的可靠性并不是针对 SQL Server 而言，而是针对为在 .NET Framework 版本 2.0 环境中执行的任何主机编写可靠代码而言。</span><span class="sxs-lookup"><span data-stu-id="d646a-106">Reliability, as discussed here, is not specific to SQL Server but to writing reliable code for any host executing in a .NET Framework version 2.0 environment.</span></span> <span data-ttu-id="d646a-107">SQL Server 是第一个广泛使用版本 2.0 的新可靠性功能的服务，所以将其作为示例。</span><span class="sxs-lookup"><span data-stu-id="d646a-107">However, SQL Server is the first service making extensive use of the new reliability features of version 2.0, so it is used as an example.</span></span>  
  
 <span data-ttu-id="d646a-108">在 SQL Server 中运行的代码必须使用与其他服务器环境相比更严格的可靠性准则。</span><span class="sxs-lookup"><span data-stu-id="d646a-108">Code running in SQL Server must deal with more stringent reliability guidelines than other server environments.</span></span> <span data-ttu-id="d646a-109">这是因为 SQL Server 在资源消耗方面的稳定操作。</span><span class="sxs-lookup"><span data-stu-id="d646a-109">This is due to SQL Server’s steady operation at the edge of resource consumption.</span></span>  <span data-ttu-id="d646a-110"><xref:System.OutOfMemoryException> 和 <xref:System.Threading.ThreadAbortException> 异常在 SQL Server 环境中比较常见。</span><span class="sxs-lookup"><span data-stu-id="d646a-110"><xref:System.OutOfMemoryException> and <xref:System.Threading.ThreadAbortException> exceptions are not uncommon in the SQL Server environment.</span></span> <span data-ttu-id="d646a-111">这些准则通常较少强调可靠性，更多专注于允许完全信任的托管代码面对 <xref:System.AppDomain> 级别的回收温和地失败，这是服务器维持一致性和可用性的主要方法。</span><span class="sxs-lookup"><span data-stu-id="d646a-111">These guidelines in general are focused less on reliability and more on allowing fully trusted managed code to fail gracefully in the face of <xref:System.AppDomain>-level recycling, which is the primary way the server maintains consistency and availability.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d646a-112">本节内容</span><span class="sxs-lookup"><span data-stu-id="d646a-112">In This Section</span></span>  

 [<span data-ttu-id="d646a-113">SQL Server 编程和宿主保护特性</span><span class="sxs-lookup"><span data-stu-id="d646a-113">SQL Server Programming and Host Protection Attributes</span></span>](sql-server-programming-and-host-protection-attributes.md)  
 <span data-ttu-id="d646a-114">介绍 SQL Server 如何使用 <xref:System.Security.Permissions.HostProtectionAttribute> 属性限制托管代码的执行。</span><span class="sxs-lookup"><span data-stu-id="d646a-114">Describes how the <xref:System.Security.Permissions.HostProtectionAttribute> attribute is used by SQL Server to restrict the execution of managed code.</span></span>  
  
 [<span data-ttu-id="d646a-115">可靠性最佳做法</span><span class="sxs-lookup"><span data-stu-id="d646a-115">Reliability Best Practices</span></span>](reliability-best-practices.md)  
 <span data-ttu-id="d646a-116">提供用于编写符合可靠性要求的代码的准则。</span><span class="sxs-lookup"><span data-stu-id="d646a-116">Provides guidelines for writing code that meets reliability requirements.</span></span>  
  
 [<span data-ttu-id="d646a-117">受约束的执行区域</span><span class="sxs-lookup"><span data-stu-id="d646a-117">Constrained Execution Regions</span></span>](constrained-execution-regions.md)  
 <span data-ttu-id="d646a-118">介绍受约束的执行区域 (CER) 的功能和行为。</span><span class="sxs-lookup"><span data-stu-id="d646a-118">Describes the function and behavior of constrained execution regions (CERs).</span></span>  
  
## <a name="reference"></a><span data-ttu-id="d646a-119">引用</span><span class="sxs-lookup"><span data-stu-id="d646a-119">Reference</span></span>  

 <xref:System.Security.Permissions.HostProtectionAttribute>  
  
 <xref:System.Security.Permissions.HostProtectionResource>
