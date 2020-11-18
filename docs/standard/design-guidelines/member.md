---
title: 成员设计准则
description: 了解 .NET 中的成员设计准则。 成员包含方法、属性、事件、构造函数和字段。
ms.date: 10/22/2008
helpviewer_keywords:
- member design guidelines [.NET Framework], about member design guidelines
- members [.NET Framework], design guidelines
- class library design guidelines [.NET Framework], members
- member design guidelines [.NET Framework]
ms.assetid: 0ce93180-1d7b-4f8c-9306-f828b2d66b8f
ms.openlocfilehash: 512fc3b7fde93279995a67be2fc0b285ba235f16
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94820938"
---
# <a name="member-design-guidelines"></a><span data-ttu-id="3f2c6-104">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="3f2c6-104">Member Design Guidelines</span></span>
<span data-ttu-id="3f2c6-105">方法、属性、事件、构造函数和字段统称为成员。</span><span class="sxs-lookup"><span data-stu-id="3f2c6-105">Methods, properties, events, constructors, and fields are collectively referred to as members.</span></span> <span data-ttu-id="3f2c6-106">成员最终是指向框架的最终用户公开框架功能的方式。</span><span class="sxs-lookup"><span data-stu-id="3f2c6-106">Members are ultimately the means by which framework functionality is exposed to the end users of a framework.</span></span>  
  
 <span data-ttu-id="3f2c6-107">成员可以为虚拟或非虚拟、具体或抽象、静态或实例，并可具有多个不同的可访问性范围。</span><span class="sxs-lookup"><span data-stu-id="3f2c6-107">Members can be virtual or nonvirtual, concrete or abstract, static or instance, and can have several different scopes of accessibility.</span></span> <span data-ttu-id="3f2c6-108">所有这些组件都提供令人难以置信的表现力，但同时需要注意框架设计器的一部分。</span><span class="sxs-lookup"><span data-stu-id="3f2c6-108">All this variety provides incredible expressiveness but at the same time requires care on the part of the framework designer.</span></span>  
  
 <span data-ttu-id="3f2c6-109">本章提供设计任何类型的成员时应遵循的基本准则。</span><span class="sxs-lookup"><span data-stu-id="3f2c6-109">This chapter offers basic guidelines that should be followed when designing members of any type.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3f2c6-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="3f2c6-110">In This Section</span></span>  
 [<span data-ttu-id="3f2c6-111">成员重载</span><span class="sxs-lookup"><span data-stu-id="3f2c6-111">Member Overloading</span></span>](member-overloading.md)  
 [<span data-ttu-id="3f2c6-112">属性设计</span><span class="sxs-lookup"><span data-stu-id="3f2c6-112">Property Design</span></span>](property.md)  
 [<span data-ttu-id="3f2c6-113">构造函数设计</span><span class="sxs-lookup"><span data-stu-id="3f2c6-113">Constructor Design</span></span>](constructor.md)  
 [<span data-ttu-id="3f2c6-114">事件设计</span><span class="sxs-lookup"><span data-stu-id="3f2c6-114">Event Design</span></span>](event.md)  
 [<span data-ttu-id="3f2c6-115">现场设计</span><span class="sxs-lookup"><span data-stu-id="3f2c6-115">Field Design</span></span>](field.md)  
 [<span data-ttu-id="3f2c6-116">扩展方法</span><span class="sxs-lookup"><span data-stu-id="3f2c6-116">Extension Methods</span></span>](extension-methods.md)  
 [<span data-ttu-id="3f2c6-117">运算符重载</span><span class="sxs-lookup"><span data-stu-id="3f2c6-117">Operator Overloads</span></span>](operator-overloads.md)  
 [<span data-ttu-id="3f2c6-118">参数设计</span><span class="sxs-lookup"><span data-stu-id="3f2c6-118">Parameter Design</span></span>](parameter-design.md)  
 <span data-ttu-id="3f2c6-119">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="3f2c6-119">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>  
  
 <span data-ttu-id="3f2c6-120">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="3f2c6-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f2c6-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3f2c6-121">See also</span></span>

- [<span data-ttu-id="3f2c6-122">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="3f2c6-122">Framework Design Guidelines</span></span>](index.md)
