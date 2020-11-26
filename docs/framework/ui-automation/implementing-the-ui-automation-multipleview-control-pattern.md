---
title: 实现 UI 自动化 MultipleView 控件模式
description: 在 UI 自动化中查看实现 MultipleView 控件模式的准则和约定。 请参阅 IMultipleViewProvider 接口的必需成员。
ms.date: 03/30/2017
helpviewer_keywords:
- UI Automation, MultipleView control pattern
- MultipleView control pattern
- control patterns, MultipleView
ms.assetid: 5bf1b248-ffee-48c8-9613-0b134bbe9f6a
ms.openlocfilehash: 7e64a696e8dc96123631853b06ea3ccee434d2f1
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96239428"
---
# <a name="implementing-the-ui-automation-multipleview-control-pattern"></a><span data-ttu-id="b5164-104">实现 UI 自动化 MultipleView 控件模式</span><span class="sxs-lookup"><span data-stu-id="b5164-104">Implementing the UI Automation MultipleView Control Pattern</span></span>

> [!NOTE]
> <span data-ttu-id="b5164-105">本文档适用于想要使用 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] 命名空间中定义的托管 <xref:System.Windows.Automation> 类的 .NET Framework 开发人员。</span><span class="sxs-lookup"><span data-stu-id="b5164-105">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="b5164-106">有关 [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)]的最新信息，请参阅 [Windows 自动化 API：UI 自动化](/windows/win32/winauto/entry-uiauto-win32)。</span><span class="sxs-lookup"><span data-stu-id="b5164-106">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](/windows/win32/winauto/entry-uiauto-win32).</span></span>  
  
 <span data-ttu-id="b5164-107">本主题介绍了实现 <xref:System.Windows.Automation.Provider.IMultipleViewProvider>的准则和约定，包括有关事件和属性的信息。</span><span class="sxs-lookup"><span data-stu-id="b5164-107">This topic introduces guidelines and conventions for implementing <xref:System.Windows.Automation.Provider.IMultipleViewProvider>, including information about events and properties.</span></span> <span data-ttu-id="b5164-108">本主题的结尾列出了指向其他参考资料的链接。</span><span class="sxs-lookup"><span data-stu-id="b5164-108">Links to additional references are listed at the end of the topic.</span></span>  
  
 <span data-ttu-id="b5164-109"><xref:System.Windows.Automation.MultipleViewPattern> 控件模式用于支持那些提供并能够在同组信息或子控件的多个表示形式间进行切换的控件。</span><span class="sxs-lookup"><span data-stu-id="b5164-109">The <xref:System.Windows.Automation.MultipleViewPattern> control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same set of information or child controls.</span></span>  
  
 <span data-ttu-id="b5164-110">可显示多个视图的控件示例包括列表视图 (可以将其内容显示为缩略图，磁贴、图标或详细信息) ，Microsoft Excel 图表 (饼图、行、栏、单元格值和公式) 、Microsoft Word 文档 (普通、Web 版式、打印布局、阅读版式、大纲) 、Microsoft Outlook 日历 (年、月、周、天) 和 Microsoft Windows Media Player 外观。</span><span class="sxs-lookup"><span data-stu-id="b5164-110">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, Web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="b5164-111">支持的视图由控件开发人员确定，并特定于每个控件。</span><span class="sxs-lookup"><span data-stu-id="b5164-111">The supported views are determined by the control developer and are specific to each control.</span></span>  
  
<a name="Implementation_Guidelines_and_Conventions"></a>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b5164-112">实现准则和约定</span><span class="sxs-lookup"><span data-stu-id="b5164-112">Implementation Guidelines and Conventions</span></span>  

 <span data-ttu-id="b5164-113">在实现 Multiple View 控件模式时，请注意以下准则和约定：</span><span class="sxs-lookup"><span data-stu-id="b5164-113">When implementing the Multiple View control pattern, note the following guidelines and conventions:</span></span>  
  
- <span data-ttu-id="b5164-114"><xref:System.Windows.Automation.Provider.IMultipleViewProvider> 还应在一个容器中实现，此容器用于管理当前视图，如果它不同于提供当前视图的控件。</span><span class="sxs-lookup"><span data-stu-id="b5164-114"><xref:System.Windows.Automation.Provider.IMultipleViewProvider> should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="b5164-115">例如，Windows 资源管理器包含当前文件夹内容的列表控件，而该控件的视图是从 Windows 资源管理器应用程序进行管理的。</span><span class="sxs-lookup"><span data-stu-id="b5164-115">For example, Windows Explorer contains a List control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>  
  
- <span data-ttu-id="b5164-116">能够对其内容进行排序的控件不被视为支持多个视图。</span><span class="sxs-lookup"><span data-stu-id="b5164-116">A control that is able to sort its content is not considered to support multiple views.</span></span>  
  
- <span data-ttu-id="b5164-117">视图的集合必须跨实例相同。</span><span class="sxs-lookup"><span data-stu-id="b5164-117">The collection of views must be identical across instances.</span></span>  
  
- <span data-ttu-id="b5164-118">视图名称必须是适合在文本到语音转换、盲文和其他用户可读的应用程序中使用。</span><span class="sxs-lookup"><span data-stu-id="b5164-118">View names must be suitable for use in Text to Speech, Braille, and other human-readable applications.</span></span>  
  
