### .NET Core
a newer version of .NET, Cross-platform / Open-source / Cloud support

### Advantages of .NET Core over ASP.NET.
- Cross-platform. 
- Open-source 
- Cloud support: ideal for deploying applications on several servers
- 独立安装部署，不依赖底层环境
- IoC Container

### Disadvantage of .NET Framework
Asp.net 耦合 IIS
底层不支持依赖注入、单元测试
Mono继承.NET Framework

### Features of .NET Core.
- Is open source: Developers can access source code freely from the open-source framework
- Supports several programming languages: Developers can use several programming languages with .NET Core
- Offers cross-platform support: Developers can port a code from one platform, like Linux or Windows, to another one, like MacOS

- 依赖注入。
- 日志系统架构。
- 引入了一个跨平台的网络服务器，kestrel。可以没有iis, apache和nginx就可以单独运行。
- 可以使用命令行创建应用。
- 使用AppSettings.json 来配置工程。
- 使用start up来注册服务。
- 更好的支持异步编程。
- 支持web socket和signal IR。
- 对于跨网站的请求的预防和保护机制。

# .NET Standard
.NET API 规范
推出 .NET Standard 的背后动机是要提高 .NET 生态系统中的一致性。

# Kestrel
Kestrel 是包含在 ASP.NET Core 项目模板中的 Web 服务器，默认处于启用状态。 
Kestrel 是asp.net core引入的跨平台的网络服务器，是默认配置。可以没有iis, apache和nginx就可以单独运行。

Kestrel is a cross-platform web server built for ASP.NET Core based on libuv – a cross-platform asynchronous I/O library.
It is a default web server pick since it is used in all ASP.NET Core templates.
It is really fast.
It is secure and good enough to use it without a reverse proxy server. However, it is still recommended that you use IIS, Nginx or Apache or something else.

# Describe the main three architectural components of .NET Core.
* Libraries: Framework libraries feature base libraries and components such as app composition types
* SDK compilers: SDK compilers make it easier for developers to build applications or programs in .NET Core
* .NET Core runtime: With garbage collection and type safety features, the .NET Core runtime component works to optimize the app’s functioning

# AddSingleton, AddScoped, AddTransient
AddSingleton (只会有一个， 配置，数据库链接字符串)
AddScoped (每次请求一个， Repository)
AddTransient (每次获取都是新的)

# How is the task different from the thread in .NET Core?
tasks: Things you need to do
threads: provide a method for accomplishing the tasks

* Thread represents an actual OS-level thread, with its own stack and kernel resources. Thread allows the highest degree of control; you can Abort() or Suspend() or Resume() a thread, you can observe its state, and you can set thread-level properties like the stack size, apartment state, or culture. ThreadPool is a wrapper around a pool of threads maintained by the CLR.

* The Task class from the Task Parallel Library offers the best of both worlds. Like the ThreadPool, a task does not create its own OS thread. Instead, tasks are executed by a TaskScheduler; the default scheduler simply runs on the ThreadPool. Unlike the ThreadPool, Task also allows you to find out when it finishes, and (via the generic Task) to return a result.




# 异步
1. 提高并发