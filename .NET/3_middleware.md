# .NET Core middleware
Integrate into the pipeline to handle requests and responses. 

if wants to implement middleware in an application, they must use the Configure() method

# execution order
request => middleware1 => middleware2 => middleware3 => middleware2 => middleware1 => res

# UseAuthentication vs UseAuthorization
Authentication 认证
Authorization 授权

# Use(), Next(), Run()
Use(): add a middleware
Next(): used to invoke the next available middleware
Run(): terminal middleware, there is no middleware to call next

# Built-in Middleware in .NET Core

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
