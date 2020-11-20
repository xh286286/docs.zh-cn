---
title: SYSLIB0009 警告
description: 了解有关生成编译时警告 SYSLIB0009 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 47b4f595a54800370da90f61d838c665df8b6091
ms.sourcegitcommit: 30a686fd4377fe6472aa04e215c0de711bc1c322
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94439971"
---
# <a name="syslib0009-the-authenticationmanager-authenticate-and-preauthenticate-methods-are-not-supported"></a>SYSLIB0009：AuthenticationManager 身份验证和预身份验证方法不受支持

从 .NET 5.0 开始，以下 API 标记为已过时。 使用这些 API 会在编译时生成警告 `SYSLIB0009`。

- <xref:System.Net.AuthenticationManager.Authenticate%2A?displayProperty=nameWithType>
- <xref:System.Net.AuthenticationManager.PreAuthenticate%2A?displayProperty=nameWithType>

## <a name="suppress-the-warning"></a>禁止显示警告

如果无法更改代码，可以通过 `#pragma` 指令或 `<NoWarn>` 项目设置来禁止显示警告。 有关示例，请参阅[禁止显示警告](syslib-obsoletions.md#suppress-warnings)。
