<h1 align="center">🌟 Midas Core Project 🌟</h1>  

<p align="center">
   <b>Integration of Kafka, H2 Database, REST API & Incentives into Midas Core (Spring Boot)</b>
</p>

<p align="center">
   <!-- Tech Badges -->
   <img src="https://img.shields.io/badge/Java-17-blue?style=for-the-badge&logo=java" />
   <img src="https://img.shields.io/badge/Spring_Boot-3.2.5-brightgreen?style=for-the-badge&logo=springboot" />
   <img src="https://img.shields.io/badge/Apache-Kafka-black?style=for-the-badge&logo=apachekafka" />
   <img src="https://img.shields.io/badge/H2-Database-yellow?style=for-the-badge&logo=databricks" />
   <img src="https://img.shields.io/badge/REST-API-orange?style=for-the-badge&logo=fastapi" />
   <img src="https://img.shields.io/badge/Maven-Build-red?style=for-the-badge&logo=apachemaven" />
</p>

---

## 📖 Project Overview  
This project implements **Midas Core**, a high-stakes financial transaction system.  
It integrates multiple external systems (**Kafka**, **H2 Database**, **REST APIs**) and processes transactions with incentives.  

The work was completed in **5 incremental tasks**, each building upon the previous.  

---

## ✅ Task 1: Environment Setup & Dependencies  
- Forked & cloned the scaffold repo.  
- Configured **Java 17** & Spring Boot.  
- Added the following dependencies:
  - `spring-boot-starter-data-jpa`  
  - `spring-boot-starter-web`  
  - `spring-kafka`  
  - `h2`  
  - `spring-boot-starter-test`  
  - `spring-kafka-test`  
  - `testcontainers-kafka`  

### 🔹 Test Output
--- BEGIN TASK ONE OUTPUT ---
Task One Tests Passed!
--- END TASK ONE OUTPUT ---

---

## ✅ Task 2: Kafka Integration  
- Implemented a **Kafka Listener** to receive transactions asynchronously.  
- Configured it to consume from the topic defined in `application.yml`.  
- Successfully deserialized messages into `Transaction` objects.  

### 🔹 First 4 Transaction Amounts
122.86, 42.87, 161.79, 22.22

---

## ✅ Task 3: H2 Database Integration  
- Integrated **H2 in-memory database** via Spring Data JPA.  
- Implemented `TransactionRecord` entity.  
- Validated transactions before persisting:
  - Valid sender/recipient  
  - Sufficient sender balance  
- Adjusted sender & recipient balances accordingly.  

### 🔹 Debug Result
Balance of waldorf after all transactions: 1203

---

## ✅ Task 4: Incentive API Integration  
- Connected to the external **Incentive REST API** at `http://localhost:8080/incentive`.  
- Posted valid transactions to the API using `RestTemplate`.  
- Applied incentive amounts:
  - Added to recipient balance  
  - Not deducted from sender  

### 🔹 Debug Result
Balance of wilbur after all transactions: 1849

---

## ✅ Task 5: Balance REST API  
- Added a **REST Controller** with endpoint:  
GET /balance?userId={id}
- Returns a JSON `Balance` object.  
- If user doesn’t exist → returns 0.  
- Runs on port **33400**.  

### 🔹 Test Output
--- BEGIN TASK FIVE OUTPUT ---
Task Five Tests Passed!
--- END TASK FIVE OUTPUT ---

---

## 🏆 Certificate  
At the end of this project, a certificate of completion was earned.  

<p align="center">
  <img src="src/image/FORAGE JP MORGAN CHASE & CO SOFTWARE ENGINEERING JOB SIMULATION_page-0001.jpg" alt="Certificate" width="600"/>
</p>

---

## 🎨 Tech Stack  
- **Java 17**  
- **Spring Boot**  
- **Apache Kafka**  
- **H2 Database**  
- **Spring Data JPA**  
- **REST APIs**  

---

## 🚀 How to Run  
1. Clone this repo  
2. Start Incentive API jar (`services/incentive-api.jar`)  
3. Run the Spring Boot application  
4. Use `/balance` endpoint to query balances  

---

<p align="center">✨ Built with dedication during J.P. Morgan’s Forage Program ✨</p>

