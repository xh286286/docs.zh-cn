---
title: 常用安全方案
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], scenarios
ms.assetid: 201923b5-5162-4a8a-8d4c-e7bd242748d5
ms.openlocfilehash: 21c8279890d1d1cf746e98f875efb6b1ff869c73
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96295075"
---
# <a name="common-security-scenarios"></a><span data-ttu-id="b5ce1-102">常用安全方案</span><span class="sxs-lookup"><span data-stu-id="b5ce1-102">Common Security Scenarios</span></span>

<span data-ttu-id="b5ce1-103">本节中的主题对众多可能的客户端和服务安全配置进行分类。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-103">The topics in this section catalog a number of possible client and service security configurations.</span></span> <span data-ttu-id="b5ce1-104">配置会随多种因素而变化。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-104">Configurations vary according to a number of factors.</span></span> <span data-ttu-id="b5ce1-105">例如，服务或客户端是否位于 Intranet 上，或者安全性是由 Windows 提供还是由传输（如 HTTPS）提供。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-105">For example, whether a service or client is on an intranet, or whether the security is provided by Windows or transport (such as HTTPS).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b5ce1-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="b5ce1-106">In This Section</span></span>  

 [<span data-ttu-id="b5ce1-107">不安全的 Internet 客户端和服务</span><span class="sxs-lookup"><span data-stu-id="b5ce1-107">Internet Unsecured Client and Service</span></span>](internet-unsecured-client-and-service.md)  
 <span data-ttu-id="b5ce1-108">一个公共的、不安全的客户端和服务的示例。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-108">An example of a public, unsecured client and service.</span></span>  
  
 [<span data-ttu-id="b5ce1-109">不安全的 Intranet 客户端和服务</span><span class="sxs-lookup"><span data-stu-id="b5ce1-109">Intranet Unsecured Client and Service</span></span>](intranet-unsecured-client-and-service.md)  
 <span data-ttu-id="b5ce1-110">基本 Windows Communication Foundation (WCF) 服务，旨在为 WCF 应用程序提供有关安全的专用网络的信息。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-110">A basic Windows Communication Foundation (WCF) service developed to provide information on a secure private network to a WCF application.</span></span>  
  
 [<span data-ttu-id="b5ce1-111">通过基本身份验证确保的传输安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-111">Transport Security with Basic Authentication</span></span>](transport-security-with-basic-authentication.md)  
 <span data-ttu-id="b5ce1-112">应用程序允许客户端使用自定义身份验证进行登录。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-112">The application allows clients to log on using custom authentication.</span></span>  
  
 [<span data-ttu-id="b5ce1-113">通过 Windows 身份验证确保的传输安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-113">Transport Security with Windows Authentication</span></span>](transport-security-with-windows-authentication.md)  
 <span data-ttu-id="b5ce1-114">显示由 Windows 安全保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-114">Shows a client and service secured by Windows security.</span></span>  
  
 [<span data-ttu-id="b5ce1-115">匿名客户端的传输安全性</span><span class="sxs-lookup"><span data-stu-id="b5ce1-115">Transport Security with an Anonymous Client</span></span>](transport-security-with-an-anonymous-client.md)  
 <span data-ttu-id="b5ce1-116">此方案使用传输安全（如 HTTPS）确保保密性和完整性。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-116">This scenario uses transport security (such as HTTPS) to ensure confidentiality and integrity.</span></span>  
  
 [<span data-ttu-id="b5ce1-117">利用证书身份验证的传输安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-117">Transport Security with Certificate Authentication</span></span>](transport-security-with-certificate-authentication.md)  
 <span data-ttu-id="b5ce1-118">显示由证书保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-118">Shows a client and service secured by a certificate.</span></span>  
  
 [<span data-ttu-id="b5ce1-119">匿名客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-119">Message Security with an Anonymous Client</span></span>](message-security-with-an-anonymous-client.md)  
 <span data-ttu-id="b5ce1-120">显示由 WCF 消息安全保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-120">Shows a client and service secured by WCF message security.</span></span>  
  
 [<span data-ttu-id="b5ce1-121">用户名客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-121">Message Security with a User Name Client</span></span>](message-security-with-a-user-name-client.md)  
 <span data-ttu-id="b5ce1-122">客户端是一个 Windows 窗体应用程序，允许客户端使用域用户名和密码登录。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-122">The client is a Windows Forms application that allows clients to log on using a domain user name and password.</span></span>  
  
 [<span data-ttu-id="b5ce1-123">使用证书客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-123">Message Security with a Certificate Client</span></span>](message-security-with-a-certificate-client.md)  
 <span data-ttu-id="b5ce1-124">服务器有多个证书，每个客户端各有一个证书。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-124">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="b5ce1-125">通过传输层安全 (TLS) 协商建立安全上下文。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-125">A security context is established through Transport Layer Security (TLS) negotiation.</span></span>  
  
 [<span data-ttu-id="b5ce1-126">Windows 客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-126">Message Security with a Windows Client</span></span>](message-security-with-a-windows-client.md)  
 <span data-ttu-id="b5ce1-127">证书客户端的变体。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-127">A variation of the certificate client.</span></span> <span data-ttu-id="b5ce1-128">服务器有多个证书，每个客户端各有一个证书。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-128">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="b5ce1-129">通过 TLS 协商建立安全上下文。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-129">A security context is established through TLS negotiation.</span></span>  
  
 [<span data-ttu-id="b5ce1-130">没有凭据协商的 Windows 客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-130">Message Security with a Windows Client without Credential Negotiation</span></span>](message-security-with-a-windows-client-without-credential-negotiation.md)  
 <span data-ttu-id="b5ce1-131">显示由 Kerberos 域保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-131">Shows a client and service secured by a Kerberos domain.</span></span>  
  
 [<span data-ttu-id="b5ce1-132">使用相互证书的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-132">Message Security with Mutual Certificates</span></span>](message-security-with-mutual-certificates.md)  
 <span data-ttu-id="b5ce1-133">服务器有多个证书，每个客户端各有一个证书。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-133">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="b5ce1-134">服务器证书随应用程序一起分发，而可在带外使用。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-134">The server certificate is distributed with the application and is available out of band.</span></span>  
  
 [<span data-ttu-id="b5ce1-135">使用已颁发令牌的消息安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-135">Message Security with Issued Tokens</span></span>](message-security-with-issued-tokens.md)  
 <span data-ttu-id="b5ce1-136">允许在独立域间建立信任的联合安全。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-136">Federated security that enables the establishment of trust between independent domains.</span></span>  
  
 [<span data-ttu-id="b5ce1-137">受信任的子系统</span><span class="sxs-lookup"><span data-stu-id="b5ce1-137">Trusted Subsystem</span></span>](trusted-subsystem.md)  
 <span data-ttu-id="b5ce1-138">客户端访问分布在网络上的一个或多个 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-138">A client accesses one or more Web services that are distributed across a network.</span></span> <span data-ttu-id="b5ce1-139">Web 服务访问必须加以保护的其他资源（如数据库或其他 Web 服务）。</span><span class="sxs-lookup"><span data-stu-id="b5ce1-139">The Web services access additional resources (such as databases or other Web services) that must be secured.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b5ce1-140">参考</span><span class="sxs-lookup"><span data-stu-id="b5ce1-140">Reference</span></span>  

 <xref:System.ServiceModel>  
  
## <a name="related-sections"></a><span data-ttu-id="b5ce1-141">相关章节</span><span class="sxs-lookup"><span data-stu-id="b5ce1-141">Related Sections</span></span>  

 [<span data-ttu-id="b5ce1-142">授权</span><span class="sxs-lookup"><span data-stu-id="b5ce1-142">Authorization</span></span>](authorization-in-wcf.md)  
  
 [<span data-ttu-id="b5ce1-143">安全性概述</span><span class="sxs-lookup"><span data-stu-id="b5ce1-143">Security Overview</span></span>](security-overview.md)  
  
 [<span data-ttu-id="b5ce1-144">安全性</span><span class="sxs-lookup"><span data-stu-id="b5ce1-144">Security</span></span>](security.md)  
  
 [<span data-ttu-id="b5ce1-145">绑定与安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-145">Bindings and Security</span></span>](bindings-and-security.md)  
  
 [<span data-ttu-id="b5ce1-146">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="b5ce1-146">Securing Services and Clients</span></span>](securing-services-and-clients.md)  
  
 [<span data-ttu-id="b5ce1-147">身份验证</span><span class="sxs-lookup"><span data-stu-id="b5ce1-147">Authentication</span></span>](authentication-in-wcf.md)  
  
 [<span data-ttu-id="b5ce1-148">授权</span><span class="sxs-lookup"><span data-stu-id="b5ce1-148">Authorization</span></span>](authorization-in-wcf.md)  
  
 [<span data-ttu-id="b5ce1-149">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="b5ce1-149">Federation and Issued Tokens</span></span>](federation-and-issued-tokens.md)  
  
 [<span data-ttu-id="b5ce1-150">审核</span><span class="sxs-lookup"><span data-stu-id="b5ce1-150">Auditing</span></span>](auditing-security-events.md)  
  
## <a name="see-also"></a><span data-ttu-id="b5ce1-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b5ce1-151">See also</span></span>

- [<span data-ttu-id="b5ce1-152">安全指导和最佳做法</span><span class="sxs-lookup"><span data-stu-id="b5ce1-152">Security Guidance and Best Practices</span></span>](security-guidance-and-best-practices.md)
- <span data-ttu-id="b5ce1-153">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="b5ce1-153">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
