---
title: .NET 正则表达式中的字符类
description: 了解如何使用字符类表示 .NET 正则表达式中的一组字符。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- character classes
- regular expressions, character classes
- characters, matching syntax
- .NET regular expressions, character classes
ms.assetid: 0f8bffab-ee0d-4e0e-9a96-2b4a252bb7e4
ms.openlocfilehash: 35ffe3f338897bc7b24a6c274b5458dd2e19918c
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95728766"
---
# <a name="character-classes-in-regular-expressions"></a><span data-ttu-id="bba04-103">正则表达式中的字符类</span><span class="sxs-lookup"><span data-stu-id="bba04-103">Character classes in regular expressions</span></span>

<span data-ttu-id="bba04-104">一个字符类定义一组字符，其中的任一字符均可出现在输入字符串中以便成功匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-104">A character class defines a set of characters, any one of which can occur in an input string for a match to succeed.</span></span> <span data-ttu-id="bba04-105">.NET 中的正则表达式语言支持以下字符类：</span><span class="sxs-lookup"><span data-stu-id="bba04-105">The regular expression language in .NET supports the following character classes:</span></span>  
  
- <span data-ttu-id="bba04-106">正字符组。</span><span class="sxs-lookup"><span data-stu-id="bba04-106">Positive character groups.</span></span> <span data-ttu-id="bba04-107">输入字符串中的字符必须匹配一组指定的字符中的某个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-107">A character in the input string must match one of a specified set of characters.</span></span> <span data-ttu-id="bba04-108">有关详细信息，请参阅[正字符组](#PositiveGroup)。</span><span class="sxs-lookup"><span data-stu-id="bba04-108">For more information, see [Positive Character Group](#PositiveGroup).</span></span>  
  
- <span data-ttu-id="bba04-109">负字符组。</span><span class="sxs-lookup"><span data-stu-id="bba04-109">Negative character groups.</span></span> <span data-ttu-id="bba04-110">输入字符串中的字符不得匹配一组指定的字符中的某个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-110">A character in the input string must not match one of a specified set of characters.</span></span> <span data-ttu-id="bba04-111">有关详细信息，请参阅[负字符组](#NegativeGroup)。</span><span class="sxs-lookup"><span data-stu-id="bba04-111">For more information, see [Negative Character Group](#NegativeGroup).</span></span>  
  
