---
title: 序列化
ms.date: 10/22/2008
ms.assetid: bebb27ac-9712-4196-9931-de19fc04dbac
ms.openlocfilehash: 58ed937df5b60daf9fcbcb7610d6026c5e9805fc
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95730924"
---
# <a name="serialization"></a><span data-ttu-id="ed15e-102">序列化</span><span class="sxs-lookup"><span data-stu-id="ed15e-102">Serialization</span></span>

<span data-ttu-id="ed15e-103">序列化是指将对象转换为可随时保存或传输的格式的过程。</span><span class="sxs-lookup"><span data-stu-id="ed15e-103">Serialization is the process of converting an object into a format that can be readily persisted or transported.</span></span> <span data-ttu-id="ed15e-104">例如，可以序列化对象，使用 HTTP 在 Internet 上传输该对象，并在目标计算机上对其进行反序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-104">For example, you can serialize an object, transport it over the Internet using HTTP, and deserialized it at the destination machine.</span></span>

 <span data-ttu-id="ed15e-105">.NET Framework 提供了针对各种序列化方案进行优化的三种主要序列化技术。</span><span class="sxs-lookup"><span data-stu-id="ed15e-105">The .NET Framework offers three main serialization technologies optimized for various serialization scenarios.</span></span> <span data-ttu-id="ed15e-106">下表列出了这些技术以及与这些技术相关的主要 Framework 类型。</span><span class="sxs-lookup"><span data-stu-id="ed15e-106">The following table lists these technologies and the main Framework types related to these technologies.</span></span>

|<span data-ttu-id="ed15e-107">**技术名称**</span><span class="sxs-lookup"><span data-stu-id="ed15e-107">**Technology Name**</span></span>|<span data-ttu-id="ed15e-108">**主要类型**</span><span class="sxs-lookup"><span data-stu-id="ed15e-108">**Main Types**</span></span>|<span data-ttu-id="ed15e-109">**方案**</span><span class="sxs-lookup"><span data-stu-id="ed15e-109">**Scenarios**</span></span>|
|-------------------------|--------------------|-------------------|
|<span data-ttu-id="ed15e-110">**数据协定序列化**</span><span class="sxs-lookup"><span data-stu-id="ed15e-110">**Data Contract Serialization**</span></span>|<xref:System.Runtime.Serialization.DataContractAttribute> <br /> <xref:System.Runtime.Serialization.DataMemberAttribute> <br /> <xref:System.Runtime.Serialization.DataContractSerializer> <br /> <xref:System.Runtime.Serialization.NetDataContractSerializer> <br /> <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> <br /> <xref:System.Runtime.Serialization.ISerializable>|<span data-ttu-id="ed15e-111">常规持久性</span><span class="sxs-lookup"><span data-stu-id="ed15e-111">General persistence</span></span><br /><span data-ttu-id="ed15e-112">Web 服务</span><span class="sxs-lookup"><span data-stu-id="ed15e-112">Web Services</span></span><br /><span data-ttu-id="ed15e-113">JSON</span><span class="sxs-lookup"><span data-stu-id="ed15e-113">JSON</span></span>|
|<span data-ttu-id="ed15e-114">**XML 序列化**</span><span class="sxs-lookup"><span data-stu-id="ed15e-114">**XML Serialization**</span></span>|<xref:System.Xml.Serialization.XmlSerializer>|<span data-ttu-id="ed15e-115">对 XML 形状具有完全控制的 XML 格式</span><span class="sxs-lookup"><span data-stu-id="ed15e-115">XML format with full control over the shape of the XML</span></span>|
|<span data-ttu-id="ed15e-116">**二进制 (和 SOAP) 的运行时序列化**</span><span class="sxs-lookup"><span data-stu-id="ed15e-116">**Runtime Serialization (Binary and SOAP)**</span></span>|<xref:System.SerializableAttribute> <br /> <xref:System.Runtime.Serialization.ISerializable> <br /> <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> <br /> <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter>|<span data-ttu-id="ed15e-117">.NET 远程处理</span><span class="sxs-lookup"><span data-stu-id="ed15e-117">.NET Remoting</span></span>|

 <span data-ttu-id="ed15e-118">✔️在设计新类型时要考虑序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-118">✔️ DO think about serialization when you design new types.</span></span>

