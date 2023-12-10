# Blazor2Angular
Rendering Blazor components within a SPA app (Angular)

## Steps to run the app

### 1. Go to the sou
    
```PowerShell
cd ./src
```

### 1. Publish the Blazor app

```PowerShell dd
dotnet publish ./Blazor2Angular.BlazorClient/
```

### 2. Copy the published files to the Angular app

```PowerShell
Remove-Item -Recurse -Force ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client/src/_content
cp -r ./Blazor2Angular.BlazorClient/bin/Release/net8.0/publish/wwwroot/_content ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client/src/

Remove-Item -Recurse -Force ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client/src/_framework
cp -r ./Blazor2Angular.BlazorClient/bin/Release/net8.0/publish/wwwroot/_framework ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client/src/

Remove-Item -Recurse -Force ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client/src/css
cp -r ./Blazor2Angular.BlazorClient/bin/Release/net8.0/publish/wwwroot/css ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client/src/

```

### 3. Run the Angular app

```PowerShellcd 
cd ./Blazor2Angular.AngularApp/blazor2angular.angularapp.client
```

```npm 
npm install

npm start
```