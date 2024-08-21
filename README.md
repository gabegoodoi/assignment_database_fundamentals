# Schema Entities

Books

    - isbn VARCHAR(13) ... PK
    - title VARCHAR(100)
    - synopsis TEXT
    - inventory INT
    - date_published DATE
    - authors_id INT ... FK references Authors
    - usd_price DECIMAL(10, 2)

Authors

    - id INT
    - name VARCHAR(100)
    - bio TEXT

Customers

    - id INT ... PK
    - name VARCHAR(100)
    - address VARCHAR(100)
    - saved_payment VARCHAR(100)

Transactions

    - id INT ... PK
    - usd_total DECIMAL(10, 2)
    - date DATE
    - customers_id INT ... FK references Customers

Orders

    - id INT ... PK
    - books_isbn VARCHAR(13) ... FK references Books
    - quantity INT
    - transactions_id INT ... FK references Transactions

# Entity Relationships

    - Authors relationship to Books: 1 to many
    - Customers relationship to Transactions: 1 to many
    - Books relationship to Orders: 1 to many
    - Transactions relationship to Orders: 1 to many

# Link to ERD
https://drive.google.com/file/d/1HnB19bjxQkqZ5lbWrtv6O02EK3D_LgB7/view?usp=sharing
