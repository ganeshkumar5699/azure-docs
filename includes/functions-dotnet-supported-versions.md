---
author: ggailey777
ms.service: azure-functions
ms.topic: include
ms.date: 01/16/2023
ms.author: glenga
---

## Supported versions

Versions of the Functions runtime support specific versions of .NET. To learn more about Functions versions, see [Azure Functions runtime versions overview](../articles/azure-functions/functions-versions.md). Version support also depends on whether your functions run in-process or isolated worker process. 

>[!NOTE]
>To learn how to change the Functions runtime version used by your function app, see [view and update the current runtime version](../articles/azure-functions/set-runtime-version.md#view-and-update-the-current-runtime-version).

The following table shows the highest level of .NET or .NET Framework that can be used with a specific version of Functions. 

| Functions runtime version | In-process<br/>([.NET class library](../articles/azure-functions/functions-dotnet-class-library.md)) | Isolated worker process<br/>([.NET Isolated](../articles/azure-functions/dotnet-isolated-process-guide.md)) |
| ---- | ---- | --- |
| Functions 4.x | .NET 6.0<sup>1</sup>  | .NET 6.0<sup>1</sup><br/>.NET 7.0<sup>2</sup><br/>.NET Framework 4.8<sup>3</sup><br/>.NET 8.0 (Preview)<sup>4</sup> |
| Functions 1.x<sup>5</sup> | .NET Framework 4.8 | n/a |

<sup>1</sup> Per the [.NET Official Support Policy], .NET 6 will reach end of support on November 12, 2024.

<sup>2</sup> Per the [.NET Official Support Policy], .NET 7 will reach end of support on May 14, 2024.

<sup>3</sup> Build process also requires [.NET 6 SDK](https://dotnet.microsoft.com/download).

<sup>4</sup> Preview support for .NET 8 function apps is currently limited to Linux applications. To develop using .NET 8 Preview SDKs in Visual Studio, you must use [Visual Studio 2022 Preview](https://visualstudio.microsoft.com/vs/preview/). Within Visual Studio, you must also get the latest toolset and template updates by navigating to `Tools->Options`, selecting `Azure Functions` under `Projects and Solutions`, and then clicking the `Check for updates` button and installing updates as prompted.

<sup>5</sup>[Support will end for version 1.x of the Azure Functions runtime on September 14, 2026](https://aka.ms/azure-functions-retirements/hostv1). We highly recommend that you [migrate your apps to version 4.x](../articles/azure-functions/migrate-version-1-version-4.md) for full support.

For the latest news about Azure Functions releases, including the removal of specific older minor versions, monitor [Azure App Service announcements](https://github.com/Azure/app-service-announcements/issues).

[.NET Official Support Policy]: https://dotnet.microsoft.com/platform/support/policy
