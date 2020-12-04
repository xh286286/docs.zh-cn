---
title: 利用 .NET IoT 库为 IoT 设备开发应用
description: 了解如何使用 .NET 为 IoT 设备和方案生成应用程序。
author: camsoper
ms.author: casoper
ms.date: 11/13/2020
ms.topic: overview
ms.prod: dotnet
ms.openlocfilehash: c3d05ec5b05780f91404c3c27e91bcd602b0faeb
ms.sourcegitcommit: b201d177e01480a139622f3bf8facd367657a472
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2020
ms.locfileid: "96591052"
---
# <a name="develop-apps-for-iot-devices-with-the-net-iot-libraries"></a><span data-ttu-id="3e5a5-103">利用 .NET IoT 库为 IoT 设备开发应用</span><span class="sxs-lookup"><span data-stu-id="3e5a5-103">Develop apps for IoT devices with the .NET IoT Libraries</span></span>

<span data-ttu-id="3e5a5-104">.NET 在各种平台和体系结构上运行。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-104">.NET runs on a variety of platforms and architectures.</span></span> <span data-ttu-id="3e5a5-105">支持常见物联网 (IoT) 板，如 Raspberry Pi 和 Hummingboard）。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-105">Common Internet of things (IoT) boards, such as Raspberry Pi and Hummingboard, are supported.</span></span> <span data-ttu-id="3e5a5-106">IoT apps 通常与专用硬件（如传感器、模拟到数字转换器和 LCD 设备）交互。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-106">IoT apps typically interact with specialized hardware, such as sensors, analog-to-digital converters, and LCD devices.</span></span> <span data-ttu-id="3e5a5-107">.NET IoT 库可实现这些方案。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-107">The .NET IoT Libraries enable these scenarios.</span></span>

## <a name="video-overview"></a><span data-ttu-id="3e5a5-108">视频概述</span><span class="sxs-lookup"><span data-stu-id="3e5a5-108">Video overview</span></span>

