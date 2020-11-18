---
title: 特性
ms.date: 10/22/2008
helpviewer_keywords:
- attributes [.NET Framework], about
- class library design guidelines [.NET Framework], attributes
ms.assetid: ee0038ef-b247-4747-a650-3c5c5cd58d8b
ms.openlocfilehash: cc4752066124a0ea8081390bfb5f3791d21ec96d
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94821614"
---
# <a name="attributes"></a><span data-ttu-id="d754e-102">属性</span><span class="sxs-lookup"><span data-stu-id="d754e-102">Attributes</span></span>
<span data-ttu-id="d754e-103"><xref:System.Attribute?displayProperty=nameWithType> 用于定义自定义属性的基类。</span><span class="sxs-lookup"><span data-stu-id="d754e-103"><xref:System.Attribute?displayProperty=nameWithType> is a base class used to define custom attributes.</span></span>

 <span data-ttu-id="d754e-104">特性是可以添加到编程元素（如程序集、类型、成员和参数）的批注。</span><span class="sxs-lookup"><span data-stu-id="d754e-104">Attributes are annotations that can be added to programming elements such as assemblies, types, members, and parameters.</span></span> <span data-ttu-id="d754e-105">它们存储在程序集的元数据中，并且可在运行时使用反射 Api 进行访问。</span><span class="sxs-lookup"><span data-stu-id="d754e-105">They are stored in the metadata of the assembly and can be accessed at runtime using the reflection APIs.</span></span> <span data-ttu-id="d754e-106">例如，框架定义 <xref:System.ObsoleteAttribute> ，它可以应用于类型或成员，以指示类型或成员已弃用。</span><span class="sxs-lookup"><span data-stu-id="d754e-106">For example, the Framework defines the <xref:System.ObsoleteAttribute>, which can be applied to a type or a member to indicate that the type or member has been deprecated.</span></span>

 <span data-ttu-id="d754e-107">特性可以具有一个或多个属性，这些属性包含与特性相关的其他数据。</span><span class="sxs-lookup"><span data-stu-id="d754e-107">Attributes can have one or more properties that carry additional data related to the attribute.</span></span> <span data-ttu-id="d754e-108">例如， `ObsoleteAttribute` 可能会携带有关已弃用类型或成员的发布的附加信息，以及替换已过时 api 的新 api 的说明。</span><span class="sxs-lookup"><span data-stu-id="d754e-108">For example, `ObsoleteAttribute` could carry additional information about the release in which a type or a member got deprecated and the description of the new APIs replacing the obsolete API.</span></span>

 <span data-ttu-id="d754e-109">应用特性时，必须指定特性的某些属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-109">Some properties of an attribute must be specified when the attribute is applied.</span></span> <span data-ttu-id="d754e-110">它们被称为必需的属性或必需的参数，因为它们表示为位置构造函数参数。</span><span class="sxs-lookup"><span data-stu-id="d754e-110">These are referred to as the required properties or required arguments, because they are represented as positional constructor parameters.</span></span> <span data-ttu-id="d754e-111">例如， <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> 的属性 <xref:System.Diagnostics.ConditionalAttribute> 是必需的属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-111">For example, the <xref:System.Diagnostics.ConditionalAttribute.ConditionString%2A> property of the <xref:System.Diagnostics.ConditionalAttribute> is a required property.</span></span>

 <span data-ttu-id="d754e-112">在应用特性时不一定要指定的属性称为可选属性， (或可选参数) 。</span><span class="sxs-lookup"><span data-stu-id="d754e-112">Properties that do not necessarily have to be specified when the attribute is applied are called optional properties (or optional arguments).</span></span> <span data-ttu-id="d754e-113">它们由可设置的属性表示。</span><span class="sxs-lookup"><span data-stu-id="d754e-113">They are represented by settable properties.</span></span> <span data-ttu-id="d754e-114">应用特性时，编译器提供了用于设置这些属性的特殊语法。</span><span class="sxs-lookup"><span data-stu-id="d754e-114">Compilers provide special syntax to set these properties when an attribute is applied.</span></span> <span data-ttu-id="d754e-115">例如， <xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> 属性表示可选参数。</span><span class="sxs-lookup"><span data-stu-id="d754e-115">For example, the <xref:System.AttributeUsageAttribute.Inherited%2A?displayProperty=nameWithType> property represents an optional argument.</span></span>

 <span data-ttu-id="d754e-116">✔️命名具有后缀 "Attribute" 的自定义属性类。</span><span class="sxs-lookup"><span data-stu-id="d754e-116">✔️ DO name custom attribute classes with the suffix "Attribute."</span></span>

 <span data-ttu-id="d754e-117">✔️将应用 <xref:System.AttributeUsageAttribute> 到自定义属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-117">✔️ DO apply the <xref:System.AttributeUsageAttribute> to custom attributes.</span></span>

 <span data-ttu-id="d754e-118">✔️提供可选参数的可设置属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-118">✔️ DO provide settable properties for optional arguments.</span></span>

 <span data-ttu-id="d754e-119">✔️确实提供必需参数的只需属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-119">✔️ DO provide get-only properties for required arguments.</span></span>

 <span data-ttu-id="d754e-120">✔️提供构造函数参数来初始化对应于所需参数的属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-120">✔️ DO provide constructor parameters to initialize properties corresponding to required arguments.</span></span> <span data-ttu-id="d754e-121">每个参数应该具有相同的名称 (但大小写不同) 为相应的属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-121">Each parameter should have the same name (although with different casing) as the corresponding property.</span></span>

 <span data-ttu-id="d754e-122">❌ 避免提供构造函数参数来初始化对应于可选参数的属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-122">❌ AVOID providing constructor parameters to initialize properties corresponding to the optional arguments.</span></span>

 <span data-ttu-id="d754e-123">换句话说，不能使用构造函数和 setter 来设置属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-123">In other words, do not have properties that can be set with both a constructor and a setter.</span></span> <span data-ttu-id="d754e-124">此准则非常明确，哪些参数是可选的，哪些是必需的，并且避免了两种方法来执行相同的操作。</span><span class="sxs-lookup"><span data-stu-id="d754e-124">This guideline makes very explicit which arguments are optional and which are required, and avoids having two ways of doing the same thing.</span></span>

 <span data-ttu-id="d754e-125">❌ 避免重载自定义特性构造函数。</span><span class="sxs-lookup"><span data-stu-id="d754e-125">❌ AVOID overloading custom attribute constructors.</span></span>

 <span data-ttu-id="d754e-126">只有一个构造函数清楚地向用户传达需要哪些参数，哪些参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="d754e-126">Having only one constructor clearly communicates to the user which arguments are required and which are optional.</span></span>

 <span data-ttu-id="d754e-127">如果可能，✔️确实密封自定义特性类。</span><span class="sxs-lookup"><span data-stu-id="d754e-127">✔️ DO seal custom attribute classes, if possible.</span></span> <span data-ttu-id="d754e-128">这样可以更快地查找属性。</span><span class="sxs-lookup"><span data-stu-id="d754e-128">This makes the look-up for the attribute faster.</span></span>

 <span data-ttu-id="d754e-129">*部分 &copy; 2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="d754e-129">*Portions &copy; 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="d754e-130">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="d754e-130">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="d754e-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d754e-131">See also</span></span>

- [<span data-ttu-id="d754e-132">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="d754e-132">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="d754e-133">使用准则</span><span class="sxs-lookup"><span data-stu-id="d754e-133">Usage Guidelines</span></span>](usage-guidelines.md)
