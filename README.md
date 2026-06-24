# Secure Cryptography API

A security-focused REST API built with FastAPI that provides cryptographic services including digital signatures, message encryption, integrity verification, and session-based authentication.

This project was developed as a final semester project for the Information Security and Cryptography course.

---

## Overview

Modern API-based systems require strong security mechanisms to ensure:

- Authentication
- Confidentiality
- Integrity
- Non-Repudiation

This project implements a centralized Security Service that acts as a Trusted Authority for secure communication between clients.

---

## Key Features

### Digital Signature (Ed25519)

- Public key management
- Signature generation
- Signature verification
- Non-repudiation support

### Encryption Services

#### AES-256 Encryption

- Symmetric encryption
- CFB mode
- High-performance data protection

#### RSA-2048 Encryption

- Public key cryptography
- Secure key exchange

#### Hybrid Encryption

- AES for message encryption
- RSA for AES key protection

### Integrity Verification

- SHA-256 Hashing
- Message integrity validation
- Tampering detection

### Session Authentication

- User registration
- User login
- Session token generation
- Protected endpoints
- Logout and token invalidation

### API Documentation

- Interactive Swagger UI
- OpenAPI specification

---

## Security Architecture

The system follows a Trusted Authority architecture where the FastAPI server acts as a centralized security service.

Client Responsibilities:

- Generate cryptographic keys
- Sign messages
- Encrypt data
- Calculate hashes

Server Responsibilities:

- Store public keys
- Verify signatures
- Validate integrity
- Manage sessions
- Provide encryption services

---

## API Endpoints

### Key Management

```http
POST /keys/store
POST /keys/store-multi
```

### Digital Signature

```http
POST /signature/verify
```

### Message Relay

```http
POST /message/relay
```

### Integrity Check

```http
POST /integrity/check
```

### Encryption

```http
POST /encrypt/aes
POST /encrypt/rsa
POST /encrypt/hybrid
```

### Authentication

```http
POST /auth/register
POST /auth/login
POST /auth/logout

GET  /auth/me
GET  /session/active
```

---

## Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Main Language |
| FastAPI | REST API Framework |
| Cryptography | Cryptographic Operations |
| Ed25519 | Digital Signature |
| AES-256 | Symmetric Encryption |
| RSA-2048 | Asymmetric Encryption |
| SHA-256 | Integrity Verification |
| Swagger UI | API Testing & Documentation |

---

## Installation

Clone repository:

```bash
git clone https://github.com/yourusername/secure-cryptography-api.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run server:

```bash
uvicorn app.main:app --reload
```

Open Swagger Documentation:

```text
http://localhost:8000/docs
```

---

## Security Concepts Implemented

- Authentication
- Confidentiality
- Integrity
- Non-Repudiation
- Public Key Infrastructure Concepts
- Session-Based Authentication
- Secure Message Transmission

---

## Future Improvements

- JWT Authentication
- OAuth2 Integration
- Database Persistence
- Role-Based Access Control (RBAC)
- End-to-End Encryption
- Docker Deployment
- Cloud Deployment

---

## Authors

- Umi Imroatus Sholekhah
- Cintiya Agustin Nareswari
- Fajar Syihabuddin

---

## Academic Project

This project was developed as part of the Information Security and Cryptography course at Universitas Negeri Surabaya.

The objective was to design and implement a secure API service integrating modern cryptographic techniques such as digital signatures, encryption, integrity verification, and authentication mechanisms into a single platform.
