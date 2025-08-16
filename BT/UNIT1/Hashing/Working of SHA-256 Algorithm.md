

---

# **Working of SHA-256 Algorithm**

---

## **1. Introduction**

* **SHA-256** = Secure Hash Algorithm with **256-bit output**.
* Developed by **NSA & NIST (2001)**.
* Standard hashing algorithm used in **Bitcoin Blockchain**.
* Converts input of any size → fixed **256-bit hash**.

---

## **2. Steps in Working of SHA-256**

1. **Pre-processing**

   * Input message is converted into **binary**.
   * Padding: Message length is padded so that total length ≡ 448 (mod 512).
   * Append 64-bit representation of original message length.
   * Final message size = multiple of **512 bits**.

2. **Divide Message into Blocks**

   * Message split into **512-bit blocks**.
   * Each block processed separately.

3. **Message Schedule Preparation**

   * Each 512-bit block divided into **16 words (32 bits each)**.
   * Expanded into **64 words** using logical functions (σ0, σ1).

4. **Initialize Hash Values**

   * 8 constant 32-bit values (H0 to H7) predefined by SHA-256.

5. **Compression Function (Main Loop)**

   * Each block goes through **64 rounds**.
   * Uses logical operations: AND, OR, XOR, ROTR (rotate right), SHR (shift right).
   * Constant values (K0 to K63) used in each round.
   * Output updates hash values.

6. **Final Hash Value**

   * After all blocks processed → final concatenated 256-bit hash.
   * This is the **digital fingerprint** of the input.

---

## **3. Diagram (Exam-friendly)**

```
Message → Pre-processing → Blocks → Compression (64 rounds) → 256-bit Hash
```

---

## **4. Properties of SHA-256**

* Fixed output length (256 bits).
* Avalanche effect (small input change → large hash change).
* Collision resistant.
* Efficient & secure for blockchain.

---

## **5. Role in Blockchain**

* Used in **Bitcoin**:

  * Mining → PoW requires finding hash below target.
  * Block header hashed with SHA-256 twice (double hashing).
* Ensures immutability & security of transactions.

---

## **6. Example**

Input: **“Hello”**
Output (SHA-256):
`185f8db32271fe25f561a6fc938b2e264306ec304eda518007d1764826381969`

---

✅ **Exam Tip Mnemonic:**
**“SHA = Split → Hash rounds → Assemble final 256-bit output.”**

---


