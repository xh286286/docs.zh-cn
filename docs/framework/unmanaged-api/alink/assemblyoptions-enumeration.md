---
title: AssemblyOptions 枚举
ms.date: 03/30/2017
api_name:
- AssemblyOptions
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type:
- apiref
ms.openlocfilehash: 352e1acd1fdd8297754e18b2e8c6448ea723a557
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95717022"
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="b6dae-102">AssemblyOptions 枚举</span><span class="sxs-lookup"><span data-stu-id="b6dae-102">AssemblyOptions Enumeration</span></span>

<span data-ttu-id="b6dae-103">枚举程序集选项。</span><span class="sxs-lookup"><span data-stu-id="b6dae-103">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b6dae-104">语法</span><span class="sxs-lookup"><span data-stu-id="b6dae-104">Syntax</span></span>  
  
```cpp  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="b6dae-105">字段</span><span class="sxs-lookup"><span data-stu-id="b6dae-105">Fields</span></span>  
  
|<span data-ttu-id="b6dae-106">字段</span><span class="sxs-lookup"><span data-stu-id="b6dae-106">Field</span></span>|<span data-ttu-id="b6dae-107">说明</span><span class="sxs-lookup"><span data-stu-id="b6dae-107">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="b6dae-108">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="b6dae-108">optAssemTitle</span></span>|<span data-ttu-id="b6dae-109">String-表示程序集标题。</span><span class="sxs-lookup"><span data-stu-id="b6dae-109">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="b6dae-110">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="b6dae-110">optAssemDescription</span></span>|<span data-ttu-id="b6dae-111">String-包含程序集说明。</span><span class="sxs-lookup"><span data-stu-id="b6dae-111">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="b6dae-112">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="b6dae-112">optAssemConfig</span></span>|<span data-ttu-id="b6dae-113">String-包含程序集配置。</span><span class="sxs-lookup"><span data-stu-id="b6dae-113">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="b6dae-114">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="b6dae-114">optAssemOS</span></span>|<span data-ttu-id="b6dae-115">字符串编码为： "dwOSPlatformId. dwOSMajorVersion. dwOSMinorVersion"。</span><span class="sxs-lookup"><span data-stu-id="b6dae-115">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="b6dae-116">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="b6dae-116">optAssemProcessor</span></span>|<span data-ttu-id="b6dae-117">ULONG</span><span class="sxs-lookup"><span data-stu-id="b6dae-117">ULONG</span></span>|  
|<span data-ttu-id="b6dae-118">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="b6dae-118">optAssemLocale</span></span>|<span data-ttu-id="b6dae-119">String-包含程序集的区域设置。</span><span class="sxs-lookup"><span data-stu-id="b6dae-119">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="b6dae-120">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="b6dae-120">optAssemVersion</span></span>|<span data-ttu-id="b6dae-121">字符串编码为： "主要版本. 次要版本. 内部版本. 修订版本"。</span><span class="sxs-lookup"><span data-stu-id="b6dae-121">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="b6dae-122">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="b6dae-122">optAssemCompany</span></span>|<span data-ttu-id="b6dae-123">String-包含公司。</span><span class="sxs-lookup"><span data-stu-id="b6dae-123">String - Contains the company.</span></span>|  
|<span data-ttu-id="b6dae-124">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="b6dae-124">optAssemProduct</span></span>|<span data-ttu-id="b6dae-125">String-包含产品名称。</span><span class="sxs-lookup"><span data-stu-id="b6dae-125">String - Contains the product name.</span></span>|  
|<span data-ttu-id="b6dae-126">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="b6dae-126">optAssemProductVersion</span></span>|<span data-ttu-id="b6dae-127">String (也称为 InformationalVersion) 。</span><span class="sxs-lookup"><span data-stu-id="b6dae-127">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="b6dae-128">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="b6dae-128">optAssemCopyright</span></span>|<span data-ttu-id="b6dae-129">String-包含版权信息。</span><span class="sxs-lookup"><span data-stu-id="b6dae-129">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="b6dae-130">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="b6dae-130">optAssemTrademark</span></span>|<span data-ttu-id="b6dae-131">String-包含商标信息。</span><span class="sxs-lookup"><span data-stu-id="b6dae-131">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="b6dae-132">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="b6dae-132">optAssemKeyFile</span></span>|<span data-ttu-id="b6dae-133"> (文件名) 字符串。</span><span class="sxs-lookup"><span data-stu-id="b6dae-133">String (file name).</span></span>|  
|<span data-ttu-id="b6dae-134">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="b6dae-134">optAssemKeyName</span></span>|<span data-ttu-id="b6dae-135"> (项名称) 的字符串。</span><span class="sxs-lookup"><span data-stu-id="b6dae-135">String (The key name).</span></span>|  
|<span data-ttu-id="b6dae-136">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="b6dae-136">optAssemAlgID</span></span>|<span data-ttu-id="b6dae-137">ULONG</span><span class="sxs-lookup"><span data-stu-id="b6dae-137">ULONG</span></span>|  
|<span data-ttu-id="b6dae-138">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="b6dae-138">optAssemFlags</span></span>|<span data-ttu-id="b6dae-139">ULONG</span><span class="sxs-lookup"><span data-stu-id="b6dae-139">ULONG</span></span>|  
|<span data-ttu-id="b6dae-140">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="b6dae-140">optAssemHalfSign</span></span>|<span data-ttu-id="b6dae-141">Bool (也称为 DelaySign) 。</span><span class="sxs-lookup"><span data-stu-id="b6dae-141">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="b6dae-142">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="b6dae-142">optAssemFileVersion</span></span>|<span data-ttu-id="b6dae-143">编码为 "ProductVersion" 的字符串，与 "" 相同。</span><span class="sxs-lookup"><span data-stu-id="b6dae-143">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="b6dae-144">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="b6dae-144">optAssemSatelliteVer</span></span>|<span data-ttu-id="b6dae-145">字符串编码为 "主要版本. 次要版本. 内部版本. 内部版本. 修订版本"。</span><span class="sxs-lookup"><span data-stu-id="b6dae-145">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="b6dae-146">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="b6dae-146">optLastAssemOption</span></span>|<span data-ttu-id="b6dae-147">元素数的计数器。</span><span class="sxs-lookup"><span data-stu-id="b6dae-147">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b6dae-148">要求</span><span class="sxs-lookup"><span data-stu-id="b6dae-148">Requirements</span></span>  

 <span data-ttu-id="b6dae-149">**标头：** alink。h</span><span class="sxs-lookup"><span data-stu-id="b6dae-149">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="b6dae-150">**库**： alink.dll</span><span class="sxs-lookup"><span data-stu-id="b6dae-150">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6dae-151">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b6dae-151">See also</span></span>

- [<span data-ttu-id="b6dae-152">Al.exe（程序集链接器）</span><span class="sxs-lookup"><span data-stu-id="b6dae-152">Al.exe (Assembly Linker)</span></span>](../../tools/al-exe-assembly-linker.md)
