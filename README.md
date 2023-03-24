# GodotNetProjectTemplate

A project template for creating a Godot .Net core project for the Godot game engine.

### Usage is simple

dotnet new Godot -o {NameOfProject} -G {PathToGodtotExe}

This will create a project that already has the necessary launch settings for running or debugging your code in Visual Studio or Jetbrains' Rider.

After creating the project simply open it int Godot editor and start working.

If you are creating the project as a child project of a solution, or running the template from an IDE such as Visual Studio or Rider, then you would pass a third argument to DotNet New , setting EnabledManagedSolution to true like so:

dotnet new Godot -o {NameOfProject} -G {PathToGodtotExe} -E true

This will automatically adjust the solution path in the Godot project file.

By default the project is created targeting Net 6.0, if you wish it to target Net 7.0 then use the -F argument like so:

dotnet new Godot -o {NameOfProject} -G {PathToGodtotExe} -F net7.0

dotnet new Godot -h will return a list of the parameters and their descriptions.
