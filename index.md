# DBMS

![alt text](images/image.png)

<div style="position:relative;width:100%;padding-bottom:56.25%;height:0;">
  <iframe
    src="https://www.youtube.com/embed/2lN_zjaOCy0?si=1BNWdKFdSOTnoamJ"
    title="YouTube video player"
    style="position:absolute;top:0;left:0;width:100%;height:100%;border:0;"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen>
  </iframe>
</div>

## Basic DBMS Interview Questions

### 1. What is meant by DBMS and what is its utility? Explain RDBMS with examples.

**DBMS (Database Management System)**
*   **Definition:** A set of applications or programs that enable users to create and maintain a database.
*   **Utility:**
    *   Provides a tool or interface for performing various operations such as inserting, deleting, updating, etc., into a database.
    *   Enables the storage of data more compactly and securely compared to a file-based system.
    *   Helps users overcome problems like **data inconsistency** and **data redundancy** in a database.
    *   Makes using a database more convenient and organized.
*   **Examples:** File systems, XML, Windows Registry, etc.

**RDBMS (Relational Database Management System)**
*   **Definition:** Introduced in the 1970s to access and store data more efficiently than DBMS.
*   **Structure:** Stores data in the form of **tables** (rows and columns) compared to DBMS which stores data as files.
*   **Utility:** Storing data as rows and columns makes it easier to locate specific values in the database and makes it more efficient compared to DBMS.
*   **Examples:** MySQL, Oracle DB, etc.

### 2. What is meant by a database?

*   **Definition:** An organized, consistent, and logical collection of data that can easily be updated, accessed, and managed.
*   **Content:** Mostly contains sets of tables or objects.
    *   **Object:** Anything created using the `create` command is a database object.
    *   **Records and Fields:** Tables consist of these.
*   **Tuple/Row:** Represents a single entry in a table.
*   **Attribute/Column:** Represents the basic units of data storage, containing information about a particular aspect of the table.
*   **Extraction:** DBMS extracts data from a database in the form of queries given by the user.

### 3. Mention the issues with traditional file-based systems that make DBMS a better choice?

*   **Absence of Indexing:** Leaves the only option of scanning the full page, making access to content tedious and super slow.
*   **Redundancy and Inconsistency:** Files have many duplicate and redundant data; changing one makes all of them inconsistent.
*   **Data Access:** Accessing data is harder because data is unorganized.
*   **Lack of Concurrency Control:** Leads to one operation locking the entire page, whereas DBMS allows multiple operations on a single file simultaneously.
*   **Other Issues:**
    *   Integrity check issues
    *   Data isolation issues
    *   Atomicity issues
    *   Security issues

### 4. Explain a few advantages of a DBMS.

*   **Data Sharing:** Data from a single database can be simultaneously shared by multiple users. This enables end-users to react to changes quickly in the database environment.
*   **Integrity Constraints:** The existence of these constraints allows storing data in an organized and refined manner.
*   **Controlling Redundancy:** Eliminates redundancy by providing a mechanism that integrates all data in a single database.
*   **Data Independence:** Allows changing the data structure without altering the composition of any executing application programs.
*   **Backup and Recovery:** Can be configured to automatically create a backup of data and restore it whenever required.
*   **Data Security:** Provides necessary tools to make storage and transfer reliable and secure.
    *   **Authentication:** The process of giving restricted access to a user.
    *   **Encryption:** Encrypting sensitive data such as OTP, credit card information, etc.

### 5. Explain different languages present in DBMS.

**DDL (Data Definition Language)**
*   Contains commands required to define the database.
*   **Examples:**
    ```sql
    CREATE, ALTER, DROP, TRUNCATE, RENAME
    ```

**DML (Data Manipulation Language)**
*   Contains commands required to manipulate the data present in the database.
*   **Examples:**
    ```sql
    SELECT, UPDATE, INSERT, DELETE
    ```

**DCL (Data Control Language)**
*   Contains commands required to deal with user permissions and controls of the database system.
*   **Examples:**
    ```sql
    GRANT, REVOKE
    ```

**TCL (Transaction Control Language)**
*   Contains commands required to deal with the transaction of the database.
*   **Examples:**
    ```sql
    COMMIT, ROLLBACK, SAVEPOINT
    ```

### 6. What is meant by ACID properties in DBMS?

