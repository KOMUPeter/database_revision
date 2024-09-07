- **Definition:** A relational database is a type of database that stores and provides access to data points that are related to one another. Data is stored in tables, which are made up of rows and columns.
  
- **Structure:**
  - **Tables:** The core component of a relational database. Each table represents an entity (e.g., Customers, Orders) and consists of rows and columns.
  - **Rows (Records):** A row in a table represents a single record or instance of an entity (e.g., a single customer).
  - **Columns (Fields):** A column represents a specific attribute of the entity (e.g., Customer Name, Order Date).

**Discussion/Activity:**
- Show a sample table and ask students to identify the rows, columns, and how data is stored in a relational format.

### 3.2 Relationships in Relational Databases

**Objective:** Learn how relationships are established between tables in a relational database.

**Content:**

- **One-to-One Relationship:** A relationship where a single record in one table corresponds to a single record in another table.
  
- **One-to-Many Relationship:** A single record in one table can be associated with multiple records in another table. This is the most common type of relationship in relational databases.
  
- **Many-to-Many Relationship:** Multiple records in one table are associated with multiple records in another table. This often requires a junction table to manage the relationships.

**Discussion/Activity:**
- Provide examples of each type of relationship and ask students to draw simple diagrams representing them.
- Discuss real-world examples, such as the relationship between Customers and Orders in an e-commerce database.

### 3.3 Primary Keys and Foreign Keys

**Objective:** Understand the roles of primary and foreign keys in ensuring data integrity.

**Content:**

- **Primary Key:** A column (or a set of columns) in a table that uniquely identifies each row in that table. It ensures that no duplicate records exist.
  
- **Foreign Key:** A column in one table that creates a relationship with the primary key in another table, establishing a link between the two tables.

