# .NET

### Installation

The Appconfi .NET SDK is available as a Nuget package, to install run the following command in the [Package Manager Console](https://docs.microsoft.com/en-us/nuget/consume-packages/install-use-packages-visual-studio)
```
Install-Package Appconfi
```
More info is available on [nuget](https://www.nuget.org/packages/Appconfi/)

### Usage

In order to use the Appconfi you will need to [create an account](https://appconfi.com/account/register).

From there you can create your first application and setup your configuration. To use the Appconfi API to access your configuration go to `/accesskeys` there you can find the `application_id` and your `application_secret`.

### How to use

```csharp

var manager = Configuration.NewInstance(applicationId, apiKey);

//Start monitoring changes
manager.StartMonitor();

//Access your application setting
var  mySetting = manager.GetSetting("my_application_setting");

//Check if a feature toggle is enable
var isEnabled = manager.IsFeatureEnabled("awesome_feature");

```

### Optional parameters

Change your environments:

```csharp

//Define your environment
var env = "PRODUCTION";

//Define a refresh interval for your configuration
var refreshInterval =  TimeSpan.FromSeconds(10);

//Define a function to resolve your setting in case of error
Func<string,string> getSetting = (key)=>ConfigurationManager.AppSettings[key];

//Define a function to check the feature toggle in case of error
Func<string,bool> getFeatureToggle = (key)=>YourToggleManager.IsEnabled(key);

//Logs errors
var logger = new MyCustomLogger()

var manager = Configuration.NewInstance(
    applicationId, 
    apiKey, 
    env, 
    refreshInterval, 
    getSetting, 
    getFeatureToggle,
    logger);

```
