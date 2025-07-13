![Alt Text](https://miro.medium.com/v2/resize:fit:4800/format:webp/0*-q0OB65GCekDIm-6.png)

## 1. Diffie–Hellman Key Exchange (DH)

###  What is it?
Diffie–Hellman (often just called Hellman) is a **key exchange protocol**. It allows two parties to agree on a shared secret over an insecure channel.
![ECDH](https://open.oregonstate.education/app/uploads/sites/137/2021/02/diffie-hellman-concept-a.gif)

###  How it works (Simplified):
1. Both parties agree on:
   - A large prime number `p`
   - A base `g` (a primitive root modulo `p`)
2. Alice picks a private number `a`, computes `A = g^a mod p`, and sends `A` to Bob.
3. Bob picks a private number `b`, computes `B = g^b mod p`, and sends `B` to Alice.
4. Alice computes `s = B^a mod p`
5. Bob computes `s = A^b mod p`
Both arrive at the same **shared key `s`**, which can now be used for encryption.
- note :
mod stands for modulo, and it represents a remainder after division.

###  Limitations:
- **Not secure against quantum attacks** (Shor’s algorithm can break it).
- Used in many protocols today (e.g., TLS, SSH), but being phased out in favor of quantum-safe alternatives.
