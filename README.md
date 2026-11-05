## Record-Edge-Detection-Using-OpenCV

## Aim:

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

## Software Required:

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## Algorithm:

## Step 1:
Import all the necessary modules for the program.

## Step 2:
Load an image using cv2.imread().

## Step 3:
Convert the image to grayscale.

## Step 4:
Apply Sobel operator using OpenCV to detect edges.

## Step 5:
Apply Prewitt operator using custom kernels.

## Step 6:
Apply Roberts operator using custom kernels.

## Step 7:
Apply Laplacian operator using OpenCV.

## Step 8:
Apply Canny edge detector using OpenCV.

## Step 9:
Display all edge-detected images for comparison.

## Program :

## Developed By: Syed Shamsheer Ali .B

## Register Number: 212225220114

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread(r'C:\Users\syedf\OneDrive\Documents\DIPT\Syed1.png')
plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

```
img = cv2.imread(r'C:\Users\syedf\OneDrive\Documents\DIPT\Syed1.png')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
sx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
sy = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5)
sobel = cv2.magnitude(sx, sy)
plt.figure(figsize=(4, 8))
plt.imshow(sobel, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.tight_layout()
plt.show()
```

```
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
laplacian = cv2.Laplacian(gray, cv2.CV_64F)
plt.imshow(abs(laplacian), cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.tight_layout()
plt.show()
```

```
gray_image = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.figure(figsize=(12, 8))
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.tight_layout()
plt.show()
```

## Output:

## Original Image:

<img width="302" height="403" alt="image" src="https://github.com/user-attachments/assets/c0f209a5-f1d6-4788-8211-df15e212d3da" />

## Sobel Edge Detector:

* Detects edges in horizontal and vertical directions.
* Produces gradient-based edge map.

## Prewitt Edge Detector:

* Similar to Sobel but simpler kernel.
* Detects directional edges.

## Roberts Edge Detector:

* Detects edges using diagonal gradients.
* Sensitive to noise.

## Sobel Edge Detection:

<img width="477" height="635" alt="image" src="https://github.com/user-attachments/assets/841c8104-db0e-4e6e-8ee0-fcb5a934683b" />

## Laplacian Edge Detector:

* Detects edges using second-order derivatives.
* Highlights rapid intensity changes.

## Laplacian Edge Detection:

<img width="426" height="582" alt="image" src="https://github.com/user-attachments/assets/81fa4cc4-4c59-48ff-b156-7cd870bb3d01" />

## Canny Edge Detector:

* Multi-stage edge detection.
* Produces clean and thin edges.

## Canny Edge Detection:

<img width="478" height="627" alt="image" src="https://github.com/user-attachments/assets/075f1098-8ab5-4b36-a841-6cda11ca3c92" />

## Result:

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
