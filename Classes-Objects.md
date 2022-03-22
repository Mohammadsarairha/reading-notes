# Classes & Objects

## Introduction to classes

- Class is a reference type,At run time, variable of a reference type contains the value null.

- To Declaring use class keyword is preceded by the access level.

```C#
public class Customer
{
   // Fields, properties, methods and events go here...
}
```

- Creating objects from class use new keyworld.

```C#
Customer object1 = new Customer();
```

- Classes fully support inheritance, When you create a class, you can inherit from any other class that is not defined as sealed.

```C#
public class Manager : Employee
{

}
```

## Constructors

- A constructor is a method whose name is the same as the name of class.

```C#
public class Manager : Employee
{
    public Manager(){

    }
}
```

## Properties

- property is like a combination of a variable and a method, and it has two methods: a get and a set method.

- A get property accessor is used to return the property value, and a set property accessor is used to assign a new value.

```C#
class Person
{
  private string name; // field

  public string Name   // property
  {
    get { return name; }   // get method
    set { name = value; }  // set method
  }
}
}
```

## Stack vs. Heap: What's the difference?

|Parameter                |Stack                                |Heap
|-------------------------|-------------------------------------|----------------------------------------------|
| Type of data structures | A stack is a linear data structure. | Heap is a hierarchical data structure        |
| Access speed            | High-speed access                   | Slower compared to stack                     |
| Access                  | Local variables only                | It allows you to access variables globally   |
| Limit of space size     | Limit on stack size dependent on OS | Does not have a specific limit on memory size|
| Resize                  | Variables cannot be resized         | Variables can be resized.                    |

## garbage collection

> The garbage collector manages the allocation and release of memory for an application , And help developers from having to manually release memory,Automatic memory management can eliminate common problems
