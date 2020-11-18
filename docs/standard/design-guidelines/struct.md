---
title: 结构设计
ms.date: 10/22/2008
helpviewer_keywords:
- class library design guidelines [.NET Framework], structures
- deallocating structures
- allocating structures
- value types, structures
- structure design
- type design guidelines, structures
- structures [.NET Framework], design guidelines
ms.assetid: 1f48b2d8-608c-4be6-9ba4-d8f203ed9f9f
ms.openlocfilehash: da831d1477b451131bb27372d65ad7229fcf3f77
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94828616"
---
# <a name="struct-design"></a><span data-ttu-id="dc74b-102">结构设计</span><span class="sxs-lookup"><span data-stu-id="dc74b-102">Struct Design</span></span>
<span data-ttu-id="dc74b-103">一般用途值类型最常称为结构，即其 c # 关键字。</span><span class="sxs-lookup"><span data-stu-id="dc74b-103">The general-purpose value type is most often referred to as a struct, its C# keyword.</span></span> <span data-ttu-id="dc74b-104">本部分提供常规结构设计的准则。</span><span class="sxs-lookup"><span data-stu-id="dc74b-104">This section provides guidelines for general struct design.</span></span>

 <span data-ttu-id="dc74b-105">❌ 不要为结构提供无参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="dc74b-105">❌ DO NOT provide a parameterless constructor for a struct.</span></span>

 <span data-ttu-id="dc74b-106">遵循此准则后，便可以创建结构的数组，而不必在每个数组项上运行构造函数。</span><span class="sxs-lookup"><span data-stu-id="dc74b-106">Following this guideline allows arrays of structs to be created without having to run the constructor on each item of the array.</span></span> <span data-ttu-id="dc74b-107">请注意，c # 不允许结构具有无参数的构造函数。</span><span class="sxs-lookup"><span data-stu-id="dc74b-107">Notice that C# does not allow structs to have parameterless constructors.</span></span>

 <span data-ttu-id="dc74b-108">❌ 不要定义可变值类型。</span><span class="sxs-lookup"><span data-stu-id="dc74b-108">❌ DO NOT define mutable value types.</span></span>

 <span data-ttu-id="dc74b-109">可变值类型有几个问题。</span><span class="sxs-lookup"><span data-stu-id="dc74b-109">Mutable value types have several problems.</span></span> <span data-ttu-id="dc74b-110">例如，当属性 getter 返回值类型时，调用方会收到一个副本。</span><span class="sxs-lookup"><span data-stu-id="dc74b-110">For example, when a property getter returns a value type, the caller receives a copy.</span></span> <span data-ttu-id="dc74b-111">由于副本是隐式创建的，因此开发人员可能不会注意到它们正在改变副本，而不是原始值。</span><span class="sxs-lookup"><span data-stu-id="dc74b-111">Because the copy is created implicitly, developers might not be aware that they are mutating the copy, and not the original value.</span></span> <span data-ttu-id="dc74b-112">此外，某些语言 (动态语言，特别) 使用可变值类型时存在问题，因为在取消引用后，即使是本地变量，也会导致复制。</span><span class="sxs-lookup"><span data-stu-id="dc74b-112">Also, some languages (dynamic languages, in particular) have problems using mutable value types because even local variables, when dereferenced, cause a copy to be made.</span></span>

 <span data-ttu-id="dc74b-113">✔️确保将所有实例数据的状态设置为零、false 或 null (适当的) 有效。</span><span class="sxs-lookup"><span data-stu-id="dc74b-113">✔️ DO ensure that a state where all instance data is set to zero, false, or null (as appropriate) is valid.</span></span>

 <span data-ttu-id="dc74b-114">这可以防止在创建结构数组时意外创建无效的实例。</span><span class="sxs-lookup"><span data-stu-id="dc74b-114">This prevents accidental creation of invalid instances when an array of the structs is created.</span></span>

 <span data-ttu-id="dc74b-115">✔️ <xref:System.IEquatable%601> 在值类型上实现。</span><span class="sxs-lookup"><span data-stu-id="dc74b-115">✔️ DO implement <xref:System.IEquatable%601> on value types.</span></span>

 <span data-ttu-id="dc74b-116"><xref:System.Object.Equals%2A?displayProperty=nameWithType>值类型上的方法导致装箱，其默认实现并不太有效，因为它使用反射。</span><span class="sxs-lookup"><span data-stu-id="dc74b-116">The <xref:System.Object.Equals%2A?displayProperty=nameWithType> method on value types causes boxing, and its default implementation is not very efficient, because it uses reflection.</span></span> <span data-ttu-id="dc74b-117"><xref:System.IEquatable%601.Equals%2A> 可以具有更好的性能，并且可以实现，以便它不会导致装箱。</span><span class="sxs-lookup"><span data-stu-id="dc74b-117"><xref:System.IEquatable%601.Equals%2A> can have much better performance and can be implemented so that it will not cause boxing.</span></span>

 <span data-ttu-id="dc74b-118">❌ 不要显式扩展 <xref:System.ValueType> 。</span><span class="sxs-lookup"><span data-stu-id="dc74b-118">❌ DO NOT explicitly extend <xref:System.ValueType>.</span></span> <span data-ttu-id="dc74b-119">事实上，大多数语言都禁止这样做。</span><span class="sxs-lookup"><span data-stu-id="dc74b-119">In fact, most languages prevent this.</span></span>

 <span data-ttu-id="dc74b-120">通常情况下，结构可能非常有用，但只应用于不会频繁装箱的小型单个不可变值。</span><span class="sxs-lookup"><span data-stu-id="dc74b-120">In general, structs can be very useful but should only be used for small, single, immutable values that will not be boxed frequently.</span></span>

 <span data-ttu-id="dc74b-121">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="dc74b-121">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="dc74b-122">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="dc74b-122">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="dc74b-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dc74b-123">See also</span></span>

- [<span data-ttu-id="dc74b-124">类型设计准则</span><span class="sxs-lookup"><span data-stu-id="dc74b-124">Type Design Guidelines</span></span>](type.md)
- [<span data-ttu-id="dc74b-125">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="dc74b-125">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="dc74b-126">在类和结构之间选择</span><span class="sxs-lookup"><span data-stu-id="dc74b-126">Choosing Between Class and Struct</span></span>](choosing-between-class-and-struct.md)
