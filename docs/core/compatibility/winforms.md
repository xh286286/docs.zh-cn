---
title: Windows 窗体重大更改
description: 列出 .NET Core 3.0 和 3.1 的 Windows 窗体中断性变更。
ms.date: 09/08/2020
ms.openlocfilehash: b944f7eea89b61f41feb8eef99e949c2d6017960
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95726426"
---
# <a name="breaking-changes-in-windows-forms-for-net-core-30-and-31"></a><span data-ttu-id="29065-103">.NET Core 3.0 和 3.1 的 Windows 窗体中断性变更</span><span class="sxs-lookup"><span data-stu-id="29065-103">Breaking changes in Windows Forms for .NET Core 3.0 and 3.1</span></span>

<span data-ttu-id="29065-104">已在 .NET Core 的版本 3.0 中添加 Windows 窗体支持。</span><span class="sxs-lookup"><span data-stu-id="29065-104">Windows Forms support was added to .NET Core in version 3.0.</span></span> <span data-ttu-id="29065-105">本文按引入了中断性变更的 .NET 版本列出了 Windows 窗体的中断性变更。</span><span class="sxs-lookup"><span data-stu-id="29065-105">This article lists breaking changes for Windows Forms by the .NET version in which they were introduced.</span></span> <span data-ttu-id="29065-106">如果要从 .NET Framework 或 .NET Core 的早期版本（3.0 或更高版本）升级 Windows 窗体应用，本文能为你提供帮助。</span><span class="sxs-lookup"><span data-stu-id="29065-106">If you're upgrading a Windows Forms app from .NET Framework or from a previous version of .NET Core (3.0 or later), this article applies to you.</span></span>

<span data-ttu-id="29065-107">本页记录了以下中断性变更：</span><span class="sxs-lookup"><span data-stu-id="29065-107">The following breaking changes are documented on this page:</span></span>

