---
ms.openlocfilehash: 60e326af0d956ceb63b32e5d3ec2436fe09a7005
ms.sourcegitcommit: b201d177e01480a139622f3bf8facd367657a472
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2020
ms.locfileid: "96591049"
---
<span data-ttu-id="08e5f-101">[使用 SFTP 客户端](https://www.raspberrypi.org/documentation/remote-access/ssh/sftp.md)，将文件从开发计算机上的发布位置复制到 Raspberry Pi 上的新文件夹中。</span><span class="sxs-lookup"><span data-stu-id="08e5f-101">[Using an SFTP client](https://www.raspberrypi.org/documentation/remote-access/ssh/sftp.md), copy the files from the publish location on the development computer to a new folder on the Raspberry Pi.</span></span>

<span data-ttu-id="08e5f-102">例如，若要使用 `scp` 命令将文件从开发计算机复制到 Raspberry Pi，请打开命令提示符并执行以下命令：</span><span class="sxs-lookup"><span data-stu-id="08e5f-102">For example, to use the `scp` command to copy files from the development computer to your Raspberry Pi, open a command prompt and execute the following:</span></span>

```console
scp -r /publish-location/* pi@raspberrypi:/home/pi/deployment-location/
```

<span data-ttu-id="08e5f-103">其中：</span><span class="sxs-lookup"><span data-stu-id="08e5f-103">Where:</span></span>

- <span data-ttu-id="08e5f-104">`-r`选项指示 `scp` 以递归方式复制文件。</span><span class="sxs-lookup"><span data-stu-id="08e5f-104">The `-r` option instructs `scp` to copy files recursively.</span></span>
- <span data-ttu-id="08e5f-105">*/publish-location/* 是在上一步中发布到的文件夹。</span><span class="sxs-lookup"><span data-stu-id="08e5f-105">*/publish-location/* is the folder you published to in the previous step.</span></span>
- <span data-ttu-id="08e5f-106">`pi@raspberypi` 用户和主机名的格式 `<username>@<hostname>` 。</span><span class="sxs-lookup"><span data-stu-id="08e5f-106">`pi@raspberypi` is the user and host names in the format `<username>@<hostname>`.</span></span>
- <span data-ttu-id="08e5f-107">*/home/pi/deployment-location/* 是 Raspberry pi 上的新文件夹。</span><span class="sxs-lookup"><span data-stu-id="08e5f-107">*/home/pi/deployment-location/* is the new folder on the Raspberry Pi.</span></span>

> [!TIP]
> <span data-ttu-id="08e5f-108">最新版本的 Windows 具有 OpenSSH，其中包括 `scp` 预安装的。</span><span class="sxs-lookup"><span data-stu-id="08e5f-108">Recent versions of Windows have OpenSSH, which includes `scp`, pre-installed.</span></span>
