---
title: 静态类设计
ms.date: 10/22/2008
helpviewer_keywords:
- type design guidelines, static classes
- class library design guidelines [.NET Framework], classes
- classes [.NET Framework], static
- static classes [.NET Framework]
- classes [.NET Framework], design guidelines
- type design guidelines, classes
ms.assetid: d67c14d8-c4dd-443f-affb-4ccae677c9b6
ms.openlocfilehash: efa5ca6e7b5e7b7d03cbe1d55471a388f3faab37
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94828655"
---
# <a name="static-class-design"></a><span data-ttu-id="c48f9-102">静态类设计</span><span class="sxs-lookup"><span data-stu-id="c48f9-102">Static Class Design</span></span>
<span data-ttu-id="c48f9-103">静态类定义为仅包含静态成员的类 (当然，除了从继承的实例成员 <xref:System.Object?displayProperty=nameWithType> 和可能的私有构造函数) 。</span><span class="sxs-lookup"><span data-stu-id="c48f9-103">A static class is defined as a class that contains only static members (of course besides the instance members inherited from <xref:System.Object?displayProperty=nameWithType> and possibly a private constructor).</span></span> <span data-ttu-id="c48f9-104">某些语言为静态类提供内置支持。</span><span class="sxs-lookup"><span data-stu-id="c48f9-104">Some languages provide built-in support for static classes.</span></span> <span data-ttu-id="c48f9-105">在 c # 2.0 和更高版本中，将类声明为静态时，它是密封的、抽象的，并且不能重写或声明任何实例成员。</span><span class="sxs-lookup"><span data-stu-id="c48f9-105">In C# 2.0 and later, when a class is declared to be static, it is sealed, abstract, and no instance members can be overridden or declared.</span></span>

 <span data-ttu-id="c48f9-106">静态类在面向对象的纯设计和简单性之间是一种折衷方案。</span><span class="sxs-lookup"><span data-stu-id="c48f9-106">Static classes are a compromise between pure object-oriented design and simplicity.</span></span> <span data-ttu-id="c48f9-107">它们通常用于提供 (等其他操作的快捷方式，如 <xref:System.IO.File?displayProperty=nameWithType>) 、扩展方法的持有者，或完全面向对象的包装器 (如) 等功能 <xref:System.Environment?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="c48f9-107">They are commonly used to provide shortcuts to other operations (such as <xref:System.IO.File?displayProperty=nameWithType>), holders of extension methods, or functionality for which a full object-oriented wrapper is unwarranted (such as <xref:System.Environment?displayProperty=nameWithType>).</span></span>

 <span data-ttu-id="c48f9-108">✔️尽量少使用静态类。</span><span class="sxs-lookup"><span data-stu-id="c48f9-108">✔️ DO use static classes sparingly.</span></span>

 <span data-ttu-id="c48f9-109">静态类只应用作框架的面向对象核心的支持类。</span><span class="sxs-lookup"><span data-stu-id="c48f9-109">Static classes should be used only as supporting classes for the object-oriented core of the framework.</span></span>

 <span data-ttu-id="c48f9-110">❌ 不要将静态类视为其他存储桶。</span><span class="sxs-lookup"><span data-stu-id="c48f9-110">❌ DO NOT treat static classes as a miscellaneous bucket.</span></span>

 <span data-ttu-id="c48f9-111">❌ 不要在静态类中声明或重写实例成员。</span><span class="sxs-lookup"><span data-stu-id="c48f9-111">❌ DO NOT declare or override instance members in static classes.</span></span>

 <span data-ttu-id="c48f9-112">如果你的编程语言没有对静态类的内置支持，✔️会将静态类声明为密封、抽象并添加私有实例构造函数。</span><span class="sxs-lookup"><span data-stu-id="c48f9-112">✔️ DO declare static classes as sealed, abstract, and add a private instance constructor if your programming language does not have built-in support for static classes.</span></span>

 <span data-ttu-id="c48f9-113">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="c48f9-113">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="c48f9-114">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="c48f9-114">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="c48f9-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c48f9-115">See also</span></span>

- [<span data-ttu-id="c48f9-116">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="c48f9-116">Type Design Guidelines</span></span>](type.md)
- [<span data-ttu-id="c48f9-117">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="c48f9-117">Framework Design Guidelines</span></span>](index.md)
