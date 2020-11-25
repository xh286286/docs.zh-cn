---
title: ISymUnmanagedENCUpdate 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate
helpviewer_keywords:
- ISymUnmanagedENCUpdate interface [.NET Framework debugging]
ms.assetid: 63a9ef45-01a6-46da-b958-5c6dc2dc232c
topic_type:
- apiref
ms.openlocfilehash: 5e3c2ecd1bdd5c1181223c7500eb7473e20fa5d4
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95731340"
---
# <a name="isymunmanagedencupdate-interface"></a><span data-ttu-id="d9cf6-102">ISymUnmanagedENCUpdate 接口</span><span class="sxs-lookup"><span data-stu-id="d9cf6-102">ISymUnmanagedENCUpdate Interface</span></span>

<span data-ttu-id="d9cf6-103">为 "编辑并继续" 功能提供函数。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-103">Provides functions for the Edit and Continue feature.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d9cf6-104">方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-104">Methods</span></span>  
  
|<span data-ttu-id="d9cf6-105">方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-105">Method</span></span>|<span data-ttu-id="d9cf6-106">说明</span><span class="sxs-lookup"><span data-stu-id="d9cf6-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d9cf6-107">GetLocalVariableCount 方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-107">GetLocalVariableCount Method</span></span>](isymunmanagedencupdate-getlocalvariablecount-method.md)|<span data-ttu-id="d9cf6-108">获取局部变量的数目。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-108">Gets the number of local variables.</span></span>|  
|[<span data-ttu-id="d9cf6-109">GetLocalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-109">GetLocalVariables Method</span></span>](isymunmanagedencupdate-getlocalvariables-method.md)|<span data-ttu-id="d9cf6-110">获取局部变量。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-110">Gets the local variables.</span></span>|  
|[<span data-ttu-id="d9cf6-111">InitializeForEnc 方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-111">InitializeForEnc Method</span></span>](isymunmanagedencupdate-initializeforenc-method.md)|<span data-ttu-id="d9cf6-112">允许在首次调用 [ISymUnmanagedENCUpdate：： UpdateSymbolStore2](isymunmanagedencupdate-updatesymbolstore2-method.md) 方法之前计算方法边界。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-112">Allows method boundaries to be computed before the first call to the [ISymUnmanagedENCUpdate::UpdateSymbolStore2](isymunmanagedencupdate-updatesymbolstore2-method.md) method.</span></span>|  
|[<span data-ttu-id="d9cf6-113">UpdateMethodLines 方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-113">UpdateMethodLines Method</span></span>](isymunmanagedencupdate-updatemethodlines-method.md)|<span data-ttu-id="d9cf6-114">允许更新尚未重新编译但行已单独移动的方法的行信息。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-114">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="d9cf6-115">允许每个语句的增量。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-115">A delta for each statement is allowed.</span></span>|  
|[<span data-ttu-id="d9cf6-116">UpdateSymbolStore2 方法</span><span class="sxs-lookup"><span data-stu-id="d9cf6-116">UpdateSymbolStore2 Method</span></span>](isymunmanagedencupdate-updatesymbolstore2-method.md)|<span data-ttu-id="d9cf6-117">如果行信息满足要求，则允许编译器省略未从程序数据库 (PDB) 流中修改的函数。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-117">Allows a compiler to omit functions that have not been modified from the program database (PDB) stream, provided that the line information meets the requirements.</span></span> <span data-ttu-id="d9cf6-118">可以通过旧的 PDB 行信息和函数中所有行的一个增量来确定正确的行信息。</span><span class="sxs-lookup"><span data-stu-id="d9cf6-118">The correct line information can be determined with the old PDB line information and one delta for all lines in the function.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d9cf6-119">要求</span><span class="sxs-lookup"><span data-stu-id="d9cf6-119">Requirements</span></span>  

 <span data-ttu-id="d9cf6-120">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d9cf6-120">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9cf6-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9cf6-121">See also</span></span>

- [<span data-ttu-id="d9cf6-122">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="d9cf6-122">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
