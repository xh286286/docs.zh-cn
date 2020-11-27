---
title: ServiceCredentials
ms.date: 03/30/2017
ms.assetid: 9c780793-4785-46f7-add9-ac1ebeadb614
ms.openlocfilehash: d7e89acedc8fc1004b0198172e58813944df85f3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96262302"
---
# <a name="servicecredentials"></a><span data-ttu-id="53638-102">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="53638-102">ServiceCredentials</span></span>

<span data-ttu-id="53638-103">ServiceCredentials</span><span class="sxs-lookup"><span data-stu-id="53638-103">ServiceCredentials</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="53638-104">语法</span><span class="sxs-lookup"><span data-stu-id="53638-104">Syntax</span></span>  
  
```csharp
class ServiceCredentials : Behavior  
{  
  string ClientCertificate;  
  string IssuedTokenAuthentication;  
  string Peer;  
  string SecureConversationAuthentication;  
  string ServiceCertificate;  
  string UserNameAuthentication;  
  string WindowsAuthentication;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="53638-105">方法</span><span class="sxs-lookup"><span data-stu-id="53638-105">Methods</span></span>  

 <span data-ttu-id="53638-106">ServiceCredentials 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="53638-106">The ServiceCredentials class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="53638-107">属性</span><span class="sxs-lookup"><span data-stu-id="53638-107">Properties</span></span>  

 <span data-ttu-id="53638-108">ServiceCredentials 类具有下列属性：</span><span class="sxs-lookup"><span data-stu-id="53638-108">The ServiceCredentials class has the following properties:</span></span>  
  
### <a name="clientcertificate"></a><span data-ttu-id="53638-109">ClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53638-109">ClientCertificate</span></span>  

 <span data-ttu-id="53638-110">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-110">Data type: string</span></span>  
  
 <span data-ttu-id="53638-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-112">此服务的客户端证书身份验证和配置设置。</span><span class="sxs-lookup"><span data-stu-id="53638-112">The client certificate authentication and provisioning settings for this service.</span></span>  
  
### <a name="issuedtokenauthentication"></a><span data-ttu-id="53638-113">IssuedTokenAuthentication</span><span class="sxs-lookup"><span data-stu-id="53638-113">IssuedTokenAuthentication</span></span>  

 <span data-ttu-id="53638-114">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-114">Data type: string</span></span>  
  
 <span data-ttu-id="53638-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-116">当前颁发的此服务的令牌身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="53638-116">The current issued token authentication settings for this service.</span></span>  
  
### <a name="peer"></a><span data-ttu-id="53638-117">对等</span><span class="sxs-lookup"><span data-stu-id="53638-117">Peer</span></span>  

 <span data-ttu-id="53638-118">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-118">Data type: string</span></span>  
  
 <span data-ttu-id="53638-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-120">对等传输终结点要使用的当前凭据身份验证和配置设置。</span><span class="sxs-lookup"><span data-stu-id="53638-120">The current credential authentication and provisioning settings to be used by peer transport endpoints.</span></span>  
  
### <a name="secureconversationauthentication"></a><span data-ttu-id="53638-121">SecureConversationAuthentication</span><span class="sxs-lookup"><span data-stu-id="53638-121">SecureConversationAuthentication</span></span>  

 <span data-ttu-id="53638-122">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-122">Data type: string</span></span>  
  
 <span data-ttu-id="53638-123">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-123">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-124">指定当前安全对话设置。</span><span class="sxs-lookup"><span data-stu-id="53638-124">Specifies the current secure conversation settings.</span></span>  
  
### <a name="servicecertificate"></a><span data-ttu-id="53638-125">ServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="53638-125">ServiceCertificate</span></span>  

 <span data-ttu-id="53638-126">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-126">Data type: string</span></span>  
  
 <span data-ttu-id="53638-127">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-127">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-128">与此服务关联的证书。</span><span class="sxs-lookup"><span data-stu-id="53638-128">The certificate associated with this service.</span></span>  
  
### <a name="usernameauthentication"></a><span data-ttu-id="53638-129">UserNameAuthentication</span><span class="sxs-lookup"><span data-stu-id="53638-129">UserNameAuthentication</span></span>  

 <span data-ttu-id="53638-130">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-130">Data type: string</span></span>  
  
 <span data-ttu-id="53638-131">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-131">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-132">此服务的用户名/密码设置。</span><span class="sxs-lookup"><span data-stu-id="53638-132">The username/password settings for this service.</span></span>  
  
### <a name="windowsauthentication"></a><span data-ttu-id="53638-133">WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="53638-133">WindowsAuthentication</span></span>  

 <span data-ttu-id="53638-134">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="53638-134">Data type: string</span></span>  
  
 <span data-ttu-id="53638-135">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="53638-135">Access type: Read-only</span></span>  
  
 <span data-ttu-id="53638-136">此服务的 Windows 身份验证设置。</span><span class="sxs-lookup"><span data-stu-id="53638-136">The Windows authentication settings for this service.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="53638-137">要求</span><span class="sxs-lookup"><span data-stu-id="53638-137">Requirements</span></span>  
  
|<span data-ttu-id="53638-138">MOF</span><span class="sxs-lookup"><span data-stu-id="53638-138">MOF</span></span>|<span data-ttu-id="53638-139">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="53638-139">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="53638-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="53638-140">Namespace</span></span>|<span data-ttu-id="53638-141">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="53638-141">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="53638-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="53638-142">See also</span></span>

- <xref:System.ServiceModel.Description.ServiceCredentials>
