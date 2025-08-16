
---

# **Symmetric Key Encryption**

---

## **1. Definition**

* A method of encryption where **same secret key (K)** is used for both **encryption** and **decryption**.
* Provides **confidentiality** but needs secure **key distribution**.

---

## **2. Working (Step-by-step)**

### **Encryption (Sender side)**

1. Sender takes **plaintext message (M)**.
2. Message is given to **encryption algorithm** along with secret key `K`.
3. Output → **Ciphertext (C)** (unreadable to unauthorized users).

### **Decryption (Receiver side)**

1. Receiver obtains **ciphertext (C)**.
2. Ciphertext is input to **decryption algorithm** with the **same key K**.
3. Output → **Original Plaintext (M)**.

👉 Key point: **Both parties must already share the same key securely**.

---

## **3. Diagram (Exam-friendly)**

```
         Sender Side                          Receiver Side
  Plaintext (M)                              Ciphertext (C)
       │                                          │
       ▼                                          ▼
 [Encryption Algo + Key K]                 [Decryption Algo + Key K]
       │                                          │
       ▼                                          ▼
 Ciphertext (C) -----------------------------> Plaintext (M)
```

---

## **4. Example Algorithms**

* DES, AES, RC4

---

## **5. Application in Blockchain**

* Used for **fast encryption of stored wallet files, off-chain data**.
* Asymmetric cryptography is preferred for **transactions**, but symmetric methods are useful for **data protection**.

---

✅ **Exam Tip Mnemonic:**
**“Symmetric = Same key for Send & Secure.”**

---

