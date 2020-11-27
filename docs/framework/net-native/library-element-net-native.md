---
title: <Library>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: f642276b-33fb-4a81-b882-8808c31ba69e
ms.openlocfilehash: aeaa6b1a9c3c4ceebdd0eab3f331a044971398bf
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96287912"
---
# <a name="library-element-net-native"></a><span data-ttu-id="caf81-102">\<Library>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="caf81-102">\<Library> Element (.NET Native)</span></span>

<span data-ttu-id="caf81-103">定义包含元数据在运行时间可以用于反射的类型和类型成员的程序集。</span><span class="sxs-lookup"><span data-stu-id="caf81-103">Defines the assembly that contains types and type members whose metadata is available for reflection at run time.</span></span>  
  
 <span data-ttu-id="caf81-104">\<Directives> 元素</span><span class="sxs-lookup"><span data-stu-id="caf81-104">\<Directives> Element</span></span>  
<span data-ttu-id="caf81-105">\<Library> 元素</span><span class="sxs-lookup"><span data-stu-id="caf81-105">\<Library> Element</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="caf81-106">语法</span><span class="sxs-lookup"><span data-stu-id="caf81-106">Syntax</span></span>  
  
```xml  
<Library Name="assembly_name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="caf81-107">特性和元素</span><span class="sxs-lookup"><span data-stu-id="caf81-107">Attributes and Elements</span></span>  

 <span data-ttu-id="caf81-108">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="caf81-108">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="caf81-109">特性</span><span class="sxs-lookup"><span data-stu-id="caf81-109">Attributes</span></span>  
  
|<span data-ttu-id="caf81-110">属性</span><span class="sxs-lookup"><span data-stu-id="caf81-110">Attribute</span></span>|<span data-ttu-id="caf81-111">描述</span><span class="sxs-lookup"><span data-stu-id="caf81-111">Description</span></span>|  
|---------------|-----------------|  
|`Name`|<span data-ttu-id="caf81-112">必需的特性。</span><span class="sxs-lookup"><span data-stu-id="caf81-112">Required attribute.</span></span> <span data-ttu-id="caf81-113">指定一个程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="caf81-113">Specifies the name of an assembly.</span></span> <span data-ttu-id="caf81-114">这个 `<Library>` 元素的子元素为在这个程序集中找到的类型和类型成员定义运行时反射策略。</span><span class="sxs-lookup"><span data-stu-id="caf81-114">Child elements of this `<Library>` element define the runtime reflection policy for types and type members found in this assembly.</span></span>|  
  
## <a name="name-attribute"></a><span data-ttu-id="caf81-115">Name 特性</span><span class="sxs-lookup"><span data-stu-id="caf81-115">Name attribute</span></span>  
  
|<span data-ttu-id="caf81-116">值</span><span class="sxs-lookup"><span data-stu-id="caf81-116">Value</span></span>|<span data-ttu-id="caf81-117">描述</span><span class="sxs-lookup"><span data-stu-id="caf81-117">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="caf81-118">assembly_name</span><span class="sxs-lookup"><span data-stu-id="caf81-118">*assembly_name*</span></span>|<span data-ttu-id="caf81-119">程序集的简单名称，不要包含文件扩展名。</span><span class="sxs-lookup"><span data-stu-id="caf81-119">The simple name of the assembly, without its file extension.</span></span> <span data-ttu-id="caf81-120">此特性对应 <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> 属性。</span><span class="sxs-lookup"><span data-stu-id="caf81-120">This attribute corresponds to the <xref:System.Reflection.AssemblyName.Name%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="caf81-121">例如，一个名为 Extensions.dll 的程序集的名称为“Extensions”。</span><span class="sxs-lookup"><span data-stu-id="caf81-121">For example, the name of an assembly named Extensions.dll is "Extensions".</span></span> <span data-ttu-id="caf81-122">参阅“备注”部分，了解支持对来自程序集的元数据有条件包含的 assembly_name 的一种特殊形式。</span><span class="sxs-lookup"><span data-stu-id="caf81-122">See the Remarks section for a special form of *assembly_name* that supports conditional inclusion of metadata from the assembly.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="caf81-123">子元素</span><span class="sxs-lookup"><span data-stu-id="caf81-123">Child Elements</span></span>  
  
|<span data-ttu-id="caf81-124">元素</span><span class="sxs-lookup"><span data-stu-id="caf81-124">Element</span></span>|<span data-ttu-id="caf81-125">描述</span><span class="sxs-lookup"><span data-stu-id="caf81-125">Description</span></span>|  
|-------------|-----------------|  
|[\<Assembly>](assembly-element-net-native.md)|<span data-ttu-id="caf81-126">将策略应用到特定程序集中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="caf81-126">Applies policy to all the types in a particular assembly.</span></span>|  
|[\<Namespace>](namespace-element-net-native.md)|<span data-ttu-id="caf81-127">将策略应用到特定命名空间中的所有类型。</span><span class="sxs-lookup"><span data-stu-id="caf81-127">Applies policy to all the types in a particular namespace.</span></span>|  
|[\<Type>](type-element-net-native.md)|<span data-ttu-id="caf81-128">将策略应用到一个特定类型，例如一个类或结构。</span><span class="sxs-lookup"><span data-stu-id="caf81-128">Applies policy to a particular type, such as a class or structure.</span></span>|  
|[\<TypeInstantiation>](typeinstantiation-element-net-native.md)|<span data-ttu-id="caf81-129">将策略应用到一个构造泛型类型。</span><span class="sxs-lookup"><span data-stu-id="caf81-129">Applies policy to a constructed generic type.</span></span> <span data-ttu-id="caf81-130">例如， [\<TypeInstantiation>](typeinstantiation-element-net-native.md) 元素可以用于定义类型的策略 `List<String>` 。</span><span class="sxs-lookup"><span data-stu-id="caf81-130">For example, a [\<TypeInstantiation>](typeinstantiation-element-net-native.md) element could be used to define policy for a `List<String>` type.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="caf81-131">父元素</span><span class="sxs-lookup"><span data-stu-id="caf81-131">Parent Elements</span></span>  
  
|<span data-ttu-id="caf81-132">元素</span><span class="sxs-lookup"><span data-stu-id="caf81-132">Element</span></span>|<span data-ttu-id="caf81-133">描述</span><span class="sxs-lookup"><span data-stu-id="caf81-133">Description</span></span>|  
|-------------|-----------------|  
|[\<Directives>](directives-element-net-native.md)|<span data-ttu-id="caf81-134">运行时指令文件的根元素。</span><span class="sxs-lookup"><span data-stu-id="caf81-134">The root element of a runtime directives file.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="caf81-135">备注</span><span class="sxs-lookup"><span data-stu-id="caf81-135">Remarks</span></span>  

 <span data-ttu-id="caf81-136">[\<Directives>](directives-element-net-native.md)元素可以包含零个、一个或多个 `<Library>` 元素。</span><span class="sxs-lookup"><span data-stu-id="caf81-136">The [\<Directives>](directives-element-net-native.md) element can contain zero, one, or more `<Library>` elements.</span></span>  
  
 <span data-ttu-id="caf81-137">`<Library>` 元素充当容器，用来定义其元数据在运行时间需要存在的程序元素；此元素不表示策略。</span><span class="sxs-lookup"><span data-stu-id="caf81-137">The `<Library>` element serves as a container to define the program elements whose metadata is needed at run time; this element doesn't express policy.</span></span> <span data-ttu-id="caf81-138">在编译时间，编译器工具仅搜索由 `<Library>` 元素指定的库，以查找其子元素识别出的程序元素。</span><span class="sxs-lookup"><span data-stu-id="caf81-138">At compile time, compiler tools search only the library designated by the `<Library>` element for program elements identified by its child elements.</span></span> <span data-ttu-id="caf81-139">与此相反，编译器工具会搜索所有库，including.NET Framework core 库，适用于元素的子元素标识的程序元素 [\<Application>](application-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="caf81-139">In contrast, compiler tools search all libraries, including.NET Framework core libraries, for program elements identified by child elements of the [\<Application>](application-element-net-native.md) element.</span></span>  
  
 <span data-ttu-id="caf81-140">`<Library>` 指令可以有条件地使用。</span><span class="sxs-lookup"><span data-stu-id="caf81-140">`<Library>` directives may be conditionally utilized.</span></span> <span data-ttu-id="caf81-141">如果元素的名称以 `<Library>` 星号 () 的开头和结尾 \* ，则 `<Library>` 只有当应用程序引用星号之间指定的程序集时，指令才会生效。</span><span class="sxs-lookup"><span data-stu-id="caf81-141">If the name of the `<Library>` element starts and ends with an asterisk (\*), the `<Library>` directive has an effect only if the assembly specified between the asterisks is referenced by the app.</span></span> <span data-ttu-id="caf81-142">例如，仅当应用引用 Utilities.dll 程序集时，以下运行时指令才适用。</span><span class="sxs-lookup"><span data-stu-id="caf81-142">For example, the following runtime directive applies only if the Utilities.dll assembly is referenced by the app.</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
  <Library Name="*Utilities*">  
   ...  
  </Library>  
</Directives>  
```  
  
## <a name="see-also"></a><span data-ttu-id="caf81-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="caf81-143">See also</span></span>

- [<span data-ttu-id="caf81-144">\<Application> 元素</span><span class="sxs-lookup"><span data-stu-id="caf81-144">\<Application> Element</span></span>](application-element-net-native.md)
- [<span data-ttu-id="caf81-145">\<Directives> 元素</span><span class="sxs-lookup"><span data-stu-id="caf81-145">\<Directives> Element</span></span>](directives-element-net-native.md)
- [<span data-ttu-id="caf81-146">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="caf81-146">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="caf81-147">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="caf81-147">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
