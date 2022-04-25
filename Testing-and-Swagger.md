# Testing and Swagger

## What Is Swagger?

Swagger allows you to describe the structure of your APIs so that machines can read them. 

Swagger (OpenAPI) is a language-agnostic specification for describing REST APIs. It allows both computers and humans to understand the capabilities of a REST API without direct access to the source code.

## Why need Swagger ?

- Minimize the amount of work needed to connect decoupled services.

- Reduce the amount of time needed to accurately document a service.

## What is OpenAPI?

OpenAPI is the global standard for writing RESTful APIs. It like a specification which enables developers around the planet to standardize the design of their APIs. Also, comply with all the safety, versioning, error handling & other best practices when writing REST APIs from the ground up. And not just ground up, even existing APIs can be tweaked to comply with a global standard.

## Advantages of Swagger

The following are advantages of the Swagger Framework:

- Synchronizes the API documentation with the server and client at the same pace.

- Allows us to generate REST API documentation and interact with the REST API. The interaction with the REST API using the Swagger UI Framework gives clear insight into how the API responds to parameters.

- Provides responses in the format of JSON and XML.

- Implementations are available for various technologies, such as Scala, Java, and HTML5.

## Swagger UI

Swagger UI offers a web-based UI that provides information about the service, using the generated OpenAPI specification. The Swashbuckle package has an embedded version of Swagger UI, so that it can be hosted in our ASP.NET Core app using a middleware. Each public action method in the controllers is available in the Swagger UI.

## Integrating Swagger UI in the ASP.NET Core Web API

We can use the Swashbuckle package to integrate Swagger into our .NET Core Web API project. It will generate the Swagger specification and a Swagger UI for our project.

There are three main components in the Swashbuckle package.

- Swashbuckle.AspNetCore.Swagger: This contains the Swagger object model and the middleware to expose SwaggerDocument objects as JSON endpoints.
- Swashbuckle.AspNetCore.SwaggerGen: A Swagger generator that builds SwaggerDocument objects directly from our routes, controllers, and models. 
- Swashbuckle.AspNetCore.SwaggerUI: An embedded version of the Swagger UI and it interprets Swagger JSON to build a rich, customizable experience for describing the web API functionality. It includes built-in test harnesses for the public methods.

## Unit Testing

Unit testing involves testing a part of an app in isolation from its infrastructure and dependencies. When unit testing controller logic, only the contents of a single action is tested, not the behavior of its dependencies or of the framework itself. As you unit test your controller actions, make sure you focus only on its behavior. A controller unit test avoids things like filters, routing, or model binding.

## Why Test Controllers

Controllers are a central part of any ASP.NET Core MVC application. As such, you should have confidence they behave as intended for your app. Automated tests can provide you with this confidence and can detect errors before they reach production. It’s important to avoid placing unnecessary responsibilities within your controllers and ensure your tests focus only on controller responsibilities.

## API Test Methods

If your app exposes web APIs, it’s a good idea to have automated tests confirm they execute as expected. The built-in TestServer makes it easy to test web APIs. If your API methods are using model binding, you should always check ModelState.IsValid, and integration tests are the right place to confirm that your model validation is working properly.

## Things I want to know more about

- What is the difference between postman and Swagger?
- Is swagger a API testing tool?
- When should I use Swagger?
- Is it best practice to test my Web API controllers directly or through an HTTP client?