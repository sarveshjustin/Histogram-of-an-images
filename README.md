# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: sarvesh s
# Register Number: 212222230135
import cv2
from matplotlib import pyplot as plt
# Load the color image
image = cv2.imread('spideriamge.jpeg')
# Convert the image to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(gray_image, cmap='gray')
plt.title('Original Grayscale Image')
plt.axis('off')
hist_original = cv2.calcHist([gray_image], [0], None, [256], [0, 256])
plt.plot(hist_original, color='black')
plt.title('Original Histogram')
plt.xlim([0, 256])
# Apply histogram equalization
equalized_image = cv2.equalizeHist(gray_image)
plt.imshow(equalized_image, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')
hist_equalized = cv2.calcHist([equalized_image], [0], None, [256], [0, 256])
plt.plot(hist_equalized, color='black')
plt.title('Equalized Histogram')
plt.xlim([0, 256])







```
## Output:
![image](https://github.com/user-attachments/assets/fbbc0cd6-7e08-42c2-a9ee-b6aa65b75c65)
![image](https://github.com/user-attachments/assets/00e3f83f-9daa-4e38-9b58-0c056f3c3a6a)
![image](https://github.com/user-attachments/assets/3adb1ff7-6279-463c-b23b-163a447b8d80)
![image](https://github.com/user-attachments/assets/4db4fd7c-b346-46b6-b82f-d1f81a15cd5e)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
V.
