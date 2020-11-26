---
title: 将 .NET for Apache Spark 作业提交到 Azure HDInsight
description: 了解如何使用 spark-submit 和 Apache Livy 将 .NET for Apache Spark 作业提交到 Azure HDInsight。
ms.date: 10/09/2020
ms.topic: conceptual
ms.custom: mvc,how-to
ms.openlocfilehash: 74be4ecf33a9a881633da0630fa1c1a4bf0b19c6
ms.sourcegitcommit: 34968a61e9bac0f6be23ed6ffb837f52d2390c85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "94688158"
---
# <a name="submit-a-net-for-apache-spark-job-to-azure-hdinsight"></a><span data-ttu-id="be9f3-103">将 .NET for Apache Spark 作业提交到 Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="be9f3-103">Submit a .NET for Apache Spark job to Azure HDInsight</span></span>

<span data-ttu-id="be9f3-104">可通过两种方法将 .NET for Apache Spark 作业部署到 HDInsight：`spark-submit` 和 Apache Livy。</span><span class="sxs-lookup"><span data-stu-id="be9f3-104">There are two ways to deploy your .NET for Apache Spark job to HDInsight: `spark-submit` and Apache Livy.</span></span>

## <a name="deploy-using-spark-submit"></a><span data-ttu-id="be9f3-105">使用 spark-submit 进行部署</span><span class="sxs-lookup"><span data-stu-id="be9f3-105">Deploy using spark-submit</span></span>

