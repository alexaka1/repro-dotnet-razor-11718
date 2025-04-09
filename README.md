# [dotnet/razor#11718](https://github.com/dotnet/razor/issues/11718) issue repro

You need 
- .Net 9 SDK
- `dotnet workload install wasm-tools` (elevated shell might be needed)

## Repro

1. Look at `BlazorWasmAot/BlazorWasmAot.Client/Pages/Counter.razor`. Should be standard Blazor
2. Look at `BlazorWasmAot/BlazorWasmAot.Client/BlazorWasmAot.Client.csproj:10` and below. AOT is enabled.
3. dotnet build -c Release
4. Observe 8 warnings of `IL2091` in the console
