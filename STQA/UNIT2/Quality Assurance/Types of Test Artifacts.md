
---

## **Types of Test Artifacts**

### **Definition**

* **Test Artifacts** are the **documents, deliverables, and by-products** created during the software testing process.
* They help in **planning, executing, tracking, and improving** the testing activities.

---

### **Types of Test Artifacts**

1. **Test Plan**

   * Describes *scope, objectives, resources, schedule, and approach* of testing.
   * Example: Banking app → modules to test, tools used, roles assigned.

2. **Test Strategy**

   * High-level approach describing *testing levels, techniques, standards, and tools*.
   * Example: Mandating automation for regression testing.

3. **Test Cases**

   * Step-by-step conditions with inputs and expected results.
   * Example: Login with valid and invalid credentials.

4. **Test Scenario**

   * High-level description of *what to test* without detailed steps.
   * Example: “Check user login functionality.”

5. **Requirement Traceability Matrix (RTM)**

   * Maps requirements ↔ test cases to ensure *complete coverage*.
   * Example: Requirement R1 linked to TC01, TC02.

6. **Test Data**

   * Input values used while executing test cases.
   * Example: Username/password combinations, payment card numbers.

7. **Defect Report / Bug Report**

   * Document describing identified defects with severity, priority, and steps to reproduce.
   * Example: “Login page crashes when entering 100+ characters in username.”

8. **Test Summary Report**

   * Final report with *test results, defect status, and quality assessment*.
   * Example: “95% test cases passed, 2 high severity defects open.”

---

### **Diagram (Hierarchy of Artifacts)**

```
 Test Strategy
       ↓
   Test Plan
       ↓
 Test Scenarios → Test Cases → Test Data
       ↓
 Defect Reports → Test Summary Report
```

---

### **Key Point**

* Test artifacts provide **transparency, traceability, and quality evidence** for stakeholders, ensuring testing is **systematic and reliable**.

---

✅ **Marks Coverage (5/5):** Definition (1) + Types (3) + Diagram/Key point (1).

---
