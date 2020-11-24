---
title: NodeList 和 NamedNodeMap 的动态更新
ms.date: 03/30/2017
ms.assetid: 76c511fd-6704-4ca4-8078-860a68d898ad
ms.openlocfilehash: 2e23507000a780246c129d470b525f19b8b3b9c9
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94827654"
---
# <a name="dynamic-updates-to-nodelists-and-namednodemaps"></a><span data-ttu-id="2b28a-102">NodeList 和 NamedNodeMap 的动态更新</span><span class="sxs-lookup"><span data-stu-id="2b28a-102">Dynamic Updates to NodeLists and NamedNodeMaps</span></span>
<span data-ttu-id="2b28a-103">由于 XmlNodeList  和 XmlNamedNodeMap  包含节点集，而 XML 文档加载到内存中并被修改，因此万维网联合会 (W3C) 规定这些包含节点集的对象必须是动态对象。</span><span class="sxs-lookup"><span data-stu-id="2b28a-103">Because the **XmlNodeList** and the **XmlNamedNodeMap** contain a set of nodes, yet the XML document is loaded into memory and is being modified, the World Wide Web Consortium (W3C) states that these objects that contain sets of nodes need to be dynamic.</span></span> <span data-ttu-id="2b28a-104">也就是说，如果基础文档更改，则这两个对象中的数据也应更改。</span><span class="sxs-lookup"><span data-stu-id="2b28a-104">That is, if the underlying document changes, then the data in these two objects should change also.</span></span> <span data-ttu-id="2b28a-105">因此，如果 XmlNodeList  包含特定元素（例如，元素 X）的所有子元素，请在文档中的元素 X 下添加另一个元素 Q。XmlNodeList  也应将新元素 Q 添加到集合中。</span><span class="sxs-lookup"><span data-stu-id="2b28a-105">Therefore, if you have an **XmlNodeList** that contains all the child elements of a particular element (for example, element X), then you add an additional element, element Q, to the document under element X. The **XmlNodeList** should also have that new element Q added to its collection.</span></span> <span data-ttu-id="2b28a-106">反过来也一样。</span><span class="sxs-lookup"><span data-stu-id="2b28a-106">The same is true in reverse.</span></span> <span data-ttu-id="2b28a-107">如果将节点添加到 XmlNodeList  ，那么基础文档也会更新。</span><span class="sxs-lookup"><span data-stu-id="2b28a-107">If a node is added to the **XmlNodeList**, the underlying document is updated as well.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b28a-108">请参阅</span><span class="sxs-lookup"><span data-stu-id="2b28a-108">See also</span></span>

- [<span data-ttu-id="2b28a-109">XML 文档对象模型 (DOM)</span><span class="sxs-lookup"><span data-stu-id="2b28a-109">XML Document Object Model (DOM)</span></span>](xml-document-object-model-dom.md)