ACID properties ensure a safe and secure way of sharing data among multiple users.

*   **A - Atomicity:**
    *   Reflects the concept of either executing the **whole query** or executing **nothing at all**.
    *   If an update occurs, it should either be reflected in the whole database or not reflected at all.
*   **C - Consistency:**
    *   Ensures that data remains consistent before and after a transaction.
*   **I - Isolation:**
    *   Ensures each transaction occurs independently of others.
    *   The state of an ongoing transaction does not affect the state of another ongoing transaction.
*   **D - Durability:**
    *   Ensures data is not lost in cases of system failure or restart.
    *   Data is present in the same state as it was before the failure/restart.

### 7. Are NULL values in a database the same as that of blank space or zero?

*   **No**, a **NULL** value is very different from zero and blank space.
*   **NULL:** Represents a value that is assigned, unknown, unavailable, or not applicable.
*   **Blank Space:** Represents a character.
*   **Zero:** Represents a number.
*   **Example:** A NULL value in "number_of_courses" means the value is unknown, whereas 0 means the student has not taken any courses.

---

## Intermediate DBMS Interview Questions

### 8. What is meant by Data Warehousing?

*   **Definition:** The process of collecting, extracting, transforming, and loading data from multiple sources and storing them into one database.
*   **Function:**
    *   Acts as a central repository where data flows from transactional systems and other relational databases.
    *   Used for data analytics.
    *   Comprises a wide variety of an organization’s historical data.
    *   Supports the decision-making process in an organization.

### 9. Explain different levels of data abstraction in a DBMS.

Data abstraction is the process of hiding irrelevant details from users. It is divided into 3 levels:

1.  **Physical Level:**
    *   The lowest level, managed by DBMS.
    *   Consists of data storage descriptions.
    *   Details are typically hidden from system admins, developers, and users.
2.  **Conceptual or Logical Level:**
    *   Level on which developers and system admins work.
    *   Determines **what** data is stored and the **relationships** between data points.
3.  **External or View Level:**
    *   Describes only part of the database.
    *   Hides details of table schema and physical storage from users.
    *   **Example:** The result of a query is View level data abstraction. A **view** is a virtual table created by selecting fields from one or more tables.

### 10. What is meant by an entity-relationship (E-R) model? Explain the terms Entity, Entity Type, and Entity Set in DBMS.

*   **E-R Model:** A diagrammatic approach to database design where real-world objects are represented as entities and relationships between them are mentioned.

**Terms:**
*   **Entity:** A real-world object having attributes that represent characteristics of that particular object.
    *   *Example:* A student, an employee, or a teacher.
*   **Entity Type:** A collection of entities that have the same attributes.
    *   One or more related tables in a database represent an entity type.
    *   Attributes uniquely identify the entity.
    *   *Example:* A student entity type has attributes like `student_id`, `student_name`, etc.
*   **Entity Set:** A set of **all** the entities present in a specific entity type in a database.
    *   *Example:* A set of all students, employees, teachers, etc.

### 11. Explain different types of relationships amongst tables in a DBMS.

*   **One to One Relationship:** Applied when a particular row in table X is linked to a **singular** row in table Y.
*   **One to Many Relationship:** Applied when a **single** row in table X is related to **many** rows in table Y.
*   **Many to Many Relationship:** Applied when **multiple** rows in table X can be linked to **multiple** rows in table Y.
*   **Self Referencing Relationship:** Applied when a particular row in table X is associated with the **same** table.

### 12. Explain the difference between intension and extension in a database.

*   **Intension (Database Schema):**
    *   Used to define the description of the database.
    *   Specified during the design of the database.
    *   Mostly remains unchanged.
*   **Extension (Snapshot):**
    *   The measure of the number of tuples present in the database at any given point in time.
    *   Value keeps changing as tuples are created, updated, or destroyed.

### 13. Explain the difference between the DELETE and TRUNCATE command in a DBMS.

**DELETE Command**
*   Needed to delete rows from a table based on the condition provided by the `WHERE` clause.
*   Deletes only rows specified by the `WHERE` clause.
*   Can be rolled back if required.
*   Maintains a log to lock the row of the table before deleting it; hence, it is **slow**.

**TRUNCATE Command**
*   Needed to remove complete data from a table.
*   Like a DELETE command with **no** `WHERE` clause.
*   Removes complete data from a table.
*   Can be rolled back even if required.
*   Does **not** maintain a log and deletes the whole table at once; hence, it is **fast**.

