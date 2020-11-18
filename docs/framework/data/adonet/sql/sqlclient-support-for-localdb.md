---
title: SqlClient 对 LocalDB 的支持
ms.date: 03/30/2017
ms.assetid: cf796898-5575-46f2-ae6e-21e5aa8c4123
ms.openlocfilehash: 55ab1346de6f5c14f15d01344a984c18edf30e02
ms.sourcegitcommit: 965a5af7918acb0a3fd3baf342e15d511ef75188
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2020
ms.locfileid: "94824475"
---
# <a name="sqlclient-support-for-localdb"></a><span data-ttu-id="4343d-102">SqlClient 对 LocalDB 的支持</span><span class="sxs-lookup"><span data-stu-id="4343d-102">SqlClient Support for LocalDB</span></span>

<span data-ttu-id="4343d-103">本文讨论如何连接到 LocalDB 数据库。</span><span class="sxs-lookup"><span data-stu-id="4343d-103">This article discusses how to connect to a LocalDB database.</span></span> <span data-ttu-id="4343d-104">LocalDB 是 SQL Server 的轻型版本。</span><span class="sxs-lookup"><span data-stu-id="4343d-104">LocalDB is a lightweight version of SQL Server.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4343d-105">备注</span><span class="sxs-lookup"><span data-stu-id="4343d-105">Remarks</span></span>
  
 <span data-ttu-id="4343d-106">若要汇总可通过 LocalDB 执行的操作：</span><span class="sxs-lookup"><span data-stu-id="4343d-106">To summarize what you can do with LocalDB:</span></span>  
  
- <span data-ttu-id="4343d-107">使用 sqllocaldb 或 app.config 文件创建和启动 LocalDB 实例。</span><span class="sxs-lookup"><span data-stu-id="4343d-107">Create and start LocalDB instances with sqllocaldb.exe or your app.config file.</span></span>  
  
- <span data-ttu-id="4343d-108">使用 sqlcmd.exe 添加和修改 LocalDB 实例中的数据库。</span><span class="sxs-lookup"><span data-stu-id="4343d-108">Use sqlcmd.exe to add and modify databases in a LocalDB instance.</span></span> <span data-ttu-id="4343d-109">例如，`sqlcmd -S (localdb)\myinst`。</span><span class="sxs-lookup"><span data-stu-id="4343d-109">For example, `sqlcmd -S (localdb)\myinst`.</span></span>  
  
- <span data-ttu-id="4343d-110">使用 `AttachDBFilename` 连接字符串关键字将数据库添加到 LocalDB 实例。</span><span class="sxs-lookup"><span data-stu-id="4343d-110">Use the `AttachDBFilename` connection string keyword to add a database to your LocalDB instance.</span></span> <span data-ttu-id="4343d-111">在使用 `AttachDBFilename` 时，如果你没有使用 `Database` 连接字符串关键字指定数据库的名称，则在应用程序关闭时，将从 LocalDB 实例中删除该数据库。</span><span class="sxs-lookup"><span data-stu-id="4343d-111">When using `AttachDBFilename`, if you do not specify the name of the database with the `Database` connection string keyword, the database will be removed from the LocalDB instance when the application closes.</span></span>  
  
- <span data-ttu-id="4343d-112">在连接字符串中指定 LocalDB 实例。</span><span class="sxs-lookup"><span data-stu-id="4343d-112">Specify a LocalDB instance in your connection string.</span></span> <span data-ttu-id="4343d-113">例如，实例名称为 `myInstance`，连接字符串将包括：</span><span class="sxs-lookup"><span data-stu-id="4343d-113">For example, your instance name is `myInstance`, the connection string would include:</span></span>  
  
    `server=(localdb)\\myInstance`  
  
 <span data-ttu-id="4343d-114">连接到 LocalDB 数据库时不允许使用 `User Instance=True`。</span><span class="sxs-lookup"><span data-stu-id="4343d-114">`User Instance=True` is not allowed when connecting to a LocalDB database.</span></span>  
  
<span data-ttu-id="4343d-115">有关安装 LocalDB 的详细信息，请参阅 [SQL Server Express localdb](/sql/database-engine/configure-windows/sql-server-express-localdb)。</span><span class="sxs-lookup"><span data-stu-id="4343d-115">For information about installing LocalDB, see [SQL Server Express LocalDB](/sql/database-engine/configure-windows/sql-server-express-localdb).</span></span>
  
## <a name="programmatically-create-a-named-instance"></a><span data-ttu-id="4343d-116">以编程方式创建命名实例</span><span class="sxs-lookup"><span data-stu-id="4343d-116">Programmatically Create a Named Instance</span></span>  

 <span data-ttu-id="4343d-117">应用程序可以创建命名实例并指定数据库，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4343d-117">An application can create a named instance and specify a database as follows:</span></span>  
  
- <span data-ttu-id="4343d-118">在 app.config 文件中指定要创建的 LocalDB 实例，如下所示。</span><span class="sxs-lookup"><span data-stu-id="4343d-118">Specify the LocalDB instances to create in the app.config file, as follows.</span></span>  <span data-ttu-id="4343d-119">实例的版本号应与 LocalDB 安装的版本号相同。</span><span class="sxs-lookup"><span data-stu-id="4343d-119">The version number of the instance should be the same as the version number of your LocalDB installation.</span></span>  
  
    ```xml  
    <?xml version="1.0" encoding="utf-8" ?>  
    <configuration>  
      <configSections>  
        <section  
        name="system.data.localdb"  
        type="System.Data.LocalDBConfigurationSection,System.Data,Version=4.0.0.0,Culture=neutral,PublicKeyToken=b77a5c561934e089"/>  
      </configSections>  
      <system.data.localdb>  
        <localdbinstances>  
          <add name="myInstance" version="11.0" />  
        </localdbinstances>  
      </system.data.localdb>  
    </configuration>  
    ```  
  
- <span data-ttu-id="4343d-120">使用 `server` 连接字符串关键字指定实例的名称。</span><span class="sxs-lookup"><span data-stu-id="4343d-120">Specify the name of the instance using the `server` connection string keyword.</span></span>  <span data-ttu-id="4343d-121">`server` 连接字符串关键字中指定的实例名称必须与 app.config 文件中指定的名称匹配。</span><span class="sxs-lookup"><span data-stu-id="4343d-121">The instance name specified in the `server` connection string keyword must match the name specified in the app.config file.</span></span>  
  
- <span data-ttu-id="4343d-122">使用 `AttachDBFilename` 连接字符串关键字来指定 .MDF 文件。</span><span class="sxs-lookup"><span data-stu-id="4343d-122">Use the `AttachDBFilename` connection string keyword to specify the .MDF file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4343d-123">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4343d-123">See also</span></span>

- [<span data-ttu-id="4343d-124">SQL Server 功能和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="4343d-124">SQL Server Features and ADO.NET</span></span>](sql-server-features-and-adonet.md)
- [<span data-ttu-id="4343d-125">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="4343d-125">ADO.NET Overview</span></span>](../ado-net-overview.md)
