1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
Answer : The "Product" and "Product_Category" entities is that a product belongs to one category.  Each product has a foreign key called "category_id" that references the primary key "id" of the "Product_Category" table. This indicates a one-to- many relationship between "Product_Category" and "Product".

In simpler terms, a product category can have many products, but a product can only belong to one category. For instance, a sports shoe category can have many different sports shoes, but a specific running shoe can only be categorized as a sports shoe and not any other category.
