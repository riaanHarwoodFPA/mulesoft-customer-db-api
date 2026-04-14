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

**Basic Mule Flow**
```
HTTP Listener → Transform Message → DB Insert
```

**Post API** 

<img width="386" height="306" alt="image" src="https://github.com/user-attachments/assets/48ddeac7-999b-45e6-80ec-9e04826e45fd" />

<img width="1381" height="815" alt="image" src="https://github.com/user-attachments/assets/e3bc1e3c-ba23-4e19-9845-15cfbaf12d20" />


**GET API** 

<img width="397" height="287" alt="image" src="https://github.com/user-attachments/assets/4584cc5a-1a04-4028-a8ae-f822eaef3dc6" />

<img width="1376" height="877" alt="image" src="https://github.com/user-attachments/assets/3886395b-838d-4d6e-9af8-7c6c8ba632b9" />



**DELETE API** 

**PATCH API** 


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

# Instructions
Open **customer-db-api** directly in VS code to see workflow. 

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

<br>
<br>

# API Specification (API Designer) 
<img width="1917" height="826" alt="image" src="https://github.com/user-attachments/assets/aa02ead8-53dc-46fd-9acc-6a07e5b6b998" />
<img width="1917" height="825" alt="image" src="https://github.com/user-attachments/assets/f44f2438-78e5-40b1-92eb-d2d1b35b754a" />
<img width="1913" height="822" alt="image" src="https://github.com/user-attachments/assets/cca5d083-46b8-4bcb-ba55-9978c5d5c9fe" />

<br>
<br>


# Issue Encountered

* Connecting to SupabaseDB. Currently geeting the following error:
<img width="1410" height="891" alt="image" src="https://github.com/user-attachments/assets/d64e272c-9c3a-4f5e-b2b6-d88d07f36c5a" />

<br>
<br>

# Diagrams & Screenshots
New Database Project set up in Supabase
<img width="1693" height="702" alt="image" src="https://github.com/user-attachments/assets/181b3fc5-c72e-46b5-aac7-83cecc916f14" />
<img width="1477" height="707" alt="image" src="https://github.com/user-attachments/assets/03ee5c5c-4bc8-4c95-9b27-8acc19a9f2b0" />

