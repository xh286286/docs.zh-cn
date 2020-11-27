---
title: <Namespace>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 57c614e5-18a9-4e87-bfd5-d0fe3396a192
ms.openlocfilehash: 05de04685f8ba746f55bf040c74fd3831c5b63ca
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96287886"
---
# <a name="namespace-element-net-native"></a><span data-ttu-id="69bcc-102">\<Namespace>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="69bcc-102">\<Namespace> Element (.NET Native)</span></span>

<span data-ttu-id="69bcc-103">将运行时反射策略应用到一个指定的命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-103">Applies runtime reflection policy to all the types in a specified namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69bcc-104">语法</span><span class="sxs-lookup"><span data-stu-id="69bcc-104">Syntax</span></span>  
  
```xml  
<Namespace Name="namespace_name"
           Activate="policy_type"
           Browse="policy_type"  
           Dynamic="policy_setting"  
           Serialize="policy_setting"  
           DataContractSerializer="policy_setting"  
           DataContractJsonSerializer="policy_setting"  
           XmlSerializer="policy_setting"  
           MarshalObject="policy_setting"  
           MarshalDelegate="policy_setting"  
           MarshalStructure="policy_setting" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="69bcc-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="69bcc-105">Attributes and Elements</span></span>  

 <span data-ttu-id="69bcc-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69bcc-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="69bcc-107">特性</span><span class="sxs-lookup"><span data-stu-id="69bcc-107">Attributes</span></span>  
  
|<span data-ttu-id="69bcc-108">属性</span><span class="sxs-lookup"><span data-stu-id="69bcc-108">Attribute</span></span>|<span data-ttu-id="69bcc-109">属性类型</span><span class="sxs-lookup"><span data-stu-id="69bcc-109">Attribute type</span></span>|<span data-ttu-id="69bcc-110">描述</span><span class="sxs-lookup"><span data-stu-id="69bcc-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Name`|<span data-ttu-id="69bcc-111">常规</span><span class="sxs-lookup"><span data-stu-id="69bcc-111">General</span></span>|<span data-ttu-id="69bcc-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-112">Required attribute.</span></span> <span data-ttu-id="69bcc-113">指定命名空间的名称。</span><span class="sxs-lookup"><span data-stu-id="69bcc-113">Specifies the name of the namespace.</span></span>|  
|`Activate`|<span data-ttu-id="69bcc-114">反射</span><span class="sxs-lookup"><span data-stu-id="69bcc-114">Reflection</span></span>|<span data-ttu-id="69bcc-115">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-115">Optional attribute.</span></span> <span data-ttu-id="69bcc-116">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="69bcc-116">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="69bcc-117">反射</span><span class="sxs-lookup"><span data-stu-id="69bcc-117">Reflection</span></span>|<span data-ttu-id="69bcc-118">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-118">Optional attribute.</span></span> <span data-ttu-id="69bcc-119">控制对有关程序元素信息的查询，但并不启用任何运行时访问。</span><span class="sxs-lookup"><span data-stu-id="69bcc-119">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="69bcc-120">反射</span><span class="sxs-lookup"><span data-stu-id="69bcc-120">Reflection</span></span>|<span data-ttu-id="69bcc-121">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-121">Optional attribute.</span></span> <span data-ttu-id="69bcc-122">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="69bcc-122">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="69bcc-123">序列化</span><span class="sxs-lookup"><span data-stu-id="69bcc-123">Serialization</span></span>|<span data-ttu-id="69bcc-124">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-124">Optional attribute.</span></span> <span data-ttu-id="69bcc-125">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="69bcc-125">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="69bcc-126">序列化</span><span class="sxs-lookup"><span data-stu-id="69bcc-126">Serialization</span></span>|<span data-ttu-id="69bcc-127">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-127">Optional attribute.</span></span> <span data-ttu-id="69bcc-128">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="69bcc-128">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="69bcc-129">序列化</span><span class="sxs-lookup"><span data-stu-id="69bcc-129">Serialization</span></span>|<span data-ttu-id="69bcc-130">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-130">Optional attribute.</span></span> <span data-ttu-id="69bcc-131">控制使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="69bcc-131">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="69bcc-132">序列化</span><span class="sxs-lookup"><span data-stu-id="69bcc-132">Serialization</span></span>|<span data-ttu-id="69bcc-133">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-133">Optional attribute.</span></span> <span data-ttu-id="69bcc-134">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="69bcc-134">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="69bcc-135">Interop</span><span class="sxs-lookup"><span data-stu-id="69bcc-135">Interop</span></span>|<span data-ttu-id="69bcc-136">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-136">Optional attribute.</span></span> <span data-ttu-id="69bcc-137">控制封送引用类型到 Windows 运行时和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="69bcc-137">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="69bcc-138">Interop</span><span class="sxs-lookup"><span data-stu-id="69bcc-138">Interop</span></span>|<span data-ttu-id="69bcc-139">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-139">Optional attribute.</span></span> <span data-ttu-id="69bcc-140">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="69bcc-140">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="69bcc-141">Interop</span><span class="sxs-lookup"><span data-stu-id="69bcc-141">Interop</span></span>|<span data-ttu-id="69bcc-142">可选特性。</span><span class="sxs-lookup"><span data-stu-id="69bcc-142">Optional attribute.</span></span> <span data-ttu-id="69bcc-143">控制封送结构到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="69bcc-143">Controls policy for marshaling structures to native code.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="69bcc-144">Name 特性</span><span class="sxs-lookup"><span data-stu-id="69bcc-144">Name attribute</span></span>  
  
