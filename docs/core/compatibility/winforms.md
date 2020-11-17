---
title: Windows 窗体重大更改
description: 列出适用于 .NET Core 和 .NET 5 的 Windows 窗体中的中断性变更。
ms.date: 09/08/2020
ms.openlocfilehash: c79fd28b5c3b81ae7ddf1ef3f470601108b87705
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94440785"
---
# <a name="breaking-changes-in-windows-forms"></a><span data-ttu-id="8a8af-103">Windows 窗体中的中断性变更</span><span class="sxs-lookup"><span data-stu-id="8a8af-103">Breaking changes in Windows Forms</span></span>

<span data-ttu-id="8a8af-104">已在 .NET Core 的版本 3.0 中添加 Windows 窗体支持。</span><span class="sxs-lookup"><span data-stu-id="8a8af-104">Windows Forms support was added to .NET Core in version 3.0.</span></span> <span data-ttu-id="8a8af-105">本文按引入了中断性变更的 .NET 版本列出了 Windows 窗体的中断性变更。</span><span class="sxs-lookup"><span data-stu-id="8a8af-105">This article lists breaking changes for Windows Forms by the .NET version in which they were introduced.</span></span> <span data-ttu-id="8a8af-106">如果要从 .NET Framework 或 .NET Core 的早期版本（3.0 或更高版本）升级 Windows 窗体应用，本文能为你提供帮助。</span><span class="sxs-lookup"><span data-stu-id="8a8af-106">If you're upgrading a Windows Forms app from .NET Framework or from a previous version of .NET Core (3.0 or later), this article applies to you.</span></span>

<span data-ttu-id="8a8af-107">本页记录了以下中断性变更：</span><span class="sxs-lookup"><span data-stu-id="8a8af-107">The following breaking changes are documented on this page:</span></span>

