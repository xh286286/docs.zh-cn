---
title: 数据协定名称
description: 发现 WCF 基础结构的数据协定和成员命名规则和默认行为，它通过使用等效的数据协定支持通信。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data contracts [WCF], naming
ms.assetid: 31f87e6c-247b-48f5-8e94-b9e1e33d8d09
ms.openlocfilehash: 3bb0aca2a1207a98b45fe8b6d43930e9b2acc5ec
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96286696"
---
# <a name="data-contract-names"></a><span data-ttu-id="6901f-103">数据协定名称</span><span class="sxs-lookup"><span data-stu-id="6901f-103">Data Contract Names</span></span>

<span data-ttu-id="6901f-104">有时，客户端和服务不共享相同的类型。</span><span class="sxs-lookup"><span data-stu-id="6901f-104">Sometimes a client and a service do not share the same types.</span></span> <span data-ttu-id="6901f-105">它们仍然可以将数据传递给对方，只要数据协定是双方等效的。</span><span class="sxs-lookup"><span data-stu-id="6901f-105">They can still pass data to each other as long as the data contracts are equivalent on both sides.</span></span> <span data-ttu-id="6901f-106">[数据协定等效](data-contract-equivalence.md) 性基于数据协定和数据成员名称，因此提供了一种机制来将类型和成员映射到这些名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-106">[Data Contract Equivalence](data-contract-equivalence.md) is based on data contract and data member names, and therefore a mechanism is provided to map types and members to those names.</span></span> <span data-ttu-id="6901f-107">本主题介绍在创建名称时，用于命名数据协定的规则以及 Windows Communication Foundation (WCF) 基础结构的默认行为。</span><span class="sxs-lookup"><span data-stu-id="6901f-107">This topic explains the rules for naming data contracts as well as the default behavior of the Windows Communication Foundation (WCF) infrastructure when creating names.</span></span>

## <a name="basic-rules"></a><span data-ttu-id="6901f-108">基本规则</span><span class="sxs-lookup"><span data-stu-id="6901f-108">Basic Rules</span></span>

<span data-ttu-id="6901f-109">有关数据协定命名的基本规则包括：</span><span class="sxs-lookup"><span data-stu-id="6901f-109">Basic rules regarding naming data contracts include:</span></span>

- <span data-ttu-id="6901f-110">完全限定的数据协定名称由命名空间和名称组成。</span><span class="sxs-lookup"><span data-stu-id="6901f-110">A fully-qualified data contract name consists of a namespace and a name.</span></span>

- <span data-ttu-id="6901f-111">数据成员只有名称，而没有命名空间。</span><span class="sxs-lookup"><span data-stu-id="6901f-111">Data members have only names, but no namespaces.</span></span>

- <span data-ttu-id="6901f-112">在处理数据协定时，WCF 基础结构区分与数据协定和数据成员的命名空间和名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="6901f-112">When processing data contracts, the WCF infrastructure is case-sensitive to both the namespaces and the names of data contracts and data members.</span></span>

## <a name="data-contract-namespaces"></a><span data-ttu-id="6901f-113">数据协定命名空间</span><span class="sxs-lookup"><span data-stu-id="6901f-113">Data Contract Namespaces</span></span>

<span data-ttu-id="6901f-114">数据协定命名空间采用统一资源标识符 (URI) 的形式。</span><span class="sxs-lookup"><span data-stu-id="6901f-114">A data contract namespace takes the form of a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="6901f-115">URI 可以是绝对的，也可以是相对的。</span><span class="sxs-lookup"><span data-stu-id="6901f-115">The URI can be either absolute or relative.</span></span> <span data-ttu-id="6901f-116">默认情况下，会为特定类型的数据协定分配公共语言运行库 (CLR) 命名空间中该类型的命名空间。</span><span class="sxs-lookup"><span data-stu-id="6901f-116">By default, data contracts for a particular type are assigned a namespace that comes from the common language runtime (CLR) namespace of that type.</span></span>

