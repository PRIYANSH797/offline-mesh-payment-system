# Offline Mesh Payment System

> Secure Offline Payment Processing System built using Java, Spring Boot, Spring Data JPA, REST APIs, and Hybrid Encryption (AES-GCM + RSA).

---

## 📖 Overview

Offline Mesh Payment System is a backend application that simulates secure offline digital payment processing for environments with limited or no internet connectivity.

The system focuses on secure transaction exchange, duplicate payment prevention using idempotency, and reliable transaction settlement using Spring Boot and Spring Data JPA.

---

## 🚀 Features

- Secure Offline Payment Processing
- RESTful APIs
- Hybrid Encryption (AES-GCM + RSA)
- Idempotency to prevent duplicate payments
- Transaction Management
- Payment Settlement
- MySQL Database Integration
- Layered Spring Boot Architecture
- Exception Handling
- Secure API Design

---

## 🛠 Tech Stack

- Java
- Spring Boot
- Spring Data JPA
- REST APIs
- MySQL
- Maven
- AES-GCM
- RSA
- Hibernate

---

## 🏗 System Architecture

```
          Sender Device
                │
                │
      Generate Payment Request
                │
                ▼
      AES-GCM Encrypt Payload
                │
                ▼
     RSA Encrypt AES Secret Key
                │
                ▼
      Offline Transfer (Mesh)
                │
                ▼
        Receiver Device
                │
                ▼
      Decrypt using RSA
                │
                ▼
      Decrypt using AES-GCM
                │
                ▼
      Validate Transaction
                │
                ▼
      Idempotency Check
                │
                ▼
      Payment Settlement
                │
                ▼
         Store in MySQL
```

---

## 📂 Project Structure

```
src
 ├── controller
 ├── service
 ├── repository
 ├── model
 ├── dto
 ├── config
 ├── security
 ├── exception
 └── util
```

---

## 🔐 Security

The project implements Hybrid Encryption to provide confidentiality and secure key exchange.

### AES-GCM

- Encrypts transaction payload
- Provides confidentiality
- Ensures integrity using authentication tags

### RSA

- Encrypts AES secret key
- Enables secure key exchange

---

## 🔄 Payment Flow

1. User initiates payment.

2. Payment payload is encrypted using AES-GCM.

3. AES key is encrypted using RSA.

4. Receiver decrypts AES key.

5. Receiver decrypts payment payload.

6. Idempotency mechanism checks duplicate transactions.

7. Valid payment is settled.

8. Transaction is stored in MySQL database.

---

## 🧠 Key Concepts Demonstrated

- Spring Boot
- REST APIs
- Spring Data JPA
- MySQL
- Hybrid Encryption
- AES-GCM
- RSA
- Idempotency
- Transaction Management
- Backend Development

---

## 📸 API Endpoints

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /payments | Initiate Payment |
| GET | /payments/{id} | Fetch Payment |
| GET | /payments | List Transactions |

---

## 💡 Future Improvements

- QR Code Payments
- Bluetooth Mesh Communication
- NFC Support
- Device Authentication
- Digital Signature Verification
- Redis-based Idempotency
- Docker Deployment
- Kubernetes Support

---

## 🎯 Learning Outcomes

This project strengthened practical understanding of:

- Spring Boot
- Backend Development
- Secure Payment Systems
- REST API Design
- Database Management
- Hybrid Encryption
- Transaction Management
- Software Architecture

---

## 👨‍💻 Author

**Priyansh Srivastava**

- Java Backend Developer
- Spring Boot Developer
- Problem Solver (650+ LeetCode Problems)
