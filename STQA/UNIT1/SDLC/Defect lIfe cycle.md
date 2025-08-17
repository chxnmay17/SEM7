
---

# **Defect Life Cycle (Bug Life Cycle)**

👉 The **Defect Life Cycle** defines the **states a defect goes through** from its identification to its closure in the software testing process.

---

### **Phases of Defect Life Cycle**

1. **New** – Defect is identified and reported by the tester.
2. **Assigned** – Project Manager/Lead assigns defect to a developer.
3. **Open** – Developer starts analyzing and fixing the defect.
4. **Fixed** – Developer resolves the issue and marks it as fixed.
5. **Retest** – Tester rechecks the defect in the new build.
6. **Verified** – If retest passes, defect is marked as verified.
7. **Closed** – Tester confirms the fix and closes the defect.
8. **Reopened** – If defect still exists after retest, it is reopened.
9. **Deferred / Rejected** – If the defect is not valid or postponed for later release.

---

### **Diagram (Exam-style)**

```
 New → Assigned → Open → Fixed → Retest → Verified → Closed
                 ↓
            Rejected / Deferred
                 ↑
              Reopened
```

---

### **Example**

* In a **Banking App**, a tester finds that “login fails with correct credentials.”
* Reported as **New → Assigned to developer → Fixed → Retested → Verified → Closed**.

---

✅ **Exam Tip:**

* Always **list the states clearly in sequence**.
* Draw a **neat diagram** with arrows (like above).
* Add **one real-world example** for clarity.

---
