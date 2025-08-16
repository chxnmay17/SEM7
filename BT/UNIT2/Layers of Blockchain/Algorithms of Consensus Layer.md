

---

# **Consensus Algorithms in Blockchain**

### **Definition**

* A **consensus algorithm** is a mechanism that ensures **all nodes in a blockchain network agree on the same ledger state**, even in the presence of failures or malicious actors.
* It provides **trust, consistency, and security** in decentralized systems.

---

### **Main Consensus Algorithms**

1. **Proof of Work (PoW)**

   * **Working:** Miners solve complex cryptographic puzzles; the first to solve adds a block.
   * **Features:** High security, energy-intensive, slower transactions.
   * **Example:** Bitcoin.
   * **Diagram (simple):**

     ```
     Miners → Solve Puzzle → Winner Adds Block → Broadcast to Network
     ```

---

2. **Proof of Stake (PoS)**

   * **Working:** Validators are chosen based on the amount of cryptocurrency staked.
   * **Features:** Energy-efficient, faster block creation, risk of centralization if wealth is concentrated.
   * **Example:** Ethereum 2.0, Cardano.
   * **Diagram (simple):**

     ```
     Nodes Stake Coins → Validator Selected → Block Added
     ```

---

3. **Delegated Proof of Stake (DPoS)**

   * **Working:** Token holders vote for a few trusted delegates who validate blocks.
   * **Features:** Very fast, democratic, but less decentralized.
   * **Example:** EOS, TRON.

---

4. **Practical Byzantine Fault Tolerance (PBFT)**

   * **Working:** Nodes exchange messages to reach agreement even if some act maliciously.
   * **Features:** High throughput, best for permissioned blockchains.
   * **Example:** Hyperledger Fabric.

---

### **Summary Table**

| Algorithm | Selection Method            | Pros                           | Cons                            | Example      |
| --------- | --------------------------- | ------------------------------ | ------------------------------- | ------------ |
| **PoW**   | Solve cryptographic puzzles | Very secure, proven            | Slow, energy-hungry             | Bitcoin      |
| **PoS**   | Stake-based validator       | Energy-efficient, scalable     | Wealth concentration            | Ethereum 2.0 |
| **DPoS**  | Delegates elected by voting | Fast, democratic               | Less decentralized              | EOS, TRON    |
| **PBFT**  | Voting among nodes          | High speed, tolerant to faults | Not scalable for large networks | Hyperledger  |

---

### **Real-World Analogy**

* **PoW:** Like a competition exam; only the fastest solver wins.
* **PoS:** Like lottery tickets; more tickets = higher chance to win.
* **DPoS:** Like electing class representatives to make decisions.
* **PBFT:** Like group discussion where majority agreement is needed.

---

### **Exam Tip (Summary)**

* Consensus algorithms ensure **agreement, trust, and security** in blockchain.
* Common algorithms: **PoW, PoS, DPoS, PBFT** – each balances **security, efficiency, and scalability** differently.

---

