# mulesoft-customer-db-api

**A MuleSoft API that connects to a postgres database (Supabase)**

<br>
This project is a MuleSoft-based REST API that integrates with PostgreSQL database hosted on supabase. The API lets users send requests (like “create a customer”) and the app stores/retrieves that data from a database (supabase). This is a test project which I'm using to experiment with mules integration tools and practice connecting different APIs together. 
<br> 
<br> 

# Workflow
```
User (Postman / App) - User sends a request (Add,Delete,Update a User) 
        ↓
   MuleSoft API (send/retrieve data) 
        ↓
   PostgreSQL Database (update database)
        ↓
   MuleSoft API 
        ↓
User gets response
```

<br>
<br>

**Example**

```
POST /customers
{
  "firstName": "Riaan",
  "lastName": "Harwood",
  "email": "riaan@email.com"
}
```

<br>
<br> 

# ⚙️ Tech Stack

* MuleSoft (Anypoint Studio)
* PostgreSQL
* Supabase
* DataWeave

<br>

# 🚀 Features

* Create a customer
* Retrieve customers
* Update customer details
* Delete a customer

<br>

# 🏗️ Architecture

This project follows a simplified API-led connectivity approach, where:

MuleSoft acts as the integration layer
PostgreSQL (Supabase) serves as the data source
DataWeave handles data transformation between layers

# 📊 Architecture Diagram:

(to be updatted) 

<br>

# 🔌 API Endpoints
➕ Create Customer

POST /customers

Creates a new customer in the database.
Example

```
Request Body

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@email.com"
}
```

<br>

# Get Customers

**GET** /customers

Retrieves all customers from the database.

<br>

# Update Customer

**PUT** /customers/{id}

Updates an existing customer's details.

<br>

# Delete Customer

**DELETE** /customers/{id}

Deletes a customer from the database.


# Issue Encountered

* Connecting to SupabaseDB. Currently geeting the following error:
<img width="1410" height="891" alt="image" src="https://github.com/user-attachments/assets/d64e272c-9c3a-4f5e-b2b6-d88d07f36c5a" />



<br>
<br>

# Diagrams & Screenshots
New Database Project set up in Supabase
<img width="1693" height="702" alt="image" src="https://github.com/user-attachments/assets/181b3fc5-c72e-46b5-aac7-83cecc916f14" />
<img width="1477" height="707" alt="image" src="https://github.com/user-attachments/assets/03ee5c5c-4bc8-4c95-9b27-8acc19a9f2b0" />

