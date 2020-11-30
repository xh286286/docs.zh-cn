---
description: -win32res（C# 编译器选项）
title: -win32res（C# 编译器选项）
ms.date: 07/20/2015
f1_keywords:
- /win32res
helpviewer_keywords:
- win32res compiler option
- /win32res compiler option [C#]
- -win32res compiler option [C#]
- win32res compiler option [C#]
ms.assetid: 3c33f750-6948-4c7e-a27e-bef98f77255b
ms.openlocfilehash: 442c788595a01db9c0a1196d9e13b2a98963a38c
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "91204341"
---
# <a name="-win32res-c-compiler-options"></a><span data-ttu-id="b87d9-103">-win32res（C# 编译器选项）</span><span class="sxs-lookup"><span data-stu-id="b87d9-103">-win32res (C# Compiler Options)</span></span>

<span data-ttu-id="b87d9-104">-win32res 选项会在输出文件中插入 Win32 资源。</span><span class="sxs-lookup"><span data-stu-id="b87d9-104">The **-win32res** option inserts a Win32 resource in the output file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b87d9-105">语法</span><span class="sxs-lookup"><span data-stu-id="b87d9-105">Syntax</span></span>  
  
```console  
-win32res:filename  
```  
  
## <a name="arguments"></a><span data-ttu-id="b87d9-106">自变量</span><span class="sxs-lookup"><span data-stu-id="b87d9-106">Arguments</span></span>  

 `filename`  
 <span data-ttu-id="b87d9-107">想向输出文件添加的资源文件。</span><span class="sxs-lookup"><span data-stu-id="b87d9-107">The resource file that you want to add to your output file.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b87d9-108">备注</span><span class="sxs-lookup"><span data-stu-id="b87d9-108">Remarks</span></span>  

 <span data-ttu-id="b87d9-109">Win32 资源文件可以用[资源编译器](resource-compiler-option.md)创建。</span><span class="sxs-lookup"><span data-stu-id="b87d9-109">A Win32 resource file can be created with the [Resource Compiler](resource-compiler-option.md).</span></span> <span data-ttu-id="b87d9-110">在编译 Visual C++ 程序时会调用资源编译器；.res 文件是从 .rc 文件创建的。</span><span class="sxs-lookup"><span data-stu-id="b87d9-110">The Resource Compiler is invoked when you compile a Visual C++ program; a .res file is created from the .rc file.</span></span>  
  
 <span data-ttu-id="b87d9-111">Win32 资源可以包含版本或位图（图标）信息，这些信息有助于在文件资源管理器中标识您的应用程序。</span><span class="sxs-lookup"><span data-stu-id="b87d9-111">A Win32 resource can contain version or bitmap (icon) information that would help identify your application in the File Explorer.</span></span> <span data-ttu-id="b87d9-112">如果不指定 -win32res，编译器将根据程序集版本生成版本信息。</span><span class="sxs-lookup"><span data-stu-id="b87d9-112">If you do not specify **-win32res**, the compiler will generate version information based on the assembly version.</span></span>  
  
 <span data-ttu-id="b87d9-113">请参阅 [-linkresource](./linkresource-compiler-option.md)（引用）或 [-resource](./resource-compiler-option.md)（附加）.NET Framework 资源文件。</span><span class="sxs-lookup"><span data-stu-id="b87d9-113">See [-linkresource](./linkresource-compiler-option.md) (to reference) or [-resource](./resource-compiler-option.md) (to attach) a .NET Framework resource file.</span></span>  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a><span data-ttu-id="b87d9-114">在 Visual Studio 开发环境中设置此编译器选项</span><span class="sxs-lookup"><span data-stu-id="b87d9-114">To set this compiler option in the Visual Studio development environment</span></span>  
  
1. <span data-ttu-id="b87d9-115">打开项目的“属性”页。</span><span class="sxs-lookup"><span data-stu-id="b87d9-115">Open the project's **Properties** page.</span></span>  
  
2. <span data-ttu-id="b87d9-116">单击“应用程序”属性页。</span><span class="sxs-lookup"><span data-stu-id="b87d9-116">Click the **Application** property page.</span></span>  
  
3. <span data-ttu-id="b87d9-117">单击“资源文件”按钮，然后使用组合框选择一个文件。</span><span class="sxs-lookup"><span data-stu-id="b87d9-117">Click on the **Resource File** button and choose a file by using the combo box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b87d9-118">示例</span><span class="sxs-lookup"><span data-stu-id="b87d9-118">Example</span></span>  

 <span data-ttu-id="b87d9-119">编译 `in.cs` 并附加 Win32 资源文件 `rf.res` 以生成 `in.exe`：</span><span class="sxs-lookup"><span data-stu-id="b87d9-119">Compile `in.cs` and attach a Win32 resource file `rf.res` to produce `in.exe`:</span></span>  
  
```console  
csc -win32res:rf.res in.cs  
```  
  
## <a name="see-also"></a><span data-ttu-id="b87d9-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b87d9-120">See also</span></span>

- [<span data-ttu-id="b87d9-121">C# 编译器选项</span><span class="sxs-lookup"><span data-stu-id="b87d9-121">C# Compiler Options</span></span>](./index.md)
- [<span data-ttu-id="b87d9-122">管理项目和解决方案属性</span><span class="sxs-lookup"><span data-stu-id="b87d9-122">Managing Project and Solution Properties</span></span>](/visualstudio/ide/managing-project-and-solution-properties)
