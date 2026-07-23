# 🛒 InfoStore API

<div align="center">

  ![Java](https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
  ![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.2.0-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
  ![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-Supported-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
  ![Hibernate](https://img.shields.io/badge/Hibernate-ORM-59666C?style=for-the-badge&logo=hibernate&logoColor=white)

  <p align="center">
    A robust RESTful API built with <b>Spring Boot</b> and <b>MySQL</b> for managing customers and orders, featuring full CRUD operations, relational cascade deletion, and Bean Validation.
  </p>

</div>

---

## 📌 Project Overview

**InfoStore** is a back-end RESTful service developed as part of the **Generation Brasil Bootcamp (Java Full Stack)**. It models a retail management system where customers can place multiple orders.

### 🌟 Key Features
* **Full CRUD Operations:** Endpoints for creating, reading, updating, and deleting Customers and Orders.
* **Relational Database Mapping:** `1:N` (One-to-Many) entity relationship using Spring Data JPA.
* **Cascade Deletion:** Deleting a customer automatically removes all associated orders (`CascadeType.REMOVE`).
* **Input Validation:** Data integrity ensured with Bean Validation annotations (`@NotBlank`, `@Email`, `@Positive`, `@Size`).
* **Custom Search Queries:** Case-insensitive search methods using JPA Query Keywords (`ContainingIgnoreCase`).

---

## 🗄️ Database Architecture & Entity Relationship

```text
+-----------------------+              +-----------------------+
|      tb_clientes      |              |      tb_pedidos       |
+-----------------------+              +-----------------------+
| PK  id        (Long)  | 1          N | PK  id        (Long)  |
|     nome      (String)| <----------> |     produto   (String)|
|     email     (String)|              |     valor     (BigDec)|
+-----------------------+              |     data      (LDT)   |
                                       | FK  cliente_id(Long)  |
                     +-----------------------+





