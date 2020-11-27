---
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: c618b5b41790b04a84b4c50fe47baa2c0cb05ab2
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96274096"
---
# <a name="symmetricsecuritybindingelement"></a><span data-ttu-id="ce529-102">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="ce529-102">SymmetricSecurityBindingElement</span></span>

<span data-ttu-id="ce529-103">SymmetricSecurityBindingElement</span><span class="sxs-lookup"><span data-stu-id="ce529-103">SymmetricSecurityBindingElement</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ce529-104">语法</span><span class="sxs-lookup"><span data-stu-id="ce529-104">Syntax</span></span>  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="ce529-105">方法</span><span class="sxs-lookup"><span data-stu-id="ce529-105">Methods</span></span>  

 <span data-ttu-id="ce529-106">SymmetricSecurityBindingElement 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="ce529-106">The SymmetricSecurityBindingElement class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="ce529-107">属性</span><span class="sxs-lookup"><span data-stu-id="ce529-107">Properties</span></span>  

 <span data-ttu-id="ce529-108">SymmetricSecurityBindingElement 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="ce529-108">The SymmetricSecurityBindingElement class has the following properties:</span></span>  
  
### <a name="messageprotectionorder"></a><span data-ttu-id="ce529-109">MessageProtectionOrder</span><span class="sxs-lookup"><span data-stu-id="ce529-109">MessageProtectionOrder</span></span>  

 <span data-ttu-id="ce529-110">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="ce529-110">Data type: string</span></span>  
  
 <span data-ttu-id="ce529-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="ce529-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ce529-112">此绑定的消息加密和签名的顺序。</span><span class="sxs-lookup"><span data-stu-id="ce529-112">The order of message encryption and signing for this binding.</span></span>  
  
### <a name="requiresignatureconfirmation"></a><span data-ttu-id="ce529-113">RequireSignatureConfirmation</span><span class="sxs-lookup"><span data-stu-id="ce529-113">RequireSignatureConfirmation</span></span>  

 <span data-ttu-id="ce529-114">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="ce529-114">Data type: boolean</span></span>  
  
 <span data-ttu-id="ce529-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="ce529-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="ce529-116">此绑定是否需要签名确认。</span><span class="sxs-lookup"><span data-stu-id="ce529-116">Whether the binding requires signature confirmation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ce529-117">要求</span><span class="sxs-lookup"><span data-stu-id="ce529-117">Requirements</span></span>  
  
|<span data-ttu-id="ce529-118">MOF</span><span class="sxs-lookup"><span data-stu-id="ce529-118">MOF</span></span>|<span data-ttu-id="ce529-119">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="ce529-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="ce529-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="ce529-120">Namespace</span></span>|<span data-ttu-id="ce529-121">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="ce529-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="ce529-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ce529-122">See also</span></span>

- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