|<span data-ttu-id="69bcc-145">值</span><span class="sxs-lookup"><span data-stu-id="69bcc-145">Value</span></span>|<span data-ttu-id="69bcc-146">描述</span><span class="sxs-lookup"><span data-stu-id="69bcc-146">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="69bcc-147">*namespace_name*</span><span class="sxs-lookup"><span data-stu-id="69bcc-147">*namespace_name*</span></span>|<span data-ttu-id="69bcc-148">命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="69bcc-148">The namespace name.</span></span> <span data-ttu-id="69bcc-149">如果 \<Namespace> 元素是 [\<Application>](application-element-net-native.md) 、或元素的子元素 [\<Library>](library-element-net-native.md) ，则 [\<Assembly>](assembly-element-net-native.md) *namespace_name* 必须是完全限定的命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="69bcc-149">If the \<Namespace> element is a child of an [\<Application>](application-element-net-native.md), [\<Library>](library-element-net-native.md), or [\<Assembly>](assembly-element-net-native.md) element, *namespace_name* must be a fully qualified namespace name.</span></span> <span data-ttu-id="69bcc-150">如果该 \<Namespace> 元素是另一个元素的子元素 \<Namespace> ，则 *namespace_name* 必须是相对的命名空间名称。</span><span class="sxs-lookup"><span data-stu-id="69bcc-150">If the \<Namespace> element is a child of another \<Namespace> element, *namespace_name* must be a relative namespace name.</span></span>|  
  
## <a name="all-other-attributes"></a><span data-ttu-id="69bcc-151">所有其他特性</span><span class="sxs-lookup"><span data-stu-id="69bcc-151">All other attributes</span></span>  
  
|<span data-ttu-id="69bcc-152">值</span><span class="sxs-lookup"><span data-stu-id="69bcc-152">Value</span></span>|<span data-ttu-id="69bcc-153">描述</span><span class="sxs-lookup"><span data-stu-id="69bcc-153">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="69bcc-154">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="69bcc-154">*policy_setting*</span></span>|<span data-ttu-id="69bcc-155">该设置将应用这个策略类型到该命名空间的所有类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-155">The setting to apply to this policy type for all types in the namespace.</span></span> <span data-ttu-id="69bcc-156">可能值为 `All`、`Auto`、`Excluded`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="69bcc-156">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="69bcc-157">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="69bcc-157">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="69bcc-158">子元素</span><span class="sxs-lookup"><span data-stu-id="69bcc-158">Child Elements</span></span>  
  
