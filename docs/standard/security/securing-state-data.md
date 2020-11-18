---
title: 保护状态数据
description: 将状态数据声明为私有或内部变量，以限制对其的访问。 此类数据仍可通过反射、序列化和调试进行访问。
ms.date: 03/30/2017
helpviewer_keywords:
- security [.NET], state data
- code security, state data
- secure coding, state data
- state data security
ms.assetid: 12671309-2877-43fe-a3df-6863507e712d
ms.openlocfilehash: 849ed993befaceda1b04becbb7fb2530c5c62a77
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94824156"
---
# <a name="securing-state-data"></a><span data-ttu-id="dbbd0-104">保护状态数据</span><span class="sxs-lookup"><span data-stu-id="dbbd0-104">Securing State Data</span></span>

<span data-ttu-id="dbbd0-105">处理敏感数据或做出任何种类的安全决策的应用程序需要将相关数据保持在自己的控制之下，而不允许其他可能的恶意代码直接访问这些数据。</span><span class="sxs-lookup"><span data-stu-id="dbbd0-105">Applications that handle sensitive data or make any kind of security decisions need to keep that data under their own control and cannot allow other potentially malicious code to access the data directly.</span></span> <span data-ttu-id="dbbd0-106">保护内存中的数据的最好方法就是，将数据声明为私有或内部（范围限定为相同的程序集内）变量。</span><span class="sxs-lookup"><span data-stu-id="dbbd0-106">The best way to protect data in memory is to declare the data as private or internal (with scope limited to the same assembly) variables.</span></span> <span data-ttu-id="dbbd0-107">然而，即使这些数据受到访问权制约，你也应当注意：</span><span class="sxs-lookup"><span data-stu-id="dbbd0-107">However, even this data is subject to access you should be aware of:</span></span>  
  
- <span data-ttu-id="dbbd0-108">通过使用反射机制，那些能够引用你的对象的、高度受信任的代码可以获取和设置私有成员。</span><span class="sxs-lookup"><span data-stu-id="dbbd0-108">Using reflection mechanisms, highly trusted code that can reference your object can get and set private members.</span></span>  
  
- <span data-ttu-id="dbbd0-109">使用序列化时，如果高度受信任的代码可以访问序列化形式的对象中的相应数据，那么它就可以有效地获取和设置私有成员。</span><span class="sxs-lookup"><span data-stu-id="dbbd0-109">Using serialization, highly trusted code can effectively get and set private members if it can access the corresponding data in the serialized form of the object.</span></span>  
  
- <span data-ttu-id="dbbd0-110">调试时，可以读取这些数据。</span><span class="sxs-lookup"><span data-stu-id="dbbd0-110">Under debugging, this data can be read.</span></span>  
  
 <span data-ttu-id="dbbd0-111">千万不要让你自己的任何方法或属性在无意中公开这些值。</span><span class="sxs-lookup"><span data-stu-id="dbbd0-111">Make sure none of your own methods or properties exposes these values unintentionally.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dbbd0-112">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbbd0-112">See also</span></span>

- [<span data-ttu-id="dbbd0-113">安全编码准则</span><span class="sxs-lookup"><span data-stu-id="dbbd0-113">Secure Coding Guidelines</span></span>](secure-coding-guidelines.md)
- [<span data-ttu-id="dbbd0-114">ASP.NET Core 安全性</span><span class="sxs-lookup"><span data-stu-id="dbbd0-114">ASP.NET Core Security</span></span>](/aspnet/core/security/)
