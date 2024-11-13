# Blazor 8.0 New Features

Static server side rendering        
![alt text](image-7.png)
Streaming Rendering
![alt text](image-8.png)

![alt text](image-9.png)

![alt text](image-10.png)
.NET 7 How it was works

Static server rendering

![alt text](image-11.png)
![alt text](image-12.png)
![alt text](image-13.png)
![alt text](image-14.png)

![alt text](image-15.png)
![alt text](image-16.png)

![alt text](image-17.png)
![alt text](image-18.png)
![alt text](image-19.png)

![alt text](image-20.png)

Blazor server has following Benefits

![alt text](image-21.png)

first app loads faster because the download size is small
![alt text](image-23.png)
![alt text](image-24.png)
![alt text](image-25.png)


![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)
![alt text](image-29.png)
![alt text](image-30.png)
It is not possible to deliver the app through content delivery network

Blazor web assembly hosting Model
![alt text](image-31.png)

![alt text](image-32.png)

![alt text](image-33.png)
![alt text](image-34.png)
![alt text](image-35.png)
![alt text](image-36.png)

![alt text](image-37.png)

![alt text](image-38.png)

![alt text](image-39.png)
![alt text](image-40.png)
![alt text](image-41.png)

![alt text](image-42.png)

![alt text](image-43.png)

![alt text](image-44.png)
![alt text](image-45.png)
![alt text](image-46.png)
upfront decision
![alt text](image-47.png)

![alt text](image-48.png)

![alt text](image-49.png)

![alt text](image-50.png)
![alt text](image-51.png)
![alt text](image-52.png)
![alt text](image-53.png)
![alt text](image-54.png)

![alt text](image-55.png)

![alt text](image-57.png)
![alt text](image-58.png)

Blazor web app in .Net 8.0


![alt text](image-59.png)

![alt text](image-60.png)
![alt text](image-61.png)
![alt text](image-62.png)
![alt text](image-63.png)

![alt text](image-64.png)
![alt text](image-65.png)
![alt text](image-66.png)
![alt text](image-67.png)
![alt text](image-68.png)
![alt text](image-69.png)

![alt text](image-70.png)
![alt text](image-71.png)
![alt text](image-72.png)
![alt text](image-74.png)
![alt text](image-75.png)
![alt text](image-77.png)
![alt text](image-78.png)
![alt text](image-79.png)
![alt text](image-80.png)
![alt text](image-81.png)
![alt text](image-82.png)
![alt text](image-83.png)
![alt text](image-84.png)
![alt text](image-85.png)
![alt text](image-86.png)
![alt text](image-87.png)
![alt text](image-88.png)
![alt text](image-89.png)
imports.razor contains common using directives

![alt text](image-90.png) 

appsetting.json

wwwroot folder

![alt text](image-91.png)
![alt text](image-92.png)
![alt text](image-93.png)
![alt text](image-94.png)


server app

![alt text](image-95.png)
![alt text](image-96.png)


client project (webassembly)
Create a new project with Blazro web app  (BlazorAppNewFeaturesDotnet8)
interactive render mode Auto
interactive location ==>Global
![alt text](image-118.png)
![alt text](image-97.png)
![alt text](image-98.png)
![alt text](image-99.png)
![alt text](image-119.png)
![alt text](image-120.png)
![alt text](image-122.png)
![alt text](image-123.png)
![alt text](image-124.png)
![alt text](image-125.png)
Server program.cs
![alt text](image-121.png)

open the project we created already(BlazorAppNewFeatures)

Balzor 8.0 Static Server Rendering
![alt text](image-101.png)
steps

![alt text](image-106.png)
![alt text](image-107.png)
![alt text](image-108.png)
![alt text](image-100.png)
imports page has common razor directives such as using direcrives

app settings.json file will have all configuration settings.

Launchsettings.json
Mainlayout page is rendering navmenu component and it contains error ui as well
![alt text](image-116.png)

Stylesheet for the mainLyout namvmenu
![alt text](image-117.png)
![alt text](image-102.png)
Program.cs 

![alt text](image-109.png)
commecnt line 7 and 25 to make static server rendering
![alt text](image-126.png)
Goto App.razor
![alt text](image-110.png)

app.razor is the page act as root component
![alt text](image-111.png)
comment line no 17 
![alt text](image-127.png)
route component sets the routing
![alt text](image-112.png)
expand Pages folder ==> goto Counter.razor
 the below image shows that interactive server mode enables.
