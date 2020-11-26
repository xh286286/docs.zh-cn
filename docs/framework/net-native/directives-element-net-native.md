---
title: <Directives>元素 (.NET Native)
ms.date: 03/30/2017
ms.assetid: 444846f3-48d5-4341-a43e-69f7221389eb
ms.openlocfilehash: 524c30872e218f6428491507bbfb4ca54b6061b1
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96251095"
---
# <a name="directives-element-net-native"></a><span data-ttu-id="eed33-102">\<Directives>元素 (.NET Native)</span><span class="sxs-lookup"><span data-stu-id="eed33-102">\<Directives> Element (.NET Native)</span></span>

<span data-ttu-id="eed33-103">.NET Native 的每个运行时指令文件中的根元素。</span><span class="sxs-lookup"><span data-stu-id="eed33-103">The root element in every runtime directives file for .NET Native.</span></span>  
  
 `<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">`
  
## <a name="syntax"></a><span data-ttu-id="eed33-104">语法</span><span class="sxs-lookup"><span data-stu-id="eed33-104">Syntax</span></span>  
  
```xml  
<Directives xmlns="http://schemas.microsoft.com/netfx/2013/01/metadata">  
   <!-- child elements -->
</Directives>  
```  
  
## <a name="attributes"></a><span data-ttu-id="eed33-105">特性</span><span class="sxs-lookup"><span data-stu-id="eed33-105">Attributes</span></span>  
  
|<span data-ttu-id="eed33-106">属性</span><span class="sxs-lookup"><span data-stu-id="eed33-106">Attribute</span></span>|<span data-ttu-id="eed33-107">描述</span><span class="sxs-lookup"><span data-stu-id="eed33-107">Description</span></span>|  
|---------------|-----------------|  
|`xmlns`|<span data-ttu-id="eed33-108">XML 命名空间。</span><span class="sxs-lookup"><span data-stu-id="eed33-108">The XML namespace.</span></span> <span data-ttu-id="eed33-109">其值始终为 `http://schemas.microsoft.com/netfx/2013/01/metadata` 。</span><span class="sxs-lookup"><span data-stu-id="eed33-109">Its value is always `http://schemas.microsoft.com/netfx/2013/01/metadata`.</span></span>|  
  
## <a name="child-elements"></a><span data-ttu-id="eed33-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eed33-110">Child elements</span></span>  
  
|<span data-ttu-id="eed33-111">元素</span><span class="sxs-lookup"><span data-stu-id="eed33-111">Element</span></span>|<span data-ttu-id="eed33-112">描述</span><span class="sxs-lookup"><span data-stu-id="eed33-112">Description</span></span>|  
|-------------|-----------------|  
|[\<Application>](application-element-net-native.md)|<span data-ttu-id="eed33-113">作为应用程序范围内的类型和其元数据可以用于反射的类型成员的容器而服务。</span><span class="sxs-lookup"><span data-stu-id="eed33-113">Serves as a container for application-wide types and type members whose metadata is available for reflection.</span></span>|  
|[\<Library>](library-element-net-native.md)|<span data-ttu-id="eed33-114">定义那些子类型和类型成员在运行时间要求元数据的程序集。</span><span class="sxs-lookup"><span data-stu-id="eed33-114">Defines the assembly whose child types and type members require metadata at run time.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eed33-115">备注</span><span class="sxs-lookup"><span data-stu-id="eed33-115">Remarks</span></span>  

 <span data-ttu-id="eed33-116">每个运行时指令文件都可以只包含一个 `<Directives>` 元素。</span><span class="sxs-lookup"><span data-stu-id="eed33-116">Each runtime directives file can contain only one `<Directives>` element.</span></span>  
  
 <span data-ttu-id="eed33-117">`<Directives>`元素可以包含零个或一个 [\<Application>](application-element-net-native.md) 元素，以及零个、一个或多个元素 [\<Library>](library-element-net-native.md) 。</span><span class="sxs-lookup"><span data-stu-id="eed33-117">The `<Directives>` element can contain zero or one [\<Application>](application-element-net-native.md) element, and zero, one, or more [\<Library>](library-element-net-native.md) elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eed33-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eed33-118">See also</span></span>

- [<span data-ttu-id="eed33-119">运行时指令 (rd.xml) 配置文件引用</span><span class="sxs-lookup"><span data-stu-id="eed33-119">Runtime Directives (rd.xml) Configuration File Reference</span></span>](runtime-directives-rd-xml-configuration-file-reference.md)
- [<span data-ttu-id="eed33-120">运行时指令元素</span><span class="sxs-lookup"><span data-stu-id="eed33-120">Runtime Directive Elements</span></span>](runtime-directive-elements.md)
