---
title: 如何使用 System.Text.Json 编写自定义序列化程序和反序列化程序
description: 了解如何使用 System.Text.Json 命名空间编写适用于 JSON 的自定义序列化程序和反序列化程序。
ms.date: 11/30/2020
no-loc:
- System.Text.Json
- Newtonsoft.Json
helpviewer_keywords:
- JSON serialization
- serializing objects
- serialization
- objects, serializing
ms.openlocfilehash: a01d3c8dd18c114ea1c3aabc402bc841a6025ffe
ms.sourcegitcommit: 721c3e4bdbb1ea0bb420818ec944c538fe5c513a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "96439774"
---
# <a name="how-to-write-custom-serializers-and-deserializers-with-no-locsystemtextjson"></a><span data-ttu-id="5767e-103">如何使用 System.Text.Json 编写自定义序列化程序和反序列化程序</span><span class="sxs-lookup"><span data-stu-id="5767e-103">How to write custom serializers and deserializers with System.Text.Json</span></span>

<span data-ttu-id="5767e-104"><xref:System.Text.Json.Utf8JsonReader?displayProperty=fullName> 是面向 UTF-8 编码 JSON 文本的一个高性能、低分配的只进读取器，从 `ReadOnlySpan<byte>` 或 `ReadOnlySequence<byte>` 读取信息。</span><span class="sxs-lookup"><span data-stu-id="5767e-104"><xref:System.Text.Json.Utf8JsonReader?displayProperty=fullName> is a high-performance, low allocation, forward-only reader for UTF-8 encoded JSON text, read from a `ReadOnlySpan<byte>` or `ReadOnlySequence<byte>`.</span></span> <span data-ttu-id="5767e-105">`Utf8JsonReader` 是一种低级类型，可用于生成自定义分析器和反序列化程序。</span><span class="sxs-lookup"><span data-stu-id="5767e-105">The `Utf8JsonReader` is a low-level type that can be used to build custom parsers and deserializers.</span></span> <span data-ttu-id="5767e-106"><xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType> 方法在后台使用 `Utf8JsonReader`。</span><span class="sxs-lookup"><span data-stu-id="5767e-106">The <xref:System.Text.Json.JsonSerializer.Deserialize%2A?displayProperty=nameWithType> method uses `Utf8JsonReader` under the covers.</span></span>

<span data-ttu-id="5767e-107"><xref:System.Text.Json.Utf8JsonWriter?displayProperty=fullName> 是一种高性能方式，从常见 .NET 类型（例如，`String`、`Int32` 和 `DateTime`）编写 UTF-8 编码的 JSON 文本。</span><span class="sxs-lookup"><span data-stu-id="5767e-107"><xref:System.Text.Json.Utf8JsonWriter?displayProperty=fullName> is a high-performance way to write UTF-8 encoded JSON text from common .NET types like `String`, `Int32`, and `DateTime`.</span></span> <span data-ttu-id="5767e-108">该编写器是一种低级类型，可用于生成自定义序列化程序。</span><span class="sxs-lookup"><span data-stu-id="5767e-108">The writer is a low-level type that can be used to build custom serializers.</span></span> <span data-ttu-id="5767e-109"><xref:System.Text.Json.JsonSerializer.Serialize%2A?displayProperty=nameWithType> 方法在后台使用 `Utf8JsonWriter`。</span><span class="sxs-lookup"><span data-stu-id="5767e-109">The <xref:System.Text.Json.JsonSerializer.Serialize%2A?displayProperty=nameWithType> method uses `Utf8JsonWriter` under the covers.</span></span>

