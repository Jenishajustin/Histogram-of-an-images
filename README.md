# EXP-3 Histogram of an images
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

### Developed By: J.JENISHA
### Register Number: 212222230056

<table>
  <tr>
    <td width=50%>
      
####  Histogram of Gray scale image and Color image  
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("gray.png")
re = cv2.resize(gray_image,(400,300))
color_image = cv2.imread("Color1.jpg",-1)
cv2.imshow("Gray Image",re)
cv2.imwrite("gray.jpg",re)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
</td>
<td>
  
## Output:
#### Input Grayscale Image and Color Image
![Screenshot 2024-03-17 113107](https://github.com/Jenishajustin/Histogram-of-an-images/assets/119405070/d774eacf-3acb-486f-b420-ff7a82e39231)

![Screenshot 2024-03-17 113124](https://github.com/Jenishajustin/Histogram-of-an-images/assets/119405070/27b6383c-56ec-4376-b774-362954df009f)

</td>
</tr>



<tr>
  <td width=50%>

#### Histogram of Grayscale image and any color image
```python
import numpy as np
import cv2
Gray_image = cv2.imread("gray.png")
Color_image = cv2.imread("Color1.jpg")
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
</td>
<td>

## Output:
#### Histogram of Grayscale image and any color image
##### Grayscale image
![Screenshot 2024-03-17 112259](https://github.com/Jenishajustin/Histogram-of-an-images/assets/119405070/7954cc3f-af27-454f-9f91-48336cfdee6c)

##### Color image
![Screenshot 2024-03-17 112314](https://github.com/Jenishajustin/Histogram-of-an-images/assets/119405070/458b7dd5-293f-456a-9e7c-dfb68d7b8de7)

</td>
</tr>



<tr>
  <td width=50%>

#### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("gray.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
## Output:
#### Histogram Equalization of Grayscale Image.
![Screenshot 2024-03-17 113341](https://github.com/Jenishajustin/Histogram-of-an-images/assets/119405070/c6308564-eb4f-4831-9ff2-9a013f7e6bcf)

![Screenshot 2024-03-17 113351](https://github.com/Jenishajustin/Histogram-of-an-images/assets/119405070/b4d3010d-eabc-44bc-bbac-e62c3e6d069b)

</td>
</tr>
</table>





## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
