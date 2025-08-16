
---

# **Asymmetric Key Encryption**

---

## **1. Definition**

* A cryptographic technique where **two different keys** are used:

  * **Public Key (Kpub):** Used for **encryption** (shared openly).
  * **Private Key (Kpri):** Used for **decryption** (kept secret).
* Also called **Public-Key Cryptography**.

---

## **2. Working (Step-by-step)**

### **Encryption (Sender side)**

1. Sender takes **plaintext message (M)**.
2. Message is encrypted using **Receiver’s Public Key (Kpub)**.
3. Output → **Ciphertext (C)** (can only be decrypted by the matching private key).

### **Decryption (Receiver side)**

1. Receiver obtains **ciphertext (C)**.
2. Ciphertext is given to **decryption algorithm** with **Receiver’s Private Key (Kpri)**.
3. Output → **Original Plaintext (M)**.

👉 Key point: Even if public key is known, only the **private key** can decrypt.

---

## **3. Diagram (Exam-friendly)**

```
         Sender Side                               Receiver Side
  Plaintext (M)                                  Ciphertext (C)
       │                                               │
       ▼                                               ▼
 [Encryption Algo + Public Key (Kpub)]        [Decryption Algo + Private Key (Kpri)]
       │                                               │
       ▼                                               ▼
 Ciphertext (C) -------------------------------> Plaintext (M)
```

---

## **4. Example Algorithms**

* RSA, ECC, ElGamal

---

## **5. Application in Blockchain**

* **Wallets:** Public key → address, Private key → access.
* **Digital Signatures & Transaction Security** (only owner with private key can authorize).

---

✅ **Exam Tip Mnemonic:**
**“Asymmetric = A pair of keys: Public for Padlock, Private for Unlock.”**

---

