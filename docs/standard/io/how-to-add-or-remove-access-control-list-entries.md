---
title: 如何：添加或删除访问控制列表条目（仅限 .NET Framework）
ms.date: 01/14/2019
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ACEs [.NET Framework]
- ACLs [.NET Framework]
- access control entries [.NET Framework]
- I/O [.NET Framework], access control list entries
- access control lists [.NET Framework]
ms.assetid: 53758b39-bd9b-4640-bb04-cad5ed8d0abf
ms.openlocfilehash: 53daa88b761f46dab26b1c12c73741e880512d8d
ms.sourcegitcommit: d8020797a6657d0fbbdff362b80300815f682f94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/24/2020
ms.locfileid: "95682687"
---
# <a name="how-to-add-or-remove-access-control-list-entries-net-framework-only"></a><span data-ttu-id="4f650-102">如何：添加或删除访问控制列表条目（仅限 .NET Framework）</span><span class="sxs-lookup"><span data-stu-id="4f650-102">How to: Add or remove Access Control List entries (.NET Framework only)</span></span>

<span data-ttu-id="4f650-103">若要向文件或目录添加或从文件或目录删除访问控制列表 (ACL) 条目，请从文件或目录获取 <xref:System.Security.AccessControl.FileSecurity> 或 <xref:System.Security.AccessControl.DirectorySecurity> 对象。</span><span class="sxs-lookup"><span data-stu-id="4f650-103">To add or remove Access Control List (ACL) entries to or from a file or directory, get the <xref:System.Security.AccessControl.FileSecurity> or <xref:System.Security.AccessControl.DirectorySecurity> object from the file or directory.</span></span> <span data-ttu-id="4f650-104">修改对象，然后将其应用回文件或目录。</span><span class="sxs-lookup"><span data-stu-id="4f650-104">Modify the object, and then apply it back to the file or directory.</span></span>  
  
## <a name="add-or-remove-an-acl-entry-from-a-file"></a><span data-ttu-id="4f650-105">添加或从文件中删除 ACL 条目</span><span class="sxs-lookup"><span data-stu-id="4f650-105">Add or remove an ACL entry from a file</span></span>  
  
1. <span data-ttu-id="4f650-106">调用 <xref:System.IO.File.GetAccessControl%2A?displayProperty=nameWithType> 方法以获取 <xref:System.Security.AccessControl.FileSecurity> 对象，该对象包含文件的当前 ACL 条目。</span><span class="sxs-lookup"><span data-stu-id="4f650-106">Call the <xref:System.IO.File.GetAccessControl%2A?displayProperty=nameWithType> method to get a <xref:System.Security.AccessControl.FileSecurity> object that contains the current ACL entries of a file.</span></span>  
  
2. <span data-ttu-id="4f650-107">添加或从步骤 1 返回的 <xref:System.Security.AccessControl.FileSecurity> 对象中删除 ACL 条目。</span><span class="sxs-lookup"><span data-stu-id="4f650-107">Add or remove ACL entries from the <xref:System.Security.AccessControl.FileSecurity> object returned from step 1.</span></span>  
  
3. <span data-ttu-id="4f650-108">将 <xref:System.Security.AccessControl.FileSecurity> 对象传递给 <xref:System.IO.File.SetAccessControl%2A?displayProperty=nameWithType> 方法以应用更改。</span><span class="sxs-lookup"><span data-stu-id="4f650-108">To apply the changes, pass the <xref:System.Security.AccessControl.FileSecurity> object to the <xref:System.IO.File.SetAccessControl%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="add-or-remove-an-acl-entry-from-a-directory"></a><span data-ttu-id="4f650-109">添加或从目录中删除 ACL 条目</span><span class="sxs-lookup"><span data-stu-id="4f650-109">Add or remove an ACL entry from a directory</span></span>  
  
1. <span data-ttu-id="4f650-110">调用 <xref:System.IO.Directory.GetAccessControl%2A?displayProperty=nameWithType> 方法以获取 <xref:System.Security.AccessControl.DirectorySecurity> 对象，该对象包含目录的当前 ACL 条目。</span><span class="sxs-lookup"><span data-stu-id="4f650-110">Call the <xref:System.IO.Directory.GetAccessControl%2A?displayProperty=nameWithType> method to get a <xref:System.Security.AccessControl.DirectorySecurity> object that contains the current ACL entries of a directory.</span></span>  
  
2. <span data-ttu-id="4f650-111">添加或从步骤 1 返回的 <xref:System.Security.AccessControl.DirectorySecurity> 对象中删除 ACL 条目。</span><span class="sxs-lookup"><span data-stu-id="4f650-111">Add or remove ACL entries from the <xref:System.Security.AccessControl.DirectorySecurity> object returned from step 1.</span></span>  
  
3. <span data-ttu-id="4f650-112">将 <xref:System.Security.AccessControl.DirectorySecurity> 对象传递给 <xref:System.IO.Directory.SetAccessControl%2A?displayProperty=nameWithType> 方法以应用更改。</span><span class="sxs-lookup"><span data-stu-id="4f650-112">To apply the changes, pass the <xref:System.Security.AccessControl.DirectorySecurity> object to the <xref:System.IO.Directory.SetAccessControl%2A?displayProperty=nameWithType> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f650-113">示例</span><span class="sxs-lookup"><span data-stu-id="4f650-113">Example</span></span>  

 <span data-ttu-id="4f650-114">你必须使用有效的用户或组帐户以运行此示例。</span><span class="sxs-lookup"><span data-stu-id="4f650-114">You must use a valid user or group account to run this example.</span></span> <span data-ttu-id="4f650-115">此示例使用 <xref:System.IO.File> 对象。</span><span class="sxs-lookup"><span data-stu-id="4f650-115">The example uses a <xref:System.IO.File> object.</span></span> <span data-ttu-id="4f650-116">对 <xref:System.IO.FileInfo>、<xref:System.IO.Directory> 和 <xref:System.IO.DirectoryInfo> 类使用相同的过程。</span><span class="sxs-lookup"><span data-stu-id="4f650-116">Use the same procedure for the <xref:System.IO.FileInfo>, <xref:System.IO.Directory>, and <xref:System.IO.DirectoryInfo> classes.</span></span>

 [!code-csharp[IO.File.GetAccessControl-SetAccessControl#1](../../../samples/snippets/csharp/VS_Snippets_CLR/IO.File.GetAccessControl-SetAccessControl/CS/sample.cs#1)]
 [!code-vb[IO.File.GetAccessControl-SetAccessControl#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/IO.File.GetAccessControl-SetAccessControl/VB/sample.vb#1)]  
