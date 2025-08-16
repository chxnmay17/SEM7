
---

# **Hashing and its Role in Blockchain**

---

## **1. What is Hashing?**

* **Definition**:
  A **hash function** converts input data of any size → fixed-length string (hash value).
* **Properties**:

  * Deterministic (same input → same output).
  * Irreversible (cannot retrieve input from hash).
  * Fast computation.
  * Collision resistant (two different inputs ≠ same output).
  * Avalanche effect (small input change → large change in hash).
* **Algorithms**: SHA-256, SHA-3, MD5 (not secure).

**Example**:
`Hello` → SHA-256 →
`185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969`

---

## **2. Role of Hashing in Blockchain**

🔑 **Hashing is the backbone of Blockchain security and integrity.**

* **Block Identification**

  * Each block has a **unique hash** generated from its data.
  * Even a small data change → new hash → tampering detected.

* **Linking of Blocks**

  * Each block contains **hash of the previous block**.
  * Creates an immutable chain (tampering breaks the chain).

* **Proof of Work (Mining)**

  * Miners solve puzzles by finding a hash below a target value.
  * Ensures consensus and prevents spam.

* **Transaction Integrity**

  * Transactions are hashed & combined in a **Merkle Tree**.
  * Merkle Root stored in block header → quick verification.

* **Digital Signatures & Wallets**

  * Hashing used with public-private keys to generate blockchain addresses.

---

## **Diagram (Exam-friendly)**

```
[Transaction Data] → SHA-256 → [Hash Value]
Block n: [Data + Prev Hash] → Hash_n
Block n+1: [Data + Hash_n] → Hash_(n+1)
```

(Shows linkage & immutability)

---

## **Real-World Example in Blockchain**

* **Bitcoin**: Uses **SHA-256** for block hashes & mining.
* Ensures that altering even 1 transaction would require recomputing hashes of all following blocks → computationally infeasible.

---

✅ **Exam Tip Mnemonic for Recall:**
**“Hash = Heart of Blockchain → Identity, Integrity, Immutability.”**

---
