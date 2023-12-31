# Minimal API and .NET

Minimal API was introduced in .NET 6

This is to track my progress through the following tutorials to stay up to date with the latest practices.
- [Create web apps and services with ASP.NET Core, minimal API, and .NET](https://learn.microsoft.com/en-us/training/paths/aspnet-core-minimal-api/)
- [Tutorial: Create a minimal API with ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-7.0&tabs=visual-studio)

## Create web apps and services with ASP.NET Core, minimal API, and .NET
### Build a web API with minimal API, ASP.NET Core, and .NET
- [x] Exercise - Create a minimal API
- [x] Exercise - Add routes
### Use a database with minimal API, Entity Framework Core, and ASP.NET Core
- [x] Exercise - Add EF Core to minimal API
- [x] Exercise - Use the SQLite database provider with EF Core
### Create a full stack application by using React and minimal API for ASP.NEt Core
- [x] Exercise - Create a front end for your app (React)
- [x] Exercise - Create an API (Connect to the API created above)

## Tutorial: Create a minimal API with ASP.NET Core
- [x] Overview
- [x] Prerequisites
- [x] Create an API project
- [x] Add NuGet packages
- [x] The model and database context classes
- [x] Add the API code
- [x] Install Postman to test the app
- [x] Examine the GET endpoints
- [x] Test the GET endpoints
- [x] Return values
- [x] Examine the PUT endpoint
- [x] Test the PUT endpoint
- [x] Examine and test the DELETE endpoint
- [x] Use the MapGroup API
- [x] Use the TypedResults API
- [x] Prevent over-posting
- [x] Next steps

## Data Strategy Comparison
My commentary on the three different ways to store and manage data in an API from the first tutorial set.
- in-memory store: Hard coded mock during POC (Proof of Concept) on how data would look or be structured.
- Entity Framework In Memory Database: Adds Entity Framework, but is still only in-memory. Data goes away if the service is restarted.
- Entity Framework SQLite: The data structure is now saved. The data is persistent if the service is stopped and restarted. However, when the application is redeployed, the data is still at the developer starting point.

These are all useful strategies along the development path, and can make sense before moving to the more permanent solution. They can all be used as stepping stones or for different use cases.

For a more robust solution the database will need changed, but most of the logic will still remain.

## My take on minimal API after adding SQLite
We are specifically comparing minimal API to Controllers.
I have always felt that Minimal API (before it now became a term, was a better approach, when first starting).

However, depending on the complexity, you may be able to keep the minimal API, or if the solution is more complex, it might make more sense to separate it out into controllers.

I have used both types of approaches in the past. Often staring with a more minimalistic approach and then separating it out to use controllers, etc. if and when it makes sense.

## My commentary on the first tutorial
- [Create web apps and services with ASP.NET Core, minimal API, and .NET](https://learn.microsoft.com/en-us/training/paths/aspnet-core-minimal-api/)

There is still so much more to be done.
- Add a new item
- Remove an item
- Update the Pizza Collection when an item changes
- This is the point where separating into services and events start to make sense.
- Without the separation, the code starts to get messy.
- Also this does not use TDD, and there are no automated tests.

## Reference
- [Minimal APIs quick reference](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis?view=aspnetcore-7.0)
- [Test Samples for Minimal APIs](https://github.com/dotnet/AspNetCore.Docs.Samples/tree/main/fundamentals/minimal-apis/samples/MinApiTestsSample)
- [Publish to Azure](https://learn.microsoft.com/en-us/azure/app-service/quickstart-dotnetcore?tabs=net70&pivots=development-environment-vs)