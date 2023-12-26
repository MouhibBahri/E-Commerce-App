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
### For this project, the chosen method for data storage revolves around the utilization of text files. We have adopted text files to store crucial information such as accounts, products, orders, and shopping carts. This decision was made for its simplicity, ease of implementation, and human-readable nature.

#### Organizing Data in Text Files
##### - **Users Accounts:** Captures username, password, and user type ( customer / admin ).
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/85c2633e-b0db-4087-aa2a-54b3b0fa06cc)

##### - **Products:** Includes essential attributes like product ID, name, description, category, price, and quantity in stock and other specific attributes relevant to each category.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/5d1de79b-e1ee-4075-b77a-00326db7e5ca)

##### - **Orders:** Details about client information and purchased products.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/259fb65c-d307-42a4-a2e7-954b240877ca)

##### - **Shopping Carts:** Manages customer carts, including product IDs and quantities.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/ab25e1e7-d69d-4c43-8781-da7ab74d0796)

### User Authentication

##### The robust user authentication system involves the `UserModel` class, `UsersList` class, and `WelcomeScreen` class.

#### UserModel Class

##### Central entity encapsulating user-related information, with subclasses for Admin and Customer
![2](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/6ab90c82-8806-470f-9f38-2bd55e407324)

#### UsersList Class
##### Manages user accounts using static map, performs CRUD operations, and enforces unique usernames.
![3](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/637f32fb-1f95-4637-82c8-d5637ea95bb7)

#### WelcomeScreen Class
##### Initial point of interaction for users, facilitating login, signup, and user type differentiation. 
![4](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/17f7edcc-aade-44c6-9be2-d7309dce6dd4)

#### IService Interface
##### After the Welcome Screen and user authentication, users are seamlessly directed to the Service Layer, where two distinct services cater to their specific needs: AdminService and CustomerService, both located in the services package.
![5](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/97179f35-f922-41eb-bcbe-a9fb704aa35a)

### AdminService Class
##### Designed for administrators, offering account, product, order management, and report generation.

#### IEntityManager
##### The AdminService utilizes the IEntityManager interface to standardize entity management operations. This interface performs CRUD operations and is implemented in the following classes: ManageAccounts, ManageOrders, and ManageProducts
![6](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/ce9f95ee-e339-4fd3-8869-fded8dd69e67)

### Product Management
##### The Product Management feature encompasses two key classes within the productsData package.

#### ProductModel Class
##### The ProductModel class serves as the base entity for product representation. it  encapsulates essential attributes common to all products( productId, productPrice, productDescription, productName, quantityInStock, score )

##### several subclasses extend from ProductModel Class: each catering to a specific product category: AdventureGear, ExplorationTools, HealthAndFitness, TravelEssentials, Others.

##### Each subclass adds its unique attributes and can override general methods, such as toString, to tailor the representation to the specific product category.
![7](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/65efeda3-f7d2-4278-9403-8d9fca06bdad)

#### ProductsList Class
###### Dynamic repository for storing and managing products in a text file, featuring CRUD operations and filtering based on a specific critera.



