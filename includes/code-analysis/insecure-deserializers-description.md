---
author: dotpaul
ms.author: paulming
ms.date: 04/05/2019
ms.topic: include
ms.openlocfilehash: 9235f1bcda7529b71aef542d3a49da08a9d4b59e
ms.sourcegitcommit: c04535ad05e374fb269fcfc6509217755fbc0d54
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2020
ms.locfileid: "96590079"
---
<span data-ttu-id="6a495-101">反序列化不受信任的数据时，不安全的反会很容易</span><span class="sxs-lookup"><span data-stu-id="6a495-101">Insecure deserializers are vulnerable when deserializing untrusted data.</span></span> <span data-ttu-id="6a495-102">攻击者可能会修改序列化的数据，使其包含意外类型，以注入具有恶意副作用的对象。</span><span class="sxs-lookup"><span data-stu-id="6a495-102">An attacker could modify the serialized data to include unexpected types to inject objects with malicious side effects.</span></span> <span data-ttu-id="6a495-103">例如，对不安全的反序列化程序的攻击可以在基础操作系统上执行命令，通过网络进行通信，或删除文件。</span><span class="sxs-lookup"><span data-stu-id="6a495-103">An attack against an insecure deserializer could, for example, execute commands on the underlying operating system, communicate over the network, or delete files.</span></span>
