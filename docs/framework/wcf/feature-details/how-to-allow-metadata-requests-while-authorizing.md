---
title: 如何：授权时允许元数据请求
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- allowing metadata requests while authorizing [WCF]
ms.assetid: 90cec34f-b619-452b-a056-8b1c0de49d05
ms.openlocfilehash: 9acc007ea7837f7b8e6c958fa81547fe4fa5b2c0
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96257608"
---
# <a name="how-to-allow-metadata-requests-while-authorizing"></a><span data-ttu-id="59834-102">如何：授权时允许元数据请求</span><span class="sxs-lookup"><span data-stu-id="59834-102">How To: Allow Metadata Requests While Authorizing</span></span>

<span data-ttu-id="59834-103">自定义授权时，可能有必要允许处理对元数据的请求。</span><span class="sxs-lookup"><span data-stu-id="59834-103">During custom authorization, it may be necessary to allow a request for metadata to be processed.</span></span> <span data-ttu-id="59834-104">以下主题将演练验证此类请求的步骤。</span><span class="sxs-lookup"><span data-stu-id="59834-104">The following topic walks through the steps to validate such a request.</span></span>  
  
 <span data-ttu-id="59834-105">有关 Windows Communication Foundation (WCF) 授权的详细信息，请参阅 [授权](authorization-in-wcf.md)。</span><span class="sxs-lookup"><span data-stu-id="59834-105">For more information about Windows Communication Foundation (WCF) authorization, see [Authorization](authorization-in-wcf.md).</span></span>  
  
### <a name="to-allow-metadata-requests-during-authorization"></a><span data-ttu-id="59834-106">授权时允许元数据请求</span><span class="sxs-lookup"><span data-stu-id="59834-106">To allow metadata requests during authorization</span></span>  
  
1. <span data-ttu-id="59834-107">创建 <xref:System.ServiceModel.ServiceAuthorizationManager> 类的扩展。</span><span class="sxs-lookup"><span data-stu-id="59834-107">Create an extension of the <xref:System.ServiceModel.ServiceAuthorizationManager> class.</span></span>  
  
2. <span data-ttu-id="59834-108">重写 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="59834-108">Override the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> method.</span></span> <span data-ttu-id="59834-109">取决于是否允许授权，该方法返回 `true` 或 `false`。</span><span class="sxs-lookup"><span data-stu-id="59834-109">The method returns `true` or `false` depending on whether authorization is allowed.</span></span> <span data-ttu-id="59834-110">有关当前过程的信息，请参见作为参数传递给该方法的 <xref:System.ServiceModel.OperationContext>。</span><span class="sxs-lookup"><span data-stu-id="59834-110">Information about the current procedure is found in the <xref:System.ServiceModel.OperationContext> passed as a parameter to the method.</span></span>  
  
3. <span data-ttu-id="59834-111">重写时，检查协定名称、命名空间和操作，如在以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="59834-111">In the override, check the contract name, namespace, and the action as shown in the following example.</span></span> <span data-ttu-id="59834-112">如果条件无效，则将返回 `true.`。</span><span class="sxs-lookup"><span data-stu-id="59834-112">If the conditions are valid, then return `true.`</span></span>  
  
4. <span data-ttu-id="59834-113">使用扩展点利用类。</span><span class="sxs-lookup"><span data-stu-id="59834-113">Use the extensibility point to employ the class.</span></span> <span data-ttu-id="59834-114">有关详细信息，请参阅 [如何：为服务创建自定义授权管理器](../extending/how-to-create-a-custom-authorization-manager-for-a-service.md)。</span><span class="sxs-lookup"><span data-stu-id="59834-114">For more information, see [How to: Create a Custom Authorization Manager for a Service](../extending/how-to-create-a-custom-authorization-manager-for-a-service.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="59834-115">示例</span><span class="sxs-lookup"><span data-stu-id="59834-115">Example</span></span>  

 <span data-ttu-id="59834-116">下面的示例演示对 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> 方法的重写。</span><span class="sxs-lookup"><span data-stu-id="59834-116">The following example shows an override of the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccessCore%2A> method.</span></span>  
  
 [!code-csharp[C_HowtoCheckForMexRequestsInAuthorization#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_howtocheckformexrequestsinauthorization/cs/source.cs#1)]
 [!code-vb[C_HowtoCheckForMexRequestsInAuthorization#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_howtocheckformexrequestsinauthorization/vb/source.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="59834-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="59834-117">See also</span></span>

- <xref:System.ServiceModel.ServiceAuthorizationManager>
- [<span data-ttu-id="59834-118">授权</span><span class="sxs-lookup"><span data-stu-id="59834-118">Authorization</span></span>](authorization-in-wcf.md)
- [<span data-ttu-id="59834-119">使用标识模型管理声明和授权</span><span class="sxs-lookup"><span data-stu-id="59834-119">Managing Claims and Authorization with the Identity Model</span></span>](managing-claims-and-authorization-with-the-identity-model.md)