![alt text](image-114.png)
![alt text](image-113.png)

 => lets turn off interactivity component by removing the
 **  @rendermode InteractiveServer**
Goto weather.razor
StreamRendering enabled in weather page
![alt text](image-115.png)
let us turn off streamrendering as well by removing the
  **@attribute [StreamRendering]**
![alt text](image-128.png)
  Now lets run the app

![alt text](image-130.png)
![alt text](image-129.png)
![alt text](image-131.png)

click the counter button .There is no action happened which means
![alt text](image-132.png)

#  Enhanced Navigation and Form Handling
![alt text](image-133.png)
![alt text](image-134.png)
![alt text](image-135.png)
![alt text](image-136.png)

![alt text](image-137.png)
![alt text](image-138.png)
![alt text](image-139.png)
![alt text](image-140.png)
![alt text](image-141.png)

![alt text](image-142.png)
![alt text](image-143.png)
blazor.web.js calaculates the changes and it updates the changes .It do not change the total DOM
![alt text](image-144.png)
![alt text](image-145.png)
![alt text](image-146.png)
![alt text](image-147.png)

Now go back to the project 
aap.razor  
as we commented  <script src="_framework/blazor.web.js"></script>
![alt text](image-148.png)
run the application
inspect element 
navigate from home to counter  focus the refresh button of the page while navigation (small flip happens)

go back to the application ==> uncomment the below code in app.razor
<script src="_framework/blazor.web.js"></script>

this turns on enhanced navigation by default.
![alt text](image-149.png)
![alt text](image-150.png)

it means it is using balzor.web.js
goto home.razor
by default enhanced naviagation enabled by default.
![alt text](image-151.png)

What if we need to disable enhanced navigation on per link basis
![alt text](image-152.png)

```razor
@page "/"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<div data-enhance-nav="false">
    <a href="counter">Counter</a>
</div>
```
![alt text](image-153.png)

Scenario to disable the enhanced navigation
such as navigating from Razor component to Non-razor component like razor pages
![alt text](image-154.png)

First we need register the services in **program.cs**
```cs
builder.Services.AddRazorPages();
app.MapRazorPages();
```
# Program.cs
```cs
using BlazorAppNewFeatures.Components;

var builder = WebApplication.CreateBuilder(args);

// Add services to the container.
builder.Services.AddRazorComponents()
    .AddInteractiveServerComponents();
builder.Services.AddRazorPages();
var app = builder.Build();

// Configure the HTTP request pipeline.
if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Error", createScopeForErrors: true);
    // The default HSTS value is 30 days. You may want to change this for production scenarios, see https://aka.ms/aspnetcore-hsts.
    app.UseHsts();
}

app.UseHttpsRedirection();

app.UseStaticFiles();
app.UseAntiforgery();

app.MapRazorComponents<App>()
    .AddInteractiveServerRenderMode();
app.MapRazorPages();
app.Run();

```

Right click the Project ==> Add New folder==> Name it as Pages==>Righ click the Pages Folder ==> add Razor Page ==> Razor Page empty template ==> name it as Test (Test.cshtml)
# test.cshtml
```cshtml
@page
@model BlazorAppNewFeatures.Pages.TestsModel
@{
}

<h1> This is a Test Page</h1>
```

Goto Home.razor
change the code as below

```razor
@page "/"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<div>
    <a href="test">Test</a>
</div>
```

Run the application
inspect ==> network ==> check the preserve log 
![alt text](image-156.png)

now first test requst made for the page .then fullpage request made for the  test page and we got the response here .This  is  because
![alt text](image-157.png)
![alt text](image-158.png)
![alt text](image-159.png)

# home.razor 
```razor
@page "/"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<div data-enhance-nav="false">
    <a href="test">Test</a>
</div>
```

build you solution and  run ==> inspect ==> network ==> check the preserve log 
![alt text](image-161.png)


# Data permanent Attribute
![alt text](image-162.png)

goto MainLayout.razor
 <div id="myDiv">
     </div>

     <script>
    var element=document.querySelector("#myDiv");
    element.innerHTML="<h1> Div content</h1>";
    </script>
# MainLayout.razor

