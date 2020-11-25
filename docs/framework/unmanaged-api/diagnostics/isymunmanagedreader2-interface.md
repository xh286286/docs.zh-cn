---
title: ISymUnmanagedReader2 接口
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2
helpviewer_keywords:
- ISymUnmanagedReader2 interface [.NET Framework debugging]
ms.assetid: a01a881b-82a3-4b3e-a3a9-9dc305c2e5f7
topic_type:
- apiref
ms.openlocfilehash: 3f34be833d3ccb5c636d2c5f18ccb6e216ef2c49
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95709071"
---
# <a name="isymunmanagedreader2-interface"></a><span data-ttu-id="297e6-102">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="297e6-102">ISymUnmanagedReader2 Interface</span></span>

<span data-ttu-id="297e6-103">表示一个符号读取器，该读取器提供对符号存储区中文档、方法和变量的访问。</span><span class="sxs-lookup"><span data-stu-id="297e6-103">Represents a symbol reader that provides access to documents, methods, and variables within a symbol store.</span></span> <span data-ttu-id="297e6-104">此接口扩展 [ISymUnmanagedReader](isymunmanagedreader-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="297e6-104">This interface extends the [ISymUnmanagedReader](isymunmanagedreader-interface.md) interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="297e6-105">方法</span><span class="sxs-lookup"><span data-stu-id="297e6-105">Methods</span></span>  
  
|<span data-ttu-id="297e6-106">方法</span><span class="sxs-lookup"><span data-stu-id="297e6-106">Method</span></span>|<span data-ttu-id="297e6-107">说明</span><span class="sxs-lookup"><span data-stu-id="297e6-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="297e6-108">GetMethodByVersionPreRemap 方法</span><span class="sxs-lookup"><span data-stu-id="297e6-108">GetMethodByVersionPreRemap Method</span></span>](isymunmanagedreader2-getmethodbyversionpreremap-method.md)|<span data-ttu-id="297e6-109">在给定方法标记和编辑并继续版本号的情况下，获取符号读取器方法。</span><span class="sxs-lookup"><span data-stu-id="297e6-109">Get a symbol reader method, given a method token and an edit-and-continue version number.</span></span>|  
|[<span data-ttu-id="297e6-110">GetMethodsInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="297e6-110">GetMethodsInDocument Method</span></span>](isymunmanagedreader2-getmethodsindocument-method.md)|<span data-ttu-id="297e6-111">获取所提供文档中包含行信息的每个方法。</span><span class="sxs-lookup"><span data-stu-id="297e6-111">Gets every method that has line information in the provided document.</span></span>|  
|[<span data-ttu-id="297e6-112">GetSymAttributePreRemap 方法</span><span class="sxs-lookup"><span data-stu-id="297e6-112">GetSymAttributePreRemap Method</span></span>](isymunmanagedreader2-getsymattributepreremap-method.md)|<span data-ttu-id="297e6-113">根据名称获取自定义属性。</span><span class="sxs-lookup"><span data-stu-id="297e6-113">Gets a custom attribute based upon its name.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="297e6-114">要求</span><span class="sxs-lookup"><span data-stu-id="297e6-114">Requirements</span></span>  

 <span data-ttu-id="297e6-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="297e6-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="297e6-116">另请参阅</span><span class="sxs-lookup"><span data-stu-id="297e6-116">See also</span></span>

- [<span data-ttu-id="297e6-117">诊断符号存储区接口</span><span class="sxs-lookup"><span data-stu-id="297e6-117">Diagnostics Symbol Store Interfaces</span></span>](diagnostics-symbol-store-interfaces.md)
- [<span data-ttu-id="297e6-118">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="297e6-118">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
