# assignment2-Yarapathineni
# Sai Tejaswini
###### favorite museum to visit:National Museum Delhi
The National Museum, New Delhi, as we see it today, has an interesting beginning. The blueprint for **establishing** the National Museum in **Delhi** was prepared by the Maurice Gwyer Committee in May 1946.

---
# Museums near to the airport
# airport that is closest to the museum
1. The Airport Museum is located inside the Melbourne International Airport, One Air Terminal Parkway, Melbourne, Florida. 
2. It houses displays of the history of the Naval Air Station Melbourne and the Melbourne International Airport. 
3. It also contains a Link Trainer and aviation artwork
---
# locations around the museum 
* This airport has domestic flights and is 3 miles from the center of Melbourne, FL.
* Another major airport is Orlando International Airport (MCO / KMCO), which has international and domestic flights from Orlando, Florida and is 63 miles from Melbourne, FL.
link to the Aboutme: https://github.com/saitejaswini2525/assignment2-Yarapathineni/blob/main/AboutMe.md

--- 
## Cities Table and locations to be visited


 here the table descibe about 4 cities and famous locations to visit in the city

|name of a city|location to visit in the city|amount of time to spend visiting the important location|
|--------------|-----------------------------|-------------------------------------------------------|
|Guntur|Chillies trade center|3hrs|
|Vijayawada|Kanaka durga temple|5hrs|
|Vizag|Rk beach|3days|
|Hyderabad|Charminar|4hrs|

----
## Quotes

>1.All of us do not have equal talent. But , all of us have an equal opportunity to develop our talents.
*Author:Dr.APJ Abdul kalam*

>2.Creativity is seeing the same thing but thinking differently.
*Author:Dr.APJ Abdul kalam*

----

## Code Fencing

> htaccess redirect to https://www

find the answer: <https://stackoverflow.com/questions/5226791/custom-error-pages-on-asp-net-mvc3>

```
protected void Application_Error() {
//while my project is running in debug mode
if (HttpContext.Current.IsDebuggingEnabled && WebConfigurationManager.AppSettings["EnableCustomErrorPage"].Equals("false"))
{
    Log.Logger.Error("unhandled exception: ", Server.GetLastError());
}
else
{
    try
    {
        var exception = Server.GetLastError();

        Log.Logger.Error("unhandled exception: ", exception);

        Response.Clear();
        Server.ClearError();
        var routeData = new RouteData();
        routeData.Values["controller"] = "Errors";
        routeData.Values["action"] = "General";
        routeData.Values["exception"] = exception;

        IController errorsController = new ErrorsController();
        var rc = new RequestContext(new HttpContextWrapper(Context), routeData);
        errorsController.Execute(rc);
    }
    catch (Exception e)
    {
        //if Error controller failed for same reason, we will display static HTML error page
        Log.Logger.Fatal("failed to display error page, fallback to HTML error: ", e);
        Response.TransmitFile("~/error.html");
    }
}
}
```

link to the snippet:<https://css-tricks.com/snippets/htaccess/custom-error-pages/>

