# Gray Level Slicing (Intensity Slicing)

## 📌 Overview

This project demonstrates the concept of **Gray Level Slicing** (or Intensity Slicing), a fundamental technique in digital image processing used to highlight a specific range of gray levels in an image.

By defining a specific intensity window, we can isolate pixels of interest while suppressing the rest. This technique is highly effective for separating specific features from the background, such as enhancing anomalies in X-ray images or highlighting water masses in satellite imagery.

---

## 🎯 Aim

To implement and visualize **Gray Level Slicing** on an image, extracting a target intensity range and generating two distinct variations: one that preserves the original background textures and another that entirely binarizes the target region.

---

## 🛠️ Technologies Used

* **Python**
* **OpenCV (`cv2`)**
* **NumPy**
* **Matplotlib**

---

## 📚 Theory

Gray level slicing highlights a specific band of intensities in an image. There are two primary variations of this transformation:

### 1. Slicing Without Background
This approach highlights the intensity range of interest by forcing it to a constant bright value (e.g., `255`) and turning all other out-of-range intensities to black (`0`). It effectively creates a binary mask of the target region.

### 2. Slicing With Background
This approach preserves the original pixel values within the target intensity range while turning all other pixel values to black (`0`). This maintains the texture and gradient detail of the highlighted region while removing distractions from the rest of the image.

---

## ⚙️ Working Principle

The image processing is dictated by a minimum intensity threshold (`rmin = 100`) and a maximum intensity threshold (`rmax = 200`).

For every pixel in the grayscale image, the following logic is applied:

* **If the pixel falls within the range (`100 <= pixel_value <= 200`)**:
  * For *Slice Without Background*: The pixel is set to `255` (White).
  * For *Slice With Background*: The pixel retains its original value.
* **If the pixel falls outside the range**:
  * For both variations, the pixel is set to `0` (Black).

---

## 🔄 Implementation Steps

### 1. Load the Images
The input image (`images3.jpg`) is loaded in both grayscale and original color formats using OpenCV.
```python
img = cv2.imread("/content/images3.jpg",0)
original_color_img_for_display = cv2.imread("/content/images3.jpg")
