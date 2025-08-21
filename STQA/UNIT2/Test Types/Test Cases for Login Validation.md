
---

## **Test Cases for Login Validation**

### **Definition**

* Test cases are a set of **conditions or inputs** with expected results to validate whether the login functionality works correctly.
* Aim: Ensure **security, correctness, and usability** of the login module.

---

### **Sample Test Cases**

| **Test Case ID** | **Input**                                       | **Expected Result**                                    |
| ---------------- | ----------------------------------------------- | ------------------------------------------------------ |
| TC01             | Valid username + valid password                 | User successfully logs in (redirect to dashboard).     |
| TC02             | Valid username + invalid password               | Error message: *“Invalid password”*.                   |
| TC03             | Invalid username + any password                 | Error message: *“User does not exist”*.                |
| TC04             | Blank username + password                       | Prompt: *“Username required”*.                         |
| TC05             | Username + blank password                       | Prompt: *“Password required”*.                         |
| TC06             | SQL injection string as input                   | System should prevent login and show error (security). |
| TC07             | Valid credentials + session timeout             | Prompt for re-login after session expiry.              |
| TC08             | Case sensitivity check (e.g., “User” vs “user”) | Respect case rules as per requirements.                |

---

### **Diagram (Login Validation Flow)**

```
[Enter Credentials] 
      ↓
[Check Validity] 
  ┌──────────────┐
  │ Valid        │──► [Dashboard]
  │ Invalid      │──► [Error Message]
  └──────────────┘
```

---

### **Key Points**

* Covers **positive and negative scenarios**.
* Ensures **functionality, error handling, and security** of login system.
* Helps prevent **unauthorized access** and improves user experience.

---

✅ **Marks Coverage (5/5):** Definition (1) + Table of test cases (3) + Diagram/Key points (1).

---
