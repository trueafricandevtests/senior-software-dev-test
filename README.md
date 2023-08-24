# Microservice-Ecommerce-Exercise

## Introduction
Welcome to the Microservice E-commerce Exercise! In this exercise, you will be building a simplified microservice-based e-commerce application. The main goal is to design and implement an Order Service that handles customer orders, product location determination, and communicates with other services. This exercise will help us assess your technical skills and architectural thinking.

## Instructions

### Step 1: Microservice Architecture Setup
1. Set up a new repository named `microservice-setup`.
2. Create a basic microservice architecture within the repository. Programming languages allowed are Java, Golang, C++ and Python. Golang or Java is a plus.

### Step 2: Implement Order Service
1. Create a new branch named `order-service`.
2. Implement the Order Service according to the provided scenario:
   - Design and implement the data schema for customer orders.
   - Implement CRUD (Create, Read, Update, Delete) operations for orders.
   - Include logic to determine the product location for shipping based on the products and customer profile in the order.
   - Implement an API endpoint `/orders/request` to receive order requests. The API should accept POST requests and handle the creation of new orders.
   ```json
   {
    "shopping_cart_id": 1,
   }
   
### Step 3: API Integration and Communication
1. Create a new branch named `api-integration`.
2. Implement API endpoints for the Order Service to communicate with other services:
   - Implement an API endpoint to alert the Shipping Service about an order along with relevant information. The API URL should be `https://127.0.0.1:8080/api/shipping/receive`, and the request body should be a JSON object:
   ```json
   {
      "order_id": 1,
      "customer_id": 1
   }
3. Implement an API endpoint to notify the Notification Service about the state of an order. The API URL should be https://127.0.0.1:8081/notifications/send, and the request body should be a JSON object:
   ```json
   {
       "customer_id": 1,
       "message": "Order completed"
   }
   
### Step 4: List Orders
Create a new branch named list-orders.
Implement an API endpoint `/orders` to list all orders processed by the Order Service. This endpoint should support GET requests.

### Step 5: Documentation
Create a new branch named documentation.
Write a README.md file that includes:
1. High-level architecture of the microservices.
2. Instructions on how to set up and run the application.
3. API documentation for the implemented endpoints.
4. Any considerations you took into account while designing the architecture or implementing services.
   
### Evaluation Criteria:
Your exercise will be evaluated based on the following criteria:
1. Correctness and completeness of the implemented services and features.
2. Clean and organized code.
3. Effective use of microservice architecture principles.
4. Proper API design and documentation.
5. Consideration of error handling and resilience.
