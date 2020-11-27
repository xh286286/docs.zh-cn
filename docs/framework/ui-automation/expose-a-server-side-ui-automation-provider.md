---
title: 公开服务器端 UI 自动化提供程序
description: 查看一个示例，该示例演示如何公开承载于 System.web 窗体窗口中的服务器端 UI 自动化提供程序。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- expose a server-side UI Automation provider
- UI Automation, server-side provider, exposing
- server-side UI Automation provider, exposing
ms.assetid: 55d419c0-2201-4101-90c9-2888df4dbb47
ms.openlocfilehash: be39130c7a91fc081256bf14a87f503d27f45129
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96276524"
---
# <a name="expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="005e9-103">公开服务器端 UI 自动化提供程序</span><span class="sxs-lookup"><span data-stu-id="005e9-103">Expose a Server-side UI Automation Provider</span></span>

> [!NOTE]
> <span data-ttu-id="005e9-104">本文档适用于想要使用 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 命名空间中定义的托管 <xref:System.Windows.Automation> 类的 .NET Framework 开发人员。</span><span class="sxs-lookup"><span data-stu-id="005e9-104">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="005e9-105">有关 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]的最新信息，请参阅 [Windows 自动化 API：UI 自动化](/windows/win32/winauto/entry-uiauto-win32)。</span><span class="sxs-lookup"><span data-stu-id="005e9-105">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](/windows/win32/winauto/entry-uiauto-win32).</span></span>  
  
 <span data-ttu-id="005e9-106">本主题包含演示如何公开承载在 <xref:System.Windows.Forms.Control?displayProperty=nameWithType> 窗口中服务器端 UI 自动化提供程序的代码示例。</span><span class="sxs-lookup"><span data-stu-id="005e9-106">This topic contains example code that shows how to expose a server-side UI Automation provider that is hosted in a <xref:System.Windows.Forms.Control?displayProperty=nameWithType> window.</span></span>  
  
 <span data-ttu-id="005e9-107">示例重写窗口过程以捕获 WM_GETOBJECT，这是客户端应用程序请求有关窗口的信息时， [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 核心服务发送的消息。</span><span class="sxs-lookup"><span data-stu-id="005e9-107">The example overrides the window procedure to trap WM_GETOBJECT, which is the message sent by the [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] core service when a client application requests information about the window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="005e9-108">示例</span><span class="sxs-lookup"><span data-stu-id="005e9-108">Example</span></span>  

 [!code-csharp[UIAFragmentProvider_snip#116](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAFragmentProvider_snip/CSharp/ListFragment.cs#116)]
 [!code-vb[UIAFragmentProvider_snip#116](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAFragmentProvider_snip/VisualBasic/ListFragment.vb#116)]  
  
## <a name="see-also"></a><span data-ttu-id="005e9-109">另请参阅</span><span class="sxs-lookup"><span data-stu-id="005e9-109">See also</span></span>

- [<span data-ttu-id="005e9-110">UI 自动化提供程序概述</span><span class="sxs-lookup"><span data-stu-id="005e9-110">UI Automation Providers Overview</span></span>](ui-automation-providers-overview.md)
- [<span data-ttu-id="005e9-111">服务器端 UI 自动化提供程序的实现</span><span class="sxs-lookup"><span data-stu-id="005e9-111">Server-Side UI Automation Provider Implementation</span></span>](server-side-ui-automation-provider-implementation.md)
