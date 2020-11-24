---
title: 保留实体引用
ms.date: 03/30/2017
ms.assetid: 000a6cae-5972-40d6-bd6c-a9b7d9649b3c
ms.openlocfilehash: 2cc2fcf3fdc2a89e4f72ae65e6e7385cb83f168c
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94823831"
---
# <a name="entity-references-are-preserved"></a><span data-ttu-id="8a69d-102">保留实体引用</span><span class="sxs-lookup"><span data-stu-id="8a69d-102">Entity References are Preserved</span></span>
<span data-ttu-id="8a69d-103">如果实体引用不是被扩展，而是被暂留，XML 文档对象模型 (DOM) 在遇到实体引用时生成 XmlEntityReference  节点。</span><span class="sxs-lookup"><span data-stu-id="8a69d-103">When the entity reference is not expanded, but preserved, the XML Document Object Model (DOM) builds an **XmlEntityReference** node when it encounters an entity reference.</span></span>  
  
 <span data-ttu-id="8a69d-104">使用以下 XML，</span><span class="sxs-lookup"><span data-stu-id="8a69d-104">Using the following XML,</span></span>  
  
```xml  
<author>Fred</author>  
<pubinfo>Published by &publisher;</pubinfo>  
```  
  
 <span data-ttu-id="8a69d-105">DOM 可以在遇到 `&publisher;` 引用时生成 XmlEntityReference  节点。</span><span class="sxs-lookup"><span data-stu-id="8a69d-105">the DOM builds an **XmlEntityReference** node when it encounters the `&publisher;` reference.</span></span> <span data-ttu-id="8a69d-106">XmlEntityReference  包含从实体声明内容中复制的子节点。</span><span class="sxs-lookup"><span data-stu-id="8a69d-106">The **XmlEntityReference** contains child nodes copied from the content in the entity declaration.</span></span> <span data-ttu-id="8a69d-107">由于上一代码示例包含实体声明文本，因此 XmlText  节点被创建为实体引用节点的子节点。</span><span class="sxs-lookup"><span data-stu-id="8a69d-107">The preceding code example contains text in the entity declaration, so an **XmlText** node is created as the child node of the entity reference node.</span></span>  
  
 <span data-ttu-id="8a69d-108">![保留的实体引用的树结构](media/xmlentityref-notexpanded-nodes.gif "xmlentityref_notexpanded_nodes")</span><span class="sxs-lookup"><span data-stu-id="8a69d-108">![Tree structure for preserved entity references](media/xmlentityref-notexpanded-nodes.gif "xmlentityref_notexpanded_nodes")</span></span>  
<span data-ttu-id="8a69d-109">保留的实体引用的树结构</span><span class="sxs-lookup"><span data-stu-id="8a69d-109">Tree structure for entity references that are preserved</span></span>  
  
 <span data-ttu-id="8a69d-110">XmlEntityReference  的子节点是在遇到实体声明时，从 XmlEntity  节点创建的所有子节点的副本。</span><span class="sxs-lookup"><span data-stu-id="8a69d-110">The child nodes of the **XmlEntityReference** are copies of all the child nodes created from the **XmlEntity** node when the entity declaration was encountered.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8a69d-111">一旦置于实体引用节点下，从 XmlEntity  复制的节点就不一定是完全相同的副本。</span><span class="sxs-lookup"><span data-stu-id="8a69d-111">The nodes copied from the **XmlEntity** are not always exact copies once placed under the entity reference node.</span></span> <span data-ttu-id="8a69d-112">可以有在实体引用节点范围内并影响子节点的最终配置的命名空间。</span><span class="sxs-lookup"><span data-stu-id="8a69d-112">There can be namespaces that are in scope at the entity reference node, and that affects the final configuration of the child nodes.</span></span>  
  
 <span data-ttu-id="8a69d-113">默认情况下，暂留的是 `&abc;` 等常规实体，并且始终都会创建 XmlEntityReference  节点。</span><span class="sxs-lookup"><span data-stu-id="8a69d-113">By default, general entities like `&abc;` are preserved and **XmlEntityReference** nodes always created.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8a69d-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a69d-114">See also</span></span>

- [<span data-ttu-id="8a69d-115">XML 文档对象模型 (DOM)</span><span class="sxs-lookup"><span data-stu-id="8a69d-115">XML Document Object Model (DOM)</span></span>](xml-document-object-model-dom.md)
