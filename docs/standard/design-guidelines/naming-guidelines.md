---
title: 命名准则
description: 在此概述中，请阅读有关在框架开发中使用的命名约定。 请参阅介绍大小写、常规命名和其他准则的文章。
ms.date: 10/22/2008
helpviewer_keywords:
- names [.NET Framework], about naming guidelines
- naming guidelines [.NET Framework]
- class library design guidelines [.NET Framework], names
- formatting [.NET Framework], names
- identifiers, class library element names
- names [.NET Framework]
- format naming guidelines [.NET Framework]
ms.assetid: fc076d66-9b5f-42d3-aa65-61d970c794a3
ms.openlocfilehash: e82b6941d3ea0243f4ae16bc9d42ea8d1f1fccfb
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94820873"
---
# <a name="naming-guidelines"></a><span data-ttu-id="654a2-104">命名准则</span><span class="sxs-lookup"><span data-stu-id="654a2-104">Naming Guidelines</span></span>
<span data-ttu-id="654a2-105">在框架开发中采用一致的命名约定集可能是框架可用性的主要贡献。</span><span class="sxs-lookup"><span data-stu-id="654a2-105">Following a consistent set of naming conventions in the development of a framework can be a major contribution to the framework’s usability.</span></span> <span data-ttu-id="654a2-106">它允许很多开发人员对广泛分隔的项目使用框架。</span><span class="sxs-lookup"><span data-stu-id="654a2-106">It allows the framework to be used by many developers on widely separated projects.</span></span> <span data-ttu-id="654a2-107">除了表单的一致性以外，框架元素的名称也必须易于理解，并且必须传达每个元素的功能。</span><span class="sxs-lookup"><span data-stu-id="654a2-107">Beyond consistency of form, names of framework elements must be easily understood and must convey the function of each element.</span></span>  
  
 <span data-ttu-id="654a2-108">本章的目的是提供一组一致的命名约定，以使开发人员能够立即了解名称。</span><span class="sxs-lookup"><span data-stu-id="654a2-108">The goal of this chapter is to provide a consistent set of naming conventions that results in names that make immediate sense to developers.</span></span>  
  
 <span data-ttu-id="654a2-109">尽管采用这些命名约定作为一般代码开发准则会使代码的命名更加一致，但你只需将它们应用到公开 (公共或受保护类型和成员的 Api，并) 显式实现的接口。</span><span class="sxs-lookup"><span data-stu-id="654a2-109">Although adopting these naming conventions as general code development guidelines would result in more consistent naming throughout your code, you are required only to apply them to APIs that are publicly exposed (public or protected types and members, and explicitly implemented interfaces).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="654a2-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="654a2-110">In This Section</span></span>  
 [<span data-ttu-id="654a2-111">大小写约定</span><span class="sxs-lookup"><span data-stu-id="654a2-111">Capitalization Conventions</span></span>](capitalization-conventions.md)  
 [<span data-ttu-id="654a2-112">通用命名约定</span><span class="sxs-lookup"><span data-stu-id="654a2-112">General Naming Conventions</span></span>](general-naming-conventions.md)  
 [<span data-ttu-id="654a2-113">程序集和 Dll 的名称</span><span class="sxs-lookup"><span data-stu-id="654a2-113">Names of Assemblies and DLLs</span></span>](names-of-assemblies-and-dlls.md)  
 [<span data-ttu-id="654a2-114">命名空间的名称</span><span class="sxs-lookup"><span data-stu-id="654a2-114">Names of Namespaces</span></span>](names-of-namespaces.md)  
 [<span data-ttu-id="654a2-115">类、结构和接口的名称</span><span class="sxs-lookup"><span data-stu-id="654a2-115">Names of Classes, Structs, and Interfaces</span></span>](names-of-classes-structs-and-interfaces.md)  
 [<span data-ttu-id="654a2-116">类型成员的名称</span><span class="sxs-lookup"><span data-stu-id="654a2-116">Names of Type Members</span></span>](names-of-type-members.md)  
 [<span data-ttu-id="654a2-117">命名参数</span><span class="sxs-lookup"><span data-stu-id="654a2-117">Naming Parameters</span></span>](naming-parameters.md)  
 [<span data-ttu-id="654a2-118">命名资源</span><span class="sxs-lookup"><span data-stu-id="654a2-118">Naming Resources</span></span>](naming-resources.md)  
 <span data-ttu-id="654a2-119">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="654a2-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="654a2-120">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="654a2-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="654a2-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="654a2-121">See also</span></span>

- [<span data-ttu-id="654a2-122">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="654a2-122">Framework Design Guidelines</span></span>](index.md)
