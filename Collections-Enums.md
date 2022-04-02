# Collections & Enums

## **Collections**

Collection classes are specialized classes for data storage and retrieval. These classes provide support for stacks, queues, lists, and hash tables. Most collection classes implement the same interfaces.

Collection types are designed to store, manage and manipulate similar data more efficiently. Data manipulation includes adding, removing, finding, and inserting data in the collection. Collection types implement the following common functionality: 

- Adding and inserting items to a collection
- Removing items from a collection
- Finding, sorting, searching items
- Replacing items
- Copy and clone collections and items
- Capacity and Count properties to find the capacity of the collection and number of items in the collection

**Simple Collection**

- The examples in this section use the generic List<T> class, which enables you to work with a strongly typed list of objects.

```C#
var salmons = new List<string>();
salmons.Add("chinook");
salmons.Add("coho");
salmons.Add("pink");
salmons.Add("sockeye");
```
- There is another way initialize generic list
```C#
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };
```
- There is tow way to iterates through the elements of a collection by using **for** or **foreach**.

**For**
```C#
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };
for (var index = 0; index < salmons.Count; index++)
{
    Console.Write(salmons[index] + " ");
}
```
**Foreach**

```C#
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };
foreach (var salmon in salmons)
{
    Console.Write(salmon + " ");
}
```

- For removes an element from the collection by specifying the object.

```C#
var salmons = new List<string> { "chinook", "coho", "pink", "sockeye" };

salmons.Remove("coho");
```
- There another example removes elements from a generic list
```C#
var numbers = new List<int> { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };

// Remove odd numbers.
for (var i = 0 ; index < numbers.Count; index++)
{
        numbers.RemoveAt(i);
}
```
## **System.Collections Classes**

|Class|	Description|
|-----|------------|
|ArrayList|	Represents an array of objects whose size is dynamically increased as required|
|Hashtable|	Represents a collection of key/value pairs that are organized based on the hash code of the key|
|Queue|	Represents a first in, first out (FIFO) collection of objects|
|Stack|	Represents a last in, first out (LIFO) collection of objects|


## **Implementing a Collection of Key/Value**

The Dictionary<TKey,TValue> generic collection enables you to access to elements in a collection by using the key of each element.

- The following code example shows how to enumerate the keys and values in a dictionary, using the KeyValuePair<TKey,TValue> structure

```C#
public readonly struct KeyValuePair<TKey,TValue>

foreach( KeyValuePair<string, string> kvp in openWith )
{
    Console.WriteLine("Key = {0}, Value = {1}",
        kvp.Key, kvp.Value);
}
```
- TKey: The type of the key.

- TValue : The type of the value.

## **Enum**

An enum is a special "class" that represents a group of constants (unchangeable/read-only variables).

To create an enum, use the **enum** keyword (instead of class or interface), and separate the enum items with a comma:

```C#
enum Level 
{
  Low,
  Medium,
  High
}
```

- You can access enum items with the dot syntax:

```C#
Level myVar = Level.Medium;
Console.WriteLine(myVar);
```

Enum inside a Class

- You can also have an enum inside a class:
```C#
class Program
{
  enum Level
  {
    Low,
    Medium,
    High
  }
  static void Main(string[] args)
  {
    Level myVar = Level.Medium;
    Console.WriteLine(myVar);
  }
}
```

Enum Values

- By default, the first item of an enum has the value 0. The second has the value 1, and so on.

- To get the integer value from an item, you must explicitly convert the item to an int:

```C#
enum Months
{
  January,    // 0
  February,   // 1
  March,      // 2
  April,      // 3
  May,        // 4
  June,       // 5
  July        // 6
}

static void Main(string[] args)
{
  int myNum = (int) Months.April;
  Console.WriteLine(myNum);
}
```

Enum in a Switch Statement

- Enums are often used in switch statements to check for corresponding values:

```C#
enum Level 
{
  Low,
  Medium,
  High
}

static void Main(string[] args) 
{
  Level myVar = Level.Medium;
  switch(myVar) 
  {
    case Level.Low:
      Console.WriteLine("Low level");
      break;
    case Level.Medium:
       Console.WriteLine("Medium level");
      break;
    case Level.High:
      Console.WriteLine("High level");
      break;
  }
}   
```


## Things I want to know more about

- Can i have my own Collections?

- whats collections is the Input/Output index-based?

- In a HashTable Key cannot be null, What Value can be ?

- What the purpose of create enums?