```razor
@inherits LayoutComponentBase

<div class="page">
    <div class="sidebar">
        <NavMenu />
    </div>

    <main>
        <div class="top-row px-4">
            <div id="myDiv">
                </div>

            <a href="https://learn.microsoft.com/aspnet/core/" target="_blank">About</a>
        </div>

        <article class="content px-4">
            @Body
        </article>
    </main>
</div>

<div id="blazor-error-ui">
    An unhandled error has occurred.
    <a href="" class="reload">Reload</a>
    <a class="dismiss">🗙</a>
</div>
<script>
    var element=document.querySelector("#myDiv");
    element.innerHTML="<h1> Div content</h1>";
    </script>
```

Run the Application 

![alt text](image-163.png)
navigate to counter 
![alt text](image-164.png)

navigate to Home
![alt text](image-165.png)

Now Div content is not there in bith component header

low lets understand why this happens

![alt text](image-166.png)
![alt text](image-167.png)
when we navigate to any component usong enhanced navigation the components executes on server to produce the response html and that html is added to the response and send back to the  browser
![alt text](image-168.png)
now blazor web js 
![alt text](image-169.png)
![alt text](image-170.png)

to make this permanent we need to use data-permanent attribute
# MainLayout.razor
    <div id="myDiv" data-permanent>

    Re Run the app.

    ![alt text](image-171.png)

    ![alt text](image-172.png)

# Enhanced page load event for listen the enhanced page updates and streaming updates
  ![alt text](image-173.png)  

  # app.razor

   <script>
     Blazor.addEventListener("enhancedload",
     () => console.log("there was an enhanced update!.."));
     </script>
# app.razor
```razor
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <base href="/" />
    <link rel="stylesheet" href="bootstrap/bootstrap.min.css" />
    <link rel="stylesheet" href="app.css" />
    <link rel="stylesheet" href="BlazorAppNewFeatures.styles.css" />
    <link rel="icon" type="image/png" href="favicon.png" />
    <HeadOutlet />
</head>

<body>
    <Routes />
    <script src="_framework/blazor.web.js"></script>
    <script>
        Blazor.addEventListener("enhancedload",
        () => console.log("there was an enhanced update!.."));
        </script>
</body>

</html>
```
run the application
inspect ==> navigate to any component
![alt text](image-174.png)
whenever we move the count gets incremented
![alt text](image-175.png)

when we want to navigate programatically 
we should use 
![alt text](image-176.png)

![alt text](image-177.png)
forceload false by default. when forceload is false
![alt text](image-178.png)

![alt text](image-179.png)

![alt text](image-180.png)

![alt text](image-181.png)
![alt text](image-182.png)

# Form handling

## Home.razor
```razor
@using System.ComponentModel.DataAnnotations;
@page "/"

<PageTitle>Home</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.
<div style="height:100vh"></div>

<EditForm  FormName="CreateForm" method="post" Model="@Item" @onValidSubmit ="AddEmployee()">
   <DataAnnotationsValidator/>
    <ValidationSummary/>
    <div>
    <label>Name:</label>
    <InputText @bind-Value="@Item.Name" />
    </div>
    <button>Submit </button>
    </EditForm>

@code{
    [SupplyParameterFromForm]
    public Employee Item {get;set;}=new ();
    private void AddEmployee(){
        //write the logic
    }
    public class Employee{
        [Required]
        public string? Name {get;set;}
    }
}
```
Run the app  .Bydefault  enhance scroll is disabled.
![alt text](image-183.png)
user scroll position is  lost
enter the Name and submit ==> again user scroll position is  lost (goes to the top of the page)

![alt text](image-184.png)

then we need to scroll down 

to avoid the lose of scrol position we use enhance attribute
Now add 
<EditForm Enhance
  FormName="CreateForm" method="post" Model="@Item" @onValidSubmit ="AddEmployee()">


and rerun the app
![alt text](image-185.png)

![alt text](image-186.png)

This is how user scroll position is not lost anymore

# Stream Rendering
![alt text](image-187.png)
![alt text](image-188.png)
![alt text](image-189.png)
![alt text](image-190.png)
![alt text](image-191.png)
![alt text](image-192.png)
![alt text](image-193.png)

![alt text](image-194.png)
![alt text](image-195.png)
![alt text](image-196.png)
![alt text](image-197.png)

Goto BlazorAppNewFeatures

app.razor
comment velow line of code 
    @*<script src="_framework/blazor.web.js"></script>*@

weather.razor

