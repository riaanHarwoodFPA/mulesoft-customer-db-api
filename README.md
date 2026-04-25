# mulesoft-customer-db-api


**A mule project that connect different API's to a PostgreSQL database (Supabase)**

<br>

This project is a MuleSoft-based REST API that integrates with a PostgreSQL database hosted on Supabase. The API allows users to send requests (e.g., “create a customer”) and store/retrieve data from the database.

This is a test project used to experiment with MuleSoft integration tools and practice connecting different APIs.

<br>

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

<br>

---




## 🔧 Basic Mule Flow


HTTP Listener → Transform Message → DB Insert

<br>

---

## 📮 POST API

Creates a new customer and adds them to the database.

<img width="533" height="273" alt="Screenshot 2026-04-21 at 12 17 56 AM" src="https://github.com/user-attachments/assets/1a286230-7fc5-4b76-bd03-9c5fff9dc092" />

<img width="1007" height="676" alt="Screenshot 2026-04-21 at 12 18 31 AM" src="https://github.com/user-attachments/assets/2caa5e7f-fc88-43d6-a9e8-5c089295050f" />

<img width="1438" height="517" alt="Screenshot 2026-04-21 at 12 22 31 AM" src="https://github.com/user-attachments/assets/b050f46c-415b-4a9b-9e60-d252ea333336" />

<br>
<br>

**Error Handlers**


**Handler 1** - Validation Error (missing inputs)

**Handler 2** - DB connection Error


<img width="508" height="313" alt="Screenshot 2026-04-21 at 8 01 38 PM" src="https://github.com/user-attachments/assets/025e05fe-8c55-488e-afd6-32c0daf994f1" />

<img width="1008" height="299" alt="Screenshot 2026-04-21 at 8 20 50 PM" src="https://github.com/user-attachments/assets/92ddb727-c4dd-4dd2-ad28-0cb053913db2" />



<br>
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
<br>

## GET Customer by {ID}

<img width="743" height="558" alt="Screenshot 2026-04-25 at 2 39 39 PM" src="https://github.com/user-attachments/assets/8fab8da1-a8cd-497f-9e7e-31e79f57aaaa" />

<br>

<img width="1014" height="614" alt="Screenshot 2026-04-25 at 2 40 02 PM" src="https://github.com/user-attachments/assets/1d668efa-cf35-447d-88ed-3ccfc0a2bb49" />

<br>
<br>

---

## ❌ DELETE API

Removes a customer from the database.

<img width="487" height="281" src="https://github.com/user-attachments/assets/b878a904-aad3-4e39-9d7b-7927193d20db" />
<img width="1382" height="738" src="https://github.com/user-attachments/assets/908a088f-c068-4424-bdd6-e3989ca2267f" />


<br>
<br>

**Error Handlers**

**Handler 1** - Unable to find user based off id {/id}

<img width="445" height="169" alt="Screenshot 2026-04-21 at 8 02 37 PM" src="https://github.com/user-attachments/assets/0e66c8d0-3695-4e86-89b6-6d472464acb1" />

<img width="389" height="163" alt="Screenshot 2026-04-21 at 8 02 48 PM" src="https://github.com/user-attachments/assets/1b328c76-f647-43de-8966-bdc6021e7140" />


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

**Handler 1** - Unable to find user based off id {/id}

**Handler 2** - DB connection Error 

**Handler 3** - Connectiont/Network error 

<img width="644" height="469" alt="Screenshot 2026-04-21 at 10 05 35 PM" src="https://github.com/user-attachments/assets/d38c33d6-ff33-436e-bc88-95e60c9289fb" />


<img width="1013" height="674" alt="Screenshot 2026-04-21 at 10 06 04 PM" src="https://github.com/user-attachments/assets/13c3239b-107b-4a6d-90b9-c486a6764c68" />



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

<img width="757" height="1667" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/d4faaada-4683-41e0-a083-a79b0598edfa" />

<br>

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

<br>
<br>

## Deployment - CloudHUB

<img width="997" height="803" alt="Screenshot 2026-04-22 at 11 39 05 AM" src="https://github.com/user-attachments/assets/36e1ee34-3519-4b7c-b033-6aef8ccb1368" />

<img width="1422" height="723" alt="Screenshot 2026-04-22 at 11 40 19 AM" src="https://github.com/user-attachments/assets/4cf43444-7362-46f8-9fa2-50adf95a77a6" />


---
<br>
<br>

## 🧩 API Specification (API Designer)


<img width="1917" height="826" src="https://github.com/user-attachments/assets/aa02ead8-53dc-46fd-9acc-6a07e5b6b998" />
<img width="1917" height="825" src="https://github.com/user-attachments/assets/f44f2438-78e5-40b1-92eb-d2d1b35b754a" />
<img width="1913" height="822" src="https://github.com/user-attachments/assets/cca5d083-46b8-4bcb-ba55-9978c5d5c9fe" />

---
<br>
<br>

## ⚠️ Issue Encountered

- Connecting to Supabase DB  
- Currently getting the following error:
- Deployment - "**No listener for endpoint: /**"
  
<img width="1410" height="891" src="https://github.com/user-attachments/assets/d64e272c-9c3a-4f5e-b2b6-d88d07f36c5a" />


<br>

---

## 🖼️ Diagrams & Screenshots

New database project setup in Supabase:

### 🔹 Supabase Database Setup

<img width="1693" height="702" src="https://github.com/user-attachments/assets/181b3fc5-c72e-46b5-aac7-83cecc916f14" />
<img width="1477" height="707" src="https://github.com/user-attachments/assets/03ee5c5c-4bc8-4c95-9b27-8acc19a9f2b0" />

<br>

---
<br>

## 📈 Future Improvements

<br>

- **Modern Frontend/UI**
- **Implement getCustomerById flow**
- Add authentication & security (OAuth/JWT)
- Improve error handling consistency across all endpoints
- Implement logging and monitoring
- Expand API with additional business logic
- Add frontend client for real-world usage


---
<br>

## 📄 Summary

<br>

This project showcases the fundamentals of building an integration-focused REST API using MuleSoft. It highlights core concepts such as API design, data transformation, error handling, and cloud database connectivity.
