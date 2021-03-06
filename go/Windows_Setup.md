# Machine Setup 

In this part of the tutorial, you will install the necessary dependencies to run GoLang and connect to Azure SQL.

## Install GoLang

If you already have Go installed on your machine, skip this step. To install GoLang, download the msi file for Windows at the [Go Downloads page](https://golang.org/dl/).

You may also have to [install git](https://git-scm.com/downloads) on your machine, to make future calls to "go get" work.

## Install the ODBC Driver and SQL Command Line Utility for SQL Server

SQLCMD is a command line tool that enables you to connect to Azure SQL or SQL Server and run queries.

1. Install the [**ODBC Driver**](https://docs.microsoft.com/sql/connect/odbc/download-odbc-driver-for-sql-server).
2. Install the [**SQL Server Command Line Utilities**](https://docs.microsoft.com/sql/tools/sqlcmd-utility).

After installing SQLCMD, you can connect to Azure SQL using the following command from a CMD session, making sure to update your connection information:

```terminal
sqlcmd -S your_server.database.windows.net -U your_user -P your_password -d your_databsae
1> # You're connected! Type your T-SQL statements here. Use the keyword 'GO' to execute each batch of statements.
```

This how to run a basic inline query. The results will be printed to STDOUT.

```terminal
sqlcmd -S your_server.database.windows.net -U your_user -P your_password -d your_database -Q "SELECT @@VERSION"
``` 

> You have successfully installed SQL Server Command Line Utilities on your Windows machine, and used them to connect to Azure SQL! 

# Return to the [**main page**](https://github.com/Azure-Samples/AzureSqlGettingStartedSamples/blob/master/go/Readme.md) to complete the tutorial.
