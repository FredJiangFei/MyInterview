# .NET Core middleware
Integrate into the pipeline to handle requests and responses. 

# use Middleware for?
1. authenticating the user
2. log the request and response
3. handle the errors
4. handle the static files such as images, Javascript or CSS files, etc.
5. Authorize the users while accessing a specific resource

# built-in Middleware
1. UseDeveloperExceptionPage()
2. UseRouting()
3. UseEndpoints()

# Execution Order of Middleware
middleware components are executed in the same order as they are added to the pipeline. 
So, we need to take care when adding the middleware components to the request processing pipeline.

request => middleware1 => middleware2 => middleware3 => middleware2 => middleware1 => response

# Request Delegates
Run, Map, and Use

# Use(), Next(), Run()
Use(): add a middleware
Next(): used to invoke the next available middleware
Run(): terminal middleware, there is no middleware to call next

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    app.Use(async (context, next) =>
    {
        await context.Response.WriteAsync("Getting Response from 1st Middleware");
        await next();
    });

    app.Run(async (context) =>
    {
        await context.Response.WriteAsync("Getting Response from 2nd Middleware");
    });

}

# UseDeveloperExceptionPage
This middleware component is going to execute when there is an unhandled exception occurred in the application and since it is in development mode

# UseRouting()
map the URL (or incoming HTTP Request) to a particular resource

# UseEndpoints()

# UseAuthentication vs UseAuthorization
Authentication 认证
Authorization 授权

# MapGet and Map
MapGet method is going to handle the GET HTTP Requests
Map method is going to handle all types of HTTP requests such as GET, POST, PUT, & DELETE, etc.

# Custom Middleware
```
    public class CustomMiddleware
    {
        private readonly RequestDelegate _next;

        public CustomMiddleware(RequestDelegate next)
        {
            _next = next;
        }

        public Task Invoke(HttpContext httpContext)
        {
           return _next(httpContext);
        }
    }
```

# Request Processing Pipeline:
public void Configure(IApplicationBuilder app)
{
    app.Use(async (context, next) =>
    {
        await context.Response.WriteAsync("Middleware1: Incoming Request\n");
        await next();
        await context.Response.WriteAsync("Middleware1: Outgoing Response\n");
    });
    app.Use(async (context, next) =>
    {
        await context.Response.WriteAsync("Middleware2: Incoming Request\n");
        await next();
        await context.Response.WriteAsync("Middleware2: Outgoing Response\n");
    });
    app.Run(async (context) =>
    {
        await context.Response.WriteAsync("Middleware3: Incoming Request handled and response generated\n");
    });
}

Middleware1: Incoming Request
Middleware2: Incoming Request
Middleware3: Incoming Request handled and response generated
Middleware2: Outgoing Response
Middleware1: Outgoing Response

# Key Points to remember:
1. middleware are going to be called one after the other.
2. middleware can perform some operations before and after call next method
3. middleware has access to both the incoming request and the outgoing response.
4. order add is the order call
