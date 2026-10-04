# spoel

*noun · Dutch*

**English:** spool, bobbin, reel.

A cylindrical holder around which thread, yarn, or film is wound. ([Dictionary](https://dictionary.cambridge.org/dictionary/dutch-english/spoel))

---

**spoel** is a distributed task execution project in early development. The planned first workload renders independent procedural-art frames and assembles them into an animation.

Currently, the application only exposes a liveness endpoint. Task execution, persistence, workers, rendering, and a frontend are not implemented but will be coming soon.

## Run locally

Install .NET SDK **10.0.401**, matching `global.json`. If using Visual Studio, use Visual Studio 2026 with the ASP.NET and web development workload. VS Code or the command line also work.

From the repository root:

```sh
dotnet build Spoel.sln
dotnet run --project src/Spoel.csproj --no-launch-profile -- --urls http://127.0.0.1:5080
```

Open <http://127.0.0.1:5080/health/live>. Expect HTTP **200** with the text **Healthy**. Stop the app with Ctrl+C. The root URL `/` has no page.