|<span data-ttu-id="69bcc-159">元素</span><span class="sxs-lookup"><span data-stu-id="69bcc-159">Element</span></span>|<span data-ttu-id="69bcc-160">描述</span><span class="sxs-lookup"><span data-stu-id="69bcc-160">Description</span></span>|  
|-------------|-----------------|  
|`<Namespace>`|<span data-ttu-id="69bcc-161">将运行时反射策略应用到一个父命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-161">Applies runtime reflection policy to all types in a parent namespace.</span></span>|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="69bcc-162">将反射策略应用到一个类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-162">Applies reflection policy to a type.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="69bcc-163">将反射策略应用到一个构造泛型类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-163">Applies reflection policy to a constructed generic type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="69bcc-164">父元素</span><span class="sxs-lookup"><span data-stu-id="69bcc-164">Parent Elements</span></span>  
  
|<span data-ttu-id="69bcc-165">元素</span><span class="sxs-lookup"><span data-stu-id="69bcc-165">Element</span></span>|<span data-ttu-id="69bcc-166">描述</span><span class="sxs-lookup"><span data-stu-id="69bcc-166">Description</span></span>|  
|-------------|-----------------|  
|[\<Application>](application-element-net-native.md)|<span data-ttu-id="69bcc-167">作为应用程序范围内的类型和元数据可以反应在运行时间的类型成员的容器而服务。</span><span class="sxs-lookup"><span data-stu-id="69bcc-167">Serves as a container for application-wide types and type members whose metadata is available for reflection at run time.</span></span> <span data-ttu-id="69bcc-168">[\<Application>](application-element-net-native.md)元素可以包含零个、一个或多个 [\<Assembly>](assembly-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="69bcc-168">The [\<Application>](application-element-net-native.md) element can have zero, one, or more [\<Assembly>](assembly-element-net-native.md) elements.</span></span>|  
|[\<Assembly>](assembly-element-net-native.md)|<span data-ttu-id="69bcc-169">将运行时反射策略应用到指定程序集中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-169">Applies runtime reflection policy to all the types in a specified assembly.</span></span>|  
|[\<Library>](library-element-net-native.md)|<span data-ttu-id="69bcc-170">定义包含元数据在运行时间可以用于反射的类型和类型成员的程序集。</span><span class="sxs-lookup"><span data-stu-id="69bcc-170">Defines the assembly that contains types and type members whose metadata is available for reflection at run time.</span></span> <span data-ttu-id="69bcc-171">[\<Library>](library-element-net-native.md)元素可以有零个或一个 [\<Assembly>](assembly-element-net-native.md) 元素。</span><span class="sxs-lookup"><span data-stu-id="69bcc-171">The [\<Library>](library-element-net-native.md) element can have zero or one [\<Assembly>](assembly-element-net-native.md) element.</span></span>|  
|`<Namespace>`|<span data-ttu-id="69bcc-172">将反射策略应用到一个父命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-172">Applies reflection policy to all types in a parent namespace.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="69bcc-173">备注</span><span class="sxs-lookup"><span data-stu-id="69bcc-173">Remarks</span></span>  

 <span data-ttu-id="69bcc-174">`Activate`、`Browse`、`Dynamic` 和 `Serialize` 特性都是可选项。</span><span class="sxs-lookup"><span data-stu-id="69bcc-174">The `Activate`, `Browse`, `Dynamic`, and `Serialize` attributes are all optional.</span></span> <span data-ttu-id="69bcc-175">如果这些都不存在，`<Namespace>` 元素仅会充当子元素的容器。</span><span class="sxs-lookup"><span data-stu-id="69bcc-175">If none are present, the `<Namespace>` element serves only as a container for child elements.</span></span> <span data-ttu-id="69bcc-176">如果它们存在，`<Namespace>` 元素会将运行时反射策略应用到一个指定的命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="69bcc-176">If they are present, the `<Namespace>` element applies runtime reflection policy to all the types in the specified namespace.</span></span>  
  
 <span data-ttu-id="69bcc-177">当它是元素的子元素时 [\<Assembly>](assembly-element-net-native.md) ， `<Namespace>` 元素将重写由元素定义的运行时反射策略  [\<Assembly>](assembly-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="69bcc-177">When it is a child of the [\<Assembly>](assembly-element-net-native.md) element, the `<Namespace>` element overrides the runtime reflection policy defined by the  [\<Assembly>](assembly-element-net-native.md) element.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69bcc-178">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69bcc-178">See also</span></span>

- [<span data-ttu-id="69bcc-179">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="69bcc-179">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
- [<span data-ttu-id="69bcc-180">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="69bcc-180">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="69bcc-181">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="69bcc-181">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
