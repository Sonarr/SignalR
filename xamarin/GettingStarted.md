ASP.NET SignalR is a new library for ASP.NET developers that simplifies the process of adding real-time web functionality to your applications. Real-time web functionality is the ability to have server-side code push content to connected clients instantly as it becomes available.

```csharp

using Microsoft.AspNet.SignalR.Client;

...
  public void Run()

  {

    var hubConnection = new HubConnection("url");
    var hubProxy = hubConnection.CreateHubProxy("HubName");
    hubProxy.On<string>("receivingData", (data) => hubConnection.TraceWriter.WriteLine(data));
    
    await hubConnection.Start();
    await hubProxy.Invoke("sendingData", "Hello World!");
  }

```



## Documentation
* 
[Tutorials and Documentation](http://www.asp.net/signalr)
* 
[Wiki](https://github.com/SignalR/SignalR/wiki)
* 
[Support Forums](http://forums.asp.net/1254.aspx)
* 
[Stackoverflow Forum](http://stackoverflow.com/questions/tagged/signalr)
* 
[Source Code Repository](https://github.com/SignalR/SignalR)
*

## Contact* 
[JabbR SignalR Room](https://jabbr.net/#/rooms/signalr)*

Twitter: @SignalR @DamianEdwards @davidfowl