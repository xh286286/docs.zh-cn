---
title: 安全协商和超时
ms.date: 03/30/2017
ms.assetid: 02a428f1-84e5-4d28-a11f-53ce31d63196
ms.openlocfilehash: 4ccc7e5539b1a772be6f9edb5a4cb4d94a8d1c1b
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96275978"
---
# <a name="security-negotiation-and-timeouts"></a><span data-ttu-id="dbc75-102">安全协商和超时</span><span class="sxs-lookup"><span data-stu-id="dbc75-102">Security Negotiation and Timeouts</span></span>

<span data-ttu-id="dbc75-103">当客户端和服务进行身份验证时，Windows Communication Foundation (WCF) 支持在身份验证过程中协商服务凭据的模式。</span><span class="sxs-lookup"><span data-stu-id="dbc75-103">When clients and services authenticate, Windows Communication Foundation (WCF) supports a mode where the service credential is negotiated as part of authentication.</span></span> <span data-ttu-id="dbc75-104">在这种情况下，客户端和服务之间将进行潜在多路交换，以便将服务凭据传播到客户端。</span><span class="sxs-lookup"><span data-stu-id="dbc75-104">In such scenarios, a potentially multi-leg exchange occurs between the client and the service to propagate the service credential to the client.</span></span> <span data-ttu-id="dbc75-105"><xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> 属性控制多路交换需要多长时间才能完成。</span><span class="sxs-lookup"><span data-stu-id="dbc75-105">The <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings.NegotiationTimeout%2A> property controls how long the multi-leg exchange can take to complete.</span></span> <span data-ttu-id="dbc75-106">但此超时仅在交换实际经过的时间超过单个请求响应的时间时才适用。</span><span class="sxs-lookup"><span data-stu-id="dbc75-106">However, this timeout only applies if the exchange actually takes more that a single request-response.</span></span> <span data-ttu-id="dbc75-107">如果协商在一次往返中完成，则该超时不适用。</span><span class="sxs-lookup"><span data-stu-id="dbc75-107">In cases where the negotiation completes in a single round trip, the timeout does not apply.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbc75-108">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbc75-108">See also</span></span>

- <xref:System.ServiceModel.Channels.LocalServiceSecuritySettings>
- [<span data-ttu-id="dbc75-109">如何：设置最大时钟偏差</span><span class="sxs-lookup"><span data-stu-id="dbc75-109">How to: Set a Max Clock Skew</span></span>](how-to-set-a-max-clock-skew.md)
