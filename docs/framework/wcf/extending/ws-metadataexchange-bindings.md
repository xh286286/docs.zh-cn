---
title: WS-MetadataExchange 绑定
ms.date: 03/30/2017
ms.assetid: 10f8de5d-b81d-4ea7-b37e-7f2c00c39714
ms.openlocfilehash: 94f0ba602cd1f58f5491a44a64e24be8ea52895b
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96293983"
---
# <a name="ws-metadataexchange-bindings"></a><span data-ttu-id="2b7ec-102">WS-MetadataExchange 绑定</span><span class="sxs-lookup"><span data-stu-id="2b7ec-102">WS-MetadataExchange Bindings</span></span>

<span data-ttu-id="2b7ec-103">本主题说明如何为各种传输构造默认的元数据交换绑定。</span><span class="sxs-lookup"><span data-stu-id="2b7ec-103">This topic describes how the default metadata exchange bindings are constructed for various transports.</span></span>  
  
## <a name="the-default-bindings"></a><span data-ttu-id="2b7ec-104">默认绑定</span><span class="sxs-lookup"><span data-stu-id="2b7ec-104">The Default Bindings</span></span>  
  
|<span data-ttu-id="2b7ec-105">默认绑定名称</span><span class="sxs-lookup"><span data-stu-id="2b7ec-105">Default Binding Name</span></span>|<span data-ttu-id="2b7ec-106">绑定的构造方式</span><span class="sxs-lookup"><span data-stu-id="2b7ec-106">How the binding is constructed</span></span>|  
|--------------------------|------------------------------------|  
|<span data-ttu-id="2b7ec-107">mexHttpBinding</span><span class="sxs-lookup"><span data-stu-id="2b7ec-107">mexHttpBinding</span></span>|<span data-ttu-id="2b7ec-108">一个禁用传输级安全性的 <xref:System.ServiceModel.WSHttpBinding>。</span><span class="sxs-lookup"><span data-stu-id="2b7ec-108">A <xref:System.ServiceModel.WSHttpBinding> with transport-level security disabled.</span></span>|  
|<span data-ttu-id="2b7ec-109">mexHttpsBinding</span><span class="sxs-lookup"><span data-stu-id="2b7ec-109">mexHttpsBinding</span></span>|<span data-ttu-id="2b7ec-110">一个支持传输级安全性的 <xref:System.ServiceModel.WSHttpBinding>。</span><span class="sxs-lookup"><span data-stu-id="2b7ec-110">A <xref:System.ServiceModel.WSHttpBinding> that supports transport-level security.</span></span>|  
|<span data-ttu-id="2b7ec-111">mexNamedPipeBinding</span><span class="sxs-lookup"><span data-stu-id="2b7ec-111">mexNamedPipeBinding</span></span>|<span data-ttu-id="2b7ec-112">一个 <xref:System.ServiceModel.Channels.CustomBinding>，它具有使用默认值的 <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>。</span><span class="sxs-lookup"><span data-stu-id="2b7ec-112">A  <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement> using the default values.</span></span>|  
|<span data-ttu-id="2b7ec-113">mexTcpBinding</span><span class="sxs-lookup"><span data-stu-id="2b7ec-113">mexTcpBinding</span></span>|<span data-ttu-id="2b7ec-114">一个 <xref:System.ServiceModel.Channels.CustomBinding>，它具有使用默认值的 <xref:System.ServiceModel.Channels.TcpTransportBindingElement>。</span><span class="sxs-lookup"><span data-stu-id="2b7ec-114">A <xref:System.ServiceModel.Channels.CustomBinding> with a <xref:System.ServiceModel.Channels.TcpTransportBindingElement> using default values.</span></span>|
