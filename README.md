# E-Commerce-App

##### Welcome to Hike Haven, an eCommerce platform developed for academic purposes using Java. This README provides essential information for users and developers.

*Note 1:* For administrative purposes, the software includes a default admin account. This account is intended for initial setup and should be promptly updated with custom credentials to enhance security.
- Username: admin
- Password: admin

*Note 2:* A detailed documentation can be found here: [Hike Haven Documentation](https://mouhibbahri.slite.page/p/Msgev4wVeab6GJ/Hike-Haven-Documentation)

## Class Diagram Overview

##### The class diagram offers a high-level view of the Hike Haven application, illustrating key classes and interfaces. Dive into each feature for an in-depth understanding.
<p align="center">
  <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/6099ce0b-5009-4de7-92a5-ae27a0376e07" height="430" alt="Class Diagram">

*Note:* The ISharedFunctions interface is crucial for consistent interaction and output formatting, such as getIntInput, printMenu, and roundPrice.

## Key Features

### Data Storage 

For this project, the chosen method for data storage revolves around the utilization of text files. We have adopted text files to store crucial information such as accounts, products, orders, and shopping carts. This decision was made for its simplicity, ease of implementation, and human-readable nature.

#### Organizing Data in Text Files:

- *Users Accounts:* Captures username, password, and user type (customer/admin).

  <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/85c2633e-b0db-4087-aa2a-54b3b0fa06cc"  height="120">
 
- *Products:* Includes essential attributes like product ID, name, description, category, price, quantity in stock, and other specific attributes relevant to each category.

  <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/5d1de79b-e1ee-4075-b77a-00326db7e5ca"  height="150">


- *Orders:* Details about client information and purchased products.
  
  <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/259fb65c-d307-42a4-a2e7-954b240877ca"  height="120">

- *Shopping Carts:* Manages customer carts, including product IDs and quantities.
 
  <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/ab25e1e7-d69d-4c43-8781-da7ab74d0796"  height="70">
<br>

### User Authentication

##### The robust user authentication system involves the UserModel class, UsersList class, and WelcomeScreen class.

- **UserModel Class**
  
 Central entity encapsulating user-related information, with subclasses for Admin and Customer.

<img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/6ab90c82-8806-470f-9f38-2bd55e407324" width="400" height="390">

<br>
<br>

- **UsersList Class**
  
Manages user accounts using a static map, performs CRUD operations, and enforces unique usernames.

<img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/637f32fb-1f95-4637-82c8-d5637ea95bb7"  height="250">
<br>
<br>

- **WelcomeScreen Class**
  
Initial point of interaction for users, facilitating login, signup, and user type differentiation.

<img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/17f7edcc-aade-44c6-9be2-d7309dce6dd4"  height="250">
<br>
<br>

- **IService Interface**
  
After the Welcome Screen and user authentication, users are seamlessly directed to the Service Layer, where two distinct services cater to their specific needs: AdminService and CustomerService, both located in the services package.

<img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/97179f35-f922-41eb-bcbe-a9fb704aa35a" height="250">
<br>
<br>

- **AdminService Class**
  
Designed for administrators, offering account, product, order management, and report generation.
<br>
<br>

- **IEntityManager**
  
The AdminService utilizes the IEntityManager interface to standardize entity management operations. This interface performs CRUD operations and is implemented in the following classes: ManageAccounts, ManageOrders, and ManageProducts.

<img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/ce9f95ee-e339-4fd3-8869-fded8dd69e67" height="360">
<br>
<br>

### Product Management
#### The Product Management feature encompasses two key classes within the productsData package.

- **ProductModel Class**
  - The ProductModel class serves as the base entity for product representation. It encapsulates essential attributes common to all products (productId, productPrice, productDescription, productName, quantityInStock, score).
  - Several subclasses extend from ProductModel Class, each catering to a specific product category: AdventureGear, ExplorationTools, HealthAndFitness, TravelEssentials, Others.
  - Each subclass adds its unique attributes and can override general methods, such as toString, to tailor the representation to the specific product category.
    <br>
    <br>
    
    <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/65efeda3-f7d2-4278-9403-8d9fca06bdad" height="340">
<br>

- **ProductsList Class**
  - Dynamic repository for storing and managing products in a text file, featuring CRUD operations and filtering based on specific criteria.

 <br>
 
### Management of Shopping Cart

#### The Shopping Cart functionality enables users to efficiently manage their selected products before finalizing a purchase.

- **ShoppingCart Class**
  - Foundation for cart management, with methods for adding, updating, and removing items.
   
    <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/6c065f47-48e2-48b2-907a-1dcdcf180fcd" height="80">
 
### Order Processing

#### Facilitates the transition from cart to order completion using the OrderModel and OrdersList classes within the UsersData package.

- **OrderModel Class**
  - The OrderModel class encapsulates the details of an order, including the customer, items selected for purchase, a unique order ID (automatically incremented), and the total price of the order.
 
    <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/a990ef4b-bb3f-4e71-b06c-f1eb34a0fcc4" height="250">
 
- **OrdersList Class**
  - The OrdersList class serves as a centralized hub for order management, featuring a static TreeMap of orders. It facilitates CRUD operations on orders, as well as the ability to save orders to and retrieve         orders from a file.
    
    <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/49a6a50c-9cd6-4d8d-9228-ba7d1d76f0cc" height="150">
  
 <br>
 
### Inventory Management

#### The Inventory Management feature in the Hike Haven application ensures automated tracking and updates of the product inventory post-purchase.

- **OrderModel Class**
  - The OrderModel class ensures inventory management during order completion. The completeOrder method within this class is executed only after verifying that each product in the order is available in stock.

- **ShoppingCart Class**
  - The ShoppingCart class ensures that products added to the cart have quantities available in stock. This preventive measure guarantees that users can only add products that are currently in stock, reducing the likelihood of issues during the order completion process.

- **ProductsList Class**
  - The updateInventory method within the OrderModel class interacts with the ProductsList class, ensuring that product quantities are appropriately updated after an order is completed. This dynamic relationship guarantees accurate and up-to-date inventory tracking.

 <br>
 
### Key Functions

1. *Automated Tracking*: Inventory is automatically updated after each purchase, ensuring real-time accuracy in product quantities.
   
2. *Preventive Measures*: The ShoppingCart class enforces restrictions on adding products to the cart, ensuring that only products with available quantities can be selected.
   
3. *Low Stock Handling*: The system is designed to address scenarios of low or out-of-stock items, enabling measures like updating product availability and providing administrators with insights on products running low within the reports.

 <br>
 
### Dynamic Product Search and Filtering

#### Search Functionality
- Users can conduct efficient searches by entering case-insensitive keywords related to product names.

#### Filtering Options
- The ProductsList class features a comprehensive method for filtering products based on multiple criteria, including price range, category, and availability.
- Filtering is entirely optional, allowing users the flexibility to choose specific criteria for refining search results.

```java
public static ArrayList<ProductModel> filterProducts(double maxPrice, double minPrice, String category, String productName, boolean inStock) {
    // Implementation details for filtering products
}
```

 <br>
 
### Payment Processing

The Payment Processing feature is seamlessly integrated into the OrderModel class. Upon completing an order, users are prompted for basic credit card information.
 <br>
<br>
 
## Optional Yet Crucial Features
 <br>
 
### Product Recommendations

#### Functionality Overview
- Hike Haven's Product Recommendation system, powered by the RecommendationSystem class, enhances the user experience by providing personalized suggestions.
- Recommendations are tailored to each user's preferences, leveraging their purchase history and patterns.

#### Scoring Algorithm
- The system employs a sophisticated scoring algorithm:
  - A score of 0.02 times the quantity bought is added for each product in the same category as the user's past purchases; which means when a user buys from a certain category, all other products from that category should be more likely to be featured.
  - An additional score of 0.01 times the quantity sold contributes to the overall product score; which means top-selling products should be more likely to be featured.

#### User-Centric Approach
- This feature creates a dynamic and engaging shopping environment, presenting users with products aligned with their interests and buying patterns.

#### Implementation Details
- The RecommendationSystem class, located in the productsData package, dynamically calculates scores for all products upon user authentication. This approach ensures a personalized and context-aware recommendation system, enhancing the overall user experience.
- It uses a combination of purchase history and global popularity to deliver relevant and enticing suggestions.

    <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/151a2b58-e076-4c1e-b3cc-9ee1c2c0b9ff"  height="100">

 <br>
 
### Generating Reports

#### Functionality Overview
- The ManageReports class, part of the services package, automates the generation of comprehensive reports, providing valuable insights for administrators.
- Reports cover diverse aspects, including financial metrics, order analytics, and product availability.

#### Key Reports
- Average Order Value
  - Calculates the average value of orders, offering an overview of customer spending patterns.
- Lowest and Highest Order
  - Identifies extreme values in the order history, aiding in understanding outliers.
- Best-Selling Products
  - Ranks products based on the quantity sold, helping administrators identify popular items.
- Low Stock Products
  - Flags products with stock quantities below a predefined threshold, prompting timely restocking decisions.

#### User-Friendly Presentation
- The show method in ManageReports ensures reports are presented in a clear and organized manner, facilitating quick comprehension.

#### Automation for Efficiency
- Reports are automatically generated at the administrator's request, saving time and ensuring up-to-date insights into the platform's performance.

#### Future Enhancements
- The system is designed with extensibility in mind, allowing for the addition of more reporting functionalities in future updates.

  <img src="https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/15c10191-53e9-4afe-8b03-b430f9041690" height="180">

<br>

## Wrap-Up
As we wrap up this journey through the developer documentation, we extend our sincere gratitude for your interest in the Hike Haven Console Application. We trust you found value in this README, and we appreciate your time and attention.

Feel free to let me know if you have any more requests or if you'd like further modifications!
