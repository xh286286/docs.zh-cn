---
title: .NET 库中断性变更
description: 列出 .NET Core 1.0-3.0 版核心 .NET 库中的中断性变更。
ms.date: 07/27/2020
ms.openlocfilehash: 0f42429e44776fc70bb99ed3bdf346f0d5dbc9eb
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "96031967"
---
# <a name="core-net-libraries-breaking-changes-in-net-core-10-30"></a><span data-ttu-id="6f4ba-103">.NET Core 1.0-3.0 中的核心 .NET 库中断性变更</span><span class="sxs-lookup"><span data-stu-id="6f4ba-103">Core .NET libraries breaking changes in .NET Core 1.0-3.0</span></span>

<span data-ttu-id="6f4ba-104">核心 .NET 库提供了 .NET Core 使用的基元和其他常规类型。</span><span class="sxs-lookup"><span data-stu-id="6f4ba-104">The core .NET libraries provide the primitives and other general types used by .NET Core.</span></span>

<span data-ttu-id="6f4ba-105">本页记录了以下中断性变更：</span><span class="sxs-lookup"><span data-stu-id="6f4ba-105">The following breaking changes are documented on this page:</span></span>

| <span data-ttu-id="6f4ba-106">重大更改</span><span class="sxs-lookup"><span data-stu-id="6f4ba-106">Breaking change</span></span> | <span data-ttu-id="6f4ba-107">引入的版本</span><span class="sxs-lookup"><span data-stu-id="6f4ba-107">Version introduced</span></span> |
| - | :-: |
| [<span data-ttu-id="6f4ba-108">报告版本的 API 现在报告产品版本而不是文件版本</span><span class="sxs-lookup"><span data-stu-id="6f4ba-108">APIs that report version now report product and not file version</span></span>](#apis-that-report-version-now-report-product-and-not-file-version) | <span data-ttu-id="6f4ba-109">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-109">3.0</span></span> |
| [<span data-ttu-id="6f4ba-110">自定义 EncoderFallbackBuffer 实例无法递归回退</span><span class="sxs-lookup"><span data-stu-id="6f4ba-110">Custom EncoderFallbackBuffer instances cannot fall back recursively</span></span>](#custom-encoderfallbackbuffer-instances-cannot-fall-back-recursively) | <span data-ttu-id="6f4ba-111">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-111">3.0</span></span> |
| [<span data-ttu-id="6f4ba-112">浮点格式设置和分析行为变更</span><span class="sxs-lookup"><span data-stu-id="6f4ba-112">Floating point formatting and parsing behavior changes</span></span>](#floating-point-formatting-and-parsing-behavior-changed) | <span data-ttu-id="6f4ba-113">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-113">3.0</span></span> |
| [<span data-ttu-id="6f4ba-114">浮点分析操作不再失败或引发 OverflowException</span><span class="sxs-lookup"><span data-stu-id="6f4ba-114">Floating-point parsing operations no longer fail or throw an OverflowException</span></span>](#floating-point-parsing-operations-no-longer-fail-or-throw-an-overflowexception) | <span data-ttu-id="6f4ba-115">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-115">3.0</span></span> |
| [<span data-ttu-id="6f4ba-116">InvalidAsynchronousStateException 已移到另一个程序集</span><span class="sxs-lookup"><span data-stu-id="6f4ba-116">InvalidAsynchronousStateException moved to another assembly</span></span>](#invalidasynchronousstateexception-moved-to-another-assembly) | <span data-ttu-id="6f4ba-117">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-117">3.0</span></span> |
| [<span data-ttu-id="6f4ba-118">替换格式错误的 UTF-8 字节序列将遵循 Unicode 准则</span><span class="sxs-lookup"><span data-stu-id="6f4ba-118">Replacing ill-formed UTF-8 byte sequences follows Unicode guidelines</span></span>](#replacing-ill-formed-utf-8-byte-sequences-follows-unicode-guidelines) | <span data-ttu-id="6f4ba-119">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-119">3.0</span></span> |
| [<span data-ttu-id="6f4ba-120">TypeDescriptionProviderAttribute 已移到另一个程序集</span><span class="sxs-lookup"><span data-stu-id="6f4ba-120">TypeDescriptionProviderAttribute moved to another assembly</span></span>](#typedescriptionproviderattribute-moved-to-another-assembly) | <span data-ttu-id="6f4ba-121">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-121">3.0</span></span> |
| [<span data-ttu-id="6f4ba-122">ZipArchiveEntry 不再处理条目大小不一致的存档</span><span class="sxs-lookup"><span data-stu-id="6f4ba-122">ZipArchiveEntry no longer handles archives with inconsistent entry sizes</span></span>](#ziparchiveentry-no-longer-handles-archives-with-inconsistent-entry-sizes) | <span data-ttu-id="6f4ba-123">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-123">3.0</span></span> |
| [<span data-ttu-id="6f4ba-124">FieldInfo.SetValue 将对静态、仅初始化字段引发异常</span><span class="sxs-lookup"><span data-stu-id="6f4ba-124">FieldInfo.SetValue throws exception for static, init-only fields</span></span>](#fieldinfosetvalue-throws-exception-for-static-init-only-fields) | <span data-ttu-id="6f4ba-125">3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-125">3.0</span></span> |
| [<span data-ttu-id="6f4ba-126">添加到内置结构类型的私有字段</span><span class="sxs-lookup"><span data-stu-id="6f4ba-126">Private fields added to built-in struct types</span></span>](#private-fields-added-to-built-in-struct-types) | <span data-ttu-id="6f4ba-127">2.1</span><span class="sxs-lookup"><span data-stu-id="6f4ba-127">2.1</span></span> |
| [<span data-ttu-id="6f4ba-128">UseShellExecute 默认值更改</span><span class="sxs-lookup"><span data-stu-id="6f4ba-128">Change in default value of UseShellExecute</span></span>](#change-in-default-value-of-useshellexecute) | <span data-ttu-id="6f4ba-129">2.1</span><span class="sxs-lookup"><span data-stu-id="6f4ba-129">2.1</span></span> |
| [<span data-ttu-id="6f4ba-130">macOS 上的 OpenSSL 版本</span><span class="sxs-lookup"><span data-stu-id="6f4ba-130">OpenSSL versions on macOS</span></span>](#openssl-versions-on-macos) | <span data-ttu-id="6f4ba-131">2.1</span><span class="sxs-lookup"><span data-stu-id="6f4ba-131">2.1</span></span> |
| [<span data-ttu-id="6f4ba-132">FileSystemInfo.Attributes 引发的 UnauthorizedAccessException</span><span class="sxs-lookup"><span data-stu-id="6f4ba-132">UnauthorizedAccessException thrown by FileSystemInfo.Attributes</span></span>](#unauthorizedaccessexception-thrown-by-filesysteminfoattributes) | <span data-ttu-id="6f4ba-133">1.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-133">1.0</span></span> |
| [<span data-ttu-id="6f4ba-134">不支持处理损坏的进程状态异常</span><span class="sxs-lookup"><span data-stu-id="6f4ba-134">Handling corrupted-process-state exceptions is not supported</span></span>](#handling-corrupted-state-exceptions-is-not-supported) | <span data-ttu-id="6f4ba-135">1.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-135">1.0</span></span> |
| [<span data-ttu-id="6f4ba-136">UriBuilder 属性不再预置前导字符</span><span class="sxs-lookup"><span data-stu-id="6f4ba-136">UriBuilder properties no longer prepend leading characters</span></span>](#uribuilder-properties-no-longer-prepend-leading-characters) | <span data-ttu-id="6f4ba-137">1.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-137">1.0</span></span> |
| [<span data-ttu-id="6f4ba-138">Process.StartInfo 对未启动的进程引发 InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="6f4ba-138">Process.StartInfo throws InvalidOperationException for processes you didn't start</span></span>](#processstartinfo-throws-invalidoperationexception-for-processes-you-didnt-start) | <span data-ttu-id="6f4ba-139">1.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-139">1.0</span></span> |

## <a name="net-core-30"></a><span data-ttu-id="6f4ba-140">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-140">.NET Core 3.0</span></span>

[!INCLUDE[APIs that report version now report product and not file version](~/includes/core-changes/corefx/3.0/version-information-changes.md)]

***

[!INCLUDE[Custom EncoderFallbackBuffer instances cannot fall back recursively](~/includes/core-changes/corefx/3.0/custom-encoderfallbackbuffer-cannot-be-recursive.md)]

<span data-ttu-id="6f4ba-141">\*\*_</span><span class="sxs-lookup"><span data-stu-id="6f4ba-141">\*\*_</span></span>

[!INCLUDE[Floating point formatting and parsing behavior changes](~/includes/core-changes/corefx/3.0/floating-point-changes.md)]

_*_

[!INCLUDE[Floating-point parsing operations no longer fail or throw an OverflowException](~/includes/core-changes/corefx/3.0/floating-point-parsing-does-not-overflow.md)]

_*_

[!INCLUDE[InvalidAsynchronousStateException moved to another assembly](~/includes/core-changes/corefx/3.0/move-invalidasynchronousstateexception.md)]

_*_

[!INCLUDE[NET Core 3.0 follows Unicode best practices when replacing ill-formed UTF-8 byte sequences](~/includes/core-changes/corefx/3.0/net-core-3-0-follows-unicode-utf8-best-practices.md)]

_*_

[!INCLUDE[TypeDescriptionProviderAttribute moved to another assembly](~/includes/core-changes/corefx/3.0/move-typedescriptionproviderattribute.md)]

_*_

[!INCLUDE[ZipArchiveEntry no longer handles archives with inconsistent entry sizes](~/includes/core-changes/corefx/3.0/ziparchiveentry-and-inconsistent-entry-sizes.md)]

_*_

[!INCLUDE [FieldInfo.SetValue throws exception for static, init-only fields](~/includes/core-changes/corefx/3.0/fieldinfo-setvalue-exception.md)]

_*_

## <a name="net-core-21"></a><span data-ttu-id="6f4ba-142">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="6f4ba-142">.NET Core 2.1</span></span>

[!INCLUDE[Private fields added to built-in struct types](~/includes/core-changes/corefx/2.1/instantiate-struct.md)]

_*_

[!INCLUDE[Change in default value of UseShellExecute](~/includes/core-changes/corefx/2.1/process-start-changes.md)]

_*_

[!INCLUDE [OpenSSL versions on macOS](../../../includes/core-changes/corefx/openssl-dependencies-macos.md)]

_*_

## <a name="net-core-10"></a><span data-ttu-id="6f4ba-143">.NET Core 1.0</span><span class="sxs-lookup"><span data-stu-id="6f4ba-143">.NET Core 1.0</span></span>

[!INCLUDE [UnauthorizedAccessException thrown by FileSystemInfo.Attributes](~/includes/core-changes/corefx/1.0/filesysteminfo-attributes-exceptions.md)]

_*_

[!INCLUDE [corrupted-state-exceptions](~/includes/core-changes/corefx/1.0/corrupted-state-exceptions.md)]

_*_

[!INCLUDE [uribuilder-behavior-changes](../../../includes/core-changes/corefx/1.0/uribuilder-behavior-changes.md)]

_*_

[!INCLUDE [startinfo-throws-exception](../../../includes/core-changes/corefx/1.0/startinfo-throws-exception.md)]

<span data-ttu-id="6f4ba-144">_\*\*</span><span class="sxs-lookup"><span data-stu-id="6f4ba-144">_\*\*</span></span>
