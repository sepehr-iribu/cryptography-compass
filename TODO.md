

## 1. Authenticated Encryption & MACs  
- AEAD modes (e.g. AES-GCM, ChaCha20-Poly1305) combine confidentiality + integrity in one operation.  
- Message Authentication Codes (HMAC is one, but also CMAC, GMAC).  

## 2. Randomness & CSPRNGs  
- Why high-quality entropy is the bedrock of all crypto.  
- Common CSPRNG designs (e.g. Fortuna, CTR-DRBG).  
- Hardware sources (RDRAND, TPM, HSMs).  

## 3. Elliptic-Curve Cryptography (ECC)  
- Curve families: secp256r1, Curve25519/Ed25519, Brainpool.  
- ECDH & ECIES for key exchange/encryption.  
- EdDSA for compact, fast signatures.  

## 4. Hybrid Encryption Schemes  
- How you combine RSA/KEM + AES-GCM (or Kyber + AES) to get both performance and security.  

## 5. Secret Sharing & MPC  
- Shamir’s Secret Sharing for splitting keys.  
- Multiparty Computation (MPC) basics.  

## 6. Certificate Management Enhancements  
- Certificate Transparency (CT) logs & monitoring.  
- OCSP Stapling and Certificate Pinning.  
- PKIX profiles (S/MIME, code signing).  

## 7. Side-Channel & Implementation Attacks  
- Timing, power analysis, fault injection.  
- Best practices to mitigate (constant-time code, blinding).  

## 8. Advanced Protocols & Use Cases  
- Secure messaging (Signal’s X3DH & Double Ratchet).  
- OAuth2/OpenID Connect (JWT in real-world APIs).  
- VPN/IPsec, SSH key formats, WireGuard.  

## 9. Zero-Knowledge Proofs & Homomorphic Encryption (Optional)  
- zk-SNARKs, zk-STARKs for privacy-preserving proofs.  
- Paillier, BGV for computation on encrypted data.  

---

Filling these in will ensure your repo covers both theory (goals and primitives) and real-world practice (protocols, attacks, mitigations).
