# ERD (Entity-Relationship Diagram)

## What is an ERD?

An Entity-Relationship Diagram (ERD) is a visual representation used to model the structure of a database. It shows entities within a system, the attributes of those entities, and the relationships between the entities. ERDs are essential for designing and understanding database structures and are used to create a blueprint for database development.

## Components of an ERD

### Entities
- **Definition:** Entities represent objects or concepts within the system that have data stored about them.
- **Notation:** Entities are typically depicted as rectangles.
- **Example:** In a library system, entities might include `Book`, `Author`, and `Borrower`.

### Attributes
- **Definition:** Attributes are properties or characteristics of entities.
- **Notation:** Attributes are usually shown as ovals connected to their respective entities.
- **Example:** The `Book` entity might have attributes like `Book_ID`, `Title`, `Publication_Date`.

### Relationships
- **Definition:** Relationships describe how entities are related to each other.
- **Notation:** Relationships are represented as diamonds connected to the entities involved.
- **Example:** In a library system, the relationship might be `Written_By` between `Book` and `Author`.

### Cardinality
- **Definition:** Cardinality defines the number of instances of one entity that can or must be associated with each instance of another entity.
- **Types:** Common cardinalities include:
  - **One-to-One (1:1):** Each instance of Entity A is related to one and only one instance of Entity B.
  - **One-to-Many (1:N):** Each instance of Entity A can be related to multiple instances of Entity B.
  - **Many-to-Many (M:N):** Multiple instances of Entity A can be related to multiple instances of Entity B.

### Primary Key
- **Definition:** A primary key is a unique identifier for each instance of an entity.
- **Notation:** Typically underlined in the entity’s attribute list.
- **Example:** `Book_ID` might be the primary key for the `Book` entity.

### Foreign Key
- **Definition:** A foreign key is an attribute that creates a relationship between two entities by referencing the primary key of another entity.
- **Notation:** Shown with a line connecting to the primary key of the related entity.

## How to Create an ERD

1. **Identify Entities:** Determine the key objects or concepts that need to be represented in the database.
2. **Identify Relationships:** Define how the entities are related and the nature of these relationships (e.g., one-to-one, one-to-many, many-to-many).
3. **Define Attributes:** List the attributes for each entity and specify the primary key.
4. **Establish Cardinality:** Determine the number of instances that can be associated between entities.
5. **Draw the ERD:** Use appropriate notation to create a diagram with entities, relationships, and attributes. Connect the entities with relationships and specify cardinality.

## Example ERD Components

### Example: Library System

- **Entities:** `Book`, `Author`, `Borrower`
- **Relationships:** 
  - `Book` is written by `Author` (Many-to-One)
  - `Borrower` borrows `Book` (Many-to-Many, typically requiring a junction table like `Loan`)

### Example ERD Diagram

```plaintext
+-----------+          +-----------+
|  Book     |          |  Author   |
+-----------+          +-----------+
| Book_ID   |          | Author_ID |
| Title     |          | Name      |
| Pub_Date  |          +-----------+
+-----------+          |
       |               |
       |  Written_By   |
       |               |
       v               v
+-----------+          +-----------+
| Borrower  |          |  Loan     |
+-----------+          +-----------+
| Borrower_ID|         | Book_ID   |
| Name      |          | Borrower_ID|
+-----------+          | Date      |
                       +-----------+
