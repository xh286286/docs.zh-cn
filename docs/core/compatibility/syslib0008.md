---
title: SYSLIB0008 警告
description: 了解有关生成编译时警告 SYSLIB0008 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 22ac5b4c5f57ec3f92585ee8d1f8cf278a15dbb0
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94440590"
---
# <a name="syslib0008-createpdbgenerator-is-not-supported"></a>SYSLIB0008：不支持 CreatePdbGenerator

从 .NET 5.0 开始，<xref:System.Runtime.CompilerServices.DebugInfoGenerator.CreatePdbGenerator?displayProperty=nameWithType> API 标记为已过时。 使用此 API 会在编译时生成警告 `SYSLIB0008`。

## <a name="suppress-the-warning"></a>禁止显示警告

如果无法更改代码，可以通过 `#pragma` 指令或 `<NoWarn>` 项目设置来禁止显示警告。 有关示例，请参阅[禁止显示警告](syslib-obsoletions.md#suppress-warnings)。
