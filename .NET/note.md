### .net 和 .net core 区别
环境：windows / 跨平台(deploy带环境打包)
program.cs: services(CORS, MediatR, Jwt), middleware(auth, exception)

AddSingleton (只会有一个， 配置，数据库链接字符串)
AddScoped (每次请求一个， Repository)
AddTransient (每次获取都是新的)

### controller(RESTful)

### Auth

### Database(ef core, linq)
stored procedure(数据库内存) / ef core(代码易维护，好开发，效率稍差)