comment
@* @attribute [StreamRendering] *@
   await Task.Delay(1000);

   and run the app ==> Navigate to weather ==> which is not showing loading..
    instead it is loading the content after 1s. 


    Now enable app.razor uncomment the below line
    <script src="_framework/blazor.web.js"></script>
    weather.razor 
    add the below line
     @attribute [StreamRendering]

     And run the App
     ![alt text](image-198.png)
     then it wilrender the data after 1s


     # Render Modes
     ![alt text](image-199.png)

     ![alt text](image-200.png)
     ![alt text](image-201.png)
     ![alt text](image-202.png)
     ![alt text](image-203.png)
     ![alt text](image-204.png)
     ![alt text](image-205.png)



     goto BlazorAppNewFeaturesDotnet8 project


![alt text](image-206.png)
![alt text](image-207.png)
![alt text](image-208.png)
![alt text](image-209.png)
![alt text](image-210.png)
![alt text](image-211.png)
![alt text](image-212.png)
![alt text](image-213.png)
![alt text](image-214.png)
![alt text](image-215.png)
![alt text](image-216.png)
![alt text](image-217.png)
![alt text](image-218.png)
![alt text](image-219.png)

![alt text](image-220.png)
**`.AddInteractiveServerComponents() `**
adds the necessary services to supprots rendering interacrive server components
![alt text](image-221.png)
**`.AddInteractiveWebAssemblyComponents()`** in Blazor WebAssembly 8.0 is used to add services that support rendering interactive WebAssembly components. This is particularly useful when you want to create interactive components that can run in the browser using WebAssembly, even if the rest of your application is using server-side rendering.

By calling this method, you're essentially configuring your Blazor WebAssembly app to handle interactive components, which can improve the user experience by making parts of your app more dynamic and responsive
![alt text](image-222.png)

**`.AddInteractiveServerRenderMode() `**in Blazor WebAssembly 8.0 is used to enable interactive server-side rendering (SSR) for your Blazor Web App. This means that your components can be rendered on the server initially, and then become interactive on the client side once the Blazor WebAssembly bundle is downloaded.

Here's a brief overview of how it works:

**Initial Server Rendering:** When a user first visits your Blazor Web App, the components are rendered on the server.

**Client Interactivity:** After the initial render, the Blazor WebAssembly bundle is downloaded to the client's browser, and the components become interactive.

**Improved Performance**: This approach can improve the initial load time and user experience, as the user sees content faster while still benefiting from the interactivity of Blazor WebAssembly.

`**.AddInteractiveWebAssemblyRenderMode()**` in Blazor 8.0 is used to enable interactive client-side rendering using Blazor WebAssembly. This means that your components will be rendered on the client side using WebAssembly, allowing for a more interactive and responsive user experience1.

Here's a brief overview of how it works:

**Client-Side Rendering:** The components are rendered on the client's browser using Blazor WebAssembly.

**Interactivity:** The components are fully interactive, meaning they can handle user input and update the UI dynamically without needing to reload the page.

**Improved Performance:** This approach can improve the user experience by reducing the initial load time and making the app more responsive.

`**.AddAdditionalAssemblies(typeof(Counter).Assembly)**` in Blazor 8.0 is used to include additional assemblies in your Blazor Web App. This is particularly useful when you have components or dependencies in separate projects that you want to use in your main Blazor project.

By specifying typeof(Counter).Assembly, you're telling Blazor to include the assembly that contains the Counter component. This ensures that Blazor can find and use the components and dependencies within that assembly.

lets demo it

in server project ==> expand the component folder ==> right click the Pages folder ==>Add Razor component 
![alt text](image-223.png)

Name it as RenderModes

nagivate to navmenu component in client project
add the below link at last 
<div class="nav-item px-3">
    <NavLink class="nav-link" href="render-modes">
        <span  aria-hidden="true"></span> Blazor Render Modes
    </NavLink>
</div>

i have removed the class for span tag
![alt text](image-224.png)

goto server project ==> Pages ==> Add new Razorcomponent==>
Name it as ShowMessage.razor
```cs
<h3>@message</h3>

<button @onclick="HandleShowMessageClick" class="btn btn-primary">ShowMessage</button>

@code {

    private string? message;
    private void HandleShowMessageClick()
    {
        message = "Message 1";
    }
}
```