## <a name="choosing-the-right-serialization-technology-to-support"></a><span data-ttu-id="ed15e-119">选择要支持的合适的序列化技术</span><span class="sxs-lookup"><span data-stu-id="ed15e-119">Choosing the Right Serialization Technology to Support</span></span>

 <span data-ttu-id="ed15e-120">✔️如果可能需要在 Web 服务中保留或使用类型的实例，则应考虑支持数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-120">✔️ CONSIDER supporting Data Contract Serialization if instances of your type might need to be persisted or used in Web Services.</span></span>

 <span data-ttu-id="ed15e-121">如果需要对序列化类型时生成的 XML 格式进行更好的控制，✔️应考虑支持 XML 序列化，而不是或除了数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-121">✔️ CONSIDER supporting the XML Serialization instead of or in addition to Data Contract Serialization if you need more control over the XML format that is produced when the type is serialized.</span></span>

 <span data-ttu-id="ed15e-122">有些互操作性方案中可能需要使用数据协定序列化不支持的 XML 构造，例如，生成 XML 属性。</span><span class="sxs-lookup"><span data-stu-id="ed15e-122">This may be necessary in some interoperability scenarios where you need to use an XML construct that is not supported by Data Contract Serialization, for example, to produce XML attributes.</span></span>

 <span data-ttu-id="ed15e-123">✔️如果您的类型的实例需要跨 .NET 远程处理边界传递，则应考虑支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-123">✔️ CONSIDER supporting the Runtime Serialization if instances of your type need to travel across .NET Remoting boundaries.</span></span>

 <span data-ttu-id="ed15e-124">❌ 出于一般持久性原因，请避免仅支持运行时序列化或 XML 序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-124">❌ AVOID supporting Runtime Serialization or XML Serialization just for general persistence reasons.</span></span> <span data-ttu-id="ed15e-125">改用数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-125">Prefer Data Contract Serialization instead.</span></span>