- <span data-ttu-id="bba04-112">任意字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-112">Any character.</span></span> <span data-ttu-id="bba04-113">正则表达式中的 `.`（圆点或句点）字符是匹配除 `\n` 之外的任何字符的通配符字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-113">The `.` (dot or period) character in a regular expression is a wildcard character that matches any character except `\n`.</span></span> <span data-ttu-id="bba04-114">有关详细信息，请参阅[任意字符](#AnyCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-114">For more information, see [Any Character](#AnyCharacter).</span></span>  
  
- <span data-ttu-id="bba04-115">通用 Unicode 类别或命名块。</span><span class="sxs-lookup"><span data-stu-id="bba04-115">A general Unicode category or named block.</span></span> <span data-ttu-id="bba04-116">输入字符串中的字符必须为特定 Unicode 类别的成员，或必须位于一系列连续的 Unicode 字符中才能成功匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-116">A character in the input string must be a member of a particular Unicode category or must fall within a contiguous range of Unicode characters for a match to succeed.</span></span> <span data-ttu-id="bba04-117">有关详细信息，请参阅 [Unicode 类别或 Unicode 块](#CategoryOrBlock)。</span><span class="sxs-lookup"><span data-stu-id="bba04-117">For more information, see [Unicode Category or Unicode Block](#CategoryOrBlock).</span></span>  
  
- <span data-ttu-id="bba04-118">负通用 Unicode 类别或命名块。</span><span class="sxs-lookup"><span data-stu-id="bba04-118">A negative general Unicode category or named block.</span></span> <span data-ttu-id="bba04-119">输入字符串中的字符不得为特定 Unicode 类别的成员，也不得位于一系列连续的 Unicode 字符中以便成功匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-119">A character in the input string must not be a member of a particular Unicode category or must not fall within a contiguous range of Unicode characters for a match to succeed.</span></span> <span data-ttu-id="bba04-120">有关详细信息，请参阅[负 Unicode 类别或 Unicode 块](#NegativeCategoryOrBlock)。</span><span class="sxs-lookup"><span data-stu-id="bba04-120">For more information, see [Negative Unicode Category or Unicode Block](#NegativeCategoryOrBlock).</span></span>  
  
- <span data-ttu-id="bba04-121">单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-121">A word character.</span></span> <span data-ttu-id="bba04-122">输入字符串中的字符可以属于适合单词中字符的任何 Unicode 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-122">A character in the input string can belong to any of the Unicode categories that are appropriate for characters in words.</span></span> <span data-ttu-id="bba04-123">有关详细信息，请参阅[单词字符](#WordCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-123">For more information, see [Word Character](#WordCharacter).</span></span>  
  
- <span data-ttu-id="bba04-124">非单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-124">A non-word character.</span></span> <span data-ttu-id="bba04-125">输入字符串中的字符可以属于作为非单词字符的任何 Unicode 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-125">A character in the input string can belong to any Unicode category that is not a word character.</span></span> <span data-ttu-id="bba04-126">有关详细信息，请参阅[非单词字符](#NonWordCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-126">For more information, see [Non-Word Character](#NonWordCharacter).</span></span>  
  
- <span data-ttu-id="bba04-127">空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-127">A white-space character.</span></span> <span data-ttu-id="bba04-128">输入字符串中的字符可以是任何 Unicode 分隔符字符以及众多控制字符中的任一字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-128">A character in the input string can be any Unicode separator character, as well as any one of a number of control characters.</span></span> <span data-ttu-id="bba04-129">有关详细信息，请参阅[空白字符](#WhitespaceCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-129">For more information, see [White-Space Character](#WhitespaceCharacter).</span></span>  
  
- <span data-ttu-id="bba04-130">非空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-130">A non-white-space character.</span></span> <span data-ttu-id="bba04-131">输入字符串中的字符可以是作为非空白字符的任何字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-131">A character in the input string can be any character that is not a white-space character.</span></span> <span data-ttu-id="bba04-132">有关详细信息，请参阅[非空白字符](#NonWhitespaceCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-132">For more information, see [Non-White-Space Character](#NonWhitespaceCharacter).</span></span>  
  
- <span data-ttu-id="bba04-133">十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-133">A decimal digit.</span></span> <span data-ttu-id="bba04-134">输入字符串中的字符可以是归类为 Unicode 十进制数字的众多字符中的任一字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-134">A character in the input string can be any of a number of characters classified as Unicode decimal digits.</span></span> <span data-ttu-id="bba04-135">有关详细信息，请参阅[十进制数字字符](#DigitCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-135">For more information, see [Decimal Digit Character](#DigitCharacter).</span></span>  
  
- <span data-ttu-id="bba04-136">非十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-136">A non-decimal digit.</span></span> <span data-ttu-id="bba04-137">输入字符串中的字符可以是任何非 Unicode 十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-137">A character in the input string can be anything other than a Unicode decimal digit.</span></span> <span data-ttu-id="bba04-138">有关详细信息，请参阅[十进制数字字符](#NonDigitCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-138">For more information, see [Decimal Digit Character](#NonDigitCharacter).</span></span>  
  
 <span data-ttu-id="bba04-139">.NET 支持字符类减法表达式，通过该表达式可以定义一组字符作为从一个字符类中排除另一字符类的结果。</span><span class="sxs-lookup"><span data-stu-id="bba04-139">.NET supports character class subtraction expressions, which enables you to define a set of characters as the result of excluding one character class from another character class.</span></span> <span data-ttu-id="bba04-140">有关详细信息，请参阅[字符类减法](#CharacterClassSubtraction)。</span><span class="sxs-lookup"><span data-stu-id="bba04-140">For more information, see [Character Class Subtraction](#CharacterClassSubtraction).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="bba04-141">按类别匹配字符的字符类（如用于匹配字词字符的 [\w](#WordCharacter)，或用于匹配 Unicode 类别的 [\p{}](#CategoryOrBlock)）依赖 <xref:System.Globalization.CharUnicodeInfo> 类提供字符类别信息。</span><span class="sxs-lookup"><span data-stu-id="bba04-141">Character classes that match characters by category, such as [\w](#WordCharacter) to match word characters or [\p{}](#CategoryOrBlock) to match a Unicode category, rely on the <xref:System.Globalization.CharUnicodeInfo> class to provide information about character categories.</span></span> <span data-ttu-id="bba04-142">在 .NET Framework 4.6.2 及更高版本中，字符类别基于 [Unicode 标准 8.0.0 版](https://www.unicode.org/versions/Unicode8.0.0/)。</span><span class="sxs-lookup"><span data-stu-id="bba04-142">In .NET Framework 4.6.2 and later versions, character categories are based on [The Unicode Standard, Version 8.0.0](https://www.unicode.org/versions/Unicode8.0.0/).</span></span>
  
<a name="PositiveGroup"></a>

## <a name="positive-character-group--"></a><span data-ttu-id="bba04-143">正字符组：[ ]</span><span class="sxs-lookup"><span data-stu-id="bba04-143">Positive character group: [ ]</span></span>  

 <span data-ttu-id="bba04-144">正字符组指定一个字符列表，其中的任何一个字符可出现在输入字符串中以便进行匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-144">A positive character group specifies a list of characters, any one of which may appear in an input string for a match to occur.</span></span> <span data-ttu-id="bba04-145">此字符列表可以单独指定和/或作为范围指定。</span><span class="sxs-lookup"><span data-stu-id="bba04-145">This list of characters may be specified individually, as a range, or both.</span></span>  
  
 <span data-ttu-id="bba04-146">用于指定各个字符列表的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="bba04-146">The syntax for specifying a list of individual characters is as follows:</span></span>  

`[*character_group*]`

 <span data-ttu-id="bba04-147">其中，*character_group* 是单个字符的列表，这些字符可出现在输入字符串中以便成功匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-147">where *character_group* is a list of the individual characters that can appear in the input string for a match to succeed.</span></span> <span data-ttu-id="bba04-148">character_group 可以包含一个或多个文本字符、[转义字符](character-escapes-in-regular-expressions.md)或字符类的任意组合。</span><span class="sxs-lookup"><span data-stu-id="bba04-148">*character_group* can consist of any combination of one or more literal characters, [escape characters](character-escapes-in-regular-expressions.md), or character classes.</span></span>  
  
 <span data-ttu-id="bba04-149">用于指定字符范围的语法如下：</span><span class="sxs-lookup"><span data-stu-id="bba04-149">The syntax for specifying a range of characters is as follows:</span></span>  
  
`[firstCharacter-lastCharacter]`  
  
 <span data-ttu-id="bba04-150">其中，*firstCharacter* 是范围的开始字符，*lastCharacter* 是范围的结束字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-150">where *firstCharacter* is the character that begins the range and *lastCharacter* is the character that ends the range.</span></span> <span data-ttu-id="bba04-151">字符范围是通过以下方式定义的一系列连续字符：指定系列中的第一个字符，连字符 (-)，然后指定系列中的最后一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-151">A character range is a contiguous series of characters defined by specifying the first character in the series, a hyphen (-), and then the last character in the series.</span></span> <span data-ttu-id="bba04-152">如果两个字符具有相邻的 Unicode 码位，则这两个字符是连续的。</span><span class="sxs-lookup"><span data-stu-id="bba04-152">Two characters are contiguous if they have adjacent Unicode code points.</span></span> <span data-ttu-id="bba04-153">firstCharacter 必须是码位较低的字符，而 lastCharacter 必须是码位较高的字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-153">*firstCharacter* must be the character with the lower code point, and *lastCharacter* must be the character with the higher code point.</span></span>

> [!NOTE]
> <span data-ttu-id="bba04-154">由于正字符组可以包含一组字符和一个字符范围，因此连字符 (`-`) 始终被解释为范围分隔符，除非它是该组的第一个或最后一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-154">Because a positive character group can include both a set of characters and a character range, a hyphen character (`-`) is always interpreted as the range separator unless it is the first or last character of the group.</span></span>

<span data-ttu-id="bba04-155">下表列出了一些常见的包含正字符类的正则表达式模式。</span><span class="sxs-lookup"><span data-stu-id="bba04-155">Some common regular expression patterns that contain positive character classes are listed in the following table.</span></span>  
  
|<span data-ttu-id="bba04-156">模式</span><span class="sxs-lookup"><span data-stu-id="bba04-156">Pattern</span></span>|<span data-ttu-id="bba04-157">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-157">Description</span></span>|  
|-------------|-----------------|  
|`[aeiou]`|<span data-ttu-id="bba04-158">匹配所有元音。</span><span class="sxs-lookup"><span data-stu-id="bba04-158">Match all vowels.</span></span>|  
|`[\p{P}\d]`|<span data-ttu-id="bba04-159">匹配所有标点符号和十进制数字字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-159">Match all punctuation and decimal digit characters.</span></span>|  
|`[\s\p{P}]`|<span data-ttu-id="bba04-160">匹配所有空白和标点符号。</span><span class="sxs-lookup"><span data-stu-id="bba04-160">Match all white space and punctuation.</span></span>|  
  
 <span data-ttu-id="bba04-161">下面的示例定义包含字符“a”和“e”的正字符组，以使输入字符串必须包含单词“grey”或“gray”且后跟另一个单词以便进行匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-161">The following example defines a positive character group that contains the characters "a" and "e" so that the input string must contain the words "grey" or "gray" followed by another word for a match to occur.</span></span>  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/positivecharclasses.cs#1)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/positivecharclasses.vb#1)]  
  
 <span data-ttu-id="bba04-162">按以下方式定义正则表达式 `gr[ae]y\s\S+?[\s|\p{P}]`：</span><span class="sxs-lookup"><span data-stu-id="bba04-162">The regular expression `gr[ae]y\s\S+?[\s|\p{P}]` is defined as follows:</span></span>  
  
|<span data-ttu-id="bba04-163">模式</span><span class="sxs-lookup"><span data-stu-id="bba04-163">Pattern</span></span>|<span data-ttu-id="bba04-164">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-164">Description</span></span>|  
|-------------|-----------------|  
|`gr`|<span data-ttu-id="bba04-165">匹配文本字符“gr”。</span><span class="sxs-lookup"><span data-stu-id="bba04-165">Match the literal characters "gr".</span></span>|  
|`[ae]`|<span data-ttu-id="bba04-166">匹配“a”或“e”。</span><span class="sxs-lookup"><span data-stu-id="bba04-166">Match either an "a" or an "e".</span></span>|  
|`y\s`|<span data-ttu-id="bba04-167">匹配后跟空白字符的文本字符“y”。</span><span class="sxs-lookup"><span data-stu-id="bba04-167">Match the literal character "y" followed by a white-space character.</span></span>|  
|`\S+?`|<span data-ttu-id="bba04-168">匹配一个或多个非空白字符（但尽可能少）。</span><span class="sxs-lookup"><span data-stu-id="bba04-168">Match one or more non-white-space characters, but as few as possible.</span></span>|  
|`[\s\p{P}]`|<span data-ttu-id="bba04-169">匹配空白字符或标点符号。</span><span class="sxs-lookup"><span data-stu-id="bba04-169">Match either a white-space character or a punctuation mark.</span></span>|  
  
 <span data-ttu-id="bba04-170">下面的示例匹配以任何大写字母开头的单词。</span><span class="sxs-lookup"><span data-stu-id="bba04-170">The following example matches words that begin with any capital letter.</span></span> <span data-ttu-id="bba04-171">它使用子表达式 `[A-Z]` 表示从 A 到 Z 的大写字母范围。</span><span class="sxs-lookup"><span data-stu-id="bba04-171">It uses the subexpression `[A-Z]` to represent the range of capital letters from A to Z.</span></span>  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#3](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/range.cs#3)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/range.vb#3)]  
  
 <span data-ttu-id="bba04-172">正则表达式 `\b[A-Z]\w*\b` 的定义如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bba04-172">The regular expression `\b[A-Z]\w*\b` is defined as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-173">模式</span><span class="sxs-lookup"><span data-stu-id="bba04-173">Pattern</span></span>|<span data-ttu-id="bba04-174">描述</span><span class="sxs-lookup"><span data-stu-id="bba04-174">Description</span></span>|  
|-------------|-----------------|  
|`\b`|<span data-ttu-id="bba04-175">在单词边界处开始。</span><span class="sxs-lookup"><span data-stu-id="bba04-175">Start at a word boundary.</span></span>|  
|`[A-Z]`|<span data-ttu-id="bba04-176">匹配从 A 到 Z 的所有大写字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-176">Match any uppercase character from A to Z.</span></span>|  
|`\w*`|<span data-ttu-id="bba04-177">匹配零个或多个单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-177">Match zero or more word characters.</span></span>|  
|`\b`|<span data-ttu-id="bba04-178">与字边界匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-178">Match a word boundary.</span></span>|  
  
<a name="NegativeGroup"></a>

## <a name="negative-character-group-"></a><span data-ttu-id="bba04-179">负字符组：[^]</span><span class="sxs-lookup"><span data-stu-id="bba04-179">Negative character group: [^]</span></span>  

 <span data-ttu-id="bba04-180">负字符组指定一个字符列表，这些字符不得出现在输入字符串中以便进行匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-180">A negative character group specifies a list of characters that must not appear in an input string for a match to occur.</span></span> <span data-ttu-id="bba04-181">此字符列表可以单独指定和/或作为范围指定。</span><span class="sxs-lookup"><span data-stu-id="bba04-181">The list of characters may be specified individually, as a range, or both.</span></span>  
  
<span data-ttu-id="bba04-182">用于指定各个字符列表的语法如下所示：</span><span class="sxs-lookup"><span data-stu-id="bba04-182">The syntax for specifying a list of individual characters is as follows:</span></span>  

`[*^character_group*]`

 <span data-ttu-id="bba04-183">其中，*character_group* 是单个字符的列表，这些字符不可出现在输入字符串中以便成功匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-183">where *character_group* is a list of the individual characters that cannot appear in the input string for a match to succeed.</span></span> <span data-ttu-id="bba04-184">character_group 可以包含一个或多个文本字符、[转义字符](character-escapes-in-regular-expressions.md)或字符类的任意组合。</span><span class="sxs-lookup"><span data-stu-id="bba04-184">*character_group* can consist of any combination of one or more literal characters, [escape characters](character-escapes-in-regular-expressions.md), or character classes.</span></span>  
  
 <span data-ttu-id="bba04-185">用于指定字符范围的语法如下：</span><span class="sxs-lookup"><span data-stu-id="bba04-185">The syntax for specifying a range of characters is as follows:</span></span>  

`[^*firstCharacter*-*lastCharacter*]`

<span data-ttu-id="bba04-186">其中，*firstCharacter* 是范围的开始字符，*lastCharacter* 是范围的结束字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-186">where *firstCharacter* is the character that begins the range and *lastCharacter* is the character that ends the range.</span></span> <span data-ttu-id="bba04-187">字符范围是通过以下方式定义的一系列连续字符：指定系列中的第一个字符，连字符 (-)，然后指定系列中的最后一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-187">A character range is a contiguous series of characters defined by specifying the first character in the series, a hyphen (-), and then the last character in the series.</span></span> <span data-ttu-id="bba04-188">如果两个字符具有相邻的 Unicode 码位，则这两个字符是连续的。</span><span class="sxs-lookup"><span data-stu-id="bba04-188">Two characters are contiguous if they have adjacent Unicode code points.</span></span> <span data-ttu-id="bba04-189">firstCharacter 必须是码位较低的字符，而 lastCharacter 必须是码位较高的字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-189">*firstCharacter* must be the character with the lower code point, and *lastCharacter* must be the character with the higher code point.</span></span>

> [!NOTE]
> <span data-ttu-id="bba04-190">由于负字符组可以包含一组字符和一个字符范围，因此连字符 (`-`) 始终被解释为范围分隔符，除非它是该组的第一个或最后一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-190">Because a negative character group can include both a set of characters and a character range, a hyphen character (`-`) is always interpreted as the range separator unless it is the first or last character of the group.</span></span>
  
 <span data-ttu-id="bba04-191">可以连接两个或更多字符范围。</span><span class="sxs-lookup"><span data-stu-id="bba04-191">Two or more character ranges can be concatenated.</span></span> <span data-ttu-id="bba04-192">例如，若要指定从“0”至“9”的十进制数范围、从“a”至“f”的小写字母范围，以及从“A”至“F”的大写字母范围，请使用 `[0-9a-fA-F]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-192">For example, to specify the range of decimal digits from "0" through "9", the range of lowercase letters from "a" through "f", and the range of uppercase letters from "A" through "F", use `[0-9a-fA-F]`.</span></span>  
  
 <span data-ttu-id="bba04-193">负字符组中的前导符 (`^`) 是强制的，指示字符组为负字符组，而不是正字符组。</span><span class="sxs-lookup"><span data-stu-id="bba04-193">The leading caret character (`^`) in a negative character group is mandatory and indicates the character group is a negative character group instead of a positive character group.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="bba04-194">较大正则表达式模式中的负字符组不是零宽度断言。</span><span class="sxs-lookup"><span data-stu-id="bba04-194">A negative character group in a larger regular expression pattern is not a zero-width assertion.</span></span> <span data-ttu-id="bba04-195">也就是说，在评估负字符组后，正则表达式引擎会在输入字符串中提升一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-195">That is, after evaluating the negative character group, the regular expression engine advances one character in the input string.</span></span>  
  
 <span data-ttu-id="bba04-196">下表列出了一些常见的包含负字符组的正则表达式模式。</span><span class="sxs-lookup"><span data-stu-id="bba04-196">Some common regular expression patterns that contain negative character groups are listed in the following table.</span></span>  
  
|<span data-ttu-id="bba04-197">模式</span><span class="sxs-lookup"><span data-stu-id="bba04-197">Pattern</span></span>|<span data-ttu-id="bba04-198">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-198">Description</span></span>|  
|-------------|-----------------|  
|`[^aeiou]`|<span data-ttu-id="bba04-199">匹配除元音以外的所有字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-199">Match all characters except vowels.</span></span>|  
|`[^\p{P}\d]`|<span data-ttu-id="bba04-200">匹配标点符号和十进制数字字符以外的所有字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-200">Match all characters except punctuation and decimal digit characters.</span></span>|  
  
 <span data-ttu-id="bba04-201">下面的示例匹配以字符“th”开头且后面不跟“o”的任何单词。</span><span class="sxs-lookup"><span data-stu-id="bba04-201">The following example matches any word that begins with the characters "th" and is not followed by an "o".</span></span>  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/negativecharclasses.cs#2)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/negativecharclasses.vb#2)]  
  
 <span data-ttu-id="bba04-202">正则表达式 `\bth[^o]\w+\b` 的定义如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bba04-202">The regular expression `\bth[^o]\w+\b` is defined as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-203">模式</span><span class="sxs-lookup"><span data-stu-id="bba04-203">Pattern</span></span>|<span data-ttu-id="bba04-204">描述</span><span class="sxs-lookup"><span data-stu-id="bba04-204">Description</span></span>|  
|-------------|-----------------|  
|`\b`|<span data-ttu-id="bba04-205">在单词边界处开始。</span><span class="sxs-lookup"><span data-stu-id="bba04-205">Start at a word boundary.</span></span>|  
|`th`|<span data-ttu-id="bba04-206">匹配文本字符“th”。</span><span class="sxs-lookup"><span data-stu-id="bba04-206">Match the literal characters "th".</span></span>|  
|`[^o]`|<span data-ttu-id="bba04-207">与不是“o”的任何字符匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-207">Match any character that is not an "o".</span></span>|  
|`\w+`|<span data-ttu-id="bba04-208">匹配一个或多个单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-208">Match one or more word characters.</span></span>|  
|`\b`|<span data-ttu-id="bba04-209">在字边界结束。</span><span class="sxs-lookup"><span data-stu-id="bba04-209">End at a word boundary.</span></span>|  
  
<a name="AnyCharacter"></a>

## <a name="any-character-"></a><span data-ttu-id="bba04-210">任意字符：.</span><span class="sxs-lookup"><span data-stu-id="bba04-210">Any character: .</span></span>  

 <span data-ttu-id="bba04-211">句点字符 (.) 匹配除 `\n`（换行符 \u000A）之外的任何字符，有以下两个限制：</span><span class="sxs-lookup"><span data-stu-id="bba04-211">The period character (.) matches any character except `\n` (the newline character, \u000A), with the following two qualifications:</span></span>  
  
- <span data-ttu-id="bba04-212">如果通过 <xref:System.Text.RegularExpressions.RegexOptions.Singleline?displayProperty=nameWithType> 选项修改正则表达式模式，或者通过 `.` 选项修改包含 `s` 字符类的模式的部分，则 `.` 可匹配任何字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-212">If a regular expression pattern is modified by the <xref:System.Text.RegularExpressions.RegexOptions.Singleline?displayProperty=nameWithType> option, or if the portion of the pattern that contains the `.` character class is modified by the `s` option, `.` matches any character.</span></span> <span data-ttu-id="bba04-213">有关详细信息，请参阅 [正则表达式选项](regular-expression-options.md)。</span><span class="sxs-lookup"><span data-stu-id="bba04-213">For more information, see [Regular Expression Options](regular-expression-options.md).</span></span>  
  
     <span data-ttu-id="bba04-214">下面的示例阐释了默认情况下以及使用 `.` 选项的情况下 <xref:System.Text.RegularExpressions.RegexOptions.Singleline?displayProperty=nameWithType> 字符类的不同的行为。</span><span class="sxs-lookup"><span data-stu-id="bba04-214">The following example illustrates the different behavior of the `.` character class by default and with the <xref:System.Text.RegularExpressions.RegexOptions.Singleline?displayProperty=nameWithType> option.</span></span> <span data-ttu-id="bba04-215">正则表达式 `^.+` 在字符串开头开始并匹配每个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-215">The regular expression `^.+` starts at the beginning of the string and matches every character.</span></span> <span data-ttu-id="bba04-216">默认情况下，匹配在第一行的结尾结束；正则表达式模式匹配回车符、`\r` 或 \u000D，但不匹配 `\n`。</span><span class="sxs-lookup"><span data-stu-id="bba04-216">By default, the match ends at the end of the first line; the regular expression pattern matches the carriage return character, `\r` or \u000D, but it does not match `\n`.</span></span> <span data-ttu-id="bba04-217">由于 <xref:System.Text.RegularExpressions.RegexOptions.Singleline?displayProperty=nameWithType> 选项将整个输入字符串解释为单行，因此它匹配输入字符串中的每个字符，包括 `\n`。</span><span class="sxs-lookup"><span data-stu-id="bba04-217">Because the <xref:System.Text.RegularExpressions.RegexOptions.Singleline?displayProperty=nameWithType> option interprets the entire input string as a single line, it matches every character in the input string, including `\n`.</span></span>  
  
     [!code-csharp[Conceptual.Regex.Language.CharacterClasses#5](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/any2.cs#5)]
     [!code-vb[Conceptual.Regex.Language.CharacterClasses#5](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/any2.vb#5)]  
  
> [!NOTE]
> <span data-ttu-id="bba04-218">由于它匹配除 `\n` 之外的任何字符，因此 `.` 字符类也匹配 `\r`（回车符 \u000D）。</span><span class="sxs-lookup"><span data-stu-id="bba04-218">Because it matches any character except `\n`, the `.` character class also matches `\r` (the carriage return character, \u000D).</span></span>  
  
- <span data-ttu-id="bba04-219">正字符组或负字符组中的句点字符将被视为原义句点字符，而非字符类。</span><span class="sxs-lookup"><span data-stu-id="bba04-219">In a positive or negative character group, a period is treated as a literal period character, and not as a character class.</span></span> <span data-ttu-id="bba04-220">有关详细信息，请参阅本主题前面部分的[正字符组](#PositiveGroup)和[负字符组](#NegativeGroup)。</span><span class="sxs-lookup"><span data-stu-id="bba04-220">For more information, see [Positive Character Group](#PositiveGroup) and [Negative Character Group](#NegativeGroup) earlier in this topic.</span></span> <span data-ttu-id="bba04-221">下面的示例通过定义包括句点字符 (`.`) 的正则表达式作为字符类和正字符组的成员来进行这方面的演示。</span><span class="sxs-lookup"><span data-stu-id="bba04-221">The following example provides an illustration by defining a regular expression that includes the period character (`.`) both as a character class and as a member of a positive character group.</span></span> <span data-ttu-id="bba04-222">正则表达式 `\b.*[.?!;:](\s|\z)` 在字边界处开始，匹配任何字符直到遇到五个标点符号标记之一（包括句点），然后匹配空白字符或字符串的末尾。</span><span class="sxs-lookup"><span data-stu-id="bba04-222">The regular expression `\b.*[.?!;:](\s|\z)` begins at a word boundary, matches any character until it encounters one of five punctuation marks, including a period, and then matches either a white-space character or the end of the string.</span></span>  
  
     [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#4](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/any1.cs#4)]
     [!code-vb[Conceptual.RegEx.Language.CharacterClasses#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/any1.vb#4)]  
  
> [!NOTE]
> <span data-ttu-id="bba04-223">由于它匹配任何字符，因此当正则表达式模式尝试多次匹配任何字符时，`.` 语言元素通常会与惰性限定符一起使用。</span><span class="sxs-lookup"><span data-stu-id="bba04-223">Because it matches any character, the `.` language element is often used with a lazy quantifier if a regular expression pattern attempts to match any character multiple times.</span></span> <span data-ttu-id="bba04-224">有关更多信息，请参见 [数量词](quantifiers-in-regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="bba04-224">For more information, see [Quantifiers](quantifiers-in-regular-expressions.md).</span></span>  
  
<a name="CategoryOrBlock"></a>

## <a name="unicode-category-or-unicode-block-p"></a><span data-ttu-id="bba04-225">Unicode 类别或 Unicode 块：\p{}</span><span class="sxs-lookup"><span data-stu-id="bba04-225">Unicode category or Unicode block: \p{}</span></span>  

 <span data-ttu-id="bba04-226">Unicode 标准为每个常规类别分配一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-226">The Unicode standard assigns each character a general category.</span></span> <span data-ttu-id="bba04-227">例如，特定字符可以是大写字母（由 `Lu` 类别表示），十进制数字（`Nd` 类别）、数学符号（`Sm` 类别）或段落分隔符（`Zl` 类别）。</span><span class="sxs-lookup"><span data-stu-id="bba04-227">For example, a particular character can be an uppercase letter (represented by the `Lu` category), a decimal digit (the `Nd` category), a math symbol (the `Sm` category), or a paragraph separator (the `Zl` category).</span></span> <span data-ttu-id="bba04-228">Unicode 标准中的特定字符集也占据连续码位的特定区域或块。</span><span class="sxs-lookup"><span data-stu-id="bba04-228">Specific character sets in the Unicode standard also occupy a specific range or block of consecutive code points.</span></span> <span data-ttu-id="bba04-229">例如，可在 \u0000 和 \u007F 之间找到基本拉丁字符集，并可在 \u0600 和 \u06FF 之间找到阿拉伯语字符集。</span><span class="sxs-lookup"><span data-stu-id="bba04-229">For example, the basic Latin character set is found from \u0000 through \u007F, while the Arabic character set is found from \u0600 through \u06FF.</span></span>  
  
 <span data-ttu-id="bba04-230">正则表达式构造</span><span class="sxs-lookup"><span data-stu-id="bba04-230">The regular expression construct</span></span>  
  
 <span data-ttu-id="bba04-231">`\p{` *name* `}`</span><span class="sxs-lookup"><span data-stu-id="bba04-231">`\p{` *name* `}`</span></span>  
  
 <span data-ttu-id="bba04-232">匹配属于 Unicode 常规类别或命名块的任何字符，其中，name 是类别缩写或命名块的名称。</span><span class="sxs-lookup"><span data-stu-id="bba04-232">matches any character that belongs to a Unicode general category or named block, where *name* is the category abbreviation or named block name.</span></span> <span data-ttu-id="bba04-233">有关类别缩写的列表，请参阅本主题稍后的[支持的 Unicode 常规类别](#SupportedUnicodeGeneralCategories)部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-233">For a list of category abbreviations, see the [Supported Unicode General Categories](#SupportedUnicodeGeneralCategories) section later in this topic.</span></span> <span data-ttu-id="bba04-234">有关命名块的列表，请参阅本主题稍后的[支持的命名块](#SupportedNamedBlocks)部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-234">For a list of named blocks, see the [Supported Named Blocks](#SupportedNamedBlocks) section later in this topic.</span></span>  
  
 <span data-ttu-id="bba04-235">下面的示例使用 `\p{`名称`}` 构造以匹配 Unicode 常规类别（在该示例中为 `Pd` 或“标点，短划线”类别）和命名块（`IsGreek` 和 `IsBasicLatin` 命名块）。</span><span class="sxs-lookup"><span data-stu-id="bba04-235">The following example uses the `\p{`*name*`}` construct to match both a Unicode general category (in this case, the `Pd`, or Punctuation, Dash category) and a named block (the `IsGreek` and `IsBasicLatin` named blocks).</span></span>  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#6](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/category1.cs#6)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/category1.vb#6)]  
  
 <span data-ttu-id="bba04-236">正则表达式 `\b(\p{IsGreek}+(\s)?)+\p{Pd}\s(\p{IsBasicLatin}+(\s)?)+` 的定义如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bba04-236">The regular expression `\b(\p{IsGreek}+(\s)?)+\p{Pd}\s(\p{IsBasicLatin}+(\s)?)+` is defined as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-237">模式</span><span class="sxs-lookup"><span data-stu-id="bba04-237">Pattern</span></span>|<span data-ttu-id="bba04-238">描述</span><span class="sxs-lookup"><span data-stu-id="bba04-238">Description</span></span>|  
|-------------|-----------------|  
|`\b`|<span data-ttu-id="bba04-239">在单词边界处开始。</span><span class="sxs-lookup"><span data-stu-id="bba04-239">Start at a word boundary.</span></span>|  
|`\p{IsGreek}+`|<span data-ttu-id="bba04-240">匹配一个或多个希腊语字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-240">Match one or more Greek characters.</span></span>|  
|`(\s)?`|<span data-ttu-id="bba04-241">匹配零个或一个空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-241">Match zero or one white-space character.</span></span>|  
|`(\p{IsGreek}+(\s)?)+`|<span data-ttu-id="bba04-242">匹配一个或多个希腊语字符后跟零个或一个空白字符的模式一次或多次。</span><span class="sxs-lookup"><span data-stu-id="bba04-242">Match the pattern of one or more Greek characters followed by zero or one white-space characters one or more times.</span></span>|  
|`\p{Pd}`|<span data-ttu-id="bba04-243">匹配“标点，短划线”字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-243">Match a Punctuation, Dash character.</span></span>|  
|`\s`|<span data-ttu-id="bba04-244">与空白字符匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-244">Match a white-space character.</span></span>|  
|`\p{IsBasicLatin}+`|<span data-ttu-id="bba04-245">匹配一个或多个基本拉丁字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-245">Match one or more basic Latin characters.</span></span>|  
|`(\s)?`|<span data-ttu-id="bba04-246">匹配零个或一个空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-246">Match zero or one white-space character.</span></span>|  
|`(\p{IsBasicLatin}+(\s)?)+`|<span data-ttu-id="bba04-247">匹配一个或多个基本拉丁字符后跟零个或一个空白字符的模式一次或多次。</span><span class="sxs-lookup"><span data-stu-id="bba04-247">Match the pattern of one or more basic Latin characters followed by zero or one white-space characters one or more times.</span></span>|  
  
<a name="NegativeCategoryOrBlock"></a>

## <a name="negative-unicode-category-or-unicode-block-p"></a><span data-ttu-id="bba04-248">负 Unicode 类别或 Unicode 块：\P{}</span><span class="sxs-lookup"><span data-stu-id="bba04-248">Negative Unicode category or Unicode block: \P{}</span></span>  

 <span data-ttu-id="bba04-249">Unicode 标准为每个常规类别分配一个字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-249">The Unicode standard assigns each character a general category.</span></span> <span data-ttu-id="bba04-250">例如，特定字符可以是大写字母（由 `Lu` 类别表示），十进制数字（`Nd` 类别）、数学符号（`Sm` 类别）或段落分隔符（`Zl` 类别）。</span><span class="sxs-lookup"><span data-stu-id="bba04-250">For example, a particular character can be an uppercase letter (represented by the `Lu` category), a decimal digit (the `Nd` category), a math symbol (the `Sm` category), or a paragraph separator (the `Zl` category).</span></span> <span data-ttu-id="bba04-251">Unicode 标准中的特定字符集也占据连续码位的特定区域或块。</span><span class="sxs-lookup"><span data-stu-id="bba04-251">Specific character sets in the Unicode standard also occupy a specific range or block of consecutive code points.</span></span> <span data-ttu-id="bba04-252">例如，可在 \u0000 和 \u007F 之间找到基本拉丁字符集，并可在 \u0600 和 \u06FF 之间找到阿拉伯语字符集。</span><span class="sxs-lookup"><span data-stu-id="bba04-252">For example, the basic Latin character set is found from \u0000 through \u007F, while the Arabic character set is found from \u0600 through \u06FF.</span></span>  
  
 <span data-ttu-id="bba04-253">正则表达式构造</span><span class="sxs-lookup"><span data-stu-id="bba04-253">The regular expression construct</span></span>  
  
 <span data-ttu-id="bba04-254">`\P{` *name* `}`</span><span class="sxs-lookup"><span data-stu-id="bba04-254">`\P{` *name* `}`</span></span>  
  
 <span data-ttu-id="bba04-255">匹配不属于 Unicode 常规类别或命名块的任何字符，其中，name是类别缩写或命名块的名称。</span><span class="sxs-lookup"><span data-stu-id="bba04-255">matches any character that does not belong to a Unicode general category or named block, where *name* is the category abbreviation or named block name.</span></span> <span data-ttu-id="bba04-256">有关类别缩写的列表，请参阅本主题稍后的[支持的 Unicode 常规类别](#SupportedUnicodeGeneralCategories)部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-256">For a list of category abbreviations, see the [Supported Unicode General Categories](#SupportedUnicodeGeneralCategories) section later in this topic.</span></span> <span data-ttu-id="bba04-257">有关命名块的列表，请参阅本主题稍后的[支持的命名块](#SupportedNamedBlocks)部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-257">For a list of named blocks, see the [Supported Named Blocks](#SupportedNamedBlocks) section later in this topic.</span></span>  
  
 <span data-ttu-id="bba04-258">下面的示例使用 `\P{`name`}`构造来删除数字字符串中的任何货币符号（在该示例中为 `Sc` 或“符号，货币”类别）。</span><span class="sxs-lookup"><span data-stu-id="bba04-258">The following example uses the `\P{`*name*`}` construct to remove any currency symbols (in this case, the `Sc`, or Symbol, Currency category) from numeric strings.</span></span>  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#7](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/notcategory1.cs#7)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#7](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/notcategory1.vb#7)]  
  
 <span data-ttu-id="bba04-259">正则表达式模式 `(\P{Sc})+` 匹配不为货币符号的一个或多个字符；它有效地从结果字符串中抽出任何货币符号。</span><span class="sxs-lookup"><span data-stu-id="bba04-259">The regular expression pattern `(\P{Sc})+` matches one or more characters that are not currency symbols; it effectively strips any currency symbol from the result string.</span></span>  
  
<a name="WordCharacter"></a>

## <a name="word-character-w"></a><span data-ttu-id="bba04-260">单词字符：\w</span><span class="sxs-lookup"><span data-stu-id="bba04-260">Word character: \w</span></span>  

 <span data-ttu-id="bba04-261">`\w` 与任何单词字符匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-261">`\w` matches any word character.</span></span> <span data-ttu-id="bba04-262">单词字符是下表中列出的任何 Unicode 类别的成员。</span><span class="sxs-lookup"><span data-stu-id="bba04-262">A word character is a member of any of the Unicode categories listed in the following table.</span></span>  
  
|<span data-ttu-id="bba04-263">Category</span><span class="sxs-lookup"><span data-stu-id="bba04-263">Category</span></span>|<span data-ttu-id="bba04-264">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-264">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="bba04-265">Ll</span><span class="sxs-lookup"><span data-stu-id="bba04-265">Ll</span></span>|<span data-ttu-id="bba04-266">字母，小写</span><span class="sxs-lookup"><span data-stu-id="bba04-266">Letter, Lowercase</span></span>|  
|<span data-ttu-id="bba04-267">Lu</span><span class="sxs-lookup"><span data-stu-id="bba04-267">Lu</span></span>|<span data-ttu-id="bba04-268">字母，大写</span><span class="sxs-lookup"><span data-stu-id="bba04-268">Letter, Uppercase</span></span>|  
|<span data-ttu-id="bba04-269">Lt</span><span class="sxs-lookup"><span data-stu-id="bba04-269">Lt</span></span>|<span data-ttu-id="bba04-270">字母，首字母大写</span><span class="sxs-lookup"><span data-stu-id="bba04-270">Letter, Titlecase</span></span>|  
|<span data-ttu-id="bba04-271">Lo</span><span class="sxs-lookup"><span data-stu-id="bba04-271">Lo</span></span>|<span data-ttu-id="bba04-272">字母，其他</span><span class="sxs-lookup"><span data-stu-id="bba04-272">Letter, Other</span></span>|  
|<span data-ttu-id="bba04-273">Lm</span><span class="sxs-lookup"><span data-stu-id="bba04-273">Lm</span></span>|<span data-ttu-id="bba04-274">字母，修饰符</span><span class="sxs-lookup"><span data-stu-id="bba04-274">Letter, Modifier</span></span>|  
|<span data-ttu-id="bba04-275">Mn</span><span class="sxs-lookup"><span data-stu-id="bba04-275">Mn</span></span>|<span data-ttu-id="bba04-276">标记，非间距</span><span class="sxs-lookup"><span data-stu-id="bba04-276">Mark, Nonspacing</span></span>|  
|<span data-ttu-id="bba04-277">Nd</span><span class="sxs-lookup"><span data-stu-id="bba04-277">Nd</span></span>|<span data-ttu-id="bba04-278">数字，十进制数</span><span class="sxs-lookup"><span data-stu-id="bba04-278">Number, Decimal Digit</span></span>|  
|<span data-ttu-id="bba04-279">Pc</span><span class="sxs-lookup"><span data-stu-id="bba04-279">Pc</span></span>|<span data-ttu-id="bba04-280">标点，连接符。</span><span class="sxs-lookup"><span data-stu-id="bba04-280">Punctuation, Connector.</span></span> <span data-ttu-id="bba04-281">此类别包含 10 个字符，最常用的字符是 LOWLINE 字符 (_)，u+005F。</span><span class="sxs-lookup"><span data-stu-id="bba04-281">This category includes ten characters, the most commonly used of which is the LOWLINE character (_), u+005F.</span></span>|  
  
 <span data-ttu-id="bba04-282">如果指定了符合 ECMAScript 的行为，则 `\w` 等效于 `[a-zA-Z_0-9]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-282">If ECMAScript-compliant behavior is specified, `\w` is equivalent to `[a-zA-Z_0-9]`.</span></span> <span data-ttu-id="bba04-283">有关 ECMAScript 正则表达式的信息，请参阅[正则表达式选项](regular-expression-options.md)中的“ECMAScript 匹配行为”部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-283">For information on ECMAScript regular expressions, see the "ECMAScript Matching Behavior" section in [Regular Expression Options](regular-expression-options.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="bba04-284">由于它匹配任何单词字符，因此当正则表达式模式尝试多次匹配任何单词字符且后跟特定单词字符时，`\w` 语言元素通常会与惰性限定符一起使用。</span><span class="sxs-lookup"><span data-stu-id="bba04-284">Because it matches any word character, the `\w` language element is often used with a lazy quantifier if a regular expression pattern attempts to match any word character multiple times, followed by a specific word character.</span></span> <span data-ttu-id="bba04-285">有关更多信息，请参见 [数量词](quantifiers-in-regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="bba04-285">For more information, see [Quantifiers](quantifiers-in-regular-expressions.md).</span></span>  
  
 <span data-ttu-id="bba04-286">下面的示例使用 `\w` 语言元素来匹配单词中的重复字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-286">The following example uses the `\w` language element to match duplicate characters in a word.</span></span> <span data-ttu-id="bba04-287">该示例定义可按如下方式解释的正则表达式模式 `(\w)\1`。</span><span class="sxs-lookup"><span data-stu-id="bba04-287">The example defines a regular expression pattern, `(\w)\1`, which can be interpreted as follows.</span></span>  
  
|<span data-ttu-id="bba04-288">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-288">Element</span></span>|<span data-ttu-id="bba04-289">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-289">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bba04-290">(\w)</span><span class="sxs-lookup"><span data-stu-id="bba04-290">(\w)</span></span>|<span data-ttu-id="bba04-291">匹配单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-291">Match a word character.</span></span> <span data-ttu-id="bba04-292">这是第一个捕获组。</span><span class="sxs-lookup"><span data-stu-id="bba04-292">This is the first capturing group.</span></span>|  
|<span data-ttu-id="bba04-293">\1</span><span class="sxs-lookup"><span data-stu-id="bba04-293">\1</span></span>|<span data-ttu-id="bba04-294">匹配第一次捕获的值。</span><span class="sxs-lookup"><span data-stu-id="bba04-294">Match the value of the first capture.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#8](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/wordchar1.cs#8)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#8](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/wordchar1.vb#8)]  
  
<a name="NonWordCharacter"></a>

## <a name="non-word-character-w"></a><span data-ttu-id="bba04-295">非单词字符：\W</span><span class="sxs-lookup"><span data-stu-id="bba04-295">Non-word character: \W</span></span>  

 <span data-ttu-id="bba04-296">`\W` 匹配任何非单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-296">`\W` matches any non-word character.</span></span> <span data-ttu-id="bba04-297">\W 语言元素等效于以下字符类：</span><span class="sxs-lookup"><span data-stu-id="bba04-297">The \W language element is equivalent to the following character class:</span></span>  
  
`[^\p{Ll}\p{Lu}\p{Lt}\p{Lo}\p{Nd}\p{Pc}\p{Lm}]`  
  
 <span data-ttu-id="bba04-298">换言之，它与下表列出的 Unicode 类别中的字符以外的任何字符匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-298">In other words, it matches any character except for those in the Unicode categories listed in the following table.</span></span>  
  
|<span data-ttu-id="bba04-299">Category</span><span class="sxs-lookup"><span data-stu-id="bba04-299">Category</span></span>|<span data-ttu-id="bba04-300">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-300">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="bba04-301">Ll</span><span class="sxs-lookup"><span data-stu-id="bba04-301">Ll</span></span>|<span data-ttu-id="bba04-302">字母，小写</span><span class="sxs-lookup"><span data-stu-id="bba04-302">Letter, Lowercase</span></span>|  
|<span data-ttu-id="bba04-303">Lu</span><span class="sxs-lookup"><span data-stu-id="bba04-303">Lu</span></span>|<span data-ttu-id="bba04-304">字母，大写</span><span class="sxs-lookup"><span data-stu-id="bba04-304">Letter, Uppercase</span></span>|  
|<span data-ttu-id="bba04-305">Lt</span><span class="sxs-lookup"><span data-stu-id="bba04-305">Lt</span></span>|<span data-ttu-id="bba04-306">字母，首字母大写</span><span class="sxs-lookup"><span data-stu-id="bba04-306">Letter, Titlecase</span></span>|  
|<span data-ttu-id="bba04-307">Lo</span><span class="sxs-lookup"><span data-stu-id="bba04-307">Lo</span></span>|<span data-ttu-id="bba04-308">字母，其他</span><span class="sxs-lookup"><span data-stu-id="bba04-308">Letter, Other</span></span>|  
|<span data-ttu-id="bba04-309">Lm</span><span class="sxs-lookup"><span data-stu-id="bba04-309">Lm</span></span>|<span data-ttu-id="bba04-310">字母，修饰符</span><span class="sxs-lookup"><span data-stu-id="bba04-310">Letter, Modifier</span></span>|  
|<span data-ttu-id="bba04-311">Mn</span><span class="sxs-lookup"><span data-stu-id="bba04-311">Mn</span></span>|<span data-ttu-id="bba04-312">标记，非间距</span><span class="sxs-lookup"><span data-stu-id="bba04-312">Mark, Nonspacing</span></span>|  
|<span data-ttu-id="bba04-313">Nd</span><span class="sxs-lookup"><span data-stu-id="bba04-313">Nd</span></span>|<span data-ttu-id="bba04-314">数字，十进制数</span><span class="sxs-lookup"><span data-stu-id="bba04-314">Number, Decimal Digit</span></span>|  
|<span data-ttu-id="bba04-315">Pc</span><span class="sxs-lookup"><span data-stu-id="bba04-315">Pc</span></span>|<span data-ttu-id="bba04-316">标点，连接符。</span><span class="sxs-lookup"><span data-stu-id="bba04-316">Punctuation, Connector.</span></span> <span data-ttu-id="bba04-317">此类别包含 10 个字符，最常用的字符是 LOWLINE 字符 (_)，u+005F。</span><span class="sxs-lookup"><span data-stu-id="bba04-317">This category includes ten characters, the most commonly used of which is the LOWLINE character (_), u+005F.</span></span>|  
  
 <span data-ttu-id="bba04-318">如果指定了符合 ECMAScript 的行为，则 `\W` 等效于 `[^a-zA-Z_0-9]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-318">If ECMAScript-compliant behavior is specified, `\W` is equivalent to `[^a-zA-Z_0-9]`.</span></span> <span data-ttu-id="bba04-319">有关 ECMAScript 正则表达式的信息，请参阅[正则表达式选项](regular-expression-options.md)中的“ECMAScript 匹配行为”部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-319">For information on ECMAScript regular expressions, see the "ECMAScript Matching Behavior" section in [Regular Expression Options](regular-expression-options.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="bba04-320">由于它匹配任何非单词字符，因此当正则表达式模式尝试多次匹配任何非单词字符且后跟特定非单词字符时，`\W` 语言元素通常会与惰性限定符一起使用。</span><span class="sxs-lookup"><span data-stu-id="bba04-320">Because it matches any non-word character, the `\W` language element is often used with a lazy quantifier if a regular expression pattern attempts to match any non-word character multiple times followed by a specific non-word character.</span></span> <span data-ttu-id="bba04-321">有关更多信息，请参见 [数量词](quantifiers-in-regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="bba04-321">For more information, see [Quantifiers](quantifiers-in-regular-expressions.md).</span></span>  
  
 <span data-ttu-id="bba04-322">下面的示例阐释 `\W` 字符类。</span><span class="sxs-lookup"><span data-stu-id="bba04-322">The following example illustrates the `\W` character class.</span></span>  <span data-ttu-id="bba04-323">它定义正则表达式模式 `\b(\w+)(\W){1,2}`，该模式匹配后跟一个或两个非单词字符（例如，空白或标点符号）的单词。</span><span class="sxs-lookup"><span data-stu-id="bba04-323">It defines a regular expression pattern, `\b(\w+)(\W){1,2}`, that matches a word followed by one or two non-word characters, such as white space or punctuation.</span></span> <span data-ttu-id="bba04-324">正则表达式模式可以解释为下表中所示内容。</span><span class="sxs-lookup"><span data-stu-id="bba04-324">The regular expression is interpreted as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-325">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-325">Element</span></span>|<span data-ttu-id="bba04-326">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-326">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bba04-327">\b</span><span class="sxs-lookup"><span data-stu-id="bba04-327">\b</span></span>|<span data-ttu-id="bba04-328">在单词边界处开始匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-328">Begin the match at a word boundary.</span></span>|  
|<span data-ttu-id="bba04-329">(\w+)</span><span class="sxs-lookup"><span data-stu-id="bba04-329">(\w+)</span></span>|<span data-ttu-id="bba04-330">匹配一个或多个单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-330">Match one or more word characters.</span></span> <span data-ttu-id="bba04-331">这是第一个捕获组。</span><span class="sxs-lookup"><span data-stu-id="bba04-331">This is the first capturing group.</span></span>|  
|<span data-ttu-id="bba04-332">(\W){1,2}</span><span class="sxs-lookup"><span data-stu-id="bba04-332">(\W){1,2}</span></span>|<span data-ttu-id="bba04-333">匹配非单词字符一次或两次。</span><span class="sxs-lookup"><span data-stu-id="bba04-333">Match a non-word character either one or two times.</span></span> <span data-ttu-id="bba04-334">这是第二个捕获组。</span><span class="sxs-lookup"><span data-stu-id="bba04-334">This is the second capturing group.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#9](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/nonwordchar1.cs#9)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#9](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/nonwordchar1.vb#9)]  
  
 <span data-ttu-id="bba04-335">由于第二个捕获组的 <xref:System.Text.RegularExpressions.Group> 对象仅包含单个捕获的非单词字符，因此该示例将从 <xref:System.Text.RegularExpressions.CaptureCollection> 属性返回的 <xref:System.Text.RegularExpressions.Group.Captures%2A?displayProperty=nameWithType> 对象中检索所有捕获的非单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-335">Because the <xref:System.Text.RegularExpressions.Group> object for the second capturing group contains only a single captured non-word character, the example retrieves all captured non-word characters from the <xref:System.Text.RegularExpressions.CaptureCollection> object that is returned by the <xref:System.Text.RegularExpressions.Group.Captures%2A?displayProperty=nameWithType> property.</span></span>  
  
<a name="WhitespaceCharacter"></a>

## <a name="whitespace-character-s"></a><span data-ttu-id="bba04-336">空格字符：\s</span><span class="sxs-lookup"><span data-stu-id="bba04-336">Whitespace character: \s</span></span>  

 <span data-ttu-id="bba04-337">`\s` 匹配任意空格字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-337">`\s` matches any whitespace character.</span></span> <span data-ttu-id="bba04-338">它等效于下表中列出的转义序列和 Unicode 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-338">It is equivalent to the escape sequences and Unicode categories listed in the following table.</span></span>  
  
|<span data-ttu-id="bba04-339">Category</span><span class="sxs-lookup"><span data-stu-id="bba04-339">Category</span></span>|<span data-ttu-id="bba04-340">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-340">Description</span></span>|  
|--------------|-----------------|  
|`\f`|<span data-ttu-id="bba04-341">窗体换页符，\u000C。</span><span class="sxs-lookup"><span data-stu-id="bba04-341">The form feed character, \u000C.</span></span>|  
|`\n`|<span data-ttu-id="bba04-342">换行符，\u000A。</span><span class="sxs-lookup"><span data-stu-id="bba04-342">The newline character, \u000A.</span></span>|  
|`\r`|<span data-ttu-id="bba04-343">回车符，\u000D。</span><span class="sxs-lookup"><span data-stu-id="bba04-343">The carriage return character, \u000D.</span></span>|  
|`\t`|<span data-ttu-id="bba04-344">制表符，\u0009。</span><span class="sxs-lookup"><span data-stu-id="bba04-344">The tab character, \u0009.</span></span>|  
|`\v`|<span data-ttu-id="bba04-345">垂直制表符，\u000B。</span><span class="sxs-lookup"><span data-stu-id="bba04-345">The vertical tab character, \u000B.</span></span>|  
|`\x85`|<span data-ttu-id="bba04-346">省略号或 NEXT LINE (NEL) 字符 (…)，\u0085。</span><span class="sxs-lookup"><span data-stu-id="bba04-346">The ellipsis or NEXT LINE (NEL) character (…), \u0085.</span></span>|  
|`\p{Z}`|<span data-ttu-id="bba04-347">匹配任何分隔符。</span><span class="sxs-lookup"><span data-stu-id="bba04-347">Matches any separator character.</span></span>|  
  
 <span data-ttu-id="bba04-348">如果指定了符合 ECMAScript 的行为，则 `\s` 等效于 `[ \f\n\r\t\v]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-348">If ECMAScript-compliant behavior is specified, `\s` is equivalent to `[ \f\n\r\t\v]`.</span></span> <span data-ttu-id="bba04-349">有关 ECMAScript 正则表达式的信息，请参阅[正则表达式选项](regular-expression-options.md)中的“ECMAScript 匹配行为”部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-349">For information on ECMAScript regular expressions, see the "ECMAScript Matching Behavior" section in [Regular Expression Options](regular-expression-options.md).</span></span>  
  
 <span data-ttu-id="bba04-350">下面的示例阐释 `\s` 字符类。</span><span class="sxs-lookup"><span data-stu-id="bba04-350">The following example illustrates the `\s` character class.</span></span> <span data-ttu-id="bba04-351">它定义正则表达式模式 `\b\w+(e)?s(\s|$)`，该模式匹配以“s”或“es”结尾且后跟一个空白字符或输入字符串末尾的单词。</span><span class="sxs-lookup"><span data-stu-id="bba04-351">It defines a regular expression pattern, `\b\w+(e)?s(\s|$)`, that matches a word ending in either "s" or "es" followed by either a white-space character or the end of the input string.</span></span> <span data-ttu-id="bba04-352">正则表达式模式可以解释为下表中所示内容。</span><span class="sxs-lookup"><span data-stu-id="bba04-352">The regular expression is interpreted as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-353">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-353">Element</span></span>|<span data-ttu-id="bba04-354">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-354">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bba04-355">\b</span><span class="sxs-lookup"><span data-stu-id="bba04-355">\b</span></span>|<span data-ttu-id="bba04-356">在单词边界处开始匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-356">Begin the match at a word boundary.</span></span>|  
|<span data-ttu-id="bba04-357">\w+</span><span class="sxs-lookup"><span data-stu-id="bba04-357">\w+</span></span>|<span data-ttu-id="bba04-358">匹配一个或多个单词字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-358">Match one or more word characters.</span></span>|  
|<span data-ttu-id="bba04-359">(e)?</span><span class="sxs-lookup"><span data-stu-id="bba04-359">(e)?</span></span>|<span data-ttu-id="bba04-360">匹配“e”零次或一次。</span><span class="sxs-lookup"><span data-stu-id="bba04-360">Match an "e" either zero or one time.</span></span>|  
|<span data-ttu-id="bba04-361">s</span><span class="sxs-lookup"><span data-stu-id="bba04-361">s</span></span>|<span data-ttu-id="bba04-362">匹配“s”。</span><span class="sxs-lookup"><span data-stu-id="bba04-362">Match an "s".</span></span>|  
|<span data-ttu-id="bba04-363">(\s&#124;$)</span><span class="sxs-lookup"><span data-stu-id="bba04-363">(\s&#124;$)</span></span>|<span data-ttu-id="bba04-364">匹配空白字符或输入字符串的末尾。</span><span class="sxs-lookup"><span data-stu-id="bba04-364">Match either a white-space character or the end of the input string.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#10](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/whitespace1.cs#10)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#10](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/whitespace1.vb#10)]  
  
<a name="NonWhitespaceCharacter"></a>

## <a name="non-whitespace-character-s"></a><span data-ttu-id="bba04-365">非空格字符：\S</span><span class="sxs-lookup"><span data-stu-id="bba04-365">Non-whitespace character: \S</span></span>  

 <span data-ttu-id="bba04-366">`\S` 匹配任何非空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-366">`\S` matches any non-white-space character.</span></span> <span data-ttu-id="bba04-367">它等效于 `[^\f\n\r\t\v\x85\p{Z}]` 正则表达式模式或与等效于 `\s` 的正则表达式模式（与空白字符匹配）相反。</span><span class="sxs-lookup"><span data-stu-id="bba04-367">It is equivalent to the `[^\f\n\r\t\v\x85\p{Z}]` regular expression pattern, or the opposite of the regular expression pattern that is equivalent to `\s`, which matches white-space characters.</span></span> <span data-ttu-id="bba04-368">有关详细信息，请参阅[空白字符：\s](#WhitespaceCharacter)。</span><span class="sxs-lookup"><span data-stu-id="bba04-368">For more information, see [White-Space Character: \s](#WhitespaceCharacter).</span></span>  
  
 <span data-ttu-id="bba04-369">如果指定了符合 ECMAScript 的行为，则 `\S` 等效于 `[^ \f\n\r\t\v]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-369">If ECMAScript-compliant behavior is specified, `\S` is equivalent to  `[^ \f\n\r\t\v]`.</span></span> <span data-ttu-id="bba04-370">有关 ECMAScript 正则表达式的信息，请参阅[正则表达式选项](regular-expression-options.md)中的“ECMAScript 匹配行为”部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-370">For information on ECMAScript regular expressions, see the "ECMAScript Matching Behavior" section in [Regular Expression Options](regular-expression-options.md).</span></span>  
  
 <span data-ttu-id="bba04-371">下面的示例阐释 `\S` 语言元素。</span><span class="sxs-lookup"><span data-stu-id="bba04-371">The following example illustrates the `\S` language element.</span></span> <span data-ttu-id="bba04-372">正则表达式模式 `\b(\S+)\s?` 匹配由空白字符分隔的字符串。</span><span class="sxs-lookup"><span data-stu-id="bba04-372">The regular expression pattern `\b(\S+)\s?` matches strings that are delimited by white-space characters.</span></span> <span data-ttu-id="bba04-373">匹配项的 <xref:System.Text.RegularExpressions.GroupCollection> 对象中的第二个元素包含匹配的字符串。</span><span class="sxs-lookup"><span data-stu-id="bba04-373">The second element in the match's <xref:System.Text.RegularExpressions.GroupCollection> object contains the matched string.</span></span> <span data-ttu-id="bba04-374">正则表达式可按下表中的方式解释。</span><span class="sxs-lookup"><span data-stu-id="bba04-374">The regular expression can be interpreted as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-375">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-375">Element</span></span>|<span data-ttu-id="bba04-376">描述</span><span class="sxs-lookup"><span data-stu-id="bba04-376">Description</span></span>|  
|-------------|-----------------|  
|`\b`|<span data-ttu-id="bba04-377">在单词边界处开始匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-377">Begin the match at a word boundary.</span></span>|  
|`(\S+)`|<span data-ttu-id="bba04-378">匹配一个或多个非空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-378">Match one or more non-white-space characters.</span></span> <span data-ttu-id="bba04-379">这是第一个捕获组。</span><span class="sxs-lookup"><span data-stu-id="bba04-379">This is the first capturing group.</span></span>|  
|`\s?`|<span data-ttu-id="bba04-380">匹配零个或一个空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-380">Match zero or one white-space character.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#11](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/nonwhitespace1.cs#11)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#11](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/nonwhitespace1.vb#11)]  
  
<a name="DigitCharacter"></a>

## <a name="decimal-digit-character-d"></a><span data-ttu-id="bba04-381">十进制数字字符：\d</span><span class="sxs-lookup"><span data-stu-id="bba04-381">Decimal digit character: \d</span></span>  

 <span data-ttu-id="bba04-382">`\d` 匹配任何十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-382">`\d` matches any decimal digit.</span></span> <span data-ttu-id="bba04-383">它等效于 `\p{Nd}` 正则表达式模式，该模式包含标准的十进制数字 0-9 以及众多其他字符集的十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-383">It is equivalent to the `\p{Nd}` regular expression pattern, which includes the standard decimal digits 0-9 as well as the decimal digits of a number of other character sets.</span></span>  
  
 <span data-ttu-id="bba04-384">如果指定了符合 ECMAScript 的行为，则 `\d` 等效于 `[0-9]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-384">If ECMAScript-compliant behavior is specified, `\d` is equivalent to  `[0-9]`.</span></span> <span data-ttu-id="bba04-385">有关 ECMAScript 正则表达式的信息，请参阅[正则表达式选项](regular-expression-options.md)中的“ECMAScript 匹配行为”部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-385">For information on ECMAScript regular expressions, see the "ECMAScript Matching Behavior" section in [Regular Expression Options](regular-expression-options.md).</span></span>  
  
 <span data-ttu-id="bba04-386">下面的示例阐释 `\d` 语言元素。</span><span class="sxs-lookup"><span data-stu-id="bba04-386">The following example illustrates the `\d` language element.</span></span> <span data-ttu-id="bba04-387">它测试输入字符串是否表示美国和加拿大的有效电话号码。</span><span class="sxs-lookup"><span data-stu-id="bba04-387">It tests whether an input string represents a valid telephone number in the United States and Canada.</span></span> <span data-ttu-id="bba04-388">正则表达式模式 `^(\(?\d{3}\)?[\s-])?\d{3}-\d{4}$` 的定义如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bba04-388">The regular expression pattern `^(\(?\d{3}\)?[\s-])?\d{3}-\d{4}$` is defined as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-389">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-389">Element</span></span>|<span data-ttu-id="bba04-390">描述</span><span class="sxs-lookup"><span data-stu-id="bba04-390">Description</span></span>|  
|-------------|-----------------|  
|`^`|<span data-ttu-id="bba04-391">从输入字符串的开头部分开始匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-391">Begin the match at the beginning of the input string.</span></span>|  
|`\(?`|<span data-ttu-id="bba04-392">匹配零个或一个“(”文本字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-392">Match zero or one literal "(" character.</span></span>|  
|`\d{3}`|<span data-ttu-id="bba04-393">匹配三个十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-393">Match three decimal digits.</span></span>|  
|`\)?`|<span data-ttu-id="bba04-394">匹配零个或一个“)”文本字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-394">Match zero or one literal ")" character.</span></span>|  
|`[\s-]`|<span data-ttu-id="bba04-395">匹配连字符或空白字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-395">Match a hyphen or a white-space character.</span></span>|  
|`(\(?\d{3}\)?[\s-])?`|<span data-ttu-id="bba04-396">匹配后跟三个十进制数字的可选左括号、可选右括号和空白字符或连字符零次或一次。</span><span class="sxs-lookup"><span data-stu-id="bba04-396">Match an optional opening parenthesis followed by three decimal digits, an optional closing parenthesis, and either a white-space character or a hyphen zero or one time.</span></span> <span data-ttu-id="bba04-397">这是第一个捕获组。</span><span class="sxs-lookup"><span data-stu-id="bba04-397">This is the first capturing group.</span></span>|  
|`\d{3}-\d{4}`|<span data-ttu-id="bba04-398">匹配后跟连字符和四个以上的十进制数字的三个十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-398">Match three decimal digits followed by a hyphen and four more decimal digits.</span></span>|  
|`$`|<span data-ttu-id="bba04-399">匹配输入字符串的末尾部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-399">Match the end of the input string.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#12](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/digit1.cs#12)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#12](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/digit1.vb#12)]  
  
<a name="NonDigitCharacter"></a>

## <a name="non-digit-character-d"></a><span data-ttu-id="bba04-400">非数字字符：\D</span><span class="sxs-lookup"><span data-stu-id="bba04-400">Non-digit character: \D</span></span>  

 <span data-ttu-id="bba04-401">`\D` 匹配任何非数字字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-401">`\D` matches any non-digit character.</span></span> <span data-ttu-id="bba04-402">它等效于 `\P{Nd}` 正则表达式模式。</span><span class="sxs-lookup"><span data-stu-id="bba04-402">It is equivalent to the `\P{Nd}` regular expression pattern.</span></span>  
  
 <span data-ttu-id="bba04-403">如果指定了符合 ECMAScript 的行为，则 `\D` 等效于 `[^0-9]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-403">If ECMAScript-compliant behavior is specified, `\D` is equivalent to  `[^0-9]`.</span></span> <span data-ttu-id="bba04-404">有关 ECMAScript 正则表达式的信息，请参阅[正则表达式选项](regular-expression-options.md)中的“ECMAScript 匹配行为”部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-404">For information on ECMAScript regular expressions, see the "ECMAScript Matching Behavior" section in [Regular Expression Options](regular-expression-options.md).</span></span>  
  
 <span data-ttu-id="bba04-405">下面的示例阐释了 \D 语言元素。</span><span class="sxs-lookup"><span data-stu-id="bba04-405">The following example illustrates the \D language element.</span></span> <span data-ttu-id="bba04-406">它测试部件号等字符串是否包含适当的十进制和非十进制数字字符的组合。</span><span class="sxs-lookup"><span data-stu-id="bba04-406">It tests whether a string such as a part number consists of the appropriate combination of decimal and non-decimal characters.</span></span> <span data-ttu-id="bba04-407">正则表达式模式 `^\D\d{1,5}\D*$` 的定义如下表所示。</span><span class="sxs-lookup"><span data-stu-id="bba04-407">The regular expression pattern `^\D\d{1,5}\D*$` is defined as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-408">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-408">Element</span></span>|<span data-ttu-id="bba04-409">描述</span><span class="sxs-lookup"><span data-stu-id="bba04-409">Description</span></span>|  
|-------------|-----------------|  
|`^`|<span data-ttu-id="bba04-410">从输入字符串的开头部分开始匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-410">Begin the match at the beginning of the input string.</span></span>|  
|`\D`|<span data-ttu-id="bba04-411">匹配非数字字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-411">Match a non-digit character.</span></span>|  
|`\d{1,5}`|<span data-ttu-id="bba04-412">匹配一到五个十进制数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-412">Match from one to five decimal digits.</span></span>|  
|`\D*`|<span data-ttu-id="bba04-413">匹配零个、一个或多个非十进制字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-413">Match zero, one, or more non-decimal characters.</span></span>|  
|`$`|<span data-ttu-id="bba04-414">匹配输入字符串的末尾部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-414">Match the end of the input string.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#13](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/nondigit1.cs#13)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#13](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/nondigit1.vb#13)]  
  
<a name="SupportedUnicodeGeneralCategories"></a>

## <a name="supported-unicode-general-categories"></a><span data-ttu-id="bba04-415">支持的 Unicode 常规类别</span><span class="sxs-lookup"><span data-stu-id="bba04-415">Supported Unicode general categories</span></span>  

 <span data-ttu-id="bba04-416">Unicode 定义下表列出的常规类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-416">Unicode defines the general categories listed in the following table.</span></span> <span data-ttu-id="bba04-417">有关详细信息，请参阅 [Unicode 字符数据库](https://www.unicode.org/reports/tr44/)中的“UCD 文件格式”和“常规类别值”子主题。</span><span class="sxs-lookup"><span data-stu-id="bba04-417">For more information, see the "UCD File Format" and "General Category Values" subtopics at the [Unicode Character Database](https://www.unicode.org/reports/tr44/).</span></span>  
  
|<span data-ttu-id="bba04-418">Category</span><span class="sxs-lookup"><span data-stu-id="bba04-418">Category</span></span>|<span data-ttu-id="bba04-419">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-419">Description</span></span>|  
|--------------|-----------------|  
|`Lu`|<span data-ttu-id="bba04-420">字母，大写</span><span class="sxs-lookup"><span data-stu-id="bba04-420">Letter, Uppercase</span></span>|  
|`Ll`|<span data-ttu-id="bba04-421">字母，小写</span><span class="sxs-lookup"><span data-stu-id="bba04-421">Letter, Lowercase</span></span>|  
|`Lt`|<span data-ttu-id="bba04-422">字母，首字母大写</span><span class="sxs-lookup"><span data-stu-id="bba04-422">Letter, Titlecase</span></span>|  
|`Lm`|<span data-ttu-id="bba04-423">字母，修饰符</span><span class="sxs-lookup"><span data-stu-id="bba04-423">Letter, Modifier</span></span>|  
|`Lo`|<span data-ttu-id="bba04-424">字母，其他</span><span class="sxs-lookup"><span data-stu-id="bba04-424">Letter, Other</span></span>|  
|`L`|<span data-ttu-id="bba04-425">所有字母字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-425">All letter characters.</span></span> <span data-ttu-id="bba04-426">这包括 `Lu`、`Ll`、`Lt`、`Lm` 和 `Lo` 字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-426">This includes the `Lu`, `Ll`, `Lt`, `Lm`, and `Lo` characters.</span></span>|  
|`Mn`|<span data-ttu-id="bba04-427">标记，非间距</span><span class="sxs-lookup"><span data-stu-id="bba04-427">Mark, Nonspacing</span></span>|  
|`Mc`|<span data-ttu-id="bba04-428">标记，间距组合</span><span class="sxs-lookup"><span data-stu-id="bba04-428">Mark, Spacing Combining</span></span>|  
|`Me`|<span data-ttu-id="bba04-429">标记，封闭</span><span class="sxs-lookup"><span data-stu-id="bba04-429">Mark, Enclosing</span></span>|  
|`M`|<span data-ttu-id="bba04-430">所有音调符号标记。</span><span class="sxs-lookup"><span data-stu-id="bba04-430">All diacritic marks.</span></span> <span data-ttu-id="bba04-431">这包括 `Mn`、`Mc` 和 `Me` 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-431">This includes the `Mn`, `Mc`, and `Me` categories.</span></span>|  
|`Nd`|<span data-ttu-id="bba04-432">数字，十进制数</span><span class="sxs-lookup"><span data-stu-id="bba04-432">Number, Decimal Digit</span></span>|  
|`Nl`|<span data-ttu-id="bba04-433">数字，字母</span><span class="sxs-lookup"><span data-stu-id="bba04-433">Number, Letter</span></span>|  
|`No`|<span data-ttu-id="bba04-434">数字，其他</span><span class="sxs-lookup"><span data-stu-id="bba04-434">Number, Other</span></span>|  
|`N`|<span data-ttu-id="bba04-435">所有数字。</span><span class="sxs-lookup"><span data-stu-id="bba04-435">All numbers.</span></span> <span data-ttu-id="bba04-436">这包括 `Nd`、`Nl` 和 `No` 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-436">This includes the `Nd`, `Nl`, and `No` categories.</span></span>|  
|`Pc`|<span data-ttu-id="bba04-437">标点，连接符</span><span class="sxs-lookup"><span data-stu-id="bba04-437">Punctuation, Connector</span></span>|  
|`Pd`|<span data-ttu-id="bba04-438">标点，短划线</span><span class="sxs-lookup"><span data-stu-id="bba04-438">Punctuation, Dash</span></span>|  
|`Ps`|<span data-ttu-id="bba04-439">标点，开始</span><span class="sxs-lookup"><span data-stu-id="bba04-439">Punctuation, Open</span></span>|  
|`Pe`|<span data-ttu-id="bba04-440">标点，结束</span><span class="sxs-lookup"><span data-stu-id="bba04-440">Punctuation, Close</span></span>|  
|`Pi`|<span data-ttu-id="bba04-441">标点，前引号（根据具体使用情况，作用可能像 Ps 或 Pe）</span><span class="sxs-lookup"><span data-stu-id="bba04-441">Punctuation, Initial quote (may behave like Ps or Pe depending on usage)</span></span>|  
|`Pf`|<span data-ttu-id="bba04-442">标点，后引号（根据具体使用情况，作用可能像 Ps 或 Pe）</span><span class="sxs-lookup"><span data-stu-id="bba04-442">Punctuation, Final quote (may behave like Ps or Pe depending on usage)</span></span>|  
|`Po`|<span data-ttu-id="bba04-443">标点，其他</span><span class="sxs-lookup"><span data-stu-id="bba04-443">Punctuation, Other</span></span>|  
|`P`|<span data-ttu-id="bba04-444">所有标点字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-444">All punctuation characters.</span></span> <span data-ttu-id="bba04-445">这包括 `Pc`、`Pd`、`Ps`, `Pe`、`Pi`、`Pf` 和 `Po` 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-445">This includes the `Pc`, `Pd`, `Ps`, `Pe`, `Pi`, `Pf`, and `Po` categories.</span></span>|  
|`Sm`|<span data-ttu-id="bba04-446">符号，数学</span><span class="sxs-lookup"><span data-stu-id="bba04-446">Symbol, Math</span></span>|  
|`Sc`|<span data-ttu-id="bba04-447">符号，货币</span><span class="sxs-lookup"><span data-stu-id="bba04-447">Symbol, Currency</span></span>|  
|`Sk`|<span data-ttu-id="bba04-448">符号，修饰符</span><span class="sxs-lookup"><span data-stu-id="bba04-448">Symbol, Modifier</span></span>|  
|`So`|<span data-ttu-id="bba04-449">符号，其他</span><span class="sxs-lookup"><span data-stu-id="bba04-449">Symbol, Other</span></span>|  
|`S`|<span data-ttu-id="bba04-450">所有符号。</span><span class="sxs-lookup"><span data-stu-id="bba04-450">All symbols.</span></span> <span data-ttu-id="bba04-451">这包括 `Sm`、`Sc`、`Sk` 和 `So` 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-451">This includes the `Sm`, `Sc`, `Sk`, and `So` categories.</span></span>|  
|`Zs`|<span data-ttu-id="bba04-452">分隔符，空白</span><span class="sxs-lookup"><span data-stu-id="bba04-452">Separator, Space</span></span>|  
|`Zl`|<span data-ttu-id="bba04-453">分隔符，行</span><span class="sxs-lookup"><span data-stu-id="bba04-453">Separator, Line</span></span>|  
|`Zp`|<span data-ttu-id="bba04-454">分隔符，段落</span><span class="sxs-lookup"><span data-stu-id="bba04-454">Separator, Paragraph</span></span>|  
|`Z`|<span data-ttu-id="bba04-455">所有分隔符字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-455">All separator characters.</span></span> <span data-ttu-id="bba04-456">这包括 `Zs`、`Zl` 和 `Zp` 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-456">This includes the `Zs`, `Zl`, and `Zp` categories.</span></span>|  
|`Cc`|<span data-ttu-id="bba04-457">其他，控制</span><span class="sxs-lookup"><span data-stu-id="bba04-457">Other, Control</span></span>|  
|`Cf`|<span data-ttu-id="bba04-458">其他，格式</span><span class="sxs-lookup"><span data-stu-id="bba04-458">Other, Format</span></span>|  
|`Cs`|<span data-ttu-id="bba04-459">其他，代理项</span><span class="sxs-lookup"><span data-stu-id="bba04-459">Other, Surrogate</span></span>|  
|`Co`|<span data-ttu-id="bba04-460">其他，私用</span><span class="sxs-lookup"><span data-stu-id="bba04-460">Other, Private Use</span></span>|  
|`Cn`|<span data-ttu-id="bba04-461">其他，未赋值（任何字符都不具有此属性）</span><span class="sxs-lookup"><span data-stu-id="bba04-461">Other, Not Assigned (no characters have this property)</span></span>|  
|`C`|<span data-ttu-id="bba04-462">所有控制字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-462">All control characters.</span></span> <span data-ttu-id="bba04-463">这包括 `Cc`、`Cf`、`Cs`、`Co` 和 `Cn` 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-463">This includes the `Cc`, `Cf`, `Cs`, `Co`, and `Cn` categories.</span></span>|  
  
 <span data-ttu-id="bba04-464">可以通过将任何特定字符传递到 <xref:System.Char.GetUnicodeCategory%2A> 方法来确定该字符的 Unicode 类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-464">You can determine the Unicode category of any particular character by passing that character to the <xref:System.Char.GetUnicodeCategory%2A> method.</span></span> <span data-ttu-id="bba04-465">下面的示例使用 <xref:System.Char.GetUnicodeCategory%2A> 方法来确定包含所选拉丁字符的数组中的每个元素的类别。</span><span class="sxs-lookup"><span data-stu-id="bba04-465">The following example uses the <xref:System.Char.GetUnicodeCategory%2A> method to determine the category of each element in an array that contains selected Latin characters.</span></span>  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#14](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/getunicodecategory1.cs#14)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#14](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/getunicodecategory1.vb#14)]  
  
<a name="SupportedNamedBlocks"></a>

## <a name="supported-named-blocks"></a><span data-ttu-id="bba04-466">支持的命名块</span><span class="sxs-lookup"><span data-stu-id="bba04-466">Supported named blocks</span></span>

<span data-ttu-id="bba04-467">.NET 提供下表中所列的命名块。</span><span class="sxs-lookup"><span data-stu-id="bba04-467">.NET provides the named blocks listed in the following table.</span></span> <span data-ttu-id="bba04-468">该组支持的命名块基于 Unicode 4.0 和 Perl 5.6。</span><span class="sxs-lookup"><span data-stu-id="bba04-468">The set of supported named blocks is based on Unicode 4.0 and Perl 5.6.</span></span> <span data-ttu-id="bba04-469">有关正则表达式使用命名块，请参阅 [Unicode 类别或 Unicode 块： \\p{}](#unicode-category-or-unicode-block-p) 部分。</span><span class="sxs-lookup"><span data-stu-id="bba04-469">For a regular expression that uses named blocks, see the [Unicode category or Unicode block: \\p{}](#unicode-category-or-unicode-block-p) section.</span></span>  
  
|<span data-ttu-id="bba04-470">码位范围</span><span class="sxs-lookup"><span data-stu-id="bba04-470">Code point range</span></span>|<span data-ttu-id="bba04-471">块名称</span><span class="sxs-lookup"><span data-stu-id="bba04-471">Block name</span></span>|  
|----------------------|----------------|  
|<span data-ttu-id="bba04-472">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="bba04-472">0000 - 007F</span></span>|`IsBasicLatin`|  
|<span data-ttu-id="bba04-473">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="bba04-473">0080 - 00FF</span></span>|`IsLatin-1Supplement`|  
|<span data-ttu-id="bba04-474">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="bba04-474">0100 - 017F</span></span>|`IsLatinExtended-A`|  
|<span data-ttu-id="bba04-475">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="bba04-475">0180 - 024F</span></span>|`IsLatinExtended-B`|  
|<span data-ttu-id="bba04-476">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="bba04-476">0250 - 02AF</span></span>|`IsIPAExtensions`|  
|<span data-ttu-id="bba04-477">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="bba04-477">02B0 - 02FF</span></span>|`IsSpacingModifierLetters`|  
|<span data-ttu-id="bba04-478">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="bba04-478">0300 - 036F</span></span>|`IsCombiningDiacriticalMarks`|  
|<span data-ttu-id="bba04-479">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="bba04-479">0370 - 03FF</span></span>|`IsGreek`<br /><br /> <span data-ttu-id="bba04-480">或</span><span class="sxs-lookup"><span data-stu-id="bba04-480">-or-</span></span><br /><br /> `IsGreekandCoptic`|  
|<span data-ttu-id="bba04-481">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="bba04-481">0400 - 04FF</span></span>|`IsCyrillic`|  
|<span data-ttu-id="bba04-482">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="bba04-482">0500 - 052F</span></span>|`IsCyrillicSupplement`|  
|<span data-ttu-id="bba04-483">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="bba04-483">0530 - 058F</span></span>|`IsArmenian`|  
|<span data-ttu-id="bba04-484">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="bba04-484">0590 - 05FF</span></span>|`IsHebrew`|  
|<span data-ttu-id="bba04-485">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="bba04-485">0600 - 06FF</span></span>|`IsArabic`|  
|<span data-ttu-id="bba04-486">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="bba04-486">0700 - 074F</span></span>|`IsSyriac`|  
|<span data-ttu-id="bba04-487">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="bba04-487">0780 - 07BF</span></span>|`IsThaana`|  
|<span data-ttu-id="bba04-488">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="bba04-488">0900 - 097F</span></span>|`IsDevanagari`|  
|<span data-ttu-id="bba04-489">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="bba04-489">0980 - 09FF</span></span>|`IsBengali`|  
|<span data-ttu-id="bba04-490">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="bba04-490">0A00 - 0A7F</span></span>|`IsGurmukhi`|  
|<span data-ttu-id="bba04-491">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="bba04-491">0A80 - 0AFF</span></span>|`IsGujarati`|  
|<span data-ttu-id="bba04-492">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="bba04-492">0B00 - 0B7F</span></span>|`IsOriya`|  
|<span data-ttu-id="bba04-493">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="bba04-493">0B80 - 0BFF</span></span>|`IsTamil`|  
|<span data-ttu-id="bba04-494">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="bba04-494">0C00 - 0C7F</span></span>|`IsTelugu`|  
|<span data-ttu-id="bba04-495">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="bba04-495">0C80 - 0CFF</span></span>|`IsKannada`|  
|<span data-ttu-id="bba04-496">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="bba04-496">0D00 - 0D7F</span></span>|`IsMalayalam`|  
|<span data-ttu-id="bba04-497">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="bba04-497">0D80 - 0DFF</span></span>|`IsSinhala`|  
|<span data-ttu-id="bba04-498">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="bba04-498">0E00 - 0E7F</span></span>|`IsThai`|  
|<span data-ttu-id="bba04-499">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="bba04-499">0E80 - 0EFF</span></span>|`IsLao`|  
|<span data-ttu-id="bba04-500">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="bba04-500">0F00 - 0FFF</span></span>|`IsTibetan`|  
|<span data-ttu-id="bba04-501">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="bba04-501">1000 - 109F</span></span>|`IsMyanmar`|  
|<span data-ttu-id="bba04-502">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="bba04-502">10A0 - 10FF</span></span>|`IsGeorgian`|  
|<span data-ttu-id="bba04-503">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="bba04-503">1100 - 11FF</span></span>|`IsHangulJamo`|  
|<span data-ttu-id="bba04-504">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="bba04-504">1200 - 137F</span></span>|`IsEthiopic`|  
|<span data-ttu-id="bba04-505">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="bba04-505">13A0 - 13FF</span></span>|`IsCherokee`|  
|<span data-ttu-id="bba04-506">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="bba04-506">1400 - 167F</span></span>|`IsUnifiedCanadianAboriginalSyllabics`|  
|<span data-ttu-id="bba04-507">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="bba04-507">1680 - 169F</span></span>|`IsOgham`|  
|<span data-ttu-id="bba04-508">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="bba04-508">16A0 - 16FF</span></span>|`IsRunic`|  
|<span data-ttu-id="bba04-509">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="bba04-509">1700 - 171F</span></span>|`IsTagalog`|  
|<span data-ttu-id="bba04-510">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="bba04-510">1720 - 173F</span></span>|`IsHanunoo`|  
|<span data-ttu-id="bba04-511">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="bba04-511">1740 - 175F</span></span>|`IsBuhid`|  
|<span data-ttu-id="bba04-512">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="bba04-512">1760 - 177F</span></span>|`IsTagbanwa`|  
|<span data-ttu-id="bba04-513">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="bba04-513">1780 - 17FF</span></span>|`IsKhmer`|  
|<span data-ttu-id="bba04-514">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="bba04-514">1800 - 18AF</span></span>|`IsMongolian`|  
|<span data-ttu-id="bba04-515">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="bba04-515">1900 - 194F</span></span>|`IsLimbu`|  
|<span data-ttu-id="bba04-516">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="bba04-516">1950 - 197F</span></span>|`IsTaiLe`|  
|<span data-ttu-id="bba04-517">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="bba04-517">19E0 - 19FF</span></span>|`IsKhmerSymbols`|  
|<span data-ttu-id="bba04-518">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="bba04-518">1D00 - 1D7F</span></span>|`IsPhoneticExtensions`|  
|<span data-ttu-id="bba04-519">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="bba04-519">1E00 - 1EFF</span></span>|`IsLatinExtendedAdditional`|  
|<span data-ttu-id="bba04-520">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="bba04-520">1F00 - 1FFF</span></span>|`IsGreekExtended`|  
|<span data-ttu-id="bba04-521">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="bba04-521">2000 - 206F</span></span>|`IsGeneralPunctuation`|  
|<span data-ttu-id="bba04-522">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="bba04-522">2070 - 209F</span></span>|`IsSuperscriptsandSubscripts`|  
|<span data-ttu-id="bba04-523">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="bba04-523">20A0 - 20CF</span></span>|`IsCurrencySymbols`|  
|<span data-ttu-id="bba04-524">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="bba04-524">20D0 - 20FF</span></span>|`IsCombiningDiacriticalMarksforSymbols`<br /><br /> <span data-ttu-id="bba04-525">或</span><span class="sxs-lookup"><span data-stu-id="bba04-525">-or-</span></span><br /><br /> `IsCombiningMarksforSymbols`|  
|<span data-ttu-id="bba04-526">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="bba04-526">2100 - 214F</span></span>|`IsLetterlikeSymbols`|  
|<span data-ttu-id="bba04-527">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="bba04-527">2150 - 218F</span></span>|`IsNumberForms`|  
|<span data-ttu-id="bba04-528">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="bba04-528">2190 - 21FF</span></span>|`IsArrows`|  
|<span data-ttu-id="bba04-529">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="bba04-529">2200 - 22FF</span></span>|`IsMathematicalOperators`|  
|<span data-ttu-id="bba04-530">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="bba04-530">2300 - 23FF</span></span>|`IsMiscellaneousTechnical`|  
|<span data-ttu-id="bba04-531">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="bba04-531">2400 - 243F</span></span>|`IsControlPictures`|  
|<span data-ttu-id="bba04-532">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="bba04-532">2440 - 245F</span></span>|`IsOpticalCharacterRecognition`|  
|<span data-ttu-id="bba04-533">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="bba04-533">2460 - 24FF</span></span>|`IsEnclosedAlphanumerics`|  
|<span data-ttu-id="bba04-534">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="bba04-534">2500 - 257F</span></span>|`IsBoxDrawing`|  
|<span data-ttu-id="bba04-535">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="bba04-535">2580 - 259F</span></span>|`IsBlockElements`|  
|<span data-ttu-id="bba04-536">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="bba04-536">25A0 - 25FF</span></span>|`IsGeometricShapes`|  
|<span data-ttu-id="bba04-537">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="bba04-537">2600 - 26FF</span></span>|`IsMiscellaneousSymbols`|  
|<span data-ttu-id="bba04-538">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="bba04-538">2700 - 27BF</span></span>|`IsDingbats`|  
|<span data-ttu-id="bba04-539">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="bba04-539">27C0 - 27EF</span></span>|`IsMiscellaneousMathematicalSymbols-A`|  
|<span data-ttu-id="bba04-540">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="bba04-540">27F0 - 27FF</span></span>|`IsSupplementalArrows-A`|  
|<span data-ttu-id="bba04-541">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="bba04-541">2800 - 28FF</span></span>|`IsBraillePatterns`|  
|<span data-ttu-id="bba04-542">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="bba04-542">2900 - 297F</span></span>|`IsSupplementalArrows-B`|  
|<span data-ttu-id="bba04-543">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="bba04-543">2980 - 29FF</span></span>|`IsMiscellaneousMathematicalSymbols-B`|  
|<span data-ttu-id="bba04-544">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="bba04-544">2A00 - 2AFF</span></span>|`IsSupplementalMathematicalOperators`|  
|<span data-ttu-id="bba04-545">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="bba04-545">2B00 - 2BFF</span></span>|`IsMiscellaneousSymbolsandArrows`|  
|<span data-ttu-id="bba04-546">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="bba04-546">2E80 - 2EFF</span></span>|`IsCJKRadicalsSupplement`|  
|<span data-ttu-id="bba04-547">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="bba04-547">2F00 - 2FDF</span></span>|`IsKangxiRadicals`|  
|<span data-ttu-id="bba04-548">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="bba04-548">2FF0 - 2FFF</span></span>|`IsIdeographicDescriptionCharacters`|  
|<span data-ttu-id="bba04-549">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="bba04-549">3000 - 303F</span></span>|`IsCJKSymbolsandPunctuation`|  
|<span data-ttu-id="bba04-550">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="bba04-550">3040 - 309F</span></span>|`IsHiragana`|  
|<span data-ttu-id="bba04-551">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="bba04-551">30A0 - 30FF</span></span>|`IsKatakana`|  
|<span data-ttu-id="bba04-552">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="bba04-552">3100 - 312F</span></span>|`IsBopomofo`|  
|<span data-ttu-id="bba04-553">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="bba04-553">3130 - 318F</span></span>|`IsHangulCompatibilityJamo`|  
|<span data-ttu-id="bba04-554">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="bba04-554">3190 - 319F</span></span>|`IsKanbun`|  
|<span data-ttu-id="bba04-555">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="bba04-555">31A0 - 31BF</span></span>|`IsBopomofoExtended`|  
|<span data-ttu-id="bba04-556">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="bba04-556">31F0 - 31FF</span></span>|`IsKatakanaPhoneticExtensions`|  
|<span data-ttu-id="bba04-557">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="bba04-557">3200 - 32FF</span></span>|`IsEnclosedCJKLettersandMonths`|  
|<span data-ttu-id="bba04-558">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="bba04-558">3300 - 33FF</span></span>|`IsCJKCompatibility`|  
|<span data-ttu-id="bba04-559">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="bba04-559">3400 - 4DBF</span></span>|`IsCJKUnifiedIdeographsExtensionA`|  
|<span data-ttu-id="bba04-560">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="bba04-560">4DC0 - 4DFF</span></span>|`IsYijingHexagramSymbols`|  
|<span data-ttu-id="bba04-561">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="bba04-561">4E00 - 9FFF</span></span>|`IsCJKUnifiedIdeographs`|  
|<span data-ttu-id="bba04-562">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="bba04-562">A000 - A48F</span></span>|`IsYiSyllables`|  
|<span data-ttu-id="bba04-563">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="bba04-563">A490 - A4CF</span></span>|`IsYiRadicals`|  
|<span data-ttu-id="bba04-564">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="bba04-564">AC00 - D7AF</span></span>|`IsHangulSyllables`|  
|<span data-ttu-id="bba04-565">D800 - DB7F</span><span class="sxs-lookup"><span data-stu-id="bba04-565">D800 - DB7F</span></span>|`IsHighSurrogates`|  
|<span data-ttu-id="bba04-566">DB80 - DBFF</span><span class="sxs-lookup"><span data-stu-id="bba04-566">DB80 - DBFF</span></span>|`IsHighPrivateUseSurrogates`|  
|<span data-ttu-id="bba04-567">DC00 - DFFF</span><span class="sxs-lookup"><span data-stu-id="bba04-567">DC00 - DFFF</span></span>|`IsLowSurrogates`|  
|<span data-ttu-id="bba04-568">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="bba04-568">E000 - F8FF</span></span>|<span data-ttu-id="bba04-569">`IsPrivateUse` 或 `IsPrivateUseArea`</span><span class="sxs-lookup"><span data-stu-id="bba04-569">`IsPrivateUse` or `IsPrivateUseArea`</span></span>|  
|<span data-ttu-id="bba04-570">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="bba04-570">F900 - FAFF</span></span>|`IsCJKCompatibilityIdeographs`|  
|<span data-ttu-id="bba04-571">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="bba04-571">FB00 - FB4F</span></span>|`IsAlphabeticPresentationForms`|  
|<span data-ttu-id="bba04-572">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="bba04-572">FB50 - FDFF</span></span>|`IsArabicPresentationForms-A`|  
|<span data-ttu-id="bba04-573">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="bba04-573">FE00 - FE0F</span></span>|`IsVariationSelectors`|  
|<span data-ttu-id="bba04-574">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="bba04-574">FE20 - FE2F</span></span>|`IsCombiningHalfMarks`|  
|<span data-ttu-id="bba04-575">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="bba04-575">FE30 - FE4F</span></span>|`IsCJKCompatibilityForms`|  
|<span data-ttu-id="bba04-576">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="bba04-576">FE50 - FE6F</span></span>|`IsSmallFormVariants`|  
|<span data-ttu-id="bba04-577">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="bba04-577">FE70 - FEFF</span></span>|`IsArabicPresentationForms-B`|  
|<span data-ttu-id="bba04-578">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="bba04-578">FF00 - FFEF</span></span>|`IsHalfwidthandFullwidthForms`|  
|<span data-ttu-id="bba04-579">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="bba04-579">FFF0 - FFFF</span></span>|`IsSpecials`|  
  
<a name="CharacterClassSubtraction"></a>

## <a name="character-class-subtraction-base_group---excluded_group"></a><span data-ttu-id="bba04-580">字符类减法：[base_group - [excluded_group]]</span><span class="sxs-lookup"><span data-stu-id="bba04-580">Character class subtraction: [base_group - [excluded_group]]</span></span>  

 <span data-ttu-id="bba04-581">一个字符类定义一组字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-581">A character class defines a set of characters.</span></span> <span data-ttu-id="bba04-582">字符类减法将产生一组字符，该组字符是从一个字符类中排除另一个字符类中的字符的结果。</span><span class="sxs-lookup"><span data-stu-id="bba04-582">Character class subtraction yields a set of characters that is the result of excluding the characters in one character class from another character class.</span></span>  
  
 <span data-ttu-id="bba04-583">字符类减法表达式具有以下形式：</span><span class="sxs-lookup"><span data-stu-id="bba04-583">A character class subtraction expression has the following form:</span></span>  
  
 <span data-ttu-id="bba04-584">`[` *base_group* `-[` *excluded_group* `]]`</span><span class="sxs-lookup"><span data-stu-id="bba04-584">`[` *base_group* `-[` *excluded_group* `]]`</span></span>  
  
 <span data-ttu-id="bba04-585">方括号 (`[]`) 和连字符 (`-`) 是强制的。</span><span class="sxs-lookup"><span data-stu-id="bba04-585">The square brackets (`[]`) and hyphen (`-`) are mandatory.</span></span> <span data-ttu-id="bba04-586">base_group 是[正字符组](#PositiveGroup)或[负字符组](#NegativeGroup)。</span><span class="sxs-lookup"><span data-stu-id="bba04-586">The *base_group* is a [positive character group](#PositiveGroup) or a [negative character group](#NegativeGroup).</span></span> <span data-ttu-id="bba04-587">*excluded_group* 部分是另一个正字符组或负字符组，或者是另一个字符类减法表达式（即，可以嵌套字符类减法表达式）。</span><span class="sxs-lookup"><span data-stu-id="bba04-587">The *excluded_group* component is another positive or negative character group, or another character class subtraction expression (that is, you can nest character class subtraction expressions).</span></span>  
  
 <span data-ttu-id="bba04-588">例如，假设你有一个由从“a”至“z”范围内的字符组成的基本组。</span><span class="sxs-lookup"><span data-stu-id="bba04-588">For example, suppose you have a base group that consists of the character range from "a" through "z".</span></span> <span data-ttu-id="bba04-589">若要定义由除字符“m”之外的基本组组成的字符集，请使用 `[a-z-[m]]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-589">To define the set of characters that consists of the base group except for the character "m", use `[a-z-[m]]`.</span></span> <span data-ttu-id="bba04-590">若要定义由除字符集“d”、“j”和“p”之外的基本组组成的字符集，请使用 `[a-z-[djp]]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-590">To define the set of characters that consists of the base group except for the set of characters "d", "j", and "p", use `[a-z-[djp]]`.</span></span> <span data-ttu-id="bba04-591">若要定义由除从“m”至“p”字符范围之外的基本组组成的字符集，请使用 `[a-z-[m-p]]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-591">To define the set of characters that consists of the base group except for the character range from "m" through "p", use `[a-z-[m-p]]`.</span></span>  
  
 <span data-ttu-id="bba04-592">可考虑使用嵌套字符类减法表达式 `[a-z-[d-w-[m-o]]]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-592">Consider the nested character class subtraction expression, `[a-z-[d-w-[m-o]]]`.</span></span> <span data-ttu-id="bba04-593">该表达式由最里面的字符范围向外计算。</span><span class="sxs-lookup"><span data-stu-id="bba04-593">The expression is evaluated from the innermost character range outward.</span></span> <span data-ttu-id="bba04-594">首先，在从“d”至“w”的字符范围中减去从“m”至“o”的字符范围，这将产生从“d”至“l”和从“p”至“w”的字符集。</span><span class="sxs-lookup"><span data-stu-id="bba04-594">First, the character range from "m" through "o" is subtracted from the character range "d" through "w", which yields the set of characters from "d" through "l" and "p" through "w".</span></span> <span data-ttu-id="bba04-595">然后，在从“a”至“z”的字符范围中减去该集合，这将产生字符集 `[abcmnoxyz]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-595">That set is then subtracted from the character range from "a" through "z", which yields the set of characters `[abcmnoxyz]`.</span></span>  
  
 <span data-ttu-id="bba04-596">可以将任何字符类用于字符类减法。</span><span class="sxs-lookup"><span data-stu-id="bba04-596">You can use any character class with character class subtraction.</span></span> <span data-ttu-id="bba04-597">若要定义字符集，且该字符集包括除空白字符 (`\s`)、标点通用类别中的字符 (`\p{P}`)、`IsGreek` 命名块中的字符 (`\p{IsGreek}`) 以及 Unicode NEXT LINE 控制字符 (\x85) 之外的所有从 \u0000 至 \uFFFF 的 Unicode 字符，请使用 `[\u0000-\uFFFF-[\s\p{P}\p{IsGreek}\x85]]`。</span><span class="sxs-lookup"><span data-stu-id="bba04-597">To define the set of characters that consists of all Unicode characters from \u0000 through \uFFFF except white-space characters (`\s`), the characters in the punctuation general category (`\p{P}`), the characters in the `IsGreek` named block (`\p{IsGreek}`), and the Unicode NEXT LINE control character (\x85), use `[\u0000-\uFFFF-[\s\p{P}\p{IsGreek}\x85]]`.</span></span>  
  
 <span data-ttu-id="bba04-598">为字符类减法表达式选择将会产生有用结果的字符类。</span><span class="sxs-lookup"><span data-stu-id="bba04-598">Choose character classes for a character class subtraction expression that will yield useful results.</span></span> <span data-ttu-id="bba04-599">避免使用产生空字符集的表达式，这将无法匹配任何内容，同时避免使用等效于初始基本组的表达式。</span><span class="sxs-lookup"><span data-stu-id="bba04-599">Avoid an expression that yields an empty set of characters, which cannot match anything, or an expression that is equivalent to the original base group.</span></span> <span data-ttu-id="bba04-600">例如，表达式 `[\p{IsBasicLatin}-[\x00-\x7F]]` 从 `IsBasicLatin` 常规类别中减去 `IsBasicLatin` 字符范围内的所有字符，其结果为空集合。</span><span class="sxs-lookup"><span data-stu-id="bba04-600">For example, the empty set is the result of the expression `[\p{IsBasicLatin}-[\x00-\x7F]]`, which subtracts all characters in the `IsBasicLatin` character range from the `IsBasicLatin` general category.</span></span> <span data-ttu-id="bba04-601">类似地，表达式 `[a-z-[0-9]]` 的结果为初始基本组。</span><span class="sxs-lookup"><span data-stu-id="bba04-601">Similarly, the original base group is the result of the expression `[a-z-[0-9]]`.</span></span>  <span data-ttu-id="bba04-602">这是因为，基本组（它是从“a”至“z”的字母组成的字符范围）不包含排除组（它是从“0”至“9”的十进制数组成的字符范围）中的任何字符。</span><span class="sxs-lookup"><span data-stu-id="bba04-602">This is because the base group, which is the character range of letters from "a" through "z", does not contain any characters in the excluded group, which is the character range of decimal digits from "0" through "9".</span></span>  
  
 <span data-ttu-id="bba04-603">下面的示例定义正则表达式 `^[0-9-[2468]]+$`，该表达式匹配输入字符串中的零和奇数。</span><span class="sxs-lookup"><span data-stu-id="bba04-603">The following example defines a regular expression, `^[0-9-[2468]]+$`, that matches zero and odd digits in an input string.</span></span>  <span data-ttu-id="bba04-604">正则表达式模式可以解释为下表中所示内容。</span><span class="sxs-lookup"><span data-stu-id="bba04-604">The regular expression is interpreted as shown in the following table.</span></span>  
  
|<span data-ttu-id="bba04-605">元素</span><span class="sxs-lookup"><span data-stu-id="bba04-605">Element</span></span>|<span data-ttu-id="bba04-606">说明</span><span class="sxs-lookup"><span data-stu-id="bba04-606">Description</span></span>|  
|-------------|-----------------|  
|^|<span data-ttu-id="bba04-607">从输入字符串的开头处开始进行匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-607">Begin the match at the start of the input string.</span></span>|  
|`[0-9-[2468]]+`|<span data-ttu-id="bba04-608">匹配任意字符（从 0 到 9，除了 2、4、6 和 8 之外）的一个或多个匹配项。</span><span class="sxs-lookup"><span data-stu-id="bba04-608">Match one or more occurrences of any character from 0 to 9 except for 2, 4, 6, and 8.</span></span> <span data-ttu-id="bba04-609">换句话说，匹配零或奇数的一个或多个匹配项。</span><span class="sxs-lookup"><span data-stu-id="bba04-609">In other words, match one or more occurrences of zero or an odd digit.</span></span>|  
|$|<span data-ttu-id="bba04-610">在输入字符串末尾结束匹配。</span><span class="sxs-lookup"><span data-stu-id="bba04-610">End the match at the end of the input string.</span></span>|  
  
 [!code-csharp[Conceptual.RegEx.Language.CharacterClasses#15](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.regex.language.characterclasses/cs/classsubtraction1.cs#15)]
 [!code-vb[Conceptual.RegEx.Language.CharacterClasses#15](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.regex.language.characterclasses/vb/classsubtraction1.vb#15)]  
  
## <a name="see-also"></a><span data-ttu-id="bba04-611">请参阅</span><span class="sxs-lookup"><span data-stu-id="bba04-611">See also</span></span>

- <xref:System.Char.GetUnicodeCategory%2A>
- [<span data-ttu-id="bba04-612">正则表达式语言 - 快速参考</span><span class="sxs-lookup"><span data-stu-id="bba04-612">Regular Expression Language - Quick Reference</span></span>](regular-expression-language-quick-reference.md)
- [<span data-ttu-id="bba04-613">正则表达式选项</span><span class="sxs-lookup"><span data-stu-id="bba04-613">Regular Expression Options</span></span>](regular-expression-options.md)
