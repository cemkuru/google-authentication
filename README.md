
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

![New Project](https://raw.githubusercontent.com/cemkuru/google-authentication/master/image/newproject.PNG "New Project")

![Create Authentication](https://raw.githubusercontent.com/cemkuru/google-authentication/master/image/newproject_2.PNG "Create Authentication")
# Create a New Database 
- Create a new database in sql server 
- ConnectionStrings in Appsettings.json changes your connections


    "ConnectionStrings": {
    "DefaultConnection": "Server= (localdb)\\mssqllocaldb;Database=TestDb;Trusted_Connection=True;MultipleActiveResultSets=true"
  }

# Apply migrations
- Run the app and select the Register link.
- Enter the email and password for the new account, and then select Register.
- Follow the instructions to apply migrations.
- Navigate to Tools > Nuget Package Manager > Package Manager Console.
- It will open the Package Manager Console. Put in the Update-Database command and    hit enter. This will update the database using Entity Framework Code First Migrations.

![Table list ](https://raw.githubusercontent.com/cemkuru/google-authentication/master/image/table.PNG "Table list ")

# Create the Google app
We need to create a new Google app on the Google API console. Navigate to https://console.developers.google.com/projectselector/apis/library and log in using your Google account. If you do not have a Google account, you need to create one. You cannot proceed without a Google account. Once you have logged in, you will be redirected to the API Manager Library page, similar to the one shown below.
