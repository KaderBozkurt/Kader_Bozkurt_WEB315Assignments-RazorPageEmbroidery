# RazorPageEmbroidery
dotnet new webapp -o RazorPageEmbroidery code -r RazorPagesEmbroidery

dotnet dev-certs https --trust

Add a folder named Models.
Add a class to the Models folder named Embroidery.cs.
Add  the Embroidery class for follow up tutorial 


Add NuGet packages and EF tools:
dotnet tool install --global dotnet-ef --version 5.*
dotnet tool install --global dotnet-aspnet-codegenerator --version 5.*
dotnet add package Microsoft.EntityFrameworkCore.Design --version 5.*
dotnet add package Microsoft.EntityFrameworkCore.SQLite --version 5.*
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design --version 5.*
dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 5.*


dotnet-aspnet-codegenerator razorpage -m Embroidery -dc RazorPagesEmbroideyContext -udl -outDir Pages/Embroiderys --referenceScriptLibraries -sqlite

Add migration:
dotnet tool install --global dotnet-ef
dotnet ef migrations add InitialCreate
dotnet ef database update

dotnet watch run
