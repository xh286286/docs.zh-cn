---
title: GetRequestedRuntimeInfo 函数
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeInfo
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeInfo
helpviewer_keywords:
- GetRequestedRuntimeInfo function [.NET Framework hosting]
ms.assetid: 0dfd7cdc-c116-4e25-b56a-ac7b0378c942
topic_type:
- apiref
ms.openlocfilehash: b120b854e1787824808dd64d95b0fa78ba6c9fa2
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95705483"
---
# <a name="getrequestedruntimeinfo-function"></a><span data-ttu-id="3a0de-102">GetRequestedRuntimeInfo 函数</span><span class="sxs-lookup"><span data-stu-id="3a0de-102">GetRequestedRuntimeInfo Function</span></span>

<span data-ttu-id="3a0de-103">获取有关应用程序请求的公共语言运行时 (CLR) 的版本和目录信息。</span><span class="sxs-lookup"><span data-stu-id="3a0de-103">Gets version and directory information about the common language runtime (CLR) requested by an application.</span></span>  
  
 <span data-ttu-id="3a0de-104">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="3a0de-104">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a0de-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a0de-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRequestedRuntimeInfo (  
    [in]  LPCWSTR  pExe,
    [in]  LPCWSTR  pwszVersion,
    [in]  LPCWSTR  pConfigurationFile,
    [in]  DWORD    startupFlags,
    [in]  DWORD    runtimeInfoFlags,
    [out] LPWSTR   pDirectory,
    [in]  DWORD    dwDirectory,
    [out] DWORD   *dwDirectoryLength,
    [out] LPWSTR   pVersion,
    [in]  DWORD    cchBuffer,
    [out] DWORD   *dwlength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3a0de-106">参数</span><span class="sxs-lookup"><span data-stu-id="3a0de-106">Parameters</span></span>  

 `pExe`  
 <span data-ttu-id="3a0de-107">中应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="3a0de-107">[in] The name of the application.</span></span>  
  
 `pwszVersion`  
 <span data-ttu-id="3a0de-108">中一个字符串，指定运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="3a0de-108">[in] A string specifying the version number of the runtime.</span></span>  
  
 `pConfigurationFile`  
 <span data-ttu-id="3a0de-109">中与相关联的配置文件的名称 `pExe` 。</span><span class="sxs-lookup"><span data-stu-id="3a0de-109">[in] The name of the configuration file that is associated with `pExe`.</span></span>  
  
 `startupFlags`  
 <span data-ttu-id="3a0de-110">中一个或多个 [STARTUP_FLAGS](startup-flags-enumeration.md) 枚举值。</span><span class="sxs-lookup"><span data-stu-id="3a0de-110">[in] One or more of the [STARTUP_FLAGS](startup-flags-enumeration.md) enumeration values.</span></span>  
  
 `runtimeInfoFlags`  
 <span data-ttu-id="3a0de-111">中一个或多个 [RUNTIME_INFO_FLAGS](runtime-info-flags-enumeration.md) 枚举值。</span><span class="sxs-lookup"><span data-stu-id="3a0de-111">[in] One or more of the [RUNTIME_INFO_FLAGS](runtime-info-flags-enumeration.md) enumeration values.</span></span>  
  
 `pDirectory`  
 <span data-ttu-id="3a0de-112">弄一个缓冲区，其中包含成功完成后运行时的目录路径。</span><span class="sxs-lookup"><span data-stu-id="3a0de-112">[out] A buffer that contains the directory path to the runtime upon successful completion.</span></span>  
  
 `dwDirectory`  
 <span data-ttu-id="3a0de-113">中目录缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="3a0de-113">[in] The length of the directory buffer.</span></span>  
  
 `dwDirectoryLength`  
 <span data-ttu-id="3a0de-114">弄指向目录路径字符串长度的指针。</span><span class="sxs-lookup"><span data-stu-id="3a0de-114">[out] A pointer to the length of the directory path string.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="3a0de-115">弄一个缓冲区，其中包含成功完成后运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="3a0de-115">[out] A buffer that contains the version number of the runtime upon successful completion.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="3a0de-116">中版本字符串缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="3a0de-116">[in] The length of the version string buffer.</span></span>  
  
 `dwlength`  
 <span data-ttu-id="3a0de-117">弄指向版本字符串长度的指针。</span><span class="sxs-lookup"><span data-stu-id="3a0de-117">[out] A pointer to the length of the version string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3a0de-118">返回值</span><span class="sxs-lookup"><span data-stu-id="3a0de-118">Return Value</span></span>  

 <span data-ttu-id="3a0de-119">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="3a0de-119">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="3a0de-120">返回代码</span><span class="sxs-lookup"><span data-stu-id="3a0de-120">Return code</span></span>|<span data-ttu-id="3a0de-121">说明</span><span class="sxs-lookup"><span data-stu-id="3a0de-121">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="3a0de-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="3a0de-122">S_OK</span></span>|<span data-ttu-id="3a0de-123">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="3a0de-123">The method completed successfully.</span></span>|  
|<span data-ttu-id="3a0de-124">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="3a0de-124">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="3a0de-125">目录缓冲区不够大，无法存储目录路径。</span><span class="sxs-lookup"><span data-stu-id="3a0de-125">The directory buffer is not large enough to store the directory path.</span></span><br /><br /> <span data-ttu-id="3a0de-126">- 或 -</span><span class="sxs-lookup"><span data-stu-id="3a0de-126">- or -</span></span><br /><br /> <span data-ttu-id="3a0de-127">版本缓冲区不够大，无法存储版本字符串。</span><span class="sxs-lookup"><span data-stu-id="3a0de-127">The version buffer is not large enough to store the version string.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3a0de-128">注解</span><span class="sxs-lookup"><span data-stu-id="3a0de-128">Remarks</span></span>  

 <span data-ttu-id="3a0de-129">`GetRequestedRuntimeInfo`方法返回有关加载到进程中的版本的运行时信息，这不一定是计算机上安装的最新版本。</span><span class="sxs-lookup"><span data-stu-id="3a0de-129">The `GetRequestedRuntimeInfo` method returns run-time information about the version loaded into the process, which is not necessarily the latest version installed on the computer.</span></span>  
  
 <span data-ttu-id="3a0de-130">在 .NET Framework 版本2.0 中，可以通过使用方法获取有关最新安装的版本的信息，如下所示 `GetRequestedRuntimeInfo` ：</span><span class="sxs-lookup"><span data-stu-id="3a0de-130">In the .NET Framework version 2.0, you can get information about the latest installed version by using the `GetRequestedRuntimeInfo` method as follows:</span></span>  
  
- <span data-ttu-id="3a0de-131">将 `pExe` 、 `pwszVersion` 和参数指定 `pConfigurationFile` 为 null。</span><span class="sxs-lookup"><span data-stu-id="3a0de-131">Specify the `pExe`, `pwszVersion`, and `pConfigurationFile` parameters as null.</span></span>  
  
- <span data-ttu-id="3a0de-132">指定参数的枚举中的 RUNTIME_INFO_UPGRADE_VERSION 标志 `RUNTIME_INFO_FLAGS` `runtimeInfoFlags` 。</span><span class="sxs-lookup"><span data-stu-id="3a0de-132">Specify the RUNTIME_INFO_UPGRADE_VERSION flag in the `RUNTIME_INFO_FLAGS` enumerations for the `runtimeInfoFlags` parameter.</span></span>  
  
 <span data-ttu-id="3a0de-133">此 `GetRequestedRuntimeInfo` 方法在以下情况下不会返回最新的 CLR 版本：</span><span class="sxs-lookup"><span data-stu-id="3a0de-133">The `GetRequestedRuntimeInfo` method does not return the latest CLR version in the following circumstances:</span></span>  
  
- <span data-ttu-id="3a0de-134">指定加载特定 CLR 版本的应用程序配置文件存在。</span><span class="sxs-lookup"><span data-stu-id="3a0de-134">An application configuration file that specifies loading a particular CLR version exists.</span></span> <span data-ttu-id="3a0de-135">请注意，.NET Framework 将使用配置文件，即使为参数指定 null 也是如此 `pConfigurationFile` 。</span><span class="sxs-lookup"><span data-stu-id="3a0de-135">Note that the .NET Framework will use the configuration file even if you specify null for the `pConfigurationFile` parameter.</span></span>  
  
- <span data-ttu-id="3a0de-136">将 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 方法指定为指定较早的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="3a0de-136">The [CorBindToRuntimeEx](corbindtoruntimeex-function.md) method was called specifying an earlier CLR version.</span></span>  
  
- <span data-ttu-id="3a0de-137">为早期 CLR 版本编译的应用程序当前正在运行。</span><span class="sxs-lookup"><span data-stu-id="3a0de-137">An application that was compiled for an earlier CLR version is currently running.</span></span>  
  
 <span data-ttu-id="3a0de-138">对于 `runtimeInfoFlags` 参数，可以一次仅指定枚举的一个体系结构常量 `RUNTIME_INFO_FLAGS` ：</span><span class="sxs-lookup"><span data-stu-id="3a0de-138">For the `runtimeInfoFlags` parameter, you can specify only one of the architecture constants of the `RUNTIME_INFO_FLAGS` enumeration at a time:</span></span>  
  
- <span data-ttu-id="3a0de-139">RUNTIME_INFO_REQUEST_IA64</span><span class="sxs-lookup"><span data-stu-id="3a0de-139">RUNTIME_INFO_REQUEST_IA64</span></span>  
  
- <span data-ttu-id="3a0de-140">RUNTIME_INFO_REQUEST_AMD64</span><span class="sxs-lookup"><span data-stu-id="3a0de-140">RUNTIME_INFO_REQUEST_AMD64</span></span>  
  
- <span data-ttu-id="3a0de-141">RUNTIME_INFO_REQUEST_X86</span><span class="sxs-lookup"><span data-stu-id="3a0de-141">RUNTIME_INFO_REQUEST_X86</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a0de-142">要求</span><span class="sxs-lookup"><span data-stu-id="3a0de-142">Requirements</span></span>  

 <span data-ttu-id="3a0de-143">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3a0de-143">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3a0de-144">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3a0de-144">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3a0de-145">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3a0de-145">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3a0de-146">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3a0de-146">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a0de-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a0de-147">See also</span></span>

- [<span data-ttu-id="3a0de-148">GetRequestedRuntimeVersion 函数</span><span class="sxs-lookup"><span data-stu-id="3a0de-148">GetRequestedRuntimeVersion Function</span></span>](getrequestedruntimeversion-function.md)
- [<span data-ttu-id="3a0de-149">GetVersionFromProcess 函数</span><span class="sxs-lookup"><span data-stu-id="3a0de-149">GetVersionFromProcess Function</span></span>](getversionfromprocess-function.md)
- [<span data-ttu-id="3a0de-150">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="3a0de-150">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
