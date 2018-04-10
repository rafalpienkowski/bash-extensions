# This repository contains handy bash extensions.

I'm going to add new scripts which in my opinion would be useful for a .Net dev.

Available scripts:
- dotnet-solution

This script creates a basic solution's folder structure. It initializes main project and dedicated test project. Created test project contains the reference to the main project. It has also referenced two handy NuGet packages: [FluentAssertions](https://fluentassertions.com) and [Moq](https://github.com/Moq/moq4/wiki/Quickstart). Creates sln file which could be beneficial for devs which plan to open the solution via full Visual Studio. In the end, Visual Studio Code will be opened.

Usage: 

```
dotnet-solution [solution-name] [main-project-name] <<template>>
```

The template name is passed to the [dotnet new] command. It will be used to create the new dotnet project based on it. More about templates you can be found under this [link](https://docs.microsoft.com/en-us/dotnet/core/tools/dotnet-new).

Example: 

```
dotnet-solution adventure-works AdventureWorks.Common classlib
```

Solution structure which will be created by the example above. I've intentionally omitted some folders.

```
+-- adventure-works
|   +-- src
|       +-- AdventureWorks.Common
|       |   +-- Class1.cs
|       |   +-- AdventureWorks.Common.csproj
|   +-- test
|       +-- AdventureWorks.Common.Tests
|       |   +-- UnitTest1.cs
|       |   +-- AdventureWorks.Common.Tests.csproj
+-- adventure-works.sln
```

To add a specific extension to your bash shell you need:
- download it to your machine
- copy to /usr/bin catalog (admin rights will be required)
- make it executable by _chmod_ command (admin rights will be required)
```
    chmod +x dotnet-solution
```

Feel free to copy, use and modify those scripts. I'm also open to all your suggestions.