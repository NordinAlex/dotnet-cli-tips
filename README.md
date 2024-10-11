# 🌐 .NET CLI Tips

📚 A comprehensive and well-organized guide and tips to essential `.NET` CLI commands for developers, including command syntax, descriptions, and examples of usage. 



📋 **Table of Contents**
- [🚀 Getting Started](#-getting-started)
- [🔧 Project and Solution Management](#-project-and-solution-management)
- [🏗️ Building, Publishing, and Running Projects](#%EF%B8%8F-building-publishing-and-running-projects)
- [🧪 Testing and Debugging](#-testing-and-debugging)
- [📦 NuGet and Package Management](#-nuget-and-package-management)
- [💾 Entity Framework Core](#-entity-framework-core)
- [🛠️ Global Tools and Workloads](#%EF%B8%8F-global-tools-and-workloads)
- [🔑 Configuration and User Secrets](#-configuration-and-user-secrets)
- [⚙️ Performance Optimization and Version Management](#%EF%B8%8F-performance-optimization-and-version-management)
- [📜 .NET SDK and Runtime Management](#-net-sdk-and-runtime-management)
## 🚀 Getting Started
Welcome to the **.NET CLI Tips**! 🎉 This repository aims to make working with `.NET` command-line tools easier for developers. Whether you're managing projects, running tests, or deploying applications, you'll find what you need right here.

🇸🇪 **Looking for the Swedish version?** Check out the [Swedish Version](README.sv.md) for instructions and commands in Swedish.

## 🔧 Project and Solution Management

Manage your projects and solutions with ease using these commands! 🛠️

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Create a new console app   | `dotnet new console`                  | Creates a new console application in the current directory. | Used to set up a simple console application.                                 |
| Create .gitignore          | `dotnet new gitignore`                | Creates a `.gitignore` file for a .NET project.             | Helps to ignore common files in version control.                             |
| Create solution            | `dotnet new sln --name MySolution`    | Creates a new .NET solution with a specified name.          | Used to organize multiple projects under a single solution.                  |
| Create class library       | `dotnet new classlib`                 | Creates a new class library.                                | Used to create reusable library code.                                        |
| Create test project        | `dotnet new xunit`                    | Creates a new xUnit test project.                           | For quickly getting started with unit testing using xUnit.                   |
| Create MVC application     | `dotnet new mvc -n MyMvcApp`          | Creates a new ASP.NET Core MVC application.                 | Used to build web applications with the MVC pattern.                         |
| Add project to solution    | `dotnet sln add MyProject.csproj`     | Adds a project to an existing solution.                     | To organize projects within a solution.                                      |
| Remove project from solution | `dotnet remove project MyLibrary.csproj` | Removes a project from a solution.                          | Useful for cleaning up solutions.                                            |
| Add project reference      | `dotnet add reference MyProject.csproj` | Adds a reference to another project.                        | Used to create dependencies between projects.                                |

## 🏗️ Building, Publishing, and Running Projects

Easily build, publish, and run your projects with the following commands. 💻

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Build project              | `dotnet build`                       | Compiles the project or solution.                          | Used to ensure that the code compiles correctly.                            |
| Clean output directories   | `dotnet clean`                       | Cleans the output directories of the project.              | Useful for starting fresh with a new build.                                  |
| Run application            | `dotnet run`                         | Runs the application from source code.                     | Great for quickly running an application during development.                 |
| Run with file watching     | `dotnet watch run`                   | Watches for changes and restarts automatically.            | Useful for development without manual restarts.                             |
| Publish in Release mode    | `dotnet publish -c Release -o ./publish` | Publishes the application to a specific folder.            | Creates a deployable version of the application for production.              |
| Publish for specific runtime | `dotnet publish -r win-x64`          | Publishes the application for a specific runtime.          | Used when deploying the application for a specific platform.                 |
| Publish self-contained     | `dotnet publish --self-contained`    | Publishes an application that does not require .NET Runtime. | For distributing applications without requiring runtime installation.       |

## 🧪 Testing and Debugging

Ensure your code is working perfectly with built-in testing tools! ✅

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Run tests                  | `dotnet test`                        | Runs all unit tests for a project.                         | Used to ensure that the code functions as expected.                         |
| Run specific tests         | `dotnet test --filter "Category=Unit"` | Runs tests that match a specific filter.                   | Useful for focusing on specific test scenarios.                             |
| Log test results           | `dotnet test --logger "trx;LogFileName=testresults.trx"` | Logs test results in `.trx` format. | Great for integrating test results into CI/CD pipelines.                     |
| Collect performance traces | `dotnet trace collect`                | Collects performance traces for a running application.     | Useful for analyzing performance issues.                                     |

## 📦 NuGet and Package Management

Manage your NuGet packages and keep your dependencies in check! 📚

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Add NuGet package          | `dotnet add package Newtonsoft.Json` | Adds a NuGet package to the project.                       | Used to include external libraries required by the project.                 |
| Remove NuGet package       | `dotnet remove package Newtonsoft.Json` | Removes a NuGet package from the project.                  | Useful for cleaning up unused packages.                                     |
| List installed packages    | `dotnet list package`                 | Lists all installed NuGet packages.                        | Provides an overview of dependencies.                                       |
| Add NuGet source           | `dotnet nuget add source "https://my-nuget-server" -n MySource` | Adds a new NuGet source. | Useful for internal package sources.                                        |
| Clear NuGet cache          | `dotnet nuget locals all --clear`     | Clears local NuGet caches.                                 | Useful for resolving cache-related issues.                                  |
| Publish NuGet package      | `dotnet nuget push MyPackage.nupkg -s https://api.nuget.org/v3/index.json -k API_KEY` | Publishes a package to a NuGet source. | To share a library via NuGet.                                               |

## 💾 Entity Framework Core

Efficiently manage your database with EF Core commands. 🗃️

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Create migration           | `dotnet ef migrations add InitialCreate` | Creates a new database migration.                          | Used to manage changes in the database schema.                              |
| Update database            | `dotnet ef database update`           | Updates the database according to the latest migrations.   | Used to apply schema changes.                                               |
| Scaffold DbContext from DB | `dotnet ef dbcontext scaffold "ConnectionString" Microsoft.EntityFrameworkCore.SqlServer` | Generates a DbContext and entities from an existing database. | Useful for generating models based on an existing database.                 |
| Remove latest migration    | `dotnet ef migrations remove`         | Removes the latest migration.                              | Used if a migration was created by mistake.                                 |

## 🛠️ Global Tools and Workloads

Install and manage global tools to extend your .NET environment. 🔧

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Install global tool        | `dotnet tool install -g dotnet-ef`    | Installs a global tool.                                    | Used to install frequently used CLI tools.                                  |
| Uninstall global tool      | `dotnet tool uninstall -g dotnet-ef`  | Uninstalls a global tool.                                  | Removes tools that are no longer needed.                                    |
| List global tools          | `dotnet tool list -g`                 | Lists all installed global tools.                          | Provides an overview of installed tools.                                    |
| Update global tools        | `dotnet tool update -g dotnet-ef`     | Updates a global tool to the latest version.               | Keeps tools up to date.                                                     |
| Install workload           | `dotnet workload install maui`        | Installs a specific workload (e.g., MAUI).                 | Used to add support for new platforms.                                      |

## 🔑 Configuration and User Secrets

Safeguard your configuration data with these commands. 🔒

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Create HTTPS certificate   | `dotnet dev-certs https --trust`      | Creates and installs a development certificate.            | Enables HTTPS on local development servers.                                 |
| Initialize user secrets    | `dotnet user-secrets init`            | Initializes a project to use user secrets.                 | Used to manage sensitive configuration data locally.                        |
| Set user secret            | `dotnet user-secrets set "MySecret" "Value"` | Adds or updates a secret for a project. | Useful for storing API keys or other sensitive data.                         |

## ⚙️ Performance Optimization and Version Management

Get the most out of your .NET apps with these performance tips! 🚀

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| Format code                | `dotnet format`                      | Formats source code according to configured rules.         | Ensures consistent code style.                                              |
| Specify SDK version        | `dotnet new globaljson --sdk-version 6.0.0` | Creates a `global.json` file to specify an SDK version.  | Ensures that the correct SDK version is used.                               |
| Optimize Release build     | `dotnet build /p:Configuration=Release` | Compiles the project in Release mode for optimized performance. | Used when preparing the application for deployment.                         |
| Migrate project            | `dotnet migrate`                      | Migrates an older project to a newer version of .NET.      | Used when upgrading older projects.                                         |

## 📜 .NET SDK and Runtime Management

Keep track of your SDKs and runtimes with these commands. 📅

| **Command**                | **Syntax**                           | **Description**                                            | **Usage**                                                                   |
|----------------------------|---------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------|
| List installed SDKs        | `dotnet --list-sdks`                  | Lists all installed .NET SDK versions.                     | Useful to see which SDK versions are available on the machine.               |
| List installed Runtimes    | `dotnet --list-runtimes`              | Lists all installed .NET Runtime versions.                 | Useful to see which runtime versions are available on the machine.           |

