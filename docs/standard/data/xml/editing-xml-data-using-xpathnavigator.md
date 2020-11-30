---
title: 使用 XPathNavigator 编辑 XML 数据
ms.date: 03/30/2017
ms.assetid: b1f91616-3115-4264-9821-c66589d11d11
ms.openlocfilehash: c35c63342548a4eaaf8afe68f542c08998de332b
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95687380"
---
# <a name="editing-xml-data-using-xpathnavigator"></a><span data-ttu-id="51b9f-102">使用 XPathNavigator 编辑 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-102">Editing XML Data using XPathNavigator</span></span>

<span data-ttu-id="51b9f-103"><xref:System.Xml.XPath.XPathNavigator> 类提供的方法用于在 <xref:System.Xml.XmlDocument> 对象包含的 XML 文档中插入、修改和移除节点和值。</span><span class="sxs-lookup"><span data-stu-id="51b9f-103">The <xref:System.Xml.XPath.XPathNavigator> class provides methods to insert, modify and remove nodes and values from an XML document contained in an <xref:System.Xml.XmlDocument> object.</span></span> <span data-ttu-id="51b9f-104">为了使用其中任何方法插入、修改和移除节点和值，<xref:System.Xml.XPath.XPathNavigator> 对象必须可编辑，即其 <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> 属性必须为 true。</span><span class="sxs-lookup"><span data-stu-id="51b9f-104">In order to use any of these methods to insert, modify, and remove nodes and values, the <xref:System.Xml.XPath.XPathNavigator> object must be editable, that is, its <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> property must be true.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="51b9f-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="51b9f-105">In This Section</span></span>  

 [<span data-ttu-id="51b9f-106">使用 XPathNavigator 插入 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-106">Insert XML Data using XPathNavigator</span></span>](insert-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="51b9f-107">描述如何使用 <xref:System.Xml.XmlDocument> 类将同级节点、子节点、属性节点和相应值插入 <xref:System.Xml.XPath.XPathNavigator> 对象。</span><span class="sxs-lookup"><span data-stu-id="51b9f-107">Describes how to insert sibling, child, attribute nodes and values in to an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="51b9f-108">使用 XPathNavigator 修改 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-108">Modify XML Data using XPathNavigator</span></span>](modify-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="51b9f-109">描述如何使用 <xref:System.Xml.XmlDocument> 类修改 <xref:System.Xml.XPath.XPathNavigator> 对象中的节点和值。</span><span class="sxs-lookup"><span data-stu-id="51b9f-109">Describes how to modify nodes and values in an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="51b9f-110">使用 XPathNavigator 删除 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-110">Remove XML Data using XPathNavigator</span></span>](remove-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="51b9f-111">描述如何使用 <xref:System.Xml.XmlDocument> 类移除 <xref:System.Xml.XPath.XPathNavigator> 对象中的节点和值。</span><span class="sxs-lookup"><span data-stu-id="51b9f-111">Describes how to remove nodes and values from an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51b9f-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="51b9f-112">See also</span></span>

- <xref:System.Xml.XmlDocument>
- <xref:System.Xml.XPath.XPathDocument>
- <xref:System.Xml.XPath.XPathNavigator>
- [<span data-ttu-id="51b9f-113">使用 XPath 数据模型处理 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-113">Process XML Data Using the XPath Data Model</span></span>](process-xml-data-using-the-xpath-data-model.md)
- [<span data-ttu-id="51b9f-114">使用 XPathDocument 和 XmlDocument 读取 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-114">Reading XML Data using XPathDocument and XmlDocument</span></span>](reading-xml-data-using-xpathdocument-and-xmldocument.md)
- [<span data-ttu-id="51b9f-115">使用 XPathNavigator 选择、计算和匹配 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-115">Selecting, Evaluating and Matching XML Data using XPathNavigator</span></span>](selecting-evaluating-and-matching-xml-data-using-xpathnavigator.md)
- [<span data-ttu-id="51b9f-116">使用 XPathNavigator 访问 XML 数据</span><span class="sxs-lookup"><span data-stu-id="51b9f-116">Accessing XML Data using XPathNavigator</span></span>](accessing-xml-data-using-xpathnavigator.md)
- [<span data-ttu-id="51b9f-117">使用 XPathNavigator 验证架构</span><span class="sxs-lookup"><span data-stu-id="51b9f-117">Schema Validation using XPathNavigator</span></span>](schema-validation-using-xpathnavigator.md)
