

---

# Logical Models in Machine Learning

### Definition

* **Logical models** are machine learning models that use **rules based on logic (if–then conditions)** to make predictions or classifications.
* They represent knowledge in terms of **propositions** (true/false statements).

---

### Key Features

* Represented as **Boolean functions**.
* Output: **Discrete values** (e.g., Yes/No, True/False, Class A/Class B).
* Suitable for problems with **clear logical rules**.
* Easy to interpret and explain.

---

### Common Logical Models

1. **Decision Trees** – hierarchical structure of if–then rules.
2. **Rule-based Classifiers** – sets of conditions like “If condition → then outcome”.
3. **Propositional Logic Models** – represent knowledge using logical operators (AND, OR, NOT).

---

### Example (Decision Tree for Weather & Playing Tennis)

If weather = **Sunny** AND humidity = **High** → Don’t Play
If weather = **Sunny** AND humidity = **Normal** → Play
If weather = **Overcast** → Play
If weather = **Rain** AND wind = **Strong** → Don’t Play
If weather = **Rain** AND wind = **Weak** → Play

📌 Here, classification (Play/Don’t Play) is made using logical conditions.

---

### Diagram (simplified decision tree)

```
          Weather?
        /    |     \
    Sunny  Overcast  Rain
     /  \      |      /  \
 Humid  Norm  Play Strong Weak
  No     Yes         No    Yes
```

---

### Advantages

* Interpretable and human-readable.
* Works well with categorical data.
* Can mimic human reasoning.

---

✅ **Exam Tip Mnemonic – LDR (Logical Models = Decision trees, Rule-based, easy to Read)**

---


