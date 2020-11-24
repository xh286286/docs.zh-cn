---
title: 将对象层次结构映射到 XML 数据
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 450e350b-6a68-4634-a2a5-33f4dc33baf0
ms.openlocfilehash: 97cc7558f51b7bcbdb5201ef0f0c463da8f2c070
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94822602"
---
# <a name="mapping-the-object-hierarchy-to-xml-data"></a><span data-ttu-id="ecfa9-102">将对象层次结构映射到 XML 数据</span><span class="sxs-lookup"><span data-stu-id="ecfa9-102">Mapping the Object Hierarchy to XML Data</span></span>
<span data-ttu-id="ecfa9-103">当 XML 文档在内存中时，概念上的表示形式是树。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-103">When an XML document is in memory, the conceptual representation is a tree.</span></span> <span data-ttu-id="ecfa9-104">编程时可使用对象层次结构访问树节点。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-104">For programming, you have an object hierarchy to access the nodes of the tree.</span></span> <span data-ttu-id="ecfa9-105">下面的示例显示 XML 内容如何成为节点。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-105">The following example shows you how the XML content becomes nodes.</span></span>  
  
 <span data-ttu-id="ecfa9-106">当将 XML 读入 XML 文档对象模型 (DOM) 中时，各片段被转换为节点，这些节点保留有关自身的附加元数据，如它们的节点类型和值。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-106">As the XML is read into the XML Document Object Model (DOM), the pieces are translated into nodes, and these nodes retain additional metadata about themselves, such as their node type and values.</span></span> <span data-ttu-id="ecfa9-107">节点类型是节点的对象，确定可执行的操作以及可设置或检索的属性。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-107">The node type is its object and is what determines what actions can be performed and what properties can be set or retrieved.</span></span>  
  
 <span data-ttu-id="ecfa9-108">如果具有下面的简单 XML：</span><span class="sxs-lookup"><span data-stu-id="ecfa9-108">If you have the following simple XML:</span></span>  
  
 <span data-ttu-id="ecfa9-109">**输入**</span><span class="sxs-lookup"><span data-stu-id="ecfa9-109">**Input**</span></span>  
  
```xml  
<book>  
    <title>The Handmaid's Tale</title>  
</book>  
```  
  
 <span data-ttu-id="ecfa9-110">输入在内存中表示为具有分配的节点类型属性的下列节点树：</span><span class="sxs-lookup"><span data-stu-id="ecfa9-110">The input is represented in memory as the following node tree with the assigned node type property:</span></span>  
  
 <span data-ttu-id="ecfa9-111">![示例节点树](media/simple-xml.gif "Simple_XML")</span><span class="sxs-lookup"><span data-stu-id="ecfa9-111">![example node tree](media/simple-xml.gif "Simple_XML")</span></span>  
<span data-ttu-id="ecfa9-112">book 和 title 节点树表示形式</span><span class="sxs-lookup"><span data-stu-id="ecfa9-112">Book and title node tree representation</span></span>  
  
 <span data-ttu-id="ecfa9-113">`book` 元素成为 XmlElement 对象，下一个元素 `title` 也成为 XmlElement，而元素内容成为 XmlText 对象。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-113">The `book` element becomes an **XmlElement** object, the next element, `title`, also becomes an **XmlElement**, while the element content becomes an **XmlText** object.</span></span> <span data-ttu-id="ecfa9-114">查看 XmlElement 方法和属性可以得知，这些方法和属性不同于 XmlText 对象的方法和属性。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-114">In looking at the **XmlElement** methods and properties, the methods and properties are different than the methods and properties available on an **XmlText** object.</span></span> <span data-ttu-id="ecfa9-115">因此，知道 XML 标记成为的节点类型至关重要，因为其节点类型确定可以执行的操作。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-115">So knowing what node type the XML markup becomes is vital, as its node type determines the actions that can be performed.</span></span>  
  
 <span data-ttu-id="ecfa9-116">下面的示例读入 XML 数据并根据节点类型写出不同的文本。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-116">The following example reads in XML data and writes out different text, depending on the node type.</span></span> <span data-ttu-id="ecfa9-117">将下面的 XML 数据文件用作输入文件 items.xml：</span><span class="sxs-lookup"><span data-stu-id="ecfa9-117">Using the following XML data file as input, **items.xml**:</span></span>  
  
 <span data-ttu-id="ecfa9-118">**输入**</span><span class="sxs-lookup"><span data-stu-id="ecfa9-118">**Input**</span></span>  
  
