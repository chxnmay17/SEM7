
---

# **Digital Signature Algorithm (DSA)**

---

## **1. What is a Digital Signature?**

* A **digital signature** is a cryptographic technique used to:

  * Verify **authenticity** (sender identity).
  * Ensure **integrity** (data not altered).
  * Provide **non-repudiation** (sender cannot deny sending).
* Works on principles of **asymmetric key cryptography** and **hashing**.

---

## **2. Digital Signature Algorithm (DSA)**

* **Introduced**: 1991 by NIST (based on discrete logarithm problem).
* **Keys Used**:

  * **Private Key** → Used for signing (sender).
  * **Public Key** → Used for verification (receiver).

---

## **3. Working of DSA**

### **Step 1: Signing**

1. Message is hashed (e.g., SHA-256).
2. Hash + private key → signature generated.
3. Signature + message sent to receiver.

### **Step 2: Verification**

1. Receiver hashes the message.
2. Uses sender’s public key + signature to verify.
3. If match → message is authentic & untampered.

---

## **Diagram (Exam-friendly)**

```
Signing:                Verification:
Message → Hash → + Private Key       Message → Hash
             ↓ Signature                   ↓ Compare
         [Send Msg + Signature] → Receiver uses Public Key
```

---

## **4. Role in Blockchain**

* Ensures **secure transactions**.
* Prevents **forgery & double spending**.
* Used in Bitcoin/Ethereum → users sign transactions with their **private keys**, nodes verify with **public keys**.

---

## **5. Real-world Example**

* **Bitcoin**: Transactions signed using **ECDSA (Elliptic Curve Digital Signature Algorithm)**, a variant of DSA.

---

✅ **Exam Tip Mnemonic:**
**“DSA = Data Security Assured → Integrity, Authenticity, Non-repudiation.”**

---


