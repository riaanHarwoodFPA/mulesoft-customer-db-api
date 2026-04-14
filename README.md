# mulesoft-customer-db-api


**A mule project that connect different API's to a PostgreSQL database (Supabase)**

<br>

This project is a MuleSoft-based REST API that integrates with a PostgreSQL database hosted on Supabase. The API allows users to send requests (e.g., “create a customer”) and store/retrieve data from the database.

This is a test project used to experiment with MuleSoft integration tools and practice connecting different APIs.

---

## 🔄 Workflow

```
User (Postman / App) → Sends Request (Add, Preview, Delete, Update)
      ↓
MuleSoft API (process request)
      ↓
PostgreSQL Database (Supabase)
      ↓
MuleSoft API (response)
      ↓
User receives response (Postman)
```

---

## 🔧 Basic Mule Flow


HTTP Listener → Transform Message → DB Insert


---

## 📮 POST API

Creates a new customer and adds them to the database.

<img width="386" height="306" src="https://github.com/user-attachments/assets/48ddeac7-999b-45e6-80ec-9e04826e45fd" />
<img width="1381" height="815" src="https://github.com/user-attachments/assets/e3bc1e3c-ba23-4e19-9845-15cfbaf12d20" />

---

## 📥 GET API

Retrieves all customers from the database as JSON.

<img width="397" height="287" src="https://github.com/user-attachments/assets/4584cc5a-1a04-4028-a8ae-f822eaef3dc6" />
<img width="1376" height="877" src="https://github.com/user-attachments/assets/3886395b-838d-4d6e-9af8-7c6c8ba632b9" />

---

## ❌ DELETE API

Removes a customer from the database.

<img width="487" height="281" src="https://github.com/user-attachments/assets/b878a904-aad3-4e39-9d7b-7927193d20db" />
<img width="1382" height="738" src="https://github.com/user-attachments/assets/908a088f-c068-4424-bdd6-e3989ca2267f" />

---

## ✏️ PATCH API

Applies partial updates to an existing customer.

---

## 🧪 Example Request


POST /customers
```
{
      "firstName": "Riaan",
      "lastName": "Harwood",
      "email": "riaan@email.com"
}
```

---

<br>

## 🛠️ Instructions

Open **customer-db-api** in VS Code OR Anypoint Studio to view and run the workflow.

Test Each API using **POSTMAN** (PORT: 8081) 


<br>

---

## ⚙️ Tech Stack

- MuleSoft (Anypoint Studio)
- PostgreSQL
- Supabase
- DataWeave

---

## 🚀 Features

- Create a customer
- Retrieve customers
- Update customer details
- Delete a customer

---

## 🏗️ Architecture

This project follows a simplified API-led connectivity approach:

- MuleSoft → Integration layer  
- PostgreSQL (Supabase) → Data source  
- DataWeave → Data transformation  

---

## 📊 Architecture Diagram

_To be updated_

---

## 🔌 Summary of API Endpoints

### ➕ Create Customer
**POST /customers**

Creates a new customer.

---

### 📥 Get Customers
**GET /customers**

Retrieves all customers.

---

### 🔄 Update Customer
**PUT /customers/{id}**

Updates an existing customer.

---

### ❌ Delete Customer
**DELETE /customers/{id}**

Deletes a customer.

---

## 🧩 API Specification (API Designer)

<img width="1917" height="826" src="https://github.com/user-attachments/assets/aa02ead8-53dc-46fd-9acc-6a07e5b6b998" />
<img width="1917" height="825" src="https://github.com/user-attachments/assets/f44f2438-78e5-40b1-92eb-d2d1b35b754a" />
<img width="1913" height="822" src="https://github.com/user-attachments/assets/cca5d083-46b8-4bcb-ba55-9978c5d5c9fe" />

---

## ⚠️ Issue Encountered

- Connecting to Supabase DB  
- Currently getting the following error:

<img width="1410" height="891" src="https://github.com/user-attachments/assets/d64e272c-9c3a-4f5e-b2b6-d88d07f36c5a" />

---

## 🖼️ Diagrams & Screenshots

New database project setup in Supabase:

<img width="1693" height="702" src="https://github.com/user-attachments/assets/181b3fc5-c72e-46b5-aac7-83cecc916f14" />
<img width="1477" height="707" src="https://github.com/user-attachments/assets/03ee5c5c-4bc8-4c95-9b27-8acc19a9f2b0" />

