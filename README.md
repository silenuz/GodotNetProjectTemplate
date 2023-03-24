# GodotNetProjectTemplate

A project template for creating a Godot .Net core project for the Godot game engine.

Hopefully I'll have nuget packages soon to ease the install process.


### Installing

Clone Repo

Copy the Godot.Net.Template folder to where you want it live, as this is the template source that will be used for generation.  
So remember to uninstall the template before deleting the folder.

After copying the folder, open a terminal in the Godot.Net.template folder and execute:

### Net 7.0

    Windows:

    dotnet new install .\

    Linux:

    dotnet new install .

    Mac:

    dotnet new install ./

### Net 6.0

    Windows:

    dotnet new --install .\

    Linux:

    dotnet new --install .

    Mac:

    dotnet new --install ./

### Usage is simple

`dotnet new Godot -o {NameOfProject} -G {PathToGodtotExe}`

Note on windows it is currently necessary to escape the back slashes in the godot exe path, for example if the exe is

`C:\Godot\Godot4.exe`

You would use:

`dotnet new Godot -o {NameOfProject} -G c:\\Godot\\Godot4.ex`

This will create a project that already has the necessary launch settings for running or debugging your code in Visual Studio or Jetbrains' Rider.

After creating the project simply open it int Godot editor and start working.

If you are creating the project as a child project of a solution, or running the template from an IDE such as Visual Studio or Rider, then you would pass a third argument to DotNet New , setting EnabledManagedSolution to true like so:

`dotnet new Godot -o {NameOfProject} -G {PathToGodtotExe} -E true`

Note that while this template will be available from the IDE project types in Rider and Visual Studio, it is best to use the command line to create the project, 
and then use add existing project to add it to the current solution, as there is no way in Rider nor Visual Studio to fill in the above parameter, which means the 
solution file generated in the project folder will have to be removed, and the solution folder path set in the Godot editor to fix it.  

Editor->Project Settings Enable advanced

Scroll down to Dotnet and set the solution folder to be the correct path.

This will automatically adjust the solution path in the Godot project file.

By default the project is created targeting Net 6.0, if you wish it to target Net 7.0 then use the -F argument like so:

`dotnet new Godot -o {NameOfProject} -G {PathToGodtotExe} -F net7.0`

`dotnet new Godot -h` will return a list of the parameters and their descriptions.

### Uninstalling

Open a terminal in the Godot.Net.template folder and execute:

### Net 7.0

    Windows:

    dotnet new uninstall .\

    Linux:

    dotnet new uninstall .

    Mac:

    dotnet new uninstall ./

### Net 6.0

    Windows:

    dotnet new --uninstall .\

    Linux:

    dotnet new --uninstall .

    Mac:

    dotnet new --uninstall ./
