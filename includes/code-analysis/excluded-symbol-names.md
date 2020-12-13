---
ms.openlocfilehash: 83644b9205d650da68c910095dd1d22a14940c44
ms.sourcegitcommit: 9b877e160c326577e8aa5ead22a937110d80fa44
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/11/2020
ms.locfileid: "97366847"
---
### <a name="exclude-specific-symbols"></a><span data-ttu-id="1f7a2-101">排除特定符号</span><span class="sxs-lookup"><span data-stu-id="1f7a2-101">Exclude specific symbols</span></span>

<span data-ttu-id="1f7a2-102">可以从分析中排除特定符号，如类型和方法。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-102">You can exclude specific symbols, such as types and methods, from analysis.</span></span> <span data-ttu-id="1f7a2-103">例如，若要指定规则不应在任何名为的类型中的任何代码上运行 `MyType` ，请将以下键-值对添加到项目中的 *editorconfig* 文件中：</span><span class="sxs-lookup"><span data-stu-id="1f7a2-103">For example, to specify that the rule should not run on any code within types named `MyType`, add the following key-value pair to an *.editorconfig* file in your project:</span></span>

```ini
dotnet_code_quality.CAXXXX.excluded_symbol_names = MyType
```

<span data-ttu-id="1f7a2-104">选项值中允许的符号名称格式 (用 `|`) 分隔：</span><span class="sxs-lookup"><span data-stu-id="1f7a2-104">Allowed symbol name formats in the option value (separated by `|`):</span></span>

- <span data-ttu-id="1f7a2-105">仅符号名称 (包含名称的所有符号，而不管包含类型或命名空间) 。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-105">Symbol name only (includes all symbols with the name, regardless of the containing type or namespace).</span></span>
- <span data-ttu-id="1f7a2-106">符号 [文档 ID 格式](../../docs/csharp/programming-guide/xmldoc/processing-the-xml-file.md#id-strings)的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-106">Fully qualified names in the symbol's [documentation ID format](../../docs/csharp/programming-guide/xmldoc/processing-the-xml-file.md#id-strings).</span></span> <span data-ttu-id="1f7a2-107">每个符号名称都需要符号类型前缀，如 `M:` 用于方法、 `T:` 类型的和 `N:` 命名空间。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-107">Each symbol name requires a symbol-kind prefix, such as `M:` for methods, `T:` for types, and `N:` for namespaces.</span></span>
- <span data-ttu-id="1f7a2-108">`.ctor` 对于构造函数和 `.cctor` 静态构造函数。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-108">`.ctor` for constructors and `.cctor` for static constructors.</span></span>

<span data-ttu-id="1f7a2-109">示例：</span><span class="sxs-lookup"><span data-stu-id="1f7a2-109">Examples:</span></span>

| <span data-ttu-id="1f7a2-110">选项值</span><span class="sxs-lookup"><span data-stu-id="1f7a2-110">Option Value</span></span> | <span data-ttu-id="1f7a2-111">总结</span><span class="sxs-lookup"><span data-stu-id="1f7a2-111">Summary</span></span> |
| --- | --- |
|`dotnet_code_quality.CAXXXX.excluded_symbol_names = MyType` | <span data-ttu-id="1f7a2-112">匹配名为的所有符号 `MyType` 。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-112">Matches all symbols named `MyType`.</span></span> |
|`dotnet_code_quality.CAXXXX.excluded_symbol_names = MyType1|MyType2` | <span data-ttu-id="1f7a2-113">匹配名为 `MyType1` 或的所有符号 `MyType2` 。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-113">Matches all symbols named either `MyType1` or `MyType2`.</span></span> |
|`dotnet_code_quality.CAXXXX.excluded_symbol_names = M:NS.MyType.MyMethod(ParamType)` | <span data-ttu-id="1f7a2-114">将特定方法 `MyMethod` 与指定的完全限定的签名相匹配。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-114">Matches specific method `MyMethod` with the specified fully qualified signature.</span></span> |
|`dotnet_code_quality.CAXXXX.excluded_symbol_names = M:NS1.MyType1.MyMethod1(ParamType)|M:NS2.MyType2.MyMethod2(ParamType)` | <span data-ttu-id="1f7a2-115">将特定方法 `MyMethod1` 与 `MyMethod2` 相应的完全限定的签名相匹配。</span><span class="sxs-lookup"><span data-stu-id="1f7a2-115">Matches specific methods `MyMethod1` and `MyMethod2` with the respective fully qualified signatures.</span></span> |