```xml  
<?xml version="1.0"?>  
<!-- This is a sample XML document -->  
<!DOCTYPE Items [<!ENTITY number "123">]>  
<Items>  
  <Item>Test with an entity: &number;</Item>  
  <Item>test with a child element <more/> stuff</Item>  
  <Item>test with a CDATA section <![CDATA[<456>]]> def</Item>  
  <Item>Test with a char entity: A</Item>  
  <!-- Fourteen chars in this element.-->  
  <Item>1234567890ABCD</Item>  
</Items>  
```  
  
 <span data-ttu-id="ecfa9-119">下面的代码示例读取 items.xml 文件，并显示每个节点类型的信息。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-119">The following code example reads the **items.xml** file and displays information for each node type.</span></span>  
  
```vb  
Imports System  
Imports System.IO  
Imports System.Xml  
  
Public Class Sample  
    Private Const filename As String = "items.xml"  
  
    Public Shared Sub Main()  
  
        Dim reader As XmlTextReader = Nothing  
  
        Try  
            ' Load the reader with the data file and
            'ignore all white space nodes.
            reader = New XmlTextReader(filename)  
            reader.WhitespaceHandling = WhitespaceHandling.None  
  
            ' Parse the file and display each of the nodes.  
            While reader.Read()  
                Select Case reader.NodeType  
                    Case XmlNodeType.Element  
                        Console.Write("<{0}>", reader.Name)  
                    Case XmlNodeType.Text  
                        Console.Write(reader.Value)  
                    Case XmlNodeType.CDATA  
                        Console.Write("<![CDATA[{0}]]>", reader.Value)  
                    Case XmlNodeType.ProcessingInstruction  
                        Console.Write("<?{0} {1}?>", reader.Name, reader.Value)  
                    Case XmlNodeType.Comment  
                        Console.Write("<!--{0}-->", reader.Value)  
                    Case XmlNodeType.XmlDeclaration  
                        Console.Write("<?xml version='1.0'?>")  
                    Case XmlNodeType.Document  
                    Case XmlNodeType.DocumentType  
                        Console.Write("<!DOCTYPE {0} [{1}]", reader.Name, reader.Value)  
                    Case XmlNodeType.EntityReference  
                        Console.Write(reader.Name)  
                    Case XmlNodeType.EndElement  
                        Console.Write("</{0}>", reader.Name)  
                End Select  
            End While  
  
        Finally  
            If Not (reader Is Nothing) Then  
                reader.Close()  
            End If  
        End Try  
    End Sub 'Main ' End class  
End Class 'Sample  
```  
  
```csharp  
using System;  
using System.IO;  
using System.Xml;  
  
public class Sample  
{  
    private const String filename = "items.xml";  
  
    public static void Main()  
    {  
        XmlTextReader reader = null;  
  
        try  
        {  
            // Load the reader with the data file and ignore
            // all white space nodes.  
            reader = new XmlTextReader(filename);  
            reader.WhitespaceHandling = WhitespaceHandling.None;  
  
            // Parse the file and display each of the nodes.  
            while (reader.Read())  
            {  
                switch (reader.NodeType)  
                {  
                    case XmlNodeType.Element:  
                        Console.Write("<{0}>", reader.Name);  
                        break;  
                    case XmlNodeType.Text:  
                        Console.Write(reader.Value);  
                        break;  
                    case XmlNodeType.CDATA:  
                        Console.Write("<![CDATA[{0}]]>", reader.Value);  
                        break;  
                    case XmlNodeType.ProcessingInstruction:  
                        Console.Write("<?{0} {1}?>", reader.Name, reader.Value);  
                        break;  
                    case XmlNodeType.Comment:  
                        Console.Write("<!--{0}-->", reader.Value);  
                        break;  
                    case XmlNodeType.XmlDeclaration:  
                        Console.Write("<?xml version='1.0'?>");  
                        break;  
                    case XmlNodeType.Document:  
                        break;  
                    case XmlNodeType.DocumentType:  
                        Console.Write("<!DOCTYPE {0} [{1}]", reader.Name, reader.Value);  
                        break;  
                    case XmlNodeType.EntityReference:  
                        Console.Write(reader.Name);  
                        break;  
                    case XmlNodeType.EndElement:  
                        Console.Write("</{0}>", reader.Name);  
                        break;  
                }  
            }  
        }  
  
        finally  
        {  
            if (reader != null)  
                reader.Close();  
        }  
    }  
} // End class  
```  
  
 <span data-ttu-id="ecfa9-120">此示例的输出显示数据到节点类型的映射。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-120">The output from the example reveals the mapping of the data to the node types.</span></span>  
  
 <span data-ttu-id="ecfa9-121">**输出**</span><span class="sxs-lookup"><span data-stu-id="ecfa9-121">**Output**</span></span>  
  
