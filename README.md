# .NET starter

[![Deploy on velixir](https://velixir.net/img/deploy-on-velixir.svg)](https://velixir.net/new?template=dotnet-minimal-api)

One `Program.cs`, one project file, no controllers. ASP.NET Core picks up the port the
platform injects automatically, so there is nothing to configure before it serves traffic.

[Deploy it on velixir](https://velixir.net/new?template=dotnet-minimal-api).

## Running it locally

```bash
dotnet run
```

## Deploying

```bash
velixir deploy
```

Deploy the folder that **contains** the `.csproj`, not `bin/Release/net10.0/publish`.
velixir builds from source; a publish output has no project file in it, so there is nothing
for the build to do.

## Note on PORT

Nothing here reads `PORT` directly. velixir sets `ASPNETCORE_HTTP_PORTS` and ASP.NET Core
binds it on startup, so leave Kestrel alone unless you have a reason not to.

## Licence

MIT.