![alt text](image-225.png)
![alt text](image-226.png)
routes.razor
![alt text](image-227.png)
![alt text](image-228.png)
![alt text](image-229.png)
![alt text](image-230.png)
![alt text](image-231.png)
![alt text](image-232.png)
![alt text](image-233.png)
![alt text](image-234.png)
Run the app
![alt text](image-235.png)
![alt text](image-236.png)
![alt text](image-237.png)
click button 
there is no interaction as it is rendering static server rendering

![alt text](image-238.png)
![alt text](image-239.png)
RenderModes.razor

@page "/render-modes"

<h3>RenderModes</h3>
<ShowMessage @rendermode="InteractiveServer"/>
@code {

}

![alt text](image-240.png)
![alt text](image-241.png)
the component is using InteractingServer rendering hosting model
![alt text](image-242.png)
in wasm tab there is no assemblies download it means interactive 
client rendering using webassembly is not used.

Click the button . It is showing the message (interactive)
![alt text](image-243.png)
![alt text](image-244.png)

# Iteractivewebassembly

rightclick on showMessage.razor ==> cut and paste in client project
![alt text](image-245.png)
![alt text](image-246.png)
![alt text](image-247.png)

Goto RenderModes.razor component
change the render mode to interactivewebassembly

![alt text](image-248.png)
![alt text](image-250.png)
![alt text](image-251.png)

Run the app
![alt text](image-252.png)

It download all necessary things and render the component
![alt text](image-253.png)
in ws tab there is no web socket connection made.This is because interactiveserver not using for rendering
![alt text](image-254.png)

# InteractiveAuto
![alt text](image-255.png)
![alt text](image-256.png)
![alt text](image-257.png)
![alt text](image-258.png)

Run the app

inspect ==> stores ==>clear the site data
![alt text](image-259.png)
then move to network in inspect ==> ws ==> click on Blazor render modes
![alt text](image-260.png)
and look into wasm as well
![alt text](image-261.png)

click the button  button also interactive


![alt text](image-262.png)
goto client project => showMessage.razor
![alt text](image-263.png)
```cs
<h3>@message</h3>
<h4>@Message</h4>

<button @onclick="HandleShowMessageClick" class="btn btn-primary">ShowMessage</button>

@code {

    private string? message;

    [Parameter]
    public string? Message { get; set; }
    private void HandleShowMessageClick()
    {
        message = "Message 1";
    }
}

```
goto Rendermodes.razor component in server

```cs

@page "/render-modes"

<h3>RenderModes</h3>
<ShowMessage @rendermode="InteractiveAuto" Message="Message from Parent"/>
@code {

}

```

# goto showmessage add one more property

   @ChildContent 
[Parameter]
    public RenderFragment? ChildContent { get; set; }



```cs
<h3>@message</h3>
<h4>@Message</h4>

@ChildContent
<button @onclick="HandleShowMessageClick" class="btn btn-primary">ShowMessage</button>

@code {

    private string? message;

    [Parameter]
    public string? Message { get; set; }
    [Parameter]
    public RenderFragment? ChildContent { get; set; }
    private void HandleShowMessageClick()
    {
        message = "Message 1";
    }
}
```


# goto RenderModes.razor

@page "/render-modes"

<h3>RenderModes</h3>
<ShowMessage @rendermode="InteractiveAuto" Message="Message from Parent">
    Child Content
    </ShowMessage>
@code {

}


run the app
will get an below error
![alt text](image-264.png)
undo the changes we made

ShowMessage.razor
<h3>@message</h3>



<button @onclick="HandleShowMessageClick" class="btn btn-primary">ShowMessage</button>

@code {

    private string? message;

    [Parameter]
    public string? Message { get; set; }
   
    private void HandleShowMessageClick()
    {
        message = "Message 1";
    }
}


![alt text](image-265.png)
![alt text](image-266.png)
![alt text](image-267.png)
![alt text](image-268.png)
![alt text](image-269.png)
![alt text](image-270.png)
![alt text](image-271.png)
![alt text](image-272.png)
in the pagelevel we have Interativeserver. but in c
hild component we cannot have Interactivewebassembly
![alt text](image-273.png)

Let set the Global interactive in app.razor
![alt text](image-274.png)

![alt text](image-276.png)
![alt text](image-275.png)
![alt text](image-277.png)
![alt text](image-278.png)

![alt text](image-279.png)
How to disable prerendering globally
![alt text](image-281.png)

# Blazor Sections
![alt text](image-282.png)
![alt text](image-284.png)
![alt text](image-283.png)


![alt text](image-285.png)
![alt text](image-286.png)
![alt text](image-287.png)