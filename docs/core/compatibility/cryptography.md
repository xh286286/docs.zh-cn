---
title: 加密中断性变更
description: 列出 .NET Core 2.1-3.0 中与加密相关的中断性变更。
ms.date: 04/22/2020
ms.openlocfilehash: a4801bb4d5a859e2c8c2b536ee0597cb4db2f65d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95682648"
---
# <a name="cryptography-breaking-changes-for-net-core-21-30"></a><span data-ttu-id="ce26f-103">.NET Core 2.1-3.0 的加密中断性变更</span><span class="sxs-lookup"><span data-stu-id="ce26f-103">Cryptography breaking changes for .NET Core 2.1-3.0</span></span>

<span data-ttu-id="ce26f-104">本页记录了以下中断性变更：</span><span class="sxs-lookup"><span data-stu-id="ce26f-104">The following breaking changes are documented on this page:</span></span>

| <span data-ttu-id="ce26f-105">重大更改</span><span class="sxs-lookup"><span data-stu-id="ce26f-105">Breaking change</span></span> | <span data-ttu-id="ce26f-106">引入的版本</span><span class="sxs-lookup"><span data-stu-id="ce26f-106">Version introduced</span></span> |
| - | :-: |
| [<span data-ttu-id="ce26f-107">Linux 不再支持 BEGIN TRUSTED CERTIFICATE 语法</span><span class="sxs-lookup"><span data-stu-id="ce26f-107">BEGIN TRUSTED CERTIFICATE syntax no longer supported on Linux</span></span>](#begin-trusted-certificate-syntax-no-longer-supported-for-root-certificates-on-linux) | <span data-ttu-id="ce26f-108">3.0</span><span class="sxs-lookup"><span data-stu-id="ce26f-108">3.0</span></span> |
| [<span data-ttu-id="ce26f-109">EnvelopedCms 默认为 AES-256 加密</span><span class="sxs-lookup"><span data-stu-id="ce26f-109">EnvelopedCms defaults to AES-256 encryption</span></span>](#envelopedcms-defaults-to-aes-256-encryption) | <span data-ttu-id="ce26f-110">3.0</span><span class="sxs-lookup"><span data-stu-id="ce26f-110">3.0</span></span> |
| [<span data-ttu-id="ce26f-111">RSAOpenSsl 密钥生成的最小大小已增加</span><span class="sxs-lookup"><span data-stu-id="ce26f-111">Minimum size for RSAOpenSsl key generation has increased</span></span>](#minimum-size-for-rsaopenssl-key-generation-has-increased) | <span data-ttu-id="ce26f-112">3.0</span><span class="sxs-lookup"><span data-stu-id="ce26f-112">3.0</span></span> |
| [<span data-ttu-id="ce26f-113">.NET Core 3.0 倾向于使用 OpenSSL 1.1.x 而不是 OpenSSL 1.0.x</span><span class="sxs-lookup"><span data-stu-id="ce26f-113">.NET Core 3.0 prefers OpenSSL 1.1.x to OpenSSL 1.0.x</span></span>](#net-core-30-prefers-openssl-11x-to-openssl-10x) | <span data-ttu-id="ce26f-114">3.0</span><span class="sxs-lookup"><span data-stu-id="ce26f-114">3.0</span></span> |
| [<span data-ttu-id="ce26f-115">CryptoStream.Dispose 仅在写入时转换最终块</span><span class="sxs-lookup"><span data-stu-id="ce26f-115">CryptoStream.Dispose transforms final block only when writing</span></span>](#cryptostreamdispose-transforms-final-block-only-when-writing) | <span data-ttu-id="ce26f-116">3.0</span><span class="sxs-lookup"><span data-stu-id="ce26f-116">3.0</span></span> |
| [<span data-ttu-id="ce26f-117">已考虑 SignedCms.ComputeSignature 的布尔参数</span><span class="sxs-lookup"><span data-stu-id="ce26f-117">Boolean parameter of SignedCms.ComputeSignature is respected</span></span>](#boolean-parameter-of-signedcmscomputesignature-is-respected) | <span data-ttu-id="ce26f-118">2.1</span><span class="sxs-lookup"><span data-stu-id="ce26f-118">2.1</span></span> |

## <a name="net-core-30"></a><span data-ttu-id="ce26f-119">.NET Core 3.0</span><span class="sxs-lookup"><span data-stu-id="ce26f-119">.NET Core 3.0</span></span>

[!INCLUDE [begin-trusted-cert-linux](~/includes/core-changes/cryptography/3.0/begin-trusted-cert-linux.md)]

***

[!INCLUDE[EnvelopedCms defaults to AES-256 encryption](~/includes/core-changes/cryptography/3.0/envelopedcms-defaults-to-aes256.md)]

<span data-ttu-id="ce26f-120">\*\*_</span><span class="sxs-lookup"><span data-stu-id="ce26f-120">\*\*_</span></span>

[!INCLUDE[Minimum size for RSAOpenSsl key generation has increased](~/includes/core-changes/cryptography/3.0/minimum-rsaopenssl-key-size-change.md)]

_*_

[!INCLUDE[.NET Core 3.0 prefers OpenSSL 1.1.x to OpenSSL 1.0.x](~/includes/core-changes/cryptography/3.0/net-core-3-0-prefers-openssl-1-1-x.md)]

_*_

[!INCLUDE [CryptoStream.Dispose transforms final block only when writing](~/includes/core-changes/cryptography/3.0/cryptography-cryptostream-dispose-final-block-write.md)]

_*_

## <a name="net-core-21"></a><span data-ttu-id="ce26f-121">.NET Core 2.1</span><span class="sxs-lookup"><span data-stu-id="ce26f-121">.NET Core 2.1</span></span>

[!INCLUDE [Boolean parameter of SignedCms.ComputeSignature is respected](~/includes/core-changes/cryptography/2.1/compute-signature-silent-parameter.md)]

<span data-ttu-id="ce26f-122">_\*\*</span><span class="sxs-lookup"><span data-stu-id="ce26f-122">_\*\*</span></span>
