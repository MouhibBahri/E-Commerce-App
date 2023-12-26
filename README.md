# E-Commerce-App

## Class Diagram Overview
###### The class diagram is a visual representation of the system's structure, depicting classes, interfaces, and their relationships. It serves as a blueprint for understanding the application's OOP implementation.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/3aa35e45-b67a-477c-82ed-848bf4555080)

## ISharedFunctions Interface
###### This interface provides methods for consistent user interaction and output formatting:
###### - getIntInput(String, int, int): Retrieves user input within a range.            
###### - printMenu(String): Displays a formatted menu.                                   
###### - roundPrice(double): Rounds a price to two decimal places. 

## Data Storage 
###### Text files are used for persistence:

###### -accounts.txt: Stores user credentials and types.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/ddc398d3-02f3-49e7-99a5-9708f5ecacc1)

###### -products.txt: Contains product details like ID, name, description, category, price, and stock.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/b8e50025-3aed-41f4-8ae7-ae3dce46f50f)

###### -orders.txt: Lists orders with client information and product details.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/14d929f3-bfcd-4b16-ad6a-ab570e3a00ff)

###### -shopping_carts.txt: Tracks customer carts with product IDs and quantities.
![image](https://github.com/MouhibBahri/E-Commerce-App/assets/123774260/6bc23398-1c36-4652-9792-b79d41716d4c)
