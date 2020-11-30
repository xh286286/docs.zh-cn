---
description: '#pragma warning - C# 参考'
title: '#pragma warning - C# 参考'
ms.date: 07/20/2015
f1_keywords:
- '#pragma warning'
helpviewer_keywords:
- '#pragma warning [C#]'
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
ms.openlocfilehash: 5b67d384e37a5e509ce8ebcc5ddeb16a4437ea2b
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "91168525"
---
# <a name="pragma-warning-c-reference"></a><span data-ttu-id="db243-103">#pragma warning（C# 参考）</span><span class="sxs-lookup"><span data-stu-id="db243-103">#pragma warning (C# Reference)</span></span>

<span data-ttu-id="db243-104">`#pragma warning` 可以启用或禁用特定警告。</span><span class="sxs-lookup"><span data-stu-id="db243-104">`#pragma warning` can enable or disable certain warnings.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="db243-105">语法</span><span class="sxs-lookup"><span data-stu-id="db243-105">Syntax</span></span>  
  
```csharp
#pragma warning disable warning-list  
#pragma warning restore warning-list  
```  
  
## <a name="parameters"></a><span data-ttu-id="db243-106">参数</span><span class="sxs-lookup"><span data-stu-id="db243-106">Parameters</span></span>  

 `warning-list`  
 <span data-ttu-id="db243-107">以逗号分隔的警告编号的列表。</span><span class="sxs-lookup"><span data-stu-id="db243-107">A comma-separated list of warning numbers.</span></span> <span data-ttu-id="db243-108">“CS”前缀是可选的。</span><span class="sxs-lookup"><span data-stu-id="db243-108">The "CS" prefix is optional.</span></span>  
  
 <span data-ttu-id="db243-109">未指定警告编号时，`disable` 会禁用所有警告，`restore` 会启用所有警告。</span><span class="sxs-lookup"><span data-stu-id="db243-109">When no warning numbers are specified, `disable` disables all warnings and `restore` enables all warnings.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="db243-110">若要在 Visual Studio 中查找警告编号，请生成项目，然后在“输出”窗口中查找警告编号。</span><span class="sxs-lookup"><span data-stu-id="db243-110">To find warning numbers in Visual Studio, build your project and then look for the warning numbers in the **Output** window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="db243-111">示例</span><span class="sxs-lookup"><span data-stu-id="db243-111">Example</span></span>  
  
```csharp
// pragma_warning.cs  
using System;  
  
#pragma warning disable 414, CS3021  
[CLSCompliant(false)]  
public class C  
{  
    int i = 1;  
    static void Main()  
    {  
    }  
}  
#pragma warning restore CS3021  
[CLSCompliant(false)]  // CS3021  
public class D  
{  
    int i = 1;  
    public static void F()  
    {  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="db243-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="db243-112">See also</span></span>

- [<span data-ttu-id="db243-113">C# 参考</span><span class="sxs-lookup"><span data-stu-id="db243-113">C# Reference</span></span>](../index.md)
- [<span data-ttu-id="db243-114">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="db243-114">C# Programming Guide</span></span>](../../programming-guide/index.md)
- [<span data-ttu-id="db243-115">C# 预处理器指令</span><span class="sxs-lookup"><span data-stu-id="db243-115">C# Preprocessor Directives</span></span>](./index.md)
- [<span data-ttu-id="db243-116">C# 编译器错误</span><span class="sxs-lookup"><span data-stu-id="db243-116">C# Compiler Errors</span></span>](../compiler-messages/index.md)