## <a name="supporting-data-contract-serialization"></a><span data-ttu-id="ed15e-126">支持数据协定序列化</span><span class="sxs-lookup"><span data-stu-id="ed15e-126">Supporting Data Contract Serialization</span></span>

 <span data-ttu-id="ed15e-127">类型可通过将应用 <xref:System.Runtime.Serialization.DataContractAttribute> 到类型，并将应用到类型 <xref:System.Runtime.Serialization.DataMemberAttribute> (字段和属性) 的成员，从而支持数据协定序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-127">Types can support Data Contract Serialization by applying the <xref:System.Runtime.Serialization.DataContractAttribute> to the type and the <xref:System.Runtime.Serialization.DataMemberAttribute> to the members (fields and properties) of the type.</span></span>

 <span data-ttu-id="ed15e-128">如果类型可用于部分信任，✔️考虑将类型为 public 的数据成员标记为公共。</span><span class="sxs-lookup"><span data-stu-id="ed15e-128">✔️ CONSIDER marking data members of your type public if the type can be used in partial trust.</span></span>

 <span data-ttu-id="ed15e-129">在完全信任中，数据协定序列化程序可以序列化和反序列化非公共类型和成员，但在部分信任环境中只能序列化和反序列化公共成员。</span><span class="sxs-lookup"><span data-stu-id="ed15e-129">In full trust, Data Contract serializers can serialize and deserialize nonpublic types and members, but only public members can be serialized and deserialized in partial trust.</span></span>

 <span data-ttu-id="ed15e-130">✔️对具有的所有属性实现 getter 和 setter <xref:System.Runtime.Serialization.DataMemberAttribute> 。</span><span class="sxs-lookup"><span data-stu-id="ed15e-130">✔️ DO implement a getter and setter on all properties that have <xref:System.Runtime.Serialization.DataMemberAttribute>.</span></span> <span data-ttu-id="ed15e-131">数据协定序列化程序需要将类型的 getter 和 setter 视为可序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-131">Data Contract serializers require both the getter and the setter for the type to be considered serializable.</span></span> <span data-ttu-id="ed15e-132"> (在 .NET Framework 3.5 SP1 中，某些集合属性可以是只能获取的 ) 。如果在部分信任环境中不使用该类型，则属性访问器中的一个或两个属性访问器都可以是非公共的。</span><span class="sxs-lookup"><span data-stu-id="ed15e-132">(In .NET Framework 3.5 SP1, some collection properties can be get-only.) If the type won’t be used in partial trust, one or both of the property accessors can be nonpublic.</span></span>

 <span data-ttu-id="ed15e-133">✔️考虑使用序列化回调来初始化已反序列化的实例。</span><span class="sxs-lookup"><span data-stu-id="ed15e-133">✔️ CONSIDER using the serialization callbacks for initialization of deserialized instances.</span></span>

 <span data-ttu-id="ed15e-134">反序列化对象时，不调用任何构造函数。</span><span class="sxs-lookup"><span data-stu-id="ed15e-134">Constructors are not called when objects are deserialized.</span></span> <span data-ttu-id="ed15e-135"> (规则有一些例外。</span><span class="sxs-lookup"><span data-stu-id="ed15e-135">(There are exceptions to the rule.</span></span> <span data-ttu-id="ed15e-136">在反序列化期间调用标记为的集合的构造函数 <xref:System.Runtime.Serialization.CollectionDataContractAttribute> 。 ) 因此，在正常构造期间执行的任何逻辑都需要作为一个序列化回调实现。</span><span class="sxs-lookup"><span data-stu-id="ed15e-136">Constructors of collections marked with <xref:System.Runtime.Serialization.CollectionDataContractAttribute> are called during deserialization.) Therefore, any logic that executes during normal construction needs to be implemented as one of the serialization callbacks.</span></span>

 <span data-ttu-id="ed15e-137">`OnDeserializedAttribute` 是最常用的回调特性。</span><span class="sxs-lookup"><span data-stu-id="ed15e-137">`OnDeserializedAttribute` is the most commonly used callback attribute.</span></span> <span data-ttu-id="ed15e-138">此系列中的其他属性还有 <xref:System.Runtime.Serialization.OnDeserializingAttribute>、<xref:System.Runtime.Serialization.OnSerializingAttribute> 和 <xref:System.Runtime.Serialization.OnSerializedAttribute>。</span><span class="sxs-lookup"><span data-stu-id="ed15e-138">The other attributes in the family are <xref:System.Runtime.Serialization.OnDeserializingAttribute>,  <xref:System.Runtime.Serialization.OnSerializingAttribute>, and <xref:System.Runtime.Serialization.OnSerializedAttribute>.</span></span> <span data-ttu-id="ed15e-139">这些属性可分别用来标记在反序列化之前、序列化之前以及序列化之后执行的回调。</span><span class="sxs-lookup"><span data-stu-id="ed15e-139">They can be used to mark callbacks that get executed before deserialization, before serialization, and finally, after serialization, respectively.</span></span>

 <span data-ttu-id="ed15e-140">✔️考虑使用 <xref:System.Runtime.Serialization.KnownTypeAttribute> 来指示在反序列化复杂对象图时应使用的具体类型。</span><span class="sxs-lookup"><span data-stu-id="ed15e-140">✔️ CONSIDER using the <xref:System.Runtime.Serialization.KnownTypeAttribute> to indicate concrete types that should be used when deserializing a complex object graph.</span></span>

 <span data-ttu-id="ed15e-141">✔️在创建或更改可序列化类型时，请考虑向后和向前兼容性。</span><span class="sxs-lookup"><span data-stu-id="ed15e-141">✔️ DO consider backward and forward compatibility when creating or changing serializable types.</span></span>

 <span data-ttu-id="ed15e-142">请记住，类型的未来版本的序列化流可反序列化到类型的当前版本，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="ed15e-142">Keep in mind that serialized streams of future versions of your type can be deserialized into the current version of the type, and vice versa.</span></span>

 <span data-ttu-id="ed15e-143">请确保您了解到数据成员（甚至是私有的和内部的）在该类型的未来版本中不能更改其名称、类型甚至顺序，除非使用显式参数将协定保留给数据协定特性。</span><span class="sxs-lookup"><span data-stu-id="ed15e-143">Make sure you understand that data members, even private and internal, cannot change their names, types, or even their order in future versions of the type unless special care is taken to preserve the contract using explicit parameters to the data contract attributes.</span></span>

 <span data-ttu-id="ed15e-144">对可序列化类型进行更改时测试序列化的兼容性。</span><span class="sxs-lookup"><span data-stu-id="ed15e-144">Test compatibility of serialization when making changes to serializable types.</span></span> <span data-ttu-id="ed15e-145">尝试将新版本反序列化为旧版本，以及将旧版本反序列化为新版本。</span><span class="sxs-lookup"><span data-stu-id="ed15e-145">Try deserializing the new version into an old version, and vice versa.</span></span>

 <span data-ttu-id="ed15e-146">✔️考虑实现 <xref:System.Runtime.Serialization.IExtensibleDataObject> 以允许在类型的不同版本之间进行往返。</span><span class="sxs-lookup"><span data-stu-id="ed15e-146">✔️ CONSIDER implementing <xref:System.Runtime.Serialization.IExtensibleDataObject> to allow round-tripping between different versions of the type.</span></span>

 <span data-ttu-id="ed15e-147">序列化程序可通过此接口确保在往返期间不丢失任何数据。</span><span class="sxs-lookup"><span data-stu-id="ed15e-147">The interface allows the serializer to ensure that no data is lost during round-tripping.</span></span> <span data-ttu-id="ed15e-148"><xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType>属性用于存储来自当前版本未知的类型的未来版本的任何数据，因此它不能将它存储在其数据成员中。</span><span class="sxs-lookup"><span data-stu-id="ed15e-148">The <xref:System.Runtime.Serialization.IExtensibleDataObject.ExtensionData%2A?displayProperty=nameWithType> property is used to store any data from the future version of the type that is unknown to the current version, and so it cannot store it in its data members.</span></span> <span data-ttu-id="ed15e-149">当随后序列化当前版本并将其反序列化为未来版本时，可在序列化流中使用附加数据。</span><span class="sxs-lookup"><span data-stu-id="ed15e-149">When the current version is subsequently serialized and deserialized into a future version, the additional data will be available in the serialized stream.</span></span>

