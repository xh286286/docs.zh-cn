---
title: 使用 XPathNavigator 的节点集定位
ms.date: 03/30/2017
ms.assetid: 1a954b41-7173-40bc-8544-d430f209b1e5
ms.openlocfilehash: 592acfb5e4065d707f4dda09f349e8b783656148
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95714293"
---
# <a name="node-set-navigation-using-xpathnavigator"></a><span data-ttu-id="bf9c1-102">使用 XPathNavigator 的节点集定位</span><span class="sxs-lookup"><span data-stu-id="bf9c1-102">Node Set Navigation Using XPathNavigator</span></span>

<span data-ttu-id="bf9c1-103">可以使用 <xref:System.Xml.XPath.XPathDocument> 类的节点集浏览方法在 <xref:System.Xml.XmlDocument> 或 <xref:System.Xml.XPath.XPathNavigator> 对象中浏览节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-103">You can navigate over nodes in an <xref:System.Xml.XPath.XPathDocument> or <xref:System.Xml.XmlDocument> object using the node set navigation methods of the <xref:System.Xml.XPath.XPathNavigator> class.</span></span> <span data-ttu-id="bf9c1-104">可以浏览所有节点，也可以浏览 <xref:System.Xml.XPath.XPathNavigator> 类的一种选择方法返回的所选节点集。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-104">You can navigate over all the nodes or over a selected set of nodes returned by one of the selection methods of the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
## <a name="element-node-set-navigation"></a><span data-ttu-id="bf9c1-105">浏览元素节点集</span><span class="sxs-lookup"><span data-stu-id="bf9c1-105">Element Node Set Navigation</span></span>  

 <span data-ttu-id="bf9c1-106"><xref:System.Xml.XPath.XPathNavigator> 类提供多种方法用于浏览元素节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-106">The <xref:System.Xml.XPath.XPathNavigator> class provides several methods used to navigate element nodes.</span></span> <span data-ttu-id="bf9c1-107">下表显示可用的浏览方法以及各种方法如何移动的说明；其中不包括用于浏览属性和命名空间节点的方法。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-107">The following table shows the navigation methods available and a description of how they move; this does not include methods used to navigate attribute and namespace nodes.</span></span>  
  
 <span data-ttu-id="bf9c1-108">若要详细了解如何在 <xref:System.Xml.XPath.XPathNavigator> 对象中选择节点，请参阅[使用 XPathNavigator 选择、计算和匹配 XML 数据](selecting-evaluating-and-matching-xml-data-using-xpathnavigator.md)。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-108">For more information about selecting nodes in an <xref:System.Xml.XPath.XPathNavigator> object, see [Selecting, Evaluating and Matching XML Data using XPathNavigator](selecting-evaluating-and-matching-xml-data-using-xpathnavigator.md).</span></span> <span data-ttu-id="bf9c1-109">若要详细了解如何浏览属性和命名空间节点，请参阅[使用 XPathNavigator 的属性和命名空间节点定位](attribute-and-namespace-node-navigation-using-xpathnavigator.md)。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-109">For more information about navigating attribute and namespace nodes, see [Attribute and Namespace Node Navigation Using XPathNavigator](attribute-and-namespace-node-navigation-using-xpathnavigator.md).</span></span>  
  