<span data-ttu-id="6901f-117">默认情况下，任何给定的 CLR 命名空间都 (格式的 *clr*) 映射到命名空间 `http://schemas.datacontract.org/2004/07/Clr.Namespace` 。</span><span class="sxs-lookup"><span data-stu-id="6901f-117">By default, any given CLR namespace (in the format *Clr.Namespace*) is mapped to the namespace `http://schemas.datacontract.org/2004/07/Clr.Namespace`.</span></span> <span data-ttu-id="6901f-118">若要重写此默认值，请对整个模块或程序集应用 <xref:System.Runtime.Serialization.ContractNamespaceAttribute> 属性。</span><span class="sxs-lookup"><span data-stu-id="6901f-118">To override this default, apply the <xref:System.Runtime.Serialization.ContractNamespaceAttribute> attribute to the entire module or assembly.</span></span> <span data-ttu-id="6901f-119">或者，若要控制每种类型的数据协定命名空间，请设置 <xref:System.Runtime.Serialization.DataContractAttribute.Namespace%2A> 的 <xref:System.Runtime.Serialization.DataContractAttribute> 属性。</span><span class="sxs-lookup"><span data-stu-id="6901f-119">Alternatively, to control the data contract namespace for each type, set the <xref:System.Runtime.Serialization.DataContractAttribute.Namespace%2A> property of the <xref:System.Runtime.Serialization.DataContractAttribute>.</span></span>

> [!NOTE]
> <span data-ttu-id="6901f-120">`http://schemas.microsoft.com/2003/10/Serialization`命名空间是保留命名空间，不能用作数据协定命名空间。</span><span class="sxs-lookup"><span data-stu-id="6901f-120">The `http://schemas.microsoft.com/2003/10/Serialization` namespace is reserved and cannot be used as a data contract namespace.</span></span>

> [!NOTE]
> <span data-ttu-id="6901f-121">不能重写包含 `delegate` 声明的数据协定类型中的默认命名空间。</span><span class="sxs-lookup"><span data-stu-id="6901f-121">You cannot override the default namespace in data contract types that contain `delegate` declarations.</span></span>

## <a name="data-contract-names"></a><span data-ttu-id="6901f-122">数据协定名称</span><span class="sxs-lookup"><span data-stu-id="6901f-122">Data Contract Names</span></span>

<span data-ttu-id="6901f-123">给定类型的默认数据协定名称是该类型的名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-123">The default name of a data contract for a given type is the name of that type.</span></span> <span data-ttu-id="6901f-124">若要重写默认值，请将 <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A> 的 <xref:System.Runtime.Serialization.DataContractAttribute> 属性设置为其他名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-124">To override the default, set the <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A> property of the <xref:System.Runtime.Serialization.DataContractAttribute> to an alternative name.</span></span> <span data-ttu-id="6901f-125">本主题中后面的“泛型类型的数据协定名称”中说明了泛型类型的特殊规则。</span><span class="sxs-lookup"><span data-stu-id="6901f-125">Special rules for generic types are described in "Data Contract Names for Generic Types" later in this topic.</span></span>

## <a name="data-member-names"></a><span data-ttu-id="6901f-126">数据成员名称</span><span class="sxs-lookup"><span data-stu-id="6901f-126">Data Member Names</span></span>

<span data-ttu-id="6901f-127">给定字段或属性的默认数据成员名称是该字段或属性的名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-127">The default name of a data member for a given field or property is the name of that field or property.</span></span> <span data-ttu-id="6901f-128">若要重写默认值，请将 <xref:System.Runtime.Serialization.DataMemberAttribute.Name%2A> 的 <xref:System.Runtime.Serialization.DataMemberAttribute> 属性设置为其他值。</span><span class="sxs-lookup"><span data-stu-id="6901f-128">To override the default, set the <xref:System.Runtime.Serialization.DataMemberAttribute.Name%2A> property of the <xref:System.Runtime.Serialization.DataMemberAttribute> to an alternative value.</span></span>

### <a name="examples"></a><span data-ttu-id="6901f-129">示例</span><span class="sxs-lookup"><span data-stu-id="6901f-129">Examples</span></span>

<span data-ttu-id="6901f-130">下面的示例演示如何重写数据协定和数据成员的默认命名行为。</span><span class="sxs-lookup"><span data-stu-id="6901f-130">The following example shows how you can override the default naming behavior of data contracts and data members.</span></span>

