
---

## **Use Case Testing**

### **Definition**

* Use Case Testing is a **black-box testing technique** that validates whether a system functions as per its **use cases** (end-user scenarios).
* Focuses on **real-life workflows** of the application instead of isolated functions.
* Ensures the system meets **functional requirements** from the user’s perspective.

---

### **Steps in Use Case Testing**

1. Identify actors (users/external systems).
2. Define use cases (scenarios of interaction).
3. Design test cases for **main flow** and **alternate flows**.
4. Execute and verify expected behavior.

---

### **Example: Online ATM Withdrawal**

**Use Case:** Withdraw Cash

* **Actors:** Customer, ATM System

* **Main Flow:**

  1. Insert card
  2. Enter PIN
  3. Select “Withdraw Cash”
  4. Enter amount
  5. Receive cash & receipt

* **Test Case Derived:**

  * Valid card + correct PIN + valid balance → cash dispensed.
  * Invalid PIN (alternate flow) → show error.
  * Insufficient balance → transaction denied.

---

### **Diagram (Simple Use Case)**

```
   [Customer] ----> (Withdraw Cash)
```

---

### **Key Points**

* Ensures **end-to-end validation** of user requirements.
* Covers **functional correctness** and **exception handling**.
* Effective for testing **business processes** in real-world scenarios.

---

✅ **Marks Coverage (5/5):** Definition (1) + Steps (1) + Example (2) + Key Points (1).

---
