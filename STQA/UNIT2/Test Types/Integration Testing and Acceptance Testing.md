
---

## **Integration Testing and Acceptance Testing**

### **1. Integration Testing**

* **Definition:** Process of testing the interaction between **two or more integrated modules** to ensure they work together as expected.
* **Objective:** Detect interface errors, data flow issues, and module interaction problems.
* **Approaches:**

  * **Top-Down:** Start from main module → integrate lower modules step by step.
  * **Bottom-Up:** Start with low-level modules → integrate upward.
  * **Big-Bang:** Combine all modules at once and test.

**Example:** In a banking app, check if the **login module** correctly passes authenticated user data to the **account summary module**.

---

### **2. Acceptance Testing**

* **Definition:** Final phase of testing performed to verify if the system meets **business requirements** and is ready for **delivery to the customer**.
* **Objective:** Validate system from **end-user’s perspective**.
* **Types:**

  * **User Acceptance Testing (UAT):** Done by end users.
  * **Alpha/Beta Testing:** Early and real-world testing by users.

**Example:** A client tests an **online ticket booking system** to check if seat selection, payment, and confirmation work as per requirements.

---

### **Comparison (Diagram/Table)**

| Aspect           | Integration Testing          | Acceptance Testing                 |
| ---------------- | ---------------------------- | ---------------------------------- |
| **Focus**        | Interfaces between modules   | Overall business/user requirements |
| **Performed By** | Developers/Testers           | End-users/Clients                  |
| **Stage**        | After unit testing           | Final stage before release         |
| **Goal**         | Ensure modules work together | Ensure product is ready for use    |

---

✅ **Marks Coverage (5/5):** Definition + Objective (2) + Examples (2) + Comparison (1).

---
