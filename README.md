# PixelCraftCV

# Image Handling & Pixel Transformations using OpenCV

## Overview
This project demonstrates fundamental image processing operations using **OpenCV in Python**.  
It covers image loading, display, brightness and contrast adjustments, cropping, resizing, bitwise operations, and color channel manipulation.

---

## Objective
To implement and understand basic image processing techniques such as:
- Reading and displaying images
- Adjusting brightness and contrast
- Cropping specific regions from images
- Performing bitwise operations
- Splitting color channels
- Resizing images

---

## Tools & Technologies
- **Python 3.7**
- **OpenCV (cv2)**
- **NumPy**
- **Matplotlib**
- **Jupyter Notebook**

---

## Implementation Steps

### 1️⃣ Read and Display Image
- Load an image using OpenCV
- Convert BGR → RGB for proper display
- Display using Matplotlib
Code:
```
plt.imshow(real_color)

plt.title("Original Color Image")
plt.axis('on')
plt.show()
```
<img width="610" height="497" alt="image" src="https://github.com/user-attachments/assets/15602df9-e712-4055-b5a5-dd8b85b07321" />

---

### 2️⃣ Brightness Adjustment
- Create a matrix of ones
- Add matrix → Brighter image
- Subtract matrix → Darker image

Code:
```
plt.figure(figsize=(20,10))
plt.subplot(141)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original"); plt.axis('off')

plt.subplot(142)
plt.imshow(cv2.cvtColor(img_darker, cv2.COLOR_BGR2RGB))
plt.title("Darker"); plt.axis('off')

plt.subplot(143)
plt.imshow(cv2.cvtColor(img_brighter, cv2.COLOR_BGR2RGB))
plt.title("Brighter"); plt.axis('off')
plt.show()
```
<img width="1211" height="323" alt="image" src="https://github.com/user-attachments/assets/4a73a745-dd80-43dc-87a6-4ec921fac30b" />

---

### 3️⃣ Contrast Modification
- Apply scaling factors (1.1, 1.2)
- Generate higher contrast images
- Display results without overflow correction
Code:
```
plt.figure(figsize=(20,10))
plt.subplot(1,3,1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original"); plt.axis('off')

plt.subplot(1,3,2)
plt.imshow(cv2.cvtColor(img_higher1, cv2.COLOR_BGR2RGB))
plt.title("Contrast 1.1"); plt.axis('off')

plt.subplot(1,3,3)
plt.imshow(cv2.cvtColor(img_higher2, cv2.COLOR_BGR2RGB))
plt.title("Contrast 1.2"); plt.axis('off')
plt.show()
```
<img width="1204" height="316" alt="image" src="https://github.com/user-attachments/assets/d02eae2e-76b9-4a51-80f2-63c45854de30" />

---

### 4️⃣ Image Cropping
- Extract a specific region (object) from the image
- Example:
  ```python
  cropped = img[20:420, 210:540]

Code:
```
import cv2

img = cv2.imread('Eagle_in_Flight.jpg')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)

cropped = img_rgb[20:420, 210:540]

plt.imshow(cropped)
plt.title("Cropped Image")
plt.axis('on')
plt.show()
```

<img width="425" height="499" alt="image" src="https://github.com/user-attachments/assets/c03a2e1b-969e-442a-95db-1491b1ebba91" />

---

## Output
The program produces:
- Original image display
- Brightness-adjusted images (brighter & darker)
- Contrast-enhanced images
- Image generated using bitwise operations
- Individual B, G, R channel views

---

## Result
Successfully implemented image processing techniques including reading, displaying, brightness and contrast adjustment, bitwise operations, and channel splitting using OpenCV in Python.
