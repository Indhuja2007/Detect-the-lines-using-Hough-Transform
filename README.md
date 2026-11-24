#  Lane Detection

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

## Learning Objective

* Understand each stage of image processing
* Learn how to build a complete computer vision pipeline
* Practice writing code in guided sections

**Important Instruction:**
👉 Write code **ONLY in places marked as `# Your Code Here`**
👉 Do NOT modify any other part of the code

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm & Explanation

---

###  Step 1: Import Libraries

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

---

###  Step 2: Read the Image

```python
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```

---

###  Step 3: Convert to Grayscale

```python
plt.imshow(gray, cmap="gray")
plt.title("Grayscale Image")
plt.axis("off")
plt.show()
```

---

###  Step 4: Display Images

```python
plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(gray, cmap="gray")
plt.title("Grayscale Image")
plt.axis("off")

plt.show()
```

---

###  Step 5: Thresholding

```python
plt.imshow(thresh, cmap="gray")
plt.title("Thresholded Image")
plt.axis("off")
plt.show()
```

---

###  Step 6: Region of Interest (ROI)

```python
plt.imshow(cv2.cvtColor(roi, cv2.COLOR_BGR2RGB))
plt.title("ROI Masked Image")
plt.axis("off")
plt.show()
```

---

### Step 7: Edge Detection (Canny)

```python
plt.imshow(edges, cmap="gray")
plt.title("Edge Detected Image")
plt.axis("off")
plt.show()
```

---

###  Step 8: Gaussian Blur

```python
plt.imshow(blurred, cmap="gray")
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

---

###  Step 9: Hough Transform

```python
line_image = image.copy()

if lines is not None:
    for line in lines:
        x1, y1, x2, y2 = np.array(line).flatten()[:4]
        cv2.line(line_image, (x1, y1), (x2, y2), (0, 255, 0), 3)

plt.imshow(cv2.cvtColor(line_image, cv2.COLOR_BGR2RGB))
plt.title("Detected Lines")
plt.axis("off")
plt.show()
```

---

### Step 10: Lane Detection Logic

```python
final_image = image.copy()

if lines is not None:
    for line in lines:
        x1, y1, x2, y2 = np.array(line).flatten()[:4]
        cv2.line(final_image, (x1, y1), (x2, y2), (0, 255, 0), 3)

plt.figure(figsize=(10, 5))
plt.imshow(cv2.cvtColor(final_image, cv2.COLOR_BGR2RGB))
plt.title("Final Lane Detection Output")
plt.axis("off")
plt.show()
```

---

##  Expected Output

* Original image

  <img width="637" height="395" alt="image" src="https://github.com/user-attachments/assets/14b53539-7af0-4127-9cba-12b7d8219cad" />

* Grayscale image

  <img width="641" height="397" alt="image" src="https://github.com/user-attachments/assets/662efb12-3eed-42d3-96c6-8ed3ca9d8675" />

* Thresholded image

  <img width="645" height="398" alt="image" src="https://github.com/user-attachments/assets/2ada8600-bed7-440b-93d4-dfb98a190911" />

* ROI masked image

  <img width="632" height="396" alt="image" src="https://github.com/user-attachments/assets/0941c922-a2d0-4d1c-8452-98219e5f71d7" />

* Edge detected image

  <img width="637" height="385" alt="image" src="https://github.com/user-attachments/assets/9f982a41-0aff-4a3d-acf4-5330d2d6821b" />

* Smoothed image

  <img width="641" height="392" alt="image" src="https://github.com/user-attachments/assets/38f11c23-50fb-4261-b239-2878f2e36b97" />

* Detected lines

  <img width="638" height="393" alt="image" src="https://github.com/user-attachments/assets/33a2b028-3593-4794-94d9-3c442a6163e5" />

* Final lane detection output

  <img width="867" height="536" alt="image" src="https://github.com/user-attachments/assets/d5ade676-2d5a-416a-9abc-47613245925e" />


---

##  Instructions

* Fill ONLY in `# Your Code Here` sections
* Do NOT change existing code
* Run step-by-step
* Verify outputs

---

## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---

##  Developed By

* **Name: INDHUJA.K** 
* **Register No: 212225040133** 
