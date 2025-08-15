

---

## **Multidimensional Scaling (MDS)**

**Definition:**
Multidimensional Scaling is a **dimensionality reduction technique** that represents **high-dimensional data** in a lower-dimensional space while preserving the **pairwise distances or dissimilarities** between data points as much as possible.

---

## **Features of MDS**

1. **Distance Preservation**

   * Maintains the original pairwise distances (Euclidean, Manhattan, etc.) between data points in the lower-dimensional representation.
   * Goal: Reduce dimensionality without losing the geometric structure.

2. **Handles Similarity/Dissimilarity Data**

   * Works with raw dissimilarity matrices (e.g., distances, correlations) instead of direct feature vectors.

3. **Metric and Non-Metric Variants**

   * **Metric MDS**: Preserves actual distances.
   * **Non-Metric MDS**: Preserves the rank order of distances.

4. **Visualization of High-Dimensional Data**

   * Often used to project data into **2D or 3D** for visualization while keeping relationships intact.

5. **Flexible Input**

   * Can be applied to numerical, categorical, or mixed-type datasets (once converted to a distance matrix).

6. **Optimization-based**

   * Finds a configuration of points that minimizes a **stress function**:

     $$
     \text{Stress} = \sqrt{\frac{\sum (d_{ij} - \delta_{ij})^2}{\sum \delta_{ij}^2}}
     $$

     where $d_{ij}$ = distance in reduced space, $\delta_{ij}$ = original dissimilarity.

7. **Interpretation**

   * Points close in reduced space are similar in original space; points far apart are dissimilar.

---

### **Example**

* If customers’ purchase patterns are recorded in 50 dimensions, MDS can map them into **2D** so that similar customers appear close together.

---

### **Diagram:**

```
High-Dimensional Space → Compute Distance Matrix → Optimize Layout → 2D/3D Map
```

---

✅ **Exam Tip:**
For a 7-mark answer:

* Define MDS (1 mark)
* List & explain 5–7 features (5 marks)
* Add a short example/diagram (1 mark)

---

