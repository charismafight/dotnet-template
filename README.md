# dotnet-template

This is a personal template for backend project, to reduce duplicated startup thing.

## Startup steps

1. dotnet new webapi --use-controllers -o {ProjectName}.
2. cd {ProjectName}.
3. refer to [MS_EF_packages](https://learn.microsoft.com/zh-cn/ef/core/providers/?tabs=dotnet-core-cli), use `dotnet add package Microsoft.EntityFrameworkCore.{db_type}`(Sqlite,InMemory) to add ef.
4. dotnet dev-certs https --trust to use https.
5. dotnet run --launch-profile https to start on https.
6. execute vscode command .net: generate assets for build and debug to generate launch.json and task.json.
7. if the dotnet version is ***9*** or above, the framework use openapi(~/openapi/v1.json) instead of the default swagger.
8. Microsoft.AspNetCore.OpenApi will be install after project created by dotnet new webapi.
9. openapi/v1.json only offers a json format document, if we want a UI format document just like swagger, MS now suggest to use Scalar.
10. dotnet add package Scalar.AspNetCore to add Scalar to project.
11. add app.MapScalarApiReference(); to program.cs.
12. try access ~/scalar/v1 to get scalar for project documents.
13. dotnet add package StyleCop.Analyzers.
14. about Directory.Packages.props, some built-in packages will be added when executing dotnet new, we should add it to Directory.Packages.props first to keep the command going.
15. global.json specifies the dotnet version dotnet cli command used, it was set to '9.0.100' as the latest till this submit.
