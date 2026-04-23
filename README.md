# **Product Inventory App (FastAPI + React)**

A full-stack **Product Inventory Management System** built using **FastAPI** for the backend and **React** for the frontend.
This application allows users to manage products with full CRUD functionality and inventory tracking.

---

## Features

### Backend (FastAPI)

* GET `/products/` → Get all products
* GET `/products/{product_id}` → Get product by ID
* POST `/products/` → Create a new product
* PUT `/products/{product_id}` → Update product
* DELETE `/products/{product_id}` → Delete product

### Frontend (React)

* Add new products
* Edit existing products
* Delete products
* Search products
* Sort products (ID, price, quantity)
* Responsive UI

---

# Tech Stack

## Backend
* FastAPI  
* SQLAlchemy  
* PostgreSQL  
* Uvicorn  

## Frontend
* React  
* Axios  
* Node.js  

---

## Backend Setup

### 1. Create and activate virtual environment

```
python -m venv myenv
myenv\Scripts\activate
```

### 2. Install dependencies

```
pip install fastapi uvicorn sqlalchemy psycopg2-binary
```

### 3. Run the application

```
cd backend
uvicorn main:app --reload
```

### 4. Access backend

* API: http://localhost:8000
* Docs: http://localhost:8000/docs
* ReDoc: http://localhost:8000/redoc

---

## Frontend Setup

```
cd frontend
npm install
npm start
```

### Access frontend

* http://localhost:3000

---

## Project Structure

```
product-inventory-app/
│
├── backend/
│   ├── main.py
│   ├── database.py
│   ├── database_models.py
│   ├── models.py
│
├── frontend/
│   ├── public/
│   ├── src/
│   ├── package.json
│
├── .gitignore
├── README.md
```

---

## API Usage Examples

### Get all products

```
curl http://localhost:8000/products/
```

### Get product by ID

```
curl http://localhost:8000/products/1
```

### Create a new product

```
curl -X POST "http://localhost:8000/products/" \
-H "Content-Type: application/json" \
-d '{
  "id": 5,
  "name": "Monitor",
  "description": "4K monitor",
  "price": 299.99,
  "quantity": 15
}'
```

### Update a product

```
curl -X PUT "http://localhost:8000/products/1" \
-H "Content-Type: application/json" \
-d '{
  "id": 1,
  "name": "Updated Product",
  "description": "Updated description",
  "price": 500,
  "quantity": 10
}'
```

### Delete a product

```
curl -X DELETE "http://localhost:8000/products/1"
```

---

## Product Model

* id: integer
* name: string
* description: string
* price: float
* quantity: integer

---

## Built With

* FastAPI – Backend framework
* SQLAlchemy – ORM
* PostgreSQL – Database
* React – Frontend
* Axios – API requests
