

---

# **Elliptic Curve Cryptography (ECC)**

---

## **1. Definition**

* ECC is a **public key cryptography** technique based on the **algebraic structure of elliptic curves** over finite fields.
* Provides **same security with smaller key size** compared to RSA.
* Widely used in **Blockchain** for generating public-private keys and digital signatures.

---

## **2. Elliptic Curve Equation**

$$
y^2 = x^3 + ax + b \pmod{p}
$$

* Forms a **curve** when plotted over finite field.
* Points on the curve form a group with defined arithmetic operations (point addition, doubling).

---

## **3. Working Principle**

1. **Key Generation**

   * Choose a random **private key (d)**.
   * Compute **public key (Q = d × G)**, where **G** is base point on the curve.

2. **Encryption (Simplified idea)**

   * Sender encrypts message M using **Receiver’s public key (Q)** and base point G.

3. **Decryption**

   * Receiver uses **private key (d)** to recover original message M.

👉 Security comes from **Elliptic Curve Discrete Logarithm Problem (ECDLP)** – very hard to reverse public key back to private key.

---

## **4. Diagram **
<img width="588" height="37" alt="image" src="https://github.com/user-attachments/assets/6f1f9dcf-1af7-408f-9ee0-30372deda32b" />

<img width="891" height="626" alt="image" src="https://github.com/user-attachments/assets/5f8ab564-f3d7-44a9-b092-d3a3e2a37522" />

<img width="1007" height="361" alt="image" src="https://github.com/user-attachments/assets/91572015-eb46-49ef-8446-82196aa79da6" />


```

---

## **5. Advantages of ECC**

* **Smaller key size, higher security** (e.g., 256-bit ECC ≈ 3072-bit RSA).
* **Efficient computation** → faster in Blockchain.
* **Widely adopted in Blockchain**: Bitcoin, Ethereum use **ECDSA** (Elliptic Curve Digital Signature Algorithm).

---

## **6. Real-World Example in Blockchain**

* **Bitcoin wallet address generation**:

  * Private Key → Public Key (via ECC) → Hashed → Wallet Address.

---

✅ **Mnemonic for Exam:**
**“ECC = Efficient, Compact, and Cryptographically secure.”**

---

