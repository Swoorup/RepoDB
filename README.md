[![SolutionBuilds](https://img.shields.io/appveyor/ci/mikependon/repodb-h87g9?label=sln%20builds&style=for-the-badge)](https://ci.appveyor.com/project/mikependon/repodb-h87g9)
[![CodeSize](https://img.shields.io/github/languages/code-size/mikependon/repodb?style=for-the-badge)](https://github.com/mikependon/RepoDb/tree/master/RepoDb.Core)
[![GitterChat](https://img.shields.io/gitter/room/mikependon/RepoDb?color=48B293&style=for-the-badge)](https://gitter.im/RepoDb/community)

<img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Icons/RepoDb-64x64.png" height="64px" />

## RepoDb - a hybrid ORM library for .NET.

RepoDb provide certain features of both lightweight-ORMs and full-ORMs. It helps the developer to simplify the “switchover” of when to use the “lightweight” and “advance” operations during the development.

### It is high-performance

This refers to “how fast” RepoDb converts the raw data into a class object, and transport the class object as an actual data in the database.

RepoDb has its own compiler. It caches the “already-generated” compiled-ILs and compiled-Expressions and reusing them for the upcoming transformations. Furthermore, RepoDb also caches the “already-executed” operation-context and reusing it for future calls.

### It is efficient

This refers to “how well-managed” RepoDb uses the computer memory when manipulating the objects all throughout the cycle of the operations.

RepoDb caches the “already-extracted” object properties, mappings and SQL statements and reusing it all throughout the process of transformations and executions. It helps eliminate the creation of unnecessary objects that leads to a low memory consumption.

## Builds and Tests Result

Project/Solution                                                                | Build                                                                                                                                                   | Version                                                                                                                          | Downloads                                                                                                                    | Unit Tests                                                                                                                                                                 | IntegrationTests                                                                                                                                                                  |
--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
[RepoDb.Core](https://github.com/mikependon/RepoDb/tree/master/RepoDb.Core)     | [![CoreBuild](https://img.shields.io/appveyor/ci/mikependon/repodb-ek0nw?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-ek0nw)   | [![CoreVersion](https://img.shields.io/nuget/v/RepoDb?style=flat-square)](https://www.nuget.org/packages/RepoDb)                 | [![CoreDL](https://img.shields.io/nuget/dt/repodb?style=flat-square)](https://www.nuget.org/packages/RepoDb)                 | [![CoreUnitTests](https://img.shields.io/appveyor/tests/mikependon/repodb-yf1cx?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-yf1cx/build/tests)   | [![CoreIntegrationTests](https://img.shields.io/appveyor/tests/mikependon/repodb-qksas?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-qksas/build/tests)   |
[RepoDb.SqLite](https://github.com/mikependon/RepoDb/tree/master/RepoDb.SqLite) | [![SqLiteBuild](https://img.shields.io/appveyor/ci/mikependon/repodb-o6787?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-o6787) | [![SqLiteVersion](https://img.shields.io/nuget/v/RepoDb.SqLite?style=flat-square)](https://www.nuget.org/packages/RepoDb.SqLite) | [![SqLiteDL](https://img.shields.io/nuget/dt/repodb.sqlite?style=flat-square)](https://www.nuget.org/packages/RepoDb.SqLite) | [![SqLiteUnitTests](https://img.shields.io/appveyor/tests/mikependon/repodb-mhpo4?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-mhpo4/build/tests) | [![SqLiteIntegrationTests](https://img.shields.io/appveyor/tests/mikependon/repodb-eg27p?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-eg27p/build/tests) |
[RepoDb.MySql](https://github.com/mikependon/RepoDb/tree/master/RepoDb.MySql)   | [![MySqlBuild](https://img.shields.io/appveyor/ci/mikependon/repodb-6adn4?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-6adn4)  | [![MySqlVersion](https://img.shields.io/nuget/v/RepoDb.MySql?style=flat-square)](https://www.nuget.org/packages/RepoDb.MySql)    | [![MySqlDL](https://img.shields.io/nuget/dt/repodb.mysql?style=flat-square)](https://www.nuget.org/packages/RepoDb.MySql)    | [![MySqlUnitTests](https://img.shields.io/appveyor/tests/mikependon/repodb-t2hy7?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-t2hy7/build/tests)  | [![MySqlIntegrationTests](https://img.shields.io/appveyor/tests/mikependon/repodb-o4t48?style=flat-square)](https://ci.appveyor.com/project/mikependon/repodb-o4t48/build/tests)  |

## Supported Databases

Practically, RepoDb has supported all RDBMS data-providers. Developers has the freedom to write their own SQL statement and execute it against the database in one-go. The execution of the SQL statements limit only from the “Execute” methods the RepoDb has provided (ie: *ExecuteQuery*, *ExecuteNonQuery*, *ExecuteScalar*, *ExecuteReader* and *ExecuteQueryMultiple*).

### Fully supported databases for fluent-methods

<img src="https://github.com/mikependon/RepoDb/blob/master/RepoDb.Wiki/Images/SqlServer.png?raw=true" height="64px" title="SqlServer" /> <img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Wiki/Images/SQLite.png" height="64px" title="SqLite" /> <img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Wiki/Images/MySql.png" height="64px" title="MySql" />

RepoDb has “fluent” methods in which the SQL Statements are automatically being constructed as part of the execution context. These methods are the most common operations being used by most developers. In this regards, RepoDb only fully supported the *SQL Server*, *SQLite*, *MySQL* and *PostgreSQL (soon)* data 

### Extensibility

RepoDb is highly extensible and dynamic enough to further support other RDBMS data-providers. The developers only need to implement certain interfaces to make it work. There will be detailed documentation soon. For now, please contact the me (as an author) for help.

## Community

RepoDb is rapidly expanding its capability to further support other RDBMS data-providers (in which each implementation differs from each other). Though it is a micro-ORM, but it really requires significant amount of time and effort to maintain.

It is now open for *community contributions* to further enhance the features of the library and as well the *community engagements*.

### Engagements

As an author, I would like to build a healthy and active community that would help fellow .NET developers build the knowledge-base when it comes to database accessibility. Please get in touch via:

- [GitHub](https://github.com/mikependon/RepoDb/issues) - for any issues, requests and problems.
- [StackOverflow](https://stackoverflow.com/questions/tagged/repodb) - for any technical questions.
- [Twitter](https://twitter.com/search?q=%23repodb) - for the latest news.
- [Gitter Chat](https://gitter.im/RepoDb/community) - for direct and live Q&A.

Any help from the community will be highly appreciated as it really helps me eliminate my full-efforts. 

## Contributions

The folder [RepoDb.Core](https://github.com/mikependon/RepoDb/tree/master/RepoDb.Core) is the code-line built via NetStandard. **This is the portable one and any pull-request must be done on this code-line.**

The folder [RepoDb](https://github.com/mikependon/RepoDb/tree/master/RepoDb) is the code-line that supports the NetFramework solutions. It is very dedicated. This must **NOT** be pulled-request as this will be **out-of-support** starting **v1.10.1**.

To contribute, open the [Issues]([https://github.com/mikependon/RepoDb/issues](https://github.com/mikependon/RepoDb/issues)) tab and filter the list of items with **for grabs** label.

## License

[Apache-2.0](http://apache.org/licenses/LICENSE-2.0.html) - Copyright © 2019 - Michael Camara Pendon

## Benchmark

Being the author of this library and to avoid the bias on the results, the benchmark to be shown on this page will always be referring to the community-approved ORM-bencher ([RawDataAccessBencher](https://github.com/FransBouma/RawDataAccessBencher) tool).

Results below is based on the recent official execution [result](https://github.com/FransBouma/RawDataAccessBencher/blob/master/Results/20190520_netcore.txt).

<img src="https://raw.githubusercontent.com/mikependon/RepoDb/master/RepoDb.Raw/RDAB/RDAB-Result.PNG" height="500px" />

RepoDb is the **fastest** and the **most-efficient** ORM as per the official [result](https://github.com/FransBouma/RawDataAccessBencher/blob/master/Results/20190520_netcore.txt) of [RawDataAccessBencher](https://github.com/FransBouma/RawDataAccessBencher) tool.

This section will always be updated with the latest official result.

## Operations

Below are the list of operations available at RepoDb.

Operation                                                                                                 | Normal<TEntity> | Normal<TEntity> (Async) | TableName | TableName (Async) | Packed Execution | Data Providers         |
----------------------------------------------------------------------------------------------------------|-----------------|-------------------------|-----------|-------------------|------------------|------------------------|
[Average](https://repodb.readthedocs.io/en/latest/pages/connection.html#average)                          | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[AverageAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#averageALL)                    | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[BatchQuery](https://repodb.readthedocs.io/en/latest/pages/connection.html#batchquery)                    | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[BulkInsert](https://repodb.readthedocs.io/en/latest/pages/connection.html#bulkinsert)                    | YES             | YES                     | YES       | YES               | NO               | SQLSVR, POSTGRESQL     |
[Count](https://repodb.readthedocs.io/en/latest/pages/connection.html#count)                              | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[CountAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#countall)                        | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[Delete](https://repodb.readthedocs.io/en/latest/pages/connection.html#delete)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[DeleteAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#deleteall)                      | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[ExecuteNonQuery](https://repodb.readthedocs.io/en/latest/pages/connection.html#executenonquery)          | YES             | YES                     | NO        | NO                | NO               | ALL                    |
[ExecuteQuery](https://repodb.readthedocs.io/en/latest/pages/connection.html#executequery)                | YES             | YES                     | NO        | NO                | NO               | ALL                    |
[ExecuteQueryMultiple](https://repodb.readthedocs.io/en/latest/pages/connection.html#executequerymultiple)| YES             | YES                     | NO        | NO                | NO               | ALL                    |
[ExecuteReader](https://repodb.readthedocs.io/en/latest/pages/connection.html#executereader)              | YES             | YES                     | NO        | NO                | NO               | ALL                    |
[ExecuteScalar](https://repodb.readthedocs.io/en/latest/pages/connection.html#executescalar)              | YES             | YES                     | NO        | NO                | NO               | ALL                    |
[Exists](https://repodb.readthedocs.io/en/latest/pages/connection.html#exists)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[Insert](https://repodb.readthedocs.io/en/latest/pages/connection.html#insert)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[InsertAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#insertall)                      | YES             | YES                     | YES       | YES               | YES         	   | MENTIONED              |
[Max](https://repodb.readthedocs.io/en/latest/pages/connection.html#max)                                  | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[MaxAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#maxall)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[Merge](https://repodb.readthedocs.io/en/latest/pages/connection.html#merge)                              | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[MergeAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#mergeall)                        | YES             | YES                     | YES       | YES               | YES              | MENTIONED              |
[Min](https://repodb.readthedocs.io/en/latest/pages/connection.html#min)                                  | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[MinAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#minall)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[Query](https://repodb.readthedocs.io/en/latest/pages/connection.html#query)                              | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[QueryAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#queryall)                        | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[QueryMultiple](https://repodb.readthedocs.io/en/latest/pages/connection.html#querymultiple)              | YES             | YES                     | NO        | NO                | YES              | MENTIONED              |
[Sum](https://repodb.readthedocs.io/en/latest/pages/connection.html#sum)                                  | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[SumAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#sumall)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[Truncate](https://repodb.readthedocs.io/en/latest/pages/connection.html#truncate)                        | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[Update](https://repodb.readthedocs.io/en/latest/pages/connection.html#update)                            | YES             | YES                     | YES       | YES               | NO               | MENTIONED              |
[UpdateAll](https://repodb.readthedocs.io/en/latest/pages/connection.html#updateall)                      | YES             | YES                     | YES       | YES               | YES              | MENTIONED              |

## Installations

RepoDb and its extension is available via Nuget as a NetStandard library. Type the commands below at the ***Package Manager Console*** window.

```
Install-Package RepoDb
Install-Package RepoDb.SqLite
Install-Package RepoDb.MySql
```

## Snippets and Samples

Let us say you have a customer class named `Customer` that has an equivalent table in the database named `[dbo].[Customer]`.

```csharp
public class Customer
{
	public int Id { get; set; }
	public string FirstName { get; set; }
	public string LastName { get; set; }
	public bool IsActive { get; set; }
	public DateTime LastUpdatedUtc { get; set; }
	public DateTime CreatedDateUtc { get; set; }
}
```

### Querying a Data

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(new { Id = 10045 });
}
```

Via Expression:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(c => c.Id == 10045);
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(new QueryField(nameof(Customer.Id), 10045));
}
```

### Querying via TableName

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", new { Id = 10045 });
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", new QueryField(nameof(Customer.Id), 10045));
}
```
	
Via Object (targetting few fields):

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query("Customer", new QueryField(nameof(Customer.Id), 10045),
		Field.From("Id", "FirstName", "LastName"));
}
```

### Inserting a Data

```csharp
var customer = new Customer
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true
};
using (var connection = new SqlConnection(ConnectionString))
{
	var id = connection.Insert<Customer, int>(customer);
}
```

### Inserting via TableName

```csharp
var customer = new
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true,
	LastUpdatedUtc = DateTime.UtcNow,
	CreatedDateUtc = DateTime.UtcNow
};
using (var connection = new SqlConnection(ConnectionString))
{
	var id = connection.Insert<int>("Customer", customer);
}
```

### Updating a Data

Via DataEntity:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer);
}
```

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, new { Id = 10045 });
}
```

Via Expression:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, e => e.Id == 10045);
}
```
	
Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	customer.FirstName = "John";
	customer.LastUpdatedUtc = DateTime.UtcNow;
	var affectedRows = connection.Update<Customer>(customer, new QueryField(nameof(Customer.Id), 10045));
}
```

### Updating via TableName

Via Dynamic Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		Id = 10045,
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer);
}
```

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer, 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer, new { Id = 10045 });
}
```
	
Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = new
	{
		FirstName = "John",
		LastUpdatedUtc = DateTime.UtcNow
	};
	var affectedRows = connection.Update("Customer", customer, new QueryField("Id", 10045));
}
```

### Deleting a Data

Via DataEntity:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.Query<Customer>(10045);
	var deletedCount = connection.Delete<Customer>(customer);
}
```

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(new { Id = 10045 });
}
```

Via Expression:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(c => c.Id == 10045);
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete<Customer>(new QueryField(nameof(Customer.Id), 10045));
}
```

### Deleting via TableName

Via PrimaryKey:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete("Customer", 10045);
}
```

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete("Customer", { Id = 10045 });
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var deletedCount = connection.Delete("Customer", new QueryField(nameof(Customer.Id), 10045));
}
```

### Merging a Data

```csharp
var customer = new Customer
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true,
	LastUpdatedUtc = DateTime.Utc,
	CreatedDateUtc = DateTime.Utc
};
using (var connection = new SqlConnection(ConnectionString))
{
	var qualifiers = new []
	{
		new Field(nameof(Customer.FirstName)),
		new Field(nameof(Customer.LastName)),
	};
	var mergeCount = connection.Merge<Customer>(customer, qualifiers);
}
```

### Merging via TableName

```csharp
var customer = new Customer
{
	FirstName = "John",
	LastName = "Doe",
	IsActive = true
};
using (var connection = new SqlConnection(ConnectionString))
{
	var qualifiers = new []
	{
		new Field(nameof(Customer.FirstName)),
		new Field(nameof(Customer.LastName)),
	};
	var mergeCount = connection.Merge("Customer", customer, qualifiers);
}
```

### Executing a Customized-Query

You can create a class with combined properties of different tables or with stored procedures. It does not need to be 100% identical to the schema, as long the property of the class is part of the result set.

```csharp
public class ComplexClass
{
	public int CustomerId { get; set; }
	public int OrderId { get; set; }
	public int ProductId { get; set; }
	public string CustomerName { get; set; }
	public string ProductName { get; set; }
	public DateTime ProductDescription { get; set; } // This is not in the CommandText, will be ignored
	public DateTime OrderDate { get; set; }
	public int Quantity { get; set; }
	public double Price { get; set; }
}
```

Then you can create this command text.

	var commandText = @"SELECT C.Id AS CustomerId
		, O.Id AS OrderId
		, P.Id AS ProductId
		, CONCAT(C.FirstName, ' ', C.LastName) AS CustomerName
		, P.Name AS ProductName
		, O.OrderDate
		, O.Quantity
		, P.Price
		, (O.Quatity * P.Price) AS Total /* Note: This is not in the class, but still it is valid */
	FROM [dbo].[Customer] C
	INNER JOIN [dbo].[Order] O ON O.CustomerId = C.Id
	INNER JOIN [dbo].[OrderItem] OI ON OI.OrderId = O.Id
	INNER JOIN [dbo].[Product] P ON P.Id = OI.ProductId
	WHERE (C.Id = @CustomerId)
		AND (O.OrderDate BETWEEN @OrderDate AND DATEADD(DAY, 1, @OrderDate));";

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.ExecuteQuery<ComplexClass>(commandText, new { CustomerId = 10045, OrderDate = DateTime.UtcNow.Date });
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var queryGroup = new QueryGroup(new []
	{
		new QueryField("CustomerId", 10045),
		new QueryField("OrderDate", DateTime.UtcNow.Date)
	});
	var customer = connection.ExecuteQuery<Customer>(commandText, queryGroup);
}
```

The `ExecuteQuery` method is purposely not being supported by `Expression` based query as we are avoiding the user to bind the complex-class to its target query text.

Note: The most optimal when it comes to performance is to used the `Object-Based`.

### Calling a StoredProcedure

Using the complex type above. If you have a stored procedure like below.

	DROP PROCEDURE IF EXISTS [dbo].[sp_get_customer_orders_by_date];
	GO
	CREATE PROCEDURE [dbo].[sp_get_customer_orders_by_date]
	(
		@CustomerId INT
		, @OrderDate DATETIME2(7)
	)
	AS
	BEGIN
		SELECT C.Id AS CustomerId
			, O.Id AS OrderId
			, P.Id AS ProductId
			, CONCAT(C.FirstName, ' ', C.LastName) AS CustomerName
			, P.Name AS ProductName
			, O.OrderDate
			, O.Quantity
			, P.Price
			, (O.Quatity * P.Price) AS Total /* Note: This is not in the class, but still it is valid */
		FROM [dbo].[Customer] C
		INNER JOIN [dbo].[Order] O ON O.CustomerId = C.Id
		INNER JOIN [dbo].[OrderItem] OI ON OI.OrderId = O.Id
		INNER JOIN [dbo].[Product] P ON P.Id = OI.ProductId
		WHERE (C.Id = @CustomerId)
			AND (O.OrderDate BETWEEN @OrderDate AND DATEADD(DAY, 1, @OrderDate));
	END

Then it can be called as below.

Via Dynamic:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var customer = connection.ExecuteQuery<ComplexClass>("[dbo].[sp_get_customer_orders_by_date]",
		param: new { CustomerId = 10045, OrderDate = DateTime.UtcNow.Date },
		commandType: CommandType.StoredProcedure);
}
```

Via Object:

```csharp
using (var connection = new SqlConnection(ConnectionString))
{
	var queryGroup = new QueryGroup(new []
	{
		new QueryField("CustomerId", 10045),
		new QueryField("OrderDate", DateTime.UtcNow.Date)
	});
	var customer = connection.ExecuteQuery<Customer>(commandText, queryGroup,
		commandType: CommandType.StoredProcedure);
}
```

Please visit the [documentation](https://repodb.readthedocs.io/en/latest/) for further details about the codes.
