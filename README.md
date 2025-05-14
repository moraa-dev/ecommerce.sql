# ecommerce.sql

# 🛒 E-Commerce Database Schema

This project contains the SQL schema for a simplified e-commerce platform. The schema supports product listings, variations, attributes, and inventory management while following normalization principles and a scalable structure.

## 📁 Files
- `ecommerce.sql`: Contains the full SQL schema for setting up the e-commerce database, including all tables, constraints, and relationships.

---

## 🧱 Schema Overview

### 🔷 Core Tables

- **`brand`**: Stores product brand names.
- **`product_category`**: Categorizes products (e.g., clothing, electronics).
- **`product`**: Main table containing general product information such as name, brand, base price, and description.

### 🧾 Product Variations

- **`size_category`**: Groups sizes into categories (e.g., shoe sizes, clothing sizes).
- **`size_option`**: Stores specific sizes (e.g., S, M, L, 42).
- **`color`**: Manages available color options.
- **`product_item`**: Represents a purchasable SKU with a unique color and size combination.
- **`product_variation`**: Maps a product to its variations (color + size).

### 🎨 Product Presentation

- **`product_image`**: Stores image URLs for product galleries.

### 📋 Product Attributes

- **`attribute_category`**: Groups attributes into types (e.g., physical, technical).
- **`attribute_type`**: Describes the type and data format of an attribute (text, number, boolean).
- **`product_attribute`**: Stores custom product characteristics like material, weight, etc.

---

## 🔗 Relationships

- Products are linked to **brands** and **categories**.
- A **product** can have multiple **product_items** based on size and color.
- Each **product_item** has a unique SKU.
- **product_attributes** and **images** enrich product listings.

---

## 🧪 Testing the Schema

To test:
1. Import `ecommerce.sql` into MySQL Workbench or a similar tool.
2. Use `INSERT` statements to add sample data.
3. Query `product_item` to see SKU-level listings.

---

## 📌 Notes

- The schema is designed for scalability and real-world use.
- Foreign keys ensure referential integrity.
- ENUMs are used for controlled attribute value types.

---

## 📄 License

This project is open for educational and demonstration purposes. Feel free to build upon it.
