# E-Commerce-App
### Welcome to Hike Haven, an eCommerce platform developed for academic purposes using Java. This README provides essential information for users and developer
### . Software Name: Hike Haven
### . Version: 1.00
### . Date: December 2023

## Class Diagram Overview
#### The class diagram offers a high-level view of the Hike Haven application, illustrating key classes and interfaces. Dive into each feature for an in-depth understanding.
![1](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/6099ce0b-5009-4de7-92a5-ae27a0376e07)

### **Note:** The `ISharedFunctions` interface is crucial for consistent interaction and output formatting. such us `getIntInput`, `printMenu`, and `roundPrice`.

## Key Features

## Data Storage 
##### Text files are used for persistence:

#### -accounts.txt: Stores user credentials and types.

#### -products.txt: Contains product details like ID, name, description, category, price, and stock.

#### -orders.txt: Lists orders with client information and product details.

#### -shopping_carts.txt: Tracks customer carts with product IDs and quantities.

## User Authentication

### UserModel Class
#### - Found in the usersData package.
#### - Serves as the base class for Admin and Customer subclasses.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/a2d2d320-a4da-494f-a4d6-2aa0d5dea6e8)

### UsersList Class
#### - Manages user accounts and performs CRUD operations.
#### - Uses a static map for account storage and retrieval.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/7e20d2d9-736d-4a22-a5b4-6d4638f7e418)

### WelcomeScreen Class
#### - Initial user interface providing login, signup, and exit options.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/17105b71-8558-458e-803d-9a03af481afb)

### IService Interface
#### - Directs users to AdminService or CustomerService post-authentication.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/600bdb3e-f881-4579-8afc-e8963f51f3f6)

### AdminService Class
#### - Tailored for administrator users.
#### - Manages accounts, products, orders, and report generation.

### IEntityManager Interface
#### - Used by AdminService to standardize CRUD operations on entities.
#### - Implemented by ManageAccounts, ManageOrders, and ManageProducts classes for respective entity management.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/a49b0635-89a7-4fae-b52d-ba01b667b5c3)

## Product Management

### ProductModel Class
#### - Base class in productsData package : The ProductModel class acts as a base class with essential attributes like product ID, price, description, name, quantity in stock, and a popularity score.
#### - Contains common product attributes : like AdventureGear, ExplorationTools, HealthAndFitness, and TravelEssentials
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/7b5408e5-a0f5-4d6a-8fa1-8250641c0925)


### ProductsList Class
#### - Manages a list of products and supports CRUD operations.



