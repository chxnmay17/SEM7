Diff?

---

## **Test Policy and Test Strategy in Test Documentation**

### **1. Test Policy**

* **Definition:** A **high-level document** that defines the **organization’s overall objectives and principles of testing**.
* **Purpose:** Ensures testing aligns with **business goals** and quality standards.
* **Key Points:**

  * Defines **testing objectives** (e.g., defect prevention, risk reduction).
  * Establishes **responsibilities and roles** in testing.
  * Provides **long-term vision** for quality assurance.
* **Example:** An IT company’s test policy may state: *“All products must undergo functional and security testing before release.”*

---

### **2. Test Strategy**

* **Definition:** A **high-level plan** derived from the test policy that describes the **approach, techniques, and standards** for testing.
* **Purpose:** Guides *how testing should be performed* across projects.
* **Key Points:**

  * Defines **testing levels** (unit, integration, system, acceptance).
  * Specifies **test design techniques** (black-box, white-box, risk-based).
  * Defines **defect severity levels, tools, and automation guidelines**.
* **Example:** An organization’s test strategy may mandate: *“Use automation for regression testing and risk-based testing for critical modules.”*

---

### **Relation in Documentation (Diagram)**

```
        Test Policy  (Overall organizational vision)
                   ↓
        Test Strategy (Approach & standards across projects)
                   ↓
        Test Plan     (Project-specific implementation)
```

---

### **Key Difference**

* **Test Policy:** *Why testing is important* (organizational vision).
* **Test Strategy:** *How testing will be done* (practical approach).

---

✅ **Marks Coverage (5/5):** Policy (2) + Strategy (2) + Relation/Diagram (1).

---


---

### ✅ **1. Test Policy** – *High-Level Company-Wide Vision*

| Aspect      | Description                                                                                                         |
| ----------- | ------------------------------------------------------------------------------------------------------------------- |
| **Scope**   | Organization-wide                                                                                                   |
| **Purpose** | Defines the **overall approach to quality and testing** in the company                                              |
| **Owner**   | Senior management or QA leadership                                                                                  |
| **Details** | - Long-term goals for quality<br>- Roles & responsibilities<br>- Commitment to testing<br>- General tools/standards |
| **Analogy** | Like a **company mission statement** for QA                                                                         |

---

### ✅ **2. Test Strategy** – *Project or Program-Level Approach*

| Aspect      | Description                                                                                                                                         |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Scope**   | Project-wide or product-wide                                                                                                                        |
| **Purpose** | Defines **how testing will be done** across the project                                                                                             |
| **Owner**   | Test Manager / QA Lead                                                                                                                              |
| **Details** | - Types of testing (unit, integration, regression, etc.)<br>- Tools and environments<br>- Test levels<br>- Risk management<br>- Entry/exit criteria |
| **Analogy** | Like a **blueprint or playbook** for how testing should happen for a specific product/project                                                       |

---

### ✅ **3. Test Plan** – *Detailed Execution-Level Plan*

| Aspect      | Description                                                                                     |
| ----------- | ----------------------------------------------------------------------------------------------- |
| **Scope**   | Specific feature, release, or sprint                                                            |
| **Purpose** | Describes **what will be tested, when, how, and by whom**                                       |
| **Owner**   | Test lead or QA engineer on the team                                                            |
| **Details** | - Test schedule<br>- Resources<br>- Specific test cases<br>- Pass/fail criteria<br>- Milestones |
| **Analogy** | Like a **checklist and timeline** for executing tests for a sprint/release                      |

---

### 🔁 Summary Table

| Item              | Scope                 | Owned by        | Answers…                           | Example                                                |
| ----------------- | --------------------- | --------------- | ---------------------------------- | ------------------------------------------------------ |
| **Test Policy**   | Org-level             | QA Leadership   | Why we test and our quality values | “We value automated testing across all products.”      |
| **Test Strategy** | Project-level         | QA/Test Manager | How we’ll approach testing         | “This app will use risk-based testing and automation.” |
| **Test Plan**     | Feature/Release-level | Test Lead/QA    | What, when, who, and how           | “We’ll test login by Aug 28 using 5 test cases.”       |

---



