1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
Answer : The "Product" and "Product_Category" entities is that a product belongs to one category.  Each product has a foreign key called "category_id" that references the primary key "id" of the "Product_Category" table. This indicates a one-to- many relationship between "Product_Category" and "Product".

  In simpler terms, a product category can have many products, but a product can only belong to one category. For instance, a sports shoe category can have many different sports shoes, but a specific running shoe can only be categorized as a sports shoe and not any other 
   category.
2. How could you ensure that each product in the "Product" table has a valid category assigned to it?
Answer : Enforce referential integrity constraints: A referential integrity constraint is a database rule that ensures the data integrity between two tables. In the context of the image, you can create a foreign key constraint on the "category_id" column in the "Product" table. This foreign key constraint would reference the primary key of the "product_category" table. By doing this, the database would only allow products to be inserted into the "Product" table if the corresponding "category_id" exists in the "product_category" table.

Validate data during insert and update operations: You can also write code to validate the data during insert and update operations on the "Product" table. This code could check if the provided "category_id" exists in the "product_category" table before inserting or updating the product record.

Both of these approaches will help to ensure that each product in the "Product" table has a valid category assigned to it.
