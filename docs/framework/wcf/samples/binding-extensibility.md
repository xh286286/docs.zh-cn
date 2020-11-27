---
title: 绑定扩展性
ms.date: 03/30/2017
ms.assetid: cabdd583-ddf5-493e-9dba-c6c31cde8f65
ms.openlocfilehash: c99713416181aed8a8800c819e0f5786411187ab
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96283596"
---
# <a name="binding-extensibility"></a><span data-ttu-id="f078f-102">绑定扩展性</span><span class="sxs-lookup"><span data-stu-id="f078f-102">Binding Extensibility</span></span>

<span data-ttu-id="f078f-103">本节包含演示 Windows Communication Foundation (WCF) 中的自定义绑定的示例。</span><span class="sxs-lookup"><span data-stu-id="f078f-103">This section contains samples that demonstrate custom binding in Windows Communication Foundation (WCF).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f078f-104">本节内容</span><span class="sxs-lookup"><span data-stu-id="f078f-104">In This Section</span></span>  

 <xref:System.ServiceModel.NetHttpBinding>  
 <span data-ttu-id="f078f-105">演示如何实现在 <xref:System.ServiceModel.Channels.HttpTransportBindingElement> 之上堆积 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement> 或 <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement> 的绑定。</span><span class="sxs-lookup"><span data-stu-id="f078f-105">Demonstrates how to implement a binding that stacks <xref:System.ServiceModel.Channels.HttpTransportBindingElement> or the <xref:System.ServiceModel.Channels.HttpsTransportBindingElement> on top of the <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>.</span></span>  
  
 [<span data-ttu-id="f078f-106">WSStreamedHttpBinding</span><span class="sxs-lookup"><span data-stu-id="f078f-106">WSStreamedHttpBinding</span></span>](wsstreamedhttpbinding.md)  
 <span data-ttu-id="f078f-107">演示如何创建一个绑定，该绑定用于在使用 HTTP 传输时支持件流式传送方案。</span><span class="sxs-lookup"><span data-stu-id="f078f-107">Demonstrates how to create a binding that is designed to support streaming scenarios when the HTTP transport is used.</span></span>  
