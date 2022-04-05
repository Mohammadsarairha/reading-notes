# Language Integrated Query (LINQ):

Is uniform query syntax to retrieve data from different sources and formats ,For example, SQL is a Structured Query Language used to save and retrieve data from a database. In the same way, LINQ is a structured query syntax built in C# and VB.NET to retrieve data from different types of data sources such as collections, ADO.Net DataSet, XML Docs, web service and MS SQL Server and other databases.

![LINQ](https://www.tutorialsteacher.com/Content/images/linq/linq-usage.PNG)

LINQ queries return results as objects. It enables you to uses object-oriented approach on the result set and not to worry about transforming different formats of results into objects.

![LINQ](https://www.tutorialsteacher.com/Content/images/linq/linq-execution.PNG)

The following example demonstrates a simple LINQ query that gets all strings from an array which contains 'a'.

```C#
// Data source
string[] names = {"Bill", "Steve", "James", "Mohan" }; 
// LINQ Query 
var myLinqQuery = from name in names 
                  where name.Contains('a') 
                  select name; 
// Query execution
foreach(var name in myLinqQuery) 
Console.Write(name + " ");
```

## Introduction to LINQ Queries:

A query is an expression that retrieves data from a data source. Queries are usually expressed in a specialized query language.

Different languages have been developed over time for the various types of data sources Like SQL  for database and XQuery for XML. 

Three Parts of a Query Operation:

All LINQ query operations consist of three distinct actions:

1. Obtain the data source.

2. Create the query.

3. Execute the query.


The following example shows how the three parts of a query operation are expressed in source code.

```C#
class IntroToLINQ
{
    static void Main()
    {
        // The Three Parts of a LINQ Query:
        // 1. Data source.
        int[] numbers = new int[7] { 0, 1, 2, 3, 4, 5, 6 };

        // 2. Query creation.
        // numQuery is an IEnumerable<int>
        var numQuery =
            from num in numbers
            where (num % 2) == 0
            select num;

        // 3. Query execution.
        foreach (int num in numQuery)
        {
            Console.Write("{0,1} ", num);
        }
    }
}
```

The following example shows how query operation work 

![query](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/media/introduction-to-linq-queries/linq-query-complete-operation.png)

## Basic LINQ Query Operations

Query syntax is similar to SQL (Structured Query Language) for the database. It is defined within the C# 

- As name suggest, Query Syntax is same like SQL (Structure Query Language) syntax.
- Query Syntax starts with from clause and can be end with Select or GroupBy clause.
- Use various other opertors like filtering, joining, grouping, sorting operators to construct the desired result.
- Implicitly typed variable - var can be used to hold the result of the LINQ query.

## There some example LINQ Query :

1. Filtering:

```C#
var queryLondonCustomers = from cust in customers
                           where cust.City == "London"
                           select cust;
```
Or can use logical AND and OR operators

```C#
where cust.City == "London" && cust.Name == "Devon"

where cust.City == "London" || cust.City == "Paris"
```
2. Ordering:

```C#
var queryLondonCustomers3 =
    from cust in customers
    where cust.City == "London"
    orderby cust.Name ascending
    select cust;
```
3. Grouping

```C#
// queryCustomersByCity is an IEnumerable<IGrouping<string, Customer>>
  var queryCustomersByCity =
      from cust in customers
      group cust by cust.City;

  // customerGroup is an IGrouping<string, Customer>
  foreach (var customerGroup in queryCustomersByCity)
  {
      Console.WriteLine(customerGroup.Key);
      foreach (Customer customer in customerGroup)
      {
          Console.WriteLine("    {0}", customer.Name);
      }
  }
```

4. Joining

```C#
var innerJoinQuery =
    from cust in customers
    join dist in distributors on cust.City equals dist.City
    select new { CustomerName = cust.Name, DistributorName = dist.Name };
```


## Things I want to know more about

- Why we should use LINQ ?

- Is linq built in C#?

- Can i use all sql operations with LINQ ?

