<img width="471" height="261" alt="image" src="https://github.com/user-attachments/assets/33635d76-e7fc-4c4e-896f-c25214a80f63" />


A loop invariant is a property that holds true before and after each iteration of a loop. We will use this method to prove that the variable `min` correctly holds the minimum value of the elements processed so far.

---

### The Loop Invariant

Let's define the loop invariant property:

> At the start of each iteration of the `for` loop, specified by the counter `i`, the variable `min` holds the minimum value in the subarray $A[0...i-1]$.

We need to prove three things for this invariant:
1.  **Initialization:** The invariant is true before the first loop iteration.
2.  **Maintenance:** If the invariant is true before an iteration, it remains true before the next iteration.
3.  **Termination:** When the loop terminates, the invariant gives us a useful property that helps show the algorithm is correct.

---

### Proof

#### 1. Initialization

* **Before the first iteration**, the loop counter `i` is initialized to `1`.
* The invariant states that `min` must hold the minimum value of the subarray $A[0...(1-1)]$, which is $A[0]$.
* The statement before the loop, `min = A[0]`, ensures this is true. The minimum value of a subarray containing just one element is the element itself.
* Thus, the invariant holds before the first iteration begins. ✅

#### 2. Maintenance

* Let's **assume** that at the start of the iteration for a given `i` (where $1 \le i < n$), the invariant is true. That is, `min` holds the minimum value from the subarray $A[0...i-1]$.
* During the loop body for iteration `i`, the element $A[i]$ is compared with `min`.
    * **Case 1: $A[i] < min$**
        The variable `min` is updated to $A[i]$. Since `min` was the minimum of $A[0...i-1]$, and $A[i]$ is even smaller, the new `min` is now the minimum of the entire subarray $A[0...i]$.
    * **Case 2: $A[i] \ge min$**
        The variable `min` remains unchanged. Since `min` is already the minimum of $A[0...i-1]$ and is less than or equal to $A[i]$, it is also the minimum of the entire subarray $A[0...i]$.
* In both cases, at the end of the iteration, `min` holds the minimum value of the subarray $A[0...i]$. When the loop counter increments to $i+1$ for the next iteration, our invariant holds true for the subarray $A[0... (i+1)-1]$.
* Therefore, the invariant is maintained from one iteration to the next. ✅

#### 3. Termination

* The loop terminates when the condition $i < n$ becomes false. Since `i` starts at 1 and increments, this happens when $i$ becomes equal to $n$.
* At the point of termination, according to our invariant, `min` holds the minimum value of the subarray $A[0...n-1]$.
* The subarray $A[0...n-1]$ represents the **entire array** of $n$ numbers.
* The final step of the algorithm is to `return(min)`.
* Thus, upon termination, the algorithm correctly returns the minimum number from the entire given array. ✅

Since all three conditions (Initialization, Maintenance, and Termination) are satisfied, the algorithm is proven to be correct.