| <span data-ttu-id="29065-108">重大更改</span><span class="sxs-lookup"><span data-stu-id="29065-108">Breaking change</span></span> | <span data-ttu-id="29065-109">引入的版本</span><span class="sxs-lookup"><span data-stu-id="29065-109">Version introduced</span></span> |
| - | :-: |
| [<span data-ttu-id="29065-110">已删除的控件</span><span class="sxs-lookup"><span data-stu-id="29065-110">Removed controls</span></span>](#removed-controls) | <span data-ttu-id="29065-111">3.1</span><span class="sxs-lookup"><span data-stu-id="29065-111">3.1</span></span> |
| [<span data-ttu-id="29065-112">如果显示工具提示，则不引发 CellFormatting 事件</span><span class="sxs-lookup"><span data-stu-id="29065-112">CellFormatting event not raised if tooltip is shown</span></span>](#cellformatting-event-not-raised-if-tooltip-is-shown) | <span data-ttu-id="29065-113">3.1</span><span class="sxs-lookup"><span data-stu-id="29065-113">3.1</span></span> |
| [<span data-ttu-id="29065-114">Control.DefaultFont 已更改为 Segoe UI 9 pt</span><span class="sxs-lookup"><span data-stu-id="29065-114">Control.DefaultFont changed to Segoe UI 9 pt</span></span>](#default-control-font-changed-to-segoe-ui-9-pt) | <span data-ttu-id="29065-115">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-115">3.0</span></span> |
| [<span data-ttu-id="29065-116">FolderBrowserDialog 的现代化</span><span class="sxs-lookup"><span data-stu-id="29065-116">Modernization of the FolderBrowserDialog</span></span>](#modernization-of-the-folderbrowserdialog) | <span data-ttu-id="29065-117">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-117">3.0</span></span> |
| [<span data-ttu-id="29065-118">已从一些 Windows 窗体类型中删除 SerializableAttribute</span><span class="sxs-lookup"><span data-stu-id="29065-118">SerializableAttribute removed from some Windows Forms types</span></span>](#serializableattribute-removed-from-some-windows-forms-types) | <span data-ttu-id="29065-119">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-119">3.0</span></span> |
| [<span data-ttu-id="29065-120">不支持 AllowUpdateChildControlIndexForTabControls 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-120">AllowUpdateChildControlIndexForTabControls compatibility switch not supported</span></span>](#allowupdatechildcontrolindexfortabcontrols-compatibility-switch-not-supported) | <span data-ttu-id="29065-121">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-121">3.0</span></span> |
| [<span data-ttu-id="29065-122">不支持 DomainUpDown.UseLegacyScrolling 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-122">DomainUpDown.UseLegacyScrolling compatibility switch not supported</span></span>](#domainupdownuselegacyscrolling-compatibility-switch-not-supported) | <span data-ttu-id="29065-123">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-123">3.0</span></span> |
| [<span data-ttu-id="29065-124">不支持 DoNotLoadLatestRichEditControl 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-124">DoNotLoadLatestRichEditControl compatibility switch not supported</span></span>](#donotloadlatestricheditcontrol-compatibility-switch-not-supported) | <span data-ttu-id="29065-125">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-125">3.0</span></span> |
| [<span data-ttu-id="29065-126">不支持 DoNotSupportSelectAllShortcutInMultilineTextBox 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-126">DoNotSupportSelectAllShortcutInMultilineTextBox compatibility switch not supported</span></span>](#donotsupportselectallshortcutinmultilinetextbox-compatibility-switch-not-supported) | <span data-ttu-id="29065-127">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-127">3.0</span></span> |
| [<span data-ttu-id="29065-128">不支持 DontSupportReentrantFilterMessage 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-128">DontSupportReentrantFilterMessage compatibility switch not supported</span></span>](#dontsupportreentrantfiltermessage-compatibility-switch-not-supported) | <span data-ttu-id="29065-129">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-129">3.0</span></span> |
| [<span data-ttu-id="29065-130">不支持 EnableVisualStyleValidation 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-130">EnableVisualStyleValidation compatibility switch not supported</span></span>](#enablevisualstylevalidation-compatibility-switch-not-supported) | <span data-ttu-id="29065-131">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-131">3.0</span></span> |
| [<span data-ttu-id="29065-132">不支持 UseLegacyContextMenuStripSourceControlValue 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-132">UseLegacyContextMenuStripSourceControlValue compatibility switch not supported</span></span>](#uselegacycontextmenustripsourcecontrolvalue-compatibility-switch-not-supported) | <span data-ttu-id="29065-133">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-133">3.0</span></span> |
| [<span data-ttu-id="29065-134">不支持 UseLegacyImages 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="29065-134">UseLegacyImages compatibility switch not supported</span></span>](#uselegacyimages-compatibility-switch-not-supported) | <span data-ttu-id="29065-135">3.0</span><span class="sxs-lookup"><span data-stu-id="29065-135">3.0</span></span> |

## <a name="net-core-31"></a><span data-ttu-id="29065-136">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="29065-136">.NET Core 3.1</span></span>

[!INCLUDE[Removed controls](~/includes/core-changes/windowsforms/3.1/remove-controls-3.1.md)]

***

[!INCLUDE[CellFormatting event](~/includes/core-changes/windowsforms/3.1/cellformatting-event-not-raised.md)]

<span data-ttu-id="29065-137">\*\*_</span><span class="sxs-lookup"><span data-stu-id="29065-137">\*\*_</span></span>

## <a name="net-core-30"></a><span data-ttu-id="29065-138">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="29065-138">.NET Core 3.0</span></span>

[!INCLUDE[Control.DefaultFont changed to Segoe UI 9pt](~/includes/core-changes/windowsforms/3.0/control-defaultfont-changed.md)]

_*_

[!INCLUDE[Modernization of the FolderBrowserDialog](~/includes/core-changes/windowsforms/3.0/modernized-folderbrowserdialog.md)]

_*_

[!INCLUDE[SerializableAttribute removed from some Windows Forms types](~/includes/core-changes/windowsforms/3.0/remove-serializationattribute.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.AllowUpdateChildControlIndexForTabControls compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-allowupdatechildcontrolindexfortabcontrols.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.DomainUpDown.UseLegacyScrolling compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-uselegacyscrolling.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.DoNotLoadLatestRichEditControl compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-donotloadlatestricheditcontrol.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.DoNotSupportSelectAllShortcutInMultilineTextBox compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-donotsupportselectallshortcutinmultilinetextbox.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.DontSupportReentrantFilterMessage compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-dontsupportreentrantfiltermessage.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.EnableVisualStyleValidation compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-enablevisualstylevalidation.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.UseLegacyContextMenuStripSourceControlValue compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-uselegacycontextmenustripsourcecontrolvalue.md)]

_*_

[!INCLUDE[Switch.System.Windows.Forms.UseLegacyImages compatibility switch not supported](~/includes/core-changes/windowsforms/3.0/deprecate-uselegacyimages.md)]

<span data-ttu-id="29065-139">_\*\*</span><span class="sxs-lookup"><span data-stu-id="29065-139">_\*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="29065-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="29065-140">See also</span></span>

- [<span data-ttu-id="29065-141">将 Windows 窗体应用移植到 .NET Core</span><span class="sxs-lookup"><span data-stu-id="29065-141">Port a Windows Forms app to .NET Core</span></span>](/dotnet/desktop/winforms/migration/?view=netdesktop-5.0&preserve-view=true)
