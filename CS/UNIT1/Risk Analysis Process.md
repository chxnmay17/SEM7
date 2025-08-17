

---

# **Risk Analysis in Cyber Security — Expanded Steps**

### **Definition (recap)**

Risk analysis = **identify → evaluate → prioritize → treat** risks to the **CIA triad** (confidentiality, integrity, availability) so that security spend matches business impact.

---

## **1) Identify Assets**

* **What to list:** data (PII, financials, source code), apps, servers, cloud services, networks, people, third-parties.
* **Classify & value:** sensitivity (Public/Internal/Confidential/Restricted), **business criticality**, replacement cost, legal/regulatory exposure.
* **Add meta:** asset owner, location, dependencies (e.g., DB depends on S3, IAM), **Exposure Factor (EF)** for loss estimation.
* **Output:** **Asset inventory** with value & classification.

## **2) Identify Threats & Vulnerabilities**

* **Threats:** malware, phishing, insider abuse, misconfigurations, supply-chain, natural disasters, power failure.
* **Vulnerabilities:** unpatched CVEs, weak auth, open S3 buckets, missing logs, default configs, social-engineering susceptibility.
* **Map pairs:** link each **threat → vulnerability → asset** (e.g., Phishing → weak user awareness → Email system).
* **Output:** **Threat–Vulnerability (T–V) map** per asset.

## **3) Assess Risk (Likelihood × Impact)**

* **Choose scale:** qualitative (Low/Med/High or 1–5) or quantitative (₹/USD).
* **Likelihood drivers:** exploitability, exposure, attacker capability, past incidents.
* **Impact dimensions:** **CIA**, financial loss, regulatory fines, safety, reputational harm, recovery time.
* **Compute:**
  `Risk = Likelihood × Impact` (inherent risk before controls).
  *Quantitative add-ons:*

  * **SLE** = Asset Value × EF
  * **ARO** = Annualized Rate of Occurrence
  * **ALE** = SLE × ARO (expected yearly loss)
* **Output:** **Risk rating** per T–V pair; **risk matrix** positioning.

## **4) Evaluate Existing Controls**

* **Types:** administrative (policies, training), technical (MFA, EDR, WAF), physical (CCTV, access badges).
* **Effectiveness:** preventive/detective/corrective; coverage, timeliness, reliability.
* **Residual risk:** re-rate **after** considering control strength & coverage gaps.
* **Output:** **Control effectiveness notes** + **residual risk**.

## **5) Risk Treatment (Select Option & Plan)**

* **Options:**

  * **Avoid** (stop risky activity/service)
  * **Mitigate** (implement controls/patches, hardening, 2FA, segmentation)
  * **Transfer** (cyber insurance, contractual shift to vendor)
  * **Accept** (documented sign-off if within appetite)
* **Plan details:** chosen controls, **risk owner**, budget, timeline, **success criteria** (e.g., reduce risk from High→Low), dependencies.
* **Output:** **Risk Treatment Plan (RTP)** / action backlog.

## **6) Documentation & Reporting**

* **Risk Register fields:** Asset | Threat | Vulnerability | Inherent Risk | Existing Controls | **Residual Risk** | Treatment | Owner | Due Date | Status.
* **Compliance tie-ins:** map to ISO 27001, NIST CSF/800-53 controls for auditability.
* **Output:** up-to-date **risk register** + management report.

## **7) Continuous Monitoring & Review**

* **When to revisit:** new systems/releases, major incidents, vendor changes, law changes (e.g., data protection rules), at least quarterly.
* **Track:** KRIs (phish click rate, patch SLA, mean-time-to-detect), control drift, exceptions.
* **Improve:** feed incidents & pen-test results back into Step 2/3.
* **Output:** **Updated risks**, trend charts, decision memos.

---

### **Mini Worked Example (threaded)**

* **Asset:** Online banking portal (Critical) — owner: IT-Apps; AV ≈ ₹1Cr/mo revenue.
* **Threat–Vuln:** Phishing → poor user awareness (no 2FA adoption).
* **Inherent Risk:** Likelihood High (3/5), Impact High (5/5) ⇒ **15/25**.
* **Existing Controls:** SPF/DKIM/DMARC, basic anti-phish training (annual) ⇒ residual **Med-High**.
* **Treatment:** Mitigate via **MFA enforcement**, quarterly simulations, just-in-time training; **owner:** CISO; **target:** reduce to **Low** in 90 days.
* **Register update:** status tracking + KPI: phish-click < 4%, MFA > 95%.

---

### **Diagram (Cycle)**

```
Assets → Threats & Vulns → Risk Assess → Control Review
     → Treatment Plan → Document/Report → Monitor ↺
```

---

### **Common Pitfalls (1–2 lines each)**

* Skipping **asset valuation** → pretty matrices, wrong priorities.
* Rating **likelihood** without evidence (no logs/KRIs).
* “Set-and-forget” controls → residual risk creeps back.

---

### **Memory Mnemonic**

**“A T L C T D M”**
**A**ssets → **T**hreats/Vulns → **L**ikelihood/Impact → **C**ontrols → **T**reatment → **D**ocument → **M**onitor

---

### **Answer structure for 8 marks**

* Definition + objective (1.5)
* 7 steps with inputs/outputs & example (5)
* Diagram + pitfalls/mnemonic (1.5)

