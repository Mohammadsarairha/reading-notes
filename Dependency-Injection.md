# Dependency Injection

## Repository Pattern in ASP.NET Core REST API

**What is Repository Pattern ?**

Repository Pattern is an abstraction of the Data Access Layer. It hides the details of how exactly the data is saved or retrieved from the underlying data source. The details of how the data is stored and retrieved is in the respective repository.

**Repository Pattern Interface**

The interface in the repository pattern specifies

* What operations (i.e methods) are supported by the repository
* The data required for each of the operations i.e the parameters that need to be passed to the method and the data the method returns
* The repository interface contains what it can do, but not, how it does, what it can do
* The implementation details are in the respective repository class that implements the repository Interface

IEmployeeRepository interface supports the following operations

* Get all data
* Get a single data by id
* Add a new data
* Update data
* Delete data

## What are the SOLID principles?

A SOLID principle is a group of 5 different design patterns whose main focus is to create loosely coupled architectures with a high level of maintainability. The name SOLID comes from the acronym of its five principles,
- S - Single Responsibility Principle;
- O - Open-Closed Principle;
- L - Liskov Substitution Principle;
- I - Interface Segregation Principle;
- D - Dependency Inversion Principle.

![SOLID principles](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/solid-with-net-core/Images/Picture1.png)
## The SOLID Principles 

**S — Single Responsibility**

If a Class has many responsibilities, it increases the possibility of bugs because making changes to one of its responsibilities, could affect the other ones without you knowing.

**O — Open-Closed**

If you want the Class to perform more functions, the ideal approach is to add to the functions that already exist NOT change them.

**L — Liskov Substitution**

If you have a Class and create another Class from it, it becomes a parent and the new Class becomes a child. The child Class should be able to do everything the parent Class can do. This process is called Inheritance.

The child Class should be able to process the same requests and deliver the same result as the parent Class or it could deliver a result that is of the same type.

**I — Interface Segregation**

When a Class is required to perform actions that are not useful, it is wasteful and may produce unexpected bugs if the Class does not have the ability to perform those actions.
A Class should perform only actions that are needed to fulfil its role. Any other action should be removed completely or moved somewhere else if it might be used by another Class in the future.

**D — Dependency Inversion**

High-level modules should not depend on low-level modules. Both should depend on the abstraction, Abstractions should not depend on details. Details should depend on abstractions.

## Things I want to know more about

1. What's design pattern mean

2. What are the three types of dependency injection?

3. What is the benefits of repository pattern?

4. What are the SOLID principles in OOP?

## Code Reference

[Reading Notes](https://github.com/Mohammadsarairha/reading-notes)