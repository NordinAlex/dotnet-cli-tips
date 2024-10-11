# 🌐 .NET CLI Tips

📚 En omfattande och välorganiserad guide och tips till viktiga `.NET` CLI-kommandon för utvecklare, inklusive kommandosyntax, beskrivningar och exempel på användning.


📋 **Innehållsförteckning**
- [🚀 Komma igång](#-komma-igång)
- [🔧 Projekt- och Lösningshantering](#-projekt--och-lösningshantering)
- [🏗️ Bygga, Publicera och Köra Projekt](#%EF%B8%8F-bygga-publicera-och-köra-projekt)
- [🧪 Testning och Felsökning](#-testning-och-felsökning)
- [📦 NuGet och Paketadministration](#-nuget-och-paketadministration)
- [💾 Entity Framework Core](#-entity-framework-core)
- [🛠️ Globala Verktyg och Arbetsbelastningar](#%EF%B8%8F-globala-verktyg-och-arbetsbelastningar)
- [🔑 Konfiguration och Användarhemligheter](#-konfiguration-och-användarhemligheter)
- [⚙️ Prestandaoptimering och Versionshantering](#%EF%B8%8F-prestandaoptimering-och-versionshantering)
- [📜 .NET SDK och Runtime-administration](#-net-sdk-och-runtime-administration)

## 🚀 Komma igång

Välkommen till **.NET CLI Tips**! 🎉 Detta repository är tänkt att göra det enklare att arbeta med `.NET`-kommandoradsverktyg för utvecklare. Oavsett om du hanterar projekt, kör tester eller distribuerar applikationer hittar du det du behöver här.

🇸🇪 **Letar du efter den engelska versionen?** Kolla in [Engelska Versionen](README.md) för instruktioner och kommandon på engelska.

## 🔧 Projekt- och Lösningshantering

Hantera dina projekt och lösningar enkelt med dessa kommandon! 🛠️

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Skapa ny konsolapplikation   | `dotnet new console`                  | Skapar en ny konsolapplikation i den aktuella katalogen.   | Används för att sätta upp en enkel konsolapplikation.                           |
| Skapa .gitignore             | `dotnet new gitignore`                | Skapar en `.gitignore`-fil för ett .NET-projekt.           | Hjälper till att ignorera vanliga filer i versionskontroll.                     |
| Skapa lösning                | `dotnet new sln --name MySolution`    | Skapar en ny .NET-lösning med ett angivet namn.            | Används för att organisera flera projekt under en lösning.                      |
| Skapa klassbibliotek         | `dotnet new classlib`                 | Skapar ett nytt klassbibliotek.                           | Används för att skapa återanvändbar bibliotekskod.                              |
| Skapa testprojekt            | `dotnet new xunit`                    | Skapar ett nytt xUnit-testprojekt.                         | För att snabbt komma igång med enhetstestning med xUnit.                        |
| Skapa MVC-applikation        | `dotnet new mvc -n MyMvcApp`          | Skapar en ny ASP.NET Core MVC-applikation.                 | Används för att bygga webbapplikationer med MVC-mönstret.                       |
| Lägg till projekt i lösning  | `dotnet sln add MyProject.csproj`     | Lägger till ett projekt i en befintlig lösning.            | För att organisera projekt inom en lösning.                                    |
| Ta bort projekt från lösning | `dotnet remove project MyLibrary.csproj` | Tar bort ett projekt från en lösning.                      | Användbart för att städa upp lösningar.                                        |
| Lägg till projektreferens    | `dotnet add reference MyProject.csproj` | Lägger till en referens till ett annat projekt.            | Används för att skapa beroenden mellan projekt.                                 |

## 🏗️ Bygga, Publicera och Köra Projekt

Bygg, publicera och kör dina projekt enkelt med följande kommandon. 💻

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Bygg projekt                 | `dotnet build`                       | Kompilerar projektet eller lösningen.                     | Används för att säkerställa att koden kompileras korrekt.                       |
| Rensa output-kataloger       | `dotnet clean`                       | Rensar projektets output-kataloger.                       | Användbart för att börja om med en ny build.                                    |
| Kör applikation              | `dotnet run`                         | Kör applikationen från källkoden.                         | Bra för att snabbt köra en applikation under utveckling.                        |
| Kör med filövervakning       | `dotnet watch run`                   | Övervakar ändringar och startar om automatiskt.           | Användbart för utveckling utan manuella omstarter.                             |
| Publicera i Release-läge     | `dotnet publish -c Release -o ./publish` | Publicerar applikationen till en specifik katalog.       | Skapar en körbar version av applikationen för produktion.                       |
| Publicera för specifik runtime | `dotnet publish -r win-x64`          | Publicerar applikationen för en specifik runtime.         | Används när applikationen ska distribueras för en viss plattform.                |
| Publicera självständig       | `dotnet publish --self-contained`    | Publicerar en applikation som inte kräver .NET Runtime.   | För att distribuera applikationer utan krav på runtime-installation.            |

## 🧪 Testning och Felsökning

Säkerställ att din kod fungerar perfekt med inbyggda testverktyg! ✅

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Kör tester                  | `dotnet test`                        | Kör alla enhetstester för ett projekt.                    | Används för att säkerställa att koden fungerar som förväntat.                    |
| Kör specifika tester        | `dotnet test --filter "Category=Unit"` | Kör tester som matchar ett specifikt filter.             | Användbart för att fokusera på specifika testscenarier.                         |
| Logga testresultat          | `dotnet test --logger "trx;LogFileName=testresults.trx"` | Loggar testresultat i `.trx`-format. | Bra för att integrera testresultat i CI/CD-pipelines.                          |
| Samla prestandaspår         | `dotnet trace collect`                | Samlar in prestandaspår för en körande applikation.       | Användbart för att analysera prestandaproblem.                                  |

## 📦 NuGet och Paketadministration

Hantera dina NuGet-paket och håll koll på dina beroenden! 📚

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Lägg till NuGet-paket       | `dotnet add package Newtonsoft.Json` | Lägger till ett NuGet-paket till projektet.               | Används för att inkludera externa bibliotek som projektet behöver.               |
| Ta bort NuGet-paket         | `dotnet remove package Newtonsoft.Json` | Tar bort ett NuGet-paket från projektet.                 | Användbart för att städa upp oanvända paket.                                     |
| Lista installerade paket    | `dotnet list package`                 | Listar alla installerade NuGet-paket.                     | Ger en översikt över beroenden.                                                |
| Lägg till NuGet-källa       | `dotnet nuget add source "https://my-nuget-server" -n MySource` | Lägger till en ny NuGet-källa. | Användbart för interna paketkällor.                                            |
| Rensa NuGet-cache           | `dotnet nuget locals all --clear`     | Rensar lokala NuGet-cachemappar.                          | Användbart för att lösa cache-relaterade problem.                               |
| Publicera NuGet-paket       | `dotnet nuget push MyPackage.nupkg -s https://api.nuget.org/v3/index.json -k API_KEY` | Publicerar ett paket till en NuGet-källa. | För att dela ett bibliotek via NuGet.                                          |

## 💾 Entity Framework Core

Hantera dina databaser effektivt med EF Core-kommandon. 🗃️

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Skapa migration             | `dotnet ef migrations add InitialCreate` | Skapar en ny databas-migration.                           | Används för att hantera ändringar i databasschemat.                             |
| Uppdatera databas           | `dotnet ef database update`           | Uppdaterar databasen enligt de senaste migrationerna.     | Används för att applicera schemaändringar.                                      |
| Generera DbContext från databas | `dotnet ef dbcontext scaffold "ConnectionString" Microsoft.EntityFrameworkCore.SqlServer` | Skapar en DbContext och entiteter från en befintlig databas. | Användbart för att skapa modeller baserat på en existerande databas.           |
| Ta bort senaste migrationen | `dotnet ef migrations remove`         | Tar bort den senaste migrationen.                         | Används om en migration skapades av misstag.                                    |

## 🛠️ Globala Verktyg och Arbetsbelastningar

Installera och hantera globala verktyg för att utöka din .NET-miljö. 🔧

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Installera globalt verktyg | `dotnet tool install -g dotnet-ef`    | Installerar ett globalt verktyg.                          | Används för att installera ofta använda CLI-verktyg.                            |
| Avinstallera globalt verktyg| `dotnet tool uninstall -g dotnet-ef`  | Avinstallerar ett globalt verktyg.                        | Tar bort verktyg som inte längre behövs.                                       |
| Lista globala verktyg       | `dotnet tool list -g`                 | Visar alla installerade globala verktyg.                   | Ger en översikt över installerade verktyg.                                      |
| Uppdatera globala verktyg   | `dotnet tool update -g dotnet-ef`     | Uppdaterar ett globalt verktyg till den senaste versionen. | Håller verktygen uppdaterade.                                                   |
| Installera arbetsbelastning | `dotnet workload install maui`        | Installerar en specifik arbetsbelastning (t.ex. MAUI).     | Används för att lägga till stöd för nya plattformar.                            |

## 🔑 Konfiguration och Användarhemligheter

Skydda din konfigurationsdata med dessa kommandon. 🔒

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Skapa HTTPS-certifikat      | `dotnet dev-certs https --trust`      | Skapar och installerar ett utvecklingscertifikat.         | Möjliggör HTTPS på lokala utvecklingsservrar.                                   |
| Initiera användarhemligheter| `dotnet user-secrets init`            | Initierar ett projekt för att använda användarhemligheter. | Används för att hantera känslig konfigurationsdata lokalt.                      |
| Sätt användarhemlighet      | `dotnet user-secrets set "MySecret" "Value"` | Lägger till eller uppdaterar en hemlighet för ett projekt. | Användbart för att lagra API-nycklar eller annan känslig data.                   |

## ⚙️ Prestandaoptimering och Versionshantering

Få ut det mesta av dina .NET-appar med dessa prestandatips! 🚀

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Formatera kod               | `dotnet format`                      | Formaterar källkoden enligt konfigurerade regler.          | För att säkerställa enhetlig kodstil.                                           |
| Specificera SDK-version     | `dotnet new globaljson --sdk-version 6.0.0` | Skapar en `global.json`-fil för att ange en SDK-version. | För att säkerställa att rätt SDK-version används.                              |
| Optimera Release-build      | `dotnet build /p:Configuration=Release` | Kompilerar projektet i Release-läge för optimerad prestanda. | Används när applikationen förbereds för distribution.                          |
| Migrera projekt             | `dotnet migrate`                      | Migrerar ett äldre projekt till en nyare version av .NET.  | Används vid uppgradering av äldre projekt.                                      |

## 📜 .NET SDK och Runtime-administration

Håll koll på dina SDK:er och runtime-versioner med dessa kommandon. 📅

| **Kommando**                 | **Syntax**                           | **Beskrivning**                                           | **Användning**                                                                 |
|------------------------------|---------------------------------------|-----------------------------------------------------------|--------------------------------------------------------------------------------|
| Lista installerade SDK:er   | `dotnet --list-sdks`                  | Visar alla installerade .NET SDK-versioner.                | Användbart för att se vilka SDK-versioner som är tillgängliga på maskinen.       |
| Lista installerade Runtimes | `dotnet --list-runtimes`              | Visar alla installerade .NET Runtime-versioner.            | Användbart för att se vilka runtime-versioner som är tillgängliga på maskinen.   |
