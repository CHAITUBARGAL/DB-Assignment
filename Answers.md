*1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.* <br>
Answer : The "Product" and "Product_Category" entities is that a product belongs to one category.  Each product has a foreign key called "category_id" that references the primary key "id" of the "Product_Category" table. This indicates a one-to- many relationship between "Product_Category" and "Product". In simpler terms, a product category can have many products, but a product can only belong to one category. For instance, a sports shoe category can have many different sports shoes, but a specific running shoe can only be categorized as a sports shoe and not any other 
   category. <br>
<br>
<br>
*2. How could you ensure that each product in the "Product" table has a valid category assigned to it?* <br>
Answer : Enforce referential integrity constraints: A referential integrity constraint is a database rule that ensures the data integrity between two tables. In the context of the image, you can create a foreign key constraint on the "category_id" column in the "Product" table. This foreign key constraint would reference the primary key of the "product_category" table. By doing this, the database would only allow products to be inserted into the "Product" table if the corresponding "category_id" exists in the "product_category" table.

Validate data during insert and update operations: You can also write code to validate the data during insert and update operations on the "Product" table. This code could check if the provided "category_id" exists in the "product_category" table before inserting or updating the product record.

Both of these approaches will help to ensure that each product in the "Product" table has a valid category assigned to it.

<br>
<br>
<br>
3. Create schema in any Database script or any ORM  <br>
Answer : product_category <br>

id (int): The unique identifier for the product category.
name (varchar): The name of the product category.
desc (text): A description of the product category.
created_at (timestamp): The date and time the product category was created.
modified_at (timestamp): The date and time the product category was last modified.
deleted_at (timestamp): The date and time the product category was soft deleted.
product

id (int): The unique identifier for the product.
name (varchar): The name of the product.
desc (text): A description of the product.
SKU (varchar): The unique stock keeping unit for the product.
category_id (int): The foreign key referencing the product_category table.
inventory_id (int): The foreign key referencing the product_inventory table (not shown in the image).
price (decimal): The price of the product.
discount_id (int): The foreign key referencing the discount table.
created_at (timestamp): The date and time the product was created.
modified_at (timestamp): The date and time the product was last modified.
deleted_at (timestamp): The date and time the product was soft deleted.
discount

id (int): The unique identifier for the discount.
name (varchar): The name of the discount.
desc (text): A description of the discount.
discount_percent (decimal): The discount percentage.
active (boolean): A flag indicating if the discount is active.
created_at (timestamp): The date and time the discount was created.
modified_at (timestamp): The date and time the discount was last modified.
deleted_at (timestamp): The date and time the discount was soft deleted.
This schema uses relationships between tables to represent complex data. For instance, a product can belong to one category (product_category) and have one discount (discount).
