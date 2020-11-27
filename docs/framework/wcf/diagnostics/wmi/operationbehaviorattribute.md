---
title: OperationBehaviorAttribute
ms.date: 03/30/2017
ms.assetid: 8c9b0755-9e83-411f-bdcb-61a586022797
ms.openlocfilehash: 76cc619aed4ba2b944a8d11dc454a40368a4068c
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96269075"
---
# <a name="operationbehaviorattribute"></a><span data-ttu-id="dbdff-102">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="dbdff-102">OperationBehaviorAttribute</span></span>

<span data-ttu-id="dbdff-103">OperationBehaviorAttribute</span><span class="sxs-lookup"><span data-stu-id="dbdff-103">OperationBehaviorAttribute</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dbdff-104">语法</span><span class="sxs-lookup"><span data-stu-id="dbdff-104">Syntax</span></span>  
  
```csharp
class OperationBehaviorAttribute : Behavior  
{  
  boolean AutoDisposeParameters;  
  string Impersonation;  
  string ReleaseInstanceMode;  
  boolean TransactionAutoComplete;  
  boolean TransactionScopeRequired;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="dbdff-105">方法</span><span class="sxs-lookup"><span data-stu-id="dbdff-105">Methods</span></span>  

 <span data-ttu-id="dbdff-106">OperationBehaviorAttribute 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="dbdff-106">The OperationBehaviorAttribute class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="dbdff-107">属性</span><span class="sxs-lookup"><span data-stu-id="dbdff-107">Properties</span></span>  

 <span data-ttu-id="dbdff-108">OperationBehaviorAttribute 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="dbdff-108">The OperationBehaviorAttribute class has the following properties:</span></span>  
  
### <a name="autodisposeparameters"></a><span data-ttu-id="dbdff-109">AutoDisposeParameters</span><span class="sxs-lookup"><span data-stu-id="dbdff-109">AutoDisposeParameters</span></span>  

 <span data-ttu-id="dbdff-110">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="dbdff-110">Data type: boolean</span></span>  
  
 <span data-ttu-id="dbdff-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="dbdff-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dbdff-112">参数自动释放功能的状态。</span><span class="sxs-lookup"><span data-stu-id="dbdff-112">The state of the auto-dispose feature for parameters.</span></span>  
  
### <a name="impersonation"></a><span data-ttu-id="dbdff-113">模拟</span><span class="sxs-lookup"><span data-stu-id="dbdff-113">Impersonation</span></span>  

 <span data-ttu-id="dbdff-114">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="dbdff-114">Data type: string</span></span>  
  
 <span data-ttu-id="dbdff-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="dbdff-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dbdff-116">指示操作支持的调用方模拟级别。</span><span class="sxs-lookup"><span data-stu-id="dbdff-116">Indicates the level of caller impersonation that the operation supports.</span></span>  
  
### <a name="releaseinstancemode"></a><span data-ttu-id="dbdff-117">ReleaseInstanceMode</span><span class="sxs-lookup"><span data-stu-id="dbdff-117">ReleaseInstanceMode</span></span>  

 <span data-ttu-id="dbdff-118">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="dbdff-118">Data type: string</span></span>  
  
 <span data-ttu-id="dbdff-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="dbdff-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dbdff-120">指示操作调用过程中何时回收对象。</span><span class="sxs-lookup"><span data-stu-id="dbdff-120">Indicates when in the course of an operation invocation to recycle the object.</span></span>  
  
### <a name="transactionautocomplete"></a><span data-ttu-id="dbdff-121">TransactionAutoComplete</span><span class="sxs-lookup"><span data-stu-id="dbdff-121">TransactionAutoComplete</span></span>  

 <span data-ttu-id="dbdff-122">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="dbdff-122">Data type: boolean</span></span>  
  
 <span data-ttu-id="dbdff-123">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="dbdff-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dbdff-124">指示在未发生未处理的异常的情况下是否自动提交当前事务。</span><span class="sxs-lookup"><span data-stu-id="dbdff-124">Indicates whether to automatically commit the current transaction if no unhandled exceptions occur.</span></span>  
  
### <a name="transactionscoperequired"></a><span data-ttu-id="dbdff-125">TransactionScopeRequired</span><span class="sxs-lookup"><span data-stu-id="dbdff-125">TransactionScopeRequired</span></span>  

 <span data-ttu-id="dbdff-126">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="dbdff-126">Data type: boolean</span></span>  
  
 <span data-ttu-id="dbdff-127">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="dbdff-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="dbdff-128">指示操作是否需要事务处理。</span><span class="sxs-lookup"><span data-stu-id="dbdff-128">Indicates whether the operation requires a transaction.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dbdff-129">要求</span><span class="sxs-lookup"><span data-stu-id="dbdff-129">Requirements</span></span>  
  
|<span data-ttu-id="dbdff-130">MOF</span><span class="sxs-lookup"><span data-stu-id="dbdff-130">MOF</span></span>|<span data-ttu-id="dbdff-131">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="dbdff-131">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="dbdff-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="dbdff-132">Namespace</span></span>|<span data-ttu-id="dbdff-133">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="dbdff-133">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="dbdff-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dbdff-134">See also</span></span>

- <xref:System.ServiceModel.OperationBehaviorAttribute>
