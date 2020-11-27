---
title: 行为安全
ms.date: 03/30/2017
ms.assetid: 19710ae3-f197-4d28-ba9d-52e465006819
ms.openlocfilehash: c06c615af773affe9b824c6a862afcbadfb16295
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96258733"
---
# <a name="behavior-security"></a><span data-ttu-id="71fa5-102">行为安全</span><span class="sxs-lookup"><span data-stu-id="71fa5-102">Behavior Security</span></span>

<span data-ttu-id="71fa5-103">本节包含演示服务行为的配置安全的示例。</span><span class="sxs-lookup"><span data-stu-id="71fa5-103">This section includes samples that demonstrate configuring security for service behaviors.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="71fa5-104">本节内容</span><span class="sxs-lookup"><span data-stu-id="71fa5-104">In This Section</span></span>  

 [<span data-ttu-id="71fa5-105">服务审核行为</span><span class="sxs-lookup"><span data-stu-id="71fa5-105">Service Auditing Behavior</span></span>](service-auditing-behavior.md)  
 <span data-ttu-id="71fa5-106">此示例演示如何在服务操作过程中使用 <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> 来启用对安全事件的审核。</span><span class="sxs-lookup"><span data-stu-id="71fa5-106">This sample demonstrates how to use the <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> to enable auditing of security events during service operations.</span></span>  
  
 [<span data-ttu-id="71fa5-107">成员资格和角色提供程序</span><span class="sxs-lookup"><span data-stu-id="71fa5-107">Membership and Role Provider</span></span>](membership-and-role-provider.md)  
 <span data-ttu-id="71fa5-108">此示例演示服务如何使用 ASP.NET 成员资格和角色提供程序来对客户端进行身份验证和授权。</span><span class="sxs-lookup"><span data-stu-id="71fa5-108">This sample demonstrates how a service can use the ASP.NET membership and role providers to authenticate and authorize clients.</span></span>  
  
 [<span data-ttu-id="71fa5-109">授予对服务操作的访问权限</span><span class="sxs-lookup"><span data-stu-id="71fa5-109">Authorizing Access to Service Operations</span></span>](authorizing-access-to-service-operations.md)  
 <span data-ttu-id="71fa5-110">此示例演示如何使用 [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) 来允许使用 <xref:System.Security.Permissions.PrincipalPermissionAttribute> 属性来授予对服务操作的访问权限。</span><span class="sxs-lookup"><span data-stu-id="71fa5-110">This sample demonstrates how to use the [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) to enable use of the <xref:System.Security.Permissions.PrincipalPermissionAttribute> attribute to authorize access to service operations.</span></span>  
  
 [<span data-ttu-id="71fa5-111">模拟客户端</span><span class="sxs-lookup"><span data-stu-id="71fa5-111">Impersonating the Client</span></span>](impersonating-the-client.md)  
 <span data-ttu-id="71fa5-112">此示例演示如何在服务中模拟调用方应用程序，以便服务可以代表调用方访问系统资源。</span><span class="sxs-lookup"><span data-stu-id="71fa5-112">This sample demonstrates how to impersonate the caller application at the service so that the service can access system resources on behalf of the caller.</span></span>
