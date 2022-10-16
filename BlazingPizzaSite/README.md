[Interact with data in Blazor web apps](https://learn.microsoft.com/en-us/training/modules/interact-with-data-blazor-web-apps/)


```
# Create blazorserver app
dotnet new blazorserver -o BlazingPizzaSite -f net6.0

# Add a new component
dotnet new razorcomponent -n PizzaBrowser -o Pages


# Add model PizzaSpecial.cs
ni -Type File .\Model\PizzaSpecial.cs -Force

# Add model Pizza.cs
ni -Type File .\Model\Pizza.cs -Force
ni -Type File .\Model\Topping.cs -Force
ni -Type File .\Model\PizzaTopping.cs -Force
ni -Type File .\Model\Address.cs -Force
ni -Type File .\Model\Order.cs -Force


# Add packages to support database access
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.Sqlite
dotnet add package System.Net.Http.Json

# Add database context
ni -Type File .\Data\PizzaStoreContext.cs -Force

# Add Controller
ni -Type File .\Controllers\SpecialsController.cs -Force

# Load data into database
ni -Type File .\Data\SeedData.cs -Force

# Add a new order configuration dialog
ni -Type File .\Shared\ConfigurePizzaDialog.razor

# Handle the state of an order
ni -Type File .\Services\OrderState.cs -Force

```
