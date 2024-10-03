# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### Developed By: KEERTHI VASAN A
### Reg.No: 212222240048
```
import cv2
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('Tiger.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![{87D9BE69-886B-4984-A154-A2CE98C3A87B}](https://github.com/user-attachments/assets/7b29871d-f588-4133-9910-9b04b371b906)

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![{3314ECF9-CE52-47DD-B279-8AF10D5BA843}](https://github.com/user-attachments/assets/468c35c1-f2dc-45c1-8c1f-bd0a46aeb38f)
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
![{740BD0BB-A014-4344-8C17-73215A42356B}](https://github.com/user-attachments/assets/881423b0-3f54-46ab-b1c2-11d7e9e86024)
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
![{0DA4FB09-6AA7-4922-BC66-283CA33A8C8B}](https://github.com/user-attachments/assets/a4af101d-f607-46e0-98d4-a4e5cbab4bee)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
