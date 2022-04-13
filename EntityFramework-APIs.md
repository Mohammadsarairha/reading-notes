# Entity Framework and APIs

## Entity Framework Core

Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the popular Entity Framework data access technology.

## The model

With EF Core, data access is performed using a model. A model is made up of entity classes and a context object that represents a session with the database

EF supports the following model development approaches:

Generate a model from an existing database.
Hand code a model to match the database.

## Querying

Instances of your entity classes are retrieved from the database using Language Integrated Query (LINQ) . 

## Saving data

Data is created, deleted, and modified in the database using instances of your entity classes. 

## ASP.NET MVC

ASP.NET MVC is a web application framework developed by Microsoft that implements the model–view–controller (MVC) pattern.

## Overview of ASP.NET Core MVC
MVC pattern : The Model-View-Controller (MVC) architectural pattern separates an application into three main groups of components: Models, Views, and Controllers.
![MVC](https://docs.microsoft.com/en-us/aspnet/core/mvc/overview/_static/mvc.png?view=aspnetcore-6.0)

Explain some benefits of using MVC

- Support of multiple views
- Faster development process
- SEO-friendly development
- More Control:
- Lightweight

MVC Responsibilities: 

- Model Responsibilities : Database tables structure . 
- View Responsibilities :  They use the Razor engine  to embed .NET code in HTML markup.
- Controller Responsibilities : Controllers are the components that handle user interaction, work with the model, and ultimately select a view to render.

## Razor Pages 

The Razor Pages framework is lightweight and very flexible. It provides the developer with full control over rendered HTML. Razor Pages is the recommended framework for cross-platform server-side HTML generation.

## Data Seeding

Database seeding is populating a database with an initial set of data. It's common to load seed data such as initial user accounts or dummy data upon initial setup of an application.

There are several ways this can be accomplished in EF Core:

- Model seed data
- Manual migration customization
- Custom initialization logic
- Building Web APIs with ASP.NET
- Web API : Web API is an application programming interface (API) that is used to enable communication or interaction with software components with each other. ASP.NET Web API is a framework that makes it easy to build HTTP Service that reaches a broad range of clients, including browsers and mobile devices. Using ASP.NET, web API can enable communicating by different devices from the same database.

![API](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/create-simple-web-api-in-asp-net-mvc/Images/image002.gif)

## Add User Secrets to .NET Core
**User secrets**  : is a secure way of storing private user information such as API keys, client secrets, and connection strings.
- Never store passwords or other sensitive data in source code.
- Production secrets shouldn't be used for development or test. Secrets shouldn't be deployed with the app

**Environment variables** : Environment variables are used to avoid storage of app secrets in code or in local configuration files. Environment variables override configuration values for all previously specified configuration sources.
**Secret Manager**: The Secret Manager tool stores sensitive data during the development of an ASP.NET Core project. a piece of sensitive data is an app secret.

## How the Secret Manager tool works

The Secret Manager tool hides implementation details, such as where and how the values are stored.

```bash
%APPDATA%\Microsoft\UserSecrets\<user_secrets_id>\secrets.json
```

Set a secret : Define an app secret consisting of a key and its value. The secret is associated with the project's UserSecretsId value

```bash
dotnet user-secrets set "Movies:ServiceApiKey" "12345"
```

## Things I want to know more about

- How i can connect database to my mvc project ?

- Is Razor page suppourt javaspcript ?

- Difference between database first approach and code first approach ?