```xml  
<?xml version='1.0'?><!--This is a sample XML document --><!DOCTYPE Items [<!ENTITY number "123">]<Items><Item>Test with an entity: 123</Item><Item>test with a child element <more> stuff</Item><Item>test with a CDATA section <![CDATA[<456>]]> def</Item><Item>Test with a char entity: A</Item><--Fourteen chars in this element.--><Item>1234567890ABCD</Item></Items>
```  
  
 <span data-ttu-id="ecfa9-122">通过逐行获取输入并使用从代码生成的输出，可以使用下表分析哪个节点测试生成哪些输出行，从而了解哪些 XML 数据成为哪种节点类型。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-122">Taking the input one line at a time and using the output generated from the code, you can use the following table to analyze what node test generated which lines of output, thereby understanding what XML data became what kind of node type.</span></span>  
  
|<span data-ttu-id="ecfa9-123">输入</span><span class="sxs-lookup"><span data-stu-id="ecfa9-123">Input</span></span>|<span data-ttu-id="ecfa9-124">Output</span><span class="sxs-lookup"><span data-stu-id="ecfa9-124">Output</span></span>|<span data-ttu-id="ecfa9-125">节点类型测试</span><span class="sxs-lookup"><span data-stu-id="ecfa9-125">Node Type Test</span></span>|  
|-----------|------------|--------------------|  
|\<?xml version="1.0"?>|\<?xml version='1.0'?>|<span data-ttu-id="ecfa9-126">XmlNodeType.XmlDeclaration</span><span class="sxs-lookup"><span data-stu-id="ecfa9-126">XmlNodeType.XmlDeclaration</span></span>|  
|\<!-- This is a sample XML document -->|\<!--This is a sample XML document -->|<span data-ttu-id="ecfa9-127">XmlNodeType.Comment</span><span class="sxs-lookup"><span data-stu-id="ecfa9-127">XmlNodeType.Comment</span></span>|  
|<span data-ttu-id="ecfa9-128">\<!DOCTYPE Items [\<!ENTITY number "123">]></span><span class="sxs-lookup"><span data-stu-id="ecfa9-128">\<!DOCTYPE Items [\<!ENTITY number "123">]></span></span>|<span data-ttu-id="ecfa9-129">\<!DOCTYPE Items [\<!ENTITY number "123">]</span><span class="sxs-lookup"><span data-stu-id="ecfa9-129">\<!DOCTYPE Items [\<!ENTITY number "123">]</span></span>|<span data-ttu-id="ecfa9-130">XmlNodeType.DocumentType</span><span class="sxs-lookup"><span data-stu-id="ecfa9-130">XmlNodeType.DocumentType</span></span>|  
|\<Items>|\<Items>|<span data-ttu-id="ecfa9-131">XmlNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-131">XmlNodeType.Element</span></span>|  
|\<Item>|\<Item>|<span data-ttu-id="ecfa9-132">XmlNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-132">XmlNodeType.Element</span></span>|  
|<span data-ttu-id="ecfa9-133">Test with an entity: &number;</span><span class="sxs-lookup"><span data-stu-id="ecfa9-133">Test with an entity: &number;</span></span>|<span data-ttu-id="ecfa9-134">与以下实体一起测试：123</span><span class="sxs-lookup"><span data-stu-id="ecfa9-134">Test with an entity: 123</span></span>|<span data-ttu-id="ecfa9-135">XmlNodeType.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-135">XmlNodeType.Text</span></span>|  
|\</Item>|\</Item>|<span data-ttu-id="ecfa9-136">XmlNodeType.EndElement</span><span class="sxs-lookup"><span data-stu-id="ecfa9-136">XmlNodeType.EndElement</span></span>|  
|\<Item>|\<Item>|<span data-ttu-id="ecfa9-137">XmNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-137">XmNodeType.Element</span></span>|  
|<span data-ttu-id="ecfa9-138">与子元素一起测试</span><span class="sxs-lookup"><span data-stu-id="ecfa9-138">test with a child element</span></span>|<span data-ttu-id="ecfa9-139">与子元素一起测试</span><span class="sxs-lookup"><span data-stu-id="ecfa9-139">test with a child element</span></span>|<span data-ttu-id="ecfa9-140">XmlNodeType.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-140">XmlNodeType.Text</span></span>|  
|\<more>|\<more>|<span data-ttu-id="ecfa9-141">XmlNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-141">XmlNodeType.Element</span></span>|  
|<span data-ttu-id="ecfa9-142">stuff</span><span class="sxs-lookup"><span data-stu-id="ecfa9-142">stuff</span></span>|<span data-ttu-id="ecfa9-143">stuff</span><span class="sxs-lookup"><span data-stu-id="ecfa9-143">stuff</span></span>|<span data-ttu-id="ecfa9-144">XmlNodeType.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-144">XmlNodeType.Text</span></span>|  
|\</Item>|\</Item>|<span data-ttu-id="ecfa9-145">XmlNodeType.EndElement</span><span class="sxs-lookup"><span data-stu-id="ecfa9-145">XmlNodeType.EndElement</span></span>|  
|\<Item>|\<Item>|<span data-ttu-id="ecfa9-146">XmlNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-146">XmlNodeType.Element</span></span>|  
|<span data-ttu-id="ecfa9-147">与 CDATA 节一起测试</span><span class="sxs-lookup"><span data-stu-id="ecfa9-147">test with a CDATA section</span></span>|<span data-ttu-id="ecfa9-148">与 CDATA 节一起测试</span><span class="sxs-lookup"><span data-stu-id="ecfa9-148">test with a CDATA section</span></span>|<span data-ttu-id="ecfa9-149">XmlTest.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-149">XmlTest.Text</span></span>|  
|<span data-ttu-id="ecfa9-150"><![CDATA[\<456>]]\></span><span class="sxs-lookup"><span data-stu-id="ecfa9-150"><![CDATA[\<456>]]\></span></span>|<span data-ttu-id="ecfa9-151"><![CDATA[\<456>]]\></span><span class="sxs-lookup"><span data-stu-id="ecfa9-151"><![CDATA[\<456>]]\></span></span>|<span data-ttu-id="ecfa9-152">XmlTest.CDATA</span><span class="sxs-lookup"><span data-stu-id="ecfa9-152">XmlTest.CDATA</span></span>|  
|<span data-ttu-id="ecfa9-153">def</span><span class="sxs-lookup"><span data-stu-id="ecfa9-153">def</span></span>|<span data-ttu-id="ecfa9-154">def</span><span class="sxs-lookup"><span data-stu-id="ecfa9-154">def</span></span>|<span data-ttu-id="ecfa9-155">XmlNodeType.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-155">XmlNodeType.Text</span></span>|  
|\</Item>|\</Item>|<span data-ttu-id="ecfa9-156">XmlNodeType.EndElement</span><span class="sxs-lookup"><span data-stu-id="ecfa9-156">XmlNodeType.EndElement</span></span>|  
|\<Item>|\<Item>|<span data-ttu-id="ecfa9-157">XmlNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-157">XmlNodeType.Element</span></span>|  
|<span data-ttu-id="ecfa9-158">Test with a char entity: &\#65;</span><span class="sxs-lookup"><span data-stu-id="ecfa9-158">Test with a char entity: &\#65;</span></span>|<span data-ttu-id="ecfa9-159">与字符实体一起测试：包含当前请求的 URL 的</span><span class="sxs-lookup"><span data-stu-id="ecfa9-159">Test with a char entity: A</span></span>|<span data-ttu-id="ecfa9-160">XmlNodeType.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-160">XmlNodeType.Text</span></span>|  
|\</Item>|\</Item>|<span data-ttu-id="ecfa9-161">XmlNodeType.EndElement</span><span class="sxs-lookup"><span data-stu-id="ecfa9-161">XmlNodeType.EndElement</span></span>|  
|\<!-- Fourteen chars in this element.-->|\<--Fourteen chars in this element.-->|<span data-ttu-id="ecfa9-162">XmlNodeType.Comment</span><span class="sxs-lookup"><span data-stu-id="ecfa9-162">XmlNodeType.Comment</span></span>|  
|\<Item>|\<Item>|<span data-ttu-id="ecfa9-163">XmlNodeType.Element</span><span class="sxs-lookup"><span data-stu-id="ecfa9-163">XmlNodeType.Element</span></span>|  
|<span data-ttu-id="ecfa9-164">1234567890ABCD</span><span class="sxs-lookup"><span data-stu-id="ecfa9-164">1234567890ABCD</span></span>|<span data-ttu-id="ecfa9-165">1234567890ABCD</span><span class="sxs-lookup"><span data-stu-id="ecfa9-165">1234567890ABCD</span></span>|<span data-ttu-id="ecfa9-166">XmlNodeType.Text</span><span class="sxs-lookup"><span data-stu-id="ecfa9-166">XmlNodeType.Text</span></span>|  
|\</Item>|\</Item>|<span data-ttu-id="ecfa9-167">XmlNodeType.EndElement</span><span class="sxs-lookup"><span data-stu-id="ecfa9-167">XmlNodeType.EndElement</span></span>|  
|\</Items>|\</Items>|<span data-ttu-id="ecfa9-168">XmlNodeType.EndElement</span><span class="sxs-lookup"><span data-stu-id="ecfa9-168">XmlNodeType.EndElement</span></span>|  
  
 <span data-ttu-id="ecfa9-169">您必须知道分配的节点类型，因为节点类型控制哪些操作有效，以及可以设置和检索哪些属性。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-169">You must know what node type is assigned, as the node type controls what kinds of actions are valid and what kind of properties you can set and retrieve.</span></span>  
  
 <span data-ttu-id="ecfa9-170">当 PreserveWhitespace 标志将数据加载到 DOM 中时，就会控制空格的节点创建。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-170">Node creation for white space is controlled when the data is loaded into the DOM by the **PreserveWhitespace** flag.</span></span> <span data-ttu-id="ecfa9-171">有关详细信息，请参阅[加载 DOM 时处理空格和有效空格](white-space-and-significant-white-space-handling-when-loading-the-dom.md)。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-171">For more information, see [White Space and Significant White Space Handling when Loading the DOM](white-space-and-significant-white-space-handling-when-loading-the-dom.md).</span></span>  
  
 <span data-ttu-id="ecfa9-172">若要向 DOM 添加新节点，请参阅[将节点插入 XML 文档中](inserting-nodes-into-an-xml-document.md)。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-172">To add new nodes to the DOM, see [Inserting Nodes into an XML Document](inserting-nodes-into-an-xml-document.md).</span></span> <span data-ttu-id="ecfa9-173">若要从 DOM 中删除节点，请参阅[从 XML 文档中删除节点、内容和值](removing-nodes-content-and-values-from-an-xml-document.md)。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-173">To remove nodes from the DOM, see [Removing Nodes, Content, and Values from an XML Document](removing-nodes-content-and-values-from-an-xml-document.md).</span></span> <span data-ttu-id="ecfa9-174">若要修改 DOM 中的节点内容，请参阅[修改 XML 文档中的节点、内容和值](modifying-nodes-content-and-values-in-an-xml-document.md)。</span><span class="sxs-lookup"><span data-stu-id="ecfa9-174">To modify the content of nodes in the DOM, see [Modifying Nodes, Content, and Values in an XML Document](modifying-nodes-content-and-values-in-an-xml-document.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ecfa9-175">请参阅</span><span class="sxs-lookup"><span data-stu-id="ecfa9-175">See also</span></span>

- [<span data-ttu-id="ecfa9-176">XML 文档对象模型 (DOM)</span><span class="sxs-lookup"><span data-stu-id="ecfa9-176">XML Document Object Model (DOM)</span></span>](xml-document-object-model-dom.md)