<!--markdownlint-disable MD034 -->
> [!VIDEO https://channel9.msdn.com/Series/IoT-101/Intro-to-IOT-with-NET-Core-1-of-9/player]

## <a name="libraries"></a><span data-ttu-id="3e5a5-109">库</span><span class="sxs-lookup"><span data-stu-id="3e5a5-109">Libraries</span></span>

<span data-ttu-id="3e5a5-110">.NET IoT 库由两个 NuGet 包组成：</span><span class="sxs-lookup"><span data-stu-id="3e5a5-110">The .NET IoT Libraries are composed of two NuGet packages:</span></span>

- <span data-ttu-id="3e5a5-111">[System.Device.Gpio](https://www.nuget.org/packages/System.Device.Gpio/) <span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-111">[System.Device.Gpio](https://www.nuget.org/packages/System.Device.Gpio/) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>
- <span data-ttu-id="3e5a5-112">[Iot.Device.Bindings](https://www.nuget.org/packages/Iot.Device.Bindings/) <span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-112">[Iot.Device.Bindings](https://www.nuget.org/packages/Iot.Device.Bindings/) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>

### <a name="systemdevicegpio"></a><span data-ttu-id="3e5a5-113">System.Device.Gpio</span><span class="sxs-lookup"><span data-stu-id="3e5a5-113">System.Device.Gpio</span></span>

<span data-ttu-id="3e5a5-114">`System.Device.Gpio` 支持各种协议，用于与低级别硬件 pin 交互以控制设备。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-114">`System.Device.Gpio` supports a variety of protocols for interacting with low-level hardware pins to control devices.</span></span> <span data-ttu-id="3e5a5-115">其中包括：</span><span class="sxs-lookup"><span data-stu-id="3e5a5-115">These include:</span></span>

- <span data-ttu-id="3e5a5-116">常规用途 I/O (GPIO)</span><span class="sxs-lookup"><span data-stu-id="3e5a5-116">General-purpose I/O (GPIO)</span></span>
- <span data-ttu-id="3e5a5-117">Inter-Integrated 线路 (I2C) </span><span class="sxs-lookup"><span data-stu-id="3e5a5-117">Inter-Integrated Circuit (I2C)</span></span>
- <span data-ttu-id="3e5a5-118">串行外围设备接口 (SPI) </span><span class="sxs-lookup"><span data-stu-id="3e5a5-118">Serial Peripheral Interface (SPI)</span></span>
- <span data-ttu-id="3e5a5-119">脉冲宽度调制 (PWM) </span><span class="sxs-lookup"><span data-stu-id="3e5a5-119">Pulse Width Modulation (PWM)</span></span>
- <span data-ttu-id="3e5a5-120">串行端口</span><span class="sxs-lookup"><span data-stu-id="3e5a5-120">Serial port</span></span>

### <a name="iotdevicebindings"></a><span data-ttu-id="3e5a5-121">Iot.Device.Bindings</span><span class="sxs-lookup"><span data-stu-id="3e5a5-121">Iot.Device.Bindings</span></span>

<span data-ttu-id="3e5a5-122">`Iot.Device.Bindings`包：</span><span class="sxs-lookup"><span data-stu-id="3e5a5-122">The `Iot.Device.Bindings` package:</span></span>

* <span data-ttu-id="3e5a5-123">包含 [设备绑定](https://github.com/dotnet/iot/blob/master/src/devices/README.md) <span class="docon docon-navigate-external x-hidden-focus"></span> ，用于通过包装 system.web 来简化应用程序开发。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-123">Contains [device bindings](https://github.com/dotnet/iot/blob/master/src/devices/README.md) <span class="docon docon-navigate-external x-hidden-focus"></span> to streamline app development by wrapping System.Device.Gpio.</span></span>
* <span data-ttu-id="3e5a5-124">支持社区，并持续添加其他绑定。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-124">Is community-supported, and additional bindings are added continually.</span></span>

<span data-ttu-id="3e5a5-125">常用的设备绑定包括：</span><span class="sxs-lookup"><span data-stu-id="3e5a5-125">Commonly used device bindings include:</span></span>

- <span data-ttu-id="3e5a5-126">[CharacterLcd-LCD 字符显示](https://github.com/dotnet/iot/tree/master/src/devices/CharacterLcd)<span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-126">[CharacterLcd - LCD character display](https://github.com/dotnet/iot/tree/master/src/devices/CharacterLcd) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>
- <span data-ttu-id="3e5a5-127">[SN74HC595-8 位移位寄存器](https://github.com/dotnet/iot/tree/master/src/devices/Sn74hc595)<span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-127">[SN74HC595 - 8-bit shift register](https://github.com/dotnet/iot/tree/master/src/devices/Sn74hc595) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>
- <span data-ttu-id="3e5a5-128">[BrickPi3](https://github.com/dotnet/iot/tree/master/src/devices/BrickPi3)<span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-128">[BrickPi3](https://github.com/dotnet/iot/tree/master/src/devices/BrickPi3) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>
- <span data-ttu-id="3e5a5-129">[Max7219 导向 Matrix 驱动程序](https://github.com/dotnet/iot/tree/master/src/devices/Max7219)<span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-129">[Max7219 - LED Matrix driver](https://github.com/dotnet/iot/tree/master/src/devices/Max7219) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>
- <span data-ttu-id="3e5a5-130">[RGBLedMatrix-RGB LED 矩阵](https://github.com/dotnet/iot/tree/master/src/devices/RGBLedMatrix)<span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-130">[RGBLedMatrix - RGB LED Matrix](https://github.com/dotnet/iot/tree/master/src/devices/RGBLedMatrix) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="3e5a5-131">支持的操作系统</span><span class="sxs-lookup"><span data-stu-id="3e5a5-131">Supported operating systems</span></span>

<span data-ttu-id="3e5a5-132">`System.Device.Gpio` 支持 ARM/ARM64 和 Windows 10 IoT Core 的大多数 Linux 版本都支持。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-132">`System.Device.Gpio` is supported on most versions of Linux that support ARM/ARM64 and Windows 10 IoT Core.</span></span>

> [!TIP]
> <span data-ttu-id="3e5a5-133">对于 Raspberry Pi，建议使用[Raspberry PI OS](https://www.raspberrypi.org/documentation/installation/installing-images/README.md) <span class="docon docon-navigate-external x-hidden-focus"></span> (以前的 Raspbian) 。  </span><span class="sxs-lookup"><span data-stu-id="3e5a5-133">For Raspberry Pi, [Raspberry Pi OS](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)  <span class="docon docon-navigate-external x-hidden-focus"></span> (formerly Raspbian) is recommended.</span></span>

## <a name="supported-hardware-platforms"></a><span data-ttu-id="3e5a5-134">支持的硬件平台</span><span class="sxs-lookup"><span data-stu-id="3e5a5-134">Supported hardware platforms</span></span>

<span data-ttu-id="3e5a5-135">`System.Device.Gpio` 与大多数单板平台兼容。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-135">`System.Device.Gpio` is compatible with most single-board platforms.</span></span> <span data-ttu-id="3e5a5-136">推荐的平台是 Raspberry Pi (2 及更高版本) 和 Hummingboard。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-136">Recommended platforms are Raspberry Pi (2 and greater) and Hummingboard.</span></span> <span data-ttu-id="3e5a5-137">已知兼容的其他平台是 BeagleBoard 和 ODROID。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-137">Other platforms known to be compatible are BeagleBoard and ODROID.</span></span>

<span data-ttu-id="3e5a5-138">通过使用 USB 到 SPI/I2C 桥，支持 PC 平台。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-138">PC platforms are supported via the use of a USB to SPI/I2C bridge.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e5a5-139">在 ARMv6 体系结构设备上不支持 .NET，其中包括 Raspberry Pi 2 之前的 Raspberry Pi 零和 Raspberry Pi 设备。</span><span class="sxs-lookup"><span data-stu-id="3e5a5-139">.NET is not supported on ARMv6 architecture devices, including Raspberry Pi Zero and Raspberry Pi devices prior to Raspberry Pi 2.</span></span>

## <a name="resources"></a><span data-ttu-id="3e5a5-140">资源</span><span class="sxs-lookup"><span data-stu-id="3e5a5-140">Resources</span></span>

- <span data-ttu-id="3e5a5-141">[Github 上的 .Net IoT 库](https://github.com/dotnet/iot)<span class="docon docon-navigate-external x-hidden-focus"></span></span><span class="sxs-lookup"><span data-stu-id="3e5a5-141">[.NET IoT Libraries on Github](https://github.com/dotnet/iot) <span class="docon docon-navigate-external x-hidden-focus"></span></span></span>
