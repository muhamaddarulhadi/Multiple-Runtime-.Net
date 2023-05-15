## Multiple Runtime .Net

#### Information on .Net Core Runtime on .Net Framework Runtime IIS Server

1. You can install .Net Core Runtime on .Net Framework Runtime IIS server, but, the application pool must be correct.
2. For example you have [.Net 4.8 Framework Runtime](https://dotnet.microsoft.com/en-us/download/dotnet-framework/net48) and [.Net Core 6.0 Runtime](https://dotnet.microsoft.com/en-us/download/dotnet/6.0) installed on the same IIS server; below is the application pool configuration :

    |No.|.Net                       |.NET CLR version            |Managed pipeline mode |
    |---|---------------------------|----------------------------|----------------------|
    |1. |.Net Framework application |.NET CLR Version v4.0.3.319 |Integrated            |
    |2. |.Net Core application      |No Managed Code             |Integrated            |

</BR>

#### Information on multiple runtime .Net Core version on IIS Server

1. You can install and running Multiple [Hosting Bundle](https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/hosting-bundle?view=aspnetcore-7.0) on the same IIS Server.
2. For example, you have [ASP.NET Core Runtime .Net 5.0](https://dotnet.microsoft.com/en-us/download/dotnet/5.0) hosting bundle installed on your IIS Server. If, you want to put .Net 6.0 projects inside that server, you can just download [ASP.NET Core Runtime .Net 6.0](https://dotnet.microsoft.com/en-us/download/dotnet/6.0) hosting bundle and install it.
3. The installer itself will tell you if a restart is needed. Restart is needed only if some files are currently in use.
4. After that, you can straight away create your web application .Net 6.0 on IIS Manager.

#### Information on .Net Framework 4.8 and .Net Core(s)

1. You can install both runtime and running it on 1 server.

</BR>

#### Reference

1. [Publish an ASP.NET Core app to IIS](https://learn.microsoft.com/en-us/aspnet/core/tutorials/publish-to-iis?view=aspnetcore-6.0&tabs=netcore-cli)
2. [Host ASP.NET Core on Windows with IIS](https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/?view=aspnetcore-6.0)
3. [The .NET Core Hosting Bundle](https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/iis/hosting-bundle?view=aspnetcore-6.0)
4. [Running .NET Core Apps on a Framework other than Compiled Version?](https://weblog.west-wind.com/posts/2021/Jun/15/Running-NET-Core-Apps-on-a-Framework-other-than-Compiled-Version)
5. [Can I keep netcore 2.2 runtime and 3.1 in the same server without conflict?](https://social.msdn.microsoft.com/Forums/en-US/36c3ec02-f2ba-4b15-8abd-11105b13635a/can-i-keep-netcore-22-runtime-and-31-in-the-same-server-without-conflict?forum=aspdotnetcore)
6. [Is it possible to install more than one version of .NET on a server?](https://serverfault.com/questions/317266/is-it-possible-to-install-more-than-one-version-of-net-on-a-server)
7. [If .Net 6 is installed on IIS will my .Net Core 3.1 app work](https://www.reddit.com/r/csharp/comments/vd5305/if_net_6_is_installed_on_iis_will_my_net_core_31/)
8. [Can I host multiple versions of ASP.NET Core websites at the same time on IIS server](https://stackoverflow.com/questions/70908316/can-i-host-multiple-versions-of-asp-net-core-websites-at-the-same-time-on-iis-se)
9. [ASP.NET Core 6 Self Hosted Windows Service without IIS (duplicate)](https://stackoverflow.com/questions/70792231/asp-net-core-6-self-hosted-windows-service-without-iis)
10. [ASP.NET Core .NET 6 Preview 7 Windows Service](https://stackoverflow.com/questions/69124310/asp-net-core-net-6-preview-7-windows-service)
11. [An asp.net core web api application, using "UseWindowsService", reports an error “System.NotSupportedException: The content root changed. Changing the host configuration is not supported ” when starting the service](https://github.com/dotnet/AspNetCore.Docs/issues/23387)
12. [Self-Contained Applications: Great Tool in .NET 6](https://blog.inedo.com/dotnet/self-contained-applications)
13. [ReadyToRun Compilation](https://learn.microsoft.com/en-us/dotnet/core/deploying/ready-to-run)
14. [How to create a self contained .Net core application?](https://dotnetthoughts.net/how-to-create-a-self-contained-dotnet-core-application/)
15. [Can I deploy .net core 3.1 and .net framework sites on IIS 8.5 at the same time?](https://stackoverflow.com/questions/60009247/can-i-deploy-net-core-3-1-and-net-framework-sites-on-iis-8-5-at-the-same-time)
16. [.Net core and .Net framework in same on premise web server IIS8.0](https://social.msdn.microsoft.com/Forums/en-US/f9b21394-a3a2-4c6c-a83d-67d18233cf8e/net-core-and-net-framework-in-same-on-premise-web-server-iis80?forum=iis7general)
17. [.NET and .NET core on same IIS server](https://serverfault.com/questions/978586/net-and-net-core-on-same-iis-server)
18. [Install .NET Core, ASP.NET Core](https://www.tutorialsteacher.com/core/aspnet-core-environment-setup)
19. [Install .NET on Windows](https://learn.microsoft.com/en-us/dotnet/core/install/windows?tabs=net70)
20. [.NET Core vs .NET Framework: How to Pick a .NET Runtime for an Application](https://stackify.com/net-core-vs-net-framework/)
21. [Side-by-Side Execution in the .NET Framework](https://learn.microsoft.com/en-us/dotnet/framework/deployment/side-by-side-execution)
22. [Multiple versions of .NET on the same server](https://stackoverflow.com/questions/49164607/multiple-versions-of-net-on-the-same-server)
