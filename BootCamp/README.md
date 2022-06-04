#How to create and deply ASP.NET app on Windows server 12

## Creating Application

### Prerequisite
  * Install latest Visual Studio IDE - [Download Page] (https://visualstudio.microsoft.com/vs/)

## Deploying Application
  * Creating Demo Application
    * Open Visual Studio editor and select File -> New -> Project
    * Select ASP.NET Core Web App. Provide _Project name_ and _Location_. Keep rest of the options to default.
    * It will create a sample application with default pages.
    * To run application on port 5100, update applicationUrl parameter in below file,
    **  <Application Name>/Properties/launchSettings.json
  * Packaging the application
    * This step will create the package of the application that we have created.
    * Create a new folder where we can create the application package files
    * From Visual Studio menu select Build-> Publish -> New -> Folder.
    * select the folder created for packaging. This will create a publish profile.
    * Click on _Publish_ button. This process will generate files for deployment.    
    

### Prerequisite
  * Install ASP.NET Core runtime - [Download link] (https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-6.0.5-windows-hosting-bundle-installer)