| <span data-ttu-id="8a8af-108">重大更改</span><span class="sxs-lookup"><span data-stu-id="8a8af-108">Breaking change</span></span> | <span data-ttu-id="8a8af-109">引入的版本</span><span class="sxs-lookup"><span data-stu-id="8a8af-109">Version introduced</span></span> |
| - | :-: |
| [<span data-ttu-id="8a8af-110">TextFormatFlags.ModifyString 已过时</span><span class="sxs-lookup"><span data-stu-id="8a8af-110">TextFormatFlags.ModifyString is obsolete</span></span>](#textformatflagsmodifystring-is-obsolete) | <span data-ttu-id="8a8af-111">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-111">5.0</span></span> |
| [<span data-ttu-id="8a8af-112">DataGridView 不再重置自定义单元格样式的字体</span><span class="sxs-lookup"><span data-stu-id="8a8af-112">DataGridView no longer resets fonts for customized cell styles</span></span>](#datagridview-no-longer-resets-fonts-for-customized-cell-styles) | <span data-ttu-id="8a8af-113">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-113">5.0</span></span> |
| [<span data-ttu-id="8a8af-114">对于 WPF 和 WinForms 应用，OutputType 设置为 WinExe</span><span class="sxs-lookup"><span data-stu-id="8a8af-114">OutputType set to WinExe for WPF and WinForms apps</span></span>](#outputtype-set-to-winexe-for-wpf-and-winforms-apps) | <span data-ttu-id="8a8af-115">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-115">5.0</span></span> |
| [<span data-ttu-id="8a8af-116">与 DataGridView 相关的 API 现在引发 InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="8a8af-116">DataGridView-related APIs now throw InvalidOperationException</span></span>](#datagridview-related-apis-now-throw-invalidoperationexception) | <span data-ttu-id="8a8af-117">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-117">5.0</span></span> |
| [<span data-ttu-id="8a8af-118">WinForms 和 WPF 应用使用 Microsoft.NET.Sdk</span><span class="sxs-lookup"><span data-stu-id="8a8af-118">WinForms and WPF apps use Microsoft.NET.Sdk</span></span>](#winforms-and-wpf-apps-use-microsoftnetsdk) | <span data-ttu-id="8a8af-119">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-119">5.0</span></span> |
| [<span data-ttu-id="8a8af-120">已删除的状态栏控件</span><span class="sxs-lookup"><span data-stu-id="8a8af-120">Removed status bar controls</span></span>](#removed-status-bar-controls) | <span data-ttu-id="8a8af-121">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-121">5.0</span></span> |
| [<span data-ttu-id="8a8af-122">WinForms 方法现在会引发 ArgumentException</span><span class="sxs-lookup"><span data-stu-id="8a8af-122">WinForms methods now throw ArgumentException</span></span>](#winforms-methods-now-throw-argumentexception) | <span data-ttu-id="8a8af-123">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-123">5.0</span></span> |
| [<span data-ttu-id="8a8af-124">WinForms 方法现在会引发 ArgumentNullException</span><span class="sxs-lookup"><span data-stu-id="8a8af-124">WinForms methods now throw ArgumentNullException</span></span>](#winforms-methods-now-throw-argumentnullexception) | <span data-ttu-id="8a8af-125">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-125">5.0</span></span> |
| [<span data-ttu-id="8a8af-126">WinForms 属性现在引发 ArgumentOutOfRangeException</span><span class="sxs-lookup"><span data-stu-id="8a8af-126">WinForms properties now throw ArgumentOutOfRangeException</span></span>](#winforms-properties-now-throw-argumentoutofrangeexception) | <span data-ttu-id="8a8af-127">5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-127">5.0</span></span> |
| [<span data-ttu-id="8a8af-128">已删除的控件</span><span class="sxs-lookup"><span data-stu-id="8a8af-128">Removed controls</span></span>](#removed-controls) | <span data-ttu-id="8a8af-129">3.1</span><span class="sxs-lookup"><span data-stu-id="8a8af-129">3.1</span></span> |
| [<span data-ttu-id="8a8af-130">如果显示工具提示，则不引发 CellFormatting 事件</span><span class="sxs-lookup"><span data-stu-id="8a8af-130">CellFormatting event not raised if tooltip is shown</span></span>](#cellformatting-event-not-raised-if-tooltip-is-shown) | <span data-ttu-id="8a8af-131">3.1</span><span class="sxs-lookup"><span data-stu-id="8a8af-131">3.1</span></span> |
| [<span data-ttu-id="8a8af-132">Control.DefaultFont 已更改为 Segoe UI 9 pt</span><span class="sxs-lookup"><span data-stu-id="8a8af-132">Control.DefaultFont changed to Segoe UI 9 pt</span></span>](#default-control-font-changed-to-segoe-ui-9-pt) | <span data-ttu-id="8a8af-133">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-133">3.0</span></span> |
| [<span data-ttu-id="8a8af-134">FolderBrowserDialog 的现代化</span><span class="sxs-lookup"><span data-stu-id="8a8af-134">Modernization of the FolderBrowserDialog</span></span>](#modernization-of-the-folderbrowserdialog) | <span data-ttu-id="8a8af-135">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-135">3.0</span></span> |
| [<span data-ttu-id="8a8af-136">已从一些 Windows 窗体类型中删除 SerializableAttribute</span><span class="sxs-lookup"><span data-stu-id="8a8af-136">SerializableAttribute removed from some Windows Forms types</span></span>](#serializableattribute-removed-from-some-windows-forms-types) | <span data-ttu-id="8a8af-137">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-137">3.0</span></span> |
| [<span data-ttu-id="8a8af-138">不支持 AllowUpdateChildControlIndexForTabControls 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-138">AllowUpdateChildControlIndexForTabControls compatibility switch not supported</span></span>](#allowupdatechildcontrolindexfortabcontrols-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-139">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-139">3.0</span></span> |
| [<span data-ttu-id="8a8af-140">不支持 DomainUpDown.UseLegacyScrolling 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-140">DomainUpDown.UseLegacyScrolling compatibility switch not supported</span></span>](#domainupdownuselegacyscrolling-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-141">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-141">3.0</span></span> |
| [<span data-ttu-id="8a8af-142">不支持 DoNotLoadLatestRichEditControl 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-142">DoNotLoadLatestRichEditControl compatibility switch not supported</span></span>](#donotloadlatestricheditcontrol-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-143">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-143">3.0</span></span> |
| [<span data-ttu-id="8a8af-144">不支持 DoNotSupportSelectAllShortcutInMultilineTextBox 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-144">DoNotSupportSelectAllShortcutInMultilineTextBox compatibility switch not supported</span></span>](#donotsupportselectallshortcutinmultilinetextbox-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-145">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-145">3.0</span></span> |
| [<span data-ttu-id="8a8af-146">不支持 DontSupportReentrantFilterMessage 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-146">DontSupportReentrantFilterMessage compatibility switch not supported</span></span>](#dontsupportreentrantfiltermessage-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-147">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-147">3.0</span></span> |
| [<span data-ttu-id="8a8af-148">不支持 EnableVisualStyleValidation 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-148">EnableVisualStyleValidation compatibility switch not supported</span></span>](#enablevisualstylevalidation-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-149">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-149">3.0</span></span> |
| [<span data-ttu-id="8a8af-150">不支持 UseLegacyContextMenuStripSourceControlValue 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-150">UseLegacyContextMenuStripSourceControlValue compatibility switch not supported</span></span>](#uselegacycontextmenustripsourcecontrolvalue-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-151">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-151">3.0</span></span> |
| [<span data-ttu-id="8a8af-152">不支持 UseLegacyImages 兼容性开关</span><span class="sxs-lookup"><span data-stu-id="8a8af-152">UseLegacyImages compatibility switch not supported</span></span>](#uselegacyimages-compatibility-switch-not-supported) | <span data-ttu-id="8a8af-153">3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-153">3.0</span></span> |

## <a name="net-50"></a><span data-ttu-id="8a8af-154">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-154">.NET 5.0</span></span>

[!INCLUDE [modifystring-field-of-textformatflags-obsolete](../../../includes/core-changes/windowsforms/5.0/modifystring-field-of-textformatflags-obsolete.md)]

***

[!INCLUDE [datagridview-doesnt-reset-custom-font-settings](../../../includes/core-changes/windowsforms/5.0/datagridview-doesnt-reset-custom-font-settings.md)]

<span data-ttu-id="8a8af-155">\*\*_</span><span class="sxs-lookup"><span data-stu-id="8a8af-155">\*\*_</span></span>

[!INCLUDE [automatically-infer-winexe-output-type](../../../includes/core-changes/windowsforms/5.0/automatically-infer-winexe-output-type.md)]

_*_

[!INCLUDE [null-owner-causes-invalidoperationexception](../../../includes/core-changes/windowsforms/5.0/null-owner-causes-invalidoperationexception.md)]

_*_

[!INCLUDE [sdk-and-target-framework-change](../../../includes/core-changes/windowsforms/5.0/sdk-and-target-framework-change.md)]

_*_

[!INCLUDE [winforms-deprecated-controls](../../../includes/core-changes/windowsforms/5.0/winforms-deprecated-controls.md)]

_*_

[!INCLUDE [invalid-args-cause-argumentexception](../../../includes/core-changes/windowsforms/5.0/invalid-args-cause-argumentexception.md)]

_*_

[!INCLUDE [null-args-cause-argumentnullexception](../../../includes/core-changes/windowsforms/5.0/null-args-cause-argumentnullexception.md)]

_*_

[!INCLUDE [invalid-args-cause-argumentoutofrangeexception](../../../includes/core-changes/windowsforms/5.0/invalid-args-cause-argumentoutofrangeexception.md)]

_*_

## <a name="net-core-31"></a><span data-ttu-id="8a8af-156">.NET Core 3.1</span><span class="sxs-lookup"><span data-stu-id="8a8af-156">.NET Core 3.1</span></span>

[!INCLUDE[Removed controls](~/includes/core-changes/windowsforms/3.1/remove-controls-3.1.md)]

_*_

[!INCLUDE[CellFormatting event](~/includes/core-changes/windowsforms/3.1/cellformatting-event-not-raised.md)]

_*_

## <a name="net-core-30"></a><span data-ttu-id="8a8af-157">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="8a8af-157">.NET Core 3.0</span></span>

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

<span data-ttu-id="8a8af-158">_\*\*</span><span class="sxs-lookup"><span data-stu-id="8a8af-158">_\*\*</span></span>

## <a name="see-also"></a><span data-ttu-id="8a8af-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="8a8af-159">See also</span></span>

- [<span data-ttu-id="8a8af-160">将 Windows 窗体应用移植到 .NET Core</span><span class="sxs-lookup"><span data-stu-id="8a8af-160">Port a Windows Forms app to .NET Core</span></span>](/dotnet/desktop/winforms/migration/?view=netdesktop-5.0&preserve-view=true)
