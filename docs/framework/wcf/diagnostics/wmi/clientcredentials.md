---
title: ClientCredentials
ms.date: 03/30/2017
ms.assetid: 41dffd6b-8f14-4fed-aefb-2a1bb168efb3
ms.openlocfilehash: c63e1b3de464b306f46e2f0935b1208d7262925a
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96274187"
---
# <a name="clientcredentials"></a><span data-ttu-id="3a301-102">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="3a301-102">ClientCredentials</span></span>

<span data-ttu-id="3a301-103">ClientCredentials</span><span class="sxs-lookup"><span data-stu-id="3a301-103">ClientCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3a301-104">语法</span><span class="sxs-lookup"><span data-stu-id="3a301-104">Syntax</span></span>  
  
```csharp
class ClientCredentials : Behavior  
{  
  string ClientCertificate;  
  string HttpDigest;  
  string IssuedToken;  
  string Peer;  
  string ServiceCertificate;  
  boolean SupportInteractive;  
  string UserName;  
  string Windows;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="3a301-105">方法</span><span class="sxs-lookup"><span data-stu-id="3a301-105">Methods</span></span>  

 <span data-ttu-id="3a301-106">ClientCredentials 类未定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="3a301-106">The ClientCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="3a301-107">属性</span><span class="sxs-lookup"><span data-stu-id="3a301-107">Properties</span></span>  

 <span data-ttu-id="3a301-108">ClientCredentials 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="3a301-108">The ClientCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="3a301-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3a301-109">ClientCertificate</span></span>  

 <span data-ttu-id="3a301-110">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-110">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-112">客户端用来向服务验证身份的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="3a301-112">The X.509 certificate the client uses to authenticate to the service.</span></span>  
  
### <a name="httpdigest"></a><span data-ttu-id="3a301-113">HttpDigest</span><span class="sxs-lookup"><span data-stu-id="3a301-113">HttpDigest</span></span>  

 <span data-ttu-id="3a301-114">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-114">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-116">当前 Http Digest 凭据。</span><span class="sxs-lookup"><span data-stu-id="3a301-116">The current Http Digest credential.</span></span>  
  
### <a name="issuedtoken"></a><span data-ttu-id="3a301-117">IssuedToken</span><span class="sxs-lookup"><span data-stu-id="3a301-117">IssuedToken</span></span>  

 <span data-ttu-id="3a301-118">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-118">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-120">用于联系本地安全令牌服务的终结点地址和绑定。</span><span class="sxs-lookup"><span data-stu-id="3a301-120">The endpoint address and binding used to contact the local security token service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="3a301-121">对等</span><span class="sxs-lookup"><span data-stu-id="3a301-121">Peer</span></span>  

 <span data-ttu-id="3a301-122">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-122">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-123">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-124">对等节点用来向网格中的其他节点验证其自身身份的凭据。</span><span class="sxs-lookup"><span data-stu-id="3a301-124">The credentials that the peer node uses to authenticate itself to other nodes in the mesh.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="3a301-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="3a301-125">ServiceCertificate</span></span>  

 <span data-ttu-id="3a301-126">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-126">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-127">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-128">服务的 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="3a301-128">The service's X.509 certificate.</span></span>  
  
### <a name="supportinteractive"></a><span data-ttu-id="3a301-129">SupportInteractive</span><span class="sxs-lookup"><span data-stu-id="3a301-129">SupportInteractive</span></span>  

 <span data-ttu-id="3a301-130">数据类型：Boolean</span><span class="sxs-lookup"><span data-stu-id="3a301-130">Data type: boolean</span></span>  
  
 <span data-ttu-id="3a301-131">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-132">一个布尔值，指定凭据是否支持交互式协商。</span><span class="sxs-lookup"><span data-stu-id="3a301-132">A Boolean value that specifies whether the credential supports interactive negotiation.</span></span>  
  
### <a name="username"></a><span data-ttu-id="3a301-133">UserName</span><span class="sxs-lookup"><span data-stu-id="3a301-133">UserName</span></span>  

 <span data-ttu-id="3a301-134">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-134">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-135">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-136">客户端用来向服务验证其自身身份的用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="3a301-136">The username and password the client uses to authenticate itself to the service.</span></span>  
  
### <a name="windows"></a><span data-ttu-id="3a301-137">Windows</span><span class="sxs-lookup"><span data-stu-id="3a301-137">Windows</span></span>  

 <span data-ttu-id="3a301-138">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="3a301-138">Data type: string</span></span>  
  
 <span data-ttu-id="3a301-139">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="3a301-139">Access type: Read-only</span></span>  
  
 <span data-ttu-id="3a301-140">客户端用来向服务验证其自身身份的 Windows 凭据。</span><span class="sxs-lookup"><span data-stu-id="3a301-140">The windows credentials the client uses to authenticate itself to the service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3a301-141">要求</span><span class="sxs-lookup"><span data-stu-id="3a301-141">Requirements</span></span>  
  
|<span data-ttu-id="3a301-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3a301-142">MOF</span></span>|<span data-ttu-id="3a301-143">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="3a301-143">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="3a301-144">命名空间</span><span class="sxs-lookup"><span data-stu-id="3a301-144">Namespace</span></span>|<span data-ttu-id="3a301-145">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="3a301-145">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3a301-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3a301-146">See also</span></span>

- <xref:System.ServiceModel.Description.ClientCredentials>
