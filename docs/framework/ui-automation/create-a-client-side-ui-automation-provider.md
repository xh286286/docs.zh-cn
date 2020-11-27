---
title: 创建客户端 UI 自动化提供程序
description: 查看有关如何创建客户端 UI 自动化提供程序的示例。 该示例为控制台窗口实现了一个简单的客户端提供程序。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- UI Automation, creating client-side provider
- client-side UI Automation provider, creating
ms.assetid: d91edaf2-be28-41ec-a508-af421cb43c3d
ms.openlocfilehash: 17a6deca2efc67d1409e89f7accf7a3b89a27807
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96276537"
---
# <a name="create-a-client-side-ui-automation-provider"></a><span data-ttu-id="8488f-104">创建客户端 UI 自动化提供程序</span><span class="sxs-lookup"><span data-stu-id="8488f-104">Create a Client-Side UI Automation Provider</span></span>

> [!NOTE]
> <span data-ttu-id="8488f-105">本文档适用于想要使用 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 命名空间中定义的托管 <xref:System.Windows.Automation> 类的 .NET Framework 开发人员。</span><span class="sxs-lookup"><span data-stu-id="8488f-105">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="8488f-106">有关 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]的最新信息，请参阅 [Windows 自动化 API：UI 自动化](/windows/win32/winauto/entry-uiauto-win32)。</span><span class="sxs-lookup"><span data-stu-id="8488f-106">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](/windows/win32/winauto/entry-uiauto-win32).</span></span>  
  
 <span data-ttu-id="8488f-107">本主题所包含的代码示例演示如何实现客户端 UI 自动化提供程序。</span><span class="sxs-lookup"><span data-stu-id="8488f-107">This topic contains example code that shows how to implement a client-side UI Automation provider.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8488f-108">示例</span><span class="sxs-lookup"><span data-stu-id="8488f-108">Example</span></span>  

 <span data-ttu-id="8488f-109">下面的示例代码可内置于动态链接库 (DLL) ，该动态链接库为控制台窗口实现非常简单的客户端提供程序。</span><span class="sxs-lookup"><span data-stu-id="8488f-109">The following example code can be built into a dynamic-link library (DLL) that implements a very simple client-side provider for a console window.</span></span> <span data-ttu-id="8488f-110">此代码不具有任何有用的功能，只是用于演示设置提供程序程序集的基本步骤，该程序集可由 UI 自动化客户端应用程序进行注册。</span><span class="sxs-lookup"><span data-stu-id="8488f-110">The code does not have any useful functionality, but is intended to demonstrate the basic steps in setting up a provider assembly that can be registered by a UI Automation client application.</span></span>  
  
 [!code-csharp[UIAClientSideProvider_snip#101](../../../samples/snippets/csharp/VS_Snippets_Wpf/UIAClientSideProvider_snip/CSharp/CSProviderProgram.cs#101)]
 [!code-vb[UIAClientSideProvider_snip#101](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/UIAClientSideProvider_snip/visualbasic/csproviderprogram.vb#101)]  
  
## <a name="see-also"></a><span data-ttu-id="8488f-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8488f-111">See also</span></span>

- [<span data-ttu-id="8488f-112">UI 自动化提供程序概述</span><span class="sxs-lookup"><span data-stu-id="8488f-112">UI Automation Providers Overview</span></span>](ui-automation-providers-overview.md)
- [<span data-ttu-id="8488f-113">注册客户端提供程序程序集</span><span class="sxs-lookup"><span data-stu-id="8488f-113">Register a Client-Side Provider Assembly</span></span>](register-a-client-side-provider-assembly.md)