## <a name="supporting-xml-serialization"></a><span data-ttu-id="ed15e-150">支持 XML 序列化</span><span class="sxs-lookup"><span data-stu-id="ed15e-150">Supporting XML Serialization</span></span>

 <span data-ttu-id="ed15e-151">数据协定序列化是 .NET Framework 中的主要 (默认) 序列化技术，但存在数据协定序列化不支持的序列化方案。</span><span class="sxs-lookup"><span data-stu-id="ed15e-151">Data Contract Serialization is the main (default) serialization technology in the .NET Framework, but there are serialization scenarios that Data Contract Serialization does not support.</span></span> <span data-ttu-id="ed15e-152">例如，数据协定序列化无法让您完全控制序列化程序生成或使用的 XML 的形状。</span><span class="sxs-lookup"><span data-stu-id="ed15e-152">For example, it does not give you full control over the shape of XML produced or consumed by the serializer.</span></span> <span data-ttu-id="ed15e-153">如果需要此类精细控制，则必须使用 XML 序列化，并且你需要设计类型以支持此序列化技术。</span><span class="sxs-lookup"><span data-stu-id="ed15e-153">If such fine control is required, XML Serialization has to be used, and you need to design your types to support this serialization technology.</span></span>

 <span data-ttu-id="ed15e-154">❌ 除非您有很好的理由来控制生成的 XML 的形状，否则应避免专门设计用于 XML 序列化的类型。</span><span class="sxs-lookup"><span data-stu-id="ed15e-154">❌ AVOID designing your types specifically for XML Serialization, unless you have a very strong reason to control the shape of the XML produced.</span></span> <span data-ttu-id="ed15e-155">此序列化技术已由上一节讨论的数据协定序列化所取代。</span><span class="sxs-lookup"><span data-stu-id="ed15e-155">This serialization technology has been superseded by the Data Contract Serialization discussed in the previous section.</span></span>

 <span data-ttu-id="ed15e-156"><xref:System.Xml.Serialization.IXmlSerializable>如果需要更好地控制序列化 XML 的形状，而不是应用 XML 序列化属性所提供的内容，✔️考虑实现接口。</span><span class="sxs-lookup"><span data-stu-id="ed15e-156">✔️ CONSIDER implementing the <xref:System.Xml.Serialization.IXmlSerializable> interface if you want even more control over the shape of the serialized XML than what’s offered by applying the XML Serialization attributes.</span></span> <span data-ttu-id="ed15e-157">利用此接口的两种方法（<xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A> 和 <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>），你可以完全控制序列化的 XML 流。</span><span class="sxs-lookup"><span data-stu-id="ed15e-157">Two methods of the interface, <xref:System.Xml.Serialization.IXmlSerializable.ReadXml%2A> and <xref:System.Xml.Serialization.IXmlSerializable.WriteXml%2A>, allow you to fully control the serialized XML stream.</span></span> <span data-ttu-id="ed15e-158">还可以通过应用来控制为类型生成的 XML 架构 `XmlSchemaProviderAttribute` 。</span><span class="sxs-lookup"><span data-stu-id="ed15e-158">You can also control the XML schema that gets generated for the type by applying the `XmlSchemaProviderAttribute`.</span></span>

