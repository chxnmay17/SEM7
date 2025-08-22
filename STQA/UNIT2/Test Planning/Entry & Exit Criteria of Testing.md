
---

## **Entry & Exit Criteria of Testing**


---

## **1. Entry Criteria**

### **Definition**

Entry criteria are **conditions or requirements that must be satisfied before testing can officially start.**
👉 Think of it as a **“checklist before boarding a flight”** – unless all conditions are met, the flight (testing) won’t take off.

---

### **Purpose**

* To make sure testing begins **only when everything is ready**.
* Avoids **wasting time** testing incomplete or unstable code.
* Ensures **quality of testing** by having all resources (documents, environment, test data) available.


---

### **Examples of Entry Criteria**

1. **Approved SRS/Design Documents**
   → Testers must know *what to test* → need clear requirements & design.

2. **Test Environment Set Up (Hardware/Software)**
   → Without proper environment (servers, OS, tools), testing can’t be executed.

3. **Test Data Prepared**
   → Realistic data must exist for meaningful test execution.

4. **Code is Unit Tested and Stable**
   → Developers finish unit testing → ensures major bugs are fixed before testers start.

---

### **In Short (Exam Writing Version)**

**Entry Criteria** are the conditions that must be met before testing begins.
**Purpose:** To ensure testing is carried out effectively with proper resources and stable code.
**Examples:** Approved SRS/design docs, test environment setup, test data availability, and unit-tested stable code.







---

## **2. Exit Criteria**

### **Definition**

Exit criteria are **conditions or requirements that must be fulfilled to formally stop testing.**
👉 Think of it as a **“landing checklist for a flight”** – testing ends only when everything is safe and goals are met.

---

### **Purpose**

* To make sure testing ends **only when software meets the quality goals**.
* Prevents **premature delivery** of software with critical issues.
* Provides **evidence** that testing is complete and product is ready.




---

### **Examples of Exit Criteria**

1. **All Planned Test Cases Executed**
   → No pending or skipped test cases.

2. **Defect Density within Acceptable Limit**
   → The number of defects per size of code is under control.

3. **Critical and High-Severity Defects Fixed & Verified**
   → Showstoppers must be resolved before release.

4. **Test Summary Report Prepared**
   → Final documentation showing coverage, defects, and overall results.

---

### **In Short (Exam Writing Version)**

**Exit Criteria** are the conditions that must be satisfied to formally conclude testing.
**Purpose:** Ensures software quality goals are met before release.
**Examples:** All test cases executed, defect density within limit, critical defects fixed and verified, test summary report prepared.


---

### **Diagram (Testing Lifecycle with Criteria)**

```
 [ Entry Criteria Met ]  →  [ Testing Activities ]  →  [ Exit Criteria Satisfied ]
```

---

### **Key Points**

* **Entry criteria = readiness check** (can we start?).
* **Exit criteria = completion check** (can we stop?).
* Helps maintain **discipline, quality, and traceability** in testing.

---

✅ **Marks Coverage (5/5):** Entry (2) + Exit (2) + Diagram/Key points (1).

---
