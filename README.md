# mulesoft-customer-db-api


**A mule project that connect different API's to a PostgreSQL database (Supabase)**

<br>

This project is a MuleSoft-based REST API that integrates with a PostgreSQL database hosted on Supabase. The API allows users to send requests (e.g., “create a customer”) and store/retrieve data from the database.

This is a test project used to experiment with MuleSoft integration tools and practice connecting different APIs.

---

## 🔄 Workflow

```
User (Postman / App) → Sends Request (Add, Retrieve, Delete, Update)
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

<img width="533" height="273" alt="Screenshot 2026-04-21 at 12 17 56 AM" src="https://github.com/user-attachments/assets/1a286230-7fc5-4b76-bd03-9c5fff9dc092" />

<img width="1007" height="676" alt="Screenshot 2026-04-21 at 12 18 31 AM" src="https://github.com/user-attachments/assets/2caa5e7f-fc88-43d6-a9e8-5c089295050f" />

<img width="1438" height="517" alt="Screenshot 2026-04-21 at 12 22 31 AM" src="https://github.com/user-attachments/assets/b050f46c-415b-4a9b-9e60-d252ea333336" />

<br>
<br>

**Error Handlers**


<br>

---

## 📥 GET API

Retrieves all customers from the database as JSON.

<img width="397" height="287" src="https://github.com/user-attachments/assets/4584cc5a-1a04-4028-a8ae-f822eaef3dc6" />
<img width="1376" height="877" src="https://github.com/user-attachments/assets/3886395b-838d-4d6e-9af8-7c6c8ba632b9" />

<br>
<br>

**Error Handlers**

**Handler 1** — Database errors

**Handler 2** — Unexpected errors


<img width="347" height="315" alt="Screenshot 2026-04-21 at 6 50 39 PM" src="https://github.com/user-attachments/assets/04964572-09eb-4213-8304-fdebd1c369d7" />

<img width="1014" height="484" alt="Screenshot 2026-04-21 at 6 51 14 PM" src="https://github.com/user-attachments/assets/f20365b1-4c90-4e70-9fcc-aa9260b239c1" />


<br>

---

## ❌ DELETE API

Removes a customer from the database.

<img width="487" height="281" src="https://github.com/user-attachments/assets/b878a904-aad3-4e39-9d7b-7927193d20db" />
<img width="1382" height="738" src="https://github.com/user-attachments/assets/908a088f-c068-4424-bdd6-e3989ca2267f" />


<br>
<br>

**Error Handlers**


<br>


---

## ✏️ PATCH API

Applies partial updates to an existing customer.

<img width="756" height="307" alt="image" src="https://github.com/user-attachments/assets/d8ad4a03-19bb-4547-b846-21dbbb956913" />


<img width="1437" height="513" alt="Screenshot 2026-04-21 at 1 05 13 AM" src="https://github.com/user-attachments/assets/0d7597d4-2176-4767-83f0-87adced6a1ce" />

<br>

**Updated Details**

<br>

<img width="1052" height="727" alt="Screenshot 2026-04-21 at 1 09 48 AM" src="https://github.com/user-attachments/assets/53bbf833-8c45-4dd6-b0ae-b9c13b704484" />

<img width="1435" height="617" alt="Screenshot 2026-04-21 at 1 10 05 AM" src="https://github.com/user-attachments/assets/4d6f9942-d704-4404-98af-0d60b4e95b3b" />


<br>
<br>

**Error Handlers**


<br>


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

+ Open **customer-db-api** in VS Code OR Anypoint Studio to view and run the workflow.

+ Test Each API using **POSTMAN** (PORT: 8081) 


<br>

---

## ⚙️ Tech Stack

- MuleSoft (Anypoint Studio) || Visual Studio 
- PostgreSQL
- Supabase
- DataWeave
- GitHub
- Postman

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

