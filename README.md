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
gray_image = cv2.imread("dala_na.png")
color_image = cv2.imread("smillepathi.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Histogram of Grayscale image and color image
```
import numpy as np
import cv2
Gray_image = cv2.imread("dala_na.png")
Color_image = cv2.imread("smillepathi.jpg")
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
gray_image = cv2.imread("smillepathi.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-03-15 103140](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/a3d45b13-cae1-45ea-996a-78ad14cddd78)


### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2024-03-15 103441](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/c6558eb0-3021-473a-9561-f13d50128439)
![Screenshot 2024-03-15 103448](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/5d3046d7-b355-4e76-a3f3-f54d0a0f45c7)
![Screenshot 2024-03-15 103421](https://github.com/SHARAN-MJ/Histogram-of-an-images/assets/119560305/7cf6e1c7-b854-4a8f-a018-f66e515e892a)




### Histogram Equalization of Grayscale Image.

![Uploading Screenshot 2024-03-15 103558.png…]()


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
