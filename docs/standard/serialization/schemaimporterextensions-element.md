---
title: <schemaImporterExtensions> 元素
description: <schemaImporterExtensions> 元素包含将 XSD 类型映射到 .NET 类型时 XmlSchemaImporter 所用的类型。
ms.date: 03/30/2017
helpviewer_keywords:
- XML serialization, configuration
- schemaImporterExtensions element
- <schemaImporterExtensions> element
ms.assetid: 465ef2a0-f909-4ac1-9a56-0ead5c849698
ms.openlocfilehash: 6b644ed1112b748be4dd301d6fa6f2a6416dc67e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95722136"
---
# <a name="schemaimporterextensions-element"></a><span data-ttu-id="9ffa4-103">\<schemaImporterExtensions> 元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-103">\<schemaImporterExtensions> element</span></span>

<span data-ttu-id="9ffa4-104">包含将 XSD 类型映射到 .NET 类型时 <xref:System.Xml.Serialization.XmlSchemaImporter> 所用的类型。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-104">Contains types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> for mapping of XSD types to .NET types.</span></span> <span data-ttu-id="9ffa4-105">有关配置文件的详细信息，请参阅[配置文件架构](../../framework/configure-apps/file-schema/index.md)。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-105">For more information about configuration files, see [Configuration File Schema](../../framework/configure-apps/file-schema/index.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9ffa4-106">语法</span><span class="sxs-lookup"><span data-stu-id="9ffa4-106">Syntax</span></span>  
  
```xml  
<schemaImporterExtensions>  
    <!-- Add types -->  
</schemaImporterExtensions>  
```  
  
## <a name="child-elements"></a><span data-ttu-id="9ffa4-107">子元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-107">Child Elements</span></span>  
  
|<span data-ttu-id="9ffa4-108">元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-108">Element</span></span>|<span data-ttu-id="9ffa4-109">描述</span><span class="sxs-lookup"><span data-stu-id="9ffa4-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="9ffa4-110">[\<add> 的 \<schemaImporterExtensions>](add-element-for-schemaimporterextensions.md) 元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-110">[\<add> Element for \<schemaImporterExtensions>](add-element-for-schemaimporterextensions.md)</span></span>|<span data-ttu-id="9ffa4-111">添加 <xref:System.Xml.Serialization.XmlSchemaImporter> 用来创建映射的类型。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-111">Adds types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> to create mappings.</span></span>|  
  
## <a name="parent-elements"></a><span data-ttu-id="9ffa4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-112">Parent Elements</span></span>  
  
|<span data-ttu-id="9ffa4-113">元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-113">Element</span></span>|<span data-ttu-id="9ffa4-114">描述</span><span class="sxs-lookup"><span data-stu-id="9ffa4-114">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="9ffa4-115">\<system.xml.serialization> 元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-115">\<system.xml.serialization> Element</span></span>](system-xml-serialization-element.md)|<span data-ttu-id="9ffa4-116">用于控制 XML 序列化的顶级元素。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-116">The top-level element for controlling XML serialization.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9ffa4-117">示例</span><span class="sxs-lookup"><span data-stu-id="9ffa4-117">Example</span></span>  

 <span data-ttu-id="9ffa4-118">下面的代码示例演示如何添加将 XSD 类型映射到 .NET 类型时 <xref:System.Xml.Serialization.XmlSchemaImporter> 所用的类型。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-118">The following code example illustrates how to add types that are used by the <xref:System.Xml.Serialization.XmlSchemaImporter> when mapping XSD types to .NET types.</span></span>  
  
```xml  
<system.xml.serialization>  
    <schemaImporterExtensions>  
        <add name = "MobileCapabilities" type =
        "System.Web.Mobile.MobileCapabilities,
        System.Web.Mobile, Version - 2.0.0.0, Culture = neutral,
        PublicKeyToken = b03f5f6f11d40a3a" />  
    </schemaImporterExtensions>  
</system.xml.serialization>  
```  
  
## <a name="see-also"></a><span data-ttu-id="9ffa4-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ffa4-119">See also</span></span>

- <xref:System.Xml.Serialization.XmlSchemaImporter>
- <xref:System.Xml.Serialization.Configuration.DateTimeSerializationSection.DateTimeSerializationMode>
- [<span data-ttu-id="9ffa4-120">配置文件架构</span><span class="sxs-lookup"><span data-stu-id="9ffa4-120">Configuration File Schema</span></span>](../../framework/configure-apps/file-schema/index.md)
- [<span data-ttu-id="9ffa4-121">\<dateTimeSerialization> 元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-121">\<dateTimeSerialization> Element</span></span>](datetimeserialization-element.md)
- <span data-ttu-id="9ffa4-122">[\<add> 的 \<schemaImporterExtensions>](add-element-for-schemaimporterextensions.md) 元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-122">[\<add> Element for \<schemaImporterExtensions>](add-element-for-schemaimporterextensions.md)</span></span>
- [<span data-ttu-id="9ffa4-123">\<system.xml.serialization> 元素</span><span class="sxs-lookup"><span data-stu-id="9ffa4-123">\<system.xml.serialization> Element</span></span>](system-xml-serialization-element.md)
