---
title: 命名参数
description: 了解参数命名准则。 例如，使用 & camel 大小写格式的描述性参数名称，& 考虑基于含义而不是类型进行命名。
ms.date: 10/22/2008
helpviewer_keywords:
- parameters, names
- names [.NET Framework], parameters
ms.assetid: ca3c956e-725a-441b-b4e3-eab5d472f41c
ms.openlocfilehash: 9f03eda511c2ef0c9565d270c52fd72bf54692d8
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95698346"
---
# <a name="naming-parameters"></a><span data-ttu-id="a1c51-104">命名参数</span><span class="sxs-lookup"><span data-stu-id="a1c51-104">Naming Parameters</span></span>

<span data-ttu-id="a1c51-105">除了可读性的明显原因外，请务必遵循有关参数名称的准则，因为当可视化设计工具提供 Intellisense 和类浏览功能时，参数将显示在文档和设计器中。</span><span class="sxs-lookup"><span data-stu-id="a1c51-105">Beyond the obvious reason of readability, it is important to follow the guidelines for parameter names because parameters are displayed in documentation and in the designer when visual design tools provide Intellisense and class browsing functionality.</span></span>

 <span data-ttu-id="a1c51-106">✔️在参数名称中使用 camelCasing。</span><span class="sxs-lookup"><span data-stu-id="a1c51-106">✔️ DO use camelCasing in parameter names.</span></span>

 <span data-ttu-id="a1c51-107">✔️使用描述性参数名称。</span><span class="sxs-lookup"><span data-stu-id="a1c51-107">✔️ DO use descriptive parameter names.</span></span>

 <span data-ttu-id="a1c51-108">✔️考虑使用基于参数含义而不是参数类型的名称。</span><span class="sxs-lookup"><span data-stu-id="a1c51-108">✔️ CONSIDER using names based on a parameter’s meaning rather than the parameter’s type.</span></span>

### <a name="naming-operator-overload-parameters"></a><span data-ttu-id="a1c51-109">命名运算符重载参数</span><span class="sxs-lookup"><span data-stu-id="a1c51-109">Naming Operator Overload Parameters</span></span>

 <span data-ttu-id="a1c51-110">`left` `right` 如果参数没有任何意义，✔️确实要使用和进行二元运算符重载参数名称。</span><span class="sxs-lookup"><span data-stu-id="a1c51-110">✔️ DO use `left` and `right` for binary operator overload parameter names if there is no meaning to the parameters.</span></span>

 <span data-ttu-id="a1c51-111">对于参数，✔️确实使用 `value` 一元运算符重载参数名称。</span><span class="sxs-lookup"><span data-stu-id="a1c51-111">✔️ DO use `value` for unary operator overload parameter names if there is no meaning to the parameters.</span></span>

 <span data-ttu-id="a1c51-112">✔️考虑运算符重载参数有意义的名称，如果这样做会增加重要值。</span><span class="sxs-lookup"><span data-stu-id="a1c51-112">✔️ CONSIDER meaningful names for operator overload parameters if doing so adds significant value.</span></span>

 <span data-ttu-id="a1c51-113">❌ 不要对运算符重载参数名称使用缩写或数值索引。</span><span class="sxs-lookup"><span data-stu-id="a1c51-113">❌ DO NOT use abbreviations or numeric indices for operator overload parameter names.</span></span>

 <span data-ttu-id="a1c51-114">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="a1c51-114">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="a1c51-115">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="a1c51-115">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="a1c51-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1c51-116">See also</span></span>

- [<span data-ttu-id="a1c51-117">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="a1c51-117">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="a1c51-118">命名准则</span><span class="sxs-lookup"><span data-stu-id="a1c51-118">Naming Guidelines</span></span>](naming-guidelines.md)