## <a name="supporting-runtime-serialization"></a><span data-ttu-id="ed15e-159">支持运行时序列化</span><span class="sxs-lookup"><span data-stu-id="ed15e-159">Supporting Runtime Serialization</span></span>

 <span data-ttu-id="ed15e-160">运行时序列化是 .NET 远程处理所使用的一种技术。</span><span class="sxs-lookup"><span data-stu-id="ed15e-160">Runtime Serialization is a technology used by .NET Remoting.</span></span> <span data-ttu-id="ed15e-161">如果你认为将使用 .NET 远程处理传输类型，则需要确保它们支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-161">If you think your types will be transported using .NET Remoting, you need to make sure they support Runtime Serialization.</span></span>

 <span data-ttu-id="ed15e-162">可以通过应用来提供对运行时序列化的基本支持 <xref:System.SerializableAttribute> ，更高级的方案涉及实现一个简单的运行时可序列化模式 (实现 <xref:System.Runtime.Serialization.ISerializable> 和提供序列化构造函数) 。</span><span class="sxs-lookup"><span data-stu-id="ed15e-162">The basic support for Runtime Serialization can be provided by applying the <xref:System.SerializableAttribute>, and more advanced scenarios involve implementing a simple Runtime Serializable Pattern (implement <xref:System.Runtime.Serialization.ISerializable> and provide serialization constructor).</span></span>

 <span data-ttu-id="ed15e-163">✔️如果你的类型将与 .NET 远程处理一起使用，请考虑支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-163">✔️ CONSIDER supporting Runtime Serialization if your types will be used with .NET Remoting.</span></span> <span data-ttu-id="ed15e-164">例如， <xref:System.AddIn?displayProperty=nameWithType> 命名空间使用 .Net 远程处理，因此在外接程序之间交换的所有类型都 `System.AddIn` 需要支持运行时序列化。</span><span class="sxs-lookup"><span data-stu-id="ed15e-164">For example, the <xref:System.AddIn?displayProperty=nameWithType> namespace uses .NET Remoting, and so all types exchanged between `System.AddIn` add-ins need to support Runtime Serialization.</span></span>

 <span data-ttu-id="ed15e-165">如果希望完全控制序列化过程，✔️应考虑实现运行时可序列化模式。</span><span class="sxs-lookup"><span data-stu-id="ed15e-165">✔️ CONSIDER implementing the Runtime Serializable Pattern if you want complete control over the serialization process.</span></span> <span data-ttu-id="ed15e-166">例如，如果您需要在对数据进行序列化或反序列化时转换数据。</span><span class="sxs-lookup"><span data-stu-id="ed15e-166">For example, if you want to transform data as it gets serialized or deserialized.</span></span>

 <span data-ttu-id="ed15e-167">此模式非常简单。</span><span class="sxs-lookup"><span data-stu-id="ed15e-167">The pattern is very simple.</span></span> <span data-ttu-id="ed15e-168">您需要执行的全部操作就是实现 <xref:System.Runtime.Serialization.ISerializable> 接口，并提供在反序列化对象时使用的特殊构造函数。</span><span class="sxs-lookup"><span data-stu-id="ed15e-168">All you need to do is implement the <xref:System.Runtime.Serialization.ISerializable> interface and provide a special constructor that is used when the object is deserialized.</span></span>

 <span data-ttu-id="ed15e-169">✔️使序列化构造函数受到保护，并严格按照此处的示例中所示，提供两个类型和命名的参数。</span><span class="sxs-lookup"><span data-stu-id="ed15e-169">✔️ DO make the serialization constructor protected and provide two parameters typed and named exactly as shown in the sample here.</span></span>

