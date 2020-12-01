---
title: 如何：检索与 WebRequest 匹配的特定于协议的 WebResponse
description: 了解如何检索与 .NET Framework 中的 WebRequest 匹配的特定于协议的 WebResponse。
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d8c90785-f16b-42a5-8439-ed2f731b2ba8
ms.openlocfilehash: fd163c115dcd19c05f93f4c202b043440834ba9d
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96266735"
---
# <a name="how-to-retrieve-a-protocol-specific-webresponse-that-matches-a-webrequest"></a><span data-ttu-id="d1ab2-103">如何：检索与 WebRequest 匹配的特定于协议的 WebResponse</span><span class="sxs-lookup"><span data-stu-id="d1ab2-103">How to: Retrieve a Protocol-Specific WebResponse that Matches a WebRequest</span></span>

<span data-ttu-id="d1ab2-104">此示例演示如何检索与 WebRequest 匹配的特定于协议的 WebResponse。</span><span class="sxs-lookup"><span data-stu-id="d1ab2-104">This example shows how to retrieve a protocol-specific WebResponse that matches a WebRequest.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d1ab2-105">示例</span><span class="sxs-lookup"><span data-stu-id="d1ab2-105">Example</span></span>  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
WebResponse resp = req.GetResponse();  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com")  
Dim resp As WebResponse = req.GetResponse()  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d1ab2-106">编译代码</span><span class="sxs-lookup"><span data-stu-id="d1ab2-106">Compiling the Code</span></span>  

 <span data-ttu-id="d1ab2-107">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="d1ab2-107">This example requires:</span></span>  
  
- <span data-ttu-id="d1ab2-108">引用 System.Net 命名空间。</span><span class="sxs-lookup"><span data-stu-id="d1ab2-108">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1ab2-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1ab2-109">See also</span></span>

- [<span data-ttu-id="d1ab2-110">请求数据</span><span class="sxs-lookup"><span data-stu-id="d1ab2-110">Requesting Data</span></span>](requesting-data.md)
