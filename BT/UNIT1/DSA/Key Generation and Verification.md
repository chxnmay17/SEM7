

---

# **DSA Key Generation and Verification**

---

## **1. Introduction**

* **DSA (Digital Signature Algorithm)** is an asymmetric cryptographic algorithm.
* Provides **authentication, integrity, and non-repudiation**.
* Uses **private key** for signing and **public key** for verification.

---

## **2. Key Generation in DSA**

1. **Select domain parameters**:

   * Large prime numbers **p** and **q**.
   * Generator value **g**.

2. **Private Key (x)**:

   * Randomly chosen integer where `1 < x < q`.

3. **Public Key (y)**:

   * Computed as `y = g^x mod p`.

👉 Result: **Key Pair = (Private Key x, Public Key y)**

---

## **3. Signature Verification in DSA**

1. **Signing (Sender)**

   * Message is hashed (e.g., SHA-256).
   * Signature `(r, s)` generated using private key `x`.
   * Sender transmits **\[Message + Signature]**.

2. **Verification (Receiver)**

   * Receiver hashes the received message.
   * Uses **public key y** + signature `(r, s)` to verify.
   * If values match → signature valid → message authentic.

---

## **4. Diagram (Exam-friendly)**

```
 Key Generation:
  Private Key (x)  →  Sign
  Public Key (y)   →  Verify

 Signing:  Message → Hash → Signature (with Private Key)
 Verification: Message → Hash → Verified (with Public Key)
```

---

## **5. Real-world Example in Blockchain**

* **Bitcoin** uses **ECDSA (Elliptic Curve DSA)**.
* Wallet owner signs transaction with **private key**.
* Network nodes verify using **public key** before adding to block.

---

✅ **Exam Tip Mnemonic:**
**“DSA → x (private) signs, y (public) verifies.”**

---