[!code-csharp[C_DataContractNames#1](~/samples/snippets/csharp/VS_Snippets_CFX/c_datacontractnames/cs/source.cs#1)]
[!code-vb[C_DataContractNames#1](~/samples/snippets/visualbasic/VS_Snippets_CFX/c_datacontractnames/vb/source.vb#1)]

## <a name="data-contract-names-for-generic-types"></a><span data-ttu-id="6901f-131">泛型类型的数据协定名称</span><span class="sxs-lookup"><span data-stu-id="6901f-131">Data Contract Names for Generic Types</span></span>

<span data-ttu-id="6901f-132">确定泛型类型的数据协定名称具有特殊的规则。</span><span class="sxs-lookup"><span data-stu-id="6901f-132">Special rules exist for determining data contract names for generic types.</span></span> <span data-ttu-id="6901f-133">这些规则有助于避免在同一泛型类型的两个封闭式泛型之间发生数据协定名称冲突。</span><span class="sxs-lookup"><span data-stu-id="6901f-133">These rules help avoid data contract name collisions between two closed generics of the same generic type.</span></span>

<span data-ttu-id="6901f-134">默认情况下，泛型类型的数据协定名称是该类型的名称，后跟字符串 "of"，后跟泛型参数的数据协定名称，然后是使用泛型参数的数据协定命名空间计算的 *哈希* 值。</span><span class="sxs-lookup"><span data-stu-id="6901f-134">By default, the data contract name for a generic type is the name of the type, followed by the string "Of", followed by the data contract names of the generic parameters, followed by a *hash* computed using the data contract namespaces of the generic parameters.</span></span> <span data-ttu-id="6901f-135">哈希值是作为唯一标识数据片段的“指纹”的数学函数的计算结果。</span><span class="sxs-lookup"><span data-stu-id="6901f-135">A hash is the result of a mathematical function that acts as a "fingerprint" that uniquely identifies a piece of data.</span></span> <span data-ttu-id="6901f-136">当所有的泛型参数都是基元类型时，将忽略哈希值。</span><span class="sxs-lookup"><span data-stu-id="6901f-136">When all of the generic parameters are primitive types, the hash is omitted.</span></span>

<span data-ttu-id="6901f-137">有关示例，请参见以下示例中的类型。</span><span class="sxs-lookup"><span data-stu-id="6901f-137">For example, see the types in the following example.</span></span>

[!code-csharp[C_DataContractNames#2](~/samples/snippets/csharp/VS_Snippets_CFX/c_datacontractnames/cs/source.cs#2)]
[!code-vb[C_DataContractNames#2](~/samples/snippets/visualbasic/VS_Snippets_CFX/c_datacontractnames/vb/source.vb#2)]

<span data-ttu-id="6901f-138">在此示例中，`Drawing<Square,RegularRedBrush>` 类型具有数据协定名称“DrawingOfSquareRedBrush5HWGAU6h”，其中“5HWGAU6h”是“urn:shapes”和“urn:default”命名空间的哈希值。</span><span class="sxs-lookup"><span data-stu-id="6901f-138">In this example, the type `Drawing<Square,RegularRedBrush>` has the data contract name "DrawingOfSquareRedBrush5HWGAU6h", where "5HWGAU6h" is a hash of the "urn:shapes" and "urn:default" namespaces.</span></span> <span data-ttu-id="6901f-139">`Drawing<Square,SpecialRedBrush>` 类型具有数据协定名称“DrawingOfSquareRedBrushjpB5LgQ_S”，其中“jpB5LgQ_S”是“urn:shapes”和“urn:special”命名空间的哈希值。</span><span class="sxs-lookup"><span data-stu-id="6901f-139">The type `Drawing<Square,SpecialRedBrush>` has the data contract name "DrawingOfSquareRedBrushjpB5LgQ_S", where "jpB5LgQ_S" is a hash of the "urn:shapes" and the "urn:special" namespaces.</span></span> <span data-ttu-id="6901f-140">请注意，如果不使用哈希值，则这两个名称将完全相同，因此会发生名称冲突。</span><span class="sxs-lookup"><span data-stu-id="6901f-140">Note that if the hash is not used, the two names are identical, and thus a name collision occurs.</span></span>

## <a name="customizing-data-contract-names-for-generic-types"></a><span data-ttu-id="6901f-141">自定义泛型类型的数据协定名称</span><span class="sxs-lookup"><span data-stu-id="6901f-141">Customizing data contract names for generic types</span></span>

<span data-ttu-id="6901f-142">有时不允许为泛型类型生成数据协定名称，如前面所述。</span><span class="sxs-lookup"><span data-stu-id="6901f-142">Sometimes, the data contract names generated for generic types, as described previously, are unacceptable.</span></span> <span data-ttu-id="6901f-143">例如，您可能事先知道不会遇到名称冲突并且想删除哈希值。</span><span class="sxs-lookup"><span data-stu-id="6901f-143">For example, you may know in advance that you will not run into name collisions and may want to remove the hash.</span></span> <span data-ttu-id="6901f-144">在这种情况下，可以使用 <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A?displayProperty=nameWithType> 属性指定一种不同的方式来生成名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-144">In this case, you can use the <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A?displayProperty=nameWithType> property to specify a different way to generate names.</span></span> <span data-ttu-id="6901f-145">您可以在 `Name` 属性内的大括号中使用数字来引用泛型参数的数据协定名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-145">You can use numbers in curly braces inside of the `Name` property to refer to data contract names of the generic parameters.</span></span> <span data-ttu-id="6901f-146"> (0 引用第一个参数，1表示第二个参数，依此类推。 ) 可以使用数字 ( # ) 在大括号内的符号来引用哈希。</span><span class="sxs-lookup"><span data-stu-id="6901f-146">(0 refers to the first parameter, 1 refers to the second, and so on.) You can use a number (#) sign inside curly braces to refer to the hash.</span></span> <span data-ttu-id="6901f-147">您可以多次使用这些引用，也可以不使用引用。</span><span class="sxs-lookup"><span data-stu-id="6901f-147">You can use each of these references multiple times or not at all.</span></span>

<span data-ttu-id="6901f-148">例如，可能对前面的泛型 `Drawing` 类型进行了声明，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="6901f-148">For example, the preceding generic `Drawing` type could have been declared as shown in the following example.</span></span>

[!code-csharp[c_DataContractNames#3](~/samples/snippets/csharp/VS_Snippets_CFX/c_datacontractnames/cs/source.cs#3)]
[!code-vb[c_DataContractNames#3](~/samples/snippets/visualbasic/VS_Snippets_CFX/c_datacontractnames/vb/source.vb#3)]

<span data-ttu-id="6901f-149">在这种情况下，`Drawing<Square,RegularRedBrush>` 类型具有数据协定名称“Drawing_using_RedBrush_brush_and_Square_shape”。</span><span class="sxs-lookup"><span data-stu-id="6901f-149">In this case, the type `Drawing<Square,RegularRedBrush>` has the data contract name "Drawing_using_RedBrush_brush_and_Square_shape".</span></span> <span data-ttu-id="6901f-150">请注意，因为 <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A> 属性中有一个“{#}”，哈希值不是名称的一部分，因此该类型容易发生命名冲突；例如，`Drawing<Square,SpecialRedBrush>` 类型将具有完全相同的数据协定名称。</span><span class="sxs-lookup"><span data-stu-id="6901f-150">Note that because there is a "{#}" in the <xref:System.Runtime.Serialization.DataContractAttribute.Name%2A> property, the hash is not a part of the name, and thus the type is susceptible to naming collisions; for example, the type `Drawing<Square,SpecialRedBrush>` would have exactly the same data contract name.</span></span>

## <a name="see-also"></a><span data-ttu-id="6901f-151">请参阅</span><span class="sxs-lookup"><span data-stu-id="6901f-151">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.DataMemberAttribute>
- <xref:System.Runtime.Serialization.ContractNamespaceAttribute>
- [<span data-ttu-id="6901f-152">使用数据协定</span><span class="sxs-lookup"><span data-stu-id="6901f-152">Using Data Contracts</span></span>](using-data-contracts.md)
- [<span data-ttu-id="6901f-153">数据协定等效性</span><span class="sxs-lookup"><span data-stu-id="6901f-153">Data Contract Equivalence</span></span>](data-contract-equivalence.md)
- [<span data-ttu-id="6901f-154">数据协定名称</span><span class="sxs-lookup"><span data-stu-id="6901f-154">Data Contract Names</span></span>](data-contract-names.md)
- [<span data-ttu-id="6901f-155">数据协定版本管理</span><span class="sxs-lookup"><span data-stu-id="6901f-155">Data Contract Versioning</span></span>](data-contract-versioning.md)
