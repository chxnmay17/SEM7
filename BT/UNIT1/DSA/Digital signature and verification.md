

---

# **Digital Signature & Verification in DSA**

---

## **1. Introduction**

* A **Digital Signature** is a cryptographic technique that ensures:

  * **Authenticity** (proves sender identity)
  * **Integrity** (data not modified)
  * **Non-repudiation** (sender cannot deny sending).
* **DSA (Digital Signature Algorithm)** uses **private key** for signing and **public key** for verification.

---

## **2. Steps in Digital Signature (Signing Process)**

1. Sender chooses a message `M`.
2. Message is hashed (e.g., using **SHA-256**).
3. Using **private key (x)** and random number `k`, signature values `(r, s)` are generated.
4. Sender transmits **\[Message + Signature]** to receiver.

---

## **3. Steps in Verification (Receiver Side)**

1. Receiver gets message `M` and signature `(r, s)`.
2. Hash the message again using the same hash function.
3. Use sender’s **public key (y)** and `(r, s)` to verify the signature.
4. If computed values match → signature is valid → message authentic.

---

## **4. Diagram (Exam-friendly)**

```
 SIGNING:                          VERIFICATION:
 Message → Hash → + Private Key     Message → Hash
                ↓ Signature                  ↓ Compare
     [Message + Signature]   →   Public Key verifies signature
```

---

## **5. Real-world Example (Blockchain)**

* **Bitcoin**: Each transaction is signed using **private key** (ECDSA).
* Nodes verify it using the **public key** before adding it to the blockchain.

---

✅ **Exam Tip Mnemonic:**
**“Private signs, Public verifies.”**

---
