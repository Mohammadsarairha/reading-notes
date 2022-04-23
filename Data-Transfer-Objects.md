# Data Transfer Objects

## What Is a DTO?

A Data Transfer Object (commonly known as a DTO) is usually an instance of a POCO (plain old CLR object) class used as a container to encapsulate data and pass it from one layer of the application to another. You would typically find DTOs being used in the service layer to return data back to the presentation layer.

It’s used only to send and receive data and does not contain in itself any business logic.

## Why Use DTOs?

The use of DTOs is very common in web development with ASP.NET Core as they provide solutions for many needs. Below are some of them:

- Separate the service layer from the database layer
- Hide specific properties that clients don’t need to receive
- Omit properties to reduce the payload size
- Manipulate nested objects to make them more convenient for clients
- Avoid “overpost” vulnerabilities
- Remove circular references (see previous section).
- Hide particular properties that clients are not supposed to view.
- Omit some properties in order to reduce payload size.
- Flatten object graphs that contain nested objects, to make them more convenient for clients.
- Decouple your service layer from your database layer.

DTOs provide an efficient way to separate domain objects from the presentation layer. This way, you can change the presentation layer without affecting the existing domain layers, and vice versa.

In the flowchart below, the client requests the server the DTO entity, the server gets the domain entity and returns the DTO entity in the response.

![flowchart](https://d585tldpucybw.cloudfront.net/sfimages/default-source/blogs/2022/2022-01/dto-flowchart.png)

## How to use DTOs

When designing and developing an application, if you’re using models to pass data between the layers and sending data back to the presentation layer, then you’re exposing the internal data structures of your application. That’s a major design flaw in your application.

## Use DTOs for abstraction

You can take advantage of DTOs to abstract the domain objects of your application from the user interface or the presentation layer. In doing so, the presentation layer of your application is decoupled from the service layer. So if you would like to change the presentation layer, you can do that easily while the application will continue to work with the existing domain layer. 

![DTO](https://blog.scottlogic.com/swaterman/assets/rethinking-the-java-dto/layers.png)

## Use DTOs for data hiding

Another reason you would want to use DTOs is data hiding. That is, by using DTOs you can return only the data requested. As an example, assume you have a method named GetAllEmployees() that returns all the data pertaining to all employees. Let’s illustrate this by writing some code.

```C#
ublic class Employee
    {
        public int Id { get; set; }
        public string FirstName { get; set; }
        public string LastName { get; set; }
        public string DepartmentName { get; set; }
        public decimal Basic { get; set; }
        public decimal DA { get; set; }
        public decimal HRA { get; set; }
        public decimal NetSalary { get; set; }
    }
```

Note the Employee class contains properties including Id, FirstName, LastName, Department, Basic, DA, HRA, and NetSalary. However, the presentation layer might only need the Id, FirstName, LastName, and Department Name of the employees from the GetAllEmployees() method. If this method returns a List<Employee> then anyone would be able to see the salary details of an employee. You don’t want that. 

To avoid this problem, you might design a DTO class named EmployeeDTO that would contain only the properties that are requested (such as Id, FirstName, LastName, and Department Name).

```C#
public class EmployeeDTO
    {
        public int Id { get; set; }
        public string FirstName { get; set; }
        public string LastName { get; set; }
        public string DepartmentName { get; set; }
    }
```

## Conclusion

The use of DTOs is highly recommended, as it becomes very advantageous to the applications, principally if the data exposed are sensitive—beyond the possibility of personalization of entities, you can avoid excessive use of queries to the APIs.

Therefore, whenever possible, try to use DTOs in your applications—besides being a good practice, it can avoid future problems.

## Things I want to know more about

- Do i always need DTO for all models ?

- Are DTOs necessary?

- Should controller return DTO?

- Where should DTO be used?