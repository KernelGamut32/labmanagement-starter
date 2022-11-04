# Azure Developer Program - Final Capstone

You will create a Lab management system in Java Spring which allows the user
to maintain details about a simple object hierarchy. This will be an API that supports
REST endpoints for CRUD (Create, Retrieve, Update, and Delete) functionality.

Your goals are:
* Finish out the build for the Java Spring API
* Deploy the API to an Azure App Service
* Build an Azure SQL database and link the API to the Azure SQL database for backend
* EXTRA: Integrate the API with Azure Key Vault for storage of the sensitive database connection string

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

## Operations

You will implement CRUD (Create/Retrieve/Update/Delete) operations for all 3 entity
types listed in the data model above.