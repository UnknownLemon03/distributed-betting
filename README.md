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
- **Others**: Docker



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

### ⏱️ Auto Game Scheduling  
- Automatically schedules **matches** at regular intervals using Spring Boot Scheduled tasks.  
- Publishes MatchCreateEvent and MatchCompleteEvent to **Kafka** for downstream processing.

## HLD
<img width="1164" height="503" alt="image" src="https://github.com/user-attachments/assets/d36d0554-da7a-41b5-aa16-7550db9f9d4a" />


### Betting flow
<img width="1374" height="510" alt="image" src="https://github.com/user-attachments/assets/e355e055-97c7-4f6d-8386-136ae1abc079" />


### Bet Settlement
<img width="1374" height="441" alt="image" src="https://github.com/user-attachments/assets/a6f1ebb3-4d3a-4dc0-803d-ede1c578475b" />


### Creating Matches 
<img width="1431" height="466" alt="image" src="https://github.com/user-attachments/assets/0041d154-404e-4f23-9e71-046e414f9cfe" />



- **API Gateway** – Entry point for all requests  
- **Auth Service** – JWT-based login and user roles (via Keycloak)  
- **Wallet Service** – Manages user funds and ledger  
- **Stock-Service** – Core logic for live interaction  
- **Order-Book Service** – Go-based matching engine  
- **Kafka** – Event streaming & decoupling  
- **Saga Orchestration** – Ensures flow reliability via gRPC
- **Match service** - auto schedules matches certain intervals
   





