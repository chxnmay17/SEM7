
*"What is iterative algorithm? Explain iterative algorithm design issues using example"* 

---

# **Iterative Algorithm & Design Issues**

## **1. Definition**

* **Iterative Algorithm**:
  An algorithm that **repeats a set of instructions** a fixed number of times or until a specific **termination condition** is met.
* Uses **loops** (`for`, `while`, `do-while`) instead of recursion.
* Often preferred for **predictable iteration counts** and lower memory overhead compared to recursion.

---

## **2. Characteristics**

* Repetition of steps.
* State changes after each iteration.
* Controlled by **loop control variables** and **termination conditions**.

---

## **3. Design Issues in Iterative Algorithms**

When designing iterative algorithms in **Design and Analysis of Algorithm (DAA)**, key issues include:

### **(i) Initialization**

* Properly set loop variables before the iteration starts.
* **Example**: In summing numbers, `sum` must be initialized to 0.

### **(ii) Loop Control**

* Decide between **fixed count loops** (`for`) and **condition-controlled loops** (`while`).
* Poor loop control can cause **infinite loops**.

### **(iii) Termination Condition**

* Clearly define when the loop should end.
* Must prevent **off-by-one errors**.

### **(iv) Maintenance of Invariants**

* Maintain certain properties after each iteration to ensure correctness (Loop Invariant Property).
* **Example**:Finding the Maximum Number in a List
*At the start of each loop, `max_so_far` stores the biggest number we've seen so far.
This property stays true after every iteration, so by the end of the loop, `max_so_far` holds the correct maximum value.


### **(v) Efficiency**

* Minimize unnecessary iterations and redundant computations.

---

## **4. Example – Summation of First n Numbers**

**Algorithm:**

```c
sum = 0;               // Initialization
for (i = 1; i <= n; i++) {  // Loop Control & Termination
    sum = sum + i;      // Update step
}
print(sum);
```

**Design Issue Handling in Example**:

1. **Initialization** → `sum = 0`, `i = 1`.
2. **Loop Control** → `i <= n` ensures exactly `n` iterations.
3. **Termination Condition** → Stops when `i = n+1`.
4. **Invariant Maintenance** → At the start of each iteration, `sum = 1+2+...+(i-1)`.
5. **Efficiency** → Single pass, O(n) time, O(1) space.

---

## **5. Diagram – Iterative Flow**

```
      ┌───────────────┐
      │ Initialization │
      └──────┬────────┘
             ↓
     ┌──────────────────┐
     │ Check Condition  │─No─→ End
     └──────┬───────────┘
            ↓ Yes
    ┌───────────────────┐
    │ Perform Operation │
    └──────┬────────────┘
           ↓
    ┌───────────────┐
    │ Update State  │
    └──────┬────────┘
           ↑ (Repeat)
```

---

✅ **Exam Tip**: For full marks, **define** iterative algorithm, **list design issues** with 1–2 lines each, and give **clear example + diagram**.

---

