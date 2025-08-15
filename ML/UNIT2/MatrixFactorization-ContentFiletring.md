
---

## **Matrix Factorization**

**Definition:**
Matrix factorization is a technique used in **recommendation systems** to decompose a large **user–item interaction matrix** into the product of two smaller matrices, representing **latent factors** of users and items.

**Purpose:**

* Discover hidden relationships between users and items
* Reduce dimensionality and fill in missing ratings

**Mathematical Form:**
If $R$ is the user–item rating matrix:

$$
R \approx P \times Q^T
$$

Where:

* $P$ → User-feature matrix (user latent factors)
* $Q$ → Item-feature matrix (item latent factors)
* Predicted rating:

  <img width="166" height="48" alt="image" src="https://github.com/user-attachments/assets/d70e5b82-bb02-4e6e-a257-0451593a059a" />


**Example:**
If User A likes "Action" and "Comedy", and Movie X is "Action", the model predicts a high rating.

---

## **Content-Based Filtering**

**Definition:**
A recommendation method that suggests items **similar to those the user has liked in the past**, based on **item features** rather than other users’ preferences.

**Key Steps:**

1. **Profile Creation** – Build a user profile using the features of liked items.
2. **Similarity Measurement** – Compare items to the profile using similarity metrics (e.g., cosine similarity, Euclidean distance).
3. **Recommendation** – Suggest items with highest similarity scores.

**Example:**

* User watches *Inception* (Features: Sci-Fi, Thriller, Director = Christopher Nolan).
* System recommends other Sci-Fi thrillers, especially Nolan movies.

**Mathematical Representation (Cosine Similarity):**

<img width="258" height="82" alt="image" src="https://github.com/user-attachments/assets/aff71244-da70-41e6-be9f-6641de68bbb1" />


---

### **Diagram:**

```
User’s Liked Items → Extract Features → Build Profile → Find Similar Items → Recommend
```

---

### **Advantages**

* No cold-start problem for items (new items can be recommended if features are known)
* Personalized recommendations

### **Limitations**

* Limited to known features; cannot suggest entirely new types of items
* Narrow recommendations (less diversity)

---

✅ **Exam Tip:**
For 7 marks:

* Define matrix factorization (1 mark) + formula/example (2 marks)
* Define content-based filtering (1 mark) + working steps (2 marks) + example/diagram (1 mark)

---


