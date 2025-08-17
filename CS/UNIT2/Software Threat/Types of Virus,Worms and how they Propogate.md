

---

## **Viruses and Worms**

* **Virus:** Malicious program that attaches itself to a host file/program and spreads when executed.
* **Worm:** Self-replicating malware that spreads independently over networks without needing a host file.

---

## **Types of Viruses**

1. **File Infector Virus** – Attaches to executable files (.exe, .com).
2. **Boot Sector Virus** – Infects master boot record (MBR) of storage devices.
3. **Macro Virus** – Targets macros in applications (e.g., MS Word).
4. **Polymorphic Virus** – Changes its code to avoid detection.
5. **Resident Virus** – Stays in memory and infects files/programs actively.

---

## **Types of Worms**

1. **Email Worms** – Spread via infected attachments/links.
2. **Internet Worms** – Exploit vulnerabilities in web applications or services.
3. **File-Sharing Worms** – Spread through peer-to-peer (P2P) networks.
4. **Instant Messaging Worms** – Propagate via chat applications.

---

## **Propagation Mechanisms**

### **A. Virus Propagation**

* Needs **host program** to spread.
* **Execution required** (e.g., double-click infected file).
* Propagation methods:

  * Copying into other files on same system.
  * Spreading via USB drives, CDs, external storage.
  * Infected documents shared via email or cloud.
  * Macro execution when user opens malicious doc.

📌 *Example:* "ILOVEYOU" virus spread through infected email attachments, activated only when opened.

---

### **B. Worm Propagation**

* **Autonomous spreading** (no host needed).
* Exploits **network vulnerabilities** to spread rapidly.
* Propagation methods:

  * **Email** – sends copies to contacts in victim’s address book.
  * **Network Scanning** – finds open ports, exploits weak security.
  * **Instant Messaging** – sends malicious links/files.
  * **File-sharing/Cloud** – replicates disguised as legitimate files.
  * **Internet** – uses scripts on websites (drive-by downloads).

📌 *Example:* *Code Red* worm spread by exploiting Microsoft IIS server vulnerability, infected **359,000 systems in less than 14 hours**.

---





### **Diagram: Propagation**

```
       Virus Propagation                     Worm Propagation
   (Needs Host Execution)                  (Self-Replicating)

 [User opens file]                      [Network Scan → Exploit]
        ↓                                       ↓
 [Infected Program]                     [Worm Copies Itself]
        ↓                                       ↓
 [Spreads via USB/Email]                [Spreads via Email, IM, LAN]
```

---

✅ **Exam Tip (5 marks):**

* Define virus & worm (2 lines).
* Mention **3–4 types each**.
* Explain propagation difference clearly.
* Add a **small diagram** → full marks.


