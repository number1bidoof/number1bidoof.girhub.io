``` mermaid
erDiagram
    CUSTOMER {
        int customer_id PK
        string customer_name
        string customer_email
        string customer_phone
    }

    PRODUCT {
        int product_id PK
        string product_name
        string product_description
        decimal product_price
    }

    SALE {
        int sale_id PK
        int customer_id FK
        date sale_date
        decimal order_price
    }

    INVENTORY {
        int product_id FK
        int stock_quantity
        string stock_ID PK
    }

    CUSTOMER ||--o{ SALE : makes
    SALE ||--o{ PRODUCT : includes
    PRODUCT ||--o{ INVENTORY : has_stock

```