|<span data-ttu-id="bf9c1-110">方法</span><span class="sxs-lookup"><span data-stu-id="bf9c1-110">Method</span></span>|<span data-ttu-id="bf9c1-111">描述</span><span class="sxs-lookup"><span data-stu-id="bf9c1-111">Description</span></span>|  
|------------|-----------------|  
|<xref:System.Xml.XPath.XPathNavigator.MoveTo%2A>|<span data-ttu-id="bf9c1-112">将 <xref:System.Xml.XPath.XPathNavigator> 移至所指定的 <xref:System.Xml.XPath.XPathNavigator> 的相同位置。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-112">Moves the <xref:System.Xml.XPath.XPathNavigator> to the same position of the <xref:System.Xml.XPath.XPathNavigator> specified.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToChild%2A>|<span data-ttu-id="bf9c1-113">将 <xref:System.Xml.XPath.XPathNavigator> 移至当前节点的子节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-113">Moves the <xref:System.Xml.XPath.XPathNavigator> to a child node of the current node.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToFirst%2A>|<span data-ttu-id="bf9c1-114">将 <xref:System.Xml.XPath.XPathNavigator> 移至当前节点的第一个同级节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-114">Moves the <xref:System.Xml.XPath.XPathNavigator> to the first sibling node of the current node.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToFirstChild%2A>|<span data-ttu-id="bf9c1-115">将 <xref:System.Xml.XPath.XPathNavigator> 移至当前节点的第一个子节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-115">Moves the <xref:System.Xml.XPath.XPathNavigator> to the first child node of the current node.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToFollowing%2A>|<span data-ttu-id="bf9c1-116">将 <xref:System.Xml.XPath.XPathNavigator> 按文档顺序移至指定的元素。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-116">Moves the <xref:System.Xml.XPath.XPathNavigator> to the specified element in document order.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToId%2A>|<span data-ttu-id="bf9c1-117">将 <xref:System.Xml.XPath.XPathNavigator> 移至 `ID` 类型属性的值与给定 <xref:System.String> 匹配的节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-117">Moves the <xref:System.Xml.XPath.XPathNavigator> to the node that has an attribute of type `ID` with a value that matches the given <xref:System.String>.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToNext%2A>|<span data-ttu-id="bf9c1-118">将 <xref:System.Xml.XPath.XPathNavigator> 移至当前节点的下一个同级节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-118">Moves the <xref:System.Xml.XPath.XPathNavigator> to the next sibling node of the current node.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToParent%2A>|<span data-ttu-id="bf9c1-119">将 <xref:System.Xml.XPath.XPathNavigator> 移至当前节点的父节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-119">Moves the <xref:System.Xml.XPath.XPathNavigator> to the parent node of the current node.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToPrevious%2A>|<span data-ttu-id="bf9c1-120">将 <xref:System.Xml.XPath.XPathNavigator> 移至当前节点的上一个同级节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-120">Moves the <xref:System.Xml.XPath.XPathNavigator> to the previous sibling node of the current node.</span></span>|  
|<xref:System.Xml.XPath.XPathNavigator.MoveToRoot%2A>|<span data-ttu-id="bf9c1-121">将 <xref:System.Xml.XPath.XPathNavigator> 移至 XML 文档的根节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-121">Moves the <xref:System.Xml.XPath.XPathNavigator> to the root node of the XML document.</span></span>|  
  
## <a name="comments-and-processing-instruction-node-navigation"></a><span data-ttu-id="bf9c1-122">浏览注释和处理指令节点</span><span class="sxs-lookup"><span data-stu-id="bf9c1-122">Comments and Processing Instruction Node Navigation</span></span>  

 <span data-ttu-id="bf9c1-123">下列 <xref:System.Xml.XPath.XPathNavigator> 类方法可以从 XML 文档中的其他节点移至注释或处理指令节点。</span><span class="sxs-lookup"><span data-stu-id="bf9c1-123">The following <xref:System.Xml.XPath.XPathNavigator> class methods are valid for moving to comments or processing instructions from other nodes in an XML document.</span></span>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveTo%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToNext%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToPrevious%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToFirst%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToFirstChild%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToChild%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToParent%2A>  
  
- <xref:System.Xml.XPath.XPathNavigator.MoveToId%2A>  
  
## <a name="see-also"></a><span data-ttu-id="bf9c1-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="bf9c1-124">See also</span></span>

- <xref:System.Xml.XmlDocument>
- <xref:System.Xml.XPath.XPathDocument>
- <xref:System.Xml.XPath.XPathNavigator>
- [<span data-ttu-id="bf9c1-125">使用 XPath 数据模型处理 XML 数据</span><span class="sxs-lookup"><span data-stu-id="bf9c1-125">Process XML Data Using the XPath Data Model</span></span>](process-xml-data-using-the-xpath-data-model.md)
- [<span data-ttu-id="bf9c1-126">使用 XPathNavigator 的属性和命名空间节点定位</span><span class="sxs-lookup"><span data-stu-id="bf9c1-126">Attribute and Namespace Node Navigation Using XPathNavigator</span></span>](attribute-and-namespace-node-navigation-using-xpathnavigator.md)
- [<span data-ttu-id="bf9c1-127">使用 XPathNavigator 提取 XML 数据</span><span class="sxs-lookup"><span data-stu-id="bf9c1-127">Extract XML Data Using XPathNavigator</span></span>](extract-xml-data-using-xpathnavigator.md)
- [<span data-ttu-id="bf9c1-128">使用 XPathNavigator 访问强类型 XML 数据</span><span class="sxs-lookup"><span data-stu-id="bf9c1-128">Accessing Strongly Typed XML Data Using XPathNavigator</span></span>](accessing-strongly-typed-xml-data-using-xpathnavigator.md)
