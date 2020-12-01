---
title: 如何：转换 WebRequest 以访问特定于协议的属性
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: d9a8eae2-7454-46f9-b43b-c98477c5bcde
ms.openlocfilehash: 09bd551dad77358b1503871c6ee100a869adf75b
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96253422"
---
# <a name="how-to-typecast-a-webrequest-to-access-protocol-specific-properties"></a><span data-ttu-id="833a1-102">如何：转换 WebRequest 以访问特定于协议的属性</span><span class="sxs-lookup"><span data-stu-id="833a1-102">How to: Typecast a WebRequest to Access Protocol Specific Properties</span></span>

<span data-ttu-id="833a1-103">此示例演示如何类型转换 WebRequest 以访问特定于协议的属性。</span><span class="sxs-lookup"><span data-stu-id="833a1-103">This example shows how to typecast a WebRequest so that you can access protocol specific properties.</span></span>  
  
## <a name="example"></a><span data-ttu-id="833a1-104">示例</span><span class="sxs-lookup"><span data-stu-id="833a1-104">Example</span></span>  
  
```csharp  
HttpWebRequest httpreq =
   (HttpWebRequest) WebRequest.Create("http://www.contoso.com/");  
```  
  
```vb  
Dim httpreq As HttpWebRequest = _  
   CType(WebRequest.Create("http://www.contoso.com/"), HttpWebRequest)  
```  
  
## <a name="see-also"></a><span data-ttu-id="833a1-105">另请参阅</span><span class="sxs-lookup"><span data-stu-id="833a1-105">See also</span></span>

- [<span data-ttu-id="833a1-106">对可插入协议进行编程</span><span class="sxs-lookup"><span data-stu-id="833a1-106">Programming Pluggable Protocols</span></span>](programming-pluggable-protocols.md)
