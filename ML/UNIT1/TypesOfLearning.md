

---

## **1. Supervised Learning**

**Definition:**
A learning method where a model is trained using a **labeled dataset** containing input–output pairs, so it learns the mapping function **f(X) → Y**.

---

### **Key Characteristics**

* **Data:** Labeled (features + target)
* **Goal:** Predict output for unseen data
* **Feedback:** Direct — model learns from correct labels
* **Examples:** Regression (continuous output), Classification (categorical output)

---

### **Working Principle (Step-by-Step)**

1. Provide dataset with **features (X)** and **labels (Y)**
2. Split into training and test sets
3. Train model on training data
4. Validate on test data and adjust parameters
5. Use model for predictions

---

### **Diagram**

```
[Input Features + Labels] → [Model Training] → [Prediction for New Data]
```

---

### **Common Algorithms**

* Linear Regression
* Logistic Regression
* Decision Trees
* Support Vector Machines (SVM)
* Neural Networks

---

### **Real-world Examples**

* Email spam detection
* Predicting house prices
* Disease diagnosis from patient data

---

### **Code Snippet**

```python
from sklearn.linear_model import LinearRegression
model = LinearRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)
```

---

---

## **2. Unsupervised Learning**

**Definition:**
A learning method where a model is trained on an **unlabeled dataset** to find hidden patterns, structures, or groupings in the data.

---

### **Key Characteristics**

* **Data:** Unlabeled (only features)
* **Goal:** Discover patterns, group similar data, reduce dimensionality
* **Feedback:** Indirect — no true output given
* **Tasks:** Clustering, Association, Dimensionality reduction

---

### **Working Principle (Step-by-Step)**

1. Provide dataset with **only input features**
2. Model groups data or finds structure based on similarity/distance
3. Output is clusters, patterns, or reduced dimensions

---

### **Diagram**

```
[Input Data (No Labels)] → [Model] → [Clusters / Patterns]
```

---

### **Common Algorithms**

* K-Means Clustering
* Hierarchical Clustering
* DBSCAN
* PCA (Principal Component Analysis)

---

### **Real-world Examples**

* Customer segmentation in marketing
* Grouping news articles by topic
* Anomaly detection in networks

---

### **Code Snippet**

```python
from sklearn.cluster import KMeans
kmeans = KMeans(n_clusters=3)
kmeans.fit(X)
clusters = kmeans.labels_
```

---

---

## **3. Semi-Supervised Learning**

**Definition:**
A learning method that uses a **small amount of labeled data** along with a **large amount of unlabeled data** to improve model accuracy.

---

### **Key Characteristics**

* **Data:** Few labeled + many unlabeled samples
* **Goal:** Reduce labeling cost while improving performance
* **Feedback:** Partial — labels for some data only
* **Use Case:** When labeling is expensive/time-consuming

---

### **Working Principle (Step-by-Step)**

1. Train initial model on **labeled data**
2. Predict labels for **unlabeled data** (pseudo-labeling)
3. Retrain model with both real and pseudo-labeled data
4. Repeat until accuracy improves

---

### **Diagram**

```
[Labeled Data] + [Unlabeled Data] → [Model] → [Better Predictions]
```

---

### **Common Algorithms**

* Self-training
* Co-training
* Graph-based semi-supervised learning
* Semi-supervised SVM

---

### **Real-world Examples**

* Medical diagnosis with few labeled cases and many unlabeled records
* Speech recognition with few labeled audio clips
* Fraud detection with limited confirmed fraud cases

---

### **Code Snippet (Pseudo-code)**

```python
model.fit(labeled_X, labeled_y)
pseudo_labels = model.predict(unlabeled_X)
model.fit(np.vstack([labeled_X, unlabeled_X]),
          np.hstack([labeled_y, pseudo_labels]))
```




---

## **4. Reinforcement Learning (RL)**

**Definition:**
A learning paradigm where an **agent** learns to make decisions by interacting with an **environment**, receiving **rewards** or **penalties** based on its actions, and aiming to maximize cumulative reward over time.

---

### **Key Characteristics**

* **Agent**: Learner/decision maker
* **Environment**: The world in which the agent acts
* **State (S)**: Current situation of the agent
* **Action (A)**: Choices available to the agent
* **Reward (R)**: Feedback signal from the environment
* **Policy (π)**: Strategy that defines the agent’s action in each state
* **Goal**: Maximize cumulative reward (return)

---

### **Working Principle (Step-by-Step)**

1. Agent observes **current state (S)**
2. Agent selects **action (A)** based on its policy
3. Environment transitions to a **new state (S')**
4. Environment gives a **reward (R)**
5. Agent updates its policy using this feedback
6. Process repeats until a stopping condition is met

---

### **Diagram**

```
   ┌─────────────┐        Action (A)        ┌─────────────┐
   │             │ ───────────────────────> │             │
   │   Agent     │                          │ Environment │
   │             │ <─────────────────────── │             │
   └─────────────┘     Reward (R), State(S) └─────────────┘
```

---

### **Types of RL**

1. **Positive RL** – Adding a reward to increase frequency of good behavior
2. **Negative RL** – Removing an unfavorable condition to encourage behavior

---

### **Common Algorithms**

* **Model-free**: Q-Learning, SARSA
* **Model-based**: Dyna-Q
* **Deep RL**: Deep Q-Networks (DQN), Policy Gradients

---

### **Real-world Examples**

* **Game AI**: AlphaGo beating human champions
* **Robotics**: Robot arm learning to pick and place objects
* **Self-driving Cars**: Learning lane following and obstacle avoidance

---

### **Code Snippet (Q-Learning Example)**

```python
import numpy as np

Q = np.zeros((state_count, action_count))
for episode in range(episodes):
    state = env.reset()
    done = False
    while not done:
        action = np.argmax(Q[state] + np.random.randn(1, action_count) * 0.01)  # Exploration
        new_state, reward, done, _ = env.step(action)
        Q[state, action] += alpha * (reward + gamma * np.max(Q[new_state]) - Q[state, action])
        state = new_state
```

---

### **Comparison with Other Learning Types**

| Feature  | Supervised          | Unsupervised      | Reinforcement                          |
| -------- | ------------------- | ----------------- | -------------------------------------- |
| Data     | Labeled             | Unlabeled         | No fixed dataset; feedback via rewards |
| Goal     | Predict output      | Find structure    | Learn optimal policy                   |
| Feedback | Known correct label | No feedback       | Reward/Penalty signal                  |
| Example  | Spam classification | Customer grouping | Game-playing AI                        |

---

**Exam Tip:**
Always **mention agent–environment loop**, **reward concept**, and **a real-world example**. Use a **diagram** for full marks.

---



