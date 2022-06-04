# How to create and deply ASP.NET app on Windows server 12

## Creating Application

### Prerequisite
  * Install latest Visual Studio IDE - [Download Page](https://visualstudio.microsoft.com/vs/)


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

## Deploying Application
### Prerequisite
  * Follow the steps to install IIS on Windows server - [Link](https://www.youtube.com/watch?v=1VdxPWwtISA)
  * Install ASP.NET Core runtime - [Download link](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-aspnetcore-6.0.5-windows-hosting-bundle-installer)
  * Opening port 5100 through firewall
    * Open _Windows Defender Firewall_ -> _Click Advanced Settings_ -> _Inbound Rule_.
    * Create new Rule -> Select _Port_ -> provide port as 5100 -> Keep all other settings to default.
    * Provide a name to this rule.

### Deploying application
  * Create a folder under C:/inetpub/<project_name>
  * Copy the contents of the package folder created in previous step under this folder
  * Open IIS Server -> Under Connections -> Add Website
  * Provide application name in _Site name_
  * Select _Physical path_ as C:/inetpub/<project_name>
  * Set port to 5100, click ok
