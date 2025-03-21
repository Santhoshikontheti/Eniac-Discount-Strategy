# Eniac-Discount-Strategy

Data analysis for a Spanish online marketplace company.

## Eniac

Eniac is an online marketplace specializing in Apple-compatible accessories. It was founded 2008 in Spain and has since grown and expanded to other neighboring countries. In addition to offering a wide catalog of products at competitive prices, Eniac provides friendly and professional tech support and consultation to its customers.
Discounts strategy

The company wants to finally settle an ongoing debate: whether or not it’s beneficial to discount products.

The Marketing Team Lead is convinced that offering discounts is beneficial in the long run. She believes discounts improve customer acquisition, satisfaction and retention, and allow the company to grow.
The main investors in the Board are worried about offering aggressive discounts. They have pointed out how the company’s recent quarterly results showed an increase in orders placed, but a decrease in the total revenue. They prefer that the company positions itself in the quality segment, rather than competing to offer the lowest prices in the market.

## Key Considerations :
1.Do aggressive discounts create noticeable higher sales?
2.Is effectiveness of discounts correlated to specific product categories?
3.Is Revenue decreasing due to misplaced discount?
4.Does refined discount strategy can effectively drive increased revenue?



## Work steps
### Data preparation (data_preparation.ipynb)

    Data cleaning
        duplicates
        missing values
        datatypes
    Inconsistency checks
        Remove unwanted orders
        Keep only orders present in both tables
        Exclude orders with unknown products
        Compare revenue from different tables
    Save cleaned and quality-controlled tables.

### Analysis (analysis.ipynb)

    Importing and data preparation
    Exploratory plots of discounts
    Product categorization
    Discount categorization and analysis
    Discount over time

### Presentation

Short business presentation of the most important results (sales_discounts.pdf).
File inventory

    README.md

    sales_discount.pdf

    scripts folder
        data_presentation.ipynb
        analysis.ipynb

    data_original folder
        orders.csv
        orderlines.csv
        products.csv
        brands.cvs

    data_cleaned folder
        orders_qu.csv
        orderlines_qu.csv
        products_qu.csv
        brands_qu.cvs

### Data table description
orders.csv

Every row in this file represents an order.

    order_id – a unique identifier for each order
    created_date – a timestamp for when the order was created
    total_paid – the total amount paid by the customer for this order, in euros
    state
        “Shopping basket” – products have been placed in the shopping basket
        “Place Order” – the order has been placed, but is awaiting shipment details
        “Pending” – the order is awaiting payment confirmation
        “Completed” – the order has been placed and paid, and the transaction is completed.
        “Cancelled” – the order has been cancelled and the payment returned to the customer.

orderlines.csv

Every row represents each one of the different products involved in an order.

    id – a unique identifier for each row in this file
    id_order – corresponds to orders.order_id
    product_id – an old identifier for each product, nowadays not in use
    product_quantity – how many units of that product were purchased on that order
    sku – stock keeping unit: a unique identifier for each product
    unit_price – the unitary price (in euros) of each product at the moment of placing that order
    date – timestamp for the processing of that product

products.csv

    sku – stock keeping unit: a unique identifier for each product
    name – product name
    desc – product description
    price – base price of the product, in euros
    promo_price – promotional price, in euros
    in_stock – whether or not the product was in stock at the moment of the data extraction
    type – a numerical code for product type

brands.csv

    short – the 3-character code by which the brand can be identified in the first 3 characters of products.sku
    long – brand name

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Aggressive discounts hinder number of sales 



![image](https://github.com/user-attachments/assets/f126fc86-1d0c-479f-864a-b186b00fcca0)




Potential revenue increases by tuning the discounts .

![image](https://github.com/user-attachments/assets/68b385a2-1ec2-4ed8-904d-24c46dc43a30)


Final recommendstions are 


--> Aggressive discounts don’t work.
--> Low to Mid discounts can increase sales and potentially better attract new customers.
--> Top-selling products sell regardless of discounts.





