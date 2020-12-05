---
title: 快速入门-使用 .NET 驱动 Raspberry Pi 的 HAT
description: 在5分钟内开始使用 .NET IoT 库，这是 Raspberry Pi 的附加板。
author: camsoper
ms.author: casoper
ms.date: 11/13/2020
ms.topic: quickstart
ms.prod: dotnet
ms.openlocfilehash: 2919db55304590f5557aa0cbda50cc4bd6640443
ms.sourcegitcommit: ecd9e9bb2225eb76f819722ea8b24988fe46f34c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "96739525"
---
# <a name="quickstart---use-net-to-drive-a-raspberry-pi-sense-hat"></a><span data-ttu-id="dcbb9-103">快速入门-使用 .NET 驱动 Raspberry Pi 的 HAT</span><span class="sxs-lookup"><span data-stu-id="dcbb9-103">Quickstart - Use .NET to drive a Raspberry Pi Sense HAT</span></span>

<span data-ttu-id="dcbb9-104">Raspberry Pi [HAT](https://www.raspberrypi.org/products/sense-hat/) <span class="docon docon-navigate-external x-hidden-focus"></span> (**H** 硬件 ttached **A** on **T** op) 是 Raspberry Pi 的附加板。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-104">The Raspberry Pi [Sense HAT](https://www.raspberrypi.org/products/sense-hat/) <span class="docon docon-navigate-external x-hidden-focus"></span> (**H** ardware **A** ttached on **T** op) is an add-on board for Raspberry Pi.</span></span> <span data-ttu-id="dcbb9-105">此感知 HAT 配有8× 8 RGB LED 矩阵、五按钮游戏杆，并包括以下传感器：</span><span class="sxs-lookup"><span data-stu-id="dcbb9-105">The Sense HAT is equipped with an 8×8 RGB LED matrix, a five-button joystick, and includes the following sensors:</span></span>

- <span data-ttu-id="dcbb9-106">陀螺仪</span><span class="sxs-lookup"><span data-stu-id="dcbb9-106">Gyroscope</span></span>
- <span data-ttu-id="dcbb9-107">加速计</span><span class="sxs-lookup"><span data-stu-id="dcbb9-107">Accelerometer</span></span>
- <span data-ttu-id="dcbb9-108">磁力计</span><span class="sxs-lookup"><span data-stu-id="dcbb9-108">Magnetometer</span></span>
- <span data-ttu-id="dcbb9-109">温度</span><span class="sxs-lookup"><span data-stu-id="dcbb9-109">Temperature</span></span>
- <span data-ttu-id="dcbb9-110">大气压力</span><span class="sxs-lookup"><span data-stu-id="dcbb9-110">Barometric pressure</span></span>
- <span data-ttu-id="dcbb9-111">湿度</span><span class="sxs-lookup"><span data-stu-id="dcbb9-111">Humidity</span></span>

<span data-ttu-id="dcbb9-112">此快速入门使用 .NET 从感知 HAT 检索传感器值、响应游戏杆输入，并推动 LED 矩阵。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-112">This quickstart uses .NET to retrieve sensor values from the Sense HAT, respond to joystick input, and drive the LED matrix.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dcbb9-113">先决条件</span><span class="sxs-lookup"><span data-stu-id="dcbb9-113">Prerequisites</span></span>

- [!INCLUDE [prereq-rpi](../includes/prereq-rpi.md)]
- <span data-ttu-id="dcbb9-114">感知 HAT</span><span class="sxs-lookup"><span data-stu-id="dcbb9-114">Sense HAT</span></span>

[!INCLUDE [prepare-pi-i2c](../includes/prepare-pi-i2c.md)]

## <a name="run-the-quickstart"></a><span data-ttu-id="dcbb9-115">运行快速入门</span><span class="sxs-lookup"><span data-stu-id="dcbb9-115">Run the quickstart</span></span>

<span data-ttu-id="dcbb9-116">将含义 HAT 附加到 Raspberry Pi。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-116">Attach the Sense HAT to your Raspberry Pi.</span></span> <span data-ttu-id="dcbb9-117">在 Raspberry Pi 上的 Bash 提示符 (本地或远程) 上，运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="dcbb9-117">From a Bash prompt on the Raspberry Pi (local or remote), run the following command:</span></span>

```bash
. <(wget -q -O - https://aka.ms/dotnet-iot-sensehat-quickstart)
```

<span data-ttu-id="dcbb9-118">命令下载并运行脚本。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-118">The command downloads and runs a script.</span></span> <span data-ttu-id="dcbb9-119">脚本：</span><span class="sxs-lookup"><span data-stu-id="dcbb9-119">The script:</span></span>

- <span data-ttu-id="dcbb9-120">安装 .NET SDK。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-120">Installs the .NET SDK.</span></span>
- <span data-ttu-id="dcbb9-121">克隆包含感知 HAT 快速入门项目的 GitHub 存储库。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-121">Clones a GitHub repository that includes the Sense HAT quickstart project.</span></span>
- <span data-ttu-id="dcbb9-122">生成项目。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-122">Builds the project.</span></span>
- <span data-ttu-id="dcbb9-123">运行该项目。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-123">Runs the project.</span></span>

<span data-ttu-id="dcbb9-124">显示传感器数据时，请查看控制台输出。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-124">Observe the console output as sensor data is displayed.</span></span> <span data-ttu-id="dcbb9-125">LED 矩阵在蓝色字段上显示黄色像素。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-125">The LED matrix displays a yellow pixel on a field of blue.</span></span> <span data-ttu-id="dcbb9-126">在任意方向上握住操纵杆会在该方向上移动黄色像素。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-126">Holding the joystick in any direction moves the yellow pixel in that direction.</span></span> <span data-ttu-id="dcbb9-127">单击中心游戏杆按钮会使背景从蓝色切换到红色。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-127">Clicking the center joystick button causes the background to switch from blue to red.</span></span>

## <a name="get-the-source-code"></a><span data-ttu-id="dcbb9-128">获取源代码</span><span class="sxs-lookup"><span data-stu-id="dcbb9-128">Get the source code</span></span>

<span data-ttu-id="dcbb9-129">此快速入门的源 [可在 GitHub 上找到](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/quickstarts/SenseHat.Quickstart) <span class="docon docon-navigate-external x-hidden-focus"></span> 。</span><span class="sxs-lookup"><span data-stu-id="dcbb9-129">The source for this quickstart is [available on GitHub](https://github.com/MicrosoftDocs/dotnet-iot-assets/tree/master/quickstarts/SenseHat.Quickstart) <span class="docon docon-navigate-external x-hidden-focus"></span>.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dcbb9-130">后续步骤</span><span class="sxs-lookup"><span data-stu-id="dcbb9-130">Next steps</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="dcbb9-131">了解如何使用常规用途输入/输出使 LED 闪烁</span><span class="sxs-lookup"><span data-stu-id="dcbb9-131">Learn to use General Purpose Input/Output to blink an LED</span></span>](../tutorials/blink-led.md)
