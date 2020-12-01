---
title: 如何：创建应用程序域
description: 了解如何在 .NET 中创建应用程序域。 可以创建应用程序域来加载亲自管理的程序集，也可以创建应用程序域来执行代码。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- application domains, creating
ms.assetid: ba1fa43e-49f5-47d9-bd7f-3024af16f4ba
ms.openlocfilehash: fb022511ee395a9312e4dbaf7c0beee03c9b4569
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96264083"
---
# <a name="how-to-create-an-application-domain"></a><span data-ttu-id="38594-104">如何：创建应用程序域</span><span class="sxs-lookup"><span data-stu-id="38594-104">How to: Create an Application Domain</span></span>

<span data-ttu-id="38594-105">需要应用程序域时，公共语言运行时主机会自动创建它们。</span><span class="sxs-lookup"><span data-stu-id="38594-105">A common language runtime host creates application domains automatically when they are needed.</span></span> <span data-ttu-id="38594-106">但是，可以创建自己的应用程序域并将其加载到需要亲自管理的程序集中。</span><span class="sxs-lookup"><span data-stu-id="38594-106">However, you can create your own application domains and load into them those assemblies that you want to manage personally.</span></span> <span data-ttu-id="38594-107">也可以创建从中执行代码的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="38594-107">You can also create application domains from which you execute code.</span></span>  
  
 <span data-ttu-id="38594-108">使用 <xref:System.AppDomain?displayProperty=nameWithType> 类中某个重载的 CreateDomain 方法，创建新的应用程序域。</span><span class="sxs-lookup"><span data-stu-id="38594-108">You create a new application domain using one of the overloaded **CreateDomain** methods in the <xref:System.AppDomain?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="38594-109">可以为应用程序域命名并按名称来引用应用程序域。</span><span class="sxs-lookup"><span data-stu-id="38594-109">You can give the application domain a name and reference it by that name.</span></span>  
  
 <span data-ttu-id="38594-110">以下示例创建新的应用程序域，并为它指定名称 `MyDomain`，然后将主机域和新创建的子应用程序域的名称打印到控制台。</span><span class="sxs-lookup"><span data-stu-id="38594-110">The following example creates a new application domain, assigns it the name `MyDomain`, and then prints the name of the host domain and the newly created child application domain to the console.</span></span>  
  
## <a name="example"></a><span data-ttu-id="38594-111">示例</span><span class="sxs-lookup"><span data-stu-id="38594-111">Example</span></span>  

 [!code-cpp[ADCreateDomain#2](../../../samples/snippets/cpp/VS_Snippets_CLR/ADCreateDomain/CPP/source2.cpp#2)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="38594-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="38594-112">See also</span></span>

- [<span data-ttu-id="38594-113">对应用程序域进行编程</span><span class="sxs-lookup"><span data-stu-id="38594-113">Programming with Application Domains</span></span>](application-domains.md#programming-with-application-domains)
- [<span data-ttu-id="38594-114">使用应用程序域</span><span class="sxs-lookup"><span data-stu-id="38594-114">Using Application Domains</span></span>](use.md)
