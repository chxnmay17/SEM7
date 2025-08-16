
---

# **Properties of Hash Function in Blockchain**

---

## **1. Introduction**

* A **hash function** maps input of any size → fixed-length output (hash).
* In Blockchain, algorithms like **SHA-256** are used.
* Ensures **security, integrity, and immutability** of data.

---

## **2. Properties of Hash Function**

1. **Deterministic**

   * Same input → always produces the same hash.
   * Ensures consistency in block/transaction verification.

2. **Fixed Output Length**

   * Regardless of input size, output is of fixed length (e.g., SHA-256 → 256 bits).
   * Standardized and easy to compare.

3. **Pre-image Resistance**

   * From a given hash, it is computationally infeasible to retrieve the original input.
   * Provides **one-way security**.

4. **Collision Resistance**

   * Two different inputs should not produce the same hash.
   * Prevents fraud and maintains integrity.

5. **Avalanche Effect**

   * A small change in input → drastically different hash.
   * Helps in detecting tampering in blockchain.

6. **Fast Computation**

   * Hashing must be computationally efficient.
   * Required for large-scale blockchain operations (mining, verification).

---

## **3. Diagram (Exam-friendly)**

```
Input Data → [Hash Function: SHA-256] → Fixed-length Hash
   "Hello"  →  185f8db32271fe25f561a6fc...
   "hello"  →  2cf24dba5fb0a30e26e83b2...
```

(Shows Avalanche Effect)

---

## **4. Real-world Example in Blockchain**

* **Bitcoin**:

  * Uses SHA-256 for block hashes & mining.
  * Any tampering with transaction data changes the block hash → invalid chain.

---

✅ **Exam Tip Mnemonic:**
**“Hash = D-F-P-C-A-F”**
(**Deterministic, Fixed length, Pre-image resistant, Collision resistant, Avalanche effect, Fast**)

---


