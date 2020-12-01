---
ms.openlocfilehash: 540eebd957ce8ce0928db2bd8317cb220cba30bb
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96031746"
---

[dotnet-install 脚本](../../tools/dotnet-install-script.md)用于 **SDK** 和 **运行时** 的自动化和非管理员安装。 可通过 <https://dot.net/v1/dotnet-install.sh> 下载脚本。

此脚本默认安装最新的 SDK [长期支持 (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) 版本，即 .NET Core 3.1。 若要安装当前版本（可能不是 (LTS) 版本），请使用 `-c Current` 参数。

```bash
./dotnet-install.sh -c Current
```

若要安装 .NET 运行时而非 SDK，请使用 `--runtime` 参数。

```bash
./dotnet-install.sh -c Current --runtime aspnetcore
```

可以通过更改 `-c` 参数以指示特定版本来安装特定版本。 以下命令将安装 .NET SDK 5.0。

```bash
./dotnet-install.sh -c 5.0
```

有关详细信息，请参阅 [dotnet-install 脚本参考](../../tools/dotnet-install-script.md)。
