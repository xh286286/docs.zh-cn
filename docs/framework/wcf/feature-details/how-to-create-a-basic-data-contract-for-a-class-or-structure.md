---
title: 如何：创建类或结构的基本数据协定
description: 按照此示例，了解如何使用 DataContractAttribute 特性在 WCF 中创建使用类或结构的数据协定。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataMemberAttribute
- DataContractAttribute class
- data contracts [WCF], creating for a class or structure
ms.assetid: bc464889-3070-4a2f-91d2-e788a0f686a7
ms.openlocfilehash: 5634eb3d3ec18d95fd7d6b3c89b572ab4f5b8eca
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96254033"
---
# <a name="how-to-create-a-basic-data-contract-for-a-class-or-structure"></a><span data-ttu-id="9017a-103">如何：创建类或结构的基本数据协定</span><span class="sxs-lookup"><span data-stu-id="9017a-103">How to: Create a Basic Data Contract for a Class or Structure</span></span>

<span data-ttu-id="9017a-104">本主题演示使用类或结构创建数据协定的基本步骤。</span><span class="sxs-lookup"><span data-stu-id="9017a-104">This topic shows the basic steps to create a data contract using a class or structure.</span></span> <span data-ttu-id="9017a-105">有关数据协定及其使用方式的详细信息，请参阅 [使用数据协定](using-data-contracts.md)。</span><span class="sxs-lookup"><span data-stu-id="9017a-105">For more information about data contracts and how they are used, see [Using Data Contracts](using-data-contracts.md).</span></span>  
  
 <span data-ttu-id="9017a-106">有关演练创建基本 Windows Communication Foundation (WCF) 服务和客户端的步骤的教程，请参阅 [入门教程](../getting-started-tutorial.md)。</span><span class="sxs-lookup"><span data-stu-id="9017a-106">For a tutorial that walks through the steps of creating a basic Windows Communication Foundation (WCF) service and client, see the [Getting Started Tutorial](../getting-started-tutorial.md).</span></span> <span data-ttu-id="9017a-107">对于包含基本服务和客户端的工作示例应用程序，请参阅 [基本数据协定](../samples/basic-data-contract.md)。</span><span class="sxs-lookup"><span data-stu-id="9017a-107">For a working sample application that consists of a basic service and client, see [Basic Data Contract](../samples/basic-data-contract.md).</span></span>  
  
### <a name="to-create-a-basic-data-contract-for-a-class-or-structure"></a><span data-ttu-id="9017a-108">创建类或结构的基本数据协定</span><span class="sxs-lookup"><span data-stu-id="9017a-108">To create a basic data contract for a class or structure</span></span>  
  
1. <span data-ttu-id="9017a-109">通过将 <xref:System.Runtime.Serialization.DataContractAttribute> 属性应用于类来声明该类型具有数据协定。</span><span class="sxs-lookup"><span data-stu-id="9017a-109">Declare that the type has a data contract by applying the <xref:System.Runtime.Serialization.DataContractAttribute> attribute to the class.</span></span> <span data-ttu-id="9017a-110">请注意，包括不带属性的公共类型在内的所有公共类型都是可序列化的。</span><span class="sxs-lookup"><span data-stu-id="9017a-110">Note that all public types, including those without attributes, are serializable.</span></span> <span data-ttu-id="9017a-111">如果不存在 <xref:System.Runtime.Serialization.DataContractSerializer> 属性，<xref:System.Runtime.Serialization.DataContractAttribute> 将推断出一个数据协定。</span><span class="sxs-lookup"><span data-stu-id="9017a-111">The <xref:System.Runtime.Serialization.DataContractSerializer> infers a data contract if the <xref:System.Runtime.Serialization.DataContractAttribute> attribute is absent.</span></span> <span data-ttu-id="9017a-112">有关详细信息，请参阅 [可序列化类型](serializable-types.md)。</span><span class="sxs-lookup"><span data-stu-id="9017a-112">For more information, see [Serializable Types](serializable-types.md).</span></span>  
  
2. <span data-ttu-id="9017a-113">通过将 <xref:System.Runtime.Serialization.DataMemberAttribute> 属性 (Attribute) 应用于每个成员来定义要序列化的成员（属性 (Property)、字段或事件）。</span><span class="sxs-lookup"><span data-stu-id="9017a-113">Define the members (properties, fields, or events) that are serialized by applying the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to each member.</span></span> <span data-ttu-id="9017a-114">这些成员称为数据成员。</span><span class="sxs-lookup"><span data-stu-id="9017a-114">These members are called data members.</span></span> <span data-ttu-id="9017a-115">默认情况下，所有公共类型都是可序列化的。</span><span class="sxs-lookup"><span data-stu-id="9017a-115">By default, all public types are serializable.</span></span> <span data-ttu-id="9017a-116">有关详细信息，请参阅 [可序列化类型](serializable-types.md)。</span><span class="sxs-lookup"><span data-stu-id="9017a-116">For more information, see [Serializable Types](serializable-types.md).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="9017a-117">您可以将 <xref:System.Runtime.Serialization.DataMemberAttribute> 属性应用于私有字段，这会导致向其他人公开此数据。</span><span class="sxs-lookup"><span data-stu-id="9017a-117">You can apply the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to private fields, causing the data to be exposed to others.</span></span> <span data-ttu-id="9017a-118">请确保成员不包含敏感数据。</span><span class="sxs-lookup"><span data-stu-id="9017a-118">Be sure that the member does not contain sensitive data.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9017a-119">示例</span><span class="sxs-lookup"><span data-stu-id="9017a-119">Example</span></span>  

 <span data-ttu-id="9017a-120">下面的示例演示如何通过将 `Person` 和 <xref:System.Runtime.Serialization.DataContractAttribute> 属性应用于类及其成员来创建 <xref:System.Runtime.Serialization.DataMemberAttribute> 类型的数据协定。</span><span class="sxs-lookup"><span data-stu-id="9017a-120">The following example shows how to create a data contract for the `Person` type by applying the <xref:System.Runtime.Serialization.DataContractAttribute> and <xref:System.Runtime.Serialization.DataMemberAttribute> attributes to the class and its members.</span></span>  
  
 [!code-csharp[DataContractAttribute#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/datacontractattribute/cs/overview.cs#2)]
 [!code-vb[DataContractAttribute#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/datacontractattribute/vb/overview.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="9017a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="9017a-121">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.DataMemberAttribute>
- [<span data-ttu-id="9017a-122">使用数据协定</span><span class="sxs-lookup"><span data-stu-id="9017a-122">Using Data Contracts</span></span>](using-data-contracts.md)
- [<span data-ttu-id="9017a-123">入门教程</span><span class="sxs-lookup"><span data-stu-id="9017a-123">Getting Started Tutorial</span></span>](../getting-started-tutorial.md)
- [<span data-ttu-id="9017a-124">入门</span><span class="sxs-lookup"><span data-stu-id="9017a-124">Getting Started</span></span>](../samples/getting-started-sample.md)