### 14. What is a lock? Explain the major difference between a shared lock and an exclusive lock during a transaction in a database.

*   **Lock:** A mechanism to protect a shared piece of data from getting updated by two or more database users at the same time. When a single user/session acquires a lock, no other user/session can modify that data until the lock is released.

**Shared Lock**
*   Required for **reading** a data item.
*   Many transactions may hold a lock on the same data item.
*   Multiple transactions are **allowed** to read data items.

**Exclusive Lock**
*   Required for any transaction about to perform a **write** operation.
*   Does **not** allow more than one transaction.
*   Prevents inconsistency in the database.

### 15. What is meant by normalization and denormalization?

*   **Normalization:**
    *   A process of reducing redundancy by organizing data into multiple tables.
    *   Leads to better usage of disk spaces.
    *   Makes it easier to maintain database integrity.
*   **Denormalization:**
    *   The reverse process of normalization.
    *   Combines tables which have been normalized into a single table.
    *   Makes data retrieval **faster**.
    *   **JOIN** operation allows creating a denormalized form by reversing normalization.

---

## Advanced DBMS Interview Questions

### 16. Explain different types of Normalization forms in a DBMS.

**1. First Normal Form (1NF)**
*   Simplest type. Conditions:
    *   Every column must have a **single value** and should be **atomic**.
    *   **Duplicate columns** from the same table should be removed.
    *   Separate tables should be created for each group of related data.
    *   Each row should be identified with a **unique column**.

**2. Second Normal Form (2NF)**
*   Conditions:
    *   Table must be in **1NF**.
    *   Every **non-prime attribute** should be **fully functionally dependent** on the primary key.
    *   *Explanation:* Every non-key attribute must depend on the primary key such that if any key element is deleted, the non-key element will be saved.

**3. Third Normal Form (3NF)**
*   Conditions:
    *   Table must be in **2NF**.
    *   There is **no transitive functional dependency** of one attribute on any attribute in the same table.

**4. Boyce-Codd Normal Form (BCNF) / 3.5NF**
*   Advanced form of 3NF. Conditions:
    *   Table must be in **3NF**.
    *   For every functional dependency `A -> B`, **A** should be the **super key** of the table.
    *   *Implication:* A can't be a non-prime attribute if B is a prime attribute.

### 17. Explain different types of keys in a database.

**1. Candidate Key**
*   A set of properties that can uniquely identify a table.
*   Each table may have multiple candidate keys.
*   One key amongst them is chosen as the primary key.
*   *Example:* `studentId` and `firstName` can both be Candidate Keys if they uniquely identify every tuple.

**2. Super Key**
*   A set of attributes that can uniquely identify a tuple.
*   Candidate key and primary key are **subsets** of the super key (the super key is their superset).

**3. Primary Key**
*   A set of attributes used to uniquely identify every tuple.
*   Chosen from the candidate keys.
*   Does **not** allow NULL values.
*   *Example:* `studentId` chosen over `firstName` for the student table.

**4. Unique Key**
*   Similar to primary key but **allows NULL values** in the column.
*   Essentially primary keys with NULL values.

**5. Alternate Key**
*   All candidate keys **not** chosen as primary keys.
*   *Example:* If `studentId` is Primary, `firstName` and `lastname` are alternate keys.

**6. Foreign Key**
*   An attribute that can only take values present in one table common to the attribute present in another table.
*   *Example:* `courseId` in the Student table is a foreign key to the Course table.

**7. Composite Key**
*   A combination of **two or more columns** that can uniquely identify each tuple in a table.
*   *Example:* Grouping `studentId` and `firstname`.

### 18. Explain the difference between a 2-tier and 3-tier architecture in a DBMS.

**2-Tier Architecture**
*   **Client-Server architecture.**
*   Applications at the client end **directly communicate** with the database at the server end.
*   **No middleware** involved.
*   **Examples:** Contact Management System created using MS-Access, Railway Reservation System.

**3-Tier Architecture**
*   Contains another layer (**Middleware**) between the client and the server.
*   Provides **GUI** to users.
*   Makes the system much more secure and accessible.
*   **Flow:** Client Application <-> Server Application <-> Database System.
*   **Examples:** Designing registration forms (text box, label, button), large websites on the Internet.