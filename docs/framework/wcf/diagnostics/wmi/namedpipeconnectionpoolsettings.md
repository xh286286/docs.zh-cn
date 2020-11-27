---
title: NamedPipeConnectionPoolSettings
ms.date: 03/30/2017
ms.assetid: 079bccb8-54b5-4436-a43d-5567763f72ce
ms.openlocfilehash: 8422e1adf9a8914b631431eba5c9c0ed058cd0f3
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96258018"
---
# <a name="namedpipeconnectionpoolsettings"></a><span data-ttu-id="0f3fe-102">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="0f3fe-102">NamedPipeConnectionPoolSettings</span></span>

<span data-ttu-id="0f3fe-103">NamedPipeConnectionPoolSettings</span><span class="sxs-lookup"><span data-stu-id="0f3fe-103">NamedPipeConnectionPoolSettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0f3fe-104">语法</span><span class="sxs-lookup"><span data-stu-id="0f3fe-104">Syntax</span></span>  
  
```csharp
class NamedPipeConnectionPoolSettings  
{  
  string GroupName;  
  datetime IdleTimeout;  
  sint32 MaxOutboundConnectionsPerEndpoint;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="0f3fe-105">方法</span><span class="sxs-lookup"><span data-stu-id="0f3fe-105">Methods</span></span>  

 <span data-ttu-id="0f3fe-106">NamedPipeConnectionPoolSettings 类不定义任何方法。</span><span class="sxs-lookup"><span data-stu-id="0f3fe-106">The NamedPipeConnectionPoolSettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="0f3fe-107">属性</span><span class="sxs-lookup"><span data-stu-id="0f3fe-107">Properties</span></span>  

 <span data-ttu-id="0f3fe-108">NamedPipeConnectionPoolSettings 类具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="0f3fe-108">The NamedPipeConnectionPoolSettings class has the following properties:</span></span>  
  
### <a name="groupname"></a><span data-ttu-id="0f3fe-109">GroupName</span><span class="sxs-lookup"><span data-stu-id="0f3fe-109">GroupName</span></span>  

 <span data-ttu-id="0f3fe-110">数据类型：字符串</span><span class="sxs-lookup"><span data-stu-id="0f3fe-110">Data type: string</span></span>  
  
 <span data-ttu-id="0f3fe-111">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0f3fe-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0f3fe-112">绑定元素使用的连接池的组名。</span><span class="sxs-lookup"><span data-stu-id="0f3fe-112">The group name of the connection pool used by the binding element.</span></span>  
  
### <a name="idletimeout"></a><span data-ttu-id="0f3fe-113">IdleTimeout</span><span class="sxs-lookup"><span data-stu-id="0f3fe-113">IdleTimeout</span></span>  

 <span data-ttu-id="0f3fe-114">数据类型：DateTime</span><span class="sxs-lookup"><span data-stu-id="0f3fe-114">Data type: datetime</span></span>  
  
 <span data-ttu-id="0f3fe-115">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0f3fe-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0f3fe-116">连接在断开前可以空闲的最长时间。</span><span class="sxs-lookup"><span data-stu-id="0f3fe-116">The maximum time the connection can be idle before being disconnected.</span></span>  
  
### <a name="maxoutboundconnectionsperendpoint"></a><span data-ttu-id="0f3fe-117">MaxOutboundConnectionsPerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f3fe-117">MaxOutboundConnectionsPerEndpoint</span></span>  

 <span data-ttu-id="0f3fe-118">数据类型：sint32</span><span class="sxs-lookup"><span data-stu-id="0f3fe-118">Data type: sint32</span></span>  
  
 <span data-ttu-id="0f3fe-119">访问类型：只读</span><span class="sxs-lookup"><span data-stu-id="0f3fe-119">Access type: Read-only</span></span>  
  
 <span data-ttu-id="0f3fe-120">客户端上每个终结点的最大出站连接数。</span><span class="sxs-lookup"><span data-stu-id="0f3fe-120">The maximum number of outbound connections for each endpoint on the client.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0f3fe-121">要求</span><span class="sxs-lookup"><span data-stu-id="0f3fe-121">Requirements</span></span>  
  
|<span data-ttu-id="0f3fe-122">MOF</span><span class="sxs-lookup"><span data-stu-id="0f3fe-122">MOF</span></span>|<span data-ttu-id="0f3fe-123">已在 Servicemodel.mof 中声明。</span><span class="sxs-lookup"><span data-stu-id="0f3fe-123">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="0f3fe-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="0f3fe-124">Namespace</span></span>|<span data-ttu-id="0f3fe-125">已在 root\ServiceModel 中定义</span><span class="sxs-lookup"><span data-stu-id="0f3fe-125">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0f3fe-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f3fe-126">See also</span></span>

- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
