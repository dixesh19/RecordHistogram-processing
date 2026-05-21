# Histogram Equalization Using OpenCV (Grayscale & Color Images)

---

## Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

- Read and display a grayscale image  
- Plot histogram of the grayscale image  
- Apply histogram equalization on grayscale image  
- Read and display a color image  
- Plot histogram of B, G, R channels  
- Convert image to HSV color space  
- Apply histogram equalization on the Value (V) channel  
- Convert the enhanced image back to BGR format  
- Display original and enhanced images with histograms  

---

## Software Used

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (`cv2`)  
- NumPy  
- Matplotlib  

---

## Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the image `parrot.jpg` in grayscale format.

### Step 3:
Display the grayscale image and plot its histogram.

### Step 4:
Apply histogram equalization using `cv2.equalizeHist()` to enhance contrast.

### Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

### Step 6:
Read the same image in color format.

### Step 7:
Split the image into B, G, R channels and plot their histograms.

### Step 8:
Convert the image from BGR to HSV color space.

### Step 9:
Apply histogram equalization on the V (Value) channel.

### Step 10:
Merge the channels and convert the image back to BGR format.

### Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

---

## Program

### Developed By:
### Name: DINESH R
### Register No: 212224240037
```
i) original grayscale image
!pip install opencv-python
import cv2
from matplotlib import pyplot as plt

image = cv2.imread("C:\\Users\\Downloads\\parrot.jpg")

gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')

 ii)Color Image Histogram Equalization

hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])

plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])


iii)  equalized image
equalized_image = cv2.equalizeHist(gray_image)

plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')


iv) equalized histogram
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])


plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])
```

---

##  Output

<img width="746" height="546" alt="image" src="https://github.com/user-attachments/assets/14a319b1-b61c-442e-9d3d-9230eda7ba4c" />

### Grayscale Histogram Equalization

- Original grayscale image is displayed  
- Histogram of original grayscale image is plotted  
- Enhanced image after histogram equalization is displayed  
- Histogram of enhanced grayscale image shows improved contrast
<img width="799" height="615" alt="image" src="https://github.com/user-attachments/assets/7185690c-b609-47b9-b945-9fd5a5740049" />

### Equalized image 

<img width="709" height="536" alt="image" src="https://github.com/user-attachments/assets/0f998e5b-c671-4f78-a852-fed6737b3156" />


### Color Image Histogram Equalization

- Original color image is displayed  
- Histogram of B, G, R channels is plotted  
- Enhanced image after HSV-based equalization is displayed
- Histogram of enhanced image shows better intensity distribution
  
<img width="792" height="610" alt="image" src="https://github.com/user-attachments/assets/6d363915-571d-40e9-b149-80ac0832eb9c" />

---

## Result

Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.
