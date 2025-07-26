#  Distributed Betting 
Distributed Betting is a low-latency, microservices-based trading and betting platform that allows users to buy and sell stocks or bet on live matches with real-time updates. Built using high-performance gRPC, Kafka, and Saga pattern, this system is designed to ensure scalability, resilience, and event-driven orchestration across services.
The platform focuses on speed, consistency, and distributed fault tolerance, making it ideal for real-time financial or match-based prediction applications.


## Demo
project is not hosted

## 🧰 Tech Stack

- **Languages**: Go, Java
- **Backend Frameworks**: Spring Boot (Java), gRPC (Java + Go)  
- **Frontend**: Next.js (in progress)  
- **Message Broker**: Apache Kafka  
- **Patterns**: Saga Pattern
- **Databases**: PostgreSQL
- **API Protocol**: gRPC,HTTP
- **Authentication**: JWT (Keyclock)
- **Others**: Docker, Kubernetes (planned)



## Features

### ✅ Real-Time Betting & Trading
- Place **bets** or **buy/sell stocks** with live updates.
- Built for **concurrent, low-latency operations** using gRPC.

### 🧩 Microservices Architecture
- Independent services for wallet, user, betting, market, and more.
- Communicate via **Kafka** and **gRPC** for performance and resilience.

### 🔁 Saga Pattern
- Ensures **distributed transaction consistency**.
- Example flow:
  - Wallet deduction → Bet placed → Event update → Rollback on failure

### 💰 Wallet & Transactions
- Fully secure and isolated **wallet service**.
- Supports deposits, withdrawals.
  
### 🧮 Custom Order Book Engine (Go)
- Supports **limit orders**, **market orders**, and **order matching** logic.
- Blazing-fast custom order book built in Go, designed for high concurrency using goroutines with deadlock-safe matching logic.
- Uses **Go routines** for high concurrency and performance.
- Handles concurrency and fairness with high efficiency.

### ⚡ Low-Latency Market Order Placement
- Orders are placed and matched within milliseconds using gRPC.
- Designed to simulate real-world exchange performance.

## HLD
<img width="1150" height="812" alt="image" src="https://github.com/user-attachments/assets/82240b77-df8d-43bc-8c01-e650f33780cb" />

### Betting flow
<img width="1644" height="620" alt="image" src="https://github.com/user-attachments/assets/7e7f47b1-2c81-4c39-b23c-33840e049fee" />

### Saga flow 
<img width="1644" height="620" alt="image" src="https://github.com/user-attachments/assets/8cf6f7f4-f0e1-4a1b-882e-30070284ee37" />

- **API Gateway** – Entry point for all requests  
- **Auth Service** – JWT-based login and user roles (via Keycloak)  
- **Wallet Service** – Manages user funds and ledger  
- **Stock-Service** – Core logic for live interaction  
- **Order-Book Service** – Go-based matching engine  
- **Kafka** – Event streaming & decoupling  
- **Saga Orchestration** – Ensures flow reliability via gRPC
   