<span data-ttu-id="5767e-110"><xref:System.Text.Json.JsonDocument?displayProperty=fullName> 提供使用 `Utf8JsonReader` 生成只读文档对象模型 (DOM) 的功能。</span><span class="sxs-lookup"><span data-stu-id="5767e-110"><xref:System.Text.Json.JsonDocument?displayProperty=fullName> provides the ability to build a read-only Document Object Model (DOM) by using `Utf8JsonReader`.</span></span> <span data-ttu-id="5767e-111">DOM 提供对 JSON 有效负载中的数据的随机访问。</span><span class="sxs-lookup"><span data-stu-id="5767e-111">The DOM provides random access to data in a JSON payload.</span></span> <span data-ttu-id="5767e-112">可以通过 <xref:System.Text.Json.JsonElement> 类型访问构成有效负载的 JSON 元素。</span><span class="sxs-lookup"><span data-stu-id="5767e-112">The JSON elements that compose the payload can be accessed via the <xref:System.Text.Json.JsonElement> type.</span></span> <span data-ttu-id="5767e-113">`JsonElement` 类型提供数组和对象枚举器，以及用于将 JSON 文本转换为常见 .NET 类型的 API。</span><span class="sxs-lookup"><span data-stu-id="5767e-113">The `JsonElement` type provides array and object enumerators along with APIs to convert JSON text to common .NET types.</span></span> <span data-ttu-id="5767e-114">`JsonDocument` 公开了 <xref:System.Text.Json.JsonDocument.RootElement> 属性。</span><span class="sxs-lookup"><span data-stu-id="5767e-114">`JsonDocument` exposes a <xref:System.Text.Json.JsonDocument.RootElement> property.</span></span>

<span data-ttu-id="5767e-115">以下部分演示如何使用这些工具读取和写入 JSON。</span><span class="sxs-lookup"><span data-stu-id="5767e-115">The following sections show how to use these tools for reading and writing JSON.</span></span>

## <a name="use-jsondocument-for-access-to-data"></a><span data-ttu-id="5767e-116">使用 JsonDocument 访问数据</span><span class="sxs-lookup"><span data-stu-id="5767e-116">Use JsonDocument for access to data</span></span>

<span data-ttu-id="5767e-117">下面的示例演示如何使用 <xref:System.Text.Json.JsonDocument> 类来随机访问 JSON 字符串中的数据：</span><span class="sxs-lookup"><span data-stu-id="5767e-117">The following example shows how to use the <xref:System.Text.Json.JsonDocument> class for random access to data in a JSON string:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/JsonDocumentDataAccess.cs" id="AverageGrades1":::

<span data-ttu-id="5767e-118">前面的代码：</span><span class="sxs-lookup"><span data-stu-id="5767e-118">The preceding code:</span></span>

* <span data-ttu-id="5767e-119">假设要分析的 JSON 处于名为 `jsonString` 的字符串中。</span><span class="sxs-lookup"><span data-stu-id="5767e-119">Assumes the JSON to analyze is in a string named `jsonString`.</span></span>
* <span data-ttu-id="5767e-120">对 `Students` 数组中具有 `Grade` 属性的对象计算平均成绩。</span><span class="sxs-lookup"><span data-stu-id="5767e-120">Calculates an average grade for objects in a `Students` array that have a `Grade` property.</span></span>
* <span data-ttu-id="5767e-121">为没有成绩的学生分配默认成绩 70。</span><span class="sxs-lookup"><span data-stu-id="5767e-121">Assigns a default grade of 70 for students who don't have a grade.</span></span>
* <span data-ttu-id="5767e-122">通过在每次迭代时使 `count` 变量递增来对学生进行计数。</span><span class="sxs-lookup"><span data-stu-id="5767e-122">Counts students by incrementing a `count` variable with each iteration.</span></span> <span data-ttu-id="5767e-123">一种替代方法是调用 <xref:System.Text.Json.JsonElement.GetArrayLength%2A>，如以下示例中所示：</span><span class="sxs-lookup"><span data-stu-id="5767e-123">An alternative is to call <xref:System.Text.Json.JsonElement.GetArrayLength%2A>, as shown in the following example:</span></span>

  :::code language="csharp" source="snippets/system-text-json-how-to/csharp/JsonDocumentDataAccess.cs" id="AverageGrades2":::

<span data-ttu-id="5767e-124">下面是此代码处理的 JSON 示例：</span><span class="sxs-lookup"><span data-stu-id="5767e-124">Here's an example of the JSON that this code processes:</span></span>

