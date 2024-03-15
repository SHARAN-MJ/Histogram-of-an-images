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
# Developed By: SHARAN MJ
# Register Number: 212222240097
```
# Grayscale image and Color image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("anil.png")
color_image = cv2.imread("dala.png",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("anil.png")
Color_image = cv2.imread("dala.png")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
# Histogram equalization of Grayscale image
```
import cv2
gray_image = cv2.imread("dala.png",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image
![Screenshot 2024-03-15 094758](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/aaca5a5b-b01d-420b-b1ae-6097233b5d1b)
![Screenshot 2024-03-15 094822](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/3ec9ffff-65c4-4c87-96b0-4135ac682400)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-15 100833](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/eb051d2e-64c9-42cf-8d91-1dfcd9aa1e2e)
![Screenshot 2024-03-15 100633](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/b2d09568-f630-47f7-9ef4-06ce0f67ab5e)
![Screenshot 2024-03-15 100656](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/d4fce2dd-33e6-434b-b630-18a77d11851c)
![Screenshot 2024-03-15 100711](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/a0966061-6cef-40fe-9a39-7c5679c5a061)



### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-15 101014](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/e9be8a28-a055-4fa2-b03c-6f18cf8b2df3)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
