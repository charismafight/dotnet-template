# dotnet-template

This is a personal template for backend project, to reduce duplicated startup thing.

## Startup steps

1. dotnet new webapi --use-controllers -o {ProjectName}
2. cd {ProjectName}
3. dotnet add package Microsoft.EntityFrameworkCore.InMemory to add ef to project
4. dotnet dev-certs https --trust to use https
5. dotnet run --launch-profile https to start on https
6. execute vscode command .net: generate assets for build and debug to generate launch.json and task.json
7. if the dotnet version is ***9*** or above, the framework use openapi(~/openapi/v1.json) instead of the default swagger
8. dotnet add package Scalar.AspNetCore to add Scalar to project
9. add app.MapScalarApiReference(); to program.cs
10. try access ~/scalar/v1 to get scalar for project documents
