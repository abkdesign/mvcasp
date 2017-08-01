# mvcasp - ASP.NET Core 2.0

### Short-term extra dependency on Webpack

Because of an outstanding implementation quirk, you’ll also need Webpack installed globally:

npm install -g webpack

### Run it

```dotnet run```

Now open http://localhost:5000/ and marvel at the glory of it all. If you’re on one of the templates that supports server-side prerendering (see above), then try disabling JS in your browser and see it still works :)

### Try it in development mode. 
Set the environment variable and then restart dotnet run. On Windows, that’s:

```set ASPNETCORE_ENVIRONMENT=Development```
```dotnet run```
… or on Mac/Linux:

```export ASPNETCORE_ENVIRONMENT=Development```
```dotnet run```

### Make a production build. 
Set the ASPNETCORE_ENVIRONMENT variable to Production and then run:

webpack --config webpack.config.vendor.js
webpack
…to regenerate both the vendor and app bundles. Now when you run the app (dotnet run again), the browser will receive fully minified resources.
