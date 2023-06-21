# IConfiguration["xxx"]

# Execution Order
later configuration sources will override the earlier configuration sources
1. appsettings.json, 
2. appsettings.{Environment}.json here we use appsettings.development.json
3. User secrets
4. Environment variables
5. Command-line arguments

# Pass Config value from Command Line
dotnet run Key="my key"