:::code language="json" source="snippets/system-text-json-how-to/csharp/GradesPrettyPrint.json":::

## <a name="use-jsondocument-to-write-json"></a><span data-ttu-id="5767e-125">使用 JsonDocument 写入 JSON</span><span class="sxs-lookup"><span data-stu-id="5767e-125">Use JsonDocument to write JSON</span></span>

<span data-ttu-id="5767e-126">下面的示例演示如何通过 <xref:System.Text.Json.JsonDocument> 写入 JSON：</span><span class="sxs-lookup"><span data-stu-id="5767e-126">The following example shows how to write JSON from a <xref:System.Text.Json.JsonDocument>:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/JsonDocumentWriteJson.cs" id="Serialize":::

<span data-ttu-id="5767e-127">前面的代码：</span><span class="sxs-lookup"><span data-stu-id="5767e-127">The preceding code:</span></span>

* <span data-ttu-id="5767e-128">读取 JSON 文件，将数据加载到 `JsonDocument` 中，并将格式化（进行了优质打印的）JSON 写入文件。</span><span class="sxs-lookup"><span data-stu-id="5767e-128">Reads a JSON file, loads the data into a `JsonDocument`, and writes formatted (pretty-printed) JSON to a file.</span></span>
* <span data-ttu-id="5767e-129">使用 <xref:System.Text.Json.JsonDocumentOptions> 可指定允许但会忽略输入 JSON 中的注释。</span><span class="sxs-lookup"><span data-stu-id="5767e-129">Uses <xref:System.Text.Json.JsonDocumentOptions> to specify that comments in the input JSON are allowed but ignored.</span></span>
* <span data-ttu-id="5767e-130">完成后，对编写器调用 <xref:System.Text.Json.Utf8JsonWriter.Flush%2A>。</span><span class="sxs-lookup"><span data-stu-id="5767e-130">When finished, calls <xref:System.Text.Json.Utf8JsonWriter.Flush%2A> on the writer.</span></span> <span data-ttu-id="5767e-131">一种替代方法是让编写器在释放时自动刷新。</span><span class="sxs-lookup"><span data-stu-id="5767e-131">An alternative is to let the writer auto-flush when it's disposed.</span></span>

<span data-ttu-id="5767e-132">下面是要由示例代码处理的 JSON 输入的示例：</span><span class="sxs-lookup"><span data-stu-id="5767e-132">Here's an example of JSON input to be processed by the example code:</span></span>

:::code language="json" source="snippets/system-text-json-how-to/csharp/Grades.json":::

<span data-ttu-id="5767e-133">结果是以下进行了优质打印的 JSON 输出：</span><span class="sxs-lookup"><span data-stu-id="5767e-133">The result is the following pretty-printed JSON output:</span></span>

:::code language="json" source="snippets/system-text-json-how-to/csharp/GradesPrettyPrint.json":::

## <a name="use-utf8jsonwriter"></a><span data-ttu-id="5767e-134">使用 Utf8JsonWriter</span><span class="sxs-lookup"><span data-stu-id="5767e-134">Use Utf8JsonWriter</span></span>

<span data-ttu-id="5767e-135">下面的示例演示如何使用 <xref:System.Text.Json.Utf8JsonWriter> 类：</span><span class="sxs-lookup"><span data-stu-id="5767e-135">The following example shows how to use the <xref:System.Text.Json.Utf8JsonWriter> class:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/Utf8WriterToStream.cs" id="Serialize":::

## <a name="use-utf8jsonreader"></a><span data-ttu-id="5767e-136">使用 Utf8JsonReader</span><span class="sxs-lookup"><span data-stu-id="5767e-136">Use Utf8JsonReader</span></span>

<span data-ttu-id="5767e-137">下面的示例演示如何使用 <xref:System.Text.Json.Utf8JsonReader> 类：</span><span class="sxs-lookup"><span data-stu-id="5767e-137">The following example shows how to use the <xref:System.Text.Json.Utf8JsonReader> class:</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/Utf8ReaderFromBytes.cs" id="Deserialize":::