<a name="Required_Members_for_IMultipleViewProvider"></a>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="b5164-119">IMultipleViewProvider 所需的成员</span><span class="sxs-lookup"><span data-stu-id="b5164-119">Required Members for IMultipleViewProvider</span></span>  

 <span data-ttu-id="b5164-120">实现 IMultipleViewProvider 需要以下属性和方法。</span><span class="sxs-lookup"><span data-stu-id="b5164-120">The following properties and methods are required for implementing IMultipleViewProvider.</span></span>  
  
|<span data-ttu-id="b5164-121">必需的成员</span><span class="sxs-lookup"><span data-stu-id="b5164-121">Required members</span></span>|<span data-ttu-id="b5164-122">成员类型</span><span class="sxs-lookup"><span data-stu-id="b5164-122">Member type</span></span>|<span data-ttu-id="b5164-123">说明</span><span class="sxs-lookup"><span data-stu-id="b5164-123">Notes</span></span>|  
|----------------------|-----------------|-----------|  
|<xref:System.Windows.Automation.Provider.IMultipleViewProvider.CurrentView%2A>|<span data-ttu-id="b5164-124">属性</span><span class="sxs-lookup"><span data-stu-id="b5164-124">Property</span></span>|<span data-ttu-id="b5164-125">无</span><span class="sxs-lookup"><span data-stu-id="b5164-125">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IMultipleViewProvider.GetSupportedViews%2A>|<span data-ttu-id="b5164-126">方法</span><span class="sxs-lookup"><span data-stu-id="b5164-126">Method</span></span>|<span data-ttu-id="b5164-127">无</span><span class="sxs-lookup"><span data-stu-id="b5164-127">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IMultipleViewProvider.GetViewName%2A>|<span data-ttu-id="b5164-128">方法</span><span class="sxs-lookup"><span data-stu-id="b5164-128">Method</span></span>|<span data-ttu-id="b5164-129">无</span><span class="sxs-lookup"><span data-stu-id="b5164-129">None</span></span>|  
|<xref:System.Windows.Automation.Provider.IMultipleViewProvider.SetCurrentView%2A>|<span data-ttu-id="b5164-130">方法</span><span class="sxs-lookup"><span data-stu-id="b5164-130">Method</span></span>|<span data-ttu-id="b5164-131">无</span><span class="sxs-lookup"><span data-stu-id="b5164-131">None</span></span>|  
  
 <span data-ttu-id="b5164-132">没有与此控件模式相关联的事件。</span><span class="sxs-lookup"><span data-stu-id="b5164-132">There are no events associated with this control pattern.</span></span>  
  
<a name="Exceptions"></a>

## <a name="exceptions"></a><span data-ttu-id="b5164-133">异常</span><span class="sxs-lookup"><span data-stu-id="b5164-133">Exceptions</span></span>  

 <span data-ttu-id="b5164-134">提供程序必须引发以下异常。</span><span class="sxs-lookup"><span data-stu-id="b5164-134">Provider must throw the following exceptions.</span></span>  
  
|<span data-ttu-id="b5164-135">例外类型</span><span class="sxs-lookup"><span data-stu-id="b5164-135">Exception type</span></span>|<span data-ttu-id="b5164-136">条件</span><span class="sxs-lookup"><span data-stu-id="b5164-136">Condition</span></span>|  
|--------------------|---------------|  
|<xref:System.ArgumentException>|<span data-ttu-id="b5164-137">当 <xref:System.Windows.Automation.Provider.IMultipleViewProvider.SetCurrentView%2A> 或 <xref:System.Windows.Automation.Provider.IMultipleViewProvider.GetViewName%2A> 与不是受支持视图集合成员的参数一同被调用时。</span><span class="sxs-lookup"><span data-stu-id="b5164-137">When either <xref:System.Windows.Automation.Provider.IMultipleViewProvider.SetCurrentView%2A> or <xref:System.Windows.Automation.Provider.IMultipleViewProvider.GetViewName%2A> is called with a parameter that is not a member of the supported views collection.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="b5164-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b5164-138">See also</span></span>

- [<span data-ttu-id="b5164-139">UI 自动化控件模式概述</span><span class="sxs-lookup"><span data-stu-id="b5164-139">UI Automation Control Patterns Overview</span></span>](ui-automation-control-patterns-overview.md)
- [<span data-ttu-id="b5164-140">在 UI 自动化提供程序中支持控件模式</span><span class="sxs-lookup"><span data-stu-id="b5164-140">Support Control Patterns in a UI Automation Provider</span></span>](support-control-patterns-in-a-ui-automation-provider.md)
- [<span data-ttu-id="b5164-141">客户端的 UI 自动化控件模式</span><span class="sxs-lookup"><span data-stu-id="b5164-141">UI Automation Control Patterns for Clients</span></span>](ui-automation-control-patterns-for-clients.md)
- [<span data-ttu-id="b5164-142">UI 自动化树概述</span><span class="sxs-lookup"><span data-stu-id="b5164-142">UI Automation Tree Overview</span></span>](ui-automation-tree-overview.md)
- [<span data-ttu-id="b5164-143">在 UI 自动化中使用缓存</span><span class="sxs-lookup"><span data-stu-id="b5164-143">Use Caching in UI Automation</span></span>](use-caching-in-ui-automation.md)
