---
title: 运行时指令元素
ms.date: 03/30/2017
ms.assetid: 3fe5848c-ecd7-4136-970b-8e48d250bde6
ms.openlocfilehash: 96bce89c02ad17d1b30eda66237f69a15123dcd3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96250796"
---
# <a name="runtime-directive-elements"></a><span data-ttu-id="fd4d3-102">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="fd4d3-102">Runtime Directive Elements</span></span>

<span data-ttu-id="fd4d3-103">运行时指令 (rd.xml) 文件格式支持以下运行时指令元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-103">The runtime directives (rd.xml) file format supports the following runtime directive elements.</span></span> <span data-ttu-id="fd4d3-104">请参阅[运行时指令 (rd.xml) 配置文件参考](runtime-directives-rd-xml-configuration-file-reference.md)了解分层表示形式。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-104">See [Runtime Directives (rd.xml) Configuration File Reference](runtime-directives-rd-xml-configuration-file-reference.md) for a hierarchical representation.</span></span>  
  
 [\<Application>](application-element-net-native.md)  
 <span data-ttu-id="fd4d3-105">将运行时反射策略应用到该应用使用的所有类型，作为应用程序范围内的类型和元数据可以反应在运行时间的类型成员的容器而服务。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-105">Applies runtime reflection policy to all types used by the app, and serves as a container for application-wide types and type members whose metadata is available for reflection at run time.</span></span> <span data-ttu-id="fd4d3-106">这是元素的子 [\<Directives>](directives-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-106">This is a child of the [\<Directives>](directives-element-net-native.md) element.</span></span>  
  
 [\<Assembly>](assembly-element-net-native.md)  
 <span data-ttu-id="fd4d3-107">将运行时策略应用到程序集中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-107">Applies runtime policy to all the types in an assembly.</span></span> <span data-ttu-id="fd4d3-108">这是和元素的子 [\<Application>](application-element-net-native.md) [\<Library>](library-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-108">This is a child of the [\<Application>](application-element-net-native.md) and [\<Library>](library-element-net-native.md) elements.</span></span>  
  
 [\<AttributeImplies>](attributeimplies-element-net-native.md)  
 <span data-ttu-id="fd4d3-109">如果其包含 [\<Type>](type-element-net-native.md) 指令是一个属性，则将运行时策略应用到该特性应用到的代码元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-109">If its containing [\<Type>](type-element-net-native.md) directive is an attribute, applies runtime policy to code elements to which that attribute is applied.</span></span>  
  
 [\<Directives>](directives-element-net-native.md)  
 <span data-ttu-id="fd4d3-110">.NET Native 的每个运行时指令文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-110">The root element in every runtime directives file for .NET Native.</span></span> <span data-ttu-id="fd4d3-111">其子元素为 [\<Application>](application-element-net-native.md) 和 [\<Library>](library-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-111">Its child elements are [\<Application>](application-element-net-native.md) and [\<Library>](library-element-net-native.md).</span></span>  
  
 [\<Event>](event-element-net-native.md)  
 <span data-ttu-id="fd4d3-112">将运行时策略应用到一个事件。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-112">Applies runtime policy to an event.</span></span> <span data-ttu-id="fd4d3-113">这是和元素的子 [\<Type>](type-element-net-native.md) [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-113">This is a child of the [\<Type>](type-element-net-native.md) and [\<TypeInstantiation>](typeinstantiation-element-net-native.md) elements.</span></span>  
  
 [\<Field>](field-element-net-native.md)  
 <span data-ttu-id="fd4d3-114">将运行时策略应用到一个字段。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-114">Applies runtime policy to a field.</span></span> <span data-ttu-id="fd4d3-115">这是和元素的子 [\<Type>](type-element-net-native.md) [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-115">This is a child of the [\<Type>](type-element-net-native.md) and [\<TypeInstantiation>](typeinstantiation-element-net-native.md) elements.</span></span>  
  
 [\<GenericParameter>](genericparameter-element-net-native.md)  
 <span data-ttu-id="fd4d3-116">将运行时策略应用到一个泛型类型或方法的参数类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-116">Applies runtime policy to the parameter type of a generic type or method.</span></span>  
  
 [\<ImpliesType>](impliestype-element-net-native.md)  
 <span data-ttu-id="fd4d3-117">如果该策略已应用到该包含类型或方法，将该运行时策略应用到一个类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-117">Applies runtime policy to a type, if that policy has been applied to the containing type or method.</span></span>  
  
 [\<Library>](library-element-net-native.md)  
 <span data-ttu-id="fd4d3-118">将运行时策略应用到程序集中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-118">Applies runtime policy to all the types in an assembly.</span></span> <span data-ttu-id="fd4d3-119">这是和元素的子 [\<Application>](application-element-net-native.md) [\<Library>](library-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-119">This is a child of the [\<Application>](application-element-net-native.md) and [\<Library>](library-element-net-native.md) elements.</span></span>  
  
 [\<Method>](method-element-net-native.md)  
 <span data-ttu-id="fd4d3-120">将运行时策略应用到一个方法。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-120">Applies runtime policy to a method.</span></span> <span data-ttu-id="fd4d3-121">这是和元素的子 [\<Type>](type-element-net-native.md) [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-121">This is a child of the [\<Type>](type-element-net-native.md) and [\<TypeInstantiation>](typeinstantiation-element-net-native.md) elements.</span></span>  
  
 [\<MethodInstantiation>](methodinstantiation-element-net-native.md)  
 <span data-ttu-id="fd4d3-122">将运行时策略应用到一个构造泛型方法。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-122">Applies runtime policy to a constructed generic method.</span></span> <span data-ttu-id="fd4d3-123">这是和元素的子 [\<Type>](type-element-net-native.md) [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-123">This is a child of the [\<Type>](type-element-net-native.md) and [\<TypeInstantiation>](typeinstantiation-element-net-native.md) elements.</span></span>  
  
 [\<Namespace>](namespace-element-net-native.md)  
 <span data-ttu-id="fd4d3-124">将运行时策略应用到命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-124">Applies runtime policy to all the types in a namespace.</span></span>  
  
 [\<Parameter>](parameter-element-net-native.md)  
 <span data-ttu-id="fd4d3-125">将运行时策略应用到传递到方法的参数类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-125">Applies runtime policy to the type of the argument passed to a method.</span></span>  
  
 [\<Property>](property-element-net-native.md)  
 <span data-ttu-id="fd4d3-126">将运行时策略应用到一个属性。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-126">Applies runtime policy to a property.</span></span> <span data-ttu-id="fd4d3-127">这是和元素的子 [\<Type>](type-element-net-native.md) [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-127">This is a child of the [\<Type>](type-element-net-native.md) and [\<TypeInstantiation>](typeinstantiation-element-net-native.md) elements.</span></span>  
  
 [\<Subtypes>](subtypes-element-net-native.md)  
 <span data-ttu-id="fd4d3-128">将运行时策略应用到从包含类型继承的所有类。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-128">Applies runtime policy to all classes inherited from the containing type.</span></span>  
  
 [\<Type>](type-element-net-native.md)  
 <span data-ttu-id="fd4d3-129">将运行时策略应用到一个类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-129">Applies runtime policy to a type.</span></span>  
  
 [\<TypeInstantiation>](typeinstantiation-element-net-native.md)  
 <span data-ttu-id="fd4d3-130">将运行时策略应用到一个构造泛型类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-130">Applies runtime policy to a constructed generic type.</span></span>  
  
 [\<TypeParameter>](typeparameter-element-net-native.md)  
 <span data-ttu-id="fd4d3-131">将运行时策略应用到以传递到方法为代表的 <xref:System.Type> 自变量类型。</span><span class="sxs-lookup"><span data-stu-id="fd4d3-131">Applies runtime policy to the type represented by a <xref:System.Type> argument passed to a method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd4d3-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fd4d3-132">See also</span></span>

- [<span data-ttu-id="fd4d3-133">rd.xml 配置文件参考</span><span class="sxs-lookup"><span data-stu-id="fd4d3-133">rd.xml Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
