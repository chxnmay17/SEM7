

---

## **Different Data Formats in Machine Learning**

Machine Learning models require input data in a structured and interpretable format.
Common data formats can be classified into **structured, unstructured, and semi-structured**.

---

### **1. Structured Data**

* **Definition**: Data stored in tabular form with rows (records) and columns (features).
* **Formats**:

  * **CSV (Comma-Separated Values)**

    * Simple text format with comma-separated entries.
    * Example:

      ```
      Age, Salary, Department
      25, 40000, IT
      30, 50000, HR
      ```
    * Pros: Easy to read, supported by all ML libraries (e.g., Pandas).
    * Cons: No data types or metadata.
  * **TSV (Tab-Separated Values)** – similar to CSV but uses tabs.
  * **XLS/XLSX** – Excel files, support formulas and multiple sheets.

**Diagram:**

| Feature  | Age | Salary | Dept |
| -------- | --- | ------ | ---- |
| Record 1 | 25  | 40000  | IT   |
| Record 2 | 30  | 50000  | HR   |

---

### **2. Unstructured Data**

* **Definition**: Data without a predefined structure; needs preprocessing before ML.
* **Types & Formats**:

  * **Text**: `.txt`, `.pdf`, `.docx` – e.g., sentiment analysis from customer reviews.
  * **Images**: `.jpg`, `.png`, `.bmp` – used in CNNs for image recognition.
  * **Audio**: `.wav`, `.mp3` – used in speech recognition models.
  * **Video**: `.mp4`, `.avi` – used in action recognition, video analytics.

---

### **3. Semi-Structured Data**

* **Definition**: Data not in strict tabular form but has some organizational structure (tags, keys).
* **Formats**:

  * **JSON (JavaScript Object Notation)**

    * Lightweight, human-readable key-value pairs.
    * Example:

      ```json
      {"Name": "John", "Age": 25, "Skills": ["Python", "ML"]}
      ```
    * Pros: Flexible, widely used in APIs.
  * **XML (eXtensible Markup Language)** – hierarchical data with tags.
  * **YAML** – human-friendly configuration data format.

---

### **4. Specialized ML Data Formats**

* **TFRecord** (TensorFlow) – binary format optimized for TensorFlow models.
* **.npy / .npz** – NumPy binary formats for fast loading of large arrays.
* **HDF5** – hierarchical format for storing large datasets (e.g., deep learning weights).

---

### **Real-world Example**

* Image Classification Pipeline: `.jpg` images → converted to NumPy arrays (`.npy`) → stored in TFRecord for TensorFlow training.
* NLP Pipeline: `.txt` reviews → converted to tokenized sequences → stored in CSV for training.

---

### **Summary Table**

| Category        | Examples             | Use in ML                   |
| --------------- | -------------------- | --------------------------- |
| Structured      | CSV, XLSX, TSV       | Tabular datasets            |
| Unstructured    | JPG, MP3, MP4, TXT   | Image, audio, text analysis |
| Semi-Structured | JSON, XML, YAML      | API data, logs              |
| Specialized ML  | TFRecord, .npy, HDF5 | Fast training data loading  |

---

✅ **Exam Tip**: Always mention **definition + examples + ML use case** for each format. This ensures full marks in a short-answer question.

---
