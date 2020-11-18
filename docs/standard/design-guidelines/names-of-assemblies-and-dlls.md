---
title: 程序集和 DLL 的名称
description: 了解 (Dll) 命名程序集和动态链接库的准则。 程序集可跨一个或多个文件，但它通常与 DLL 相互映射。
ms.date: 10/22/2008
helpviewer_keywords:
- names [.NET Framework], DLLs
- names [.NET Framework], assemblies
- assemblies [.NET Framework], names
- DLLs, names
ms.assetid: e800b610-31b4-4949-9c14-cb60e9f254be
ms.openlocfilehash: 2d1484889eb7db537de970c31109f26a6d61ad8d
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94830046"
---
# <a name="names-of-assemblies-and-dlls"></a><span data-ttu-id="87fa3-104">程序集和 DLL 的名称</span><span class="sxs-lookup"><span data-stu-id="87fa3-104">Names of Assemblies and DLLs</span></span>
<span data-ttu-id="87fa3-105">程序集是托管代码程序的部署和标识单元。</span><span class="sxs-lookup"><span data-stu-id="87fa3-105">An assembly is the unit of deployment and identity for managed code programs.</span></span> <span data-ttu-id="87fa3-106">尽管程序集可跨一个或多个文件，但通常程序集与 DLL 相互映射。</span><span class="sxs-lookup"><span data-stu-id="87fa3-106">Although assemblies can span one or more files, typically an assembly maps one-to-one with a DLL.</span></span> <span data-ttu-id="87fa3-107">因此，本节仅介绍 DLL 命名约定，然后可以将其映射到程序集命名约定。</span><span class="sxs-lookup"><span data-stu-id="87fa3-107">Therefore, this section describes only DLL naming conventions, which then can be mapped to assembly naming conventions.</span></span>

 <span data-ttu-id="87fa3-108">✔️为程序集 Dll 选择名称，这些名称建议了大块功能，如 System.object。</span><span class="sxs-lookup"><span data-stu-id="87fa3-108">✔️ DO choose names for your assembly DLLs that suggest large chunks of functionality, such as System.Data.</span></span>

 <span data-ttu-id="87fa3-109">程序集和 DLL 的名称不必与命名空间名称对应，但在命名程序集时遵循命名空间名称是合理的。</span><span class="sxs-lookup"><span data-stu-id="87fa3-109">Assembly and DLL names don’t have to correspond to namespace names, but it is reasonable to follow the namespace name when naming assemblies.</span></span> <span data-ttu-id="87fa3-110">合理的经验法则是基于程序集中包含的命名空间的公共前缀来命名 DLL。</span><span class="sxs-lookup"><span data-stu-id="87fa3-110">A good rule of thumb is to name the DLL based on the common prefix of the namespaces contained in the assembly.</span></span> <span data-ttu-id="87fa3-111">例如，可以调用具有两个命名空间和的程序集 `MyCompany.MyTechnology.FirstFeature` `MyCompany.MyTechnology.SecondFeature` `MyCompany.MyTechnology.dll` 。</span><span class="sxs-lookup"><span data-stu-id="87fa3-111">For example, an assembly with two namespaces, `MyCompany.MyTechnology.FirstFeature` and `MyCompany.MyTechnology.SecondFeature`, could be called `MyCompany.MyTechnology.dll`.</span></span>

 <span data-ttu-id="87fa3-112">✔️考虑根据以下模式命名 Dll：</span><span class="sxs-lookup"><span data-stu-id="87fa3-112">✔️ CONSIDER naming DLLs according to the following pattern:</span></span>

 `<Company>.<Component>.dll`

 <span data-ttu-id="87fa3-113">其中 `<Component>` 包含一个或多个以句点分隔的子句。</span><span class="sxs-lookup"><span data-stu-id="87fa3-113">where `<Component>` contains one or more dot-separated clauses.</span></span> <span data-ttu-id="87fa3-114">例如：</span><span class="sxs-lookup"><span data-stu-id="87fa3-114">For example:</span></span>

 <span data-ttu-id="87fa3-115">`Litware.Controls.dll`.</span><span class="sxs-lookup"><span data-stu-id="87fa3-115">`Litware.Controls.dll`.</span></span>

 <span data-ttu-id="87fa3-116">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="87fa3-116">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="87fa3-117">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="87fa3-117">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="87fa3-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="87fa3-118">See also</span></span>

- [<span data-ttu-id="87fa3-119">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="87fa3-119">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="87fa3-120">命名准则</span><span class="sxs-lookup"><span data-stu-id="87fa3-120">Naming Guidelines</span></span>](naming-guidelines.md)
