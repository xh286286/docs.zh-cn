---
title: ISymUnmanagedNamespace 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace
helpviewer_keywords:
- ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: d42bea4e-5848-4e43-a883-69af7a313ce9
topic_type:
- apiref
ms.openlocfilehash: d9b295060426acd7f925bcf19c05ba216fdc2a4d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95707893"
---
# <a name="isymunmanagednamespace-interface"></a><span data-ttu-id="09b07-102">ISymUnmanagedNamespace 接口</span><span class="sxs-lookup"><span data-stu-id="09b07-102">ISymUnmanagedNamespace Interface</span></span>

<span data-ttu-id="09b07-103">表示命名空间。</span><span class="sxs-lookup"><span data-stu-id="09b07-103">Represents a namespace.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="09b07-104">方法</span><span class="sxs-lookup"><span data-stu-id="09b07-104">Methods</span></span>  
  
|<span data-ttu-id="09b07-105">方法</span><span class="sxs-lookup"><span data-stu-id="09b07-105">Method</span></span>|<span data-ttu-id="09b07-106">说明</span><span class="sxs-lookup"><span data-stu-id="09b07-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="09b07-107">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="09b07-107">GetName Method</span></span>](isymunmanagednamespace-getname-method.md)|<span data-ttu-id="09b07-108">获取此命名空间的名称。</span><span class="sxs-lookup"><span data-stu-id="09b07-108">Gets the name of this namespace.</span></span>|  
|[<span data-ttu-id="09b07-109">GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="09b07-109">GetNamespaces Method</span></span>](isymunmanagednamespace-getnamespaces-method.md)|<span data-ttu-id="09b07-110">获取此命名空间的子级。</span><span class="sxs-lookup"><span data-stu-id="09b07-110">Gets the children of this namespace.</span></span>|  
|[<span data-ttu-id="09b07-111">GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="09b07-111">GetVariables Method</span></span>](isymunmanagednamespace-getvariables-method.md)|<span data-ttu-id="09b07-112">返回在此命名空间中的全局范围内定义的所有变量。</span><span class="sxs-lookup"><span data-stu-id="09b07-112">Returns all variables defined at global scope within this namespace.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="09b07-113">要求</span><span class="sxs-lookup"><span data-stu-id="09b07-113">Requirements</span></span>  

 <span data-ttu-id="09b07-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="09b07-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09b07-115">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09b07-115">See also</span></span>

- [<span data-ttu-id="09b07-116">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="09b07-116">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
