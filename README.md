# Spring Boot 3 + JPA (DSList Workshop)

This project is a hands-on workshop built with Spring Boot 3, Java 21, and JPA/Hibernate.  
It demonstrates how to build a RESTful API using modern Java and Spring technologies with a relational database.  
The system manages **games and game lists**, supporting custom ordering and SQL seed scripts.  

This project was made through Dev Superior intensive course  *"Intensivão Java Spring"* @acenelio (Github).  

---

## ✅ Features

- REST API for **Games** and **Game Lists**  
- Full CRUD operations on entities  
- DTO pattern to decouple domain and transport layers  
- Relational mapping with JPA / Hibernate  
- Custom native SQL queries  
- Database seeding with `import.sql`  
- Layered architecture (Controller, Service, Repository)  

---

## 🧰 Tech Stack

- Java 21 (compatible with Java 17+)  
- Spring Boot 3.x  
- Spring Web  
- Spring Data JPA  
- H2 Database (dev/test)  
- PostgreSQL (production)  
- Maven  

---

## 📁 Project Structure

```
project-root/
├── src/
│   ├── main/
│   │   ├── java/com.ranieri.dslist/
│   │   │   ├── DslistApplication.java   # Spring Boot entry point
│   │   │   ├── controllers/             # REST controllers
│   │   │   │   ├── GameController.java
│   │   │   │   └── GameListController.java
│   │   │   ├── dto/                     # Data Transfer Objects
│   │   │   │   ├── GameDTO.java
│   │   │   │   └── GameMinDTO.java
│   │   │   ├── entities/                # JPA Entities
│   │   │   │   ├── Game.java
│   │   │   │   └── GameList.java
│   │   │   ├── projections/             # Query projections
│   │   │   │   └── GameMinProjection.java
│   │   │   ├── repositories/            # JPA Repositories
│   │   │   │   ├── GameRepository.java
│   │   │   │   └── GameListRepository.java
│   │   │   └── services/                # Business logic
│   │   │       ├── GameService.java
│   │   │       └── GameListService.java
│   │   └── resources/
│   │       ├── application.properties   # Spring Boot config
│   │       └── import.sql               # Initial DB seed data
│   └── test/java/com.ranieri.dslist/
│       └── DslistApplicationTests.java  # Basic integration test
│
├── pom.xml   # Maven config
├── mvnw / mvnw.cmd  # Maven wrapper
└── README.md  # You're reading it!
```

---

## 🖥️ How to Run

### Prerequisites
- Java 21 (or Java 17+)  
- Maven installed (or use included wrapper)  
- PostgreSQL (if running in production mode)  

### Steps
Clone the project:
```bash
git clone https://github.com/your-username/dslist-springboot3.git
cd dslist-springboot3
```

Run with H2 (default dev profile):
```bash
./mvnw spring-boot:run
```

Or configure PostgreSQL in `application.properties`:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/dslist
spring.datasource.username=youruser
spring.datasource.password=yourpass
```

Then start:
```bash
./mvnw spring-boot:run
```

Access the API:
```
http://localhost:8080/games
http://localhost:8080/lists
```

---

## 🧪 Testing

The project includes a basic Spring Boot test class to ensure the application context loads.  

Run tests:
```bash
./mvnw test
```

---

## 🎯 Learning Objectives

- Model relationships in a relational DB using **JPA/Hibernate**  
- Use **DTOs** and **Projections** to optimize data transfer  
- Handle database seeding with SQL scripts  
- Organize a Spring Boot project using layered architecture  
- Perform custom SQL queries within Spring Data JPA  

---

## 📄 License

This project is intended for educational purposes only.  
You are free to fork, clone, and use it to study or as the base of your own experiments.  
