[Interact with data in Blazor web apps](https://learn.microsoft.com/en-us/training/modules/interact-with-data-blazor-web-apps/)


```
# Create blazorserver app
dotnet new blazorserver -o BlazingPizzaSite -f net6.0

# Add a new component
dotnet new razorcomponent -n PizzaBrowser -o Pages


# Add model PizzaSpecial
ni -Type File .\Model\PizzaSpecial.cs -Force


# Add packages to support database access
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.Sqlite
dotnet add package System.Net.Http.Json

# Add database context
ni -Type File .\Data\PizzaStoreContext.cs -Force

# Add Controller
ni -Type File .\Controllers\SpecialsController.cs -Force

```
