
## run locally
```sh
# The system cannot find the file specified.
 C:\Users\1905028\AppData\Local\AzureFunctionsTools\Releases\3.47.0\cli_x64\func.exe host start --csharp --useHttps --cert WingetRest_TemporaryKey.pfx --password 12345
```

```sh
 host start --useHttps --cert $(ProjectDir)WingetRest_TemporaryKey.pfx --password 12345
```


```sh
# ok
 C:\Users\1905028\AppData\Local\AzureFunctionsTools\Releases\3.47.0\cli_x64\func.exe host start --useHttps --cert D:\project\winget\winget-cli-restsource\src\WinGet.RestSource.Functions\WingetRest_TemporaryKey.pfx --password 12345
```

## Publish
```sh
C:\Users\1905028\AppData\Local\AzureFunctionsTools\Releases\3.47.0\cli_x64\func.exe  azure functionapp publish <app_name>

C:\Users\1905028\AppData\Local\AzureFunctionsTools\Releases\3.47.0\cli_x64\func.exe  azure functionapp publish WinGetRestSourceFunctions

C:\Users\1905028\AppData\Local\AzureFunctionsTools\Releases\3.47.0\cli_x64\func.exe  azure functionapp publish WinGetRestSourceFunctions --csharp
```


C:\Users\1905028\AppData\Local\AzureFunctionsTools\Releases\3.47.0\cli_x64\func.exe  azure functionapp logstream WinGetRestSourceFunctions


func azure functionapp publish kimi-function  --javascript
func azure functionapp publish WinGetRestSourceFunctions
func azure functionapp publish WinGetRestSourceFunctions --dotnet-version '6.0'


https://wingetrestsourcefunctions.azurewebsites.net/api

https://kimi-function.azurewebsites.net/api/simple-interest?code=o5yWARU2NYXnuZi27uFpDyCGIIFGZz0HM-CcQsk7D5P0AzFumV8zwg==&principal=5000&rate=.035&term=36


az functionapp config set --net-framework-version v6.0 -g <RESOURCE_GROUP_NAME> -n <APP_NAME>
az functionapp config set --net-framework-version v6.0 -g winget -n WinGetRestSourceFunctions

az functionapp config set --net-framework-version dotnetcore3 -g winget -n WinGetRestSourceFunctions



```sh
PS D:\tmp\winget-cli-restsource\src\WinGet.RestSource.Functions> func azure functionapp publish  --h

                  %%%%%%
                 %%%%%%
            @   %%%%%%    @
          @@   %%%%%%      @@
       @@@    %%%%%%%%%%%    @@@
     @@      %%%%%%%%%%        @@
       @@         %%%%       @@
         @@      %%%       @@
           @@    %%      @@
                %%
                %

Usage: func azure functionapp <action> [-/--options]

Actions: 
fetch-app-settings  Retrieve App Settings from your Azure-hosted Function App and store locally Aliases: fetch-app-settings, fetch
    <FunctionAppName> Function App name
    --slot               The deployment slot in the function app to use (if configured)
    --access-token       Access token to use for performing authenticated azure actions
    --access-token-stdin Read access token from stdin e.g: az account get-access-token | func ... --access-token-stdin
    --management-url     Management URL for Azure Cloud e.g: --management-url https://management.azure.com.
    --subscription       Default subscription to use

list-functions      List functions in a given function app on azure.
    <FunctionAppName> Function App name
    --show-keys          Shows function links with their keys.
    --slot               The deployment slot in the function app to use (if configured)
    --access-token       Access token to use for performing authenticated azure actions
    --access-token-stdin Read access token from stdin e.g: az account get-access-token | func ... --access-token-stdin
    --management-url     Management URL for Azure Cloud e.g: --management-url https://management.azure.com.
    --subscription       Default subscription to use

logstream           Show interactive streaming logs for an Azure-hosted Function App
    <FunctionAppName> Function App name
    --browser            Open Azure Application Insights Live Stream in a browser.
    --slot               The deployment slot in the function app to use (if configured)
    --access-token       Access token to use for performing authenticated azure actions
    --access-token-stdin Read access token from stdin e.g: az account get-access-token | func ... --access-token-stdin
    --management-url     Management URL for Azure Cloud e.g: --management-url https://management.azure.com.
    --subscription       Default subscription to use

publish             Publish the current directory contents to an Azure Function App. Locally deleted files are not removed from destination.  
    <FunctionAppName> Function App name
    --publish-local-settings [-i] Updates App Settings for the function app in Azure during deployment.
    --publish-settings-only [-o]  Only publish settings and skip the content. Default is prompt.
    --overwrite-settings [-y]     Only to be used in conjunction with -i or -o. Overwrites AppSettings in Azure with local value if different 
                                  . Default is prompt.
    --list-ignored-files          Displays a list of files that will be ignored from publishing based on .funcignore
    --list-included-files         Displays a list of files that will be included in publishing based on .funcignore
    --nozip                       Turns the default Run-From-Package mode off.
    --build-native-deps           Skips generating .wheels folder when publishing python function apps.
    --build [-b]                  Perform build action when deploying to a Linux function app. (accepts: remote, local)
    --no-bundler                  [Deprecated] Skips generating a bundle when publishing python function apps with build-native-deps.
    --show-keys                   Adds function keys to the URLs displayed in the logs.
    --additional-packages         List of packages to install when building native dependencies. For example: "python3-dev libevent-dev"      
    --force                       Depending on the publish scenario, this will ignore pre-publish checks
    --csx                         use old style csx dotnet functions
    --no-build                    Skip building and fetching dependencies for the function project.
    --dotnet-cli-params           When publishing dotnet functions, the core tools calls 'dotnet build --output bin/publish --configuration r 
                                  elease'. Any parameters passed to this will be appended to the command line.
    --dotnet-version              Only applies to dotnet-isolated applications. Specifies the .NET version for the function app. For example, 
                                   set to '5.0' when publishing a .NET 5.0 app.
    --slot                        The deployment slot in the function app to use (if configured)
    --access-token                Access token to use for performing authenticated azure actions
    --access-token-stdin          Read access token from stdin e.g: az account get-access-token | func ... --access-token-stdin
    --management-url              Management URL for Azure Cloud e.g: --management-url https://management.azure.com.
    --subscription                Default subscription to use
 ```



 ##
 vs-2022
  No valid package source found for Microsoft.Cloud.InstrumentationFramework.NetStd.


## Logs
Monitoring -> Logs -> Query
```sh
traces
| where severityLevel >= 2
```


az functionapp config appsettings list --name WinGetRestSourceFunctions --resource-group winget