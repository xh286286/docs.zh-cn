---
title: 扩展安全性
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], extending
ms.assetid: a015a040-9fdf-4147-9ea9-f83b570be1d4
ms.openlocfilehash: d91f4812dbccb7807be2e0780cccd1d0c38b1f40
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96273056"
---
# <a name="extending-security"></a><span data-ttu-id="fed42-102">扩展安全性</span><span class="sxs-lookup"><span data-stu-id="fed42-102">Extending Security</span></span>

<span data-ttu-id="fed42-103">为了容纳新的声明类型和自定义令牌，你可以将 Windows Communication Foundation (WCF) 的安全基础结构扩展。</span><span class="sxs-lookup"><span data-stu-id="fed42-103">To accommodate new claim types and custom tokens, you can extend the security infrastructure of Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="fed42-104">本节中的主题将向您介绍如何完成此任务。</span><span class="sxs-lookup"><span data-stu-id="fed42-104">The topics in this section show you how this is done.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="fed42-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="fed42-105">In This Section</span></span>  
  
 [<span data-ttu-id="fed42-106">自定义凭据和凭据验证</span><span class="sxs-lookup"><span data-stu-id="fed42-106">Custom Credential and Credential Validation</span></span>](custom-credential-and-credential-validation.md)  
 <span data-ttu-id="fed42-107">说明在验证自定义凭据时如何使用标识模型。</span><span class="sxs-lookup"><span data-stu-id="fed42-107">Explains how the Identity Model is used when validating custom credentials.</span></span>  
  
 [<span data-ttu-id="fed42-108">自定义令牌</span><span class="sxs-lookup"><span data-stu-id="fed42-108">Custom Tokens</span></span>](custom-tokens.md)  
 <span data-ttu-id="fed42-109">安全令牌服务 (STS) 颁发的令牌通常为 SAML 令牌。</span><span class="sxs-lookup"><span data-stu-id="fed42-109">Issued tokens from a Security Token Service (STS) are typically SAML tokens.</span></span> <span data-ttu-id="fed42-110">本主题说明如何创建自定义令牌类型。</span><span class="sxs-lookup"><span data-stu-id="fed42-110">This topic explains how to create a custom token type.</span></span>  
  
 [<span data-ttu-id="fed42-111">自定义授权</span><span class="sxs-lookup"><span data-stu-id="fed42-111">Custom Authorization</span></span>](custom-authorization.md)  
 <span data-ttu-id="fed42-112">说明如何实现自定义授权。</span><span class="sxs-lookup"><span data-stu-id="fed42-112">Explains how to implement custom authorization.</span></span>  
  
 [<span data-ttu-id="fed42-113">重写服务标识以便进行身份验证</span><span class="sxs-lookup"><span data-stu-id="fed42-113">Overriding the Identity of a Service for Authentication</span></span>](overriding-the-identity-of-a-service-for-authentication.md)  
 <span data-ttu-id="fed42-114">介绍如何重写身份验证服务的标识。</span><span class="sxs-lookup"><span data-stu-id="fed42-114">Describes how to override the identity of a service for authentication.</span></span>  
  
 [<span data-ttu-id="fed42-115">如何：创建自定义客户端标识验证工具</span><span class="sxs-lookup"><span data-stu-id="fed42-115">How to: Create a Custom Client Identity Verifier</span></span>](how-to-create-a-custom-client-identity-verifier.md)  
 <span data-ttu-id="fed42-116">演示如何验证自定义终结点标识。</span><span class="sxs-lookup"><span data-stu-id="fed42-116">Demonstrates how to validate a custom endpoint identity.</span></span>  
  
 [<span data-ttu-id="fed42-117">如何：使用独立的 X.509 证书进行签名和加密</span><span class="sxs-lookup"><span data-stu-id="fed42-117">How to: Use Separate X.509 Certificates for Signing and Encryption</span></span>](how-to-use-separate-x-509-certificates-for-signing-and-encryption.md)  
 <span data-ttu-id="fed42-118">通常使用单个证书对消息进行签名和加密。</span><span class="sxs-lookup"><span data-stu-id="fed42-118">Messages are typically signed and encrypted with a single certificate.</span></span> <span data-ttu-id="fed42-119">本主题说明如何按照要求使用两个证书。</span><span class="sxs-lookup"><span data-stu-id="fed42-119">This topic explains how two certificates can be used, when required.</span></span>  
  
 [<span data-ttu-id="fed42-120">如何：更改 X.509 证书私钥的加密提供程序</span><span class="sxs-lookup"><span data-stu-id="fed42-120">How to: Change the Cryptographic Provider for an X.509 Certificate's Private Key</span></span>](change-cryptographic-provider-x509-certificate-private-key.md)  
 <span data-ttu-id="fed42-121">说明如何更改用于提供 x.509 证书的私钥的加密提供程序，以及如何将该提供程序集成到 Windows Communication Foundation (WCF) 框架中。</span><span class="sxs-lookup"><span data-stu-id="fed42-121">Explains how to change the cryptographic provider used to provide an X.509 certificate's private key and how to integrate the provider into the Windows Communication Foundation (WCF) framework.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="fed42-122">参考</span><span class="sxs-lookup"><span data-stu-id="fed42-122">Reference</span></span>  

 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.IdentityModel.Policy>  
  
 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Selectors>  
  
## <a name="related-sections"></a><span data-ttu-id="fed42-123">相关章节</span><span class="sxs-lookup"><span data-stu-id="fed42-123">Related Sections</span></span>  

 [<span data-ttu-id="fed42-124">安全性</span><span class="sxs-lookup"><span data-stu-id="fed42-124">Security</span></span>](../feature-details/security.md)  
  
 [<span data-ttu-id="fed42-125">基本 WCF 编程</span><span class="sxs-lookup"><span data-stu-id="fed42-125">Basic WCF Programming</span></span>](../basic-wcf-programming.md)  
  
## <a name="see-also"></a><span data-ttu-id="fed42-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fed42-126">See also</span></span>

- [<span data-ttu-id="fed42-127">安全性概述</span><span class="sxs-lookup"><span data-stu-id="fed42-127">Security Overview</span></span>](../feature-details/security-overview.md)
