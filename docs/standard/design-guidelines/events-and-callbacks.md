---
title: 事件和回调
ms.date: 10/22/2008
helpviewer_keywords:
- events [.NET Framework], extensibility
- methods [.NET Framework], callback
- callback methods
- callbacks
ms.assetid: 48b55c60-495f-4089-9396-97f9122bba7c
ms.openlocfilehash: 82c1df01197e04d14436b6e5b3b2c6aaa249add2
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94821224"
---
# <a name="events-and-callbacks"></a><span data-ttu-id="cba8d-102">事件和回调</span><span class="sxs-lookup"><span data-stu-id="cba8d-102">Events and Callbacks</span></span>
<span data-ttu-id="cba8d-103">回调是允许框架通过委托回调到用户代码的扩展点。</span><span class="sxs-lookup"><span data-stu-id="cba8d-103">Callbacks are extensibility points that allow a framework to call back into user code through a delegate.</span></span> <span data-ttu-id="cba8d-104">通常通过方法的参数将这些委托传递到框架。</span><span class="sxs-lookup"><span data-stu-id="cba8d-104">These delegates are usually passed to the framework through a parameter of a method.</span></span>

 <span data-ttu-id="cba8d-105">事件是回调的一种特殊情况，它支持将委托 (事件处理程序) 提供便利且一致的语法。</span><span class="sxs-lookup"><span data-stu-id="cba8d-105">Events are a special case of callbacks that supports convenient and consistent syntax for supplying the delegate (an event handler).</span></span> <span data-ttu-id="cba8d-106">此外，Visual Studio 的语句完成和设计器还提供了有关使用基于事件的 Api 的帮助。</span><span class="sxs-lookup"><span data-stu-id="cba8d-106">In addition, Visual Studio's statement completion and designers provide help in using event-based APIs.</span></span> <span data-ttu-id="cba8d-107"> (参阅 [事件设计](event.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="cba8d-107">(See [Event Design](event.md).)</span></span>

 <span data-ttu-id="cba8d-108">✔️考虑使用回调来允许用户提供要由框架执行的自定义代码。</span><span class="sxs-lookup"><span data-stu-id="cba8d-108">✔️ CONSIDER using callbacks to allow users to provide custom code to be executed by the framework.</span></span>

 <span data-ttu-id="cba8d-109">✔️考虑使用事件来允许用户自定义框架的行为，而无需了解面向对象的设计。</span><span class="sxs-lookup"><span data-stu-id="cba8d-109">✔️ CONSIDER using events to allow users to customize the behavior of a framework without the need for understanding object-oriented design.</span></span>

 <span data-ttu-id="cba8d-110">✔️确实比普通回调更喜欢事件，因为它们对更广泛的开发人员更熟悉，并与 Visual Studio 语句完成集成。</span><span class="sxs-lookup"><span data-stu-id="cba8d-110">✔️ DO prefer events over plain callbacks, because they are more familiar to a broader range of developers and are integrated with Visual Studio statement completion.</span></span>

 <span data-ttu-id="cba8d-111">❌ 避免在性能敏感的 Api 中使用回调。</span><span class="sxs-lookup"><span data-stu-id="cba8d-111">❌ AVOID using callbacks in performance-sensitive APIs.</span></span>

 <span data-ttu-id="cba8d-112">✔️在使用回调定义 Api 时，请使用新的 `Func<...>` 、 `Action<...>` 或 `Expression<...>` 类型而不是自定义委托。</span><span class="sxs-lookup"><span data-stu-id="cba8d-112">✔️ DO use the new `Func<...>`, `Action<...>`, or `Expression<...>` types instead of custom delegates, when defining APIs with callbacks.</span></span>

 <span data-ttu-id="cba8d-113">`Func<...>` 和 `Action<...>` 表示泛型委托。</span><span class="sxs-lookup"><span data-stu-id="cba8d-113">`Func<...>` and `Action<...>` represent generic delegates.</span></span> <span data-ttu-id="cba8d-114">`Expression<...>` 表示可以编译并随后在运行时调用的函数定义，但也可以进行序列化并传递到远程进程。</span><span class="sxs-lookup"><span data-stu-id="cba8d-114">`Expression<...>` represents function definitions that can be compiled and subsequently invoked at runtime but can also be serialized and passed to remote processes.</span></span>

 <span data-ttu-id="cba8d-115">✔️使用而不 `Expression<...>` 是使用和委托来度量和了解性能的含义 `Func<...>` `Action<...>` 。</span><span class="sxs-lookup"><span data-stu-id="cba8d-115">✔️ DO measure and understand performance implications of using `Expression<...>`, instead of using `Func<...>` and `Action<...>` delegates.</span></span>

 <span data-ttu-id="cba8d-116">`Expression<...>` 类型在逻辑上与 `Func<...>` 和 `Action<...>` 委托等效。</span><span class="sxs-lookup"><span data-stu-id="cba8d-116">`Expression<...>` types are in most cases logically equivalent to `Func<...>` and `Action<...>` delegates.</span></span> <span data-ttu-id="cba8d-117">它们之间的主要区别在于委托旨在用于本地处理方案;表达式适用于在远程进程或计算机中计算表达式的好处。</span><span class="sxs-lookup"><span data-stu-id="cba8d-117">The main difference between them is that the delegates are intended to be used in local process scenarios; expressions are intended for cases where it's beneficial and possible to evaluate the expression in a remote process or machine.</span></span>

 <span data-ttu-id="cba8d-118">✔️可以通过调用委托来了解这一点，因为你正在执行任意代码，这可能会对安全性、正确性和兼容性产生影响。</span><span class="sxs-lookup"><span data-stu-id="cba8d-118">✔️ DO understand that by calling a delegate, you are executing arbitrary code and that could have security, correctness, and compatibility repercussions.</span></span>

 <span data-ttu-id="cba8d-119">*部分 &copy; 2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="cba8d-119">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="cba8d-120">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="cba8d-120">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="cba8d-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cba8d-121">See also</span></span>

- [<span data-ttu-id="cba8d-122">扩展性设计</span><span class="sxs-lookup"><span data-stu-id="cba8d-122">Designing for Extensibility</span></span>](designing-for-extensibility.md)
- [<span data-ttu-id="cba8d-123">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="cba8d-123">Framework Design Guidelines</span></span>](index.md)
