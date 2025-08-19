**examples of geometric models** 

---

## ✅ 1. **k-Nearest Neighbors (k-NN)**

### 📌 What it is:

A very simple model that **classifies** a data point based on the **closest points around it**.

### 🧠 Key idea:

> "You are most likely to be similar to your neighbors."

### 🧾 How it works (step by step):

1. A new point appears.
2. The model looks at the **k closest points** to it (k is a number you choose, like 3 or 5).
3. It **counts** which class is most common among those neighbors.
4. It assigns the new point to that class.

### 📊 Example:

* You want to predict if a fruit is an apple or orange.
* The 3 closest fruits are: apple, apple, orange.
* Majority is apple → predict **apple**.

✅ Used for classification, simple to understand, no training step!

---

## ✅ 2. **Support Vector Machine (SVM)**

### 📌 What it is:

A model that finds the **best possible boundary** between classes.

### 🧠 Key idea:

> "Let’s draw a line (or plane) that not only separates the classes, but **does it with the most space between them**."

### 🧾 How it works:

1. Plots all points in space.
2. Finds the **line or hyperplane** that separates the classes.
3. Chooses the one with the **largest margin** (gap) between the two classes.
4. Uses this line to classify new points.

### 📊 Example:

Imagine cats and dogs on a graph — SVM draws a line between them so that it's **as far away as possible from both groups**.

✅ Very powerful for classification, works well even in high-dimensional space.

---

## ✅ 3. **Clustering Algorithm: k-Means**

### 📌 What it is:

An **unsupervised** learning algorithm that **groups data into clusters**.

### 🧠 Key idea:

> "Let’s find k group centers (means), and assign points to the nearest center."

### 🧾 How it works:

1. Choose the number of clusters (k).
2. Randomly place k “centers” in space.
3. Assign each point to the nearest center.
4. Move the centers to the **average** of their assigned points.
5. Repeat steps 3–4 until everything stops changing.

### 📊 Example:

You give customer data with no labels. k-Means might group them into:

* Low spenders
* Medium spenders
* High spenders

✅ Used for grouping, pattern discovery, market segmentation, etc.

---

## 🔁 Quick Summary Table

| Algorithm   | Type           | What it does                                         |
| ----------- | -------------- | ---------------------------------------------------- |
| **k-NN**    | Classification | Looks at nearest neighbors and picks majority class  |
| **SVM**     | Classification | Finds the best boundary (hyperplane) between classes |
| **k-Means** | Clustering     | Groups data into k clusters based on similarity      |

---
