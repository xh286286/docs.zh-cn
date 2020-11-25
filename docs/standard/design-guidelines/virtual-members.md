---
title: 虚成员
ms.date: 10/22/2008
helpviewer_keywords:
- overridable members
- virtual members
- members [.NET Framework], virtual
ms.assetid: 8ff4eb97-0364-43ec-8a02-934b5cd94d19
ms.openlocfilehash: 7727ea7fcfdbbecf2e53ddd7a44b4cf907211f80
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95734343"
---
# <a name="virtual-members"></a><span data-ttu-id="1733d-102">虚成员</span><span class="sxs-lookup"><span data-stu-id="1733d-102">Virtual Members</span></span>

<span data-ttu-id="1733d-103">可以重写虚拟成员，从而更改子类的行为。</span><span class="sxs-lookup"><span data-stu-id="1733d-103">Virtual members can be overridden, thus changing the behavior of the subclass.</span></span> <span data-ttu-id="1733d-104">它们与回调在其提供的扩展性上非常相似，但它们在执行性能和内存消耗方面都更好。</span><span class="sxs-lookup"><span data-stu-id="1733d-104">They are quite similar to callbacks in terms of the extensibility they provide, but they are better in terms of execution performance and memory consumption.</span></span> <span data-ttu-id="1733d-105">此外，在需要创建一种特殊类型 (特殊化) 的方案中，虚拟成员更加自然。</span><span class="sxs-lookup"><span data-stu-id="1733d-105">Also, virtual members feel more natural in scenarios that require creating a special kind of an existing type (specialization).</span></span>

 <span data-ttu-id="1733d-106">虚拟成员比回调和事件更好，但其性能不如非虚拟方法。</span><span class="sxs-lookup"><span data-stu-id="1733d-106">Virtual members perform better than callbacks and events, but do not perform better than non-virtual methods.</span></span>

 <span data-ttu-id="1733d-107">虚拟成员的主要缺点是，在编译时只能修改虚拟成员的行为。</span><span class="sxs-lookup"><span data-stu-id="1733d-107">The main disadvantage of virtual members is that the behavior of a virtual member can only be modified at the time of compilation.</span></span> <span data-ttu-id="1733d-108">可以在运行时修改回调行为。</span><span class="sxs-lookup"><span data-stu-id="1733d-108">The behavior of a callback can be modified at runtime.</span></span>

 <span data-ttu-id="1733d-109">由于对虚拟成员的任何调用都可以以不可预知的方式重写，并且可以执行任意代码，因此虚拟成员（如回调 (和回调) 可能更多的设计、测试和维护。</span><span class="sxs-lookup"><span data-stu-id="1733d-109">Virtual members, like callbacks (and maybe more than callbacks), are costly to design, test, and maintain because any call to a virtual member can be overridden in unpredictable ways and can execute arbitrary code.</span></span> <span data-ttu-id="1733d-110">此外，通常还需要更多的工作来清楚地定义虚拟成员的协定，因此设计和记录这些成员的成本更高。</span><span class="sxs-lookup"><span data-stu-id="1733d-110">Also, much more effort is usually required to clearly define the contract of virtual members, so the cost of designing and documenting them is higher.</span></span>

 <span data-ttu-id="1733d-111">❌ 不要将成员设为虚拟的，除非您有充分的理由这样做，并且您知道与设计、测试和维护虚拟成员相关的所有成本。</span><span class="sxs-lookup"><span data-stu-id="1733d-111">❌ DO NOT make members virtual unless you have a good reason to do so and you are aware of all the costs related to designing, testing, and maintaining virtual members.</span></span>

 <span data-ttu-id="1733d-112">在无需中断兼容性的情况下，虚拟成员就可以对其进行更改，而不是包容性。</span><span class="sxs-lookup"><span data-stu-id="1733d-112">Virtual members are less forgiving in terms of changes that can be made to them without breaking compatibility.</span></span> <span data-ttu-id="1733d-113">而且，它们比非虚拟成员慢，主要是因为对虚拟成员的调用不内联。</span><span class="sxs-lookup"><span data-stu-id="1733d-113">Also, they are slower than non-virtual members, mostly because calls to virtual members are not inlined.</span></span>

 <span data-ttu-id="1733d-114">✔️考虑将扩展性限制为仅绝对必要的。</span><span class="sxs-lookup"><span data-stu-id="1733d-114">✔️ CONSIDER limiting extensibility to only what is absolutely necessary.</span></span>

 <span data-ttu-id="1733d-115">✔️比虚拟成员的公共可访问性更喜欢受保护的可访问性。</span><span class="sxs-lookup"><span data-stu-id="1733d-115">✔️ DO prefer protected accessibility over public accessibility for virtual members.</span></span> <span data-ttu-id="1733d-116">公共成员应通过调用受保护的虚拟成员) 来提供扩展性 (。</span><span class="sxs-lookup"><span data-stu-id="1733d-116">Public members should provide extensibility (if required) by calling into a protected virtual member.</span></span>

 <span data-ttu-id="1733d-117">类的公共成员应为该类的直接使用者提供正确的一组功能。</span><span class="sxs-lookup"><span data-stu-id="1733d-117">The public members of a class should provide the right set of functionality for direct consumers of that class.</span></span> <span data-ttu-id="1733d-118">虚拟成员设计为在子类中被重写，受保护的可访问性是将所有虚拟扩展点的范围限定为可使用这些扩展点的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="1733d-118">Virtual members are designed to be overridden in subclasses, and protected accessibility is a great way to scope all virtual extensibility points to where they can be used.</span></span>

 <span data-ttu-id="1733d-119">*部分 &copy; 2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="1733d-119">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="1733d-120">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="1733d-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="1733d-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1733d-121">See also</span></span>

- [<span data-ttu-id="1733d-122">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="1733d-122">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="1733d-123">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="1733d-123">Designing for Extensibility</span></span>](designing-for-extensibility.md)