```csharp
[Serializable]
public class Person : ISerializable
{
    protected Person(SerializationInfo info, StreamingContext context)
    {
        // ...
    }
}
```

 <span data-ttu-id="ed15e-170">✔️ <xref:System.Runtime.Serialization.ISerializable> 显式实现成员。</span><span class="sxs-lookup"><span data-stu-id="ed15e-170">✔️ DO implement the <xref:System.Runtime.Serialization.ISerializable> members explicitly.</span></span>

 <span data-ttu-id="ed15e-171">✔️将链接要求应用到 <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType> 实现。</span><span class="sxs-lookup"><span data-stu-id="ed15e-171">✔️ DO apply a link demand to <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=nameWithType> implementation.</span></span> <span data-ttu-id="ed15e-172">这可确保只有完全受信任的核心和运行时序列化程序才能访问成员。</span><span class="sxs-lookup"><span data-stu-id="ed15e-172">This ensures that only fully trusted core and the Runtime Serializer have access to the member.</span></span>

 <span data-ttu-id="ed15e-173">*部分©2005，2009 Microsoft Corporation。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="ed15e-173">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="ed15e-174">*经许可重印皮尔逊教育，Inc. 的作者 [：从框架设计指导原则：用于可重复使用的 .Net 库的约定、惯例和模式; 第2版](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) By Krzysztof Cwalina，Brad Abrams，通过 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分2008发布。*</span><span class="sxs-lookup"><span data-stu-id="ed15e-174">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="ed15e-175">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed15e-175">See also</span></span>

- [<span data-ttu-id="ed15e-176">框架设计准则</span><span class="sxs-lookup"><span data-stu-id="ed15e-176">Framework Design Guidelines</span></span>](index.md)
- [<span data-ttu-id="ed15e-177">使用准则</span><span class="sxs-lookup"><span data-stu-id="ed15e-177">Usage Guidelines</span></span>](usage-guidelines.md)