<span data-ttu-id="5767e-138">前面的代码假设 `jsonUtf8` 变量是包含有效 JSON（编码为 UTF-8）的字节数组。</span><span class="sxs-lookup"><span data-stu-id="5767e-138">The preceding code assumes that the `jsonUtf8` variable is a byte array that contains valid JSON, encoded as UTF-8.</span></span>

### <a name="filter-data-using-utf8jsonreader"></a><span data-ttu-id="5767e-139">使用 Utf8JsonReader 筛选数据</span><span class="sxs-lookup"><span data-stu-id="5767e-139">Filter data using Utf8JsonReader</span></span>

<span data-ttu-id="5767e-140">下面的示例演示如何同步读取文件并搜索值。</span><span class="sxs-lookup"><span data-stu-id="5767e-140">The following example shows how to synchronously read a file, and search for a value.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/Utf8ReaderFromFile.cs":::

<span data-ttu-id="5767e-141">若要获取此示例的异步版本，请参阅 [.NET 示例 JSON 项目](https://github.com/dotnet/samples/blob/18e31a5f1abd4f347bf96bfdc3e40e2cfb36e319/core/json/Program.cs)。</span><span class="sxs-lookup"><span data-stu-id="5767e-141">For an asynchronous version of this example, see [.NET samples JSON project](https://github.com/dotnet/samples/blob/18e31a5f1abd4f347bf96bfdc3e40e2cfb36e319/core/json/Program.cs).</span></span>

<span data-ttu-id="5767e-142">前面的代码：</span><span class="sxs-lookup"><span data-stu-id="5767e-142">The preceding code:</span></span>

* <span data-ttu-id="5767e-143">假设 JSON 包含一个对象数组，并且每个对象都可能包含一个字符串类型的“name”属性。</span><span class="sxs-lookup"><span data-stu-id="5767e-143">Assumes the JSON contains an array of objects and each object may contain a "name" property of type string.</span></span>
* <span data-ttu-id="5767e-144">对对象以及以“University”结尾的属性值进行计数。</span><span class="sxs-lookup"><span data-stu-id="5767e-144">Counts objects and "name" property values that end with "University".</span></span>
* <span data-ttu-id="5767e-145">假设文件编码为 UTF-16，并将它转码为 UTF-8。</span><span class="sxs-lookup"><span data-stu-id="5767e-145">Assumes the file is encoded as UTF-16 and transcodes it into UTF-8.</span></span> <span data-ttu-id="5767e-146">可以使用以下代码，将编码为 UTF-8 的文件直接读入 `ReadOnlySpan<byte>`：</span><span class="sxs-lookup"><span data-stu-id="5767e-146">A file encoded as UTF-8 can be read directly into a `ReadOnlySpan<byte>`, by using the following code:</span></span>

  ```csharp
  ReadOnlySpan<byte> jsonReadOnlySpan = File.ReadAllBytes(fileName);
  ```

  <span data-ttu-id="5767e-147">如果文件包含 UTF-8 字节顺序标记 (BOM)，请在将字节传递给 `Utf8JsonReader` 之前将它删除，因为读取器需要文本。</span><span class="sxs-lookup"><span data-stu-id="5767e-147">If the file contains a UTF-8 byte order mark (BOM), remove it before passing the bytes to the `Utf8JsonReader`, since the reader expects text.</span></span> <span data-ttu-id="5767e-148">否则，BOM 被视为无效 JSON，读取器将引发异常。</span><span class="sxs-lookup"><span data-stu-id="5767e-148">Otherwise, the BOM is considered invalid JSON, and the reader throws an exception.</span></span>

<span data-ttu-id="5767e-149">下面是前面的代码可以读取的 JSON 示例。</span><span class="sxs-lookup"><span data-stu-id="5767e-149">Here's a JSON sample that the preceding code can read.</span></span> <span data-ttu-id="5767e-150">生成的摘要消息为“2 out of 4 have names that end with 'University'”：</span><span class="sxs-lookup"><span data-stu-id="5767e-150">The resulting summary message is "2 out of 4 have names that end with 'University'":</span></span>

:::code language="json" source="snippets/system-text-json-how-to/csharp/Universities.json":::

### <a name="read-from-a-stream-using-utf8jsonreader"></a><span data-ttu-id="5767e-151">使用 Utf8JsonReader 从流中读取</span><span class="sxs-lookup"><span data-stu-id="5767e-151">Read from a stream using Utf8JsonReader</span></span>

<span data-ttu-id="5767e-152">当读取大型文件（例如，1 GB 或更大的文件）时，你可能希望避免一次性将整个文件加载到内存中。</span><span class="sxs-lookup"><span data-stu-id="5767e-152">When reading a large file (a gigabyte or more in size, for example), you might want to avoid having to load the entire file into memory at once.</span></span> <span data-ttu-id="5767e-153">此时，可以使用 <xref:System.IO.FileStream>。</span><span class="sxs-lookup"><span data-stu-id="5767e-153">For this scenario, you can use a <xref:System.IO.FileStream>.</span></span>

<span data-ttu-id="5767e-154">使用 `Utf8JsonReader` 从流中读取时，适用以下规则：</span><span class="sxs-lookup"><span data-stu-id="5767e-154">When using the `Utf8JsonReader` to read from a stream, the following rules apply:</span></span>

* <span data-ttu-id="5767e-155">包含部分 JSON 有效负载的缓冲区必须至少与其中的最大 JSON 令牌一样大，以便读取器可以推进进度。</span><span class="sxs-lookup"><span data-stu-id="5767e-155">The buffer containing the partial JSON payload must be at least as large as the largest JSON token within it so that the reader can make forward progress.</span></span>
* <span data-ttu-id="5767e-156">缓冲区的大小必须至少与 JSON 中的最大空格序列一样大。</span><span class="sxs-lookup"><span data-stu-id="5767e-156">The buffer must be at least as large as the largest sequence of white space within the JSON.</span></span>
* <span data-ttu-id="5767e-157">读取器不会跟踪已读取的数据，直到它完全读取 JSON 有效负载中的下一个 <xref:System.Text.Json.Utf8JsonReader.TokenType%2A>。</span><span class="sxs-lookup"><span data-stu-id="5767e-157">The reader doesn't keep track of the data it has read until it completely reads the next <xref:System.Text.Json.Utf8JsonReader.TokenType%2A> in the JSON payload.</span></span> <span data-ttu-id="5767e-158">因此，当缓冲区中有剩余字节时，必须再次将它们传递给读取器。</span><span class="sxs-lookup"><span data-stu-id="5767e-158">So when there are bytes left over in the buffer, you have to pass them to the reader again.</span></span> <span data-ttu-id="5767e-159">你可以使用 <xref:System.Text.Json.Utf8JsonReader.BytesConsumed%2A> 来确定剩余的字节数。</span><span class="sxs-lookup"><span data-stu-id="5767e-159">You can use <xref:System.Text.Json.Utf8JsonReader.BytesConsumed%2A> to determine how many bytes are left over.</span></span>

<span data-ttu-id="5767e-160">下面的代码演示了如何从流中读取。</span><span class="sxs-lookup"><span data-stu-id="5767e-160">The following code illustrates how to read from a stream.</span></span> <span data-ttu-id="5767e-161">本示例显示了 <xref:System.IO.MemoryStream>。</span><span class="sxs-lookup"><span data-stu-id="5767e-161">The example shows a <xref:System.IO.MemoryStream>.</span></span> <span data-ttu-id="5767e-162">类似的代码将使用 <xref:System.IO.FileStream>，当 `FileStream` 在开头包含 UTF-8 BOM 时除外。</span><span class="sxs-lookup"><span data-stu-id="5767e-162">Similar code will work with a <xref:System.IO.FileStream>, except when the `FileStream` contains a UTF-8 BOM at the start.</span></span> <span data-ttu-id="5767e-163">在这种情况下，需要先从缓冲区中去除这三个字节，然后再将剩余字节传递到 `Utf8JsonReader`。</span><span class="sxs-lookup"><span data-stu-id="5767e-163">In that case, you need to strip those three bytes from the buffer before passing the remaining bytes to the `Utf8JsonReader`.</span></span> <span data-ttu-id="5767e-164">否则，读取器将引发异常，因为 BOM 不被视为 JSON 的有效部分。</span><span class="sxs-lookup"><span data-stu-id="5767e-164">Otherwise the reader would throw an exception, since the BOM is not considered a valid part of the JSON.</span></span>

<span data-ttu-id="5767e-165">示例代码从 4 KB 缓冲区开始，每当发现大小不足以容纳完整的 JSON 令牌（必须容纳完整的令牌，读取器才能推动处理 JSON 有效负载）时，就会使缓冲区大小成倍增加。</span><span class="sxs-lookup"><span data-stu-id="5767e-165">The sample code starts with a 4KB buffer and doubles the buffer size each time it finds that the size is not large enough to fit a complete JSON token, which is required for the reader to make forward progress on the JSON payload.</span></span> <span data-ttu-id="5767e-166">仅当设置的初始缓冲区非常小（例如 10 个字节）时，代码片段中提供的 JSON 示例才会触发缓冲区大小增加。</span><span class="sxs-lookup"><span data-stu-id="5767e-166">The JSON sample provided in the snippet triggers a buffer size increase only if you set a very small initial buffer size, for example, 10 bytes.</span></span> <span data-ttu-id="5767e-167">如果将初始缓冲区大小设置为 10，则 `Console.WriteLine` 语句会说明缓冲区大小增加的原因和影响。</span><span class="sxs-lookup"><span data-stu-id="5767e-167">If you set the initial buffer size to 10, the `Console.WriteLine` statements illustrate the cause and effect of buffer size increases.</span></span> <span data-ttu-id="5767e-168">在初始缓冲区大小为 4KB 时，每个 `Console.WriteLine` 都会显示整个示例 JSON，并且不必增加缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="5767e-168">At the 4KB initial buffer size, the entire sample JSON is shown by each `Console.WriteLine`, and the buffer size never has to be increased.</span></span>

:::code language="csharp" source="snippets/system-text-json-how-to/csharp/Utf8ReaderPartialRead.cs":::

<span data-ttu-id="5767e-169">前面的示例未对缓冲区大小的增长设置任何限制。</span><span class="sxs-lookup"><span data-stu-id="5767e-169">The preceding example sets no limit to how large the buffer can grow.</span></span> <span data-ttu-id="5767e-170">如果令牌大小太大，则代码可能会失败，并出现 <xref:System.OutOfMemoryException> 异常。</span><span class="sxs-lookup"><span data-stu-id="5767e-170">If the token size is too large, the code could fail with an <xref:System.OutOfMemoryException> exception.</span></span> <span data-ttu-id="5767e-171">如果 JSON 包含大小约为 1 GB 或更大的令牌，则会发生这种情况，因为将 1 GB 大小加倍会导致令牌太大，无法放入 `int32` 缓冲区。</span><span class="sxs-lookup"><span data-stu-id="5767e-171">This can happen if the JSON contains a token that is around 1 GB or more in size, because doubling the 1 GB size results in a size that is too large to fit into an `int32` buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="5767e-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="5767e-172">See also</span></span>

* [<span data-ttu-id="5767e-173">System.Text.Json 概述</span><span class="sxs-lookup"><span data-stu-id="5767e-173">System.Text.Json overview</span></span>](system-text-json-overview.md)
* [<span data-ttu-id="5767e-174">如何自定义字符编码</span><span class="sxs-lookup"><span data-stu-id="5767e-174">How to customize character encoding</span></span>](system-text-json-character-encoding.md)
* [<span data-ttu-id="5767e-175">如何编写用于 JSON 序列化的自定义转换器</span><span class="sxs-lookup"><span data-stu-id="5767e-175">How to write custom converters for JSON serialization</span></span>](system-text-json-converters-how-to.md)
* <span data-ttu-id="5767e-176">[System.Text.Json API 参考](xref:System.Text.Json)</span><span class="sxs-lookup"><span data-stu-id="5767e-176">[System.Text.Json API reference](xref:System.Text.Json)</span></span>
