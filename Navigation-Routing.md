# Navigation Properties and Routing
## Routing in MVC

ASP.NET introduced Routing to eliminate the needs of mapping each URL with a physical file. Routing enables us to define a URL pattern that maps to the request handler.

## Route

Route defines the URL pattern and handler information. All the configured routes of an application stored in RouteTable and will be used by the Routing engine to determine appropriate handler class or file for an incoming request.

![Route](https://www.tutorialsteacher.com/Content/images/mvc/routing-process.png)

## Configure a Route

Every MVC application must configure (register) at least one route configured by the MVC framework by default. You can register a route in RouteConfig class, which is in RouteConfig.cs under App_Start folder. The following figure illustrates how to configure a route in the RouteConfig class .

## URL Pattern
The URL pattern is considered only after the domain name part in the URL. For example, the URL pattern "{controller}/{action}/{id}" would look like localhost:1234/{controller}/{action}/{id}. Anything after "localhost:1234/" would be considered as a controller name. The same way, anything after the controller name would be considered as action name and then the value of id parameter.

![URL Pattern](https://www.tutorialsteacher.com/Content/images/mvc/url-routing.png)

If the URL doesn't contain anything after the domain name, then the default controller and action method will handle the request. For example, http://localhost:1234 would be handled by the HomeController and the Index() method as configured in the default parameter.

## Multiple Routes
You can also configure a custom route using the MapRoute extension method. You need to provide at least two parameters in MapRoute, route name, and URL pattern. The Defaults parameter is optional.

## Route Constraints
You can also apply restrictions on the value of the parameter by configuring route constraints. For example, the following route applies a limitation on the id parameter that the id's value must be numeric.

## Register Routes
Now, after configuring all the routes in the RouteConfig class, you need to register it in the Application_Start() event in the Global.asax so that it includes all your routes into the RouteTable

![Register Routes](https://www.tutorialsteacher.com/Content/images/mvc/Route-configuration-process.png)

## Routing in ASP.NET Core MVC

Routing is the process through which the application matches an incoming URL path and executes the corresponding action methods. ASP.NET Core MVC uses a routing middleware to match the URLs of incoming requests and map them to specific action methods.

We can define the routes either in the startup code or as attributes. They describe how we can match the URL paths with the action methods. We can also use routes to generate URLs for links that are sent out in responses.

There are two types of routing for action methods:

- Conventional Routing
- Attribute Routing

```C#
app.UseEndpoints(endpoints =>
{
    endpoints.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
});
```

## Attribute Routing
By placing a route on the controller or the action method, we can make use of the Attribute Routing feature.

Let’s modify the Configure() method in the startup.cs class and remove the default routes that we had defined earlier.

 
```C#
app.UseEndpoints(endpoints =>
{
    endpoints.MapControllers();
});
```

## Conclusion
In this article we have learned the following topics:

- Creating a Conventional Routing pattern for an ASP.NET Core MVC application
- Configuring Attribute Routing for controllers and action methods
- Setup multiple routes for both conventional and attribute routing

