

---

# Local Binary Pattern (LBP) Feature Extraction

### Definition

* **Local Binary Pattern (LBP)** is a **texture feature extraction technique** used in image processing and computer vision.
* It captures **local texture patterns** by comparing each pixel with its neighboring pixels.

---

### Working Principle

1. **Neighborhood Comparison**

   * For each pixel, take the **3×3 neighborhood**.
   * Compare each neighbor with the center pixel.
2. **Binary Encoding**

   * If neighbor ≥ center pixel → assign **1**, else assign **0**.
3. **Form a Binary Number**

   * Read binary digits in a fixed order (e.g., clockwise).
   * Convert this binary code into a **decimal number** → LBP value.
4. **Feature Representation**

   * Replace the center pixel with its LBP value.
   * Build a **histogram of LBP values** over the whole image → used as texture feature.

---

### Example

**Step-by-step on a 3×3 patch**

```
Neighborhood pixels:          Thresholding (center=50):
  45  55  60                   0   1   1
  30  50  65        --->       0   C   1
  25  40  70                   0   0   1
```

* Binary pattern (clockwise from top-left): **01110001**
* Decimal value = **113** → LBP code for center pixel.

---

### Diagram (conceptual)

```
 Original Image Patch        Binary Pattern → Decimal
      [3x3]                    LBP value (Feature)
```

---

### Applications

* **Face Recognition** – captures fine facial texture details.
* **Texture Classification** – fabric analysis, material recognition.
* **Medical Imaging** – detecting tissue patterns in scans.
* **Object Detection** – background subtraction and image retrieval.

---

### Advantages

* **Simple & efficient** (fast computation).
* **Rotation & grayscale invariant** (robust to lighting changes).
* Compact representation of local texture.

### Limitations

* Sensitive to **noise** in flat regions.
* Works only for **micro-texture patterns**.

---

✅ **Exam Tip Mnemonic – “C-B-H-A”**

* **C**ompare neighbors
* **B**inary encode
* **H**istogram of features
* **A**pply in recognition

---


