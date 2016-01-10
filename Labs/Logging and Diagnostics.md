## Logging

## Setting up your application 
1. Use the application from the first lab (or setup steps from the fisrt lab).
2. Add the console logging provider to `project.json`:

    ```JSON
      "dependencies": {
        "Microsoft.AspNet.IISPlatformHandler": "1.0.0-*",
        "Microsoft.AspNet.Server.Kestrel": "1.0.0-*",
        "Microsoft.Extensions.Logging.Console": "1.0.0-*"
      },
    ```
3. Navigate to `Startup.cs` Change the `Configure` method to:
    
    ```C#
        public void Configure(IApplicationBuilder app, ILoggerFactory loggerFactory)
        {
            loggerFactory.AddConsole();
            ...
        }
    ```
4. In Visual Studio, change the active command to web by navigating to the play/run button and changing the drop down to the web command. 

    ![image](https://cloud.githubusercontent.com/assets/95136/12222924/633ef134-b7c1-11e5-9146-da36013da8d8.png)

5. Run the application and open a browser window with `http://localhost:5000/` as the address.