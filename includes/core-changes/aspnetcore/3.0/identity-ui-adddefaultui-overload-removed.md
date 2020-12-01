---
ms.openlocfilehash: e77312605ee367c159171e305d8f69429f9ac58b
ms.sourcegitcommit: 0802ac583585110022beb6af8ea0b39188b77c43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "96032278"
---
### <a name="identity-adddefaultui-method-overload-removed"></a><span data-ttu-id="0ba0d-101">标识：已删除 AddDefaultUI 方法重载</span><span class="sxs-lookup"><span data-stu-id="0ba0d-101">Identity: AddDefaultUI method overload removed</span></span>

<span data-ttu-id="0ba0d-102">从 ASP.NET Core 3.0 开始，[IdentityBuilderUIExtensions.AddDefaultUI(IdentityBuilder,UIFramework)](/dotnet/api/microsoft.aspnetcore.identity.identitybuilderuiextensions.adddefaultui?view=aspnetcore-2.2#Microsoft_AspNetCore_Identity_IdentityBuilderUIExtensions_AddDefaultUI_Microsoft_AspNetCore_Identity_IdentityBuilder_Microsoft_AspNetCore_Identity_UI_UIFramework_) 方法重载不再存在。</span><span class="sxs-lookup"><span data-stu-id="0ba0d-102">Starting with ASP.NET Core 3.0, the [IdentityBuilderUIExtensions.AddDefaultUI(IdentityBuilder,UIFramework)](/dotnet/api/microsoft.aspnetcore.identity.identitybuilderuiextensions.adddefaultui?view=aspnetcore-2.2#Microsoft_AspNetCore_Identity_IdentityBuilderUIExtensions_AddDefaultUI_Microsoft_AspNetCore_Identity_IdentityBuilder_Microsoft_AspNetCore_Identity_UI_UIFramework_) method overload no longer exists.</span></span>

#### <a name="version-introduced"></a><span data-ttu-id="0ba0d-103">引入的版本</span><span class="sxs-lookup"><span data-stu-id="0ba0d-103">Version introduced</span></span>

<span data-ttu-id="0ba0d-104">3.0</span><span class="sxs-lookup"><span data-stu-id="0ba0d-104">3.0</span></span>

#### <a name="reason-for-change"></a><span data-ttu-id="0ba0d-105">更改原因</span><span class="sxs-lookup"><span data-stu-id="0ba0d-105">Reason for change</span></span>

<span data-ttu-id="0ba0d-106">此更改是采用静态 Web 资产功能的结果。</span><span class="sxs-lookup"><span data-stu-id="0ba0d-106">This change was a result of adoption of the static web assets feature.</span></span>

#### <a name="recommended-action"></a><span data-ttu-id="0ba0d-107">建议操作</span><span class="sxs-lookup"><span data-stu-id="0ba0d-107">Recommended action</span></span>

<span data-ttu-id="0ba0d-108">调用 <xref:Microsoft.AspNetCore.Identity.IdentityBuilderUIExtensions.AddDefaultUI(Microsoft.AspNetCore.Identity.IdentityBuilder)?displayProperty=nameWithType> 而不是使用两个参数的重载。</span><span class="sxs-lookup"><span data-stu-id="0ba0d-108">Call <xref:Microsoft.AspNetCore.Identity.IdentityBuilderUIExtensions.AddDefaultUI(Microsoft.AspNetCore.Identity.IdentityBuilder)?displayProperty=nameWithType> instead of the overload that takes two arguments.</span></span> <span data-ttu-id="0ba0d-109">如果使用的是 Bootstrap 3，还应将以下行添加到项目文件中的 `<PropertyGroup>` 元素：</span><span class="sxs-lookup"><span data-stu-id="0ba0d-109">If you're using Bootstrap 3, also add the following line to a `<PropertyGroup>` element in your project file:</span></span>

```xml
<IdentityUIFrameworkVersion>Bootstrap3</IdentityUIFrameworkVersion>
```

#### <a name="category"></a><span data-ttu-id="0ba0d-110">类别</span><span class="sxs-lookup"><span data-stu-id="0ba0d-110">Category</span></span>

<span data-ttu-id="0ba0d-111">ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="0ba0d-111">ASP.NET Core</span></span>

#### <a name="affected-apis"></a><span data-ttu-id="0ba0d-112">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="0ba0d-112">Affected APIs</span></span>

[<span data-ttu-id="0ba0d-113">IdentityBuilderUIExtensions.AddDefaultUI(IdentityBuilder,UIFramework)</span><span class="sxs-lookup"><span data-stu-id="0ba0d-113">IdentityBuilderUIExtensions.AddDefaultUI(IdentityBuilder,UIFramework)</span></span>](/dotnet/api/microsoft.aspnetcore.identity.identitybuilderuiextensions.adddefaultui?view=aspnetcore-2.2#Microsoft_AspNetCore_Identity_IdentityBuilderUIExtensions_AddDefaultUI_Microsoft_AspNetCore_Identity_IdentityBuilder_Microsoft_AspNetCore_Identity_UI_UIFramework_)

<!--

#### Affected APIs

`M:Microsoft.AspNetCore.Identity.IdentityBuilderUIExtensions.AddDefaultUI(Microsoft.AspNetCore.Identity.IdentityBuilder,Microsoft.AspNetCore.Identity.UI.UIFramework)`

-->
