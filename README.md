# API_Ecommerce_E2E 🚀

   End-to-End API Automation Testing framework for an **E-commerce application** using **Postman**, **Newman**, and **Git**.
                
   This project covers the complete API flow including authentication, product creation, order creation, order verification, and cleanup (delete operations).



## 🔧 Tech Stack
                  
                  - **Postman** – API test design
                  - **Newman** – CLI execution
                  - **JavaScript** – Test scripting
                  - **Git & GitHub** – Version control
                  - **Jenkins (optional)** – CI execution



## 📁 Project Structure

                    API_Ecommerce_E2E/
                    │
                    ├── Ecommerce_E2E.postman_collection.json # Postman collection
                    ├── data/
                    │ └── shirt.jpg # Product image for upload
                    ├── README.md

                    ## 🔄 API Test Flow (E2E)
            
            1. **Login**
               - Authenticates user
               - Stores token in collection variables
            
            2. **Create Product**
               - Uploads product with image
               - Stores `productId`
            
            3. **Create Order**
               - Places order using `productId`
               - Stores `orderId`
            
            4. **View Order Details**
               - Fetches order information
               - Validates response fields
            
            5. **Delete Product**
               - Deletes created product
            
            6. **Delete Order**
               - Deletes created order
            

## ▶️ How to Run Tests (CLI)

### Prerequisites
      - Node.js installed
      - Newman installed
      
      ```bash
      npm install -g newman

## ** Run Collection**

           newman run Ecommerce_E2E.postman_collection.json

 ## ** Notes**

                All variables are managed using Postman Collection Variables
                
                Image upload uses local file path (Newman compatible)
                
                No Postman Cloud files are used
                
                Tests are CI-safe and Git-friendly

## **Reports (Optional)**

To generate HTML report:

      newman run Ecommerce_E2E.postman_collection.json -r cli,htmlextra
