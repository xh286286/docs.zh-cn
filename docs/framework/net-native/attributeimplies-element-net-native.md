---
title: <AttributeImplies>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 82db7193-a860-418b-84fc-fff2fdf2e025
ms.openlocfilehash: 4171345bb5337436142128623abc7d183c4477ff
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96288107"
---
# <a name="attributeimplies-element-net-native"></a><span data-ttu-id="24378-102">\<AttributeImplies>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="24378-102">\<AttributeImplies> Element (.NET Native)</span></span>

<span data-ttu-id="24378-103">为包含特性应用的代码元素定义策略。</span><span class="sxs-lookup"><span data-stu-id="24378-103">Defines policy for code elements the containing attribute is applied to.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24378-104">语法</span><span class="sxs-lookup"><span data-stu-id="24378-104">Syntax</span></span>  
  
```xml  
<AttributeImplies Activate="policy_type"  
                  Browse="policy_type"  
                  Dynamic="policy_type"  
                  Serialize="policy_type"
                  DataContractSerializer="policy_setting"  
                  DataContractJsonSerializer="policy_setting"  
                  XmlSerializer="policy_setting"  
                  MarshalObject="policy_setting"  
                  MarshalDelegate="policy_setting"  
                  MarshalStructure="policy_setting" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="24378-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="24378-105">Attributes and Elements</span></span>  

 <span data-ttu-id="24378-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="24378-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="24378-107">特性</span><span class="sxs-lookup"><span data-stu-id="24378-107">Attributes</span></span>  
  
|<span data-ttu-id="24378-108">属性</span><span class="sxs-lookup"><span data-stu-id="24378-108">Attribute</span></span>|<span data-ttu-id="24378-109">属性类型</span><span class="sxs-lookup"><span data-stu-id="24378-109">Attribute type</span></span>|<span data-ttu-id="24378-110">描述</span><span class="sxs-lookup"><span data-stu-id="24378-110">Description</span></span>|  
|---------------|--------------------|-----------------|  
|`Activate`|<span data-ttu-id="24378-111">反射</span><span class="sxs-lookup"><span data-stu-id="24378-111">Reflection</span></span>|<span data-ttu-id="24378-112">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-112">Optional attribute.</span></span> <span data-ttu-id="24378-113">控制运行时对构造函数的访问，以启用实例激活。</span><span class="sxs-lookup"><span data-stu-id="24378-113">Controls runtime access to constructors to enable activation of instances.</span></span>|  
|`Browse`|<span data-ttu-id="24378-114">反射</span><span class="sxs-lookup"><span data-stu-id="24378-114">Reflection</span></span>|<span data-ttu-id="24378-115">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-115">Optional attribute.</span></span> <span data-ttu-id="24378-116">控制对有关程序元素信息的查询，但并不启用任何运行时访问。</span><span class="sxs-lookup"><span data-stu-id="24378-116">Controls querying for information about program elements, but does not enable any runtime access.</span></span>|  
|`Dynamic`|<span data-ttu-id="24378-117">反射</span><span class="sxs-lookup"><span data-stu-id="24378-117">Reflection</span></span>|<span data-ttu-id="24378-118">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-118">Optional attribute.</span></span> <span data-ttu-id="24378-119">控制运行时对所有类型成员的访问，包括构造函数、方法、字段、属性和事件，以启用动态编程。</span><span class="sxs-lookup"><span data-stu-id="24378-119">Controls runtime access to all type members, including constructors, methods, fields, properties, and events, to enable dynamic programming.</span></span>|  
|`Serialize`|<span data-ttu-id="24378-120">序列化</span><span class="sxs-lookup"><span data-stu-id="24378-120">Serialization</span></span>|<span data-ttu-id="24378-121">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-121">Optional attribute.</span></span> <span data-ttu-id="24378-122">控制运行时对构造函数、字段和属性的访问，使类型实例得到序列化和反序列化处理，这是通过库进行的，例如 Newtonsoft JSON 序列化程序。</span><span class="sxs-lookup"><span data-stu-id="24378-122">Controls runtime access to constructors, fields, and properties, to enable type instances to be serialized and deserialized by libraries such as the Newtonsoft JSON serializer.</span></span>|  
|`DataContractSerializer`|<span data-ttu-id="24378-123">序列化</span><span class="sxs-lookup"><span data-stu-id="24378-123">Serialization</span></span>|<span data-ttu-id="24378-124">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-124">Optional attribute.</span></span> <span data-ttu-id="24378-125">控制使用 <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> 类的序列化策略。</span><span class="sxs-lookup"><span data-stu-id="24378-125">Controls policy for serialization that uses the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType> class.</span></span>|  
|`DataContractJsonSerializer`|<span data-ttu-id="24378-126">序列化</span><span class="sxs-lookup"><span data-stu-id="24378-126">Serialization</span></span>|<span data-ttu-id="24378-127">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-127">Optional attribute.</span></span> <span data-ttu-id="24378-128">控制使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> 类的 JSON 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="24378-128">Controls policy for JSON serialization that uses the <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType> class.</span></span>|  
|`XmlSerializer`|<span data-ttu-id="24378-129">序列化</span><span class="sxs-lookup"><span data-stu-id="24378-129">Serialization</span></span>|<span data-ttu-id="24378-130">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-130">Optional attribute.</span></span> <span data-ttu-id="24378-131">控制使用 <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> 类的 XML 序列化策略。</span><span class="sxs-lookup"><span data-stu-id="24378-131">Controls policy for XML serialization that uses the <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType> class.</span></span>|  
|`MarshalObject`|<span data-ttu-id="24378-132">Interop</span><span class="sxs-lookup"><span data-stu-id="24378-132">Interop</span></span>|<span data-ttu-id="24378-133">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-133">Optional attribute.</span></span> <span data-ttu-id="24378-134">控制封送引用类型到 Windows 运行时和 COM 的策略。</span><span class="sxs-lookup"><span data-stu-id="24378-134">Controls policy for marshaling reference types to Windows Runtime and COM.</span></span>|  
|`MarshalDelegate`|<span data-ttu-id="24378-135">Interop</span><span class="sxs-lookup"><span data-stu-id="24378-135">Interop</span></span>|<span data-ttu-id="24378-136">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-136">Optional attribute.</span></span> <span data-ttu-id="24378-137">控制将委托类型作为函数指针封送到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="24378-137">Controls policy for marshaling delegate types as function pointers to native code.</span></span>|  
|`MarshalStructure`|<span data-ttu-id="24378-138">Interop</span><span class="sxs-lookup"><span data-stu-id="24378-138">Interop</span></span>|<span data-ttu-id="24378-139">可选特性。</span><span class="sxs-lookup"><span data-stu-id="24378-139">Optional attribute.</span></span> <span data-ttu-id="24378-140">控制封送处理值类型到本机代码的策略。</span><span class="sxs-lookup"><span data-stu-id="24378-140">Controls policy for marshaling value types to native code.</span></span>|  
  
## <a name="all-attributes"></a><span data-ttu-id="24378-141">所有特性</span><span class="sxs-lookup"><span data-stu-id="24378-141">All attributes</span></span>  
  
|<span data-ttu-id="24378-142">值</span><span class="sxs-lookup"><span data-stu-id="24378-142">Value</span></span>|<span data-ttu-id="24378-143">描述</span><span class="sxs-lookup"><span data-stu-id="24378-143">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="24378-144">*策略_设置*</span><span class="sxs-lookup"><span data-stu-id="24378-144">*policy_setting*</span></span>|<span data-ttu-id="24378-145">该设置将应用到这种策略类型。</span><span class="sxs-lookup"><span data-stu-id="24378-145">The setting to apply to this policy type.</span></span> <span data-ttu-id="24378-146">可能值为 `All`、`Auto`、`Excluded`、`Public`、`PublicAndInternal`、`Required Public`、`Required PublicAndInternal` 以及 `Required All`。</span><span class="sxs-lookup"><span data-stu-id="24378-146">Possible values are `All`, `Auto`, `Excluded`, `Public`, `PublicAndInternal`, `Required Public`, `Required PublicAndInternal`, and `Required All`.</span></span> <span data-ttu-id="24378-147">有关详细信息，请参阅[运行时指令策略设置](runtime-directive-policy-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="24378-147">For more information, see [Runtime Directive Policy Settings](runtime-directive-policy-settings.md).</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="24378-148">子元素</span><span class="sxs-lookup"><span data-stu-id="24378-148">Child Elements</span></span>  

 <span data-ttu-id="24378-149">无。</span><span class="sxs-lookup"><span data-stu-id="24378-149">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="24378-150">父元素</span><span class="sxs-lookup"><span data-stu-id="24378-150">Parent Elements</span></span>  
  
|<span data-ttu-id="24378-151">元素</span><span class="sxs-lookup"><span data-stu-id="24378-151">Element</span></span>|<span data-ttu-id="24378-152">描述</span><span class="sxs-lookup"><span data-stu-id="24378-152">Description</span></span>|  
|-------------|-----------------|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="24378-153">将反射策略应用到一种类型及其所有成员。</span><span class="sxs-lookup"><span data-stu-id="24378-153">Applies reflection policy to a type and all its members.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="24378-154">备注</span><span class="sxs-lookup"><span data-stu-id="24378-154">Remarks</span></span>  

 <span data-ttu-id="24378-155">如果它的包含类型是一个特性（即，从 `<AttributeImplies>` 中派生出的一个类），则使用 <xref:System.Attribute?displayProperty=nameWithType> 元素。</span><span class="sxs-lookup"><span data-stu-id="24378-155">The `<AttributeImplies>` element is used if its containing type is an attribute (that is, a class derived from <xref:System.Attribute?displayProperty=nameWithType>).</span></span> <span data-ttu-id="24378-156">如果该特性被应用到特定的程序元素，由 `<AttributeImplies>` 元素定义的策略将应用到该程序元素。</span><span class="sxs-lookup"><span data-stu-id="24378-156">If the attribute is applied to a particular program element, the policy defined by the `<AttributeImplies>` element applies to that program element.</span></span>  
  
 <span data-ttu-id="24378-157">反射、序列化和互操作特性都是可选项，但必须存在至少一项。</span><span class="sxs-lookup"><span data-stu-id="24378-157">The reflection, serialization, and interop attributes are all optional, although at least one should be present.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24378-158">请参阅</span><span class="sxs-lookup"><span data-stu-id="24378-158">See also</span></span>

- [<span data-ttu-id="24378-159">\<Type> 元素</span><span class="sxs-lookup"><span data-stu-id="24378-159">\<Type> Element</span></span>](type-element-net-native.md)
- [<span data-ttu-id="24378-160">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="24378-160">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="24378-161">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="24378-161">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
- [<span data-ttu-id="24378-162">运行时指令策略设置</span><span class="sxs-lookup"><span data-stu-id="24378-162">Runtime Directive Policy Settings</span></span>](runtime-directive-policy-settings.md)
