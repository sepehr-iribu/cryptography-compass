#  Digital Signature Algorithms: 
##  Overview

| **Algorithm** | **Full Name**                          | **Standard** | **Underlying Crypto**    | **Hash Function** |
|---------------|----------------------------------------|--------------|---------------------------|-------------------|
| RS256         | RSASSA-PKCS1-v1_5 with SHA-256         | PKCS #1 v1.5 | RSA (modular exponentiation) | SHA-256           |
| PS256         | RSASSA-PSS with SHA-256                | PKCS #1 v2.1 | RSA (modular exponentiation) | SHA-256           |
| ECDSA         | Elliptic Curve Digital Signature Algo  | FIPS 186-4   | ECC (Elliptic Curves)     | SHA-256 (or other)|

---

##  Architecture and Properties

### 1. RS256 (RSA with PKCS#1 v1.5 padding)
- **Signature** = `S = m^d mod n` (with padding)
- **Verification** = `m' = S^e mod n`
- Simple but **older** scheme, susceptible to **padding oracle attacks** if not carefully implemented.
- Widely used in JWTs and TLS but **not recommended** for new systems.

### 2. PS256 (RSA-PSS)
- Uses **Probabilistic Signature Scheme (PSS)** with salt to prevent padding attacks.
- Recommended RSA-based signature scheme today.
- **Still not quantum-resistant.**

### 3. ECDSA
- Based on **elliptic curve math** (hard to reverse discrete logarithm over EC groups).
- Much **smaller key sizes** for equivalent security.
- Requires **secure random number generation** – vulnerable if nonce reuse happens.
- Common in blockchain, TLS, SSH, and JWTs.

---

##  Cryptographic Architecture Comparison

| **Feature**   | **RSA / DH**      | **ECC**             | **Kyber (Post-Quantum)** |
|---------------|-------------------|----------------------|---------------------------|
| Based on      | Number theory      | Elliptic curves      | Lattices (LWE, MLWE)      |
| Quantum safe  |  No              |  No                |  Yes                    |
| Key sizes     |  Huge (2048+ bits)|  Medium (256–521 bits) |  Small (~800–1500 bytes) |
| Performance   |  Slow            |  Fast              |  Very fast              |
| Used in TLS?  |  Yes             |  Yes               |  Yes (in hybrid TLS)    |
| JWT Signing   |  RS256, PS256    |  ECDSA             |  (Not supported natively) |

---

##  Summary

- **RS256** is the simplest but least secure of the three — avoid for future-proof applications.
- **PS256** is a modern RSA signature with stronger security guarantees.
- **ECDSA** offers fast, compact signatures but must handle randomness securely.
- **Kyber**, while not a signature scheme, is used in **key exchange (KEM)** — part of **post-quantum cryptography**. Signature equivalents for PQC include **Dilithium** and **SPHINCS+**.

---
