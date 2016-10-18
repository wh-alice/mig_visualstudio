---
title: "Managing Load Test Results in the Load Test Results Repository"
ms.custom: na
ms.date: "10/03/2016"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "load tests, results repository"
  - "results, load test"
  - "load test results, repository"
  - "Load Test Results Repository"
ms.assetid: 1cd63c4b-4f74-4133-b675-5e8fbeab25f3
caps.latest.revision: 44
ms.author: "ahomer"
manager: "douge"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Managing Load Test Results in the Load Test Results Repository
When you run your load tests, any information gathered during a load test run may be stored in the *Load Test Results Repository*, which is a SQL database. The Load Test Results Repository contains performance counter data and any information about recorded errors. The Results Repository database is created by setup for controllers, or created automatically on the first local run of a load test. For a local run, the database will be created automatically if the load test schema is not present.  
  
 If you modify the controller's results repository connection string to use a different server, the new server must have the loadtestresultsrepository.sql script run to create the schema. For information about how to set up the Load Test Results Repository, see [How to: Create a Load Test Results Repository Using SQL](../test/how-to--create-a-load-test-results-repository-using-sql.md).  
  
 Visual Studio Enterprise provides named counter sets which collect common performance counters based on a technology. These sets are useful when you are analyzing an IIS server, an ASP.NET server, or a SQL server. All of the data collected with counter sets is stored in the Load Test Results Repository.  
  
> [!IMPORTANT]
>  There is a difference between a counter set and the performance counter data. A counter set is metadata. It defines a group of performance counters that should be collected from a computer that is performing a particular role such as IIS or SQL Server. The counter set is part of the load test definition. Performance counter data is collected based on the counter sets, the mapping of the counter set to a specific computer, and the sample rate.  
  
 **Requirements**  
  
-   Visual Studio Enterprise  
  
## SQL Server 2012 versions  
 To use load tests, you can use [SQL Server 2012 Express LocalDB](http://msdn.microsoft.com/library/hh510202.aspx) which is installed with [!INCLUDE[vs2011_subs](../test/includes/vs2011_subs_md.md)] Ultimate and is the default database server for load tests (including Microsoft Excel integration). SQL Server Express LocalDB is an execution mode of SQL Server Express that is targeted to program developers. SQL Server Express LocalDB installation copies a minimal set of files necessary to start the SQL Server Database Engine.  
  
> [!NOTE]
>  If you upgrade from [!INCLUDE[vsUltRosarioShort](../test/includes/vsultrosarioshort_md.md)] and SQL Server Express is detected with an existing load test database, Visual Studio Enterprise will try to connect to it and use it. Additionally, if SQL Server Express is detected, Visual Studio will try to create the load test database using SQL Server Express instead of SQL Server Express LocalDB.  
  
 If your team expects heavy database needs, or your projects outgrow SQL Server 2012 Express LocalDB, you should consider upgrading to either SQL Express or full SQL Server to provide further scaling potential. If you upgrade SQL Server, the MDF and LDF files for the SQL Server 2012 Express LocalDB are stored in the user profile folder. These files can be used to import the load test database to SQL Server Express 2012 or SQL Server 2012.  
  
 You can download SQL Server Express 2012 from the Microsoft Download center: [Microsoft SQL Server Express 2012](http://www.microsoft.com/download/details.aspx?id=29062).  
  
## Load test results store considerations  
 When Visual Studio Enterprise is installed, the load test results store is set up to use an instance of SQL Express that is installed on the computer. SQL Express is limited to using a maximum of 4 GB of disk space. If you will run many load tests over a long period of time, you should consider configuring the load test results store to use an instance of the full SQL Server product if available.  
  
## Load test analyzer tasks  
  
|Tasks|Associated topics|  
|-----------|-----------------------|  
|**Set up a load test results repository:** You can set up a load test results repository on a SQL database. **Note:**  A load test repository can also be created when you install a test controller. For more information, see [Install and configure test agents](../test/install-and-configure-test-agents.md).|-   [How to: Create a Load Test Results Repository Using SQL](../test/how-to--create-a-load-test-results-repository-using-sql.md)|  
|**Selecting and viewing a results repository:** You can select a specific results repository. You are not limited to a local results store. Frequently, load tests are run on a remote set of Agent computers. Test results from your agents or your local computer can be saved to any SQL server on which you have created a load test results store. In either case, you must identify where to store your load test results by using the **Administer Test Controllers** window.|-   [How to: Select a Load Test Results Repository](../test/how-to--select-a-load-test-results-repository.md)<br />-   [How to: Access Load Test Results for Analysis](../test/how-to--access-load-test-results-for-analysis.md)|  
|**Deleting a load test result from the repository:** You can remove a load test result from the **Load Test Editor** by using the **Open and Manage Load Test Results** dialog box.|-   [How to: Delete Load Test Results from a Repository](../test/how-to--delete-load-test-results-from-a-repository.md)|  
|**Import and export results into a repository:** You can import and export load test results from the **Load Test Editor**.|-   [How to: Import Load Test Results into a Repository](../test/how-to--import-load-test-results-into-a-repository.md)<br />-   [How to: Export Load Test Results from a Repository](../test/how-to--export-load-test-results-from-a-repository.md)|  
  
## Related tasks  
 [Analyzing Load Test Results](../test/analyzing-load-test-results-using-the-load-test-analyzer.md)  
  
 You can view the results of both a running load test and a completed load test by using the Load Test Analyzer.  
  
## See Also  
 [Creating and Editing Load Tests](http://msdn.microsoft.com/en-us/e2985d15-60a7-4177-93b4-f986c2936337)   
 [Running Load Tests](../test_notintoc/running-load-tests.md)   
 [Analyzing Load Test Results](../test/analyzing-load-test-results-using-the-load-test-analyzer.md)   
 [Web performance and load tests in Visual Studio](../test_notintoc/web-performance-and-load-tests-in-visual-studio.md)   
 [How to: Access Load Test Results for Analysis](../test/how-to--access-load-test-results-for-analysis.md)