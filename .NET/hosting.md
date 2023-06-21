# Main() method is the entry point for the .net core application to execute.

# host application with default configurations
CreateHostBuilder() > CreateDefaultBuilder()

# CreateDefaultBuilder()
1. Setting up the webserver
    InProcess hosting 
    OutOfProcess hosting
2. Loading the host and application configuration from various configuration sources
3. Configuring logging

# InProcess hosting 
hosting the application in IIS or IIS Express scenarios


# What happens when we set the Hosting model as InProcess?


# What is IIS Express?
The IIS Express is a lightweight, self-contained version of IIS.

# Why InProcess Hosting Gives Better Performance?
In OutOfProcess hosting, there are 2 web servers
1. An internal web server (Kestrel)
2. One external web server (IIS, Nginx, or Apache)

In InProcess hosting model, there is only one web server i.e. IIS.


# Kestrel （cross-platform web server）
The Kestrel is the cross-platform web server for the ASP.NET Core application. 


# How to run the application using Kestrel Web Server?
- launchSettings.json
    IIS
    Kestrel

# How to run a .NET Core application using .NET Core CLI?

# OutOfProcess Hosting
Way 1: 
    Only internal web server (Kestrel) is used to process the incoming HTTP requests 

Way2: 
    Kestrel used with a reverse proxy server such as IIS, Apache, or Nginx. 

### reverse proxy server
reverse proxy server provides an additional layer of configuration and security which is not available with the Kestrel Server
It also maintains the load balancing. 