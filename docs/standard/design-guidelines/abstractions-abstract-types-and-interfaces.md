---
title: 抽象（抽象类型和接口）
ms.date: 10/22/2008
helpviewer_keywords:
- interfaces [.NET Framework], abstract
- abstract interfaces [.NET Framework]
- abstract types [.NET Framework]
- types [.NET Framework], abstract
ms.assetid: 0a632bc7-9b03-44ee-8842-c82f88672a45
ms.openlocfilehash: f5169cf730dc987526765c9538978901d424814b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95701401"
---
# <a name="abstractions-abstract-types-and-interfaces"></a><span data-ttu-id="27f3f-102">抽象（抽象类型和接口）</span><span class="sxs-lookup"><span data-stu-id="27f3f-102">Abstractions (Abstract Types and Interfaces)</span></span>

<span data-ttu-id="27f3f-103">抽象是一种类型，它描述协定，但不提供协定的完全实现。</span><span class="sxs-lookup"><span data-stu-id="27f3f-103">An abstraction is a type that describes a contract but does not provide a full implementation of the contract.</span></span> <span data-ttu-id="27f3f-104">抽象通常作为抽象类或接口实现，它们附带一组明确定义的参考文档，其中描述了实现协定的类型所需的语义。</span><span class="sxs-lookup"><span data-stu-id="27f3f-104">Abstractions are usually implemented as abstract classes or interfaces, and they come with a well-defined set of reference documentation describing the required semantics of the types implementing the contract.</span></span> <span data-ttu-id="27f3f-105">.NET Framework 中的一些最重要的抽象包括 <xref:System.IO.Stream> 、 <xref:System.Collections.Generic.IEnumerable%601> 和 <xref:System.Object> 。</span><span class="sxs-lookup"><span data-stu-id="27f3f-105">Some of the most important abstractions in the .NET Framework include <xref:System.IO.Stream>, <xref:System.Collections.Generic.IEnumerable%601>, and <xref:System.Object>.</span></span>

 <span data-ttu-id="27f3f-106">您可以通过实现支持抽象协定的具体类型，并将此具体类型与) 抽象 (操作的框架 Api 结合使用来扩展框架。</span><span class="sxs-lookup"><span data-stu-id="27f3f-106">You can extend frameworks by implementing a concrete type that supports the contract of an abstraction and using this concrete type with framework APIs consuming (operating on) the abstraction.</span></span>

 <span data-ttu-id="27f3f-107">很难设计一种有意义且有用的抽象方法，它能够经受时间测试。</span><span class="sxs-lookup"><span data-stu-id="27f3f-107">A meaningful and useful abstraction that is able to withstand the test of time is very difficult to design.</span></span> <span data-ttu-id="27f3f-108">主要难点是获得正确的成员集，而不是更少的成员。</span><span class="sxs-lookup"><span data-stu-id="27f3f-108">The main difficulty is getting the right set of members, no more and no fewer.</span></span> <span data-ttu-id="27f3f-109">如果抽象的成员太多，就会变得难以甚至不可能实现。</span><span class="sxs-lookup"><span data-stu-id="27f3f-109">If an abstraction has too many members, it becomes difficult or even impossible to implement.</span></span> <span data-ttu-id="27f3f-110">如果它的成员对于承诺的功能而言太少，则在很多有趣的情况下它将变得毫无用处。</span><span class="sxs-lookup"><span data-stu-id="27f3f-110">If it has too few members for the promised functionality, it becomes useless in many interesting scenarios.</span></span>

 <span data-ttu-id="27f3f-111">框架中的抽象太多也会对框架的可用性产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="27f3f-111">Too many abstractions in a framework also negatively affect usability of the framework.</span></span> <span data-ttu-id="27f3f-112">很难理解抽象，而不了解它如何适应具体实现和在抽象上操作的 Api 的更大的了解。</span><span class="sxs-lookup"><span data-stu-id="27f3f-112">It is often quite difficult to understand an abstraction without understanding how it fits into the larger picture of the concrete implementations and the APIs operating on the abstraction.</span></span> <span data-ttu-id="27f3f-113">此外，抽象和其成员的名称都必须是抽象的，这通常会使它们变得难懂和 unapproachable，而无需事先了解其使用情况的更广泛的上下文。</span><span class="sxs-lookup"><span data-stu-id="27f3f-113">Also, names of abstractions and their members are necessarily abstract, which often makes them cryptic and unapproachable without first understanding the broader context of their usage.</span></span>

 <span data-ttu-id="27f3f-114">不过，抽象提供了极其强大的可扩展性，其他扩展性机制通常不会匹配。</span><span class="sxs-lookup"><span data-stu-id="27f3f-114">However, abstractions provide extremely powerful extensibility that the other extensibility mechanisms cannot often match.</span></span> <span data-ttu-id="27f3f-115">它们是多个体系结构模式的核心，如插件、控制反转 (IoC) 、管道等。</span><span class="sxs-lookup"><span data-stu-id="27f3f-115">They are at the core of many architectural patterns, such as plug-ins, inversion of control (IoC), pipelines, and so on.</span></span> <span data-ttu-id="27f3f-116">它们对于框架的可测试性也极其重要。</span><span class="sxs-lookup"><span data-stu-id="27f3f-116">They are also extremely important for testability of frameworks.</span></span> <span data-ttu-id="27f3f-117">好的抽象使你可以出于单元测试的目的，为大量依赖关系提供存根。</span><span class="sxs-lookup"><span data-stu-id="27f3f-117">Good abstractions make it possible to stub out heavy dependencies for the purpose of unit testing.</span></span> <span data-ttu-id="27f3f-118">总的来说，抽象负责面向面向对象的现代框架的丰富丰富。</span><span class="sxs-lookup"><span data-stu-id="27f3f-118">In summary, abstractions are responsible for the sought-after richness of the modern object-oriented frameworks.</span></span>

 <span data-ttu-id="27f3f-119">❌ 不要提供抽象，除非通过开发一些具体的实现和使用抽象的 Api 来对它们进行测试。</span><span class="sxs-lookup"><span data-stu-id="27f3f-119">❌ DO NOT provide abstractions unless they are tested by developing several concrete implementations and APIs consuming the abstractions.</span></span>

 <span data-ttu-id="27f3f-120">✔️在设计抽象类和接口时，请仔细选择抽象类和接口。</span><span class="sxs-lookup"><span data-stu-id="27f3f-120">✔️ DO choose carefully between an abstract class and an interface when designing an abstraction.</span></span>

 <span data-ttu-id="27f3f-121">✔️考虑为抽象的具体实现提供引用测试。</span><span class="sxs-lookup"><span data-stu-id="27f3f-121">✔️ CONSIDER providing reference tests for concrete implementations of abstractions.</span></span> <span data-ttu-id="27f3f-122">此类测试应该允许用户测试其实现是否能正确实现协定。</span><span class="sxs-lookup"><span data-stu-id="27f3f-122">Such tests should allow users to test whether their implementations correctly implement the contract.</span></span>

 <span data-ttu-id="27f3f-123">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="27f3f-123">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="27f3f-124">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="27f3f-124">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="27f3f-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="27f3f-125">See also</span></span>

- [<span data-ttu-id="27f3f-126">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="27f3f-126">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="27f3f-127">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="27f3f-127">Designing for Extensibility</span></span>](designing-for-extensibility.md)
