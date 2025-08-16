

---

# **Importance of Hashing in Blockchain**

---

## **1. Introduction**

* **Hashing** = Process of converting input data → fixed-length string (hash) using algorithms like **SHA-256**.
* Fundamental to blockchain because it ensures **security, integrity, and immutability**.

---

## **2. Importance of Hashing in Blockchain**

1. **Block Identification**

   * Each block has a **unique hash** → acts as a digital fingerprint.
   * Even a small data change → completely new hash (avalanche effect).

2. **Immutability & Tamper Detection**

   * Every block stores the **hash of previous block**.
   * If any transaction is altered → hash changes → chain breaks → tampering detected.

3. **Transaction Integrity**

   * Hashing ensures data inside a block/transaction cannot be changed without detection.

4. **Proof of Work (Mining)**

   * Miners must find a hash value below a target (nonce-based).
   * Prevents spam and secures the network.

5. **Efficient Verification via Merkle Trees**

   * Transactions hashed and arranged in a Merkle tree → quick verification with Merkle Root.

---

## **3. Diagram (Exam-friendly)**

```
Block n: [Data + Prev Hash] → Hash_n
Block n+1: [Data + Hash_n] → Hash_(n+1)
```

(Shows how hashes link blocks securely)

---

## **4. Real-world Example**

* **Bitcoin** uses SHA-256:

  * Block header → hashed to generate block hash.
  * Ensures no one can modify past transactions without re-mining the entire chain.

---

✅ **Exam Tip Mnemonic**:
**“Hash = Heart of Blockchain → Identity, Integrity, Immutability.”**

---

