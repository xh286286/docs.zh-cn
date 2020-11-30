---
title: 全球化配置设置
description: 了解对 .NET Core 应用的全球化方面进行配置的运行时设置。例如，如何分析日语日期。
ms.date: 05/18/2020
ms.topic: reference
ms.openlocfilehash: fc98e965093c28b75b9b66e4f1c9f147abd4680e
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95721903"
---
# <a name="run-time-configuration-options-for-globalization"></a><span data-ttu-id="50644-103">用于全球化的运行时配置选项</span><span class="sxs-lookup"><span data-stu-id="50644-103">Run-time configuration options for globalization</span></span>

## <a name="invariant-mode"></a><span data-ttu-id="50644-104">固定模式</span><span class="sxs-lookup"><span data-stu-id="50644-104">Invariant mode</span></span>

- <span data-ttu-id="50644-105">确定 .NET Core 应用是否以全球化固定模式运行而无权访问特定区域性的数据和行为。</span><span class="sxs-lookup"><span data-stu-id="50644-105">Determines whether a .NET Core app runs in globalization-invariant mode without access to culture-specific data and behavior.</span></span>
- <span data-ttu-id="50644-106">如果省略此设置，应用可运行并可访问区域性数据。</span><span class="sxs-lookup"><span data-stu-id="50644-106">If you omit this setting, the app runs with access to cultural data.</span></span> <span data-ttu-id="50644-107">它等效于将值设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="50644-107">This is equivalent to setting the value to `false`.</span></span>
- <span data-ttu-id="50644-108">有关详细信息，请参阅 [.NET Core 全球化固定模式](https://github.com/dotnet/runtime/blob/master/docs/design/features/globalization-invariant-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="50644-108">For more information, see [.NET Core globalization invariant mode](https://github.com/dotnet/runtime/blob/master/docs/design/features/globalization-invariant-mode.md).</span></span>

| | <span data-ttu-id="50644-109">设置名</span><span class="sxs-lookup"><span data-stu-id="50644-109">Setting name</span></span> | <span data-ttu-id="50644-110">值</span><span class="sxs-lookup"><span data-stu-id="50644-110">Values</span></span> |
| - | - | - |
| <span data-ttu-id="50644-111">**runtimeconfig.json**</span><span class="sxs-lookup"><span data-stu-id="50644-111">**runtimeconfig.json**</span></span> | `System.Globalization.Invariant` | <span data-ttu-id="50644-112">`false` - 可访问区域性数据</span><span class="sxs-lookup"><span data-stu-id="50644-112">`false` - access to cultural data</span></span><br/><span data-ttu-id="50644-113">`true` - 以固定模式运行</span><span class="sxs-lookup"><span data-stu-id="50644-113">`true` - run in invariant mode</span></span> |
| <span data-ttu-id="50644-114">MSBuild 属性</span><span class="sxs-lookup"><span data-stu-id="50644-114">**MSBuild property**</span></span> | `InvariantGlobalization` | <span data-ttu-id="50644-115">`false` - 可访问区域性数据</span><span class="sxs-lookup"><span data-stu-id="50644-115">`false` - access to cultural data</span></span><br/><span data-ttu-id="50644-116">`true` - 以固定模式运行</span><span class="sxs-lookup"><span data-stu-id="50644-116">`true` - run in invariant mode</span></span> |
| <span data-ttu-id="50644-117">**环境变量**</span><span class="sxs-lookup"><span data-stu-id="50644-117">**Environment variable**</span></span> | `DOTNET_SYSTEM_GLOBALIZATION_INVARIANT` | <span data-ttu-id="50644-118">`0` - 可访问区域性数据</span><span class="sxs-lookup"><span data-stu-id="50644-118">`0` - access to cultural data</span></span><br/><span data-ttu-id="50644-119">`1` - 以固定模式运行</span><span class="sxs-lookup"><span data-stu-id="50644-119">`1` - run in invariant mode</span></span> |

### <a name="examples"></a><span data-ttu-id="50644-120">示例</span><span class="sxs-lookup"><span data-stu-id="50644-120">Examples</span></span>

<span data-ttu-id="50644-121">runtimeconfig.json 文件：</span><span class="sxs-lookup"><span data-stu-id="50644-121">*runtimeconfig.json* file:</span></span>

```json
{
   "runtimeOptions": {
      "configProperties": {
         "System.Globalization.Invariant": true
      }
   }
}
```

<span data-ttu-id="50644-122">项目文件：</span><span class="sxs-lookup"><span data-stu-id="50644-122">Project file:</span></span>

```xml
<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>
    <InvariantGlobalization>true</InvariantGlobalization>
  </PropertyGroup>

</Project>
```

## <a name="era-year-ranges"></a><span data-ttu-id="50644-123">纪元年份范围</span><span class="sxs-lookup"><span data-stu-id="50644-123">Era year ranges</span></span>

- <span data-ttu-id="50644-124">确定是否放宽对支持多个纪元的日历的范围检查，或者超出纪元日期范围的日期是否引发 <xref:System.ArgumentOutOfRangeException>。</span><span class="sxs-lookup"><span data-stu-id="50644-124">Determines whether range checks for calendars that support multiple eras are relaxed or whether dates that overflow an era's date range throw an <xref:System.ArgumentOutOfRangeException>.</span></span>
- <span data-ttu-id="50644-125">如果省略此设置，则会放宽范围检查。</span><span class="sxs-lookup"><span data-stu-id="50644-125">If you omit this setting, range checks are relaxed.</span></span> <span data-ttu-id="50644-126">它等效于将值设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="50644-126">This is equivalent to setting the value to `false`.</span></span>
- <span data-ttu-id="50644-127">有关详细信息，请参阅[日历、纪元和日期范围：放宽的范围检查](../../standard/datetime/working-with-calendars.md#calendars-eras-and-date-ranges-relaxed-range-checks)。</span><span class="sxs-lookup"><span data-stu-id="50644-127">For more information, see [Calendars, eras, and date ranges: Relaxed range checks](../../standard/datetime/working-with-calendars.md#calendars-eras-and-date-ranges-relaxed-range-checks).</span></span>

| | <span data-ttu-id="50644-128">设置名</span><span class="sxs-lookup"><span data-stu-id="50644-128">Setting name</span></span> | <span data-ttu-id="50644-129">值</span><span class="sxs-lookup"><span data-stu-id="50644-129">Values</span></span> |
| - | - | - |
| <span data-ttu-id="50644-130">**runtimeconfig.json**</span><span class="sxs-lookup"><span data-stu-id="50644-130">**runtimeconfig.json**</span></span> | `Switch.System.Globalization.EnforceJapaneseEraYearRanges` | <span data-ttu-id="50644-131">`false` - 放宽的范围检查</span><span class="sxs-lookup"><span data-stu-id="50644-131">`false` - relaxed range checks</span></span><br/><span data-ttu-id="50644-132">`true` - 超出范围导致异常</span><span class="sxs-lookup"><span data-stu-id="50644-132">`true` - overflows cause an exception</span></span> |
| <span data-ttu-id="50644-133">**环境变量**</span><span class="sxs-lookup"><span data-stu-id="50644-133">**Environment variable**</span></span> | <span data-ttu-id="50644-134">不可用</span><span class="sxs-lookup"><span data-stu-id="50644-134">N/A</span></span> | <span data-ttu-id="50644-135">不可用</span><span class="sxs-lookup"><span data-stu-id="50644-135">N/A</span></span> |

## <a name="japanese-date-parsing"></a><span data-ttu-id="50644-136">日语日期分析</span><span class="sxs-lookup"><span data-stu-id="50644-136">Japanese date parsing</span></span>

- <span data-ttu-id="50644-137">确定是否成功分析包含“1”或“Gannen”作为年份的字符串，或是否仅支持“1”。</span><span class="sxs-lookup"><span data-stu-id="50644-137">Determines whether a string that contains either "1" or "Gannen" as the year parses successfully or whether only "1" is supported.</span></span>
- <span data-ttu-id="50644-138">如果省略此设置，则成功分析包含“1”或“Gannen”作为年份的字符串。</span><span class="sxs-lookup"><span data-stu-id="50644-138">If you omit this setting, strings that contain either "1" or "Gannen" as the year parse successfully.</span></span> <span data-ttu-id="50644-139">它等效于将值设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="50644-139">This is equivalent to setting the value to `false`.</span></span>
- <span data-ttu-id="50644-140">有关详细信息，请参阅[用多个纪元表示日历中的日期](../../standard/datetime/working-with-calendars.md#represent-dates-in-calendars-with-multiple-eras)。</span><span class="sxs-lookup"><span data-stu-id="50644-140">For more information, see [Represent dates in calendars with multiple eras](../../standard/datetime/working-with-calendars.md#represent-dates-in-calendars-with-multiple-eras).</span></span>

| | <span data-ttu-id="50644-141">设置名</span><span class="sxs-lookup"><span data-stu-id="50644-141">Setting name</span></span> | <span data-ttu-id="50644-142">值</span><span class="sxs-lookup"><span data-stu-id="50644-142">Values</span></span> |
| - | - | - |
| <span data-ttu-id="50644-143">**runtimeconfig.json**</span><span class="sxs-lookup"><span data-stu-id="50644-143">**runtimeconfig.json**</span></span> | `Switch.System.Globalization.EnforceLegacyJapaneseDateParsing` | <span data-ttu-id="50644-144">`false` - 支持“Gannen”或“1”</span><span class="sxs-lookup"><span data-stu-id="50644-144">`false` - "Gannen" or "1" is supported</span></span><br/><span data-ttu-id="50644-145">`true` - 仅支持“1”</span><span class="sxs-lookup"><span data-stu-id="50644-145">`true` - only "1" is supported</span></span> |
| <span data-ttu-id="50644-146">**环境变量**</span><span class="sxs-lookup"><span data-stu-id="50644-146">**Environment variable**</span></span> | <span data-ttu-id="50644-147">不可用</span><span class="sxs-lookup"><span data-stu-id="50644-147">N/A</span></span> | <span data-ttu-id="50644-148">不可用</span><span class="sxs-lookup"><span data-stu-id="50644-148">N/A</span></span> |

## <a name="japanese-year-format"></a><span data-ttu-id="50644-149">日语年份格式</span><span class="sxs-lookup"><span data-stu-id="50644-149">Japanese year format</span></span>

- <span data-ttu-id="50644-150">确定是将日本历时代的第一年的格式设置为“Gannen”还是设置为一个数字。</span><span class="sxs-lookup"><span data-stu-id="50644-150">Determines whether the first year of a Japanese calendar era is formatted as "Gannen" or as a number.</span></span>
- <span data-ttu-id="50644-151">如果省略此设置，则第一年的格式设置为“Gannen”。</span><span class="sxs-lookup"><span data-stu-id="50644-151">If you omit this setting, the first year is formatted as "Gannen".</span></span> <span data-ttu-id="50644-152">它等效于将值设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="50644-152">This is equivalent to setting the value to `false`.</span></span>
- <span data-ttu-id="50644-153">有关详细信息，请参阅[用多个纪元表示日历中的日期](../../standard/datetime/working-with-calendars.md#represent-dates-in-calendars-with-multiple-eras)。</span><span class="sxs-lookup"><span data-stu-id="50644-153">For more information, see [Represent dates in calendars with multiple eras](../../standard/datetime/working-with-calendars.md#represent-dates-in-calendars-with-multiple-eras).</span></span>

| | <span data-ttu-id="50644-154">设置名</span><span class="sxs-lookup"><span data-stu-id="50644-154">Setting name</span></span> | <span data-ttu-id="50644-155">值</span><span class="sxs-lookup"><span data-stu-id="50644-155">Values</span></span> |
| - | - | - |
| <span data-ttu-id="50644-156">**runtimeconfig.json**</span><span class="sxs-lookup"><span data-stu-id="50644-156">**runtimeconfig.json**</span></span> | `Switch.System.Globalization.FormatJapaneseFirstYearAsANumber` | <span data-ttu-id="50644-157">`false` - 将格式设置为“Gannen”</span><span class="sxs-lookup"><span data-stu-id="50644-157">`false` - format as "Gannen"</span></span><br/><span data-ttu-id="50644-158">`true` - 将格式设置为数字</span><span class="sxs-lookup"><span data-stu-id="50644-158">`true` - format as number</span></span> |
| <span data-ttu-id="50644-159">**环境变量**</span><span class="sxs-lookup"><span data-stu-id="50644-159">**Environment variable**</span></span> | <span data-ttu-id="50644-160">不可用</span><span class="sxs-lookup"><span data-stu-id="50644-160">N/A</span></span> | <span data-ttu-id="50644-161">不可用</span><span class="sxs-lookup"><span data-stu-id="50644-161">N/A</span></span> |

## <a name="nls"></a><span data-ttu-id="50644-162">NLS</span><span class="sxs-lookup"><span data-stu-id="50644-162">NLS</span></span>

- <span data-ttu-id="50644-163">确定 .NET 是否使用适用于 Windows 应用的 Unicode (ICU) 全球化 API 的区域语言支持 (NLS) 或国际组件。</span><span class="sxs-lookup"><span data-stu-id="50644-163">Determines whether .NET uses National Language Support (NLS) or International Components for Unicode (ICU) globalization APIs for Windows apps.</span></span> <span data-ttu-id="50644-164">默认情况下，.NET 5.0 和更高版本在 Windows 10 2019 年 5 月更新和更高版本上使用 ICU 全球化 API。</span><span class="sxs-lookup"><span data-stu-id="50644-164">.NET 5.0 and later versions use ICU globalization APIs by default on Windows 10 May 2019 Update and later versions.</span></span>
- <span data-ttu-id="50644-165">如果省略此设置，则默认情况下，.NET 使用 ICU 全球化 API。</span><span class="sxs-lookup"><span data-stu-id="50644-165">If you omit this setting, .NET uses ICU globalization APIs by default.</span></span> <span data-ttu-id="50644-166">它等效于将值设置为 `false`。</span><span class="sxs-lookup"><span data-stu-id="50644-166">This is equivalent to setting the value to `false`.</span></span>
- <span data-ttu-id="50644-167">有关详细信息，请参阅[全球化 API 在 Windows 上使用 ICU 库](../compatibility/globalization/5.0/icu-globalization-api.md)。</span><span class="sxs-lookup"><span data-stu-id="50644-167">For more information, see [Globalization APIs use ICU libraries on Windows](../compatibility/globalization/5.0/icu-globalization-api.md).</span></span>

| | <span data-ttu-id="50644-168">设置名</span><span class="sxs-lookup"><span data-stu-id="50644-168">Setting name</span></span> | <span data-ttu-id="50644-169">值</span><span class="sxs-lookup"><span data-stu-id="50644-169">Values</span></span> | <span data-ttu-id="50644-170">已引入</span><span class="sxs-lookup"><span data-stu-id="50644-170">Introduced</span></span> |
| - | - | - | - |
| <span data-ttu-id="50644-171">**runtimeconfig.json**</span><span class="sxs-lookup"><span data-stu-id="50644-171">**runtimeconfig.json**</span></span> | `System.Globalization.UseNls` | <span data-ttu-id="50644-172">`false` - 使用 ICU 全球化 API</span><span class="sxs-lookup"><span data-stu-id="50644-172">`false` - Use ICU globalization APIs</span></span><br/><span data-ttu-id="50644-173">`true` - 使用 NLS 全球化 API</span><span class="sxs-lookup"><span data-stu-id="50644-173">`true` - Use NLS globalization APIs</span></span> | <span data-ttu-id="50644-174">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="50644-174">.NET 5.0</span></span> |
| <span data-ttu-id="50644-175">**环境变量**</span><span class="sxs-lookup"><span data-stu-id="50644-175">**Environment variable**</span></span> | `DOTNET_SYSTEM_GLOBALIZATION_USENLS` | <span data-ttu-id="50644-176">`false` - 使用 ICU 全球化 API</span><span class="sxs-lookup"><span data-stu-id="50644-176">`false` - Use ICU globalization APIs</span></span><br/><span data-ttu-id="50644-177">`true` - 使用 NLS 全球化 API</span><span class="sxs-lookup"><span data-stu-id="50644-177">`true` - Use NLS globalization APIs</span></span> | <span data-ttu-id="50644-178">.NET 5.0</span><span class="sxs-lookup"><span data-stu-id="50644-178">.NET 5.0</span></span> |
