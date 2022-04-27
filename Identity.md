## ASP.NET Core Identity

ASP.NET Core Identity is a fully featured membership system for creating and maintaining user logins. Using Identity API, you can sign in & sign out users, reset their passwords , lockout users & Implement Multi Factor Authentication. It can also integrate with the external login providers like Microsoft Account, Facebook, Google, etc.

When we create a new application, we can install the ASP.NET Core identity by choosing the Individual Accounts under the Authentication Type Option. Most of the Identity related services and UI forms like Register, Login & Logout are automatically created for us.

In this tutorial, we will create the project with No Authentication and then we will add the Identity API. In this way you will learn the Identity API better.

1. Is an API that supports user interface (UI) login functionality.

2. Manages users, passwords, profile data, roles, claims, tokens, email confirmation, and more.

Identity is typically configured using a SQL Server database to store user names, passwords, and profile data. Alternatively, another persistent store can be used, for example, Azure Table Storage

![Identity](https://chsakell.files.wordpress.com/2018/04/aspnet-core-identity-03.png)

## Microsoft identity platform is

1. An evolution of the Azure Active Directory (Azure AD) developer platform.

2. Unrelated to ASP.NET Core Identity.

ASP.NET Core Identity adds user interface (UI) login functionality to ASP.NET Core web apps. To secure web APIs and SPAs, use IdentityServer4.

### IdentityServer4 enables the following security features:

- Authentication as a Service (AaaS)

- Single sign-on/off (SSO) over multiple application types

- Access control for APIs

- Federation Gateway

## ASP.NET Core 2.0 Authentication and Authorization System Demystified

![Authorization](https://miro.medium.com/max/1200/1*nfrQRCcWW7BsrpIetVl49Q.jpeg)

### Identity

Key to understanding how authentication works is to first understand what an identity is in ASP.NET Core 2.0. There are three classes which represent the identity of a user: Claim, ClaimsIdentity, and ClaimsPrincipal

### Claims

A Claim represents a single fact about the user. It could be the user's first name, last name, age, employer, birth date, or anything else that is true about the user. A single claim will contain only a single piece of information. A claim representing something about a user John Smith could be his first name: John. A second claim would be his last name: Smith.

### ClaimsIdentity

An Identity represents a form of identification or, in other words, a single way of proving who you are. In real life this could be a driver's license. In ASP.Net Core, it is a ClaimsIdentity. This class represents a single form of digital identification.

### ClaimsPrincipal

A Principal represents the actual user. It can contain one or more instances of ClaimsIdentity, just like in life a person may have a driver's license, concealed-carry permit, social security card, and a passport.

### Verbs

There are 5 verbs (these can also be thought of as commands or behaviors) that are invoked by the auth system,

1. Authenticate Gets the user’s information if any exists (e.g. decoding the user’s cookie, if one exists)

2. Challenge Requests authentication by the user (e.g. showing a login page)

3. SignIn Persists the user’s information somewhere (e.g. writes a cookies)

4. SignOut Removes the user’s persisted information (e.g. deletes the cookies)

5. Forbid Denies access to a resource for unauthenticated users or authenticated but unauthorized users (e.g. displaying a “not authorized” page)

## Authentication Handlers

Authentication handlers are components that actually implement the behavior of the 5 verbs.Authentication handlers must be registered with the auth system in order to be used and are associated with schemes.

## Authentication Middleware

A middleware is a module that can be inserted into the startup sequence and is run on every request.


## Things I want to know more about

- Is ASP.NET Core identity secure?

- What is ASP NET identity used for?

- What is the purpose of authentication?

- What are the types of authorization?