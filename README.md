# PowerShell-GUI-Starter
A starter for designing a GUI using WPF and presenting it via PowerShell.

## Pre-Requisites
You need the following extensions added to Visual Studio:
1. [Git Extensions](https://gitextensions.github.io/)
1. [XAML Styler for Visual Studio 2022](https://marketplace.visualstudio.com/items?itemName=TeamXavalon.XAMLStyler2022)
1. You need to SMS Admin PowerShell module installed

## Getting Started
To start from scratch, do the following:
1. Using PowerShell, navigate to the folder where you want to create a new Repository:
```PowerShell
md src
```
1. Start Visual Studio
1. Select `Open a local folder`
1. Select the folder where you wanted to create your new repository.
1. In the `Solution Explorer` double-click on `Folder View`.
1. Right click on the ROOT folder > Add > New Folder.  Name the folder `src`.  This folder will hold the WPF project that will allow the developer to use the designer to create the XAML form that the GUI will use.
1. Right click on the ROOT folder > Add > New Folder.  Name the folder `PoshGUI`.  This folder will hold the assets required to **run* the new GUI.
1. Right Click on the folder `PoshGUI` and select Add > new File.  Name the new file `PoshGUI.ps1`.
1. Right click on the folder `PoshGUI` and select Add > new file.  Name the file `PoshGUI.xaml`.

### Create the WPF project
1. Right click on the `src` folder and select `Open in Terminal`.
1. In the `Terminal` window type:
```cmd
dotnet new sln -n PoshGUI
dotnet new wpf -n PoshGUI
```
1. In the `Solution Explorer` use the `refresh` button.
1. Expand the `scr` folder, and double-click on the `PoshGUI.sln` file.
1. In the `Solution Explorer`, right-click on the `Solution 'PoshGUI' (0 projects)` and select Add > Existing Project.
1. Navigate to the `src\PoshGUI` folder created earlier.
1. Select the `PoshGUI.csproj` file and click on `open`.

### END structure
The complete folder structure should be along the lines of:
```
\src
	\PoshGUI
		\App.xaml
		\App.xaml.cs
		\AssemblyInfo.cs
		\MainWindow.xaml
		\MainWindow.xaml.cs
		\PoshGUI.csproj
	\PoshGUI.sln
\PoshGUI
	\PoshGUI.ps1
	\PoshGUI.xaml
```

## What's next?
1. Use the WPF project to DESIGN any GUI form, by editing the `src\PoshGUI\MainWindow.xaml` file.
1. After updating the WPF project, always copy the **content** of the file into the file `\PoshGUI\PoshGUI.xaml`.
1. Add any `assets`, such as icons, images, etc. to the `\PoshGUI` folder.

### Making changes
GitHub is your repository for all the source code and versions.  As more than 1 person can make changes it is important that you correctly manage your GIT.
All changes are assuming you are using Visual Studio and have the solution (SLN) loaded.

#### PULL - The latest version from GitHub
ALWAYS **PULL** to get the latest version from source control! This will ensure that you have locally the **latest version** of the `main` branch from GitHub.
1. GIT > PULL

#### COMMIT - Changes locally
It is a good idea to `commit` changes you make to your local copy GIT (think of it like a database), so that you don't loose any changes.  NOTE: These changes are local to you and only you!  Anyone doing a GIT > PULL will not see your changes at this time!
1. Git > Commit or Stash
1. In the `Git Changes` view, review the changed files, add a message explaining the reason for the changes, and click on `Commit All`.

#### PUSH - Local changes up to GitHub
When you have `committed` changes that you want to make to the repository on GitHub, and to make them available to all users:
1. Git > Push