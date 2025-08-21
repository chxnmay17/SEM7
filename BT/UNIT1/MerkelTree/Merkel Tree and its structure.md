---

# **Merkle Tree in Blockchain**

---

## **1. What is Merkle Tree?**

* **Definition**:
  A **Merkle Tree (Hash Tree)** is a **binary tree** structure where:

  * **Leaf nodes** = hashes of individual transactions.
  * **Non-leaf nodes** = hashes of their child nodes.
  * **Root node** = Merkle Root (single hash representing all transactions).
* Named after **Ralph Merkle** (1979).
* Used in **Blockchain** for efficient & secure verification of large data sets.

---

## **2. Structure of Merkle Tree**

* **Step 1**: Each transaction (Tx) is hashed → leaf node.
* **Step 2**: Pair of hashes combined → hashed again to form parent node.
* **Step 3**: Process continues until one root hash remains → **Merkle Root**.
* **Merkle Root** is stored in the **block header**.

---

## **Diagram (Exam-friendly)**

<img width="828" height="716" alt="image" src="https://github.com/user-attachments/assets/9275909d-f168-4caf-a702-2e10c4e9e8e6" />


---

## **3. Role in Blockchain**

* **Efficient Verification**:
  Instead of downloading all transactions, nodes only check **Merkle Path**.
* **Integrity & Security**:
  Any change in a single transaction → changes Merkle Root → tampering detected.
* **Scalability**:
  Lightweight clients (SPV – Simplified Payment Verification) use Merkle Trees to verify transactions without downloading the entire blockchain.

---

## **Real-World Example**

* **Bitcoin**: Uses Merkle Tree to summarize all transactions in a block.
* Merkle Root stored in the block header ensures immutability.

---

✅ **Exam Tip Mnemonic**:
**“Merkle = Many Tx → One Root → Easy Verify.”**

---
