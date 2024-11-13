

Blazor is component based application

Routable (or) Page Component
non-routable component &rarr; which sometimes called reusable components

![alt text](image-288.png)
![alt text](image-289.png)


let us create Routable Component
![alt text](image-290.png)

![alt text](image-291.png)
![alt text](image-292.png)

Right click on Pages &rarr; Add Razor Component &rarr; Servers.razor

@page "/servers"  <mark> `Routable Component` </mark>
 <h3>Servers</h3>

@code {

}

Run the App
![alt text](image-293.png)

# Lets create non routable component

Right click on Components &rarr; Add New Folder  &rarr; Controls  &rarr;Right click on Controls folder &rarr; add Razor component &rarr;ServerComponent.razor
<p> Server is online</p>

@code {

}

![alt text](image-294.png)

Next we need add this inside routable component

goto Servers.razor


<ServerManagement_components_Demo.Components.Controls.ServerComponent>
</ServerManagement_components_Demo.Components.Controls.ServerComponent>

instead of writing the above code we can simply write in below format using 
@using directive in page level. 
the same can be used in application level also for that we need use the same in imports.razor page

@page "/servers"  
@using ServerManagement_components_Demo.Components.Controls
 <h3>Servers</h3>


<br/>
<br/>

<ServerManagement_components_Demo.Components.Controls.ServerComponent>
</ServerManagement_components_Demo.Components.Controls.ServerComponent>

@code {

}


# imports.razor
@using ServerManagement_components_Demo.Components.Controls

# servers.razor
@page "/servers" 

 <h3>Servers</h3>
<br/>
<br/>
<ServerComponent> </ServerComponent>
@code {

}

# Razor Syntax Implicit Razor Expression