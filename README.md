# Azure Developer Program - Final Capstone

You will create a Lab management system in Java Spring which allows the user
to maintain details about a simple object hierarchy. This will be an API that supports
REST endpoints for CRUD (Create, Retrieve, Update, and Delete) functionality.

Your goals are:
* Finish out the build for the Java Spring API
* Build an Azure SQL database and link the API to the Azure SQL database for backend
* Deploy the API to an Azure App Service
* EXTRA: Integrate the API with Azure Key Vault for storage of the sensitive database connection string

Fork this repository into your GitHub account so you can work on the project independently

## Data Model:

### Category

* ID (INT, primary key)
* Name (NVARCHAR(35))

### Author

* ID (INT, primary key)
* First Name (NVARCHAR(30))
* Last Name (NVARCHAR(40))

### Lab

* ID (INT, primary key)
* Name (NVARCHAR(50))
* Description (NVARCHAR(100))
* Category ID (INT, foreign key linking to Category table)
* Author ID (INT, foreign key linking to Author table)

## Operations To Be Supported

You will implement CRUD (Create/Retrieve/Update/Delete) operations for all 3 entity
types listed in the data model above.

## Cloud Deployment

### Azure SQL Database

* Create a new database on the existing `socgensqlserver` which resides in the `socgen-sqlserver-rg` resource group in our Azure Sandbox Subscription
* Establish connectivity between your API and the Azure SQL database and confirm ability
to persist data from a locally-running instance of the app (a POSTMan collection is included
in this repository to provide sample requests)

### Azure App Service

* Deploy your API to Azure App Service for Cloud hosting
* Ensure that the linkage between your API and the backend Azure SQL database remains intact
* Confirm ability to persist data from the Azure-hosted instance of the app (again, you can use
the provided POSTMan collection for sample requests)

### Azure Key Vault Integration

* Create an Azure Key Vault and add a secret to the vault for connection string
* Enable linkage between your hosted Azure app instance and the Key Vault for pulling
the secret
* Remove any references to connection string in your app configuration
* Confirm that connectivity between your API and the Azure SQL database remains in place

## Reference Materials

### Websites

* https://learn.microsoft.com/en-us/azure/developer/java/spring-framework/configure-spring-data-jdbc-with-azure-sql-server
* https://learn.microsoft.com/en-us/azure/developer/java/spring-framework/deploy-spring-boot-java-app-on-linux
* https://azure.github.io/AppService/2019/07/30/Key-Vault-References-with-Spring-Apps.html

### Solution

One possible solution for the capstone project is available at https://github.com/KernelGamut32/labmanagement. You can use the solution to help you finish out the Java parts of the app (if needed). The solution also includes ARM templates for creating the various objects in Azure if you
want to reference as you create your own, and images for application settings used in the app.

## Where To Go For Help

You can email the instructor at asanders@gamuttechnologysvcs.com