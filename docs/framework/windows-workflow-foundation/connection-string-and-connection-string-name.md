---
title: 连接字符串和连接字符串名称
ms.date: 03/30/2017
ms.assetid: 473e7a3c-c88a-4a01-914a-bea82ba42866
ms.openlocfilehash: 5352dbac09565e872493581a2809409b156d1300
ms.sourcegitcommit: bc293b14af795e0e999e3304dd40c0222cf2ffe4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/26/2020
ms.locfileid: "96248859"
---
# <a name="connection-string-and-connection-string-name"></a><span data-ttu-id="0cc2a-102">连接字符串和连接字符串名称</span><span class="sxs-lookup"><span data-stu-id="0cc2a-102">Connection String and Connection String Name</span></span>

<span data-ttu-id="0cc2a-103">"**连接字符串**" 属性指定 SQL 工作流实例存储应用于连接到永久性数据库的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="0cc2a-103">**Connection String** property specifies the connection string that the SQL Workflow Instance Store should use to connect to a persistence database.</span></span> <span data-ttu-id="0cc2a-104">此参数为可选参数。</span><span class="sxs-lookup"><span data-stu-id="0cc2a-104">This parameter is an optional parameter.</span></span> <span data-ttu-id="0cc2a-105">"**连接字符串名称**" 属性指定 SQL 工作流实例存储区用于连接到持久性数据库的已命名连接字符串的名称。</span><span class="sxs-lookup"><span data-stu-id="0cc2a-105">**Connection String Name** property specifies the name of the named connection string that the SQL Workflow Instance Store should use to connect to the persistence database.</span></span> <span data-ttu-id="0cc2a-106">此参数为可选参数。</span><span class="sxs-lookup"><span data-stu-id="0cc2a-106">This parameter is an optional parameter.</span></span> <span data-ttu-id="0cc2a-107">如果您不希望 SQL 工作流实例存储使用默认命名的连接字符串 **DefaultSqlWorkflowInstanceStoreConnectionString**，则应为 "连接字符串名称" 属性或 "连接字符串" 属性指定一个值。</span><span class="sxs-lookup"><span data-stu-id="0cc2a-107">You should specify a value for the Connection String Name property or the Connection String property if you do not want the SQL Workflow Instance Store to use the default named connection string **DefaultSqlWorkflowInstanceStoreConnectionString**.</span></span>
