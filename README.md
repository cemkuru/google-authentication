

#### Authentication Using Google In ASP.NET Core
# Introduction
Sometimes, we want our users to log in using their existing credentials from third-party applications, such as Facebook, Twitter, Google, and so on. In this article, we are going to look into authentication of an ASP.NET Core app using a Google account.

# Prerequisites
- Install .NET Core 2.2.0 or above SDK from [here](https://dotnet.microsoft.com/download "here").
- Install the latest version of Visual Studio 2017 from [here](https://visualstudio.microsoft.com/tr/downloads/ "here").

# Create a New ASP.NET Core Project
- Create a new project.
- Select ASP.NET Core Web Application and Next.
- Provide a Project name and confirm or change the Location. Select Create.
- Select ASP.NET Core 2.2 in the drop down. Select Web Application in the template list.
- Under Authentication, select Change and set the authentication to Individual User Accounts. Select OK.
- In the Create a new ASP.NET Core Web Application window, select Create.

# Create a New Database 
- Create a new database in sql server 
- ConnectionStrings in Appsettings.json changes your connections


			 "ConnectionStrings": {
   					 "DefaultConnection": "Server=	(localdb)\\mssqllocaldb;Database=TestDb;Trusted_Connection=True;MultipleActiveResultSets=true"
  	}

            ...
# Apply migrations
- Run the app and select the Register link.
- Enter the email and password for the new account, and then select Register.
- Follow the instructions to apply migrations.