<span data-ttu-id="be9f3-106">可以使用 [spark-submit](https://spark.apache.org/docs/latest/submitting-applications.html) 命令将 .NET for Apache Spark 作业提交到 Azure HDInsight。</span><span class="sxs-lookup"><span data-stu-id="be9f3-106">You can use the [spark-submit](https://spark.apache.org/docs/latest/submitting-applications.html) command to submit .NET for Apache Spark jobs to Azure HDInsight.</span></span>

1. <span data-ttu-id="be9f3-107">导航到 Azure 门户中的 HDInsight Spark 群集，然后选择“SSH + 群集登录名”  。</span><span class="sxs-lookup"><span data-stu-id="be9f3-107">Navigate to your HDInsight Spark cluster in Azure portal, and then select **SSH + Cluster login**.</span></span>

2. <span data-ttu-id="be9f3-108">复制 ssh 登录信息，并将登录名粘贴到终端。</span><span class="sxs-lookup"><span data-stu-id="be9f3-108">Copy the ssh login information and paste the login into a terminal.</span></span> <span data-ttu-id="be9f3-109">使用在群集创建期间设置的密码登录到群集。</span><span class="sxs-lookup"><span data-stu-id="be9f3-109">Sign in to your cluster using the password you set during cluster creation.</span></span> <span data-ttu-id="be9f3-110">应会看到“欢迎使用 Ubuntu 和 Spark”的消息。</span><span class="sxs-lookup"><span data-stu-id="be9f3-110">You should see messages welcoming you to Ubuntu and Spark.</span></span>

3. <span data-ttu-id="be9f3-111">使用 spark-submit 命令在 HDInsight 群集上运行应用  。</span><span class="sxs-lookup"><span data-stu-id="be9f3-111">Use the **spark-submit** command to run your app on your HDInsight cluster.</span></span> <span data-ttu-id="be9f3-112">请记得将示例脚本中的 mycontainer 和 mystorageaccount 替换为 blob 容器和存储帐户的实际名称   。</span><span class="sxs-lookup"><span data-stu-id="be9f3-112">Remember to replace **mycontainer** and **mystorageaccount** in the example script with the actual names of your blob container and storage account.</span></span> <span data-ttu-id="be9f3-113">另外，还需将 microsoft-spark jar 替换为要使用的 Spark 和 .NET for Apache Spark 版本。</span><span class="sxs-lookup"><span data-stu-id="be9f3-113">Also remember to replace the microsoft-spark jar with the version of Spark and .NET for Apache Spark being used.</span></span>

   ```bash
   $SPARK_HOME/bin/spark-submit \
   --master yarn \
   --class org.apache.spark.deploy.dotnet.DotnetRunner \
   wasbs://mycontainer@mystorageaccount.blob.core.windows.net/microsoft-spark-<spark_majorversion-spark_minorversion>_<scala_majorversion.scala_minorversion>-<spark_dotnet_version>.jar \
   wasbs://mycontainer@mystorageaccount.blob.core.windows.net/publish.zip mySparkApp
   ```

## <a name="deploy-using-apache-livy"></a><span data-ttu-id="be9f3-114">使用 Apache Livy 进行部署</span><span class="sxs-lookup"><span data-stu-id="be9f3-114">Deploy using Apache Livy</span></span>

<span data-ttu-id="be9f3-115">可以使用 [Apache Livy](https://livy.incubator.apache.org/)（即 Apache Spark REST API）将 .NET for Apache Spark 作业提交到 Azure HDInsight Spark 群集。</span><span class="sxs-lookup"><span data-stu-id="be9f3-115">You can use [Apache Livy](https://livy.incubator.apache.org/), the Apache Spark REST API, to submit .NET for Apache Spark jobs to an Azure HDInsight Spark cluster.</span></span> <span data-ttu-id="be9f3-116">有关详细信息，请参阅[使用 Apache Livy 提交远程作业](/azure/hdinsight/spark/apache-spark-livy-rest-interface)。</span><span class="sxs-lookup"><span data-stu-id="be9f3-116">For more information, see [Remote jobs with Apache Livy](/azure/hdinsight/spark/apache-spark-livy-rest-interface).</span></span>

<span data-ttu-id="be9f3-117">可使用 `curl` 在 Linux 上运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="be9f3-117">You can run the following command on Linux using `curl`:</span></span>

```bash
curl -k -v -X POST "https://<your spark cluster>.azurehdinsight.net/livy/batches" \
-u "<hdinsight username>:<hdinsight password>" \
-H "Content-Type: application/json" \
-H "X-Requested-By: <hdinsight username>" \
-d @- << EOF
{
    "file":"abfss://<your-file-system-name>@<your-storage-account-name>.dfs.core.windows.net/<some dir>/microsoft-spark-<spark_majorversion-spark_minorversion>_<scala_majorversion.scala_minorversion>-<spark_dotnet_version>.jar",
    "className":"org.apache.spark.deploy.dotnet.DotnetRunner",
    "files":["abfss://<your-file-system-name>@<your-storage-account-name>.dfs.core.windows.net/<some dir>/<udf assembly>", "abfss://<your-file-system-name>@<your-storage-account-name>.dfs.core.windows.net/<some dir>/<file>"],
    "args":["abfss://<your-file-system-name>@<your-storage-account-name>.dfs.core.windows.net/<some dir>/<your app>.zip","<your app>","<app arg 1>","<app arg 2>,"...","<app arg n>"]
}
EOF
```

## <a name="next-steps"></a><span data-ttu-id="be9f3-118">后续步骤</span><span class="sxs-lookup"><span data-stu-id="be9f3-118">Next steps</span></span>

* [<span data-ttu-id="be9f3-119">.NET for Apache Spark 入门</span><span class="sxs-lookup"><span data-stu-id="be9f3-119">Get started with .NET for Apache Spark</span></span>](../tutorials/get-started.md)
* [<span data-ttu-id="be9f3-120">将 .NET for Apache Spark 应用程序部署到 Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="be9f3-120">Deploy a .NET for Apache Spark application to Azure HDInsight</span></span>](../tutorials/hdinsight-deployment.md)
* [<span data-ttu-id="be9f3-121">HDInsight 文档</span><span class="sxs-lookup"><span data-stu-id="be9f3-121">HDInsight Documentation</span></span>](/azure/hdinsight/)
